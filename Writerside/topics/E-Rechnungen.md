# WHMCS Lexware Office Modul

Das WHMCS Lexware Office Modul ermöglicht die Integration von Rechnungen aus WHMCS in Lexoffice. Dabei wird ein Problem deutlich, das durch die unterschiedliche Handhabung von Netto- und Bruttopreisen in WHMCS und Lexoffice entsteht.

## Problemstellung

WHMCS erlaubt global nur die Einstellung von **Netto- oder Bruttopreisen**.
Das bedeutet, dass entweder alle Rechnungen auf Basis von Nettopreisen (zzgl. Mehrwertsteuer) oder auf Basis von Bruttopreisen (inkl. Mehrwertsteuer) erstellt werden.

Das WHMCS hier nur Netto oder Brutto vorsieht, widerspricht den Anforderungen:

- **Privatkunden (B2C)** Rechnungen auf Basis von Bruttopreisen erstellt werden (Preis inklusive Mehrwertsteuer).
- **Geschäftskunden (B2B)** Rechnungen auf Basis von Nettopreisen erstellt werden (Preis exklusive Mehrwertsteuer).

Da viele Hosting-Anbieter in WHMCS für Transparenz und Benutzerfreundlichkeit Bruttopreise verwenden, ergibt sich ein Konflikt bei der Integration mit Lexoffice.

## Anforderungen von Lexoffice

Lexoffice setzt für die Erstellung von E-Rechnungen voraus, dass Rechnungen im **Netto-Rechenverfahren** erstellt werden. Lexoffice erklärt hierzu:

> Wechseln Sie auf Netto-Rechnung. Das Format der E-Rechnung unterstützt nur das Netto-Rechenverfahren. Um Abweichungen bei der Verwendung des Brutto-Rechenverfahrens zu vermeiden, muss bei der Erstellung von Rechnungen in Lexware Office der Schalter "Netto" verwendet werden:
>
> Quelle: [Lexoffice Support - Checkliste Erstellung von E-Rechnungen](https://support.lexoffice.de/de-form/articles/9800578-checkliste-erstellung-von-e-rechnungen#h_ae082b3116)

## Das konkrete Problem

Durch die Nutzung von Bruttopreisen in WHMCS und die notwendige Umstellung auf Nettopreise für Geschäftskunden in Lexoffice treten **Rundungsdifferenzen** auf. Diese ergeben sich aus dem kaufmännischen Runden, das Lexoffice beim Konvertieren der Preise vornimmt.

### Beispiel für Rundungsdifferenzen

1. In WHMCS wird ein Produkt für **10,99 € (Bruttopreis)** angeboten.
2. Lexoffice wandelt diesen Bruttopreis in einen Nettopreis um, z. B. **9,24 €** (bei 19 % MwSt.).
3. Lexoffice rechnet nun **9,24 * 1,19**, der Betrag ist dann **10,9956**. Es wird auf **11,00 €** aufgerundet.

Das führt dazu, dass die ursprüngliche Rechnung in WHMCS mit einem Bruttopreis von 10,99 € nicht mehr exakt mit der Rechnung in Lexoffice übereinstimmt. In der Praxis kann das bedeuten:

- Der Kunde bezahlt nur 10,99 € (laut WHMCS-Rechnung).
- In Lexoffice wird ein Betrag von 11,00 € ausgewiesen.
- Der verbleibende Cent führt zu Buchhaltungsproblemen und unnötigen Mehraufwänden.

## Lösung des Problems

Um das Problem zu beheben, wird nach der Übermittlung an Lexware Office auf Rundungsdifferenzen geprüft.
Falls eine Rundungsdifferenz festgestellt wird, wird die erste Rechnungsposition auf der WHMCS-Rechnung angepasst, um diese Differenz auszugleichen.

### Anpassung der Produktpreise

Diese Anpassung führt zwangsläufig dazu, dass sich der Rechnungsbetrag um einen Cent ändert.
Dies könnte zu Problemen bei der Bestellung führen. Daher empfehlen wir, die Produktpreise entsprechend zu gestalten, um Rundungsdifferenzen vorzubeugen.
Zum Beispiel:

- Statt **10,99 €** sollte der Produktpreis auf **11,00 €** oder **10,98** angepasst werden.

Durch diese Maßnahme kann sichergestellt werden, dass keine Differenzen zwischen WHMCS und Lexoffice entstehen und der Buchhaltungsprozess reibungslos funktioniert.

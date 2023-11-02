# Updateverlauf

Die letzte version des lexoffice WHMCS Moduls können Sie in Ihrem [Kundencenter](https://portal.becker-software.de)
unter "Downloads" abrufen.

## Version 3.1.8 {collapsible="true"}

**Fehlerbehebungen**

- Behebung eines Fehlers, welcher dafür gesorgt, hat das, bei manchen WHMCS Instanzen die lexoffice PDF nicht geladen
  wird.

## Version 3.1.7 {collapsible="true"}

- Erkennung von weiteren Sprachpaketen ausser "german", alle Sprachparkete die mit german beginnen werden als deutsch
  erkannt. Beispiel: german-informal

## Version 3.1.5 {collapsible="true"}

- Korrigierte Anzeige von Sonderzeichen im Firmennamen.

## Version 3.1.1 {collapsible="true"}

**Major Release!**

- Integration als lexoffice Partner
- Custom field für die lexoffice Kundennummer

> **Hinweis:** Nach der Installation der neuen Version, stellen Sie sicher Sie ein neues Feld anlegen für die
> Kundennummer und in den Moduleinstellungen zuweisen.
> {style: warning}

## Version 2.2.4 {collapsible="true"}

- Bitte beachten Sie das, ggf. die Einstellungen neu übernommen werden müssen. Insbesondere der API Schlüssel.

## Version 2.1.11 {collapsible="true"}

- Der Import von Rechnungen bei EU Kunden hat zu einem Fehler geführt.
- Rechnungen, die durch einen Cronjob ausgeführt worden sind, wurden nicht importiert.
- Rechnungsemails wurden nicht beim Cron erstellten Rechnungen versendet, da Lexoffice die Rechnung nicht rechtzeitig
  importierten konnte. Die Rechnung wird zusätzlich bei
  Rechnungsversand zu Lexoffice hochgeladen, dadurch kann der Rechnungsversand 2-4 Sekunden länger dauern.

## Version 2.1.6 {collapsible="true"}

- Mehrzeilige Rechnungen werden jetzt auch in lexoffice als Name und Beschreibung übertragen. Dabei ist
  immer die erste Zeile der Produktname und alle folgenden Zeilen die Beschreibung.
- Fehler beim Erstellen von Kontakten behoben
- Automatische Zeichenlimitierung für Produktnamen eingeführt

## Version 2.1.5 {collapsible="true"}

- Behebung von einem Fehler der zur Erstellung eines neuen Kontaktes geführt hat bei jedem neuen Beleg.

## Version 2.1.4 {collapsible="true"}

- Unterstützung von PHP 8.1

## Version 2.1.3 {collapsible="true"}

- Fehlerbehebung bei der Verwendung von mehreren Custom Fields.

## Version 2.1.2 {collapsible="true"}

- Fehlerbehebungen beim Rendering von Rechnungen

## Version 2.1.1 {collapsible="true"}

- Fehlerbehebungen

## Version 2.1.0 {collapsible="true"}

- Release
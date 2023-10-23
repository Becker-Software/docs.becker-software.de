# Konfiguration

## Historische Rechnungen

Wenn Sie wünschen die alten Rechnungen **nicht** in sevDesk importiert werden, so können Sie dies in den
Moduleinstellungen festlegen.

Die Einstellung `Rechnungssynchronisierung ab` bestimmt, ab welchem Datum (einschließlich) keine Rechnungen mehr
importiert werden sollen. Alle Rechnungen vor dem angegebenen Datum werden **nicht** importiert.

> Achten Sie auf die korrekte Formatierung des Datums. Das Datum muss im Format `dd-mm-yyyy` angegeben werden.
> Z.B. `26-12-2022`
> {style: note}

Wünschen Sie z.B. das nur Rechnungen ab dem 26.12.2022 erstellt werden, so tragen Sie in dieses Feld `26-12-2022` ein
und
Speichern Sie Ihre Einstellungen. Alle Rechnungen bis zum 25.12.2022 werden dann noch über WHMCS ausgeliefert und nicht
importiert.

## Moduleinstellungen

### Lizenzschlüssel

Um das Modul nutzen zu können, ist es erforderlich, dass Sie eine gültige Lizenz besitzen. Diese Lizenz können Sie über
im Kundenportal unter https://portal.becker-software.de abrufen und muss in den Einstellungen des Moduls hinterlegt
werden, bevor Sie es nutzen können.

Bitte beachten Sie, dass das Modul ohne eine gültige Lizenz deaktiviert wird und
somit nicht verwendet, werden kann. Sollten Sie Probleme mit der Lizenzierung haben, wenden Sie sich bitte an unseren
Support unter info@becker-software.de.

### Rechnungssynchronisation ab

> Bitte stellen Sie sicher das in Ihrem Theme ordner die invoicepdf-fallback.tpl vorhanden ist.
> {style: info}

Die Einstellung `Rechnungssynchronisierung ab` bestimmt, ab welchem Datum (einschließlich) keine Rechnungen mehr
importiert werden sollen. Alle Rechnungen vor dem angegebenen Datum werden mithilfe des WHMCS Rechnungstemplates
ausgeliefert.

### Zahlungsstatus

Diese Einstellung bestimmt, ob nur vollständig bezahlte Rechnungen zu sevDesk Importiert werden sollen.

### sevDesk Custom Field

Um das Modul nutzen zu können, muss das "sevDesk Custom Field" in den Einstellungen konfiguriert werden. Dafür muss
zunächst ein Custom Field in WHMCS erstellt werden, welches anschließend in den Modul-Einstellungen ausgewählt und
gespeichert werden muss.

### Konto DE

Das Konto DE wird für alle Rechnungen verwendet, die in Deutschland erstellt wurden.

### Konto EU B2B

Das Konto EU B2B wird für alle Rechnungen verwendet, die in der EU erstellt wurden und eine gültige Umsatzsteuer-ID im
Kundencenter hinterlegt haben.

### Konto EU B2C

Das Konto EU B2C wird für alle Rechnungen verwendet, die in der EU erstellt wurden und keine gültige Umsatzsteuer-ID im
Kundencenter hinterlegt haben.

### Konto Drittland

Das Konto Drittland wird für alle Rechnungen verwendet, die außerhalb der EU erstellt wurden.
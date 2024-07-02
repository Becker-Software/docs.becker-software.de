> Verfügbar ab Version 3.4.0
{style="warning"}

# Variablen

Das Modul erlaubt die Verwendung von Variablen in den Zahlungstext, Rechnungseinleitung sowie dem Rechnungsschlussatz.
Die Variablen werden durch den gleichen Parser wie in WHMCS verarbeitet und funktionen aus den WHMCS Modulen können
ebenfalls verwendet werden.

## Client ($client.x)

| Variable                              | Datentyp      | Beispielwert                         | Beschreibung                                                            |
|---------------------------------------|---------------|--------------------------------------|-------------------------------------------------------------------------|
| {$client.userid}                      | Integer       | 1                                    | Die eindeutige ID des Kunden.                                           |
| {$client.client_id}                   | Integer       | 1                                    | Die ID des Kunden, üblicherweise identisch mit userid.                  |
| {$client.id}                          | Integer       | 1                                    | Die ID des Kunden, ebenfalls identisch mit userid.                      |
| {$client.owner_user_id}               | Integer       | 1                                    | Die ID des Benutzers, dem der Kunde gehört.                             |
| {$client.uuid}                        | String        | 301fcb00-25cc-41ec-876a-594fe5003390 | Universally Unique Identifier (UUID) des Kunden.                        |
| {$client.firstname}                   | String        | Max                                  | Vorname des Kunden.                                                     |
| {$client.lastname}                    | String        | Mustermann                           | Nachname des Kunden.                                                    |
| {$client.fullname}                    | String        | Max Mustermann                       | Vollständiger Name des Kunden.                                          |
| {$client.companyname}                 | String        |                                      | Firmenname des Kunden, falls vorhanden.                                 |
| {$client.email}                       | String        | test@example.local                   | E-Mail-Adresse des Kunden.                                              |
| {$client.address1}                    | String        | Beispielstraße 15                    | Adresse Zeile 1 des Kunden.                                             |
| {$client.address2}                    | String        |                                      | Adresse Zeile 2 des Kunden, falls vorhanden.                            |
| {$client.city}                        | String        | Musterstadt                          | Stadt des Kunden.                                                       |
| {$client.fullstate}                   | String        | Florida                              | Bundesland des Kunden.                                                  |
| {$client.state}                       | String        | FL                                   | Bundesland des Kunden, abgekürzt.                                       |
| {$client.postcode}                    | String        | 12345                                | Postleitzahl des Kunden.                                                |
| {$client.countrycode}                 | String        | DE                                   | Ländercode des Kunden (ISO 3166-1 alpha-2).                             |
| {$client.country}                     | String        | DE                                   | Land des Kunden (ISO 3166-1 alpha-2).                                   |
| {$client.phonenumber}                 | String        |                                      | Telefonnummer des Kunden.                                               |
| {$client.tax_id}                      | String        |                                      | Steuer-ID des Kunden, falls vorhanden.                                  |
| {$client.email_preferences.general}   | String        | 1                                    | E-Mail-Präferenz für allgemeine Benachrichtigungen.                     |
| {$client.email_preferences.invoice}   | String        | 1                                    | E-Mail-Präferenz für Rechnungen.                                        |
| {$client.email_preferences.support}   | String        | 1                                    | E-Mail-Präferenz für Support.                                           |
| {$client.email_preferences.product}   | String        | 1                                    | E-Mail-Präferenz für Produktinformationen.                              |
| {$client.email_preferences.domain}    | String        | 1                                    | E-Mail-Präferenz für Domaininformationen.                               |
| {$client.email_preferences.affiliate} | String        | 1                                    | E-Mail-Präferenz für Affiliate-Programme.                               |
| {$client.statecode}                   | String        | FL                                   | Abkürzung des Bundeslandes des Kunden.                                  |
| {$client.countryname}                 | String        | Germany                              | Name des Landes des Kunden.                                             |
| {$client.phonecc}                     | Integer       | 49                                   | Ländervorwahl der Telefonnummer des Kunden.                             |
| {$client.phonenumberformatted}        | String        |                                      | Formatierte Telefonnummer des Kunden.                                   |
| {$client.telephoneNumber}             | String        |                                      | Telefonnummer des Kunden.                                               |
| {$client.billingcid}                  | Integer       | 0                                    | ID der zugehörigen Rechnungsadresse, falls vorhanden.                   |
| {$client.notes}                       | String        |                                      | Notizen zum Kunden.                                                     |
| {$client.currency}                    | Integer       | 1                                    | ID der Währung des Kunden.                                              |
| {$client.defaultgateway}              | String        |                                      | Standard-Zahlungsgateway des Kunden.                                    |
| {$client.cctype}                      | String        | null                                 | Kreditkartentyp des Kunden, falls vorhanden.                            |
| {$client.cclastfour}                  | String        | null                                 | Letzten vier Ziffern der Kreditkarte des Kunden, falls vorhanden.       |
| {$client.gatewayid}                   | String        | null                                 | ID des Zahlungsgateways des Kunden.                                     |
| {$client.groupid}                     | Integer       | 0                                    | Gruppen-ID des Kunden, falls vorhanden.                                 |
| {$client.status}                      | String        | Inactive                             | Status des Kundenkontos.                                                |
| {$client.credit}                      | String        | 0.00                                 | Guthaben des Kunden.                                                    |
| {$client.taxexempt}                   | Boolean       | false                                | Steuerbefreiung des Kunden (true oder false).                           |
| {$client.latefeeoveride}              | Boolean       | false                                | Überschreibt die Standard-Mahngebühreneinstellungen (true oder false).  |
| {$client.overideduenotices}           | Boolean       | false                                | Überschreibt die Standard-Fälligkeitshinweise (true oder false).        |
| {$client.separateinvoices}            | Boolean       | false                                | Separate Rechnungen für den Kunden (true oder false).                   |
| {$client.disableautocc}               | Boolean       | false                                | Automatische Kreditkartenzahlungen deaktivieren (true oder false).      |
| {$client.emailoptout}                 | Boolean       | true                                 | Kunde hat sich von E-Mail-Benachrichtigungen abgemeldet.                |
| {$client.marketing_emails_opt_in}     | Boolean       | false                                | Kunde hat sich für Marketing-E-Mails angemeldet.                        |
| {$client.overrideautoclose}           | Boolean       | false                                | Überschreibt die automatische Schließung von Tickets (true oder false). |
| {$client.allowSingleSignOn}           | Boolean       | 1                                    | Einmalanmeldung erlauben (1 oder 0).                                    |
| {$client.email_verified}              | Boolean       | false                                | E-Mail-Adresse des Kunden verifiziert (true oder false).                |
| {$client.language}                    | String        | german                               | Bevorzugte Sprache des Kunden.                                          |
| {$client.isOptedInToMarketingEmails}  | Boolean       | false                                | Kunde hat sich für Marketing-E-Mails angemeldet.                        |
| {$client.tax_state}                   | String        | Florida                              | Steuerrelevantes Bundesland des Kunden.                                 |
| {$client.tax_countrycode}             | String        | DE                                   | Steuerrelevantes Land des Kunden (ISO 3166-1 alpha-2).                  |
| {$client.lastlogin}                   | String / Date | No Login Logged                      | Letzter Login des Kunden.                                               |
| {$client.customfields1}               | String        |                                      | Benutzerdefiniertes Feld 1.                                             |
| {$client.customfields[0].id}          | Integer       | 5                                    | ID des benutzerdefinierten Feldes 1.                                    |
| {$client.customfields[0].value}       | String        |                                      | Wert des benutzerdefinierten Feldes 1.                                  |
| {$client.customfields[1].id}          | Integer       | 25                                   | ID des benutzerdefinierten Feldes 2.                                    |
| {$client.customfields[1].value}       | String        |                                      | Wert des benutzerdefinierten Feldes 2.                                  |
| {$client.customfields[2].id}          | Integer       | 26                                   | ID des benutzerdefinierten Feldes 3.                                    |
| {$client.customfields[2].value}       | String        |                                      | Wert des benutzerdefinierten Feldes 3.                                  |
| {$client.customfields[3].id}          | Integer       | 27                                   | ID des benutzerdefinierten Feldes 4.                                    |
| {$client.customfields[3].value}       | String        | 8d8c101d-eab7-4fb4-81cb-e0e5b28585c4 | Wert des benutzerdefinierten Feldes 4.                                  |
| {$client.customfields[4].id}          | Integer       | 28                                   | ID des benutzerdefinierten Feldes 5.                                    |
| {$client.customfields[4].value}       | String        | 10001                                | Wert des benutzerdefinierten Feldes 5.                                  |
| {$client.customfields[5].id}          | Integer       | 29                                   | ID des benutzerdefinierten Feldes 6.                                    |
| {$client.customfields[5].value}       | String        |                                      | Wert des benutzerdefinierten Feldes 6.                                  |
| {$client.customfields0}               | String        |                                      | Benutzerdefiniertes Feld 1.                                             |
| {$client.customfields1}               | String        |                                      | Benutzerdefiniertes Feld 2.                                             |
| {$client.customfields2}               | String        |                                      | Benutzerdefiniertes Feld 2.                                             |
| {$client.customfields3}               | String        |                                      | Benutzerdefiniertes Feld 3.                                             |
| {$client.customfields4}               | String        | 8d8c101d-eab7-4fb4-81cb-e0e5b28585c4 | Benutzerdefiniertes Feld 4.                                             |
| {$client.customfields5}               | String        | 10001                                | Benutzerdefiniertes Feld 5.                                             |
| {$client.customfields6}               | String        |                                      | Benutzerdefiniertes Feld 6.                                             |

## Invoice ($invoice.X)

| Variable                               | Datentyp                | Beispielwert        | Beschreibung                                                     |
|----------------------------------------|-------------------------|---------------------|------------------------------------------------------------------|
| `{$invoice.invoiceid}`                 | Integer                 | 727                 | Die eindeutige WHMCS System ID der Rechnung.                     |
| `{$invoice.userid}`                    | Integer                 | 12                  | Die WHMCS ID des Kunden, dem die Rechnung gehört.                |
| `{$invoice.date}`                      | String (Datum)          | 2024-06-28          | Erstellungsdatum der Rechnung.                                   |
| `{$invoice.duedate}`                   | String (Datum)          | 2024-07-12          | Fälligkeitsdatum der Rechnung.                                   |
| `{$invoice.datepaid}`                  | String (Datum und Zeit) | 0000-00-00 00:00:00 | Datum und Uhrzeit der Zahlung, falls bezahlt.                    |
| `{$invoice.lastcaptureattempt}`        | String (Datum und Zeit) | 0000-00-00 00:00:00 | Letzter Zahlungsversuch.                                         |
| `{$invoice.subtotal}`                  | String                  | 0.84                | Zwischensumme der Rechnung vor Steuern und Gutschriften.         |
| `{$invoice.credit}`                    | String                  | 0.00                | Angewendete Gutschrift auf die Rechnung.                         |
| `{$invoice.tax}`                       | String                  | 0.16                | Erster Steuerbetrag der Rechnung.                                |
| `{$invoice.tax2}`                      | String                  | 0.00                | Zweiter Steuerbetrag der Rechnung, falls vorhanden.              |
| `{$invoice.total}`                     | String                  | 1.00                | Gesamtbetrag der Rechnung.                                       |
| `{$invoice.balance}`                   | String                  | 1.00                | Restbetrag der Rechnung.                                         |
| `{$invoice.taxrate}`                   | String                  | 19.000              | Erster Steuersatz der Rechnung.                                  |
| `{$invoice.taxrate2}`                  | String                  | 0.000               | Zweiter Steuersatz der Rechnung, falls vorhanden.                |
| `{$invoice.status}`                    | String                  | Unpaid              | Status der Rechnung (z.B. Unpaid, Paid, Cancelled).              |
| `{$invoice.paymentmethod}`             | String                  | banktransfer        | Zahlungsmethode der Rechnung.                                    |
| `{$invoice.notes}`                     | String                  |                     | Notizen zur Rechnung, falls vorhanden.                           |
| `{$invoice.ccgateway}`                 | Boolean                 | false               | Gibt an, ob ein Kreditkartengateway verwendet wird.              |
| `{$invoice.items[0].item.id}`          | Integer                 | 700                 | ID des ersten Rechnungspostens.                                  |
| `{$invoice.items[0].item.type}`        | String                  |                     | Typ des ersten Rechnungspostens.                                 |
| `{$invoice.items[0].item.relid}`       | Integer                 | 0                   | Zugehörige ID des ersten Rechnungspostens.                       |
| `{$invoice.items[0].item.description}` | String                  | test                | Beschreibung des ersten Rechnungspostens.                        |
| `{$invoice.items[0].item.amount}`      | String                  | 1.00                | Betrag des ersten Rechnungspostens.                              |
| `{$invoice.items[0].item.taxed}`       | Boolean                 | 1                   | Gibt an, ob der erste Rechnungsposten besteuert wird (1 oder 0). |

## Custom Fields ($customfields.X)

Custom Fields werden als Array übergeben, dabei wird der name des Custom Fields als Key verwendet.
Dem Key werden alle Zeichen bis auf a-z A-Z 0-9 entfernt und in Kleinbuchstaben umgewandelt.

Beispiel

| Name des Custom Fields | Template Variable |
|------------------------|-------------------|
| `Lexoffice ID`       | `{$customfields.lexoffice_id}` |
| `Lexoffice Customer ID`       | `{$customfields.lexoffice_customer_id }` |
| `lexoffice_customer_id`       | `{$customfields.lexoffice_customer_id }` |
| `Geschlecht (optional)`       | `{$customfields.geschlecht_optional}` |

## Sepa Pre-Notification ($sepa_prenotification_X)

> Um die SEPA Vorabinformation zu verwenden, muss ein Custom Field Field mit dem Namen `SEPA Prenotification Days` oder `sepa_prenotification_days` erstellt werden.
> Der Inhalt des Custom Fields muss die Anzahl der Tage enthalten.
> {style="note"}

> Wenn das Custom Field leer oder nicht vorhanden ist, werden 14 Tage verwendet.
> {style="warning"}

| Variable                            | Datentyp                | Beispielwert        | Beschreibung                                          |
|-------------------------------------|-------------------------|---------------------|-------------------------------------------------------|
| `{$sepa_prenotification_date}`      | String (Datum)          | 2024-06-28          | Erstellungsdatum der Rechnung + Prenotificaiton Time  |
| `{$sepa_prenotification_due_date}`  | String (Datum)          | 2024-07-12          | Fälligkeitsdatum der Rechnung + Prenotificaiton Time  |

Die Spezielle Variable `{$sepa_prenotification_date}` oder `{$sepa_prenotification_due_date}` wird verwendet um das Datum der SEPA Vorabinformation zu setzen.
Hierbei handelt es sich um ein Datum, welches in der SEPA Vorabinformation als Datum des Einzugs angegeben wird.

## IF-Abfrage

```smarty
{if $invoice.tax > 0}
    Die Rechnung enthält Steuern.
{else}
    Die Rechnung enthält keine Steuern.
{/if}
```

**Ausgabe**
```text
Die Rechnung enthält Steuern.
```

## Datum Formatieren

Stunden werden mittels Smarty date_format direktives formatiert.

[Zur vollständigen Dokumentation von date_format](https://www.smarty.net/docsv2/de/language.modifier.date.format.tpl)

### 14:33:00
```smarty
{$invoice.date|date_format:"%H:%M:%S"}
```

**Ausgabe**
```text
14:33:00
```

### 28.06.2024
<code-block lang="smarty" ignore-vars="true">
    {$invoice.date|date_format:"%d.%m.%Y"} 
</code-block>

**Ausgabe**
```text
28.06.2024
```
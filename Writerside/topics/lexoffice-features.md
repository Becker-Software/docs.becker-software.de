# Features

Hier finden Sie eine Zusammenfassung der unterstützen Funktionen des Moduls.

## Rechnungsimport

Das Modul unterstützt den automatischen beidseitigen Rechnungsimport von lexoffice zu WHMCS. Das Modul ersetzt die
Erstellung der PDF-Rechnungen, durch die Rechnungen von lexoffice. Damit nutzen Sie Ihre lexoffice Templates direkt in
WHMCS.

## DATEV Export

Mit lexoffice können Sie Ihren Steuerberater direkt einladen. Dieser kann über das Steuerberaterportal bequem Exporte im
DATEV Format herunterladen.

## Kontaktsyncronisation \[Addon\]

Statt bei Rechnungsstellung erfolgt eine zwei Wege Synchronisation. Kunden, die in WHMCS bearbeitet werden, werden
direkt in lexoffice upgedatet und lexoffice Kundenstamm Änderungen direkt in WHMCS.

## Automatische Verbuchung

Ihre Rechnungen werden in lexoffice direkt auf das richtige Buchhaltungskonto gebucht, egal ob Inland,
Innergemeinschaftlich oder International.

## Stornoübertrag

Werden Rechnungen in lexoffice Storniert, so wird die Rechnung in WHMCS ebenfalls storniert, sofern diese noch als
Unbezahlt markiert ist.

## Kontaktsyncronisation

Die Synchronisationsfähigkeiten des WHMCS lexoffice Moduls werden durch bestimmte Einschränkungen der lexoffice API
begrenzt. Sollten bei einem Kunden mehrere Einträge in den oben genannten Kategorien auftreten, wird die
Synchronisierung von WHMCS zu lexoffice für diesen speziellen Kunden unterbrochen. Es ist wichtig zu beachten, dass
Änderungen, die direkt in lexoffice vorgenommen werden, sich weiterhin in WHMCS widerspiegeln.

In Situationen, in denen
es mehrere Einträge gibt, ist das Modul so konfiguriert, dass es automatisch immer den ersten Eintrag auswählt. Dies
stellt sicher, dass trotz der API-Beschränkungen von lexoffice, Datenintegrität und -konsistenz zwischen den beiden
Systemen so gut wie möglich aufrechterhalten werden.
# Umstellung auf den neuen Autorisierungsschlüssel für lexoffice API Nutzer

## Was hat sich geändert?

Bei lexoffice wurde kürzlich eine Ratenlimitierung für die Nutzung der API über Schlüsselauthentifizierung eingeführt.
Um eine optimale Funktionalität und Sicherheit zu gewährleisten, ist es nun erforderlich, dass alle Nutzer ihre
bisherigen API-Schlüssel widerrufen und auf die neue Authentifizierungsmethode umstellen. Diese Anpassung sorgt dafür,
dass Sie nicht von der neuen Rate Limitierung von 2 Sekunden betroffen sind, die bei der Public API eingeführt wurde.

## Schritt-für-Schritt Anleitung zur Umstellung

### Schritt 1: Widerruf des alten API-Schlüssels

1. Loggen Sie sich in Ihr lexoffice Konto ein.
2. Navigieren Sie zum Bereich `Erweiterungen`.
3. Wählen Sie dort `lexoffice Public API`.
4. Finden Sie den zu widerrufenden Schlüssel in der Liste und klicken Sie auf `Widerrufen`.

### Schritt 2: Einrichten des neuen Autorisierungsschlüssels

1. Öffnen Sie Ihr WHMCS Admin Interface
2. Gehen Sie in die Moduleinstellungen des Addons.
3. Klicken Sie auf den Link `Schlüssel abrufen` in den Moduleinstellungen.
4. Melden Sie sich an, falls notwendig.
5. Nach der Anmeldung wird Ihnen ein neuer `Autorisierungsschlüssel` angezeigt.
6. Kopieren Sie diesen Schlüssel.

### Schritt 3: Aktualisierung des Addons

1. Wechseln Sie zurück zum WHMCS Admin Interface.
2. Fügen Sie den kopierten `Autorisierungsschlüssel` in das entsprechende Feld innerhalb der Moduleinstellungen ein.

### Schritt 4: Abschluss der Umstellung

1. Speichern Sie die Änderungen in den Moduleinstellungen Ihres Addons.
2. Überprüfen Sie, ob das Addon korrekt funktioniert, indem Sie eine Testaktion durchführen, wie z.B. das Herunterladen
   eines Belegs.

## Wichtige Hinweise

- Nachdem Sie den alten Schlüssel widerrufen haben, funktionieren alle Dienste, die diesen Schlüssel verwenden, nicht
  mehr. Stellen Sie sicher, dass Sie sofort den neuen Autorisierungsschlüssel einrichten.
- Die Rate Limitierung von 2 Sekunden bedeutet, dass Anfragen an die lexoffice API nur alle 2 Sekunden erfolgen können.
  Planen Sie Ihre Workflows entsprechend, um diese Einschränkung zu berücksichtigen.
- Alle bisher über die Public API hinterlegten Webhooks werden deaktiviert. Sie müssen diese Webhooks erneut
  einrichten, wenn Sie sie weiterhin verwenden möchten.
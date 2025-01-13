# Verlust der Authentifizierung

Lexware Office verwendet für die Authentifizierung OAuth2. Dieser Authentifizierungsmechanismus basiert darauf, dass wir mittels des Authentifizierungstokens, welchen Sie bei der Installation von Lexoffice in unser Addon übertragen, einen Zugangsdatensatz bestehend aus Zugriffs- und Erneuerungstoken erhalten.

Diese beiden Token haben vordefinierte Ablaufdaten:

*   **Zugriffstoken**: Wird für den Zugang auf die Lexoffice API verwendet und ist nur wenige Stunden gültig.

*   **Erneuerungstoken**: Dient ausschließlich dazu, einen neuen Zugangsdatensatz abzurufen, und ist mehrere Tage gültig.


Unser Addon verwaltet die Aktualisierung der Zugangsdaten vollautomatisch und aktualisiert den Zugangsdatensatz in regelmäßigen Abständen, spätestens 15 Minuten vor Ablauf. Dafür ist es allerdings notwendig, dass der Cronjob mindestens minütlich oder höchstens alle 5 Minuten ausgeführt wird.

## Probleme bei der Authentifizierung

Sollte der Cronjob nicht wie vorgesehen ausgeführt werden oder eine andere Störung auftreten, kann es zu einem Verlust der Authentifizierung kommen. In diesem Fall wird unser Addon versuchen, den Zugriffstoken mithilfe des Erneuerungstokens erneut abzurufen. Wenn der Erneuerungstoken jedoch ebenfalls abgelaufen ist, ist eine manuelle Eingabe eines neuen Authentifizierungstokens erforderlich.

### Mögliche Ursachen für den Verlust der Authentifizierung

1.  **Cronjob nicht aktiv**: Der Cronjob wurde deaktiviert oder nicht korrekt konfiguriert.
2.  **Serverprobleme**: Der Server war über einen längeren Zeitraum nicht erreichbar.
3.  **Ungültige Token**: Die Tokens wurden durch Änderungen an den Berechtigungen in Lexoffice ungültig.

### Wiederherstellung der Authentifizierung

1.  Melden Sie sich in Ihrem Lexoffice-Konto an.
2.  Navigieren Sie zu den API-Einstellungen und generieren Sie einen neuen Authentifizierungstoken.
3.  Geben Sie diesen Token in den Einstellungen des Addons ein.
4.  Stellen Sie sicher, dass der Cronjob wie folgt konfiguriert ist:
    *   **Frequenz**: Alle 1 bis 5 Minuten.
    *   **Skript**: Das Skript, das für die Token-Aktualisierung verantwortlich ist, muss korrekt eingebunden sein.

Nach diesen Schritten sollte die Authentifizierung wiederhergestellt sein und die Tokens automatisch aktualisiert werden.

### Zusätzliche Schritte
Nach einem Authentifizierungsverlust ist es erforderlich das hinterlegte Webhooks wieder eingerichtet werden.
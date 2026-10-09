# Game Over Testseite

Eine erfundene Reservierungsseite für Tests des Buchungs-Agenten von Game Over.
Sie ahmt den Ablauf echter Buchungsseiten nach, damit Browser-Skripte geübt werden können, ohne einen echten Anbieter zu belasten.

**Sie speichert nichts und sendet nichts.**
Kein Netzwerkaufruf, kein Cookie, kein lokaler Speicher, keine echte Reservierung.
Eingegebene Daten verlassen den Browser nicht.

Adresse: https://soleilphoenix.github.io/game-over-testseite/

## Ablauf

1. Datum und Personenzahl wählen, "Zeiten anzeigen" drücken.
2. Die Zeiten erscheinen nach rund 400 Millisekunden.
3. Zeit wählen, Name, E-Mail und Telefon eintragen, Bedingungen akzeptieren, "Verbindlich reservieren".
4. Die Bestätigung nennt eine Nummer nach dem Muster `T-<Datum>-<Uhrzeit>-<Personen>`, zum Beispiel `T-20261212-1930-08`.

## Feste Regeln der Seite

- Frei sind 17:00, 18:30 und 19:30 Uhr, 21:00 Uhr ist immer ausgebucht.
- Der 24.12.2026 ist ganz ausgebucht.
- Ab 13 Personen verweist die Seite aufs Telefon.
- Ein Cookie-Hinweis liegt über der Seite, er setzt keine Cookies.

## Varianten

- `?variante=anzahlung` verlangt vor der Buchung eine Kreditkarte für eine Anzahlung. Ein Agent muss dort abbrechen.
- `?variante=fehler` lässt die Buchung nach dem letzten Klick mit einer Fehlermeldung scheitern, ohne Bestätigung.

## Stabile Auswahlpfade

`#datum`, `#personen`, `#zeiten-zeigen`, `#meldung`, `button.zeit[data-zeit]`, `#name`, `#email`, `#telefon`, `#agb`, `#reservieren`, `#formular-meldung`, `#bestaetigung`, `#bestaetigungsnummer`, `#bestaetigung-details`, `#cookie-notwendig`, `#cookie-alle`.

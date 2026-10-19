# Wikirace

Ein Wikipedia-Rennen für mehrere Spieler: Lobby erstellen oder per 4-Buchstaben-Code beitreten, Start- und Zielartikel festlegen und gleichzeitig losrennen. Gespielt wird auf Wikipedia in einem neuen Tab; auf der Seite trägt man jeden besuchten Artikel ein. Die Rangliste zeigt Klicks und Zeit live.

## Hinweis

Die Mehrspieler-Lobbys nutzen die Live-Verbindung von Claude-Artefakten (`window.claude.use("room")`). Außerhalb von Claude (z. B. auf GitHub Pages) lädt die Seite im Einzelspieler-Modus. Für Mehrspieler außerhalb von Claude braucht es ein eigenes Backend (z. B. Firebase oder einen WebSocket-Server).

## Starten

`index.html` im Browser öffnen oder per GitHub Pages veröffentlichen.

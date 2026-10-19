# Wikirace

Ein Wikipedia-Rennen für mehrere Spieler, direkt im Browser.

- Lobby erstellen oder per 4-Buchstaben-Code bzw. Einladungslink beitreten (bis 16 Spieler)
- Die Leitung legt Start- und Zielartikel fest (selbst eingeben, Klassiker oder ganz zufällig) in Deutsch, Englisch, Französisch oder Italienisch
- Alle starten nach einem Countdown gleichzeitig; die Artikel laden direkt auf der Seite, jeder Link-Klick zählt
- Live-Rangliste mit Klicks, Zeit und aktuellem Artikel aller Spieler

## Hosting

Einfach `index.html` per GitHub Pages veröffentlichen: Settings → Pages → Deploy from branch `main` / root.

## Technik

- Kein eigener Server nötig: Die Spieler verbinden sich per WebRTC direkt miteinander ([PeerJS](https://peerjs.com), Vermittlung über den kostenlosen PeerJS-Cloud-Server). Der Browser der Leitung hält den Spielstand.
- Artikel kommen live über die Wikipedia-API.
- Verlässt die Leitung die Seite, endet die Lobby.
- In sehr strengen Netzwerken (manche Firmen- oder Schulnetze) kann die direkte Verbindung scheitern.

# Wikirace

Ein Wikipedia-Rennen für mehrere Spieler, direkt im Browser.

- Lobby erstellen oder per 4-Buchstaben-Code bzw. Einladungslink beitreten (bis 16 Spieler)
- Die Leitung legt Start- und Zielartikel fest (selbst eingeben, Klassiker oder ganz zufällig) in Deutsch, Englisch, Französisch oder Italienisch
- Alle starten nach einem Countdown gleichzeitig; die Artikel laden direkt auf der Seite, jeder Link-Klick zählt
- Live-Rangliste mit Klicks, Zeit und aktuellem Artikel aller Spieler

## Hosting

Einfach `index.html` per GitHub Pages veröffentlichen: Settings → Pages → Deploy from branch `main` / root.

## Technik

- Kein eigener Server nötig: Die Spieler tauschen Nachrichten über einen öffentlichen MQTT-Broker aus ([HiveMQ](https://www.hivemq.com/mqtt/public-mqtt-broker/), per verschlüsseltem WebSocket mit [MQTT.js](https://github.com/mqttjs/MQTT.js)). Das klappt auch zwischen verschiedenen Netzwerken, ohne direkte Verbindung. Der Browser der Leitung hält den Spielstand.
- Artikel kommen live über die Wikipedia-API.
- Verlässt die Leitung die Seite, endet die Lobby.
- Der Broker ist öffentlich, die Nachrichten (Namen, Artikel, Zeiten) sind also nicht privat. Für ein Spiel unter Freunden reicht das.
- Manche sehr strengen Netzwerke (Firmen- oder Schulnetze) sperren den Port 8884; dann klappt die Verbindung dort nicht.

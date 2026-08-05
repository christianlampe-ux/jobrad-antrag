# Briefing: Fortschrittsanzeige

## Ziel

Die Fortschrittsanzeige macht den Stand der Antragsstrecke jederzeit verständlich. Sie zeigt, dass der Antrag aus vier aufeinanderfolgenden Schritten besteht und in welchem Schritt sich die antragstellende Person aktuell befindet.

## Verhalten und Darstellung

- Die Anzeige enthält alle vier Schritte in ihrer festen Reihenfolge.
- Jeder Schritt ist mit einer eindeutigen Bezeichnung und seiner Position gekennzeichnet, zum Beispiel „Schritt 2 von 4“.
- Der aktuelle Schritt wird visuell eindeutig hervorgehoben: Er erhält eine deutlich sichtbare Markierung, eine betonte Beschriftung und ein zusätzliches, nicht farbabhängiges Merkmal wie ein ausgefülltes Symbol, einen Rahmen oder das Präfix „Aktueller Schritt“.
- Bereits abgeschlossene Schritte werden als abgeschlossen gekennzeichnet. Nachfolgende Schritte bleiben als noch nicht begonnen erkennbar.
- Die Markierung des aktuellen Schritts bleibt während der Bearbeitung sichtbar und wird beim Wechsel in den nächsten Schritt aktualisiert.
- Auf kleinen Bildschirmen darf die Anzeige platzsparend dargestellt werden, muss aber weiterhin den aktuellen Schritt sowie die Gesamtzahl der vier Schritte verständlich vermitteln.

## UX-Rationale

Die Fortschrittsanzeige reduziert die Unsicherheit darüber, wo man sich in der Antragsstrecke befindet und was noch vor einem liegt. Das ist besonders relevant im Zusammenhang mit der Research-Erkenntnis aus Issue #12: Testpersonen verlieren in der Antragsstrecke die Orientierung und brechen deshalb ab. Eine jederzeit sichtbare und eindeutig markierte Position stärkt die Orientierung, macht den verbleibenden Aufwand einschätzbar und kann dadurch Abbrüche reduzieren.

## Accessibility

Der aktuelle Schritt muss auch ohne Farbe erkennbar sein. Die Hervorhebung darf daher nicht ausschließlich über eine Farbänderung erfolgen, sondern muss durch Form, Symbol, Text, Gewichtung oder eine Kombination daraus unterstützt werden. Für Screenreader wird der aktuelle Schritt mit `aria-current="step"` ausgezeichnet. Die Reihenfolge der vier Schritte und ihr Status (abgeschlossen, aktuell oder noch nicht begonnen) müssen außerdem programmatisch erfassbar sein.

## Akzeptanzkriterien

- Die vier Schritte sind in ihrer Reihenfolge sichtbar.
- Der aktuelle Schritt ist eindeutig als „Schritt X von 4“ erkennbar.
- Der aktuelle Schritt unterscheidet sich auch bei deaktivierter Farbwahrnehmung eindeutig von den anderen Schritten.
- Der aktuelle Schritt trägt `aria-current="step"`.
- Abgeschlossene und noch nicht begonnene Schritte sind voneinander und vom aktuellen Schritt unterscheidbar.
- Die Anzeige funktioniert verständlich auf Desktop- und Mobilansichten.

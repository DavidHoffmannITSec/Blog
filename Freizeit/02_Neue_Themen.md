
# Projekte mit neuen Themen

Täglich kam ich nach Hause, nicht erschöpft, sondern voller Ideen. Während die Ausbildung im zweiten Jahr langsam in Richtung Prüfungen ging, 
begann für mich nach Feierabend erst das richtige Abenteuer. Die Schule lehrte mich die Theorie. Doch das, was mich wirklich formte, lernte ich zu 
Hause. Projekt für Projekt.

## Webentwicklung

Im zweiten Lehrjahr begann ich, mich intensiv mit Webentwicklung auseinanderzusetzen. Ich wollte nicht einfach nur statische Webseiten bauen, sondern 
richtige Webanwendungen. Ich lernte TypeScript, kombinierte es mit Next.js, HTML und CSS und erstellte meine erste eigene Anwendung. Eine voll funktionsfähige "Pizza Hut Webseite".

Die Idee war einfach, man sollte Pizzen auswählen und bestellen können. Doch ich ging weiter. Ich integrierte eine Datenbank, über die die Bestellungen
verarbeitet wurden, arbeitete an einem ansprechenden Frontend und kümmerte mich sogar um die Sicherheit. Ich informierte mich über SQL-Injection, 
Cross-Site-Scripting (XSS) und implementierte Gegenmaßnahmen.
Dabei stieß ich zum ersten Mal auf Begriffe wie **OWASP Top 10**. Und was als "ich will einfach nur eine Webseite bauen" begann, wurde schnell zu einer Leidenschaft für IT-Sicherheit. Ich durchforstete YouTube, Reddit, Stackoverflow, Blogs und Foren und sog alles auf, was mit Pentesting und Web-Schwachstellen zu tun hatte. Ich wollte wissen, wie Angriffe funktionieren und wie man sich davor schützt.

Ich testete meine eigene Seite, fand Lücken, schloss sie wieder. Mir fehlte zwar damals noch die tiefe Expertise, um wie ein Profi zu testen, aber die Grundsteine waren gelegt.

## Der Sudoku-Solver 

Einige Zeit später packte mich eine neue Idee: Ein **Sudoku-Solver**. Ich war gut in Sudoku und wollte wissen wie schwer kann das sein?

Also schnappte ich mir mein Whiteboard, zeichnete ein paar Ideen auf und fing an zu planen. Ich entwickelte ein GUI in Python, programmierte einen
**Backtracking-Algorithmus**, um fehlende Zahlen zu berechnen, und schaffte es, dass mein Programm sogar Fehler im Sudoku erkennen konnte zum Beispiel, wenn es mathematisch gar nicht lösbar war.

Das alleine war schon cool, aber es reichte mir nicht.

Ich fragte mich: "Wie kann ich das Ding online nutzen auf Seiten wie sudoku.com?"
Also begann ich zu tüfteln. Zuerst dachte ich daran, die Zahlen manuell einzugeben. Dann entdeckte ich im Netzwerk-Tab der Entwicklerkonsole einen POST-Request mit einem Key, der das Sudoku-Muster enthielt. Ich nutzte diesen Key in meiner Anwendung und konnte damit das Sudoku automatisch befüllen und lösen lassen.

Doch ich ging noch einen Schritt weiter.

Ich wollte, dass mein Tool Screenshots analysieren kann, ohne dass ich überhaupt Zahlen eingeben muss. Also begann ich, mich mit **OCR (Optical Character Recognition)** auseinanderzusetzen. Anfangs klappte nichts. Falsche Erkennungen, unklare Zahlen, fehlende Felder. Doch ich blieb 1,5 Monate lang dran.
Ich probierte verschiedene Bibliotheken, passte Parameter an, trainierte Schriftmodelle bis es endlich funktionierte.

Mein Sudoku-Solver konnte:
- Ein Sudoku anhand eines Screenshots erkennen  
- Die Zahlen per **OCR** extrahieren  
- Das Rätsel lösen  
- Es **automatisch** Feld für Feld im Browser auf sudoku.com eintragen

Es war mein erstes großes Projekt, bei dem ich Technologien nutzte, die ich nicht in der Ausbildung gelernt hatte. Ich kombinierte Python, GUI,
Algorithmen, Webautomation und Bildverarbeitung und bewies mir selbst "Ich kann mehr, als ich dachte".

## Kleine Projekte, große Wirkung

Zwischen diesen Meilensteinen baute ich weitere kleinere Projekte. Webseiten, Tools, Skripte, oft einfach aus Neugier oder weil ich eine bestimmte 
Idee hatte. Sie waren nicht alle groß, aber sie hatten eins gemeinsam: Sie brachten mich weiter.

Jedes dieser Projekte lehrte mich, Unbekanntes zu erforschen, neue Technologien selbstständig zu verstehen und mich an Herausforderungen zu wagen, 
vor denen ich früher vielleicht zurückgeschreckt wäre.

---

## Fazit: Lernen beginnt da, wo der Lehrplan aufhört

Diese Jahre haben mir gezeigt, dass die Ausbildung wichtig war, aber das, was ich außerhalb des Unterrichts gelernt habe, war genauso entscheidend.

Durch meine eigenen Projekte lernte ich, eigenständig zu denken und Probleme kreativ zu lösen, mich in neue Themen wie Websicherheit, OCR und Automatisierung einzuarbeiten und wie viel Spaß ich daran habe, Dinge zu verstehen und umzusetzen
Ob Pizza-Webseite, Sudoku-Solver, Scripte oder einfache Algorithmen, jedes Projekt war ein Schritt auf meinem Weg zum Entwickler. 

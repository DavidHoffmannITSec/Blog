# ZUGFeRD

Nach meinem ersten großen Projekt, der interaktiven Fahrzeugkarte, ging es bei Minova für mich direkt spannend weiter. Ich war nun im vierten 
Monat als Entwickler im Team, und langsam fühlte ich mich angekommen. Mein Code wurde produktiv eingesetzt, ich kannte die Abläufe im 
Unternehmen, und vor allem war ich bereit für das nächste große Thema.
Dieses Thema hieß **ZUGFeRD**.

## Was ist ZUGFeRD überhaupt?

ZUGFeRD (Zentraler User Guide des Forums elektronische Rechnung Deutschland) ist ein Standard für elektronische Rechnungen. Im Kern handelt es
sich dabei um eine **hybride PDF-Rechnung**, die neben der sichtbaren Darstellung auch strukturierte XML-Daten enthält, standardisiert und 
ideal für die automatische Weiterverarbeitung in ERP-Systemen.

Ziel des Standards: Rechnungen, die sowohl Menschen als auch Maschinen verstehen können, ohne dass man zwei Dokumente pflegen muss.
Und genau das wollten wir bei Minova umsetzen.

## Die Ausgangslage: Rechnungen mit Zukunft

Bisher wurden unsere Rechnungen bei Minova klassisch als PDFs erzeugt, also ohne eingebettete Metadaten, ohne Struktur. Sie sahen gut aus, 
funktionierten für Kunden, aber waren für automatisierte Verarbeitung nur eingeschränkt nutzbar.

Unser Ziel: Sobald eine Rechnung erzeugt wird, sollte sie automatisch ZUGFeRD-konforme Metadaten enthalten. Das bedeutet, dass im Hintergrund 
alle relevanten Daten, wie Rechnungsnummer, Beträge, Positionen, Steuern, als XML eingebettet werden sollen. Unsichtbar für den Endnutzer, 
aber Gold wert für automatisierte Prozesse auf Kundenseite.

## Woche 1: Eintauchen in die Welt von ZUGFeRD

In der ersten Woche machten wir, ein kleines Team aus drei Entwicklern, genau das, was gute Entwickler eben tun, recherchieren, lesen, 
ausprobieren. ZUGFeRD klang auf den ersten Blick simpel („PDF + XML“), aber die technischen und formalen Anforderungen hatten es in sich.
Wir studierten die offiziellen Spezifikationen, luden uns Beispielrechnungen herunter, analysierten die unterschiedlichen Versionen 
(ZUGFeRD 1.0, 2.0, 2.1...) und verstanden schnell: Es geht nicht nur darum, ein XML an ein PDF anzuhängen. Es geht um Struktur, Validierung, 
Konformität und eine saubere Einbettung im richtigen Format. Das Ganze soll ja später maschinenlesbar sein.
Wir sprachen über Profile wie EN 16931, diskutierten über Rechnungspositionen, UBL vs. CII, und irgendwann war kam der Punkt, an dem wir 
loslegen konnten.

## Woche 2–3: Von der Theorie in den Code

Die erste Implementierung war eine Art „Proof of Concept“. Wir bauten einen PDF-Prototyp mit eingebetteter XML-Datei welches manuell erstellt und 
über ein kleines Tool injiziert wurde. Dann testeten wir das PDF mit offiziellen Validatoren. Fehler über Fehler. Mal war das XML nicht korrekt 
eingebettet, mal fehlte die notwendige MIME-Kennung. Dann wieder akzeptierte der Viewer das Format, aber unser Code zum Einbetten war zu 
unsauber.

Also gingen wir tiefer.
Wir entwickelten in Java eine Funktion, die beim Erstellen der Rechnung im System automatisch die XML-Metadaten nach ZUGFeRD-Standard generiert.
Dabei achteten wir auf Felder wie:

- Käufer/Verkäufer
- Rechnungspositionen
- Gesamtbeträge, Steuern
- Währung, Datum, UID-Nummern

Diese XML-Struktur wurde dann direkt in das PDF als Anhang eingebettet, genau wie es ZUGFeRD verlangt.
Wir testeten die PDF-Dateien mit dem offiziellen ZUGFeRD-Validator und endlich kamen wir dem Ziel näher. Die Dateien waren nicht nur valide, 
sie ließen sich auch in verschiedenen ERP-Systemen fehlerfrei auslesen. Es funktionierte.

## Woche 4–6: Der Sprung in die Produktion

Nachdem der Prototyp stand, kam der spannende Teil, die Integration in das Produktivsystem.
Wir banden unseren ZUGFeRD-Code in die bestehende Rechnungserstellungslogik ein, wo die Rechnungen generiert, gespeichert und verschickt wurden.
Das bedeutete, dass jeder Rechnungslauf, der ab jetzt durchgeführt wurde, im Hintergrund eine vollständig strukturierte XML-Komponente enthielt.
Natürlich testeten wir viel. Nicht jede Rechnung hatte die gleichen Felder. Manche hatten Rabatte, andere mehrere Steuersätze, wieder andere 
Sonderfälle. Wir mussten viele Varianten abdecken, doch mit jeder Iteration wurde der Code robuster.

Nach einigen Wochen haben wir es endlich geschafft. ZUGFeRD war implementiert und die Rechnungen enthielten Metadaten, die automatisch verarbeitet
werden können.

## Fazit: Mehr als nur PDF

Die Arbeit an ZUGFeRD war für mich ein Augenöffner. Ich hatte zuvor nie bewusst mit hybriden Dateiformaten gearbeitet. Noch nie war mir so 
deutlich geworden, wie wichtig Standards in der digitalen Kommunikation sind und wie kompliziert es sein kann, diese korrekt umzusetzen.

Ich lernte in dieser Zeit, wie wichtig Teamarbeit ist, gerade bei neuen Themen. Wie viel Zeit es kostet, sich wirklich in ein Format wie ZUGFeRD 
einzuarbeiten und wie erleichternd es ist, wenn am Ende eine automatisch erzeugte Rechnung **valide**, **konform** und **nutzbar** ist.

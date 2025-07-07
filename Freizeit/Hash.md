# Ein eigener Hashalgorithmus

Nach meiner Ausbildung zum Fachinformatiker für Anwendungsentwicklung begann für mich ein neuer Lebensabschnitt. Ich war frisch im Berufsalltag angekommen,
die Routinen stellten sich langsam ein, aber in meinem Kopf war bereits wieder Platz für neue Ideen. Ich wollte wieder etwas Eigenes schaffen. 
Etwas, das mich fordert, überfordert, begeistert und weiterbringt.
Und dann kam mir der Gedanke WWarum nicht einen eigenen Hashalgorithmus bauen?"

## Der Einstieg in die Welt der Kryptografie

Zuvor hatte ich Passwörter klassisch mit bekannten Verfahren wie **Argon2** gespeichert, sicher, effizient und etabliert. Aber ich wollte mehr. 
Ich wollte verstehen, wie Kryptografie funktioniert. Nicht nur anwenden, sondern begreifen, wie aus ein paar mathematischen Operationen ein sicherer 
Hash entsteht. Ich konnte einfach nicht begreifen, wie man einen Algorithmus schreiben kann, der fest integriert ist, jedoch nicht umkehrbar ist.

Also begann ich zu recherchieren. Eine Woche lang „studierte“ ich die Theorie hinter Hashfunktionen. Ich wollte wissen wie Kompressionsfunktionen funktionieren,
warum Padding wichtig ist, was Salt ist, was S-Boxen und P-Boxen sind und wieso sie zu Diffusion und Verwirrung führen. Ich tauchte tief in die Details von 
**SHA-256**, **SHA-512** und **Argon2** ein und begann, mein eigenes Design zu entwerfen.

## Der Entwurf von DavoHash512

Ich setzte mir das Ziel, einen Algorithmus zu entwickeln, der:
- nicht trivial rückrechenbar ist
- eine starke Avalanche-Wirkung zeigt
- interessante kryptografische Ideen kombiniert
- einen 512-Bit-Hashwert erzeugt

### 🔹 Die S-Box: Verwirrung durch Chaos

Eine meiner ersten Designentscheidungen war, eine eigene S-Box zu erstellen, also eine Tabelle zur Substitution von Eingabewerten, die aus eigentlich 
einfachen Bytes hochkomplexe Muster erzeugt. Ich füllte sie mit einer Mischung aus extremen, zufälligen und bewusst chaotischen Werten, um möglichst 
viel Unvorhersehbarkeit zu erzeugen.

### 🔹 Die P-Box: Ordnung durch Mathematik

Bei der P-Box, also der Permutation der Bits, entschied ich mich für eine selbst definierte Reihenfolge, inspiriert von mathematischen Konstanten 
wie **π, e** und dem **goldenen Schnitt**. Mein Ziel war, systematische, aber schwer vorhersagbare Verschiebungen zu erzeugen.

### 🔹 Die Rundenstruktur

Der Hashprozess selbst läuft in mehreren **Runden** ab, bei denen der interne Zustand wieder und wieder transformiert wird. Ich setzte bewusst auf 
**Avalanche-Effekte**. Bereits ein einziges geändertes Zeichen im Input sollte den gesamten Hash vollständig verändern. Um das zu erreichen, 
verwendete ich zahlreiche **Bitoperationen, Rotationen, XORs und mehr**, die ich über Wochen hinweg iterativ anpasste.

### 🔹 Die Finalisierungsphase

Besonders stolz bin ich auf die Finalisierungsphase. Am Ende der Rundenstruktur wird der gesamte Zustand nochmal durchgemischt, rotiert, verknüpft 
und gegen feste Werte getestet. Ziel war es, mögliche Restmuster zu eliminieren und die Hash-Ausgabe weiter zu randomisieren.

Das Ergebnis: Ein 64 Byte langer Hash (512 Bit), schwer vorhersehbar, stabil, und voller kleiner, durchdachter Komponenten.

## Vom Konzept zum Härtetest

Nach der Entwicklung folgten die Tests. Ich Testete meinen Hash gegen:
- extrem große Eingaben laufen  
- Sonderzeichen, Unicode-Zeichen und sogar nicht-lateinische Zeichen 
- Timing-Angriffe (durch gezielte Zeitmessungen)
- und weitere Angriffe

Natürlich ist DavoHash512 ist nicht der schnellste Algorithmus und nicht Perfekt, aber das war auch nie mein Ziel. Ich wollte ein System schaffen, 
das robust ist, logisch aufgebaut und für mich persönlich eine "Lernreise durch die Welt der Kryptografie" bedeutet.

Ich habe viele Ressourcen genutzt, wie z. B. Online-Foren, technische Blogs, Künstliche Intelligenz, aber vor allem auch logisches Denken, Neugier und 
den Willen, wirklich zu verstehen, was hinter den Kulissen moderner Kryptografie passiert.

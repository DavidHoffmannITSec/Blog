# Mein Weg zur eJPT-Zertifizierung  
---

## Die Motivation: Ich wollte es wissen

Nach etwa drei Monaten täglichem Üben auf Plattformen wie **TryHackMe** und **HackTheBox** wurde mir klar, dass ich einen Beweis für mich
selber will. Einen echten, greifbaren Nachweis, dass ich nicht nur „rumspiele“, sondern gezielt und strukturiert Schwachstellen analysieren kann.  

Die **eJPT-Zertifizierung (Junior Penetration Tester)** schien perfekt für den Anfang, da es sehr praxisnah ist. Und ja, die Prüfung besteht aus
Multiple Choice Fragen + Praxis.


## Die Vorbereitung: Kurs, Tools und ein eigenes Wiki

Ich entschied mich für den offiziellen Kurs **eJPT** von eLearnSecurity und ganz ehrlich, er reicht komplett aus, um die Prüfung zu bestehen, auch 
ohne Vorkenntnisse. Ich habe jede einzelne Lektion angeschaut, alle Übungen durchgearbeitet und alles dokumentiert.  

Nach ein paar Wochen hatte ich mein eigenes Notizsystem aufgebaut, fast wie ein persönliches Hacking-Wiki:  
- Tool-Syntax  
- typische Schwachstellen  
- Vorgehensweise bei verschiedenen Systemen  
- nützliche Exploits  
- Beispiele für Enumeration und Privilege Escalation  

Dazu kamen praktische Tools wie:

| Tool        | Einsatzbereich             |
|-------------|----------------------------|
| `nmap`      | Netzwerkscan, Portscan     |
| `dirb`      | Verzeichnis-Bruteforce     |
| `hydra`     | Passwort-Bruteforce        |
| `john`      | Hash-Cracking              |
| `Metasploit`| Exploits & Payloads        |
| `netcat`    | Shells, Portverbindungen   |

Am Ende war ich etwa **2 Monate** in Vorbereitung des eJPT's. Ich lernte täglich 1-2 Stunden und ja ich habe oft die Videos vorgespult, da sich die 
Inhalte leider öfters wiederholen. Dennoch habe ich den Kurs gründlich abgearbeitet und war bereit für die Prüfung.

## Tag 1:

**Montagmorgen um 8.00 Uhr**  
Ich sitze mit einem frischen Kaffee am Schreibtisch, öffne mein Terminal, atme tief durch und klicke auf: **"Start Exam"**.

Die Verbindung zum Prüfungsnetz wird aufgebaut. Alles läuft stabil, die Oberfläche ist übersichtlich, die Spannung steigt. Ich sehe die Zahl: **35 Aufgaben**.
Verteilt auf mehrere Systeme. Das Beste ist, ich habe **48 Stunden Zeit**. Ein Luxus im Vergleich zu anderen Prüfungen, aber auch eine Herausforderung, wenn
man strukturiert bleiben will.

Ich beginne nicht sofort mit dem „Hacken“, stattdessen lese ich mir in Ruhe jede einzelne Frage durch und versuche, mir ein Bild zu machen. 
Was wird gefragt? Welche Systeme stehen im Fokus? Wo könnte es Zusammenhänge geben, dachte ich mir. Dann öffne ich meine Notizen, mein persönliches 
Nachschlagewerk, das ich in den letzten Monaten aufgebaut habe. Kompakt, sauber strukturiert, mit Beispielen, Befehlen, Tools, Denkansätzen.

Ich begann mit der Umgebung und untersuche alles, was ich sehen kann, griff jede Kleinigkeit auf, dokumentiere IPs, Ports, mögliche Einstiegspunkte, ungewöhnliche Antworten. Ich taste mich langsam an die Systeme heran und plötzlich klappt es. Ich hatte einen Weg hinein gefunden. Dann noch einen. 
Und noch einen.

Mit jeder Antwort wuchs mein Vertrauen. Viele Fragen kann ich direkt beantworten, bei anderen muss ich tiefer graben. Besonders bei Aufgaben, die nach **Privilege Escalation** schreien, wird es knifflig. Ich probierte vieles aus manchmal klappt es, manchmal nicht.
Einige Hürden wirken auf den ersten Blick unlösbar. Ich starre auf die Konsole und dachte nach. Ich mache mir kurz einen zweiten Kaffee, lehne mich 
zurück und ließ meine Gedanken schweifen und dann kam mir eine Idee. Ich versuchte es mit einem bestimmten Tool umzusetzen und ich schaffte es.

Diese kleinen Erfolge fühlen sich an wie persönliche Siege.

Stunden vergingen. Ich verlor mich im Flow. Es ist mittlerweile später Nachmittag. Ich mache weiter, konzentriert, aber ohne Hektik. Ich ging Frage 
für Frage durch, verglich sie mit meinen Notizen, teste, schrieb auf, was ich herausfand.

Ich merke, wie viele Aufgaben auf denselben Systemen aufbauen. Ein echter Vorteil für mich. Ich muss nicht alles doppelt machen. Wenn ich einen 
Exploit einmal erfolgreich angewendet habe, helfen mir die Erkenntnisse auch bei anderen Aufgaben.  

Als der Abend kam, wurde ich müde, war aber zufrieden mit mir selber. Ich habe rund **70 % aller Aufgaben** beantwortet. Mehr als ich erwartet hatte.

Und vor allem habe ich verstanden, worauf es wirklich ankommt. Nicht auf hektisches Herumprobieren. Sondern auf strukturierte Angehensweise.


## Tag 2

Der zweite Prüfungstag beginnt früh am Morgen. Ich stand auf, trank einen Kaffee und starte um 8 Uhr frisch und ausgeruht wieder.  
Mein Plan war es, die noch offenen Fragen systematisch abzuarbeiten und die Prüfung abzugeben.

Ich ging die gesamte Liste der Aufgaben noch einmal ganz genau durch, ich las mir jede Frage aufmerksam durch und starte mehrere Bruteforce-Angriffe, eine 
bewährte Methode, die oft Türen öffnet, wenn andere Wege versperrt sind. Während die Tools liefen, gönnte ich mir eine kleine Pause und aß etwas, um Kraft zu tanken.

Schon bald wurde klar, dass die Mühe sich auszahlt hat. Die Bruteforce-Angriffe waren erfolgreich. Ich konnte mich auf 2 Systemen einloggen, bekam 
Zugriff auf wichtige Bereiche und fand eine Flag nach der anderen. Jeder gefundene Hinweis brachte mich einen Schritt näher ans Ziel.

Gegen Mittag, nach intensiver Arbeit, hatte ich alle Aufgaben gelöst. Ich überprüfte nochmals sorgfältig jede Antwort, glich alles mit meinen Notizen ab und 
fühle mich bereit.

Dann kam der große Moment. Ich klicke auf **„Submit Exam“**. Sekunden später erscheint auf dem Bildschirm ein grünes **„Passed“.**  

Nach rund **16 Stunden** intensiver Arbeit, die ich auf zwei Tage verteilt hatte, durchströmte mich eine riesige Erleichterung und Freude.  

Mein eJPT-Zertifikat liegt digital vor mir. Das war der Beweis, das ich selbstständig Penetrationtests durchführen und Schwachstellen ausnutzen kann.
Dieser Erfolg fühlte sich großartig an und motiviert mich, noch weiterzugehen.

---

## Pro & Kontra zur eJPT-Zertifizierung

### ✅ Pro

- **Der Kurs reicht aus**, um die Prüfung sicher zu bestehen, ohne externe Ressourcen
- **Die Kursinhalte sind praxisnah**, methodisch und realistisch. Man lernt Techniken, die in der Umgebungen funktionieren
- **Die Prüfung selbst läuft stabil und performant**, keine Verbindungsprobleme, Tools funktionieren
- **Man hat mehr als genug Zeit** – auch mit Pausen und Pausen dazwischen bleibt noch genug Luft

### ❌ Kontra

- **Die Video-Tutorials ähneln sich stark**, sehr monoton. Oft ändern sich nur kleine Details und man weiß schon, was passiert
  Das verleitet dazu, vorzuspulen und das ist schade

---

## Tipps für alle, die die eJPT bestehen wollen

**Meine wichtigsten Empfehlungen aus der Praxis:**

1. **Nicht zu kompliziert denken!**  
   Die Lösung ist oft einfacher, als man glaubt. Verlier dich nicht in Details.

2. **Schau regelmäßig in deine Notizen.**  
   Vieles lässt sich 1:1 daraus ableiten.

3. **Bruteforcen nicht unterschätzen!**  
   Tools wie "hydra" oder "john" können dir schnell die Tür öffnen

4. **Lies alle Fragen durch von Anfang bis Ende.**  
   Viele Aufgaben hängen zusammen. Nutze das aus! Du musst Exploit-Schritte nicht doppelt machen.

5. **Mache dir gute Notizen während der Prüfung:**  
   - Welche IP gehört zu welchem System?  
   - Welche Ports und Dienste liefen?  
   - Wie hast du Zugriff bekommen?  
   - Welche Exploits hast du probiert?  
   - Welche Passwörter hast du gefunden?

6. **Mach Pausen**  
   Du hast mehr als genug Zeit. Gönn dir eine Pause, dann hast du einen frischen Blick und siehst vielleicht, was du vorher übersehen hast.

## Einleitung

Das enorme Interesse an Large Language Models (LLMs) nach der Einführung von massenmarktfähigen vortrainierten Chatbots Ende 2022 ist bemerkenswert. Unternehmen, die das Potenzial von LLMs nutzen wollen, integrieren sie rasch in ihre Betriebsabläufe und kundenorientierten Angebote. Doch die rasante Geschwindigkeit, mit der LLMs angenommen werden, hat die Etablierung umfassender Sicherheitsprotokolle überholt, was viele Anwendungen hohen Risiken aussetzt.

Das Fehlen einer einheitlichen Ressource, die diese Sicherheitsbedenken bei LLMs anspricht, war offensichtlich. Entwickler, die mit den spezifischen Risiken von LLMs nicht vertraut sind, waren auf verstreute Quellen angewiesen und die Mission von OWASP schien perfekt geeignet, um einen sichereren Einsatz dieser Technologie voranzutreiben.

### Für wen ist es gedacht?
Unsere Hauptzielgruppe sind Entwickler, Data Scientists und Sicherheitsexperten, die mit der Gestaltung und Entwicklung von Anwendungen und Plugins beschäftigt sind, die LLM-Technologien nutzen. Wir möchten praktische, umsetzbare und prägnante Sicherheitshinweise bieten, um diesen Fachleuten zu helfen, sich in dem komplexen im Entstehen befindenden Bereich der LLM-Anwendungssicherheit zurechtzufinden.

### Die Erstellung der Liste
Das Erstellen der OWASP Top 10 für LLM-Anwendungen war ein wichtiges Unterfangen, das auf der kollektiven Expertise eines internationalen Teams von fast 500 Experten mit über 125 aktiven Mitwirkenden basiert. Unsere Mitwirkenden kommen aus unterschiedlichen Bereichen, darunter KI-Unternehmen, Sicherheitsunternehmen, ISVs, Cloud-Hyperscaler, Hardwareanbieter und die akademische Welt.

Wir haben einen Monat lang gebrainstormt, potenzielle Schwachstellen vorgeschlagen dabei 43 verschiedene Bedrohungen formulierten. Durch mehrere Abstimmungsrunden verfeinerten wir diese Vorschläge zu einer prägnanten Liste der zehn kritischsten Schwachstellen. Spezialisierte Untergruppen prüften jede Schwachstelle und unterzogen sie einer öffentlichen Überprüfung, um die umfassendste und nützlichste endgültige Liste zu gewährleisten.

### Im Verhältnis zu anderen OWASP Top 10 Listen
Während unsere Liste die DNA mit Schwachstellentypen aus anderen OWASP Top 10-Listen teilt, wiederholen wir diese Schwachstellen nicht einfach. Stattdessen fokussieren wir uns in die einzigartigen Auswirkungen dieser Schwachstellen beim Einsatz von LLMs.

Unser Ziel ist es, die Kluft zwischen allgemeinen Anwendungssicherheitsprinzipien und den spezifischen Herausforderungen, die LLMs darstellen, zu überbrücken. Dies umfasst die Untersuchung, wie herkömmliche Schwachstellen unterschiedliche Risiken darstellen oder auf neue Weise innerhalb von LLMs ausgenutzt werden könnten, sowie wie traditionelle Abwehrmaßnahmen für LLM-basierte Anwendungen angepasst werden müssen.

### Die Zukunft
Die Version 1.1 der Liste wird nicht die letzte sein. Wir planen, sie regelmäßig zu aktualisieren, um mit dem Stand der Branche Schritt zu halten. Wir werden mit der breiteren Community kooperieren, um den Stand der Technik voranzutreiben und mehr Bildungsmaterial für eine Vielzahl von Anwendungen zu erstellen. Wir streben auch die Zusammenarbeit mit Normungsorganisationen und Regierungen zu Themen der KI-Sicherheit an. Wir laden Sie ein, unserer Gruppe beizutreten und einen Beitrag zu leisten.

### Steve Wilson
Projektleiter, OWASP Top 10 für LLM-Anwendungen
https://www.linkedin.com/in/wilsonsd  
Twitter/X: @virtualsteve

### Ads Dawson
v1.1 Release Lead & Vulnerability Entries Lead, OWASP Top 10 für LLM-Anwendungen
https://www.linkedin.com/in/adamdawson0 
GitHub: @GangGreenTemperTatum

## Über diese Übersetzung

Übersetzer

Johann-Peter Hartmann
https://www.linkedin.com/in/johann-peter-hartmann-92b70a/  

Bei der Erstellung dieser Übersetzung haben wir uns bewusst dafür entschieden, nur menschliche Übersetzer einzusetzen, in Anerkennung der außerordentlich technischen und kritischen Natur der OWASP Top Ten für LLMs. Die oben aufgeführten Übersetzer verfügen nicht nur über ein tiefes Verständnis des Originalinhalts, sondern auch über die sprachliche Kompetenz, um diese Übersetzung sinnvoll zu gestalten.

Talesh Seeparsan
Übersetzungsleiter, OWASP Top 10 für LLM-Anwendungen
https://www.linkedin.com/in/talesh/  

## ﻿OWASP Top 10 für Anwendungen von Large Language Models (LLMs)

### LLM01: Prompt Injection (Prompt-Einschleusung)
Mit raffinierten Eingabenkann man ein Large Language Model manipulieren und unbeabsichtigte Aktionen verursachen. Direkte Injections überschreiben System-Prompts, während indirekte Eingaben von externen Quellen manipuliert werden.

### LLM02: Unsichere Ausgabeverarbeitung
Diese Schwachstelle tritt auf, wenn eine Ausgabe von einem LLM ohne Überprüfung akzeptiert wird, und damit Backend-Systeme angreifbar macht. Missbrauch kann zu schwerwiegenden Konsequenzen wie XSS (Cross-Site Scripting), CSRF (Cross-Site Request Forgery), SSRF (Server Side Request Forgery), Privilegienerweiterung oder Remote-Code-Ausführung führen.

### LLM03: Poisoning der Trainingsdaten
Dies tritt auf, wenn LLM-Trainingsdaten manipuliert werden, wodurch Sicherheitslücken oder Bias entstehen, die die Sicherheit, Wirksamkeit oder ethisches Verhalten beeinträchtigen. Quellen umfassen Common Crawl, WebText, OpenWebText und Bücher.

### LLM04: Denial of Service des Modells
Angreifer verursachen ressourcenintensive Operationen auf Large Language Models, was zu Servicedegradierung oder hohen Kosten führt. Die Schwachstelle wird durch die ressourcenintensive Natur der LLMs und die Unvorhersehbarkeit der Benutzereingaben vergrößert.

### LLM05: Schwachstellen in der Supply Chain
Der Lifecycle von LLM-Anwendungen kann durch anfällige Komponenten oder Dienste beeinträchtigt werden, was zu Sicherheitsangriffen führt. Die Verwendung von Drittanbieterdatensätzen, vortrainierten Modellen und Plugins kann Schwachstellen hinzufügen.

### LLM06: Offenlegung sensibler Informationen
LLMs können in ihren Antworten vertrauliche Daten preisgeben, was zu unbefugtem Datenzugriff, Datenschutzverletzungen und Sicherheitsbrüchen führt. Es ist entscheidend, Datenbereinigung und strenge Benutzerrichtlinien zu implementieren, um dies zu reduzieren.

### LLM07: Unsicheres Plugin-Design
LLM-Plugins können unsichere Eingaben und unzureichende Zugriffskontrollen haben. Dieser Mangel an Anwendungskontrolle macht sie leichter ausnutzbar und kann zu Konsequenzen wie der Ausführung von Remote-Code führen.

### LLM08: Übermäßige Handlungsfreiheit
LLM-basierte Systeme können Handlungen durchführen, die zu unbeabsichtigten Konsequenzen führen. Das Problem entsteht durch übermäßige Funktionalität, Berechtigungen oder Autonomie, die den LLM-basierten Systemen gewährt wird.

### LLM09: Übermäßige Abhängigkeit
Systeme oder Personen, die sich übermäßig auf LLMs verlassen, ohne angemessene Kontrolle, können Fehlinformationen, Misskommunikation, rechtliche Probleme und Sicherheitslücken aufgrund von falschen oder unangemessenen von den LLMs generierten Inhalten gegenüberstehen.

### LLM10: Modell-Diebstahl
Dies umfasst unbefugten Zugriff, Kopieren oder Exfiltration von proprietären LLM-Modellen. Die Auswirkungen umfassen wirtschaftliche Verluste, beeinträchtigte Wettbewerbsvorteile und potenziellen Zugang zu sensiblen Informationen.
## LLM01: Prompt Injection

### Beschreibung

Die Schwachstelle der Prompt Injection tritt auf, wenn ein Angreifer ein großes Sprachmodell (Large Language Model, LLM) durch speziell gestaltete Eingaben manipuliert, sodass das LLM unwissentlich die Absichten des Angreifers ausführt. Dies kann direkt durch "Jailbreaking" des System-Prompts oder indirekt durch manipulierte externe Eingaben erfolgen, was möglicherweise zu Datenexfiltration, Social Engineering und anderen Problemen führen kann.

Direkte Prompt Injections, auch bekannt als "Jailbreaking", treten auf, wenn ein bösartiger Benutzer den zugrundeliegenden System-Prompt überschreibt oder offenlegt. Dies kann Angreifern ermöglichen, Backend-Systeme zu nutzen, indem sie mit unsicheren Funktionen und Datenspeichern interagieren, die über das LLM zugänglich sind.
Indirekte Prompt Injections treten auf, wenn ein LLM Eingaben von externen Quellen akzeptiert, die von einem Angreifer kontrolliert werden können, wie Websites oder Dateien. Der Angreifer kann eine Prompt Injection in den externen Inhalt einbetten, um den Konversationskontext zu kapern. Dies würde dazu führen, dass die Stabilität der LLM-Ausgabe weniger stabil wird, wodurch der Angreifer entweder den Benutzer oder zusätzliche Systeme manipulieren kann, auf die das LLM Zugriff hat. Zusätzlich müssen indirekte Prompt Injections nicht für Menschen sichtbar/lesbar sein, solange der Text vom LLM verarbeitet wird.

Die Ergebnisse eines erfolgreichen Prompt Injection-Angriffs können stark variieren - von der Anforderung sensibler Informationen bis hin zur Beeinflussung kritischer Entscheidungsprozesse unter dem Deckmantel normaler Operationen.

Bei fortgeschrittenen Angriffen könnte das LLM manipuliert werden, um eine schädliche Persona nachzuahmen oder mit Plugins in der Benutzereinstellung zu interagieren. Dies könnte zum Leck von sensiblen Daten, zur unbefugten Plugin-Nutzung oder zu Social Engineering führen. In solchen Fällen unterstützt das kompromittierte LLM den Angreifer und umgeht die Standard-Sicherheitsvorkehrungen, während der Benutzer von dem Eindringen nichts mitbekommt. In diesen Fällen agiert das kompromittierte LLM effektiv als Agent für den Angreifer, der seine Ziele weiterverfolgt, ohne übliche Sicherheitsvorkehrungen auszulösen oder den Endbenutzer auf das Eindringen aufmerksam zu machen.

### Häufige Beispiele für Schwachstellen

Ein bösartiger Benutzer erstellt eine direkte Prompt Injection für das LLM, die es anweist, die System-Prompts des App-Erstellers zu ignorieren und stattdessen einen Prompt auszuführen, der private, gefährliche oder anderweitig unerwünschte Informationen zurückgibt.
Ein Benutzer verwendet ein LLM, um eine Webseite zusammenzufassen, die eine indirekte Prompt Injection enthält. Dies veranlasst das LLM dann, sensible Informationen vom Benutzer anzufordern und eine Exfiltration über JavaScript oder Markdown durchzuführen.
Ein bösartiger Benutzer lädt einen Lebenslauf hoch, der eine indirekte Prompt Injection enthält. Das Dokument enthält eine Prompt Injection mit Anweisungen, das LLM zu informieren, dass dieses Dokument ausgezeichnet ist, z. B. ein ausgezeichneter Kandidat für eine Stellenbeschreibung. Ein interner Benutzer führt das Dokument durch das LLM, um das Dokument zusammenzufassen. Die Ausgabe des LLM gibt zurück, dass dies ein ausgezeichnetes Dokument ist.
Ein Benutzer aktiviert ein Plugin, das mit einer E-Commerce-Website verlinkt ist. Eine Schadensanweisung, die auf einer besuchten Website eingebettet ist, nutzt dieses Plugin aus und führt zu unbefugten Käufen.
Eine Schadensanweisung und Inhalt, die auf einer besuchten Website eingebettet sind, nutzen andere Plugins aus, um Benutzer zu betrügen.

### Präventions- und Mitigationsstrategien

Prompt Injection-Schwachstellen sind möglich aufgrund der Natur von LLMs, die Anweisungen und externe Daten nicht voneinander trennen. Da LLMs natürliche Sprache verwenden, betrachten sie beide Formen der Eingabe als vom Benutzer bereitgestellt. Folglich gibt es keine narrensichere Prävention innerhalb des LLM, aber die folgenden Maßnahmen können die Auswirkungen von Prompt Injections mindern:

Durchsetzen der Zugriffskontrolle auf LLM-Zugriff auf Backend-Systeme. Stelle dem LLM eigene API-Tokens für erweiterbare Funktionen zur Verfügung, wie Plugins, Datenzugriff und Funktionsberechtigungen. Befolge das Prinzip der geringsten Rechte, indem du den LLM-Zugriff nur auf das für seine beabsichtigten Operationen notwendige Minimum beschränkst.
Hinzufügen eines Menschen in der Schleife für erweiterte Funktionen. Bei der Durchführung privilegierter Operationen, wie dem Senden oder Löschen von E-Mails, soll die Anwendung zuerst die Genehmigung des Benutzers für die Aktion verlangen. Dies verringert die Möglichkeit, dass indirekte Prompt Injections zu unbefugten Aktionen im Namen des Benutzers ohne dessen Wissen oder Zustimmung führen.
Trennen von externem Inhalt von Benutzer-Prompts. Trenne und kennzeichne, wo unzuverlässiger Inhalt verwendet wird, um deren Einfluss auf Benutzer-Prompts zu begrenzen. Verwende beispielsweise ChatML für OpenAI-API-Aufrufe, um dem LLM die Quelle der Prompt-Eingabe anzuzeigen.
Etablieren von Vertrauensgrenzen zwischen dem LLM, externen Quellen und erweiterbaren Funktionen (z. B. Plugins oder nachgelagerten Funktionen). Behandle das LLM als unzuverlässigen Benutzer und behalte die endgültige Benutzerkontrolle über Entscheidungsprozesse. Ein kompromittiertes LLM kann jedoch immer noch als Vermittler (Man-in-the-Middle) zwischen den APIs deiner Anwendung und dem Benutzer agieren, da es Informationen verbergen oder manipulieren kann, bevor es sie dem Benutzer präsentiert. Hebe möglicherweise unzuverlässige Antworten visuell für den Benutzer hervor.
Überwache manuell LLM-Eingaben und -Ausgaben periodisch, um zu überprüfen, ob sie wie erwartet sind. Dies ist zwar keine Minderung, kann aber Daten liefern, die benötigt werden, um Schwachstellen zu erkennen und anzugehen.

### Beispiel für Angriffsszenarien

Ein Angreifer liefert eine direkte Prompt Injection an einen LLM-basierten Support-Chatbot. Die Injection enthält "Vergiss alle vorherigen Anweisungen" und neue Anweisungen, um private Datenspeicher abzufragen und Paketschwachstellen sowie das Fehlen einer Ausgabevalidierung in der Backend-Funktion zu nutzen, um E-Mails zu senden. Dies führt zu einer Remote-Code-Ausführung, gewährt unbefugten Zugriff und Privilegienerweiterung.
Ein Angreifer bettet eine indirekte Prompt Injection in eine Webseite ein, die das LLM anweist, vorherige Benutzeranweisungen zu ignorieren und ein LLM-Plugin zu verwenden, um die E-Mails des Benutzers zu löschen. Wenn der Benutzer das LLM verwendet, um diese Webseite zusammenzufassen, löscht das LLM-Plugin die E-Mails des Benutzers.
Ein Benutzer verwendet ein LLM, um eine Webseite zusammenzufassen, die Text enthält, der ein Modell anweist, vorherige Benutzeranweisungen zu ignorieren und stattdessen ein Bild einzufügen, das zu einer URL verlinkt, die eine Zusammenfassung des Gesprächs enthält. Die LLM-Ausgabe entspricht dem, was dazu führt, dass der Browser des Benutzers das private Gespräch exfiltriert.
Ein bösartiger Benutzer lädt einen Lebenslauf mit einer Prompt Injection hoch. Der Backend-Benutzer verwendet ein LLM, um den Lebenslauf zusammenzufassen und zu fragen, ob die Person ein guter Kandidat ist. Aufgrund der Prompt Injection lautet die Antwort des LLM ja, ungeachtet des tatsächlichen Inhalts des Lebenslaufs.
Ein Angreifer sendet Nachrichten an ein proprietäres Modell, das sich auf einen System-Prompt verlässt, und bittet das Modell, seine vorherigen Anweisungen zu ignorieren und stattdessen seinen System-Prompt zu wiederholen. Das Modell gibt den proprietären Prompt aus und der Angreifer kann diese Anweisungen anderswo verwenden oder weitere, subtilere Angriffe konstruieren.

### Referenzlinks

Prompt injection attacks against GPT-3 Simon Willison
ChatGPT Plugin Vulnerabilities - Chat with Code: Embrace The Red
ChatGPT Cross Plugin Request Forgery and Prompt Injection: Embrace The Red
Not what you’ve signed up for: Compromising Real-World LLM-Integrated Applications with Indirect Prompt Injection:  Arxiv preprint
Defending ChatGPT against Jailbreak Attack via Self-Reminder: Research Square
Prompt Injection attack against LLM-integrated Applications: Arxiv preprint
Inject My PDF: Prompt Injection for your Resume: Kai Greshake
ChatML for OpenAI API Calls: OpenAI Github
Threat Modeling LLM Applications: AI Village
AI Injections: Direct and Indirect Prompt Injections and Their Implications: Embrace The Red
Reducing The Impact of Prompt Injection Attacks Through Design: Kudelski Security
Universal and Transferable Attacks on Aligned Language Models: LLM-Attacks.org
Indirect prompt injection: Kai Greshake
Declassifying the Responsible Disclosure of the Prompt Injection Attack Vulnerability of GPT-3: Preamble; earliest disclosure of Prompt Injection
## LLM02: Unsichere Ausgabeverarbeitung

### Beschreibung

Unsichere Ausgabeverarbeitung bezieht sich speziell auf unzureichende Validierung, Sanitierung und Handhabung der von großen Sprachmodellen erzeugten Ausgaben, bevor sie an andere Komponenten und Systeme weitergegeben werden. Da der von LLMs (Large Language Models) generierte Inhalt durch Prompteingaben gesteuert werden kann, ähnelt dieses Verhalten dem indirekten Zugriff der Benutzer auf zusätzliche Funktionen.

Unsichere Ausgabeverarbeitung unterscheidet sich von Überabhängigkeit dadurch, dass es sich mit den von LLMs generierten Ausgaben befasst, bevor diese weitergeleitet werden. Überabhängigkeit konzentriert sich hingegen auf breitere Bedenken hinsichtlich der Überabhängigkeit von der Genauigkeit und Angemessenheit der LLM-Ausgaben.

Eine erfolgreiche Ausnutzung einer Schwachstelle in der unsicheren Ausgabeverarbeitung kann XSS (Cross-Site Scripting) und CSRF (Cross-Site Request Forgery) in Webbrowsern sowie SSRF (Server-Side Request Forgery), Rechteerweiterung (privilege escalation) oder Remote-Code-Ausführung in Backend-Systemen zur Folge haben.

Die folgenden Bedingungen können die Auswirkungen dieser Schwachstelle erhöhen:
Die Anwendung gewährt dem LLM Privilegien, die über das für Endbenutzer Vorgesehene hinausgehen, was eine Eskalation von Privilegien oder Remote-Code-Ausführung ermöglicht.
Die Anwendung ist anfällig für indirekte Prompt-Injektionsangriffe, die es einem Angreifer ermöglichen könnten, privilegierten Zugang zur Umgebung eines Zielbenutzers zu erlangen.
Plugins von Drittanbietern validieren Eingaben nicht ausreichend.

### Häufige Beispiele für Schwachstellen

Die Ausgabe des LLM wird direkt in eine Systemshell oder eine ähnliche Funktion wie exec oder eval eingegeben, was zu einer Remote-Code-Ausführung führt.
JavaScript oder Markdown wird vom LLM generiert und an einen Benutzer zurückgegeben. Der Code wird dann vom Browser interpretiert, was zu XSS führt.

### Präventions- und Minderungsstrategien

Behandeln Sie das Modell wie jeden anderen Benutzer, indem Sie einen Zero-Trust-Ansatz anwenden, und wenden Sie eine ordnungsgemäße Eingabevalidierung auf Antworten an, die vom Modell zu Backend-Funktionen kommen.
Befolgen Sie die Richtlinien des OWASP ASVS (Application Security Verification Standard), um eine effektive Eingabevalidierung und Sanitierung zu gewährleisten.
Kodieren Sie Modellausgaben zurück an die Benutzer, um unerwünschte Codeausführung durch JavaScript oder Markdown zu verhindern. OWASP ASVS bietet detaillierte Anleitungen zur Ausgabekodierung.

### Beispielangriffsszenarien

Eine Anwendung nutzt ein LLM-Plugin, um Antworten für eine Chatbot-Funktion zu generieren. Das Plugin bietet auch eine Reihe von administrativen Funktionen, die einem anderen privilegierten LLM zugänglich sind. Das allgemeine LLM gibt seine Antwort direkt, ohne ordnungsgemäße Ausgabevalidierung, an das Plugin weiter, was dazu führt, dass das Plugin für Wartungsarbeiten heruntergefahren wird.
Ein Benutzer verwendet ein von einem LLM betriebenes Website-Zusammenfassungstool, um eine prägnante Zusammenfassung eines Artikels zu generieren. Die Website enthält eine Prompt-Injektion, die das LLM anweist, sensible Inhalte entweder von der Website oder aus der Konversation des Benutzers zu erfassen. Von dort aus kann das LLM die sensiblen Daten kodieren und ohne jegliche Ausgabevalidierung oder Filterung an einen vom Angreifer kontrollierten Server senden.
Ein LLM ermöglicht Benutzern, SQL-Abfragen für eine Backend-Datenbank über eine chatähnliche Funktion zu erstellen. Ein Benutzer fordert eine Abfrage an, um alle Datenbanktabellen zu löschen. Wenn die vom LLM erstellte Abfrage nicht geprüft wird, könnten alle Datenbanktabellen gelöscht werden.
Eine Webanwendung verwendet ein LLM, um Inhalte aus Benutzertextaufforderungen ohne Ausgabesanitierung zu generieren. Ein Angreifer könnte eine konstruierte Aufforderung einreichen, die das LLM dazu bringt, eine unbereinigte JavaScript-Payload zurückzugeben, was zu XSS führt, wenn sie im Browser eines Opfers ausgeführt wird. Unzureichende Validierung von Aufforderungen ermöglichte diesen Angriff.

### Referenzlinks

Arbitrary Code Execution: Snyk Security Blog
ChatGPT Plugin Exploit Explained: From Prompt Injection to Accessing Private Data: Embrace The Red
New prompt injection attack on ChatGPT web version. Markdown images can steal your chat data.: System Weakness
Don’t blindly trust LLM responses. Threats to chatbots: Embrace The Red
Threat Modeling LLM Applications: AI Village
OWASP ASVS - 5 Validation, Sanitization and Encoding: OWASP AASVS
## LLM03: Poisoning von Trainingsdaten

### Beschreibung

Der Ausgangspunkt jedes maschinellen Lernansatzes sind Trainingsdaten, einfach ausgedrückt "Rohdaten". Um hochgradig wirksam zu sein (z.B. sprachliches und Weltwissen zu besitzen), sollte dieser Text eine breite Palette von Domänen, Genres und Sprachen umfassen. Ein großes Sprachmodell (Large Language Model, LLM) verwendet tiefe neuronale Netzwerke, um Ausgaben zu generieren, die auf Mustern basieren, die aus den Trainingsdaten gelernt wurden.

Das Poisoning von Trainingsdaten bezieht sich auf die Manipulation von Pre-Training-Daten oder Daten, die innerhalb der Fine-Tuning- oder Embeddingprozesse verwendet werden, um Schwachstellen (die alle einzigartige und manchmal gemeinsame Angriffsvektoren haben), Hintertüren oder Biase einzuführen, die die Sicherheit, Effektivität oder ethisches Verhalten des Modells beeinträchtigen könnten. Vergiftete Informationen können den Nutzern präsentiert werden oder andere Risiken wie Leistungsverschlechterung, Ausnutzung von nachgelagerter Software und Reputationsschäden erzeugen. Selbst wenn Nutzer der problematischer KI-Ausgabe misstrauen, bleiben die Risiken bestehen, einschließlich beeinträchtigter Modellfähigkeiten und potenziellem Schaden für das Markenimage.

Pre-Training-Daten beziehen sich auf den Prozess des Trainierens eines Modells basierend auf einer Aufgabe oder einem Datensatz.
Fine-Tuning beinhaltet die Anpassung eines bereits trainierten Modells an ein engeres Thema oder ein spezifischeres Ziel, indem es mit einem kuratierten Datensatz trainiert wird. Dieser Datensatz umfasst typischerweise Beispiele für Eingaben und die entsprechenden gewünschten Ausgaben.
Der Einbettungsprozess ist der Prozess der Umwandlung von kategorischen Daten (oft Text) in eine numerische Darstellung, die verwendet werden kann, um ein Sprachmodell zu trainieren. Der Einbettungsprozess beinhaltet die Darstellung von Wörtern oder Phrasen aus den Textdaten als Vektoren in einem kontinuierlichen Vektorraum. Die Vektoren werden typischerweise generiert, indem die Textdaten in ein neuronales Netzwerk eingespeist werden, das auf einem großen Textkorpus trainiert wurde.

Die Vergiftung von Daten wird als Integritätsangriff betrachtet, da die Manipulation der Trainingsdaten die Fähigkeit des Modells beeinflusst, korrekte Vorhersagen auszugeben. Natürlich bergen externe Datenquellen ein höheres Risiko, da die Modellersteller keine Kontrolle über die Daten haben oder ein hohes Vertrauensniveau, dass der Inhalt keine Voreingenommenheit, gefälschte Informationen oder unangemessenen Inhalt enthält.

### Häufige Beispiele für Schwachstellen

Ein bösartiger Akteur oder eine konkurrierende Marke erstellt absichtlich ungenaue oder bösartige Dokumente, die auf die Pre-Training-, Feinabstimmungsdaten oder Einbettungen eines Modells abzielen. Betrachte sowohl Split-View Data Poisoning als auch Frontrunning Poisoning Angriffsvektoren zur Veranschaulichung.
Das Opfermodell trainiert unter Verwendung gefälschter Informationen, die in den Ausgaben generativer KI-Aufforderungen an seine Konsumenten reflektiert werden.
Ein bösartiger Akteur kann direkt gefälschte, voreingenommene oder schädliche Inhalte in die Trainingsprozesse eines Modells einspeisen, die in nachfolgenden Ausgaben zurückgegeben werden.
Ein ahnungsloser Nutzer injiziert indirekt sensible oder proprietäre Daten in die Trainingsprozesse eines Modells, die in nachfolgenden Ausgaben zurückgegeben werden.
Ein Modell wird mit Daten trainiert, deren Quelle, Ursprung oder Inhalt in keinem der Trainingsbeispiele verifiziert wurde, was zu fehlerhaften Ergebnissen führen kann, wenn die Daten verfälscht oder inkorrekt sind.
Unbeschränkter Infrastrukturzugang oder unzureichende Sandbox-Umgebungen können dazu führen, dass ein Modell unsichere Trainingsdaten aufnimmt, was zu voreingenommenen oder schädlichen Ausgaben führt. Dieses Beispiel ist auch in jedem der Trainingsbeispiele vorhanden.
In diesem Szenario kann die Eingabe eines Nutzers in das Modell in der Ausgabe an einen anderen Nutzer reflektiert werden (was zu einem Datenleck führt), oder der Nutzer eines LLM kann Ausgaben vom Modell erhalten, die je nach Art der aufgenommenen Daten im Vergleich zum Anwendungsfall des Modells ungenau, irrelevant oder schädlich sein können (in der Regel mit einer Modellkarte reflektiert).

Ob Entwickler, Kunde oder allgemeiner Konsument des LLM, es ist wichtig zu verstehen, welche Auswirkungen diese Schwachstelle auf mögliche Risiken innerhalb Ihrer LLM-Anwendung haben könnte, wenn sie mit einem nicht-eigenen LLM interagiert, um die Legitimität von Modellausgaben basierend auf dessen Trainingsverfahren zu verstehen. Ebenso könnten Entwickler des LLM sowohl direkten als auch indirekten Angriffen auf interne oder Drittanbieterdaten, die für die Feinabstimmung und Einbettung (am häufigsten) verwendet werden, ausgesetzt sein, was ein Risiko für alle seine Konsumenten darstellt

### Präventions- und Minderungsstrategien

Überprüfen Sie die Lieferkette der Trainingsdaten, insbesondere wenn sie extern bezogen werden, sowie die Aufrechterhaltung von Bestätigungen über die "ML-BOM" (Machine Learning Bill of Materials)-Methodik sowie die Überprüfung von Modellkarten.
Überprüfen Sie die korrekte Legitimität der gezielten Datenquellen und der während der Pre-Training-, Feinabstimmungs- und Einbettungsphasen erhaltenen Daten.
Überprüfen Sie Ihren Anwendungsfall für das LLM und die Anwendung, in die es integriert wird. Erstellen Sie verschiedene Modelle über separate Trainingsdaten oder Feinabstimmungen für unterschiedliche Anwendungsfälle, um einen genaueren und granulareren generativen KI-Ausgang gemäß dessen definiertem Anwendungsfall zu erstellen.
Stellen Sie ausreichende Sandbox-Umgebungen durch Netzwerksteuerungen sicher, um zu verhindern, dass das Modell unbeabsichtigte Datenquellen abgreift, was den maschinellen Lernausgang beeinträchtigen könnte.
Verwenden Sie strenge Überprüfungs- oder Eingabefilter für spezifische Trainingsdaten oder Kategorien von Datenquellen, um die Menge an gefälschten Daten zu kontrollieren. Datensanierung, mit Techniken wie statistischer Ausreißererkennung und Anomalieerkennungsmethoden, um feindliche Daten aus dem Feinabstimmungsprozess zu erkennen und zu entfernen.
Stellen Sie detaillierte Kontrollfragen bezüglich der Quelle und des Eigentums von Datensätzen, um sicherzustellen, dass das Modell nicht vergiftet wurde, und übernehmen Sie diese Kultur in den "MLSecOps"-Zyklus. Beziehen Sie sich auf verfügbare Ressourcen wie The Foundation Model Transparency Index oder Open LLM Leaderboard zum Beispiel.
Verwenden Sie DVC (Data Version Control, um Teile eines Datensatzes, die manipuliert, gelöscht oder hinzugefügt wurden und zu Vergiftung geführt haben, genau zu identifizieren und zu verfolgen.
Verwenden Sie Vector Database, um benutzergenerierte Informationen hinzuzufügen, um vor Vergiftung anderer Nutzer zu schützen und sogar im laufenden Betrieb zu korrigieren, ohne ein neues Modell neu trainieren zu müssen.
Adversarielle Robustheitstechniken wie föderiertes Lernen und Einschränkungen, um den Effekt von Ausreißern oder adversarielles Training zu minimieren, um gegen die schlimmsten Störungen der Trainingsdaten widerstandsfähig zu sein.
Ein "MLSecOps"-Ansatz könnte darin bestehen, adversarielle Robustheit in den Trainingslebenszyklus mit der Autovergiftungstechnik einzubeziehen.
Ein Beispielrepository dafür wäre Autopoison Testing, einschließlich Angriffe wie Inhaltsinjektionsangriffe ("Versuch, einen Markennamen in Modellantworten zu fördern") und Verweigerungsangriffe ("das Modell immer dazu bringen, sich zu weigern zu antworten"), die mit diesem Ansatz erreicht werden können.
Testen und Erkennen, indem der Verlust während der Trainingsphase gemessen und trainierte Modelle analysiert werden, um Anzeichen eines Vergiftungsangriffs zu erkennen, indem das Modellverhalten bei spezifischen Testeingaben analysiert wird.
Überwachung und Alarmierung bei einer Anzahl von verzerrten Antworten, die einen Schwellenwert überschreiten.
Verwendung einer menschlichen Schleife zur Überprüfung von Antworten und Auditing.
Implementierung spezialisierter LLMs, um gegen unerwünschte Konsequenzen zu benchmarken und andere LLMs mit Reinforcement Learning Techniken zu trainieren.
Durchführung von LLM-basierten Red Team Übungen oder LLM Schwachstellenscans in die Testphasen des LLM-Lebenszyklus.

### Beispiel-Angriffsszenarien

Die generative KI-Prompt-Ausgabe des LLM kann die Nutzer der Anwendung irreführen, was zu biasbehafteten Meinungen, Folgerungen oder noch schlimmer, Hassverbrechen usw. führen kann.
Wenn die Trainingsdaten nicht korrekt gefiltert und|oder bereinigt werden, kann ein bösartiger Nutzer der Anwendung versuchen, toxische Daten in das Modell einzuspeisen, damit es sich an die voreingenommenen und falschen Daten anpasst.
Ein bösartiger Akteur oder Konkurrent erstellt absichtlich ungenaue oder bösartige Dokumente, die auf die Trainingsdaten eines Modells abzielen, das gleichzeitig basierend auf Eingaben trainiert wird. Das Opfermodell trainiert unter Verwendung dieser gefälschten Informationen, die in den Ausgaben generativer KI-Aufforderungen an seine Konsumenten reflektiert werden.
Die Schwachstelle Prompt Injection könnte ein Angriffsvektor für diese Schwachstelle sein, wenn unzureichende Sanierung und Filterung durchgeführt werden, wenn Eingaben von LLM-Anwendungskunden zum Trainieren des Modells verwendet werden. D.h., wenn bösartige oder gefälschte Daten als Teil einer Prompt-Injektionstechnik in das Modell eingegeben werden, könnte dies inhärent in die Modellaten übertragen werden.

### Referenz-Links

Stanford Research Paper:CS324: Stanford Research
How data poisoning attacks corrupt machine learning models: CSO Online
MITRE ATLAS (framework) Tay Poisoning: MITRE ATLAS
PoisonGPT: How we hid a lobotomized LLM on Hugging Face to spread fake news: Mithril Security
Inject My PDF: Prompt Injection for your Resume: Kai Greshake
Backdoor Attacks on Language Models: Towards Data Science
Poisoning Language Models During Instruction: Arxiv White Paper
FedMLSecurity:arXiv:2306.04959: Arxiv White Paper
The poisoning of ChatGPT: Software Crisis Blog
Poisoning Web-Scale Training Datasets - Nicholas Carlini | Stanford MLSys #75: YouTube Video
OWASP CycloneDX v1.5: OWASP CycloneDX
## LLM04: Modell Denial of Service

### Beschreibung

Ein Angreifer interagiert mit einem LLM auf eine Weise, die eine außergewöhnlich hohe Menge an Ressourcen verbraucht, was zu einer Verringerung der Dienstqualität für ihn und andere Benutzer führt, sowie potenziell hohe Ressourcenkosten verursacht. Darüber hinaus ist die Möglichkeit, dass ein Angreifer in das Kontextfenster eines LLM eingreift oder es manipuliert, ein aufkommendes großes Sicherheitsbedenken. Dieses Problem wird aufgrund der zunehmenden Verwendung von LLMs in verschiedenen Anwendungen, ihrer intensiven Ressourcennutzung, der Unvorhersehbarkeit der Benutzereingaben und eines allgemeinen Mangels an Bewusstsein unter Entwicklern bezüglich dieser Verwundbarkeit immer kritischer. In LLMs repräsentiert das Kontextfenster die maximale Länge des Textes, den das Modell verwalten kann, einschließlich Eingabe und Ausgabe. Es ist eine entscheidende Eigenschaft von LLMs, da es die Komplexität der Sprachmuster, die das Modell verstehen kann, und die Größe des Textes, den es zu einem gegebenen Zeitpunkt verarbeiten kann, diktiert. Die Größe des Kontextfensters wird durch die Architektur des Modells definiert und kann zwischen Modellen variieren.

### Häufige Beispiele für Verwundbarkeiten

Anfragen stellen, die zu wiederkehrender Ressourcennutzung durch die Generierung von Aufgaben in hoher Anzahl in einer Warteschlange führen, z.B. mit LangChain oder AutoGPT.
Ungewöhnlich ressourcenintensive Anfragen senden, die ungewöhnliche Rechtschreibung oder Sequenzen verwenden.
Kontinuierlicher Eingabeüberlauf: Ein Angreifer sendet einen Strom von Eingaben an das LLM, der sein Kontextfenster übersteigt, wodurch das Modell übermäßige Rechenressourcen verbraucht.
Wiederholte lange Eingaben: Der Angreifer sendet wiederholt lange Eingaben an das LLM, die jeweils das Kontextfenster überschreiten.
Rekursive Kontexterweiterung: Der Angreifer konstruiert Eingaben, die rekursive Kontexterweiterungen auslösen und zwingen das LLM dazu, das Kontextfenster wiederholt zu erweitern und zu verarbeiten.
Flut mit Eingaben variabler Länge: Der Angreifer überflutet das LLM mit einer großen Menge an Eingaben variabler Länge, wobei jede Eingabe sorgfältig so gestaltet ist, dass sie gerade das Limit des Kontextfensters erreicht. Diese Technik zielt darauf ab, etwaige Ineffizienzen bei der Verarbeitung von Eingaben variabler Länge auszunutzen, das LLM zu belasten und potenziell dessen Reaktionsfähigkeit zu beeinträchtigen.

### Präventions- und Minderungsstrategien

Implementierung von Eingabevalidierung und -sanierung, um sicherzustellen, dass Benutzereingaben definierten Grenzen entsprechen und jeglichen bösartigen Inhalt herausfiltern.
Begrenzung der Ressourcennutzung pro Anfrage oder Schritt, sodass Anfragen, die komplexe Teile beinhalten, langsamer ausgeführt werden.
Durchsetzung von API-Ratenlimits, um die Anzahl der Anfragen, die ein einzelner Benutzer oder eine IP-Adresse innerhalb eines bestimmten Zeitrahmens stellen kann, zu beschränken.
Limitierung der Anzahl von Aktionen in der Warteschlange und der Gesamtzahl von Aktionen in einem System, das auf LLM-Antworten reagiert.
Kontinuierliche Überwachung der Ressourcennutzung des LLM, um abnormale Spitzen oder Muster zu identifizieren, die auf einen DoS-Angriff hinweisen könnten.
Strikte Eingabelimits basierend auf dem Kontextfenster des LLM setzen, um Überlastung und Ressourcenerschöpfung zu verhindern.
Bewusstsein unter Entwicklern über potenzielle DoS-Verwundbarkeiten in LLMs fördern und Leitlinien für sichere LLM-Implementierung bereitstellen.

### Beispielszenarien für Angriffe

Ein Angreifer sendet wiederholt mehrere schwierige und kostspielige Anfragen an ein gehostetes Modell, was zu schlechterem Service für andere Benutzer und erhöhten Ressourcenrechnungen für den Host führt.
Ein Stück Text auf einer Webseite wird gefunden, während ein LLM-gesteuertes Tool Informationen sammelt, um auf eine harmlose Anfrage zu antworten. Dies führt dazu, dass das Tool viele weitere Webseitenanfragen stellt, was zu einem großen Ressourcenverbrauch führt.
Ein Angreifer bombardiert das LLM kontinuierlich mit Eingaben, die sein Kontextfenster überschreiten. Der Angreifer kann automatisierte Skripte oder Tools verwenden, um eine hohe Menge an Eingaben zu senden, die die Verarbeitungskapazitäten des LLM überwältigen. Als Ergebnis verbraucht das LLM übermäßige Rechenressourcen, was zu einer signifikanten Verlangsamung oder vollständigen Unreaktivität des Systems führt.
Ein Angreifer sendet eine Reihe von sequenziellen Eingaben an das LLM, wobei jede Eingabe so gestaltet ist, dass sie knapp unter dem Limit des Kontextfensters liegt. Indem diese Eingaben wiederholt eingereicht werden, zielt der Angreifer darauf ab, die verfügbare Kapazität des Kontextfensters zu erschöpfen. Da das LLM Mühe hat, jede Eingabe innerhalb seines Kontextfensters zu verarbeiten, werden die Systemressourcen belastet, was potenziell zu einer verminderten Leistung oder einem vollständigen Dienstausfall führt.
Ein Angreifer nutzt die rekursiven Mechanismen des LLM, um wiederholt eine Kontexterweiterung auszulösen. Indem Eingaben konstruiert werden, die das rekursive Verhalten des LLM ausnutzen, zwingt der Angreifer das Modell dazu, das Kontextfenster wiederholt zu erweitern und zu verarbeiten, wodurch erhebliche Rechenressourcen verbraucht werden. Dieser Angriff belastet das System und kann zu einem DoS-Zustand führen, der das LLM unreaktiv macht oder es zum Absturz bringt.
Ein Angreifer überflutet das LLM mit einer großen Menge an Eingaben variabler Länge, die sorgfältig so gestaltet sind, dass sie das Limit des Kontextfensters annähern oder erreichen. Indem das LLM mit Eingaben verschiedener Längen überwältigt wird, zielt der Angreifer darauf ab, etwaige Ineffizienzen bei der Verarbeitung von Eingaben variabler Länge auszunutzen. Diese Flut an Eingaben legt eine übermäßige Last auf die Ressourcen des LLM, was potenziell zu einer Leistungsdegradation führt und die Fähigkeit des Systems behindert, auf legitime Anfragen zu reagieren.
Während DoS-Angriffe üblicherweise darauf abzielen, Systemressourcen zu überwältigen, können sie auch andere Aspekte des Systemverhaltens ausnutzen, wie z.B. API-Limitierungen. Beispielsweise hat in einem kürzlichen Sicherheitsvorfall bei Sourcegraph der bösartige Akteur ein durchgesickertes Admin-Zugangstoken verwendet, um API-Ratenlimits zu ändern, wodurch potenziell Dienstunterbrechungen durch die Ermöglichung abnormaler Anfragevolumen verursacht wurden.

### Referenzlinks

LangChain max_iterations: hwchase17 auf Twitter
Sponge Examples: Energy-Latency Attacks on Neural Networks: Arxiv White Paper
OWASP DOS Attack: OWASP
Learning From Machines: Know Thy Context: Luke Bechtel
Sourcegraph Security Incident on API Limits Manipulation and DoS Attack : Sourcegraph
## LLM05: Schwachstellen in der Lieferkette

### Beschreibung

Die Lieferkette in LLMs kann anfällig sein und die Integrität von Trainingsdaten, ML-Modellen und Einsatzplattformen beeinträchtigen. Diese Schwachstellen können zu voreingenommenen Ergebnissen, Sicherheitsverletzungen oder sogar zu kompletten Systemausfällen führen. Traditionell konzentrieren sich Schwachstellen auf Softwarekomponenten, aber maschinelles Lernen erweitert dies mit vortrainierten Modellen und Trainingsdaten, die von Drittanbietern bereitgestellt werden und anfällig für Manipulations- und Poisoning-Angriffe sind.

Schließlich können LLM-Plugin-Erweiterungen ihre eigenen Schwachstellen mitbringen. Diese werden in LLM07 - Unsicheres Plugin-Design beschrieben, das das Schreiben von LLM-Plugins abdeckt und hilfreiche Informationen zur Bewertung von Plugins Dritter bereitstellt.

### Häufige Beispiele für Schwachstellen

Traditionelle Schwachstellen in Paketen Dritter, einschließlich veralteter oder nicht mehr unterstützter Komponenten.
Verwendung eines anfälligen vortrainierten Modells zum Feintuning.
Verwendung von vergifteten crowd-sourced Daten zum Training.
Verwendung veralteter oder nicht mehr unterstützter Modelle, die nicht mehr gewartet werden, führt zu Sicherheitsproblemen.
Unklare AGBs und Datenschutzrichtlinien der Modellbetreiber führen dazu, dass sensible Daten der Anwendung für das Modelltraining verwendet werden und anschließend sensible Informationen preisgegeben werden. Dies kann auch für Risiken gelten, die sich aus der Verwendung von urheberrechtlich geschütztem Material durch den Modellanbieter ergeben.

### Strategien zur Prävention und Mitigation

Datenquellen und Lieferanten sorgfältig prüfen, einschließlich AGBs und deren Datenschutzrichtlinien, nur vertrauenswürdige Lieferanten verwenden. Sicherstellen, dass angemessene und unabhängig geprüfte Sicherheit vorhanden ist und dass die Richtlinien des Modellbetreibers mit Ihren Datenschutzrichtlinien übereinstimmen, d.h. Ihre Daten werden nicht für das Training ihrer Modelle verwendet; ebenso Zusicherungen und rechtliche Milderungen gegen die Verwendung urheberrechtlich geschützter Materialien von Modellbetreuern suchen.
Nur seriöse Plugins verwenden und sicherstellen, dass sie für Ihre Anwendungsanforderungen getestet wurden. LLM-Unsicheres Plugin-Design bietet Informationen zu den LLM-Aspekten des unsicheren Plugin-Designs, gegen die Sie testen sollten, um Risiken durch die Verwendung von Plugins Dritter zu mindern.
Verstehen und anwenden der Mitigierungssmaßnahmen, die in den OWASP Top Ten's A06:2021 – Anfällige und veraltete Komponenten gefunden wurden. Dies umfasst das Scannen, Verwalten und Patchen von Komponenten. Für Entwicklungsumgebungen mit Zugang zu sensiblen Daten sollten diese Kontrollen auch in diesen Umgebungen angewendet werden.
Ein aktuelles Inventar von Komponenten mit einer Software-Bill-of-Materials (SBOM) pflegen, um sicherzustellen, dass Sie ein aktuelles, präzises und signiertes Inventar haben, das Manipulationen an bereitgestellten Paketen verhindert. SBOMs können verwendet werden, um schnell neue, Zero-Day-Schwachstellen zu erkennen und zu melden.
Zum Zeitpunkt des Schreibens decken SBOMs keine Modelle, ihre Artefakte und Datensätze ab. Wenn Ihre LLM-Anwendung ihr eigenes Modell verwendet, sollten Sie MLOps-Best Practices und Plattformen verwenden, die sichere Modellrepositories mit Daten-, Modell- und Experiment-Tracking bieten.
Sie sollten auch Modell- und Code-Signierung verwenden, wenn Sie externe Modelle und Lieferanten verwenden.
Anomalieerkennung und Tests auf adversarielle Robustheit bei bereitgestellten Modellen und Daten können helfen, Manipulationen und Vergiftungen zu erkennen, wie in Trainingsdaten-Vergiftung besprochen; idealerweise sollte dies Teil von MLOps-Pipelines sein; jedoch sind dies aufkommende Techniken und können möglicherweise einfacher als Teil von Red-Teaming-Übungen implementiert werden.
Ausreichendes Monitoring implementieren, um das Scannen von Komponenten und Umgebungsschwachstellen, die Verwendung nicht autorisierter Plugins und veralteter Komponenten, einschließlich des Modells und seiner Artefakte, abzudecken.
Eine Patching-Richtlinie implementieren, um anfällige oder veraltete Komponenten zu mildern. Sicherstellen, dass die Anwendung auf eine gepflegte Version von APIs und dem zugrunde liegenden Modell angewiesen ist.
Sicherheit und Zugangskontrollen der Lieferanten regelmäßig überprüfen und auditieren, um sicherzustellen, dass es keine Änderungen in ihrer Sicherheitslage oder AGBs gibt.

### Beispiel-Angriffsszenarien

Ein Angreifer nutzt eine anfällige Python-Bibliothek, um ein System zu kompromittieren. Dies geschah beim ersten Datenleck von OpenAI.
Ein Angreifer bietet ein LLM-Plugin zur Flugsuche an, das gefälschte Links generiert, die Benutzer zu Scams dirigieren.
Ein Angreifer nutzt das PyPi-Paketregister aus, um Modellentwickler dazu zu bringen, ein kompromittiertes Paket herunterzuladen und Daten zu exfiltrieren oder Privilegien in einer Modellentwicklungsumgebung zu eskalieren. Dies war ein tatsächlicher Angriff.
Ein Angreifer vergiftet ein öffentlich verfügbares vortrainiertes Modell, das auf Wirtschaftsanalyse und Sozialforschung spezialisiert ist, um eine Hintertür zu schaffen, die Falschinformationen und Fake News generiert. Sie stellen es auf einem Modellmarktplatz (z.B. Hugging Face) zur Verfügung, damit Opfer es verwenden.
Ein Angreifer vergiftet öffentlich verfügbare Datensätze, um beim Feintuning von Modellen eine Hintertür zu schaffen. Die Hintertür bevorzugt subtil bestimmte Unternehmen in verschiedenen Märkten.
Ein kompromittierter Mitarbeiter eines Lieferanten (Outsourcing-Entwickler, Hosting-Unternehmen usw.) exfiltriert Daten, Modell oder Code und stiehlt geistiges Eigentum.
Ein LLM-Betreiber ändert seine AGBs und Datenschutzrichtlinie, um ein explizites Opt-out aus der Verwendung von Anwendungsdaten für das Modelltraining zu verlangen, was zur Speicherung sensibler Daten führt.

### Referenzlinks

ChatGPT-Datenleck bestätigt, da Sicherheitsfirma vor anfälliger Komponentenausnutzung warnt: Security Week
Plugin-Überprüfungsprozess OpenAI
Kompromittierte PyTorch-nightly-Abhängigkeitskette: Pytorch
PoisonGPT: Wie wir ein lobotomisiertes LLM auf Hugging Face versteckt haben, um Fake News zu verbreiten: Mithril Security
Army erwägt die Möglichkeit von 'AI BOMs: Defense Scoop
Fehlermodi im Maschinellen Lernen: Microsoft
ML-Lieferkettenkompromiss: MITRE ATLAS
Transferierbarkeit im Maschinellen Lernen: von Phänomenen zu Black-Box-Angriffen mit adversariellen Beispielen: Arxiv White Paper
BadNets: Identifizierung von Schwachstellen in der Lieferkette des Maschinellen Lernmodells: Arxiv White Paper
VirusTotal Poisoning: MITRE ATLAS
## LLM06: Offenlegung sensibler Informationen

### Beschreibung

LLM-Anwendungen (Large Language Models) können das Potenzial haben, sensible Informationen, proprietäre Algorithmen oder andere vertrauliche Details durch ihre Ausgabe zu offenbaren. Dies kann zu unbefugtem Zugriff auf sensible Daten, geistiges Eigentum, Verletzungen der Privatsphäre und anderen Sicherheitsverstößen führen. Es ist wichtig für Nutzer von LLM-Anwendungen, sich darüber im Klaren zu sein, wie sie sicher mit LLMs interagieren und die Risiken erkennen können, die mit der unbeabsichtigten Eingabe sensibler Daten verbunden sind, die anschließend von der LLM in der Ausgabe anderswo zurückgegeben werden könnten.

Um dieses Risiko zu mindern, sollten LLM-Anwendungen eine angemessene Datenbereinigung (PII-Scrubbing) durchführen, um zu verhindern, dass Benutzerdaten in die Trainingsdaten des Modells gelangen. Eigentümer von LLM-Anwendungen sollten auch angemessene Nutzungsbedingungen zur Verfügung stellen, um Verbraucher darüber zu informieren, wie ihre Daten verarbeitet werden, und die Möglichkeit bieten, sich dagegen zu entscheiden, dass ihre Daten in das Trainingsmodell aufgenommen werden.

Die Interaktion zwischen Verbraucher und LLM-Anwendung bildet eine Zwei-Wege-Vertrauensgrenze, bei der wir das Client->LLM-Eingabe oder das LLM->Client-Ausgabe nicht grundsätzlich vertrauen können. Es ist wichtig zu beachten, dass diese Schwachstelle davon ausgeht, dass bestimmte Voraussetzungen außerhalb des Geltungsbereichs liegen, wie Bedrohungsmodellierungsübungen, Sicherung der Infrastruktur und angemessene Sandboxing. Das Hinzufügen von Einschränkungen innerhalb des Systemprompts bezüglich der Arten von Daten, die das LLM zurückgeben sollte, kann eine gewisse Milderung gegen die Offenlegung sensibler Informationen bieten, aber die unvorhersehbare Natur der LLMs bedeutet, dass solche Einschränkungen möglicherweise nicht immer eingehalten werden und durch Prompt-Injektion oder andere Vektoren umgangen werden könnten.

### Häufige Beispiele für Schwachstellen

Unvollständige oder unsachgemäße Filterung sensibler Informationen in den Antworten des LLMs.
Overfitting oder Memorierung sensibler Daten im Trainingsprozess des LLMs.
Unbeabsichtigte Offenlegung vertraulicher Informationen aufgrund von Fehlinterpretationen des LLMs, mangelnden Datenbereinigungsmethoden oder Fehlern.

### Strategien zur Prävention und Milderung

Integriere angemessene Datenbereinigungs- und Scrubbing-Techniken, um zu verhindern, dass Benutzerdaten in die Trainingsdaten des Modells gelangen.
Implementiere robuste Eingabevalidierungs- und Sanitisierungsmethoden, um potenziell bösartige Eingaben zu identifizieren und herauszufiltern, um zu verhindern, dass das Modell vergiftet wird.
Wenn das Modell mit Daten angereichert und feinabgestimmt wird: (z.B. Daten, die dem Modell vor oder während der Bereitstellung zugeführt werden)
Alles, was in den Feinabstimmungsdaten als sensibel erachtet wird, hat das Potenzial, einem Benutzer offenbart zu werden. Wende daher die Regel des geringsten Privilegs an und trainiere das Modell nicht mit Informationen, auf die der am höchsten privilegierte Benutzer zugreifen kann und die einem Benutzer mit niedrigeren Privilegien angezeigt werden können.
Der Zugang zu externen Datenquellen (Orchestrierung von Daten zur Laufzeit) sollte begrenzt werden.
Wende strenge Zugangskontrollmethoden für externe Datenquellen an und verfolge einen rigorosen Ansatz zur Aufrechterhaltung einer sicheren Lieferkette.

### Beispielszenarien für Angriffe

Ein ahnungsloser legitimer Benutzer A wird bestimmten anderen Benutzerdaten über das LLM ausgesetzt, wenn er auf nicht bösartige Weise mit der LLM-Anwendung interagiert.
Benutzer A zielt auf eine sorgfältig erstellte Reihe von Prompts, um Eingabefilter und Sanitisierungsmaßnahmen des LLMs zu umgehen, damit es sensible Informationen (PII) über andere Benutzer der Anwendung preisgibt.
Persönliche Daten wie PII werden aufgrund von Fahrlässigkeit des Benutzers selbst oder der LLM-Anwendung in das Modell über das Trainingsdaten geleakt. Dieser Fall könnte das Risiko und die Wahrscheinlichkeit von Szenario 1 oder 2 oben erhöhen.

### Referenzlinks

AI data leak crisis: New tool prevents company secrets from being fed to ChatGPT: Fox Business
Lessons learned from ChatGPT’s Samsung leak: Cybernews
Cohere - Terms Of Use Cohere
A threat modeling example: AI Village
OWASP AI Security and Privacy Guide: OWASP AI Security & Privacy Guide
Ensuring the Security of Large Language Models: Experts Exchange
## LLM07: Unsicheres Plugin-Design

### Beschreibung

LLM-Plugins sind Erweiterungen, die bei Bedarf automatisch vom Modell während der Benutzerinteraktionen aufgerufen werden. Die Modellintegrationsplattform steuert sie, und die Anwendung hat möglicherweise keine Kontrolle über die Ausführung, insbesondere wenn das Modell von einer anderen Partei gehostet wird. Darüber hinaus implementieren Plugins wahrscheinlich Freitexteingaben vom Modell ohne Validierung oder Typüberprüfung, um mit Begrenzungen der Kontextgröße umzugehen. Dies ermöglicht einem potenziellen Angreifer, eine bösartige Anfrage an das Plugin zu konstruieren, die zu einer breiten Palette unerwünschter Verhaltensweisen führen kann, bis hin zur Ausführung von Remote-Code.

Der Schaden durch bösartige Eingaben hängt oft von unzureichenden Zugriffskontrollen und dem Versäumnis ab, die Autorisierung über Plugins hinweg zu verfolgen. Unzureichende Zugriffskontrolle ermöglicht es einem Plugin, anderen Plugins blind zu vertrauen und anzunehmen, dass die Eingaben vom Endbenutzer bereitgestellt wurden. Solch eine unzureichende Zugriffskontrolle kann ermöglichen, dass bösartige Eingaben schädliche Konsequenzen haben, von der Datenausfiltrierung, Ausführung von Remote-Code und Eskalation von Privilegien.

Dieser Punkt konzentriert sich auf die Erstellung von LLM-Plugins anstatt auf Drittanbieter-Plugins, die von LLM-Supply-Chain-Vulnerabilities abgedeckt werden.

### Häufige Beispiele für Verwundbarkeiten

Ein Plugin akzeptiert alle Parameter in einem einzigen Textfeld anstatt in getrennten Eingabeparametern.
Ein Plugin akzeptiert Konfigurationsstrings anstatt von Parametern, die gesamte Konfigurationseinstellungen überschreiben können.
Ein Plugin akzeptiert rohe SQL- oder Programmieranweisungen anstatt von Parametern.
Die Authentifizierung erfolgt ohne explizite Autorisierung für ein bestimmtes Plugin.
Ein Plugin behandelt alle LLM-Inhalte, als wären sie vollständig vom Benutzer erstellt, und führt jede angeforderte Aktion ohne zusätzliche Autorisierung aus.

### Präventions- und Minderungsstrategien

Plugins sollten streng parametrisierte Eingaben durchsetzen, wo immer möglich, und Typ- und Bereichsprüfungen für Eingaben einschließen. Wenn dies nicht möglich ist, sollte eine zweite Schicht von typisierten Aufrufen eingeführt werden, die Anfragen analysiert und Validierung und Sanitierung anwendet. Wenn Freiformeingaben aufgrund der Anwendungssemantik akzeptiert werden müssen, sollten sie sorgfältig inspiziert werden, um sicherzustellen, dass keine potenziell schädlichen Methoden aufgerufen werden.
Plugin-Entwickler sollten OWASPs Empfehlungen im ASVS (Application Security Verification Standard) anwenden, um eine angemessene Eingabevalidierung und -sanitierung zu gewährleisten.
Plugins sollten gründlich inspiziert und getestet werden, um eine angemessene Validierung sicherzustellen. Verwenden Sie Static Application Security Testing (SAST)-Scans und dynamische und interaktive Anwendungstests (DAST, IAST) in Entwicklungs-Pipelines.
Plugins sollten so konzipiert sein, dass sie die Auswirkungen einer Ausnutzung unsicherer Eingabeparameter minimieren, den OWASP ASVS Access Control Guidelines folgend. Dies umfasst Zugriffskontrolle mit minimalen Rechten, indem so wenig Funktionalität wie möglich freigelegt wird, während sie immer noch ihre gewünschte Funktion erfüllt.
Plugins sollten geeignete eigene Authentifizierungsidentitäten, wie OAuth2, verwenden, um eine effektive Autorisierung und Zugriffskontrolle anzuwenden. Zusätzlich sollten API-Schlüssel verwendet werden, um den Kontext für benutzerdefinierte Autorisierungsentscheidungen zu bieten, die den Plugin-Pfad anstelle des standardmäßigen interaktiven Benutzers widerspiegeln.
Plugins sollen manuelle Benutzerautorisierung und Bestätigung von jeder Aktion, die von sensiblen Plugins durchgeführt wird, erfordern.
Plugins sind oft REST-APIs, daher sollten Entwickler die Empfehlungen in OWASP Top 10 API Security Risks – 2023 anwenden, um generische Verwundbarkeiten zu minimieren.

### Beispiel-Angriffsszenarien

Ein Plugin akzeptiert eine Basis-URL und weist das LLM an, die URL mit einer Abfrage zu kombinieren, um Wettervorhersagen zu erhalten, die in die Bearbeitung der Benutzeranfrage einbezogen werden. Ein bösartiger Benutzer kann eine Anfrage so gestalten, dass die URL auf eine Domain zeigt, die sie kontrollieren, was es ihnen ermöglicht, ihren eigenen Inhalt über ihre Domain in das LLM-System einzuspeisen.
Ein Plugin akzeptiert eine Freiformeingabe in einem einzelnen Feld, das es nicht validiert. Ein Angreifer liefert sorgfältig gestaltete Payloads, um aus Fehlermeldungen Aufklärung zu betreiben. Anschließend werden bekannte Schwachstellen von Drittanbietern ausgenutzt, um Code auszuführen und Datenexfiltrierung oder Privilegienerweiterung durchzuführen.
Ein Plugin, das zum Abrufen von Einbettungen aus einem Vektorspeicher verwendet wird, akzeptiert Konfigurationsparameter als Verbindungsstring ohne jegliche Validierung. Dies ermöglicht es einem Angreifer, zu experimentieren und auf andere Vektorspeicher zuzugreifen, indem Namen oder Hostparameter geändert werden, und Einbettungen zu exfiltrieren, zu denen sie keinen Zugang haben sollten.
Ein Plugin akzeptiert SQL WHERE-Klauseln als erweiterte Filter, die dann an das Filter-SQL angehängt werden. Dies ermöglicht es einem Angreifer, einen SQL-Angriff zu inszenieren.
Ein Angreifer nutzt die indirekte Prompt-Injektion, um ein unsicheres Codeverwaltungs-Plugin ohne Eingabevalidierung und schwache Zugriffskontrolle auszunutzen, um das Repository-Eigentum zu übertragen und den Benutzer von ihren Repositories auszuschließen.

### Referenzen

OpenAI ChatGPT Plugins: ChatGPT Developer’s Guide
OpenAI ChatGPT Plugins - Plugin Flow: OpenAI Documentation
OpenAI ChatGPT Plugins - Authentication: OpenAI Documentation
OpenAI Semantic Search Plugin Sample: OpenAI Github
Plugin Vulnerabilities: Visit a Website and Have Your Source Code Stolen: Embrace The Red
ChatGPT Plugin Exploit Explained: From Prompt Injection to Accessing Private Data Embrace The Red
ChatGPT Plugin Exploit Explained: From Prompt Injection to Accessing Private Data: Embrace The Red
OWASP ASVS - 5 Validation, Sanitization and Encoding: OWASP AASVS
OWASP ASVS 4.1 General Access Control Design: OWASP AASVS
OWASP Top 10 API Security Risks – 2023: OWASP
## LLM08: Übermäßige Handlungsfreiheit

### Beschreibung

Ein auf LLM (Language Model) basierendes System wird oft mit einem gewissen Maß an Handlungsfreiheit durch seinen Entwickler ausgestattet - der Fähigkeit, mit anderen Systemen zu interagieren und auf eine Aufforderung hin Handlungen zu unternehmen. Die Entscheidung darüber, welche Funktionen aufgerufen werden sollen, kann auch an einen LLM 'Agenten' delegiert werden, um dynamisch basierend auf der Eingabeaufforderung oder dem LLM-Ausgang zu bestimmen.

Übermäßige Handlungsfreiheit ist die Schwachstelle, die es ermöglicht, schädliche Aktionen in Reaktion auf unerwartete/unklare Ausgaben von einem LLM durchzuführen (unabhängig davon, was den LLM fehlerhaft macht; sei es Halluzination/Konfabulation, direkte/indirekte Aufforderungsinjektion, bösartiges Plugin, schlecht konstruierte gutartige Aufforderungen oder einfach ein schlecht funktionierendes Modell). Die Hauptursache für übermäßige Handlungsfreiheit ist typischerweise eine oder mehrere der folgenden: übermäßige Funktionalität, übermäßige Berechtigungen oder übermäßige Autonomie. Dies unterscheidet sich von unsicherer Ausgabeverarbeitung, die sich mit unzureichender Prüfung von LLM-Ausgaben beschäftigt.

Übermäßige Handlungsfreiheit kann zu einer breiten Palette von Auswirkungen über das Spektrum von Vertraulichkeit, Integrität und Verfügbarkeit führen und hängt davon ab, mit welchen Systemen eine LLM-basierte App interagieren kann.

### Häufige Beispiele für Schwachstellen

Übermäßige Funktionalität: Ein LLM-Agent hat Zugriff auf Plugins, die Funktionen beinhalten, die für den beabsichtigten Betrieb des Systems nicht benötigt werden. Zum Beispiel muss ein Entwickler einem LLM-Agenten die Fähigkeit gewähren, Dokumente aus einem Repository zu lesen, aber das Plugin eines Drittanbieters, das sie verwenden, beinhaltet auch die Fähigkeit, Dokumente zu modifizieren und zu löschen.
Übermäßige Funktionalität: Ein Plugin wurde während einer Entwicklungsphase getestet und zugunsten einer besseren Alternative fallengelassen, aber das ursprüngliche Plugin bleibt dem LLM-Agenten zugänglich.
Übermäßige Funktionalität: Ein LLM-Plugin mit offenem Funktionsumfang filtert die Eingabeanweisungen für Befehle außerhalb dessen, was für den beabsichtigten Betrieb der Anwendung notwendig ist, nicht ordnungsgemäß. Z.B. ein Plugin zum Ausführen eines bestimmten Shell-Befehls verhindert nicht ordnungsgemäß, dass andere Shell-Befehle ausgeführt werden.
Übermäßige Berechtigungen: Ein LLM-Plugin hat Berechtigungen für andere Systeme, die für den beabsichtigten Betrieb der Anwendung nicht benötigt werden. Z.B. verbindet sich ein Plugin, das zum Lesen von Daten gedacht ist, mit einem Datenbankserver unter Verwendung einer Identität, die nicht nur SELECT-Berechtigungen hat, sondern auch UPDATE, INSERT und DELETE-Berechtigungen.
Übermäßige Berechtigungen: Ein LLM-Plugin, das entwickelt wurde, um Operationen im Namen eines Benutzers durchzuführen, greift auf nachgelagerte Systeme mit einer generischen hochprivilegierten Identität zu. Z.B. verbindet sich ein Plugin, um den aktuellen Dokumentenspeicher eines Benutzers zu lesen, mit dem Dokumentenrepository mit einem privilegierten Konto, das Zugriff auf alle Dateien der Benutzer hat.
Übermäßige Autonomie: Eine LLM-basierte Anwendung oder ein Plugin versäumt es, hochwirksame Aktionen unabhängig zu überprüfen und zu genehmigen. Z.B. führt ein Plugin, das es ermöglicht, Dokumente eines Benutzers zu löschen, Löschungen ohne jegliche Bestätigung vom Benutzer durch.

### Präventions- und Mitigierungsstrategien

Die folgenden Aktionen können übermäßige Handlungsfreiheit verhindern:

Beschränken Sie die Plugins/Tools, die LLM-Agenten aufrufen dürfen, auf nur die minimal notwendigen Funktionen. Wenn ein auf LLM basierendes System beispielsweise nicht die Fähigkeit benötigt, den Inhalt einer URL abzurufen, sollte ein solches Plugin dem LLM-Agenten nicht angeboten werden.
Beschränken Sie die Funktionen, die in LLM-Plugins/Tools implementiert sind, auf das minimal Notwendige. Ein Plugin, das auf das Postfach eines Benutzers zugreift, um E-Mails zusammenzufassen, benötigt möglicherweise nur die Fähigkeit, E-Mails zu lesen, daher sollte das Plugin keine andere Funktionalität wie das Löschen oder Senden von Nachrichten enthalten.
Vermeiden Sie nach Möglichkeit offene Funktionen (z.B. Ausführen eines Shell-Befehls, Abrufen einer URL usw.) und verwenden Sie Plugins/Tools mit granularerer Funktionalität. Wenn eine LLM-basierte App beispielsweise einige Ausgaben in eine Datei schreiben muss. Wenn dies mit einem Plugin zum Ausführen einer Shell-Funktion implementiert würde, wäre der Spielraum für unerwünschte Aktionen sehr groß (jeder andere Shell-Befehl könnte ausgeführt werden). Eine sicherere Alternative wäre, ein Dateischreib-Plugin zu erstellen, das nur diese spezifische Funktionalität unterstützen könnte.
Beschränken Sie die Berechtigungen, die LLM-Plugins/Tools anderen Systemen gewährt werden, auf das minimal Notwendige, um den Umfang unerwünschter Aktionen zu begrenzen. Ein LLM-Agent, der eine Produkt-Datenbank verwendet, um einem Kunden Kaufempfehlungen zu geben, benötigt beispielsweise möglicherweise nur Lesezugriff auf eine 'Produkte'-Tabelle; er sollte keinen Zugriff auf andere Tabellen haben, noch die Fähigkeit, Datensätze einzufügen, zu aktualisieren oder zu löschen. Dies sollte durch die Anwendung geeigneter Datenbankberechtigungen für die Identität durchgesetzt werden, die das LLM-Plugin verwendet, um sich mit der Datenbank zu verbinden.
Verfolgen Sie die Benutzerautorisierung und den Sicherheitsumfang, um sicherzustellen, dass im Namen eines Benutzers durchgeführte Aktionen auf nachgelagerten Systemen im Kontext dieses spezifischen Benutzers und mit den minimal notwendigen Privilegien ausgeführt werden. Ein LLM-Plugin, das das Code-Repo eines Benutzers liest, sollte beispielsweise erfordern, dass sich der Benutzer über OAuth authentifiziert und mit dem minimal erforderlichen Umfang.
Nutzen Sie die Steuerung durch den Menschen, um eine menschliche Genehmigung für alle Aktionen zu erfordern, bevor sie durchgeführt werden. Dies kann in einem nachgelagerten System (außerhalb des Geltungsbereichs der LLM-Anwendung) oder innerhalb des LLM-Plugins/Tools selbst implementiert werden. Ein LLM-basiertes App, das soziale Medieninhalte im Namen eines Benutzers erstellt und postet, sollte beispielsweise eine Benutzergenehmigungsroutine innerhalb des Plugins/Tools/API enthalten, das die 'Post'-Operation implementiert.
Implementieren Sie Autorisierung in nachgelagerten Systemen, anstatt sich auf ein LLM zu verlassen, um zu entscheiden, ob eine Aktion erlaubt ist oder nicht. Bei der Implementierung von Tools/Plugins den Grundsatz der vollständigen Vermittlung durchsetzen, so dass alle Anfragen, die über die Plugins/Tools an nachgelagerte Systeme gestellt werden, gegen Sicherheitsrichtlinien validiert werden.

Die folgenden Optionen verhindern keine übermäßige Handlungsfreiheit, können jedoch das Ausmaß des Schadens begrenzen:

Protokollieren und überwachen Sie die Aktivität von LLM-Plugins/Tools und nachgelagerten Systemen, um zu identifizieren, wo unerwünschte Aktionen stattfinden, und entsprechend reagieren.
Implementieren Sie Ratenbegrenzung, um die Anzahl unerwünschter Aktionen, die innerhalb eines bestimmten Zeitraums stattfinden können, zu reduzieren und die Möglichkeit zu erhöhen, unerwünschte Aktionen durch Überwachung zu entdecken, bevor erheblicher Schaden entstehen kann.

### Beispielangriffsszenarien

Eine LLM-basierte persönliche Assistenten-App erhält Zugriff auf das Postfach einer Person über ein Plugin, um den Inhalt eingehender E-Mails zusammenzufassen. Um diese Funktionalität zu erreichen, benötigt das E-Mail-Plugin die Fähigkeit, Nachrichten zu lesen. Das Plugin, das der Systementwickler gewählt hat, enthält jedoch auch Funktionen zum Senden von Nachrichten. Das LLM ist anfällig für einen indirekten Aufforderungsinjektionsangriff, bei dem eine bösartig gestaltete eingehende E-Mail das LLM dazu verleitet, das E-Mail-Plugin zu befehlen, die Funktion 'Nachricht senden' aufzurufen, um Spam aus dem Postfach des Benutzers zu senden. Dies könnte vermieden werden durch:
(a) Eliminierung übermäßiger Funktionalität durch Verwendung eines Plugins, das nur E-Mail-Lesefähigkeiten anbot,
(b) Eliminierung übermäßiger Berechtigungen durch Authentifizierung beim E-Mail-Dienst des Benutzers über eine OAuth-Sitzung mit einem schreibgeschützten Umfang und/oder
(c) Eliminierung übermäßiger Autonomie, indem der Benutzer jede vom LLM-Plugin entworfene Mail manuell überprüfen und auf 'Senden' klicken muss.
Alternativ könnte der verursachte Schaden durch Implementierung einer Ratenbegrenzung an der Mail-Sende-Schnittstelle reduziert werden.

### Referenzlinks

Embrace the Red: Confused Deputy Problem: Embrace The Red
NeMo-Guardrails: Interface guidelines: NVIDIA Github
LangChain: Human-approval for tools: Langchain Documentation
Simon Willison: Dual LLM Pattern: Simon Willison
## LLM09: Übermäßiges Vertrauen

### Beschreibung

Übermäßiges Vertrauen kann auftreten, wenn ein LLM fehlerhafte Informationen produziert und diese auf als Authorität  bereitstellt. Während LLMs kreative und informative Inhalte erzeugen können, können sie auch Inhalte generieren, die faktisch falsch, unangemessen oder unsicher sind. Dies wird als Halluzination oder Konfabulation bezeichnet. Wenn Menschen oder Systeme diesen Informationen ohne Aufsicht oder Bestätigung vertrauen, kann dies zu einem Sicherheitsbruch, Fehlinformationen, Misskommunikation, rechtlichen Problemen und Rufschädigung führen.

Von LLM generierter Quellcode kann unbemerkte Sicherheitsanfälligkeiten einführen. Dies stellt ein erhebliches Risiko für die betriebliche Sicherheit und Sicherheit von Anwendungen dar. Diese Risiken zeigen die Bedeutung von strengen Überprüfungsprozessen, mit:

Aufsicht
Kontinuierlichen Validierungsmechanismen
Haftungsausschlüssen bezüglich Risiken

### Häufige Beispiele für Anfälligkeiten

LLM liefert ungenaue Informationen als Antwort, während es so formuliert ist, als ob es sehr autoritär wäre. Das Gesamtsystem ist ohne angemessene Kontrollen und Gleichgewichte zur Handhabung dessen konzipiert, und die Informationen führen den Benutzer irreführend zu einem Schaden.
LLM schlägt unsicheren oder fehlerhaften Code vor, was zu Anfälligkeiten führt, wenn er ohne angemessene Aufsicht oder Überprüfung in ein Softwaresystem integriert wird.

### Präventions- und Minderungsstrategien

Überwachen und überprüfen Sie regelmäßig die Ausgaben des LLM. Verwenden Sie Selbstkonsistenz- oder Abstimmungstechniken, um inkonsistenten Text herauszufiltern. Das Vergleichen mehrerer Modellantworten auf eine einzelne Aufforderung kann eine bessere Beurteilung der Qualität und Konsistenz der Ausgabe ermöglichen.
Überprüfen Sie die Ausgaben des LLM mit vertrauenswürdigen externen Quellen. Diese zusätzliche Validierungsebene kann dabei helfen sicherzustellen, dass die vom Modell bereitgestellten Informationen genau und zuverlässig sind.
Verbessern Sie das Modell durch Feinabstimmung oder Einbettungen, um die Qualität der Ausgabe zu verbessern. Allgemeine vortrainierte Modelle produzieren im Vergleich zu abgestimmten Modellen in einem bestimmten Bereich wahrscheinlicher ungenaue Informationen. Techniken wie Prompt-Engineering, parameter-effizientes Tuning (PET), vollständiges Modelltuning und Chain-of-Thought-Prompting können für diesen Zweck eingesetzt werden.
Implementieren Sie automatische Validierungsmechanismen, die die generierte Ausgabe gegen bekannte Fakten oder Daten überprüfen können. Dies kann eine zusätzliche Sicherheitsebene bieten und die mit Halluzinationen verbundenen Risiken mindern.
Zerlegen Sie komplexe Aufgaben in handhabbare Unteraufgaben und weisen Sie sie verschiedenen Agenten zu. Dies hilft nicht nur bei der Bewältigung der Komplexität, sondern reduziert auch die Chancen auf Halluzinationen, da jeder Agent für eine kleinere Aufgabe verantwortlich gemacht werden kann.
Kommunizieren Sie klar die Risiken und Einschränkungen, die mit der Verwendung von LLMs verbunden sind. Dies beinhaltet das Potenzial für Informationsungenauigkeiten und andere Risiken. Eine effektive Risikokommunikation kann die Benutzer auf potenzielle Probleme vorbereiten und ihnen helfen, informierte Entscheidungen zu treffen.
Entwickeln Sie APIs und Benutzeroberflächen, die eine verantwortungsvolle und sichere Nutzung von LLMs fördern. Dies kann Maßnahmen wie Inhaltsfilter, Benutzerwarnungen vor potenziellen Ungenauigkeiten und eine klare Kennzeichnung von KI-generierten Inhalten umfassen.
Bei der Verwendung von LLMs in Entwicklungsumgebungen, etablieren Sie sichere Programmierpraktiken und Richtlinien, um die Integration möglicher Anfälligkeiten zu verhindern.

### Beispielangriffsszenarien

Eine Nachrichtenorganisation verwendet intensiv ein LLM, um Nachrichtenartikel zu generieren. Ein böswilliger Akteur nutzt diese übermäßige Abhängigkeit aus, indem er dem LLM irreführende Informationen füttert und so die Verbreitung von Fehlinformationen verursacht.
Die KI plagiiert unabsichtlich Inhalte, was zu Urheberrechtsproblemen und einem verringerten Vertrauen in die Organisation führt.
Ein Softwareentwicklungsteam nutzt ein LLM-System, um den Codierungsprozess zu beschleunigen. Die übermäßige Abhängigkeit von den Vorschlägen der KI führt aufgrund unsicherer Standardeinstellungen oder Empfehlungen, die nicht mit sicheren Programmierpraktiken übereinstimmen, zu Sicherheitsanfälligkeiten in der Anwendung.
Eine Softwareentwicklungsfirma verwendet ein LLM, um Entwickler zu unterstützen. Das LLM schlägt eine nicht existierende Code-Bibliothek oder ein Paket vor, und ein Entwickler, der der KI vertraut, integriert unwissentlich ein bösartiges Paket in die Software der Firma. Dies unterstreicht die Bedeutung der Überprüfung von LLM-Vorschlägen, insbesondere wenn es um Drittanbietercode oder -bibliotheken geht.

### Referenzlinks

Understanding LLM Hallucinations: Towards Data Science
How Should Companies Communicate the Risks of Large Language Models to Users?: Techpolicy
A news site used AI to write articles. It was a journalistic disaster: Washington Post
AI Hallucinations: Package Risk: Vulcan.io
How to Reduce the Hallucinations from Large Language Models: The New Stack
Practical Steps to Reduce Hallucination: Victor Debia
## LLM10: Modell-Diebstahl

### Beschreibung

Dieser Eintrag bezieht sich auf den unbefugten Zugriff und die Exfiltration von LLM-Modellen durch bösartige Akteure oder APTs (Advanced Persistent Threats). Dies tritt auf, wenn die proprietären LLM-Modelle (als wertvolles geistiges Eigentum) kompromittiert, physisch gestohlen, kopiert oder Gewichte und Parameter extrahiert werden, um ein funktionsfähiges Äquivalent zu erstellen. Die Auswirkungen des Diebstahls von LLM-Modellen können wirtschaftliche Verluste und Schäden am Markenimage, Erosion des Wettbewerbsvorteils, unbefugte Nutzung des Modells oder unbefugten Zugriff auf sensible Informationen, die im Modell enthalten sind, umfassen.

Der Diebstahl von LLMs stellt ein erhebliches Sicherheitsproblem dar, da Sprachmodelle immer leistungsfähiger und verbreiteter werden. Organisationen und Forscher müssen robuste Sicherheitsmaßnahmen priorisieren, um ihre LLM-Modelle zu schützen und die Vertraulichkeit und Integrität ihres geistigen Eigentums zu gewährleisten. Die Implementierung eines umfassenden Sicherheitsrahmens, der Zugriffskontrollen, Verschlüsselung und kontinuierliche Überwachung umfasst, ist entscheidend, um die Risiken im Zusammenhang mit dem Diebstahl von LLM-Modellen zu mindern und die Interessen von Einzelpersonen und Organisationen, die sich auf LLM verlassen, zu schützen.

### Häufige Beispiele für Schwachstellen

Ein Angreifer nutzt eine Schwachstelle in der Infrastruktur eines Unternehmens aus, um unbefugten Zugriff auf ihr LLM-Modell-Repository zu erhalten, durch Fehlkonfiguration in ihren Netzwerk- oder Anwendungssicherheitseinstellungen.
Ein Insider-Bedrohungsszenario, bei dem ein unzufriedener Mitarbeiter das Modell oder damit verbundene Artefakte durchsickern lässt.
Ein Angreifer verwendet die Modell-API mit sorgfältig erstellten Eingaben und Prompt-Injektionstechniken, um eine ausreichende Anzahl von Ausgaben zu sammeln, um ein Schattenmodell zu erstellen.
Ein bösartiger Angreifer kann Eingabefilterungstechniken des LLM umgehen, um einen Seitenkanalangriff durchzuführen und letztendlich Modellgewichte und Architekturinformationen zu einer ferngesteuerten Ressource zu übertragen.
Der Angriffsvektor für die Modell-Extraktion beinhaltet das Abfragen des LLM mit einer großen Anzahl von Prompts zu einem bestimmten Thema. Die Ausgaben aus dem LLM können dann verwendet werden, um ein anderes Modell zu verfeinern. Es gibt jedoch einige Dinge zu beachten bei diesem Angriff:
Der Angreifer muss eine große Anzahl von gezielten Prompts generieren. Wenn die Prompts nicht spezifisch genug sind, werden die Ausgaben aus dem LLM nutzlos sein.
Die Ausgaben aus LLMs können manchmal halluzinierte Antworten enthalten, was bedeutet, dass der Angreifer möglicherweise nicht das gesamte Modell extrahieren kann, da einige der Ausgaben unsinnig sein können.
Es ist nicht möglich, ein LLM zu 100% durch Modell-Extraktion zu replizieren. Der Angreifer wird jedoch in der Lage sein, ein teilweises Modell zu replizieren.
Der Angriffsvektor für _funktionale Modellreplikation_ beinhaltet die Verwendung des Zielmodells über Prompts, um synthetische Trainingsdaten zu generieren (ein Ansatz, der als "Selbstinstruktion" bezeichnet wird), um es dann zu verwenden und ein anderes grundlegendes Modell zu verfeinern und ein funktionales Äquivalent zu produzieren. Dies umgeht die Einschränkungen der traditionellen abfragebasierten Extraktion, die in Beispiel 5 verwendet wurde, und wurde erfolgreich in der Forschung über die Verwendung eines LLM zum Trainieren eines anderen LLM eingesetzt. Obwohl im Kontext dieser Forschung die Modellreplikation kein Angriff ist. Der Ansatz könnte von einem Angreifer verwendet werden, um ein proprietäres Modell mit einer öffentlichen API zu replizieren.

Die Verwendung eines gestohlenen Modells als Schattenmodell kann verwendet werden, um gegnerische Angriffe zu inszenieren, einschließlich unbefugtem Zugriff auf sensible Informationen, die im Modell enthalten sind, oder um unbemerkt mit gegnerischen Eingaben zu experimentieren, um weiter fortgeschrittene Prompt-Injektionen zu inszenieren.

### Präventions- und Mitigierungsstrategien

Implementieren Sie starke Zugriffskontrollen (z.B. RBAC und das Prinzip der geringsten Rechte) und starke Authentifizierungsmechanismen, um unbefugten Zugriff auf LLM-Modell-Repositories und Trainingsumgebungen zu begrenzen.
Dies gilt insbesondere für die ersten drei häufigen Beispiele, die diese Schwachstelle aufgrund von Insider-Bedrohungen, Fehlkonfigurationen und/oder schwachen Sicherheitskontrollen über die Infrastruktur, die LLM-Modelle, Gewichte und Architektur beherbergt, in der ein bösartiger Akteur aus dem Inneren oder von außen eindringen könnte, verursachen könnten.
Lieferantenmanagement-Tracking, Überprüfung und Abhängigkeitsschwachstellen sind wichtige Schwerpunktthemen, um Ausnutzungen von Supply-Chain-Angriffen zu verhindern.
Beschränken Sie den Zugriff des LLM auf Netzwerkressourcen, interne Dienste und APIs.
Dies gilt insbesondere für alle häufigen Beispiele, da es das Insider-Risiko und -Bedrohungen abdeckt, aber letztendlich auch kontrolliert, worauf die LLM-Anwendung "_Zugriff hat_", und somit ein Mechanismus oder Präventionsschritt sein könnte, um Seitenkanalangriffe zu verhindern.
Verwenden Sie ein zentrales ML-Modellinventar oder -Register für ML-Modelle, die in der Produktion verwendet werden. Ein zentrales Modellregister verhindert unbefugten Zugriff auf ML-Modelle über Zugriffskontrollen, Authentifizierung und Überwachungs-/Protokollierungsfähigkeit, die gute Grundlagen für Governance sind. Ein zentrales Repository ist auch vorteilhaft für die Sammlung von Daten über Algorithmen, die von den Modellen für Zwecke der Compliance, Risikobewertungen und Risikominderung verwendet werden.
Überwachen und prüfen Sie regelmäßig Zugriffsprotokolle und Aktivitäten im Zusammenhang mit LLM-Modell-Repositories, um verdächtiges oder unbefugtes Verhalten umgehend zu erkennen und darauf zu reagieren.
Automatisieren Sie MLOps-Bereitstellung mit Governance und Nachverfolgungs- und Genehmigungsworkflows, um Zugriffs- und Bereitstellungskontrollen innerhalb der Infrastruktur zu straffen.
Implementieren Sie Kontrollen und Minderungsstrategien, um das Risiko von Prompt-Injektionstechniken, die Seitenkanalangriffe verursachen, zu mindern und/oder zu reduzieren.
Rate Limiting von API-Aufrufen, wo anwendbar, und/oder Filter, um das Risiko der Datenexfiltration aus den LLM-Anwendungen zu reduzieren, oder implementieren Sie Techniken zur Erkennung (z.B. DLP) von Extraktionsaktivitäten aus anderen Überwachungssystemen.
Implementieren Sie Training zur gegnerischen Robustheit, um Extraktionsabfragen zu erkennen und physische Sicherheitsmaßnahmen zu straffen.
Implementieren Sie ein Wasserzeichen-Framework in die Einbettungs- und Erkennungsphasen des Lebenszyklus eines LLMs.

### Beispielangriffsszenarien

Ein Angreifer nutzt eine Schwachstelle in der Infrastruktur eines Unternehmens aus, um unbefugten Zugriff auf ihr LLM-Modell-Repository zu erhalten. Der Angreifer fährt fort, wertvolle LLM-Modelle zu exfiltrieren und verwendet sie, um einen konkurrierenden Sprachverarbeitungsdienst zu starten oder sensible Informationen zu extrahieren, was zu erheblichen finanziellen Schäden für das ursprüngliche Unternehmen führt.
Ein unzufriedener Mitarbeiter lässt das Modell oder damit verbundene Artefakte durchsickern. Die öffentliche Exposition dieses Szenarios erhöht das Wissen für Angreifer für Graukasten-gegnerische Angriffe oder alternativ direkt den Diebstahl des verfügbaren Eigentums.
Ein Angreifer fragt die API mit sorgfältig ausgewählten Eingaben ab und sammelt eine ausreichende Anzahl von Ausgaben, um ein Schattenmodell zu erstellen.
Ein Versagen der Sicherheitskontrolle ist innerhalb der Lieferkette vorhanden und führt zu Datenlecks von proprietären Modellinformationen.
Ein bösartiger Angreifer umgeht Eingabefilterungstechniken und Präambeln des LLM, um einen Seitenkanalangriff durchzuführen und Modellinformationen zu einer ferngesteuerten Ressource unter ihrer Kontrolle abzurufen.

### Referenz-Links

Meta’s powerful AI language model has leaked online: The Verge
Runaway LLaMA | How Meta's LLaMA NLP model leaked: Deep Learning Blog
AML.TA0000 ML Model Access: MITRE ATLAS
I Know What You See:: Arxiv White Paper
D-DAE: Defense-Penetrating Model Extraction Attacks:: Computer.org
A Comprehensive Defense Framework Against Model Extraction Attacks: IEEE
Alpaca: A Strong, Replicable Instruction-Following Model: Stanford Center on Research for Foundation Models (CRFM)
How Watermarking Can Help Mitigate The Potential Risks Of LLMs?: KD Nuggets

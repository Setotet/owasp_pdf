## Einleitung

### Entstehung der Liste

Das enorme Interesse an Large Language Models (LLMs) nach der Einführung massentauglicher, vortrainierten Chatbots Ende 2022 ist beachtlich. Unternehmen, die das Potenzial von LLMs nutzen wollen, integrieren sie rasch in ihre Geschäftsprozesse und kundenzugänglichen Angeboten. Die rasante Geschwindigkeit, mit der LLMs eingeführt werden, hat jedoch dazu geführt, dass die Etablierung umfassender Sicherheitsprotokolle in Verzug geraten ist, sodass viele Anwendungen mit hohen Risiken behaftet sind.

Das Fehlen einer einheitlichen Ressource, die diese Sicherheitsbedenken in Bezug auf LLMs adressiert, war offensichtlich. Entwicklerinnen und Entwickler, die mit den spezifischen Risiken von LLMs nicht vertraut waren, mussten sich auf diverse Quellen verlassen und die Mission von OWASP schien perfekt geeignet, um einen sichereren Einsatz dieser Technologie voranzutreiben.

### Zielgruppe

Unsere Hauptzielgruppe sind Entwickelnde, Data Scientists und Sicherheitsexpertinnen und -experten, die sich mit dem Design und der Entwicklung von Anwendungen und Plugins beschäftigen, die LLM-Technologien nutzen. Wir möchten praktische, umsetzbare und prägnante Sicherheitsempfehlungen bereitstellen, um diesen Fachleuten zu helfen, sich in dem komplexen und aufstrebenden Gebiet der Sicherheit von LLM-Anwendungen zurechtzufinden.

### Die Erstellung der Liste

Das Erstellen der OWASP Top 10 für LLM-Anwendungen war ein wichtiges Unterfangen, das auf der kollektiven Expertise eines internationalen Teams von fast 500 Expertinnen und Experten mit über 125 aktiven Mitgestaltenden basiert. Unsere Mitwirkenden kommen aus den unterschiedlichsten Bereichen, darunter KI-Unternehmen, Sicherheitsfirmen, ISVs, Cloud-Hyperscaler, Hardware-Anbieter und die akademische Welt.

Wir haben einen Monat lang gebrainstormt, potenzielle Schwachstellen vorgeschlagen und dabei 43 verschiedene Bedrohungen formuliert. In mehreren Abstimmungsrunden haben wir diese Vorschläge zu einer prägnanten Liste der zehn kritischsten Schwachstellen verfeinert. Spezialisierte Untergruppen untersuchten jede Schwachstelle und unterzogen sie einer öffentlichen Überprüfung, um sicherzustellen, dass die endgültige Liste so umfassend und nützlich wie möglich war.

### Das Verhältnis zu anderen OWASP Top 10 Listen

Während unsere Liste die DNA mit Schwachstellentypen aus anderen OWASP Top 10-Listen teilt, wiederholen wir diese Schwachstellen nicht einfach. Stattdessen fokussieren wir uns auf die einzigartigen Auswirkungen dieser Schwachstellen bei der Verwendung von LLMs.

Unser Ziel ist es, die Lücke zwischen allgemeinen Prinzipien der Anwendungssicherheit und den spezifischen Herausforderungen von LLMs zu schließen. Dies beinhaltet die Untersuchung, wie herkömmliche Schwachstellen in LLMs andere Risiken darstellen oder auf neue Weise ausgenutzt werden können und wie herkömmliche Abwehrmaßnahmen für LLM-basierte Anwendungen angepasst werden müssen.

### Die Zukunft

Version 1.1 der Liste wird nicht die letzte sein. Wir planen, sie regelmäßig zu aktualisieren, um mit den Entwicklungen in der Branche Schritt zu halten. Wir werden mit der erweiterten Community zusammenarbeiten, um den Stand der Technik voranzutreiben und mehr Schulungsmaterial für eine Vielzahl von Anwendungen zu erstellen. Ebenso streben wir auch die Zusammenarbeit mit Standardisierungsorganisationen und Regierungen in Fragen der KI-Sicherheit an. Sie sind herzlich eingeladen, sich unserer Gruppe anzuschließen und einen Beitrag zu leisten.

### Steve Wilson

Projektleiter, OWASP Top 10 für LLM-Anwendungen
[https://www.linkedin.com/in/wilsonsd](https://www.linkedin.com/in/wilsonsd/)  
Twitter/X: @virtualsteve

### Ads Dawson

v1.1 Release Lead & Vulnerability Entries Lead, OWASP Top 10 für LLM-Anwendungen
[https://www.linkedin.com/in/adamdawson0](https://www.linkedin.com/in/adamdawson0/) 
GitHub: @GangGreenTemperTatum

## Über diese Übersetzung

**Übersetzer**

Johann-Peter Hartmann
[https://www.linkedin.com/in/johann-peter-hartmann-92b70a/](https://www.linkedin.com/in/johann-peter-hartmann-92b70a/)  

Philippe Schrettenbrunner
[https://www.linkedin.com/in/philippe-schrettenbrunner/](https://www.linkedin.com/in/philippe-schrettenbrunner/)

Bei der Erstellung dieser Übersetzung haben wir uns bewusst dafür entschieden, nur menschliche Übersetzer einzusetzen, in Anerkennung der außerordentlich technischen und kritischen Natur der OWASP Top Ten für LLMs. Die oben aufgeführten Übersetzer verfügen nicht nur über ein tiefes Verständnis des Originalinhalts, sondern auch über die sprachliche Kompetenz, um diese Übersetzung sinnvoll zu gestalten.

Talesh Seeparsan
Übersetzungsleiter, OWASP Top 10 für LLM-Anwendungen
[https://www.linkedin.com/in/talesh/](https://www.linkedin.com/in/talesh/)  

## OWASP Top 10 für Anwendungen von Large Language Models (LLMs)

### LLM01: Prompt Injection (Prompt-Einschleusung)
Mittels raffinierter Eingaben kann ein Large Language Model manipuliert und unbeabsichtigte Aktionen ausgelöst werden. Direkte Injections überschreiben System-Prompts, während indirekte Eingaben von externen Quellen manipuliert werden.

### LLM02: Unsichere Ausgabeverarbeitung
Diese Schwachstelle tritt auf, wenn eine Ausgabe von einem LLM ungeprüft akzeptiert wird, wodurch Backend-Systeme angreifbar werden. Ein Missbrauch kann zu schwerwiegenden Folgen wie XSS (Cross-Site Scripting), CSRF (Cross-Site Request Forgery), SSRF (Server Side Request Forgery), Privilegienerweiterung oder Remote-Code-Ausführung führen.

### LLM03: Poisoning von Trainingsdaten
Dies tritt auf, wenn LLM-Trainingsdaten manipuliert werden und dadurch Sicherheitslücken oder Bias entstehen, die Sicherheit, Performance oder ethisches Verhalten beeinträchtigen. Quellen umfassen Common Crawl, WebText, OpenWebText und Bücher.

### LLM04: Denial of Service des Modells
Angreifende verursachen ressourcenintensive Operationen auf Large Language Models, was zu Beeinträchtigung oder hohen Kosten führt. Die Schwachstelle wird durch die ressourcenintensive Natur von LLMs und die Unvorhersehbarkeit von Benutzereingaben verstärkt.

### LLM05: Schwachstellen in der Lieferkette
Der Lebenszyklus von LLM-Anwendungen kann durch verwundbare Komponenten oder Dienste beeinträchtigt werden, was zu Sicherheitsangriffen führen kann. Die Verwendung von Datensätzen von Drittanbietern, vortrainierten Modellen und Plugins kann zu weiteren Schwachstellen führen.

### LLM06: Offenlegung sensibler Informationen
LLMs können in ihren Antworten vertrauliche Daten preisgeben, was zu unbefugtem Datenzugriff, Datenschutzverletzungen und Sicherheitsverstößen führt. Datenbereinigung und strenge Benutzerrichtlinien sind unerlässlich, um dies zu verhindern.

### LLM07: Unsicheres Plugin-Design
LLM-Plugins können unsichere Eingaben und unzureichende Zugriffskontrollen haben. Dieser Mangel an Anwendungskontrolle macht sie leichter ausnutzbar und kann zu Konsequenzen wie der Ausführung von Remote-Code führen.

### LLM08: Übermäßige Handlungsfreiheit
LLM-basierte Systeme können Aktionen ausführen, die zu unbeabsichtigten Konsequenzen führen. Das Problem entsteht durch übermäßige Funktionalität, Berechtigungen oder Autonomie, die LLM-basierten Systemen gewährt werden.

### LLM09: Übermäßige Abhängigkeit
Systeme oder Personen, die sich ohne angemessene Kontrolle zu sehr auf LLMs verlassen, können durch falsche oder unangemessene Inhalte, die von LLMs generiert werden, mit Fehlinformationen, Misskommunikation, rechtlichen Problemen und Sicherheitslücken konfrontiert werden.

### LLM10: Modell-Diebstahl
Dies umfasst den unbefugten Zugriff, das Kopieren oder die Exfiltration von proprietären LLM-Modellen. Die Folgen sind wirtschaftliche Verluste, Verlust von Wettbewerbsvorteilen und potenzieller Zugriff auf sensible Informationen.

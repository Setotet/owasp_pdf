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

Bei der Erstellung dieser Übersetzung haben wir uns bewusst dafür entschieden, nur menschliche Übersetzer einzusetzen, in Anerkennung der außerordentlich technischen und kritischen Natur der OWASP Top Ten für LLMs. Die oben aufgeführten Übersetzer verfügen nicht nur über ein tiefes Verständnis des Originalinhalts, sondern auch über die sprachliche Kompetenz, um diese Übersetzung sinnvoll zu gestalten.

Talesh Seeparsan
Übersetzungsleiter, OWASP Top 10 für LLM-Anwendungen
[https://www.linkedin.com/in/talesh/](https://www.linkedin.com/in/talesh/)  

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

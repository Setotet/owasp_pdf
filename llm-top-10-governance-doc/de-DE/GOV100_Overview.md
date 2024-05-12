## Übersicht

Jeder Internetnutzende und jedes Unternehmen muss sich auf die kommende Welle leistungsfähiger Anwendungen generativer künstlicher Intelligenz (GenAI) vorbereiten. GenAI verspricht enorme Innovationen, Effizienz und kommerzielle Vorteile in einer Vielzahl von Branchen. Doch wie jede leistungsstarke Technologie in einem frühen Entwicklungsstadium birgt sie ihre eigenen offensichtlichen und unerwarteten Herausforderungen.

Künstliche Intelligenz hat in den letzten 50 Jahren große Fortschritte gemacht und eine Vielzahl von Unternehmensprozessen unauffällig unterstützt, bis das öffentliche Erscheinen von ChatGPT die Entwicklung und Nutzung von Large Language Models (LLMs) sowohl bei Einzelpersonen als auch bei Unternehmen vorangetrieben hat. Anfangs waren diese Technologien auf akademische Studien oder die Ausführung bestimmter, aber wichtiger Aktivitäten innerhalb von Unternehmen beschränkt und nur für wenige Auserwählte sichtbar. Die jüngsten Fortschritte in der Verfügbarkeit von Daten, Computerleistung, GenAI-Fähigkeiten und die Veröffentlichung von Tools wie Llama 2, ElevenLabs und Midjourney haben AI jedoch von einer Nische zu einer allgemein weitverbreiteten Akzeptanz gebracht. Diese Verbesserungen haben nicht nur die GenAI-Technologien zugänglicher gemacht, sondern auch den kritischen Bedarf für Unternehmen erzeugt, solide Strategien für die Integration und Nutzung von AI in ihren Geschäftstätigkeiten zu entwickeln, was einen großen Schritt nach vorn in der Art und Weise darstellt, wie wir Technologie nutzen.

  - Künstliche Intelligenz ist ein breiter Begriff, der alle Bereiche der Informatik umfasst, in denen Maschinen Aufgaben auszuführen, die normalerweise menschliche Intelligenz erfordern würden. Maschinelles Lernen und generative AI sind zwei Unterkategorien von KI.
  - Maschinelles Lernen ist eine Unterkategorie von KI, die sich auf das Erstellen von Algorithmen konzentriert, die aus Daten lernen. Maschinelle Lernalgorithmen werden mit Datensätzen trainiert und können dann diese Daten verwenden, um Vorhersagen oder Entscheidungen für neue Daten zu treffen.
  - Generative AI ist eine Art von maschinellem Lernen, die sich auf das Generieren neuer Daten konzentriert. Oftmals stützt sich GenAI auf die Verwendung von Large Language Models, um die erforderlichen Aufgaben zur Erstellung der neuen Daten durchzuführen.
  - Ein Large Language Model (LLM) ist eine Art von KI-Modell, das menschenähnlich Text verarbeitet und generiert. Im Kontext der künstlichen Intelligenz bezieht sich ein "Modell" auf ein System, das trainiert wurde, um Vorhersagen basierend auf Eingabedaten zu treffen. LLMs werden speziell auf großen Datensätzen natürlicher Sprache trainiert, daher der Name Large Language Models.

Organisationen betreten bei der Sicherung und Überwachung von GenAI-Lösungen Neuland. Der schnelle Fortschritt von GenAI eröffnet auch Türen für Gegner, ihre Angriffsstrategien zu verbessern und stellt damit eine doppelte Herausforderung aus Verteidigung und Bedrohungseskalation dar.

Unternehmen verwenden künstliche Intelligenz in vielen Bereichen, einschließlich HR, Recruiting, E-Mail-Spam-Filterung, bei SIEM für Verhaltensanalysen und in Managed Detection and Response-Anwendungen. Der Schwerpunkt dieses Dokuments liegt jedoch auf Large Language Model-Anwendungen und ihrer Funktion bei der Erstellung generierter Inhalte.

### Verantwortungsvolle und vertrauenswürdige künstliche Intelligenz

Da Herausforderungen und Vorteile der künstlichen Intelligenz entstehen – und Vorschriften und Gesetze verabschiedet werden – entwickeln sich die Prinzipien und Säulen der verantwortungsvollen und vertrauenswürdigen KI-Nutzung von idealistischen Zielen und Bedenken kommend zu etablierten Standards.

[Die OWASP AI Exchange Working Group](https://owasp-ai-exchange.web.app/) verfolgt diese Veränderungen und geht die breitgefächerten und herausfordernden Überlegungen für alle Aspekte der künstlichen Intelligenz an.

>||center|16|16 Vertrauenswürdige künstliche Intelligenz

>indianred|white|left|14|18 ZUVERLÄSSIG
    >indianred|white|left|12|16 Robust
    >indianred|white|left|12|16 Verantwortlich
    >indianred|white|left|12|16 Überwacht
    >indianred|white|left|12|16 Transparent
    >indianred|white|left|12|16 Erklärbar

>forestgreen|white|left|14|18 RESILIENT
    >forestgreen|white|left|12|16 Sicher
    >forestgreen|white|left|12|16 Geschützt
    >forestgreen|white|left|12|16 Privat
    >forestgreen|white|left|12|16 Effektiv

>dodgerblue|white|left|14|18 VERANTWORTUNGSVOLL
    >dodgerblue|white|left|12|16 Fair
    >dodgerblue|white|left|12|16 Ethisch
    >dodgerblue|white|left|12|16 Inklusiv
    >dodgerblue|white|left|12|16 Nachhaltig
    >dodgerblue|white|left|12|16 Zweckmäßig

####$ Abbildung 1.1 Säulen der vertrauenswürdigen künstlichen Intelligenz
#####     erstellt vom Montreal Ethics Institute Beispiel

### Zielgruppe
Die OWASP Top 10 LLM AI Security & Governance Checkliste ist für Führungskräfte aus Exekutive, Technik, Cybersicherheit, Datenschutz, Compliance und Recht, DevSecOps, MLSecOps und Cybersicherheitsteams und Verteidiger gedacht. Sie richtet sich an Personen, die bestrebt sind, in der schnelllebigen KI-Welt einen Schritt voraus zu sein, mit dem Ziel, KI nicht nur für den Unternehmenserfolg zu nutzen, sondern auch gegen die Risiken überstürzter oder unsicherer KI-Implementierungen zu schützen. Diese Führungskräfte und Teams müssen Taktiken entwickeln, um Chancen zu ergreifen, Herausforderungen zu bekämpfen und Risiken zu mindern.

Diese Checkliste soll diesen Führungskräften aus Technologie und Business dabei helfen, schnell die Risiken und Vorteile der Nutzung von LLM zu verstehen und sich auf die Entwicklung einer umfassenden Liste kritischer Bereiche und Aufgaben zu konzentrieren, die benötigt werden, um die Organisation zu verteidigen und zu schützen, während sie eine Large Language Model-Strategie entwickeln.

Es ist die Hoffnung des OWASP Top 10 für das LLM-Applikationen-Teams, dass diese Liste Organisationen hilft, ihre bestehenden Verteidigungstechniken zu verbessern und Techniken zu entwickeln, um die neuen Bedrohungen anzugehen, die aus der Nutzung dieser aufregenden Technologie resultieren.

### Warum eine Checkliste?

Checklisten, die zur Formulierung von Strategien verwendet werden, verbessern die Genauigkeit, definieren Ziele, bewahren die Einheitlichkeit und fördern zielgerichtetes, bedachtes Arbeiten, wodurch das Übersehen und Verpassen von Details reduziert wird. Die Nutzung einer Checkliste erhöht nicht nur das Vertrauen in eine sichere Einführung, sondern fördert auch zukünftige Organisationsinnovationen, indem sie eine einfache und effektive Möglichkeit für kontinuierliche Verbesserungen bietet.

### Einschränkung

Obwohl dieses Dokument Organisationen dabei unterstützen soll, eine anfängliche LLM-Strategie in einer sich schnell ändernden technischen, rechtlichen und regulatorischen Umgebung zu entwickeln, ist es nicht vollständig und deckt nicht jeden Anwendungsfall oder jede Verpflichtung ab. Die Nutzung dieses Dokuments soll Organisationen dazu anregen, Bewertungen und Praktiken über den Umfang der bereitgestellten Checkliste hinaus so zu erweitern, wie es für ihren Anwendungsfall oder ihre Zuständigkeit erforderlich ist.

### Die Herausforderungen von Large Language Models

Large Language Models stehen vor mehreren ernsthaften und einzigartigen Problemen. Eines der wichtigsten ist, dass  die Steuerungs- und Datenebenen beim Arbeiten mit LLMs nicht strikt isoliert oder trennbar sind. Zusätzlich sind LLMs von Natur aus nicht deterministisch und liefern beim gleichen Prompt unterschedliche Ergebnisse. LLMs verwenden semantische Suche anstelle einer Schlüsselwortsuche. Der Kernunterschied ist dabei, dass der Algorithmus des Modells die Begriffe in der Antwort priorisiert. Das ist eine deutliche Abweichung von der gewohnten Art und Weise, wie Verbraucher bisher Technologie genutzt haben, und es wirkt sich auf die Konsistenz und Zuverlässigkeit der Ergebnisse aus. Halluzinationen, die aus den Lücken und Fehlern der Trainingsdaten resultieren sind das Ergebnis dieser Methode.

Es gibt Strategien, um die Zuverlässigkeit zu verbessern und die Angriffsfläche für Jailbreaking, Modelltäuschungen und Halluzinationen zu reduzieren, aber im Ergebnis geht es um einen Kompromiss zwischen Einschränkungen und Nutzen bezüglich Kosten und Funktionalität.

Die Nutzung und Anwendung von LLMs erhöht die Angriffsfläche einer Organisation. Einige Risiken der Risiken von LLM-Applikationen sind einzigartig, aber viele von ihnen sind bekannte Problemfelder, wie die Software Bill of Materials (SBoM), die Lieferkette, Data Loss Protection (DLP) und unautorisierter Zugriff. Dazu kommen verstärkte Risiken, die nicht direkt mit GenAI zusammenhängen, bei denen GenAI aber die Effizienz, Fähigkeit und Wirksamkeit von Angreifern, die Organisationen, Einzelpersonen und Regierungssysteme angreifen und bedrohen erhöht.

Angreifer nutzen zunehmend LLM- und Generative AI-Tools, um traditionelle Methoden des Angriffs auf Organisationen, Einzelpersonen und Behörden zu verbessern und zu beschleunigen. LLMs verbessern ihre Fähigkeit, Techniken zu verfeinern, um mühelos neue Malware zu erstellen, die möglicherweise mit neuartigen Zero-Day-Schwachstellen eingebettet ist oder darauf ausgelegt ist, die Erkennung zu umgehen. Sie können auch ausgeklügelte, einzigartige oder maßgeschneiderte Phishing-Schemata generieren. Die Erstellung überzeugender Deepfakes, sei es Video oder Audio, vereinfacht Social-Engineering. Zusätzlich vereinfachen diese Tools Einbrüche und die Entwicklung innovativer Hacking-Fähigkeiten. In Zukunft wird der „maßgeschneiderte“ und kombinierte Einsatz von KI-Technologie durch kriminelle Akteure eigene Antworten und dedizierte Lösungen für die angemessene Verteidigung und Widerstandsfähigkeit der Organisationen erfordern.

Organisationen gehen aber auch ein Risiko ein,wenn sie die Fähigkeiten von LLMs NICHT nutzen, und erzeugen damit einen Wettbewerbsnachteil. Sie werden auf dem Markt von Kunden und Partnern als veraltet und unfähig zum Skalieren personalisierter Kommunikation wahrgenommen. Ihnen wird Innovationsstagnation, betriebliche Ineffizienz, ein höheres Risiko durch menschlicher Fehler in Prozessen und ineffiziente Nutzung von menschlicher Arbeit unterstellt.

Das Verständnis der verschiedenen Arten von Bedrohungen und deren Integration in die Geschäftsstrategie hilft dabei, sowohl die Vor- als auch die Nachteile der Nutzung von Large Language Models (LLMs) gegenüber der Nichtnutzung abzuwägen und sicherzustellen, dass sie die Geschäftsziele beschleunigen und nicht behindern.

### LLM-Bedrohungskategorien

>||center|16|16 KI-Bedrohungskarte

    >cornflower|white|left|14|18 Bedrohungen durch NICHT-Nutzung von KI-Modellen
    >cornflower|white|left|14|18 Bedrohungen durch Nutzung von KI-Modellen
    >dodgerblue|white|left|14|18 Bedrohungen für KI-Modelle
    >fidblue|white|left|14|18 Bedrohungen durch KI-Modelle
    >darkblue|white|left|14|18 KI-rechtliche & regulatorische Bedrohungen

##### Abbildung 1.2 Arten von KI-Bedrohungen
>white|black|center Quelle: sdunn



### Schulungen zu Sicherheit und Datenschutz in der künstlichen Intelligenz

Mitarbeiter in Organisationen profitieren von Schulungen, um künstliche Intelligenz, generative künstliche Intelligenz und die zukünftigen potenziellen Konsequenzen des Aufbaus, Kaufs oder der Nutzung von LLMs zu verstehen. Schulungen für zulässige Nutzung und Sicherheitsbewusstsein sollten sich sowohl an alle Mitarbeiter richten als auch spezialisiert an bestimmte Bereiche wie Personalwesen, Rechtsabteilung, Entwickler, Datenteams und Sicherheitsteams sein.

Richtlinien für faire Nutzung und gesunde Interaktion sind Schlüsselaspekte, die ein Eckpfeiler für den Erfolg zukünftiger KI-Cybersicherheitsbewusstseinskampagnen sein werden, wenn man sie von Anfang an integriert. Sir werden den Benutzern das Wissen über die grundlegenden Regeln für die Interaktion sowie die Fähigkeit vermitteln und gutes von schlechtem oder unethischem Verhalten zu unterscheiden.

##$ Integration von LLM-Sicherheit und -Governance mit bestehenden,
###   etablierten Praktiken und Kontrollen

Obw ohl KI und generative KI eine neue Dimension zu Cybersicherheit, Resilienz, Datenschutz und der Erfüllung rechtlicher und regulatorischer Anforderungen hinzufügen, sind die lang existierenden bewährten Praktiken immer noch der beste Weg, um Probleme zu identifizieren, Schwachstellen zu finden, diese zu beheben und potenzielle Sicherheitsprobleme zu reduzieren.

  ● Stellen Sie sicher, dass das Management von KI-Systemen mit bestehenden organisatorischen Praktiken integriert ist.
  ● Stellen Sie sicher, dass KI/ML-Systeme bestehenden Datenschutz-, Governance- und Sicherheitspraktiken folgen und bei Bedarf spezifische KI-Datenschutz-, Governance- und Sicherheitspraktiken implementiert werden.

### Grundlegende Sicherheitsprinzipien

LLM-Fähigkeiten führen neue Varianten von Angriffen und Angriffsflächen ein. LLMs sind anfällig für komplexe Geschäftslogikfehler, wie z. B. Prompt-Injektion, unsicheres Plugin-Design und Remote-Code-Ausführung. Existierende Best Practices sind der beste Weg, um diese Probleme zu lösen. Ein internes Produktsicherheitsteam, das sichere Softwareüberprüfung, Architektur, Data-Governance und Drittanbieterbewertungen versteht, muss überprüfen, wie geeignet die existierenden Mechanismen sind, um Probleme zu finden, die durch LLM verschärf werden könnten, wie z. B. Stimmklonung, Personifizierung oder das Umgehen von Captchas.

Angesichts der aktuellen Fortschritte im maschinellen Lernen, NLP (Natural Language Processing), NLU (Natural Language Understanding), Deep Learning und in jüngster Zeit LLMs (Large Language Models) und Generative AI wird empfohlen, Fachleute aus in diesen Bereichen in Cybersicherheits- und Devops-Teams einzubeziehen. Ihre Expertise wird nicht nur bei der Einführung dieser Technologien, sondern auch bei der Entwicklung innovativer Analysen und Antworten auf neu entstehende Herausforderungen helfen.

### Risiko

Der Verweis auf Risiko verwendet die Definition as ISO 31000: Risiko = "Effekt der Unsicherheit auf Ziele." Zu den in der Checkliste enthaltenen LLM-Risiken gehören gegnerische, sicherheitstechnische, rechtliche, regulatorische, rufschädigende, finanzielle und wettbewerbliche Risiken.

### Schwachstellen- und Mitigationstaxonomie

Aktuelle Systeme zur Klassifizierung von Schwachstellen und zum Austausch von Bedrohungsinformationen, wie etwa OVAL, STIX, CVE und CWE, arbeiten noch an der  Fähigkeit, spezifische Schwachstellen und Bedrohungen in Bezug auf große Sprachmodelle (LLMs) und Prediction-Modelle zu überwachen und die Verteidiger zu alarmieren. Es wird erwartet, dass Organisationen sich auf diese etablierten und anerkannten Standards wie CVE für die Klassifizierung von Schwachstellen und STIX für den Austausch von Informationen über Cyber-Bedrohungen (CTI) stützen werden, wenn Schwachstellen oder Bedrohungen für KI/ML-Systeme und deren Lieferketten identifiziert werden.
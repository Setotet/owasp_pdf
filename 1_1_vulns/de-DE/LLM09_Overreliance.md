## LLM09: Übermäßiges Vertrauen

### Beschreibung

Übermäßiges Vertrauen kann auftreten, wenn ein LLM fehlerhafte Informationen produziert und diese als korrekt darstellt. Während LLMs kreative und informative Inhalte erzeugen können, können sie auch Inhalte generieren, die faktisch falsch, unangemessen oder unsicher sind. Dies wird als Halluzination oder Konfabulation bezeichnet. Wenn Menschen oder Systeme diesen Informationen ohne Kontrolle oder Nachprüfung vertrauen, kann dies zu Sicherheitslücken, Fehlinformationen, Misskommunikation, rechtlichen Problemen oder Rufschädigung führen.

Durch LLMs generierter Quellcode kann unbemerkt Sicherheitslücken einführen. Dies stellt ein erhebliches Risiko für die betriebliche Sicherheit und Sicherheit von Anwendungen dar. Diese Risiken zeigen die Bedeutung von strengen Überprüfungsprozessen, mit:

* Kontrollen
* Kontinuierlichen Validierungsmechanismen
* Haftungsausschlüssen bezüglich Risiken

### Häufige Beispiele für Anfälligkeiten

1. LLMs liefern inkorrekte Informationen als Antwort, die durch ihre Formulierung korrekt wirken. In einem System ohne saubere Gewaltenteilung erhält der Nutzer irreführende Informationen, die zu seinem Schaden führen.
2. LLMs generieren unsicheren oder fehlerhaften Code, der zu Sicherheitslücken führt, wenn er ohne angemessene Aufsicht oder Überprüfung in eine Software integriert wird.

### Präventions- und Mitigationsstrategien

1. Überwachen und überprüfen Sie regelmäßig die Ausgaben des LLMs. Verwenden Sie Selbstkonsistenz- oder Votingmechanismen, um inkonsistenten Text herauszufiltern. Das Vergleichen der Antworten mehrerer Modelle für den gleichen Prompt kann eine bessere Beurteilung der Qualität und Konsistenz der Ausgabe ermöglichen.
2. Überprüfen Sie die Ausgaben des LLM mit vertrauenswürdigen externen Quellen. Diese zusätzliche Validierungsebene kann dabei helfen sicherzustellen, dass die vom Modell bereitgestellten Informationen akkurat und zuverlässig sind.
3. Verbessern Sie das Modell durch Finetuning oder Embeddings, um die Qualität der Ausgabe zu verbessern. Allgemeine vortrainierte Modelle produzieren im Vergleich zu auf einen bestimmten Bereich spezialisierten Modellen  wahrscheinlicher ungenaue Informationen. Techniken wie Prompt-Engineering, parameter-effizientes Tuning (PET), vollständiges Modelltuning und Chain-of-Thought-Prompting können für diesen Zweck eingesetzt werden.
4. Implementieren Sie automatische Validierungsmechanismen, die die generierte Ausgabe gegen bekannte Fakten oder Daten überprüfen können. Dies kann eine zusätzliche Sicherheitsebene bieten und die mit Halluzinationen verbundenen Risiken mindern.
5. Zerlegen Sie komplexe Aufgaben in handhabbare Unteraufgaben und weisen Sie sie verschiedenen Agenten zu. Dies hilft nicht nur bei der Bewältigung der Komplexität, sondern reduziert auch die Chancen auf Halluzinationen, da jeder Agent für eine kleinere Aufgabe verantwortlich gemacht werden kann.
6. Kommunizieren Sie klar die Risiken und Einschränkungen, die mit der Verwendung von LLMs verbunden sind. Dies beinhaltet das Potenzial für Informationsungenauigkeiten und andere Risiken. Eine effektive Risikokommunikation kann die Benutzer auf potenzielle Probleme vorbereiten und ihnen helfen, informierte Entscheidungen zu treffen.
7. Entwickeln Sie APIs und Benutzeroberflächen, die eine verantwortungsvolle und sichere Nutzung von LLMs fördern. Dies kann Maßnahmen wie Inhaltsfilter, Benutzerwarnungen vor potenziellen Ungenauigkeiten und eine klare Kennzeichnung von KI-generierten Inhalten umfassen.
8. Bei der Verwendung von LLMs in Entwicklungsumgebungen, etablieren Sie sichere Programmierpraktiken und Richtlinien, um die Integration möglicher Anfälligkeiten zu verhindern.

### Beispiele für Angriffsszenarien

1. Eine Nachrichtenorganisation verwendet intensiv ein LLM, um Nachrichtenartikel zu generieren. Ein böswilliger Akteur nutzt diese übermäßige Abhängigkeit aus, indem er dem LLM irreführende Informationen füttert und so die Verbreitung von Fehlinformationen verursacht.
2. Die KI plagiiert unabsichtlich Inhalte, was zu Urheberrechtsproblemen und einem verringerten Vertrauen in die Organisation führt.
3. Ein Softwareentwicklungsteam nutzt ein LLM-System, um das Programmieren zu beschleunigen. Die übermäßige Abhängigkeit von den Vorschlägen der KI führt aufgrund unsicherer Defaults oder Empfehlungen ohne sichere Programmierpraktiken zu Sicherheitslücken in der Anwendung.
4. Eine Softwareentwicklungsfirma verwendet ein LLM, um Entwickler zu unterstützen. Das LLM schlägt eine nicht existierende Code-Bibliothek oder ein Paket vor, und ein Entwickler, der der KI vertraut, integriert unwissentlich ein bösartiges Paket in die Software der Firma. Dies unterstreicht die Bedeutung der Überprüfung von LLM-Vorschlägen, insbesondere wenn es um Drittanbietercode oder -bibliotheken geht.

### Referenzlinks

1. [Understanding LLM Hallucinations](https://towardsdatascience.com/llm-hallucinations-ec831dcd7786): **Towards Data Science**
2. [How Should Companies Communicate the Risks of Large Language Models to Users?](https://techpolicy.press/how-should-companies-communicate-the-risks-of-large-language-models-to-users/): **Techpolicy**
3. [A news site used AI to write articles. It was a journalistic disaster](https://www.washingtonpost.com/media/2023/01/17/cnet-ai-articles-journalism-corrections/): **Washington Post**
4. [AI Hallucinations: Package Risk](https://vulcan.io/blog/ai-hallucinations-package-risk): **Vulcan.io**
5. [How to Reduce the Hallucinations from Large Language Models](https://thenewstack.io/how-to-reduce-the-hallucinations-from-large-language-models/): **The New Stack**
6. [Practical Steps to Reduce Hallucination](https://newsletter.victordibia.com/p/practical-steps-to-reduce-hallucination): **Victor Debia**

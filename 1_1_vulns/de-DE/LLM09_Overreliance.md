## LLM09: Übermäßiges Vertrauen

### Beschreibung

Übermäßiges Vertrauen kann entstehen, wenn ein LLM falsche Informationen produziert und diese als Autorität verbreitet. Während LLMs kreative und informative Inhalte produzieren können, können sie auch Inhalte produzieren, die faktisch falsch, unangemessen oder unsicher sind. Dies wird als Halluzination oder Konfabulation bezeichnet. Wenn Menschen oder Systeme diesen Informationen ohne Aufsicht oder Bestätigung vertrauen, kann dies zu Sicherheitsverletzungen, Fehlinformationen, Fehlkommunikation, rechtlichen Problemen und Rufschädigung führen.

Von LLM erzeugter Quellcode kann unbemerkt Sicherheitslücken einführen. Dies stellt ein erhebliches Risiko für die Betriebs- und Anwendungssicherheit dar. Diese Risiken unterstreichen die Bedeutung strenger Verifikationsprozesse:

* Überwachung
* Kontinuierliche Validierungsmechanismen
* Haftungsausschlüsse für Risiken

### Häufige Beispiele für Anfälligkeiten

1. Das LLM liefert ungenaue Informationen als Antwort, während es sehr autoritär formuliert ist. Das gesamte System ist ohne angemessene Kontrollen und Gleichgewichte für den Umgang damit konzipiert, und die Informationen führen den Benutzer in die Irre.
2. LLM schlägt unsicheren oder fehlerhaften Code vor, der zu Schwachstellen führt, wenn er ohne angemessene Kontrolle oder Überprüfung in ein Softwaresystem integriert wird.

### Präventions- und Minderungsstrategien

1. Überwachen und überprüfen Sie regelmäßig die Ausgaben des LLM. Verwenden Sie Selbstkonsistenz- oder Abgleichtechniken, um inkonsistenten Text herauszufiltern. Der Vergleich mehrerer Musterantworten auf eine Anfrage kann eine bessere Beurteilung der Qualität und Konsistenz der Ausgabe ermöglichen.
2. Überprüfen Sie die Ausgabe des LLM mit vertrauenswürdigen externen Quellen. Diese zusätzliche Validierungsebene kann helfen sicherzustellen, dass die vom Modell gelieferten Informationen genau und zuverlässig sind.
3. Verbessern Sie das Modell durch Feinabstimmung oder Einbettungen, um die Qualität der Ausgabe zu verbessern. Allgemeine vortrainierte Modelle neigen eher dazu, ungenaue Informationen zu liefern, als Modelle, die auf einen bestimmten Bereich abgestimmt sind. Techniken wie Prompt-Engineering, parameter-effizientes Tuning (PET), vollständiges Modelltuning und Chain-of-Thought-Prompting können zu diesem Zweck eingesetzt werden.
4. Implementieren Sie automatische Validierungsmechanismen, die die generierte Ausgabe mit bekannten Fakten oder Daten vergleichen können. Dies kann eine zusätzliche Sicherheitsebene bieten und die mit Halluzinationen verbundenen Risiken verringern.
5. Zerlegen Sie komplexe Aufgaben in handhabbare Unteraufgaben und weisen Sie sie verschiedenen Agenten zu. Dies hilft nicht nur bei der Bewältigung der Komplexität, sondern verringert auch die Wahrscheinlichkeit von Halluzinationen, da jeder Agent für eine kleinere Aufgabe verantwortlich gemacht werden kann.
6. Kommunizieren Sie klar die Risiken und Einschränkungen, die mit der Verwendung von LLMs verbunden sind. Dies schließt das Potenzial für Informationsungenauigkeiten und andere Risiken ein. Eine effektive Risikokommunikation kann die Nutzer auf mögliche Probleme vorbereiten und ihnen helfen, informierte Entscheidungen zu treffen. 7. Entwickeln Sie APIs und Benutzeroberflächen, die eine verantwortungsvolle und sichere Nutzung von LLMs fördern. Dies kann Maßnahmen wie Inhaltsfilter, Benutzerwarnungen vor potenziellen Ungenauigkeiten und eine klare Kennzeichnung von KI-generierten Inhalten umfassen.
8. Bei der Verwendung von LLMs in Entwicklungsumgebungen sichere Programmierpraktiken und -richtlinien einzuführen, um die Integration potenzieller Schwachstellen zu verhindern.

### Beispiele für Angriffsszenarien

1. Eine Nachrichtenorganisation nutzt ein LLM intensiv, um Nachrichtenartikel zu generieren. Ein böswilliger Akteur nutzt diese übermäßige Abhängigkeit aus, indem er das LLM mit irreführenden Informationen füttert und so die Verbreitung von Fehlinformationen verursacht.
2. Die KI plagiiert unbeabsichtigt Inhalte, was zu Urheberrechtsproblemen und einem Vertrauensverlust in die Organisation führt.
3. Ein Softwareentwicklungsteam verwendet ein LLM-System, um den Kodierungsprozess zu beschleunigen. Die übermäßige Abhängigkeit von den Vorschlägen der KI führt zu Sicherheitslücken in der Anwendung aufgrund unsicherer Standardeinstellungen oder Empfehlungen, die nicht sicheren Programmierpraktiken entsprechen.
4. Eine Softwareentwicklungsfirma verwendet ein LLM, um Entwickler zu unterstützen. Das LLM schlägt eine nicht existierende Codebibliothek oder ein nicht existierendes Paket vor, und ein Entwickler, der der KI vertraut, integriert unwissentlich ein schädliches Paket in die Software des Unternehmens. Dies unterstreicht die Bedeutung der Überprüfung von LLM-Vorschlägen, insbesondere wenn es sich um Code oder Bibliotheken von Drittanbietern handelt.

### Referenzlinks

1. [Understanding LLM Hallucinations](https://towardsdatascience.com/llm-hallucinations-ec831dcd7786): **Towards Data Science**
2. [How Should Companies Communicate the Risks of Large Language Models to Users?](https://techpolicy.press/how-should-companies-communicate-the-risks-of-large-language-models-to-users/): **Techpolicy**
3. [A news site used AI to write articles. It was a journalistic disaster](https://www.washingtonpost.com/media/2023/01/17/cnet-ai-articles-journalism-corrections/): **Washington Post**
4. [AI Hallucinations: Package Risk](https://vulcan.io/blog/ai-hallucinations-package-risk): **Vulcan.io**
5. [How to Reduce the Hallucinations from Large Language Models](https://thenewstack.io/how-to-reduce-the-hallucinations-from-large-language-models/): **The New Stack**
6. [Practical Steps to Reduce Hallucination](https://newsletter.victordibia.com/p/practical-steps-to-reduce-hallucination): **Victor Debia**

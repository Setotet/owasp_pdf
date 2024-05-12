## LLM05: Schwachstellen in der Lieferkette

### Beschreibung

Die Lieferkette in LLMs kann anfällig sein und die Integrität von Trainingsdaten, ML-Modellen und Bereitstellungsplattformen beeinträchtigen. Diese Schwachstellen können zu verzerrten Ergebnissen, Sicherheitsverletzungen oder sogar zu kompletten Systemausfällen führen. Traditionell konzentrieren sich Schwachstellen auf Softwarekomponenten, aber beim maschinellen Lernen kommen vortrainierte Modelle und Trainingsdaten von Drittanbietern hinzu, die anfällig für Manipulations- und Vergiftungsangriffe sind.

Schließlich können LLM-Plugin-Erweiterungen ihre eigenen Schwachstellen mitbringen. Diese werden in [LLM07 - Unsicheres Plugin-Design](InsecurePluginDesign.md) beschrieben, das das Schreiben von LLM-Plugins abdeckt und nützliche Informationen zur Bewertung von Plugins von Drittanbietern liefert.

### Häufige Beispiele für Schwachstellen

1. Traditionelle Schwachstellen in Paketen von Drittanbietern, einschließlich veralteter oder nicht mehr unterstützter Komponenten.
2. Verwendung eines anfälligen, vortrainierten Modells für das Feintuning.
3. Verwendung vergifteter Crowd-Sourced-Daten für das Training.
4. Verwendung veralteter oder nicht mehr unterstützter Modelle, die nicht mehr gewartet werden und zu Sicherheitsproblemen führen.
5. Unklare AGB und Datenschutzrichtlinien der Modellbetreiber führen dazu, dass sensible Daten der Anwendung für das Modelltraining verwendet werden und anschließend sensible Informationen preisgegeben werden. Dies kann auch für Risiken gelten, die sich aus der Verwendung von urheberrechtlich geschütztem Material durch den Modellanbieter ergeben.

### Strategien zur Prävention und Mitigation

1. Datenquellen und -anbieter sorgfältig prüfen, einschließlich der Allgemeinen Geschäftsbedingungen und der Datenschutzrichtlinien; nur vertrauenswürdige Anbieter verwenden. Stellen Sie sicher, dass angemessene und unabhängig geprüfte Sicherheit vorhanden ist und dass die Richtlinien des Modellanbieters mit Ihren Datenschutzrichtlinien übereinstimmen, d.h. dass Ihre Daten nicht für das Training ihrer Modelle verwendet werden.
2. Verwenden Sie nur seriöse Plugins und stellen Sie sicher, dass diese für Ihre Anwendungsanforderungen getestet wurden. LLM Unsicheres Plugin-Design bietet Informationen über die LLM-Aspekte eines unsicheren Plugin-Designs, gegen die Sie testen sollten, um die Risiken bei der Verwendung von Plugins Dritter zu minimieren.
3. die in den OWASP Top 10 [A06:2021 - Vulnerable and Outdated Components] (https://owasp.org/Top10/A06_2021-Vulnerable_and_Outdated_Components/) identifizierten Abhilfemaßnahmen zu verstehen und anzuwenden. Dies beinhaltet das Scannen, Verwalten und Patchen von Komponenten. Für Entwicklungsumgebungen mit Zugriff auf sensible Daten sollten diese Kontrollen auch in diesen Umgebungen angewendet werden.
4. Führen Sie ein aktuelles Inventar der Komponenten mit einem Software Bill of Materials (SBOM), um sicherzustellen, dass Sie über ein aktuelles, genaues und signiertes Inventar verfügen, das Manipulationen an bereitgestellten Paketen verhindert. SBOMs können verwendet werden, um neue Zero-Day-Schwachstellen schnell zu identifizieren und zu melden.
5. Zum Zeitpunkt der Erstellung decken SBOMs keine Modelle, deren Artefakte und Datensätze ab. Wenn Ihre LLM-Anwendung ein eigenes Modell verwendet, sollten Sie die MLOps Best Practices und Plattformen verwenden, die sichere Modell-Repositories mit Daten-, Modell- und Experimentverfolgung bieten.
6. Sie sollten auch Modell- und Codesignatur verwenden, wenn Sie externe Modelle und Anbieter verwenden. 
7. Anomalieerkennung und Robustheitstests gegenüber angreiferischen Manipulationen bei bereitgestellten Modellen und Daten können helfen, Manipulationen und Vergiftungen zu erkennen, wie in [Trainingsdaten-Vergiftung](https://github.com/OWASP/www-project-top-10-for-large-language-model-applications/blob/main/1_0_vulns/Training_Data_Poisoning.md) besprochen; idealerweise sollte dies Teil von MLOps-Pipelines sein; jedoch sind dies aufkommende Techniken und können möglicherweise einfacher als Teil von Red-Teaming-Übungen implementiert werden.
8. Implementierung einer ausreichenden Überwachung, um das Scannen von Komponenten und Schwachstellen in der Umgebung, die Verwendung nicht autorisierter Plugins und veralteter Komponenten, einschließlich des Modells und seiner Artefakte, abzudecken.
9. Implementieren Sie eine Patching-Richtlinie, um anfällige oder veraltete Komponenten abzuschwächen. Sicherstellen, dass die Anwendung von einer gepflegten Version der APIs und des zugrundeliegenden Modells abhängig ist.
10. Sicherheits- und Zugangskontrollen der Lieferanten regelmäßig überprüfen und auditieren, um sicherzustellen, dass es keine Änderungen an ihrer Sicherheitslage oder ihren Geschäftsbedingungen gibt.

### Beispiele für Angriffsszenarien

1. Angreifende verwenden eine verwundbare Python-Bibliothek, um ein System zu kompromittieren. Dies geschah beim ersten OpenAI-Datenleck.
2. Angreifende bieten ein LLM-Plugin für die Flugsuche an, das gefälschte Links generiert, die Benutzer auf betrügerische Websites leiten.
3. Angreifende nutzen das PyPi-Paketregister aus, um Modellentwickler dazu zu bringen, ein kompromittiertes Paket herunterzuladen und Daten zu exfiltrieren oder Privilegien in einer Modellentwicklungsumgebung zu eskalieren. Dies war ein echter Angriff.
4. Angreifende vergiften ein öffentlich verfügbares vortrainiertes Modell, das auf Wirtschaftsanalyse und Sozialforschung spezialisiert ist, um eine Hintertür zu schaffen, die Falschinformationen und Fake News generiert. Er stellt das Modell auf einem Marktplatz für Modelle (z. B. Hugging Face) zur Verfügung, damit die Opfer es verwenden.
5. Angreifende vergiften öffentlich verfügbare Datensätze, um eine Hintertür bei der Feinabstimmung von Modellen zu schaffen. Die Hintertür begünstigt auf subtile Weise bestimmte Unternehmen in verschiedenen Märkten. 
6. Eine kompromittierte Person eines Lieferanten (Outsourcing-Entwickler, Hosting-Unternehmen usw.) exfiltriert Daten, Modell oder Code und stiehlt geistiges Eigentum.
7. Ein LLM-Betreiber ändert seine AGB und Datenschutzbestimmungen dahingehend, dass eine ausdrückliche Ablehnung der Verwendung von Anwendungsdaten für das Modelltraining erforderlich ist, was zur Speicherung sensibler Daten führt.

### Referenzlinks

1. [ChatGPT-Datenleck bestätigt, da Sicherheitsfirma vor anfälliger Komponentenausnutzung warnt](https://www.securityweek.com/chatgpt-data-breach-confirmed-as-security-firm-warns-of-vulnerable-component-exploitation/): **Security Week**
2. [Plugin-Überprüfungsprozess](https://platform.openai.com/docs/plugins/review) **OpenAI**
3. [Kompromittierte PyTorch-nightly-Abhängigkeitskette](https://pytorch.org/blog/compromised-nightly-dependency/): **Pytorch**
4. [PoisonGPT: Wie wir ein lobotomisiertes LLM auf Hugging Face versteckt haben, um Fake News zu verbreiten](https://blog.mithrilsecurity.io/poisongpt-how-we-hid-a-lobotomized-llm-on-hugging-face-to-spread-fake-news/): **Mithril Security**
5. [Army erwägt die Möglichkeit von 'AI BOMs](https://defensescoop.com/2023/05/25/army-looking-at-the-possibility-of-ai-boms-bill-of-materials/): **Defense Scoop**
6. [Fehlermodi im Maschinellen Lernen](https://learn.microsoft.com/en-us/security/engineering/failure-modes-in-machine-learning): **Microsoft**
7. [ML-Lieferkettenkompromiss](https://atlas.mitre.org/techniques/AML.T0010/): **MITRE ATLAS**
8. [Transferierbarkeit im Maschinellen Lernen: von Phänomenen zu Black-Box-Angriffen mit adversariellen Beispielen](https://arxiv.org/pdf/1605.07277.pdf): **Arxiv White Paper**
9. [BadNets: Identifizierung von Schwachstellen in der Lieferkette des Maschinellen Lernmodells](https://arxiv.org/abs/1708.06733): **Arxiv White Paper**
10. [VirusTotal Poisoning](https://atlas.mitre.org/studies/AML.CS0002): **MITRE ATLAS**

## LLM10: Modell-Diebstahl

### Beschreibung

Dieser Eintrag bezieht sich auf den unbefugten Zugriff und die Exfiltration von LLM-Modellen durch böswillige Akteure oder APTs (Advanced Persistent Threats). Dies geschieht, wenn proprietäre LLM-Modelle (als wertvolles geistiges Eigentum) kompromittiert, physisch gestohlen, kopiert oder Gewichte und Parameter extrahiert werden, um ein funktionsfähiges Äquivalent zu erstellen. Die Auswirkungen des Diebstahls von LLM-Modellen können wirtschaftliche Verluste und Imageschäden, die Erosion von Wettbewerbsvorteilen, die unbefugte Nutzung des Modells oder den unbefugten Zugriff auf sensible Informationen, die im Modell enthalten sind, umfassen.

Der Diebstahl von LLMs stellt ein erhebliches Sicherheitsproblem dar, da Sprachmodelle immer leistungsfähiger und weiter verbreitet werden. Organisationen und Forscher müssen robusten Sicherheitsmaßnahmen Priorität einräumen, um ihre LLM-Modelle zu schützen und die Vertraulichkeit und Integrität ihres geistigen Eigentums zu gewährleisten. Die Implementierung eines umfassenden Sicherheitsrahmens, der Zugriffskontrollen, Verschlüsselung und kontinuierliche Überwachung umfasst, ist entscheidend, um das Risiko des Diebstahls von LLM-Modellen zu verringern und die Interessen von Einzelpersonen und Organisationen zu schützen, die auf LLMs angewiesen sind.

### Häufige Beispiele für Schwachstellen

1. Angreifenden nutzen eine Schwachstelle in der Infrastruktur einer Organisation aus, um sich durch Fehlkonfiguration der Netzwerk- oder Anwendungssicherheitseinstellungen unberechtigten Zugriff auf das LLM-Modell-Repository zu verschaffen.
2. Ein Insider-Bedrohungsszenario, bei dem ein unzufriedener Mitarbeiter das Modell oder damit verbundene Artefakte nach außen dringen lässt.
3. Angreifenden verwenden die Modell-API mit sorgfältig erstellten Eingaben und Prompt-Injection-Techniken, um eine ausreichende Anzahl von Ausgaben zu sammeln, um ein Schattenmodell zu erstellen.
4. Böswillige Angreifenden können die Eingabefiltertechniken des LLM umgehen, um einen Seitenkanalangriff durchzuführen und schließlich Modellgewichte und Architekturinformationen an eine entfernte Ressource zu übertragen.
5. Der Angriffsvektor für die Extraktion von Modellen beinhaltet die Abfrage des LLM mit einer großen Anzahl von Prompts zu einem bestimmten Thema. Die Ausgabe des LLM kann dann verwendet werden, um ein anderes Modell zu verfeinern. Bei diesem Angriff sind jedoch einige Dinge zu beachten:
   - Angreifenden müssen eine große Anzahl spezifischer Prompts erzeugen. Wenn die Prompts nicht spezifisch genug sind, ist die Ausgabe des LLM nutzlos.
   - Die Ausgaben von LLMs können manchmal halluzinierte Antworten enthalten, was bedeutet, dass Angreifenden möglicherweise nicht in der Lage sind, das gesamte Modell zu extrahieren, da einige der Ausgaben sinnlos sein können.
   - Es ist nicht möglich, ein LLM zu 100 % durch Modellextraktion zu replizieren. Angreifenden werden jedoch in der Lage sein, ein Teilmodell zu replizieren.
6. Der Angriffsvektor für die **_funktionale Modellreplikation_** besteht darin, das Zielmodell über Prompts zu verwenden, um synthetische Trainingsdaten zu erzeugen (ein Ansatz, der als "Selbstinstruktion" bezeichnet wird), und diese dann zu verwenden, um ein anderes Basismodell zu verfeinern und ein funktionales Äquivalent zu erzeugen. Dieser Ansatz umgeht die Beschränkungen der traditionellen abfragebasierten Extraktion, die in Beispiel 5 verwendet wurde, und wurde erfolgreich in der Forschung über die Verwendung eines LLM zum Trainieren eines anderen LLM eingesetzt. Im Kontext dieser Forschung stellt die Modellreplikation keinen Angriff dar. Der Ansatz könnte von Angreifenden verwendet werden, um ein proprietäres Modell mit einer öffentlichen API zu replizieren.

Die Verwendung eines gestohlenen Modells als Schattenmodell kann dazu genutzt werden, Angriffe des Gegners zu inszenieren, einschließlich des unbefugten Zugriffs auf sensible Informationen, die im Modell enthalten sind, oder um unbemerkt mit Eingaben des Gegners zu experimentieren, um fortgeschrittenere Prompt-Injektionen zu inszenieren.

### Präventions- und Mitigierungsstrategien

1. starke Zugriffskontrollen (z. B. RBAC und das Prinzip der geringsten Rechte) und starke Authentifizierungsmechanismen implementieren, um den unbefugten Zugriff auf LLM-Modell-Repositories und Trainingsumgebungen zu beschränken.
   1. Dies gilt insbesondere für die ersten drei häufigen Beispiele, die diese Schwachstelle aufgrund von Insider-Bedrohungen, Fehlkonfigurationen und/oder schwachen Sicherheitskontrollen der Infrastruktur, die LLM-Modelle, -Gewichte und -Architektur beherbergt, verursachen könnten, in die ein böswilliger Akteur von innen oder außen eindringen könnte.
   2. die Nachverfolgbarkeit, die Verifizierung und die Schwachstellen im Lieferantenmanagement sind wichtige Schwerpunktthemen, um die Ausnutzung von Supply-Chain-Angriffen zu verhindern.
2. Beschränken Sie den Zugriff des LLM auf Netzwerkressourcen, interne Dienste und APIs.
   1. Dies gilt insbesondere für alle gängigen Beispiele, da es Risiken und Bedrohungen durch Insider abdeckt, aber letztlich auch kontrolliert, worauf die LLM-Anwendung "zugreifen" darf, und somit einen Mechanismus oder eine Präventivmaßnahme zur Verhinderung von Seitenkanalangriffen darstellen kann.
3. Verwenden Sie ein zentrales ML-Modellinventar oder -register für ML-Modelle, die in der Produktion verwendet werden. Ein zentrales Modellregister verhindert den unbefugten Zugriff auf ML-Modelle durch Zugriffskontrollen, Authentifizierung und Überwachungs-/Protokollierungsfähigkeiten, die gute Grundlagen für Governance sind. Ein zentrales Repository ist auch vorteilhaft, um Daten über die von den Modellen verwendeten Algorithmen für Zwecke der Compliance, Risikobewertung und Risikominderung zu sammeln.
4. Überwachen und prüfen Sie regelmäßig Zugriffsprotokolle und Aktivitäten im Zusammenhang mit LLM-Modell-Repositories, um verdächtiges oder unbefugtes Verhalten umgehend zu erkennen und darauf zu reagieren.
5. Automatisieren der MLOps-Bereitstellung mit Governance-, Nachverfolgungs- und Genehmigungsworkflows, um die Zugriffs- und Bereitstellungskontrollen innerhalb der Infrastruktur zu rationalisieren.
6. Implementieren Sie Kontrollen und Minderungsstrategien, um das Risiko von Prompt-Injection-Techniken, die Seitenkanalangriffe verursachen, zu mindern und/oder zu reduzieren.
7. ggf. Ratenbegrenzung von API-Aufrufen und/oder Filterung, um das Risiko der Datenexfiltration aus LLM-Anwendungen zu reduzieren, oder Implementierung von Techniken zur Erkennung (z. B. DLP) von Extraktionsaktivitäten aus anderen Überwachungssystemen.
8. Implementierung von Robustheitstrainings, um Extraktionsanfragen zu erkennen und physische Sicherheitsmaßnahmen zu verstärken.
9. Implementieren eines Wasserzeichen-Frameworks in den Einbettungs- und Erkennungsphasen des Lebenszyklus eines LLM.

### Beispiele für Angriffsszenarien

1. Angreifenden nutzen eine Schwachstelle in der Infrastruktur eines Unternehmens aus, um sich unberechtigten Zugriff auf dessen LLM-Modell-Repository zu verschaffen. Der Angreifer exfiltriert wertvolle LLM-Modelle und verwendet sie, um einen konkurrierenden Sprachverarbeitungsdienst zu starten oder sensible Informationen zu extrahieren, wodurch dem ursprünglichen Unternehmen erheblicher finanzieller Schaden entsteht.
2. Ein unzufriedener Mitarbeiter lässt das Modell oder damit verbundene Artefakte nach außen dringen. Das öffentliche Bekanntwerden dieses Szenarios erhöht das Wissen für Angreifende, die Gray-Box-Angriffe oder alternativ den direkten Diebstahl des verfügbaren Eigentums planen. 3. Ein Angreifer fragt die API mit sorgfältig ausgewählten Eingaben ab und sammelt eine ausreichende Anzahl von Ausgaben, um ein Schattenmodell zu erstellen.
4. Ein Versagen der Sicherheitskontrolle in der Lieferkette führt zum Abfluss von proprietären Modellinformationen.
5. Böswilliger Angreifende umgeht die Eingabefilterung und die Präambel des LLM, um einen Seitenkanalangriff durchzuführen und Modellinformationen über eine ferngesteuerte Ressource unter seiner Kontrolle zu erlangen.

### Referenz-Links

1. [Meta’s powerful AI language model has leaked online](https://www.theverge.com/2023/3/8/23629362/meta-ai-language-model-llama-leak-online-misuse): **The Verge**
2. [Runaway LLaMA | How Meta's LLaMA NLP model leaked](https://www.deeplearning.ai/the-batch/how-metas-llama-nlp-model-leaked/): **Deep Learning Blog**
3. [AML.TA0000 ML Model Access](https://atlas.mitre.org/tactics/AML.TA0000): **MITRE ATLAS**
4. [I Know What You See:](https://arxiv.org/pdf/1803.05847.pdf): **Arxiv White Paper**
5. [D-DAE: Defense-Penetrating Model Extraction Attacks:](https://www.computer.org/csdl/proceedings-article/sp/2023/933600a432/1He7YbsiH4c): **Computer.org**
6. [A Comprehensive Defense Framework Against Model Extraction Attacks](https://ieeexplore.ieee.org/document/10080996): **IEEE**
7. [Alpaca: A Strong, Replicable Instruction-Following Model](https://crfm.stanford.edu/2023/03/13/alpaca.html): **Stanford Center on Research for Foundation Models (CRFM)**
8. [How Watermarking Can Help Mitigate The Potential Risks Of LLMs?](https://www.kdnuggets.com/2023/03/watermarking-help-mitigate-potential-risks-llms.html): **KD Nuggets**

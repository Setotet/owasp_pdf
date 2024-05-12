## LLM06: Offenlegung sensibler Informationen

### Beschreibung

LLM-Anwendungen (Large Language Models) können das Potenzial haben, durch ihre Ausgabe sensible Informationen, proprietäre Algorithmen oder andere vertrauliche Details zu offenbaren. Dies kann zu unberechtigtem Zugriff auf sensible Daten, geistiges Eigentum, Verletzungen der Privatsphäre und anderen Sicherheitsverletzungen führen. Es ist wichtig, dass die Benutzerinnen und Benutzer von LLM-Anwendungen wissen, wie sie sicher mit LLMs interagieren können, und dass sie sich der Risiken bewusst sind, die mit der unbeabsichtigten Eingabe sensibler Daten verbunden sind, die dann von der LLM in der Ausgabe an anderer Stelle zurückgegeben werden können.

Um dieses Risiko zu mindern, sollten LLM-Anwendungen eine angemessene Datenbereinigung (PII-Scrubbing) durchführen, um zu verhindern, dass Benutzerdaten in die Trainingsdaten des Modells gelangen. Die Eigentümer von LLM-Anwendungen sollten auch angemessene Nutzungsbedingungen bereitstellen, um die Verbraucher darüber zu informieren, wie ihre Daten verarbeitet werden, und ihnen die Möglichkeit geben, die Einbeziehung ihrer Daten in das Trainingsmodell abzulehnen.

Die Interaktion zwischen Menschen und der LLM-Anwendung stellt eine Zwei-Wege-Vertrauensgrenze dar, bei der wir weder der Client->LLM-Eingabe noch der LLM->Client-Ausgabe grundsätzlich vertrauen können. Es ist wichtig anzumerken, dass diese Schwachstelle davon ausgeht, dass bestimmte Voraussetzungen, wie Bedrohungsmodellierungsübungen, Sicherung der Infrastruktur und angemessenes Sandboxing, nicht gegeben sind. Das Hinzufügen von Einschränkungen in der Systemabfrage bezüglich der Art der Daten, die das LLM zurückgeben soll, kann einen gewissen Schutz vor der Offenlegung sensibler Informationen bieten, aber die unvorhersehbare Natur von LLMs bedeutet, dass solche Einschränkungen möglicherweise nicht immer eingehalten werden und durch Prompt-Injection oder andere Vektoren umgangen werden können.

### Häufige Beispiele für Schwachstellen

1. Unvollständiges oder unangemessenes Filtern sensibler Informationen in den Antworten des LLM.
2. Überanpassung oder Speicherung sensibler Daten während des Trainingsprozesses des LLM.
3. Unbeabsichtigte Offenlegung vertraulicher Informationen aufgrund von Fehlinterpretationen durch den LLM, unzureichenden Datenbereinigungsmethoden oder Fehlern.

### Strategien zur Prävention und Milderung

1. Integration geeigneter Datenbereinigungs- und Scrubbing-Techniken, um zu verhindern, dass Benutzerdaten in die Trainingsdaten des Modells gelangen.
2. robuste Eingabevalidierungs- und -bereinigungsmethoden implementieren, um potenziell schädliche Eingaben zu identifizieren und herauszufiltern, damit das Modell nicht vergiftet wird.
3. Wenn das Modell mit Daten angereichert und [feinabgestimmt](https://github.com/OWASP/www-project-top-10-for-large-language-model-applications/wiki/Definitions) wird: (z. B. Daten, die dem Modell vor oder während der Bereitstellung zugeführt werden)
   1. Alles, was in den Feinabstimmungsdaten als sensibel eingestuft wird, kann einem Benutzer angezeigt werden. Daher sollte die Regel des geringsten Privilegs angewendet werden und das Modell nicht mit Informationen trainiert werden, auf die der Benutzer mit dem höchsten Privileg Zugriff hat und die einem Benutzer mit niedrigeren Privilegien angezeigt werden könnten.
   2. Der Zugriff auf externe Datenquellen (Orchestrierung von Daten zur Laufzeit) sollte eingeschränkt werden.
   3. Strenge Zugriffskontrollmethoden für externe Datenquellen anwenden und einen rigorosen Ansatz zur Aufrechterhaltung einer sicheren Lieferkette verfolgen.
### Beispielszenarien für Angriffe

1. Ein ahnungsloser, legitimer Benutzer A wird durch das LLM bestimmten Daten anderer Benutzer ausgesetzt, wenn er in nicht böswilliger Weise mit der LLM-Anwendung interagiert.
2. Benutzer A zielt darauf ab, durch eine sorgfältig ausgeklügelte Abfolge von Eingabeaufforderungen die Eingabefilter und Sanierungsmaßnahmen des LLM zu umgehen, um sensible Informationen (PII) über andere Benutzer der Anwendung preiszugeben.
3. Personenbezogene Daten (PII) werden aufgrund von Nachlässigkeit des Benutzers selbst oder der LLM-Anwendung über die Trainingsdaten an das Modell weitergegeben. Dieser Fall könnte das Risiko und die Wahrscheinlichkeit von Szenario 1 oder 2 oben erhöhen.

### Referenzlinks

1. [AI data leak crisis: New tool prevents company secrets from being fed to ChatGPT](https://www.foxbusiness.com/politics/ai-data-leak-crisis-prevent-company-secrets-chatgpt): **Fox Business**
2. [Lessons learned from ChatGPT’s Samsung leak](https://cybernews.com/security/chatgpt-samsung-leak-explained-lessons/): **Cybernews**
3. [Cohere - Terms Of Use](https://cohere.com/terms-of-use) **Cohere**
4. [A threat modeling example](https://aivillage.org/large%20language%20models/threat-modeling-llm/): **AI Village**
5. [OWASP AI Security and Privacy Guide](https://owasp.org/www-project-ai-security-and-privacy-guide/): **OWASP AI Security & Privacy Guide**
6. [Ensuring the Security of Large Language Models](https://www.experts-exchange.com/articles/38220/Ensuring-the-Security-of-Large-Language-Models-Strategies-and-Best-Practices.html): **Experts Exchange**

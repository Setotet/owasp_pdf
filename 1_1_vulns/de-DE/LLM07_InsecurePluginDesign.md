## LLM07: Unsicheres Plugin-Design

### Beschreibung

LLM-Plugins sind Erweiterungen, die bei Bedarf automatisch vom Modell während der Benutzerinteraktionen aufgerufen werden. Sie werden von der Modellintegrationsplattform gesteuert und die Anwendung hat möglicherweise keine Kontrolle über ihre Ausführung, insbesondere wenn das Modell von einer anderen Partei gehostet wird. Darüber hinaus implementieren Plugins wahrscheinlich Freitexteingaben aus dem Modell ohne Validierung oder Typüberprüfung, um mit Beschränkungen der Kontextgröße umzugehen. Dadurch können potenzielle Angreifende eine böswillige Anfrage an das Plugin konstruieren, die zu einem breiten Spektrum an unerwünschtem Verhalten bis hin zur Ausführung von Remote-Code führen kann.

Der Schaden, der durch böswillige Eingaben verursacht wird, hängt oft von unzureichenden Zugriffskontrollen und dem Versäumnis ab, die Autorisierung über Plugins hinweg zu verfolgen. Unzureichende Zugriffskontrollen ermöglichen es einem Plugin, anderen Plugins blind zu vertrauen und davon auszugehen, dass die Eingaben vom Endbenutzer stammen. Solche unzureichenden Zugriffskontrollen können dazu führen, dass böswillige Eingaben schädliche Folgen haben, von der Datenausfiltrierung über die Ausführung von Remote-Code bis hin zur Privilegieneskalation.

Dieser Abschnitt konzentriert sich auf die Erstellung von LLM-Plugins und nicht auf Plugins von Drittanbietern, die durch LLM-Supply-Chain-Schwachstellen abgedeckt werden.

### Gängige Beispiele für Schwachstellen

1. Ein Plugin akzeptiert alle Parameter in einem einzigen Textfeld anstatt in separaten Eingabeparametern.
2. Ein Plugin akzeptiert Konfigurationsstrings anstelle von Parametern, die alle Konfigurationseinstellungen überschreiben können.
3. Ein Plugin akzeptiert rohe SQL- oder Programmieranweisungen anstelle von Parametern.
4. Die Authentifizierung erfolgt ohne explizite Autorisierung für ein bestimmtes Plugin.
5. Ein Plugin behandelt alle LLM-Inhalte so, als ob sie vollständig vom Benutzer erstellt wurden, und führt jede angeforderte Aktion ohne zusätzliche Autorisierung aus.

### Präventions- und Mitigationsstrategien

1. Plugins sollten, wo immer möglich, streng parametrisierte Eingaben erzwingen und Typ- und Bereichsprüfungen für Eingaben vorsehen. Wenn dies nicht möglich ist, sollte eine zweite Schicht von typisierten Aufrufen eingeführt werden, die die Anfragen parst und eine Validierung und Bereinigung durchführt. Wenn Freiform-Eingaben aufgrund der Anwendungssemantik akzeptiert werden müssen, sollten diese sorgfältig geprüft werden, um sicherzustellen, dass keine potenziell schädlichen Methoden aufgerufen werden.
2. Plugin-Entwickler sollten die Empfehlungen aus dem OWASP ASVS (Application Security Verification Standard) anwenden, um eine angemessene Validierung und Bereinigung von Eingaben sicherzustellen.
3. Plugins sollten gründlich geprüft und getestet werden, um eine angemessene Validierung zu gewährleisten. Verwenden Sie statische Anwendungssicherheitstests (SAST) und dynamische und interaktive Anwendungstests (DAST, IAST) in den Entwicklungspipelines.
4. Plugins sollten so entworfen werden, dass die Auswirkungen der Ausnutzung unsicherer Eingabeparameter gemäß den OWASP ASVS Access Control Guidelines minimiert werden. Dies beinhaltet eine Zugriffskontrolle mit den geringsten Rechten, die so wenig Funktionalität wie möglich preisgibt, aber dennoch die gewünschte Funktion erfüllt.
5. Plugins sollten geeignete Authentifizierungsidentitäten wie OAuth2 verwenden, um eine effektive Autorisierung und Zugriffskontrolle anzuwenden. Darüber hinaus sollten API-Schlüssel verwendet werden, um Kontext für benutzerdefinierte Autorisierungsentscheidungen bereitzustellen, die die Plugin-Route und nicht den interaktiven Standardbenutzer widerspiegeln.
6. Manuelle Benutzerautorisierung und Bestätigung für alle Aktionen, die von sensiblen Plugins durchgeführt werden, erforderlich machen.
7. Plugins sind in der Regel REST APIs. Daher sollten Entwickler die Empfehlungen in OWASP Top 10 API Security Risks - 2023 befolgen, um allgemeine Schwachstellen zu minimieren.

## Beispiele für Angriffsszenarien

1. Ein Plugin akzeptiert eine Basis-URL und weist das LLM an, die URL mit einer Anfrage zu kombinieren, um Wettervorhersagen zu erhalten, die in die Bearbeitung der Benutzeranfrage einfließen. Böswillige Personen können eine Anfrage so gestalten, dass die URL auf eine von ihm kontrollierte Domäne verweist, wodurch sie ihre eigenen Inhalte über diese in das LLM-System einspeisen können.
2. Ein Plugin akzeptiert eine freie Eingabe in ein einzelnes Feld, die nicht validiert wird. Angreifende liefern sorgfältig gestaltete Payloads, um Fehlermeldungen auszuspähen. Anschließend nutzen sie bekannte Sicherheitslücken von Drittanbietern aus, um Code auszuführen, Daten zu exfiltrieren oder Rechte zu erweitern.
3. Ein Plugin, das zum Abrufen von Embeddings aus einem Vektorspeicher verwendet wird, akzeptiert Konfigurationsparameter als Verbindungsstring ohne jegliche Validierung. Dadurch können Angreifende experimentieren und auf andere Vektorspeicher zugreifen, indem sie Namen oder Hostparameter ändern und Embeddings exfiltriert, auf die sie keinen Zugriff haben sollten.
4. Ein Plugin akzeptiert SQL WHERE-Klauseln als erweiterte Filter, die dann an die SQL-Bedingungen angehängt werden. Dadurch können Angreifende einen SQL-Angriff durchführen.
5. Angreifende nutzen eine indirekte Prompt-Injection aus, um ein unsicheres Codeverwaltungs-Plugin ohne Eingabevalidierung und mit schwacher Zugriffskontrolle auszunutzen, um den Besitz von Repositories zu übertragen und Personen von ihren Repositories auszuschließen.

### Referenzen

1. [OpenAI ChatGPT Plugins](https://platform.openai.com/docs/plugins/introduction): **ChatGPT Developer’s Guide**
2. [OpenAI ChatGPT Plugins - Plugin Flow](https://platform.openai.com/docs/plugins/introduction/plugin-flow): **OpenAI Documentation**
3. [OpenAI ChatGPT Plugins - Authentication](https://platform.openai.com/docs/plugins/authentication/service-level): **OpenAI Documentation**
4. [OpenAI Semantic Search Plugin Sample](https://github.com/openai/chatgpt-retrieval-plugin): **OpenAI Github**
5. [Plugin Vulnerabilities: Visit a Website and Have Your Source Code Stolen](https://embracethered.com/blog/posts/2023/chatgpt-plugin-vulns-chat-with-code/): **Embrace The Red**
6. [ChatGPT Plugin Exploit Explained: From Prompt Injection to Accessing Private Data](https://embracethered.com/blog/posts/2023/chatgpt-cross-plugin-request-forgery-and-prompt-injection./) **Embrace The Red**
7. [ChatGPT Plugin Exploit Explained: From Prompt Injection to Accessing Private Data](https://embracethered.com/blog/posts/2023/chatgpt-cross-plugin-request-forgery-and-prompt-injection./): **Embrace The Red**
8. [OWASP ASVS - 5 Validation, Sanitization and Encoding](https://owasp-aasvs4.readthedocs.io/en/latest/V5.html#validation-sanitization-and-encoding): **OWASP AASVS**
9. [OWASP ASVS 4.1 General Access Control Design](https://owasp-aasvs4.readthedocs.io/en/latest/V4.1.html#general-access-control-design): **OWASP AASVS**
10. [OWASP Top 10 API Security Risks – 2023](https://owasp.org/API-Security/editions/2023/en/0x11-t10/): **OWASP**

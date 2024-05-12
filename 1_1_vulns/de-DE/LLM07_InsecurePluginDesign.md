## LLM07: Unsicheres Plugin-Design

### Beschreibung

LLM-Plugins sind Erweiterungen, die bei Bedarf automatisch vom Modell während der Benutzerinteraktionen aufgerufen werden. Sie werden von der Modellintegrationsplattform gesteuert und die Anwendung hat möglicherweise keine Kontrolle über ihre Ausführung, insbesondere wenn das Modell von einer anderen Partei gehostet wird. Darüber hinaus implementieren Plugins wahrscheinlich Freitexteingaben aus dem Modell ohne Validierung oder Typüberprüfung, um mit Beschränkungen der Kontextgröße umzugehen. Dadurch können potenzielle Angreifende eine böswillige Anfrage an das Plugin konstruieren, die zu einem breiten Spektrum an unerwünschtem Verhalten bis hin zur Ausführung von Remote-Code führen kann.

Der Schaden, der durch böswillige Eingaben verursacht wird, hängt oft von unzureichenden Zugriffskontrollen und dem Versäumnis ab, die Autorisierung über Plugins hinweg zu verfolgen. Unzureichende Zugriffskontrollen ermöglichen es einem Plugin, anderen Plugins blind zu vertrauen und davon auszugehen, dass die Eingaben vom Endbenutzer stammen. Solche unzureichenden Zugriffskontrollen können dazu führen, dass böswillige Eingaben schädliche Folgen haben, von der Datenausfiltrierung über die Ausführung von Remote-Code bis hin zur Privilegieneskalation.

Dieser Abschnitt konzentriert sich auf die Erstellung von LLM-Plugins und nicht auf Plugins von Drittanbietern, die durch LLM-Supply-Chain-Schwachstellen abgedeckt werden.

### Häufige Beispiele für Verwundbarkeiten

1. Ein Plugin akzeptiert alle Parameter in einem einzigen Textfeld anstatt in separaten Eingabeparametern.
2. Ein Plugin akzeptiert Konfigurationsstrings anstelle von Parametern, die alle Konfigurationseinstellungen überschreiben können.
3. Ein Plugin akzeptiert rohe SQL- oder Programmieranweisungen anstelle von Parametern.
4. Die Authentifizierung erfolgt ohne explizite Autorisierung für ein bestimmtes Plugin.
5. Ein Plugin behandelt alle LLM-Inhalte so, als ob sie vollständig vom Benutzer erstellt wurden, und führt jede angeforderte Aktion ohne zusätzliche Autorisierung aus.

### Präventions- und Minderungsstrategien

1. Plugins sollten, wo immer möglich, streng parametrisierte Aufrufe erzwingen und Typ- und Bereichsprüfungen für Aufrufe enthalten. Wenn dies nicht möglich ist, sollte eine zweite Schicht von typisierten Aufrufen eingeführt werden, die die Anfragen analysiert und Validierung und Sanitisierung anwendet. Wenn Freiformeingaben aufgrund der Anwendungssemantik akzeptiert werden müssen, sollten diese sorgfältig geprüft werden, um sicherzustellen, dass keine potenziell schädlichen Methoden aufgerufen werden.
2. Plugin-Entwickler sollten die Empfehlungen des OWASP im Application Security Verification Standard (ASVS) anwenden, um eine angemessene Validierung und Sanitisierung von Eingaben zu gewährleisten.
3. Plugins sollten gründlich geprüft und getestet werden, um eine angemessene Validierung zu gewährleisten. Statisches Application Security Testing (SAST) und dynamisches und interaktives Application Testing (DAST, IAST) sollten in Entwicklungspipelines verwendet werden.
4. Plugins sollten so entworfen werden, dass die Auswirkungen der Ausnutzung unsicherer Eingabeparameter minimiert werden, in Übereinstimmung mit den OWASP ASVS Access Control Guidelines. Dies beinhaltet Zugriffskontrolle mit minimalen Rechten, indem so wenig Funktionalität wie möglich offengelegt wird, während die gewünschte Funktion erfüllt wird.
5. Plugins sollten geeignete eigene Authentifizierungsidentitäten wie OAuth2 verwenden, um eine effektive Autorisierung und Zugriffskontrolle zu implementieren. Zusätzlich sollten API-Schlüssel verwendet werden, um den Kontext für benutzerdefinierte Autorisierungsentscheidungen bereitzustellen, die den Plugin-Pfad anstelle des standardmäßigen interaktiven Benutzers widerspiegeln.
6. Plugins sollten eine manuelle Benutzerautorisierung und Bestätigung für jede Aktion erfordern, die von sensiblen Plugins durchgeführt wird.
7. Plugins sind oft REST APIs, daher sollten Entwickler die Empfehlungen in OWASP Top 10 API Security Risks - 2023 anwenden, um generische Schwachstellen zu minimieren.

### Beispiel-Angriffsszenarien

1. Ein Plugin akzeptiert eine Basis-URL und weist das LLM an, die URL mit einer Anfrage zu kombinieren, um Wettervorhersagen zu erhalten, die in die Bearbeitung der Benutzeranfrage einfließen. Ein böswilliger Benutzer kann eine Anfrage so gestalten, dass die URL auf eine von ihm kontrollierte Domäne zeigt, wodurch er seine eigenen Inhalte über seine Domäne in das LLM-System einspeisen kann.
2. Ein Plugin akzeptiert eine Freiformeingabe in ein einzelnes Feld, das es nicht validiert. Angreifende liefern sorgfältig gestaltete Payloads, um aus Fehlermeldungen Informationen zu gewinnen. Anschließend werden bekannte Schwachstellen von Drittanbietern ausgenutzt, um Code auszuführen, Daten zu exfiltrieren oder Privilegien zu erweitern.
3. Ein Plugin, das zum Abrufen von Einbettungen aus einem Vektorspeicher verwendet wird, akzeptiert Konfigurationsparameter als Verbindungszeichenfolge ohne jegliche Validierung. Dadurch können Angreifende mit anderen Vektorspeichern experimentieren und durch Änderung von Hostnamen oder -parametern auf diese zugreifen und Einbettungen exfiltrieren, auf die er keinen Zugriff haben sollte.
4. Ein Plugin akzeptiert SQL WHERE-Klauseln als erweiterte Filter, die dann an die Filter-SQL angehängt werden. Dadurch können Angreifende einen SQL-Angriff inszenieren.
5. Angreifende nutzen indirekte Prompt-Injektion aus, um ein unsicheres Codeverwaltungs-Plugin ohne Eingabevalidierung und schwache Zugriffskontrolle auszunutzen, um Repository-Eigentum zu übertragen und den Benutzer aus dem Repository auszuschließen.

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

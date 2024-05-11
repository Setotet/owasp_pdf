## LLM04: Modell Denial of Service

### Beschreibung

Angreifende interagieren mit einem LLM auf eine Weise, die eine außergewöhnlich große Menge an Ressourcen verbraucht, was zu einer Verschlechterung der Servicequalität für sie und andere Personen führt und potenziell hohe Ressourcenkosten verursacht. Darüber hinaus stellt die Möglichkeit, dass Angreifende in das Kontextfenster eines LLM eindringen oder es manipulieren, ein erhebliches Sicherheitsproblem dar. Dieses Problem wird immer kritischer aufgrund der zunehmenden Verwendung von LLMs in verschiedenen Anwendungen, ihrer intensiven Ressourcennutzung, der Unvorhersehbarkeit von Benutzereingaben und eines allgemeinen Mangels an Bewusstsein für diese Verwundbarkeit unter Entwicklern. In LLMs stellt das Kontextfenster die maximale Textlänge dar, die das Modell verwalten kann, einschließlich Eingabe und Ausgabe. Es ist ein entscheidendes Merkmal von LLMs, da es die Komplexität der Sprachmuster bestimmt, die das Modell verstehen kann, und die Länge des Textes, den es zu einem gegebenen Zeitpunkt verarbeiten kann. Die Größe des Kontextfensters wird durch die Architektur des Modells bestimmt und kann von Modell zu Modell variieren.

### Häufige Beispiele für Verwundbarkeiten

1. das Senden von Anfragen, die durch das Erzeugen einer großen Anzahl von Tasks in einer Warteschlange, z. B. mit LangChain oder AutoGPT, zu einer sich wiederholenden Ressourcennutzung führen.
2. ungewöhnlich ressourcenintensive Anfragen senden, die ungewöhnliche Schreibweisen oder Sequenzen verwenden.
3. Kontinuierlicher Eingabe-Überlauf: Angreifende senden einen Strom von Eingaben an das LLM, der dessen Kontextfenster überschreitet, wodurch das Modell übermäßige Rechenressourcen verbraucht.
4. Wiederholte lange Eingaben: Angreifende senden wiederholt lange Eingaben an das LLM, die jeweils das Kontextfenster überschreiten.
5. Rekursive Kontexterweiterung: Angreifende konstruieren Eingaben, die rekursive Kontexterweiterungen auslösen und das LLM zwingen, das Kontextfenster wiederholt zu erweitern und zu verarbeiten.
6. Überflutung mit Eingaben variabler Länge: Angreifende überfluten das LLM mit einer großen Anzahl von Eingaben variabler Länge, wobei jede Eingabe sorgfältig so konstruiert ist, dass sie gerade die Grenze des Kontextfensters erreicht. Diese Technik zielt darauf ab, mögliche Ineffizienzen bei der Verarbeitung von Eingaben variabler Länge auszunutzen, das LLM zu überlasten und möglicherweise seine Reaktionsfähigkeit zu beeinträchtigen.

### Präventions- und Minderungsstrategien

1. Implementierung einer Eingabevalidierung und -sanierung, um sicherzustellen, dass die Benutzereingaben den definierten Grenzen entsprechen, und um schädliche Inhalte herauszufiltern.
2. Begrenzung des Ressourcenverbrauchs pro Anfrage oder Schritt, um die Ausführung von Anfragen mit komplexen Teilen zu verlangsamen.
3. Durchsetzung von API-Rate-Limiting, um die Anzahl der Anfragen zu begrenzen, die ein einzelner Benutzer oder eine IP-Adresse in einem bestimmten Zeitraum stellen kann.
4. Begrenzung der Anzahl der Aktionen in der Warteschlange und der Gesamtzahl der Aktionen in einem System, das auf LLM-Antworten reagiert.
5. Kontinuierliche Überwachung der LLM-Ressourcennutzung, um unnormale Spitzen oder Muster zu erkennen, die auf einen DoS-Angriff hindeuten könnten.
6. Strikte Eingabelimits basierend auf dem Kontextfenster des LLM, um Überlastung und Ressourcenerschöpfung zu vermeiden.
7. Sensibilisierung von Entwicklern für potenzielle DoS-Schwachstellen in LLMs und Bereitstellung von Richtlinien für die sichere Implementierung von LLMs.

### Beispielszenarien für Angriffe

1. Angreifende senden wiederholt mehrere komplexe und teure Anfragen an ein gehostetes Modell, was zu einer Verschlechterung des Dienstes für andere Benutzer und zu höheren Ressourcenkosten für den Host führt.
2. Ein Stück Text auf einer Webseite wird gefunden, während ein LLM-gesteuertes Tool Informationen sammelt, um auf eine harmlose Anfrage zu antworten. Dies führt dazu, dass das Tool viele weitere Anfragen an die Webseite stellt, was zu einem hohen Ressourcenverbrauch führt.
3. Angreifende bombardieren das LLM kontinuierlich mit Eingaben, die das Kontextfenster des LLM überschreiten. Die Angreifenden können automatisierte Skripte oder Tools verwenden, um eine große Menge an Eingaben zu senden, die die Verarbeitungskapazität des LLM übersteigen. Infolgedessen verbraucht der LLM übermäßig viele Rechenressourcen, was zu einer erheblichen Verlangsamung oder zum völligen Ausfall des Systems führt.
4. Angreifende senden eine Reihe von sequentiellen Eingaben an das LLM, wobei jede Eingabe so gestaltet ist, dass sie knapp unterhalb der Grenze des Kontextfensters liegt. Durch das wiederholte Senden dieser Eingaben versuchen die Angreifenden, die verfügbare Kapazität des Kontextfensters auszuschöpfen. Da der LLM Mühe hat, jede Eingabe innerhalb seines Kontextfensters zu verarbeiten, werden die Systemressourcen belastet, was potenziell zu einer verminderten Leistung oder einem vollständigen Ausfall des Dienstes führt.
5. Angreifende nutzen die rekursiven Mechanismen des LLM, um wiederholt eine Kontexterweiterung auszulösen. Indem Eingaben konstruiert werden, die das rekursive Verhalten des LLM ausnutzen, zwingt der Angreifer das Modell dazu, das Kontextfenster wiederholt zu erweitern und zu verarbeiten, wodurch erhebliche Rechenressourcen verbraucht werden. Dieser Angriff belastet das System und kann zu einem DoS-Zustand führen, der das LLM reaktionsunfähig macht oder zum Absturz bringt.
6. Angreifende überfluten das LLM mit einer großen Anzahl von Eingaben variabler Länge, die sorgfältig so gestaltet sind, dass sie sich der Grenze des Kontextfensters nähern oder diese erreichen. Durch die Überflutung des LLM mit Eingaben variabler Länge versuchen die Angreifenden, mögliche Ineffizienzen bei der Verarbeitung von Eingaben variabler Länge auszunutzen. Diese Flut von Eingaben belastet die Ressourcen des LLM übermäßig, was zu einer Verschlechterung der Leistung führen und die Fähigkeit des Systems, auf legitime Anfragen zu reagieren, beeinträchtigen kann.
7. Während DoS-Angriffe in der Regel darauf abzielen, Systemressourcen zu überlasten, können sie auch andere Aspekte des Systemverhaltens ausnutzen, wie z.B. API-Beschränkungen. Bei einem kürzlich aufgetretenen Sicherheitsvorfall bei Sourcegraph beispielsweise nutzte der böswillige Akteur ein durchgesickertes Admin-Zugriffstoken, um API-Rate-Limiting zu ändern, was potenziell zu Dienstunterbrechungen führte, indem es anormale Anfragevolumina zuließ.

### Referenzlinks

1. [LangChain max_iterations](https://twitter.com/hwchase17/status/1608467493877579777): **hwchase17 auf Twitter**
2. [Sponge Examples: Energy-Latency Attacks on Neural Networks](https://arxiv.org/abs/2006.03463): **Arxiv White Paper**
3. [OWASP DOS Attack](https://owasp.org/www-community/attacks/Denial_of_Service): **OWASP**
4. [Learning From Machines: Know Thy Context](https://lukebechtel.com/blog/lfm-know-thy-context): **Luke Bechtel**
5. [Sourcegraph Security Incident on API Limits Manipulation and DoS Attack ](https://about.sourcegraph.com/blog/security-update-august-2023): **Sourcegraph**
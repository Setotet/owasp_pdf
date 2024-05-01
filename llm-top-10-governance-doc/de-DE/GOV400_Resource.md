## Ressourcen

[OWASP Top 10 für Large Language Models](https://owasp.org/www-project-top-10-for-large-language-model-applications/assets/PDF/OWASP-Top-10-for-LLMs-2023-v1_1.pdf)

  >dodgerblue|white|left|12|16 LLM01: Prompt Injection (Prompt-Einschleusung)
  >azure|black|justified|10|12 Mit raffinierten Eingabenkann man ein Large Language Model manipulieren und unbeabsichtigte Aktionen verursachen. Direkte Injections überschreiben System-Prompts, während indirekte Eingaben von externen Quellen manipuliert werden.

  >dodgerblue|white|left|12|16 LLM02: Unsichere Ausgabeverarbeitung
  >azure|black|justified|10|12 Diese Schwachstelle tritt auf, wenn eine Ausgabe von einem LLM ohne Überprüfung akzeptiert wird, und damit Backend-Systeme angreifbar macht. Missbrauch kann zu schwerwiegenden Konsequenzen wie XSS (Cross-Site Scripting), CSRF (Cross-Site Request Forgery), SSRF (Server Side Request Forgery), Privilegienerweiterung oder Remote-Code-Ausführung führen.

  >dodgerblue|white|left|12|16 LLM03: Poisoning der Trainingsdaten
  >azure|black|justified|10|12 Dies tritt auf, wenn LLM-Trainingsdaten manipuliert werden, wodurch Sicherheitslücken oder Bias entstehen, die die Sicherheit, Wirksamkeit oder ethisches Verhalten beeinträchtigen. Quellen umfassen Common Crawl, WebText, OpenWebText und Bücher.

  >dodgerblue|white|left|12|16 LLM04: Denial of Service des Modells
  >azure|black|justified|10|12 Angreifer verursachen ressourcenintensive Operationen auf Large Language Models, was zu Servicedegradierung oder hohen Kosten führt. Die Schwachstelle wird durch die ressourcenintensive Natur der LLMs und die Unvorhersehbarkeit der Benutzereingaben vergrößert.

  >dodgerblue|white|left|12|16 LLM05: Schwachstellen in der Supply Chain
  >azure|black|justified|10|12 Der Lifecycle von LLM-Anwendungen kann durch anfällige Komponenten oder Dienste beeinträchtigt werden, was zu Sicherheitsangriffen führt. Die Verwendung von Drittanbieterdatensätzen, vortrainierten Modellen und Plugins kann Schwachstellen hinzufügen.

  >dodgerblue|white|left|12|16 LLM06: Offenlegung sensibler Informationen
  >azure|black|justified|10|12 LLMs können in ihren Antworten vertrauliche Daten preisgeben, was zu unbefugtem Datenzugriff, Datenschutzverletzungen und Sicherheitsbrüchen führt. Es ist entscheidend, Datenbereinigung und strenge Benutzerrichtlinien zu implementieren, um dies zu reduzieren.

  >dodgerblue|white|left|12|16 LLM07: Unsicheres Plugin-Design
  >azure|black|justified|10|12 LLM-Plugins können unsichere Eingaben und unzureichende Zugriffskontrollen haben. Dieser Mangel an Anwendungskontrolle macht sie leichter ausnutzbar und kann zu Konsequenzen wie der Ausführung von Remote-Code führen.

  >dodgerblue|white|left|12|16 LLM08: Übermäßige Handlungsfreiheit
  >azure|black|justified|10|12 LLM-basierte Systeme können Handlungen durchführen, die zu unbeabsichtigten Konsequenzen führen. Das Problem entsteht durch übermäßige Funktionalität, Berechtigungen oder Autonomie, die den LLM-basierten Systemen gewährt wird.

  >dodgerblue|white|left|12|16 LLM09: Übermäßige Abhängigkeit
  >azure|black|justified|10|12 Systeme oder Personen, die sich übermäßig auf LLMs verlassen, ohne angemessene Kontrolle, können Fehlinformationen, Misskommunikation, rechtliche Probleme und Sicherheitslücken aufgrund von falschen oder unangemessenen von den LLMs generierten Inhalten gegenüberstehen.

  >dodgerblue|white|left|12|16 LLM10: Modell-Diebstahl
  >azure|black|justified|10|12 Dies umfasst unbefugten Zugriff, Kopieren oder Exfiltration von proprietären LLM-Modellen. Die Auswirkungen umfassen wirtschaftliche Verluste, beeinträchtigte Wettbewerbsvorteile und potenziellen Zugang zu sensiblen Informationen.

##### Figure 4.1  OWASP Top 10 for Large Language Model Applications

![OWASP Top10 für LLM Visuell](images/GOV1_Fig_4_2_de-DE.png)
##### Abbildung 4.2 OWASP Top 10 für Large-Language-Model-Anwendungen visualisiert


### OWASP-Ressourcen

Die Verwendung von LLM-Lösungen erweitert die Angriffsfläche einer Organisation und stellt neue Herausforderungen dar, die spezielle Taktiken und Verteidigungen erfordern. Es enthält auch Probleme, die analog zu bekannten Problemen sind, für die bereits etablierte Cybersecurity-Verfahren und Milderungsmaßnahmen existieren. Die Integration der LLM-Cybersicherheit in die etablierten Cybersicherheitskontrollen, -prozesse und -verfahren einer Organisation ermöglicht es einer Organisation, ihre Anfälligkeit für Bedrohungen zu verringern.
Wie sie integriert werden, ist verfügbar unter den [OWASP-Integrationsstandards.](https://owasp.org/www-project-integration-standards/)

#### OWASP-Ressource
  [OWASP SAMM](https://owasp.org/www-project-samm/)
#### Beschreibung
  Software Assurance Maturity Model
#### Warum es empfohlen wird & Wo es verwendet wird
  Es bietet eine effektive und messbare Möglichkeit, die sichere Entwicklung eines Unternehmens zu analysieren und zu verbessern. SAMM unterstützt den kompletten Software-Lebenszyklus. Es ist iterativ und risikobasiert, ermöglicht Unternehmen, Lücken in der sicheren Softwareentwicklung zu identifizieren und zu priorisieren, damit Ressourcen für die Verbesserung des Prozesses dort eingesetzt werden können, wo die Bemühungen den größten Verbesserungseffekt haben.

#### OWASP-Ressource
  [OWASP AI Exchange](https://owasp.org/www-project-ai-security-and-privacy-guide/owaspaiexchange.html)
  [OWASP Machine Learning Security Top 10](https://mltop10.info/)
#### Beschreibung
  OWASP-Projekt zum weltweiten Austausch über AI-Sicherheit, Förderung der Standardausrichtung und Antrieb der Zusammenarbeit.
  OWASP AI Exchange ist die Eingabemethode für den OWASP AI Security and Privacy Guide
  OWASP Machine Learning Security Top 10 Sicherheitsprobleme von maschinellen Lernsystemen
#### Warum es empfohlen wird & wo es verwendet wird
  Dieses Projekt umfasst die ML Top 10 und ist ein lebendiges Arbeitsdokument, das klare und handlungsorientierte Einblicke in das Entwerfen, Erstellen, Testen und Beschaffen von sicheren und datenschutzorientierten AI-Systemen bietet. Es ist die beste OWASP-Ressource für globale regulatorische und Datenschutzinformationen zu KI.

#### OWASP-Ressource
   [Open Common Requirement Enumeration : OpenCRE](https://www.opencre.org/)
#### Beschreibung
  Die OpenCRE ist die interaktive Content-Linking-Plattform zur Zusammenführung von Sicherheitsstandards und -richtlinien in einer Übersicht.
#### Warum es empfohlen wird & wo es verwendet wird
  Nutzen Sie diese Seite, um nach Standards zu suchen. Sie können nach Standardnamen oder nach Kontrolltyp suchen.

#### OWASP-Ressource
  [OWASP Threat Modeling](https://owasp.org/www-community/Threat_Modeling)
#### Beschreibung
  Ein strukturierter, formaler Prozess für die Bedrohungsmodellierung einer Anwendung
#### Warum es empfohlen wird & wo es verwendet wird
  Erfahren Sie alles über Bedrohungsmodellierung (Threat Modeling), das eine strukturierte Darstellung aller Informationen ist, die die Sicherheit einer Anwendung beeinflussen.

#### OWASP-Ressource
  [OWASP CycloneDX](https://owasp.org/www-project-cyclonedx/)
#### Beschreibung
  OWASP CycloneDX ist ein vollständiger Bill-of-Materials (BOM) Standard, der erweiterte Lieferkettenfähigkeiten für die Reduzierung von Cyberrisiken bietet.
#### Warum es empfohlen wird & Wo es verwendet wird
  Moderne Software wird unter Verwendung von Drittanbieter- und Open-Source-Komponenten zusammengestellt. Sie werden auf komplexe und einzigartige Weise zusammengefügt und mit Originalcode integriert, um die gewünschte Funktionalität zu erreichen. Ein SBOM bietet ein genaues Inventar aller Komponenten, das Organisationen ermöglicht, Risiken zu identifizieren, größere Transparenz zu ermöglichen und schnelle Auswirkungsanalysen durchzuführen.
  [EO 14028](https://www.nist.gov/itl/executive-order-14028-improving-nations-cybersecurity/software-security-supply-chains-software-1) stellte Mindestanforderungen für SBOM für föderale Systeme bereit.

#### OWASP-Ressource
  [OWASP Software Component Verification Standard (SCVS)](https://scvs.owasp.org/)
#### Beschreibung
  Eine gemeinschaftlich getriebene Anstrengung, um ein Rahmenwerk für die Identifizierung von Aktivitäten, Kontrollen und Best Practices zur Identifizierung und Reduzierung von Risiken in einer Software-Lieferkette zu etablieren.
#### Warum es empfohlen wird & wo es verwendet wird
  Nutzen Sie SCVS, um einen gemeinsamen Satz von Aktivitäten, Kontrollen und Best Practices zu entwickeln, die das Risiko in einer Software-Lieferkette reduzieren können und eine Basislinie und einen Weg zur Reife der Wachsamkeit der Software-Lieferkette identifizieren.

#### OWASP-Ressource
  [OWASP API Security Project](https://owasp.org/www-project-api-security/)
#### Beschreibung
  API-Sicherheit konzentriert sich auf Strategien und Lösungen, um die einzigartigen Schwachstellen und Sicherheitsrisiken von Application Programming Interfaces (APIs) zu verstehen und zu mildern.
#### Warum es empfohlen wird & wo es verwendet wird
  APIs sind ein grundlegendes Element der Verbindung von Anwendungen, und das Reduzieren von Fehlkonfigurationen oder Schwachstellen ist obligatorisch, um Benutzer und Organisationen zu schützen. Verwenden Sie es für Sicherheitstests und Red Teaming der Build- und Produktionsumgebungen.

#### OWASP-Ressource
  [OWASP Top 10 CI/CD Sicherheitsrisiken](https://owasp.org/www-project-top-10-ci-cd-security-risks/)
#### Beschreibung
  Hilft Verteidigern, Fokusbereiche für die Sicherung ihres CI/CD-Ökosystems zu identifizieren.
#### Warum es empfohlen wird & wo es verwendet wird
  CI/CD-Umgebungen, -Prozesse und -Systeme sind das Ökosystem moderner Softwareorganisationen. Sie liefern Code vom Entwicklungsrechner eines Ingenieurs bis zur Produktion. Sie haben ihre eigene einzigartige Angriffsfläche und sind ein häufiges Angriffsziel. Verwenden Sie es für Sicherheitstests und Red Teaming der Build- und Produktionsumgebungen.

#### OWASP-Ressource
  [OWASP Application Security Verification Standard ASVS](https://owasp.org/www-project-application-security-verification-standard/)
#### Beschreibung
  Das Application-Security-Verification-Standard(ASVS) Projekt bietet eine Grundlage für das Testen von technischen Sicherheitskontrollen von Webanwendungen und bietet Entwicklern auch eine Liste von Anforderungen für die sichere Entwicklung.
#### Warum es empfohlen wird & wo es verwendet wird
  Ein Kochbuch für Webanwendungssicherheitsanforderungen, Sicherheitstests und Metriken. Verwenden Sie es, um Sicherheits-User-Stories und Sicherheits-Use-Case-Release-Tests zu etablieren.

#### OWASP-Ressource
  [OWASP Threat and Safeguard Matrix (TaSM)](https://owasp.org/www-project-threat-and-safeguard-matrix/)
#### Beschreibung
  Eine aktionsorientierte Sichtweise zum Schutz und Ermöglichen der Geschäftsabläufe.
#### Warum es empfohlen wird & wo es verwendet wird
  Diese Matrix ermöglicht es einem Unternehmen, seine Hauptbedrohungen mit den NIST Cyber Security Framework-Funktionen (Identifizieren, Schützen, Erkennen, Reagieren & Wiederherstellen) zu überlagern, um einen robusten Sicherheitsplan zu erstellen. Verwenden Sie es als Dashboard, um die Sicherheit im gesamten Unternehmen zu verfolgen und zu berichten.

#### OWASP-Ressource
   [Defect Dojo](https://www.defectdojo.com/)
#### Beschreibung
  Ein Open-Source-Schwachstellenmanagement-Tool, das den Testprozess durch Vorlagen, Berichtsgenerierung, Metriken und Baseline-Selbstbedienungswerkzeuge vereinfacht.
#### Warum es empfohlen wird & wo es verwendet wird
  Verwenden Sie das Defect Dojo, um die Zeit für das Protokollieren von Schwachstellen mit Vorlagen für Schwachstellen, Importen für gängige Schwachstellenscanner, Berichtsgenerierung und Metriken zu reduzieren.


### MITRE-Ressourcen

Die zunehmende Häufigkeit von LLM-Bedrohungen zeigt den Wert eines Resilienz-first-Ansatzes zur Verteidigung der Angriffsfläche einer Organisation. Bestehende TTPs werden mit neuen Angriffsflächen und Fähigkeiten in LLM-Gegnerbedrohungen und -milderungen kombiniert. MITRE unterhält einen gut etablierten und weit akzeptierten Mechanismus zur Koordinierung von Gegnertaktiken und -verfahren auf der Grundlage von Beobachtungen aus der realen Welt.

Die Koordination und Kartierung der LLM-Sicherheitsstrategie einer Organisation auf MITRE ATT&CK und MITRE ATLAS ermöglicht es einer Organisation zu entdecken, wo die LLM-Sicherheit durch aktuelle Prozesse wie API-Sicherheitsstandards abgedeckt ist oder wo Sicherheitslücken bestehen.

MITRE ATT&CK (Adversarial Tactics, Techniques, and Common Knowledge) ist ein Rahmenwerk, eine Sammlung von Datenmatrizen und ein Bewertungstool, das von der MITRE Corporation entwickelt wurde, um Organisationen zu helfen, herauszufinden, wie gut ihre Cybersicherheit über ihre gesamte digitale Angriffsfläche funktioniert und zuvor nicht entdeckte Lücken zu finden. Es ist ein Wissensrepository, das weltweit verwendet wird. Die MITRE ATT&CK-Matrix enthält eine Sammlung von Strategien, die von Gegnern verwendet werden, um ein bestimmtes Ziel zu erreichen. In der ATT&CK-Matrix werden diese Ziele als Taktiken klassifiziert. Die Ziele sind in Angriffsreihenfolge dargestellt, beginnend mit Aufklärung und fortschreitend bis zum letztendlichen Ziel der Exfiltration oder Wirkung.

MITRE ATLAS, das für "Adversarial Threat Landscape for Artificial Intelligence Systems" steht, ist eine Wissensbasis, die auf realen Beispielen von Angriffen auf maschinelle Lernsysteme (ML) durch böswillige Akteure basiert. ATLAS basiert auf der MITRE ATT&CK-Architektur, und seine Taktiken und Verfahren ergänzen die in ATT&CK gefundenen.

#### MITRE-Ressource
  [MITRE ATT&CK](https://attack.mitre.org/)
#### Beschreibung
  Wissensbasis zu Gegnertaktiken und -techniken basierend auf Beobachtungen aus der realen Welt
#### Warum es empfohlen wird & wo es verwendet wird
  Die ATT&CK-Wissensbasis wird als Grundlage für die Entwicklung spezifischer Bedrohungsmodelle und Methodologien verwendet. Kartieren Sie bestehende Kontrollen innerhalb der Organisation auf Gegnertaktiken und -techniken, um Lücken oder Bereiche zum Testen zu identifizieren.

#### MITRE-Ressource
  [MITRE ATT&CK Workbench](https://mitre-engenuity.org/cybersecurity/center-for-threat-informed-defense/our-work/attck-workbench/)
#### Beschreibung
  Erstellen oder erweitern Sie ATT&CK-Daten in einer lokalen Wissensdatenbank
#### Warum es empfohlen wird & wo es verwendet wird
  Verwalten und hosten Sie eine angepasste Kopie der ATT&CK-Wissensdatenbank. Diese lokale Kopie der ATT&CK-Wissensbasis kann mit neuen oder aktualisierten Techniken, Taktiken, Milderungsgruppen und Software erweitert werden, die spezifisch für Ihre Organisation sind.

#### MITRE-Ressource
   [MITRE ATLAS](https://atlas.mitre.org/)
#### Beschreibung
  MITRE ATLAS (Adversarial Threat Landscape for Artificial-Intelligence Systems) ist eine Wissensdatenbank zu Gegnertaktiken, -techniken und Fallstudien für maschinelle Lernsysteme (ML) basierend auf Beobachtungen aus der realen Welt, Demonstrationen von ML-Red-Teams und Sicherheitsgruppen sowie dem Stand des Möglichen aus der akademischen Forschung
#### Warum es empfohlen wird & wo es verwendet wird
  Verwenden Sie es, um bekannte ML-Schwachstellen zu kartieren und Checks und Kontrollen auf vorgeschlagene Projekte oder bestehende Systeme abzubilden.

#### MITRE-Ressource
  [MITRE ATT&CK Powered Suit](https://mitre-engenuity.org/cybersecurity/center-for-threat-informed-defense/attack-powered-suit/)
#### Beschreibung
  ATT&CK Powered Suit ist eine Browsererweiterung, die die MITRE ATT&CK-Wissensbasis in Reichweite bringt.
#### Warum es empfohlen wird & Wo es verwendet wird
  Fügen Sie sie Ihrem Browser hinzu, um schnell nach Taktiken, Techniken und mehr zu suchen, ohne Ihren Workflow zu unterbrechen.

#### MITRE-Ressource
  [The Threat Report ATT&CK Mapper (TRAM)](https://mitre-engenuity.org/cybersecurity/center-for-threat-informed-defense/our-work/threat-report-attck-mapper-tram/)
#### Beschreibung
  Automatisiert die TTP-Identifizierung in CTI-Berichten
#### Warum es empfohlen wird & Wo es verwendet wird
  Das Mapping von TTPs, die in CTI-Berichten gefunden wurden, auf MITRE ATT&CK ist schwierig, fehleranfällig und zeitaufwändig. TRAM verwendet LLMs, um diesen Prozess für die 50 häufigsten Techniken zu automatisieren. Unterstützt Juypter-Notebooks.

#### MITRE-Ressource
   [Attack Flow v2.1.0](https://center-for-threat-informed-defense.github.io/attack-flow/)
#### Beschreibung
  Attack Flow ist eine Sprache zur Beschreibung, wie Cyber-Gegner verschiedene offensive Techniken kombinieren und sequenzieren, um ihre Ziele zu erreichen.
#### Warum es empfohlen wird & Wo es verwendet wird
  Attack Flow hilft zu visualisieren, wie ein Angreifer eine Technik verwendet, damit Verteidiger und Führungskräfte verstehen, wie Gegner operieren, und ihre defensive Position verbessern.

#### MITRE-Ressource
  [MITRE Caldera](https://caldera.mitre.org/)
#### Beschreibung
  Eine Cybersecurity-Plattform (Framework), die entwickelt wurde, um die Emulation von Gegnern leicht zu automatisieren, manuellen Red Teams zu helfen und die Reaktion auf Vorfälle zu automatisieren.
#### Warum es empfohlen wird & Wo es verwendet wird
  Für Caldera sind Plugins verfügbar, die die Kernfähigkeiten des Frameworks erweitern und zusätzliche Funktionalitäten bieten, einschließlich Agenten, Berichterstattung, Sammlungen von TTPs und anderen.
  [Hier ist die Plugin-Bibliothek.](https://caldera.readthedocs.io/en/latest/Plugin-library.html)

#### MITRE-Ressource
  [CALDERA-Plugin: Arsenal](https://www.mitre.org/news-insights/news-release/microsoft-and-mitre-create-tool-help-security-teams-prepare-attacks)
#### Beschreibung
  Ein Plugin, das für die Gegneremulation von KI-fähigen Systemen entwickelt wurde.
#### Warum es empfohlen wird & Wo es verwendet wird
  Dieses Plugin bietet in MITRE ATLAS definierte TTPs, um mit CALDERA zu interagieren.

#### MITRE-Ressource
  [Atomic Red Team](https://github.com/redcanaryco/atomic-red-team)
#### Beschreibung
  Bibliothek von Tests, die dem MITRE ATT&CK-Framework zugeordnet sind.
#### Warum es empfohlen wird & Wo es verwendet wird
  Verwenden Sie es, um Kontrollen in einer Umgebung zu validieren und zu testen. Sicherheitsteams können Atomic Red Team verwenden, um Kontrollen zu testen.
  Sie können atomare Tests direkt von der Kommandozeile aus ausführen; keine Installation ist erforderlich.

#### MITRE-Ressource
  [MITRE CTI-Blueprints](https://mitre-engenuity.org/cybersecurity/center-for-threat-informed-defense/our
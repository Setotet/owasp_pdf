## Introduzione

L’ondata di interesse frenetico per i modelli di linguaggio a grandi dimensioni (LLM, dall’inglese Large Language Models), in seguito all’introduzione sul mercato di massa dei chatbot pre-addestrati a fine 2022, è stata notevole. Le aziende, impazienti di sfruttare il potenziale degli LLM, stanno rapidamente integrandoli nei loro sistemi e nelle offerte destinate ai clienti. Eppure, l’incredibile velocità alla quale gli LLM stanno venendo adottati ha superato il tempo necessario a stabilire dei protocolli di sicurezza completi, lasciando molte applicazioni vulnerabili a problemi di alto rischio.

L’assenza di una risorsa unificata che affrontasse questi problemi di sicurezza negli LLM era evidente. Gli sviluppatori, non essendo familiari con i rischi associati agli LLM, sono stati lasciati con risorse sparse e la missione di OWASP sembrava prestarsi perfettamente ad aiutare a guidare un’adozione sicura di questa tecnologia.

### A chi si rivolge questo documento?

Il nostro pubblico principale sono gli sviluppatori, i data scientist e gli esperti di sicurezza incaricati di pianificare e costruire applicazioni e plugin basati su tecnologie LLM. Il nostro obiettivo è fornire una guida pratica e concisa per aiutare questi professionisti a muoversi nel terreno complesso e in continua evoluzione della sicurezza degli LLM.

### La creazione della lista

La creazione dell’OWASP Top 10 per le applicazioni LLM è stata un’impresa significativa, basata sull’esperienza collettiva di un gruppo internazionale di quasi 500 esperti, con più di 125 contributori attivi. I nostri collaboratori provengono da contesti diversi, che includono aziende nel campo dell’intelligenza artificiale, aziende del settore della sicurezza, editori di software indipendenti, piattaforme cloud e hyperscale, e il mondo della ricerca accademica.


Nel corso di un mese, abbiamo discusso e proposto potenziali vulnerabilità e i membri del gruppo hanno considerato fino a 43 minacce distinte. Attraverso molteplici round di selezione, abbiamo ridotto queste proposte fino ad arrivare a una lista concisa delle 10 vulnerabilità più critiche.

Ognuna di queste vulnerabilità, congiuntamente agli esempi, ai suggerimenti relativi alla prevenzione, agli scenari di attacco e ai riferimenti, è stata ulteriormente esaminata e rifinita da sotto-gruppi specializzati e sottoposta a una revisione pubblica, per assicurare che la lista finale fosse il più possibile completa e concretamente applicabile.


### Relazione con le altre liste OWASP Top 10

Anche se la nostra lista condivide il DNA con i tipi di vulnerabilità che si possono trovare nelle altre liste OWASP Top 10, non ci limitiamo a reiterarle, ma analizziamo le implicazioni uniche che queste vulnerabilità hanno quando appaiono in applicazioni basate sugli LLM.

Il nostro obiettivo è di colmare la distanza tra i principi generali di sicurezza delle applicazioni e le sfide specifiche poste dagli LLM. Questo include l’esplorazione di come le vulnerabilità tradizionali possano porre rischi differenti o possano essere sfruttate in nuovi modi con gli LLM, e come i rimedi tradizionali debbano essere adattati alle applicazioni basate sugli LLM.

### Riguardo versione 1.1

Anche se la nostra lista condivide il DNA con i tipi di vulnerabilità che si possono trovare nelle altre liste OWASP Top 10, non ci limitiamo a reiterarle, ma analizziamo le implicazioni uniche che queste vulnerabilità hanno quando appaiono in applicazioni basate sugli LLM.

Il nostro obiettivo è di colmare la distanza tra i principi generali di sicurezza delle applicazioni e le sfide specifiche poste dagli LLM. Questo include l’esplorazione di come le vulnerabilità tradizionali possano porre rischi differenti o possano essere sfruttate in nuovi modi con gli LLM, e come i rimedi tradizionali debbano essere adattati alle applicazioni basate sugli LLM.

### Il futuro

La versione 1.1 di questa lista non sarà l’ultima. Ci aspettiamo di aggiornare questa lista periodicamente, per stare al passo con l’evoluzione del settore. Lavoreremo con la comunità per far evolvere la tecnologia e creare altro materiale di studio per una serie di casi d’uso. Miriamo inoltre a collaborare con gli organismi di standardizzazione e i governi a riguardo della sicurezza dell’intelligenza artificiale. Ti invitiamo a unirti al nostro gruppo e contribuire.


#### Steve Wilson
Responsabile del progetto OWASP Top 10 per le applicazioni LLM
https://www.linkedin.com/in/wilsonsd    
Twitter/X: @virtualsteve

#### Ads Dawson
Responsabile della release 1.1 e responsabile voci di vulerabilità per il progetto OWASP Top 10 per le applicazioni LLM
https://www.linkedin.com/in/adamdawson0 
GitHub: @GangGreenTemperTatum

## Riguardo alla traduzione

### Traduttori

#### Fabrizio Cilli
https://www.linkedin.com/in/fabriziocilli/  
#### Matteo Dora
https://www.linkedin.com/in/mattbit/  


Nella realizzazione di questa traduzione, abbiamo scelto consapevolmente di impiegare solo traduttori umani, riconoscendo la natura eccezionalmente tecnica e critica dell’OWASP Top Ten per gli LLM. I traduttori elencati sopra non solo possiedono una profonda comprensione del contenuto originale, ma anche la fluidità per rendere questa traduzione un successo.

#### Talesh Seeparsan
Responsabile traduzioni, OWASP Top 10 per le applicazioni LLM
https://www.linkedin.com/in/talesh/  



## OWASP Top 10 per le applicazioni LLM

### LLM01: Iniezione di prompt
Input artificiosi possono manipolare un modello linguistico di grandi dimensioni, causando azioni non volute. Le iniezioni dirette sovrascrivono i prompt di sistema, mentre quelle indirette manipolano gli input provenienti da fonti esterne.

### LLM02: Gestione non sicura dell'output
Questa vulnerabilità accade quando l'output dell'LLM è accettato senza previa verifica, esponendo i sistemi backend. L'abuso può portare a conseguenze gravi come XSS, CSRF, SSRF, escalation dei privilegi o esecuzione di codice remoto.

### LLM03: Avvelenamento dei dati di apprendimento
Questo si verifica quando i dati di apprendimento dell'LLM vengono manomessi, introducendo vulnerabilità o bias che ne compromettono la sicurezza, l'efficacia o il comportamento etico. Le fonti di dati includono Common Crawl, WebText, OpenWebText e libri.

### LLM04: Denial of Service del Modello
Degli attaccanti causano operazioni che richiedono molte risorse sui modelli linguistici di grandi dimensioni, portando a degrado del servizio o a costi elevati. La vulnerabilità è amplificata dalla natura intensiva delle risorse degli LLM e dall'imprevedibilità degli input dell'utente.

### LLM05: Vulnerabilità della Supply-Chain
Il ciclo di vita dell'applicazione LLM può essere compromesso da componenti o servizi vulnerabili, portando ad attacchi di sicurezza. L'utilizzo di dataset, modelli pre-addestrati e plugin di terze parti può aggiungere altre vulnerabilità.

### LLM06: Diffusione di Informazioni Sensibili
Gli LLM possono rivelare dati confidenziali nelle risposte, portando ad accessi non autorizzati, violazioni della privacy e falle di sicurezza. Per mitigare questo rischio, è cruciale implementare un processo di sanitizzazione dei dati e politiche utente rigorose.

### LLM07: Progettazione Insicura dei Plugin
I plugin LLM possono avere input non sicuri e controlli di accesso insufficienti. Questa mancanza di controllo dell'applicazione li rende più facili da sfruttare e può comportare conseguenze come l'esecuzione remota di codice.

### LLM08: Eccessiva Autonomia
I sistemi basati sugli LLM possono intraprendere azioni che conducono a conseguenze non volute. Il problema nasce da funzionalità, permessi o autonomia eccessivi concessi a questi sistemi.

### LLM09: Eccessivo Affidamento
Senza supervisione, sistemi o persone eccessivamente dipendenti dagli LLM possono incorrere in disinformazione, malfunzionamenti, problemi legali e vulnerabilità di sicurezza dovute a contenuti errati o inappropriati generati dagli LLM.

### LLM10: Furto del Modello
Questa vulnerabilità consiste nell'accesso non autorizzato, la copia o l'esfiltrazione di modelli LLM proprietari. L'impatto include perdite economiche, compromissione del vantaggio competitivo e potenziale accesso a informazioni sensibili.
## LLM01: Iniezione di prompt

### Descrizione

La vulnerabilità di tipo iniezione di prompt (inglese: prompt injection) si verifica quando un attaccante manipola un modello linguistico di grandi dimensioni (LLM) attraverso input artificiosi, facendo in modo che l’LLM risponda inconsapevolmente alle intenzioni dell’attaccante. Questo può essere fatto direttamente attraverso il “jailbreaking” del prompt di sistema, oppure indirettamente, attraverso degli input esterni manipolati, portando potenzialmente all’esfiltrazione di dati, all’ingegneria sociale e altri problemi.

L'iniezione di prompt diretta, conosciuta anche come "jailbreaking", si verifica quando un utente malintenzionato sovrascrive o rivela il prompt di sistema sottostante. Ciò può consentire agli attaccanti di sfruttare i sistemi backend interagendo con funzioni insicure e archivi di dati accessibili tramite l'LLM.

L'iniezione di prompt indiretta si verifica quando un LLM accetta input da fonti esterne che possono essere controllate da un attaccante, come siti web o file. L'attaccante può incorporare un'iniezione di prompt nel contenuto esterno, dirottando il contesto della conversazione. Ciò causerebbe una minore stabilità dell'output dell'LLM, consentendo all'attaccante di manipolare l'utente o i sistemi aggiuntivi a cui l'LLM può accedere. Inoltre, le iniezioni di prompt indirette non hanno bisogno di essere visibili o leggibili da un umano, purché il testo venga analizzato dall'LLM.

I risultati di un attacco di iniezione di prompt di successo possono variare notevolmente — dalla richiesta di informazioni sensibili all'influenza su processi decisionali critici sotto mentite spoglie di normale funzionamento.

In attacchi avanzati, l'LLM può essere manipolato per impersonare un personaggio nocivo o interagire con plugin nell'ambiente dell'utente. Ciò può portare alla divulgazione di dati sensibili, all'uso non autorizzato di plugin o all'ingegneria sociale. In tali casi, l'LLM compromesso aiuta l'attaccante, aggirando i meccanismi di protezione standard e mantenendo l'utente all'oscuro dell'intrusione. In questi casi, l'LLM compromesso agisce in sostanza come un agente per l'attaccante, perseguendo i suoi obiettivi senza innescare i normali meccanismi di protezione o senza segnalare l'intrusione all'utente finale.

### Esempi comuni di vulnerabilità

Un utente malintenzionato crea un'iniezione di prompt diretta per l'LLM, ordinandogli di ignorare i prompt di sistema del creatore dell'applicazione e invece eseguire un prompt che restituisce informazioni private, pericolose o in generale indesiderabili.
Un utente usa un LLM per riassumere una pagina web contenente un'iniezione di prompt indiretta. Ciò fa sì che l'LLM richieda informazioni sensibili all'utente e le esfiltri tramite JavaScript o Markdown.
Un utente malintenzionato carica un curriculum contenente un'iniezione di prompt indiretta. Il documento contiene un'iniezione di prompt con istruzioni per far sì che l'LLM informi gli utenti che questo documento è eccellente, ad esempio un candidato eccellente per un ruolo lavorativo. Un utente interno analizza il documento tramite l'LLM per riassumerne il contenuto. In conseguenza all'iniezione di prompt, l'output dell'LLM indica che il documento è eccellente.
Un utente abilita un plugin collegato a un sito di e-commerce. Un'istruzione nociva incorporata in un sito web visitato sfrutta questo plugin, portando a acquisti non autorizzati.
Un'istruzione e del contenuto nocivi, incorporati in un sito web visitato, sfruttano altri plugin per truffare gli utenti.

### Strategie di prevenzione e mitigazione

Le iniezioni di prompt sono possibili a causa della natura degli LLM, che non separano le istruzioni dai dati esterni. Poiché gli LLM utilizzano il linguaggio naturale, considerano entrambe le forme di input come fornite dall'utente. Di conseguenza, non esiste una prevenzione infallibile all'interno dell'LLM, ma le seguenti misure possono mitigare l'impatto delle iniezioni di prompt:

Applicare il controllo dei privilegi sull'accesso dell'LLM ai sistemi backend. Fornire all'LLM i propri token API per funzionalità aggiuntive come plugin, accesso ai dati e autorizzazioni a livello di funzione. Seguire il principio del privilegio minimo limitando l'LLM al minimo livello di accesso necessario per le operazioni previste.
Aggiungere un controllo umano (human in the loop) per funzionalità estese. Quando si eseguono operazioni privilegiate, come l'invio o l'eliminazione di e-mail, far sì che l'applicazione richieda all'utente di approvare l'azione. Ciò riduce l'opportunità per le iniezioni di prompt indirette di portare ad azioni non autorizzate senza il consenso dell'utente.
Separare il contenuto esterno dai prompt dell'utente. Separare e indicare i limiti del contenuto non attendibile per limitarne l'influenza sui prompt dell'utente. Ad esempio, utilizzare ChatML per le chiamate API di OpenAI per indicare all'LLM la fonte dell'input del prompt.
Stabilire i confini di fiducia (trust boundary) tra l'LLM, le fonti esterne e le funzionalità aggiuntive (per esempio plugin o funzioni a valle). Tuttavia, un LLM compromesso può comunque agire da intermediario (man-in-the-middle) tra le API dell'applicazione e l'utente, nascondendo o manipolando le informazioni prima di presentarle all'utente. Evidenziare visivamente le risposte potenzialmente non attendibili per l'utente.
Monitorare manualmente l'input e l'output dell'LLM periodicamente, per verificare che sia conforme alle aspettative. Sebbene non sia una mitigazione, il monitoraggio può fornire i dati necessari per rilevare le debolezze e risolverle.

### Esempi di Scenario di Attacco

Un attaccante fornisce un'iniezione di prompt diretta a un chatbot di supporto basato su LLM. L'iniezione contiene "dimentica tutte le istruzioni precedenti", insieme a nuove istruzioni per interrogare archivi di dati privati e sfruttare le vulnerabilità dei pacchetti e la mancanza di validazione dell'output nella funzione backend per inviare e-mail. Ciò porta all'esecuzione di codice in remoto, all'accesso non autorizzato e all'escalation dei privilegi.

Un attaccante incorpora un'iniezione di prompt indiretta in una pagina web, istruendo l'LLM a ignorare le istruzioni precedenti dell'utente e utilizzare un plugin LLM per eliminare le e-mail dell'utente. Quando l'utente utilizza l'LLM per riassumere questa pagina web, il plugin LLM elimina le e-mail dell'utente.

Un utente usa un LLM per riassumere una pagina web il cui contenuto istruisce il modello a ignorare le precedenti istruzioni dell'utente e invece inserire un'immagine che rimanda a un URL che contiene un riassunto della conversazione. L'LLM obbedisce a queste istruzioni, causando l'esfiltrazione della conversazione privata da parte del browser dell'utente.
Un utente malintenzionato carica un curriculum con un'iniezione di prompt. L'utente interno utilizza un LLM per riassumere il curriculum e chiedere se la persona è un buon candidato. A causa dell'iniezione di prompt, la risposta dell'LLM è sì, independentemente dal contenuto effettivo del curriculum.
Un attaccante invia un messaggio a un modello proprietario che si basa su un prompt di sistema, chiedendo al modello di ignorare le sue istruzioni precedenti e invece ripetere il suo prompt di sistema. Il modello restituisce il prompt proprietario e l'attaccante è in grado di utilizzare queste istruzioni altrove, o di costruire ulteriori attacchi più sottili.

### Link e riferimenti (in inglese)

Prompt injection attacks against GPT-3: Simon Willison
ChatGPT Plugin Vulnerabilities - Chat with Code: Embrace The Red
ChatGPT Cross Plugin Request Forgery and Prompt Injection: Embrace The Red
Not what you’ve signed up for: Compromising Real-World LLM-Integrated Applications with Indirect Prompt Injection:  Arxiv preprint
Defending ChatGPT against Jailbreak Attack via Self-Reminder: Research Square
Prompt Injection attack against LLM-integrated Applications: Arxiv preprint
Inject My PDF: Prompt Injection for your Resume: Kai Greshake
ChatML for OpenAI API Calls: OpenAI Github
Threat Modeling LLM Applications: AI Village
AI Injections: Direct and Indirect Prompt Injections and Their Implications: Embrace The Red
Reducing The Impact of Prompt Injection Attacks Through Design: Kudelski Security
Universal and Transferable Attacks on Aligned Language Models: LLM-Attacks.org
Indirect prompt injection: Kai Greshake
Declassifying the Responsible Disclosure of the Prompt Injection Attack Vulnerability of GPT-3: Preamble; earliest disclosure of Prompt Injection
## LLM02: Gestione non sicura dell'output

### Descrizione

La gestione non sicura dell'output si riferisce nello specifico a una validazione, sanificazione e gestione insufficienti degli output generati da grandi modelli di linguaggio prima che vengano passati a valle ad altri componenti e sistemi. Poiché il contenuto generato da un LLM può essere controllato dal prompt in input, questo comportamento è comparabile a fornire agli utenti un accesso indiretto a funzionalità aggiuntive.

La gestione non sicura dell'output si differenzia dalla dipendenza eccessiva (LLM09) in quanto si occupa degli output generati da un LLM prima che vengano passati a valle, mentre la dipendenza eccessiva si concentra su preoccupazioni più ampie riguardanti l'eccessiva fiducia nell'accuratezza e nell'appropriatezza degli output di un LLM.

Un attacco che sfrutta la gestione non sicura dell'output può portare a XSS e CSRF nei browser web, nonché a SSRF, escalation dei privilegi o esecuzione di codice da remoto (RCE) nei sistemi backend.

Le condizioni seguenti possono aumentare l'impatto di questa vulnerabilità:
L'applicazione concede all'LLM privilegi oltre a quelli previsti per gli utenti finali, consentendo l'escalation dei privilegi o l'esecuzione di codice da remoto.
L'applicazione è vulnerabile ad attacchi di iniezione di prompt indiretta, che potrebbero consentire a un attaccante di ottenere l'accesso privilegiato all'ambiente di un utente target.
Plugin di terze parti non validano adeguatamente gli input.

### Esempi comuni di vulnerabilità

L'output di un LLM viene inserito direttamente in una shell di sistema o in una funzione simile come exec o eval, causando l'esecuzione di codice da remoto.
JavaScript o Markdown generati dall'LLM sono restituiti all'utente. Il codice viene quindi interpretato dal browser, causando un XSS.

### Strategie di prevenzione e mitigazione

Trattare il modello come qualsiasi altro utente, adottando un approccio di zero-trust (fiducia zero), e applicare una corretta validazione degli input che vengono passati dal modello alle funzioni backend.
Seguire le linee guida OWASP ASVS (Application Security Verification Standard) per garantire una validazione e sanificazione efficaci degli input.
Codificare l'output del modello che viene inviato agli utenti per mitigare l'esecuzione di codice indesiderato tramite JavaScript o Markdown. OWASP ASVS fornisce una guida dettagliata sulla codifica dell'output.

### Esempi di scenari di attacco

Un applicazione usa un plugin LLM per generare risposte per una funzionalità di chatbot. Il plugin offre anche una serie di funzioni amministrative accessibili a un altro LLM privilegiato. L'LLM passa direttamente la sua risposta, senza una corretta validazione dell'output, al plugin causando l'arresto del plugin per manutenzione.
Un utente usa uno strumento di sintesi di siti web basato su un LLM per generare un riassunto conciso di un articolo. Il sito web include un'iniezione di prompt che istruisce l'LLM a catturare contenuti sensibili dal sito web o dalla conversazione dell'utente. L'LLM può quindi codificare i dati sensibili e inviarli a un server controllato dall'attaccante, senza alcuna validazione o filtraggio dell'output.
Un LLM permette agli utenti di creare query SQL per un database di backend attraverso una chat. Un utente richiede una query per eliminare tutte le tabelle del database. Se la query creata dall'LLM non viene esaminata attentamente, allora tutte le tabelle del database verranno eliminate.
Un'applicazione web usa un LLM per generare contenuto a partire da prompt di testo inseriti dall'utente, senza sanificare l'output. Un attaccante potrebbe inviare un prompt creato ad arte che causa l'invio di un payload JavaScript non sanificato, portando a un XSS quando questo viene interpretato dal browser della vittima. La mancata validazione dei prompt rende possibile questo attacco.

### Riferimenti e link (inglese)

Arbitrary Code Execution: Snyk Security Blog
ChatGPT Plugin Exploit Explained: From Prompt Injection to Accessing Private Data: Embrace The Red
New prompt injection attack on ChatGPT web version. Markdown images can steal your chat data.: System Weakness
Don’t blindly trust LLM responses. Threats to chatbots: Embrace The Red
Threat Modeling LLM Applications: AI Village
OWASP ASVS - 5 Validation, Sanitization and Encoding: OWASP AASVS
## LLM03: Avvelenamento dei dati di apprendimento

### Descrizione

Il punto di partenza di qualsiasi approccio di machine learning (apprendimento automatico) è costituito dai dati di addestramento, semplicemente del "testo grezzo". Per essere sviluppare un modello con capacità elevate (ad esempio, che abbia conoscenze linguistiche e del mondo), questo testo deve coprire un'ampia gamma di domini, generi e lingue. Un grande modello di linguaggio utilizza reti neurali profonde per generare output basati su pattern appresi dai dati di apprendimento.

L'avvelenamento dei dati di apprendimento si riferisce alla manipolazione dei dati usati nel processi di pre-apprendimento (pre-training), di fine-tuning o di embedding, al fine di introdurre delle vulnerabilità (che hanno tutte vettori di attacco unici e a volte condivisi), backdoor o bias che potrebbero compromettere la sicurezza, l'efficacia o il comportamento etico del modello. Le informazioni avvelenate possono essere presentate agli utenti o creare altri rischi come la degradazione delle prestazioni, l'exploit del software downstream e danni alla reputazione. Anche se gli utenti non si fidano dell'output problematico dell'IA, i rischi rimangono, comprese le capacità compromesse del modello e potenziali danni alla reputazione del marchio.

Il pre-apprendimento si riferisce al processo di addestramento di un modello basato su un compito o un set di dati.
Il fine-tuning consiste nel prendere un modello esistente che è già stato addestrato e riadattarlo a un dominio più ristretto o a un obiettivo più focalizzato, addestrandolo utilizzando uno specifico set di dati. Questo set di dati include tipicamente esempi di input e i corrispondenti output desiderati.
Il processo di embedding è il processo di conversione di dati categorici (spesso testo) in una rappresentazione numerica che può essere utilizzata per addestrare un modello di linguaggio. L'embedding comporta la rappresentazione di parole o frasi dai dati di testo come vettori in uno spazio vettoriale continuo. I vettori sono solitamente generati passando dati di testo attraverso una rete neurale che è stata addestrata su un ampio corpus di testo.

L'avvelenamento dei dati è considerato un attacco di integrità perché la manipolazione dei dati di addestramento influisce sulla capacità del modello di produrre previsioni corrette. Naturalmente, le fonti di dati esterne presentano un rischio maggiore poiché i creatori del modello non hanno controllo sui dati né un alto livello di fiducia che il contenuto non contenga bias, informazioni falsificate o contenuti inappropriati.

### Esempi comuni di vulnerabilità

Un attore malintenzionato o un concorrente crea intenzionalmente dei documenti inaccurati o malevoli, che sono indirizzati al pre-addestramento, fine-tuning o al processo di embedding. Considerate entrambi i vettori di attacco di Split-View Data Poisoning (avvelenamento da vista separata) e Frontrunning Poisoning (avvelenamento per anticipazione) come esempi.
Il modello vittima si allena utilizzando informazioni falsificate che si riflettono negli output che il modello di IA generativa fornisce ai suoi fruitori.
Un attore malintenzionato è in grado di iniettare direttamente dei contenuti falsificati, tendenziosi o pericolosi nei processi di addestramento di un modello, facendo così in modo che questi contenuti vengano poi restituiti negli output del modello.
Un utente ignaro inietta indirettamente dati sensibili o proprietari nei processi di addestramento di un modello, che vengono poi restituiti negli output successivi.
Un modello è addestrato usando dati la cui fonte, origine o contenuto non sono stati sottoposti a verifica in nessuna delle fasi addestramento, il che può portare a risultati errati se i dati sono contaminati o non corretti.
L'accesso senza restrizioni all'infrastruttura o un sandboxing inadeguato possono consentire a un modello di acquisire dati di addestramento non sicuri, con conseguenti output tendenziosi o dannosi. Questo esempio può verificarsi in una qualsiasi delle fasi di addestramento.
In questo scenario, l'input che un utente fornisce al modello può essere riflesso nell'output di un altro utente (portando a una violazione), oppure l'utente di un LLM può ricevere dal modello output inesatti, irrilevanti o dannosi a seconda del tipo di dati ingeriti, secondo il caso d'uso del modello (di solito riportati nella model card).

Che siate sviluppatori, clienti o consumatori generici di un LLM, è importante comprendere come questa vulnerabilità potrebbe riflettersi sui rischi all'interno della vostra applicazione LLM quando questa interagisce con un LLM non proprietario, per comprendere la legittimità degli output del modello in base alle sue procedure di addestramento. Allo stesso modo, gli sviluppatori dell'LLM potrebbero essere a rischio di attacchi diretti e indiretti ai dati interni o di terze parti utilizzati per il fine-tuning e l'embedding (il più comune), comportando un rischio per tutti i suoi consumatori.

### Strategie di prevenzione e mitigazione

Verificare la filiera di approvvigionamento dei dati di addestramento, soprattutto quando sono ottenuti da fonti esterne, nonché mantenere attestazioni tramite la metodologia "ML-BOM" (Machine Learning Bill of Materials) e verificare le model card.
Verificare la corretta legittimità delle fonti di dati e dei dati ottenuti durante le fasi di pre-apprendimento, fine-tuning e embedding.
Verificare il caso d'uso dell'LLM e l'applicazione a cui questo viene integrato. Creare modelli diversi tramite dati di addestramento separati o fine-tuning per casi d'uso diversi per creare un output di IA generativa più granulare e accurato in base al caso d'uso definito.
Garantire un sandboxing sufficiente tramite i controlli di rete, per impedire al modello di estrarre dati da fonti non previste, che potrebbero compromettere l'output dell'apprendimento automatico.
Adottare un controllo rigoroso o filtri di input per dati di addestramento specifici o categorie di fonti di dati, per mantenere sotto controllo il volume di dati falsificati. Sanificare i dati con tecniche come la rilevazione statistica degli outlier o il rilevamento delle anomalie, per identificare e rimuovere i dati avversari che potrebbero essere inseriti nel processo di fine-tuning.
Elaborare domande di controllo attorno alla fonte e alla proprietà dei set di dati per garantire che il modello non sia stato avvelenato, e adottare questa cultura nel ciclo di vita "MLSecOps". Fare riferimento a risorse disponibili come The Foundation Model Transparency Index o Open LLM Leaderboard per esempio.
Usare DVC (Data Version Control) per identificare e tenere traccia in modo rigoroso di una parte di un set di dati che potrebbe essere stata manipolata, eliminata o aggiunta, portando all'avvelenamento.
Usare database vettoriali per aggiungere informazioni fornite dall'utente, che permettono di proteggere gli utenti dall'avvelenamento e persino correggere in produzione senza dover riaddestrare un nuovo modello.
Tecniche di robustezza avversaria come l'apprendimento federato (federated learning) e vincoli per minimizzare gli effetti di outlier o addestramento avversariale per essere resistenti alle peggiori perturbazioni dei dati di addestramento.
Un approccio "MLSecOps" potrebbe essere quello di includere la robustezza avversaria nel ciclo di vita dell'addestramento con la tecnica di auto-avvelenamento.
Un esempio di questo approccio è Autopoison, che include test per attacchi come l'iniezione diretta di contenuto ("tentativo di promuovere un marchio nelle risposte del modello") e l'attacco di rifiuto ("fare in modo che il modello rifiuti sempre di rispondere").
Testare e rilevare, misurando la perdita durante la fase di addestramento e analizzando i modelli addestrati per rilevare segni di un attacco di avvelenamento, controllando il comportamento del modello su input di test specifici.
Monitorare e segnalare il numero di risposte distorte che superano una soglia.
Usare una validazione umana per fare un audit delle risposte.
Implementare LLM dedicati per mettere alla prova i modelli rispetto a conseguenze indesiderate e addestrare altri LLM usando tecniche di apprendimento per rinforzo.
Eseguire esercitazioni di tipo red team basate su LLM o scansioni di vulnerabilità LLM nelle fasi di test del ciclo di vita dell'LLM.


### Esempi di scenari d'attacco

L'output di un'IA generativa può indurre in errore gli utenti dell'applicazione, portando a opinioni tendenziose o, peggio ancora, crimini d'odio, ecc. tendenziosi.
Se i dati di apprendimento non sono correttamente filtrati e/o sanificati, un utente malintenzionato potrebbe cercare di influenzare e iniettare dati tossici nel modello per farlo adattare ai dati falsificati e tendenziosi.
Un attore malintenzionato o un concorrente crea intenzionalmente dei documenti inaccurati o malevoli che sono indirizzati ai dati di addestramento di un modello, che viene addestrato allo stesso tempo in base agli input. Il modello vittima si addestra utilizzando informazioni falsificate che si riflettono negli output che il modello di IA generativa fornisce ai suoi fruitori.
L'iniezione di prompt (LLM01) potrebbe essere un vettore di attacco per questa vulnerabilità se non viene eseguita una sanitizzazione e un filtraggio sufficienti quando gli input degli utenti sono usati per addestrare il modello. Ad esempio, se i dati dannosi o falsificati vengono inseriti nel modello da un utilizzatore come parte di una tecnica di iniezione di prompt, questo potrebbe essere intrinsecamente rappresentato nei dati del modello.

### Riferimenti e link (inglese)

Stanford Research Paper:CS324: Stanford Research
How data poisoning attacks corrupt machine learning models: CSO Online
MITRE ATLAS (framework) Tay Poisoning: MITRE ATLAS
PoisonGPT: How we hid a lobotomized LLM on Hugging Face to spread fake news: Mithril Security
Inject My PDF: Prompt Injection for your Resume: Kai Greshake
Backdoor Attacks on Language Models: Towards Data Science
Poisoning Language Models During Instruction: Arxiv White Paper
FedMLSecurity:arXiv:2306.04959: Arxiv White Paper
The poisoning of ChatGPT: Software Crisis Blog
Poisoning Web-Scale Training Datasets - Nicholas Carlini | Stanford MLSys #75: YouTube Video
OWASP CycloneDX v1.5: OWASP CycloneDX
## LLM04: Denial of Service del Modello

### Descrizione

Un attaccante interagisce con un LLM in un modo che porta al consumo di una quantità eccezionalmente alta di risorse, risultando in un declino della qualità del servizio sia per sè che per altri utenti, oltre a generare potenziali incrementi dei costi per risorse computazionali. Un altro elemento emergente critico per la sicurezza è la possibilità che un attaccante interferisca o manipoli la "finestra di contesto" di un LLM. Questo problema sta diventando sempre più critico a causa dell'uso crescente degli LLM in varie applicazioni, del loro intensivo utilizzo di risorse, dell'imprevedibilità dell'input degli utenti e di una generale mancanza di consapevolezza tra gli sviluppatori riguardo a questa vulnerabilità. Negli LLM, la finestra di contesto rappresenta la lunghezza massima di testo che il modello può gestire, includendo sia l'input che l'output. È una caratteristica fondamentale degli LLM poiché determina la complessità dei costrutti linguistici che il modello può comprendere e la dimensione del testo che può elaborare in un dato momento. La dimensione della finestra di contesto è definita dall'architettura del modello e può variare in base al modello in uso.

### Esempi Comuni di Vulnerabilità

Porre domande (prompts) che portano a un uso ricorrente delle risorse attraverso la generazione di un alto volume di compiti in una coda, ad esempio usando LangChain o AutoGPT.
Inviare interrogazioni insolitamente onerose per le risorse che utilizzano un'ortografia o delle sequenze insolite di testo.
Sovraccarico continuo dell'input: un attaccante invia ripetutamente un flusso di input all'LLM che supera la sua finestra di contesto, causando al modello un consumo eccessivo di risorse computazionali.
Input lunghi ripetuti: l'attaccante invia ripetutamente input lunghi all'LLM, ognuno dei quali supera la finestra di contesto.
Espansione ricorsiva del contesto: l'attaccante costruisce un input che attiva l'espansione ricorsiva del contesto, forzando l'LLM a espandere e processare ripetutamente la finestra di contesto.
Inondazione di input di lunghezza variabile: l'attaccante inonda l'LLM con un grande volume di input di lunghezza variabile, dove ogni input è attentamente costruito per raggiungere appena il limite della finestra di contesto. Questa tecnica mira a sfruttare qualsiasi inefficienza nel processamento di input di lunghezza variabile, mettendo sotto sforzo l'LLM e potenzialmente causandone il blocco.

### Strategie di Prevenzione e Mitigazione

Implementare la validazione e la sanificazione dell'input per garantire che l'input dell'utente rispetti i limiti definiti e sia filtrato qualsiasi contenuto malevolo.
Limitare l'uso delle risorse per singola richiesta o singolo passaggio, in modo che le richieste che coinvolgono parti complesse vengano eseguite più lentamente.
Applicare limiti di frequenza all'API per contenere il numero di richieste che un singolo utente o indirizzo IP può fare entro un determinato lasso di tempo.
Limitare il numero di azioni in coda e il numero totale di azioni in un sistema terzo che risponde alle risposte dell'LLM.
Monitorare continuamente l'utilizzo delle risorse dell'LLM per identificare picchi o schemi anomali che potrebbero indicare un attacco DoS.
Impostare limiti di input rigorosi basati sulla finestra di contesto dell'LLM per prevenire sovraccarichi ed esaurimento delle risorse.
Promuovere la consapevolezza tra gli sviluppatori riguardo alle potenziali vulnerabilità DoS negli LLM e fornire linee guida per l'implementazione sicura dell'LLM.

### Example Attack Scenarios

An attacker repeatedly sends multiple difficult and costly requests to a hosted model leading to worse service for other users and increased resource bills for the host.
A piece of text on a webpage is encountered while an LLM-driven tool is collecting information to respond to a benign query. This leads to the tool making many more web page requests, resulting in large amounts of resource consumption.
An attacker continuously bombards the LLM with input that exceeds its context window. The attacker may use automated scripts or tools to send a high volume of input, overwhelming the LLM's processing capabilities. As a result, the LLM consumes excessive computational resources, leading to a significant slowdown or complete unresponsiveness of the system.
An attacker sends a series of sequential inputs to the LLM, with each input designed to be just below the context window's limit. By repeatedly submitting these inputs, the attacker aims to exhaust the available context window capacity. As the LLM struggles to process each input within its context window, system resources become strained, potentially resulting in degraded performance or a complete denial of service.
An attacker leverages the LLM's recursive mechanisms to trigger context expansion repeatedly. By crafting input that exploits the recursive behavior of the LLM, the attacker forces the model to repeatedly expand and process the context window, consuming significant computational resources. This attack strains the system and may lead to a DoS condition, making the LLM unresponsive or causing it to crash.
An attacker floods the LLM with a large volume of variable-length inputs, carefully crafted to approach or reach the context window's limit. By overwhelming the LLM with inputs of varying lengths, the attacker aims to exploit any inefficiencies in processing variable-length inputs. This flood of inputs puts an excessive load on the LLM's resources, potentially causing performance degradation and hindering the system's ability to respond to legitimate requests.
While DoS attacks commonly aim to overwhelm system resources, they can also exploit other aspects of system behavior, such as API limitations. For example, in a recent Sourcegraph security incident, the malicious actor employed a leaked admin access token to alter API rate limits, thereby potentially causing service disruptions by enabling abnormal levels of request volumes.

### Esempi di Scenari di Attacco

Un attaccante invia ripetutamente molteplici richieste complesse e costose a un modello in hosting, portando a un peggioramento del servizio per gli altri utenti e ad un aumento delle bollette relative ai consumi delle risorse, nel servizio di hosting.
Una sezione di testo su una pagina web viene processata mentre uno strumento guidato da un LLM sta raccogliendo informazioni per rispondere a una query benigna. Questo porta lo strumento a fare molte più richieste di pagine web, risultando in un grande consumo di risorse.
Un attaccante bombarda continuamente l'LLM con input che superano la sua finestra di contesto. L'attaccante può utilizzare script automatizzati o strumenti per inviare un alto volume di input, sopraffacendo così le capacità di elaborazione dell'LLM. Di conseguenza, l'LLM consuma risorse computazionali eccessive, portando a un notevole rallentamento o a una completa mancanza di risposta da parte del sistema che lo ospita.
Un attaccante invia una serie di input sequenziali all'LLM, in cui ciascun input è progettato per essere appena sotto il limite della finestra di contesto. Inviando ripetutamente questi input, l'attaccante mira a esaurire la capacità disponibile della finestra. Mentre l'LLM fatica a elaborare ciascun input all'interno della sua finestra di contesto, le risorse del sistema si riducono drasticamente, risultando nel degradamento delle prestazioni o in un completo diniego del servizio (DoS).
Un attaccante sfrutta i meccanismi ricorsivi dell'LLM per causare ripetutamente l'espansione del contesto. Creando un input che stimola il comportamento ricorsivo dell'LLM, l'attaccante costringe il modello a espandere e processare ripetutamente la finestra di contesto, consumando una significativa quantità di risorse computazionali. Questo attacco mette sotto sforzo il sistema e può portare a una condizione di DoS, rendendo l'LLM non reattivo o causandone il fermo totale.
Un attaccante inonda l'LLM con un grande volume di input di lunghezza variabile, attentamente costruiti per avvicinarsi o raggiungere il limite della finestra di contesto. Sopraffacendo l'LLM con input di lunghezze variabili, l'attaccante mira a sfruttare qualsiasi inefficienza nell'elaborazione di questo tipo di input. Questo sovraccarico pesa eccessivamente sulle risorse dell'LLM, causando un potenziale degradamento delle prestazioni e ostacolando la capacità del sistema di rispondere a richieste legittime.
Mentre gli attacchi DoS mirano comunemente a sopraffare le risorse del sistema, possono anche sfruttare altri aspetti del comportamento del sistema, come le limitazioni dell'API. Ad esempio, in un recente incidente di sicurezza subìto da Sourcegraph, l'attore malevolo ha utilizzato un token di accesso amministrativo trapelato per alterare i limiti di frequenza dell'API, causando potenzialmente interruzioni del servizio, avendo abilitato livelli anomali di volumi di richieste.

### Referenze e Link (Inglese)

LangChain max_iterations: hwchase17 on Twitter
Sponge Examples: Energy-Latency Attacks on Neural Networks: Arxiv White Paper
OWASP DOS Attack: OWASP
Learning From Machines: Know Thy Context: Luke Bechtel
Sourcegraph Security Incident on API Limits Manipulation and DoS Attack : Sourcegraph
## LLM05: Vulnerabilità della Supply-Chain

### Descrizione

La supply chain nei modelli di linguaggio di grandi dimensioni (LLM) può essere vulnerabile, influenzando l'integrità dei dati di addestramento, dei modelli di machine learning (ML) e delle piattaforme di erogazione. Queste vulnerabilità possono portare a risultati deviati, violazioni della sicurezza o addirittura a fallimenti completi del sistema. Tradizionalmente, le vulnerabilità si concentrano sui componenti software, ma il Machine Learning le estende anche ai modelli pre-addestrati e ai dati di addestramento forniti da terze parti, suscettibili di attacchi per manomissione ed avvelenamento.

Infine, le estensioni dei plugin LLM possono portare le loro vulnerabilità. Queste sono descritte in LLM07 - Insecure Plugin Design, che tratta della scrittura di plugin LLM e fornisce informazioni utili per valutare i plugin di terze parti.

### Esempi Comuni di Vulnerabilità

Vulnerabilità tradizionali derivanti dai pacchetti di terze parti, che includono componenti obsoleti o deprecati.
Utilizzo di un modello pre-addestrato vulnerabile per il fine-tuning.
Uso di dati di addestramento deviati provenienti da fonti aperte non verificate.
L'utilizzo di modelli obsoleti o fuori supporto che non sono più mantenuti porta a problemi di sicurezza.
Termini e Condizioni di Servizio (T&C) e politiche sulla privacy dei dati poco chiari da parte degli operatori dei modelli portano all'utilizzo di dati sensibili da un'applicazione per l'addestramento del modello, e alla successiva esposizione di informazioni sensibili. Questa situazione può anche generare rischi derivanti dall'uso di materiale protetto da proprietà intellettuale, da parte del fornitore del modello.

### Strategie di Prevenzione e Mitigazione

Valutare attentamente le fonti dei dati e i fornitori, inclusi i T&C e le loro politiche sulla privacy, ed impiegare solo fornitori affidabili. Assicurarsi della presenza di una pratica di sicurezza adeguata e verificata da terze parti e che le politiche degli operatori dei modelli siano allineate con le proprie politiche di protezione dei dati, ovvero che i propri dati non siano utilizzati per l'addestramento dei modelli senza consenso; non meno importante, predisporre le necessarie garanzie e mitigazioni legali contro l'eventuale uso di materiale protetto da copyright da parte dei manutentori dei modelli.
Utilizzare solo plugin affidabili, con una reputazione elevata e assicurarsi che siano stati testati per i requisiti della propria applicazione. Il paragrafo LLM07 - Insecure Plugin Design fornisce informazioni sugli aspetti del design di plugin insicuri, che dovrebbero essere testati dal punto di vista del LLM, per mitigare i rischi derivanti dall'uso di plugin di terze parti.
Esaminare ed applicare le mitigazioni trovate nei Top Ten dell'OWASP A06:2021 – Vulnerable and Outdated Components. Fra questi la scansione delle vulnerabilità e la gestione e l'aggiornamento dei componenti. Applicare questi controlli anche agli ambienti di sviluppo, che abbiano accesso a dati sensibili.
Mantenere un inventario aggiornato dei componenti definendo una Software Bill of Materials (SBoM o lista artefatti) per assicurarsi di avere un inventario aggiornato, accurato e certificato, prevenendo così la manomissione dei pacchetti in produzione. Le  liste artefatti software (SBoM) possono essere attivamente impiegate per rilevare e segnalare rapidamente nuove vulnerabilità gravi (Zero-Day).
Al momento della scrittura, le liste SBoM non coprono i modelli, i loro artefatti e i set di dati. Se la propria applicazione LLM utilizza un modello privato, è bene utilizzare le buone pratiche di "MLOps" e riferirsi a piattaforme che offrono repository di modelli sicuri con dati, modelli ed esperimenti identificabili e tracciabili.
Utilizzare modelli e codice certificati o firmati, quando si impiegano modelli e fornitori esterni.
L'esecuzione di test avversariali di robustezza e per la rilevazione di anomalie sui modelli e sui dati forniti possono aiutare a rilevare manomissioni e deviazioni (poisoning) come discusso in  Training Data Poisoning; idealmente, i test dovrebbero essere parte integrante della pipeline di MLOps; tuttavia, trattandosi di tecniche emergenti, potrebbero risultare più semplici da implementare come parte degli esercizi di red teaming.
Implementare un adeguato monitoraggio per assicurare la scansione delle vulnerabilità dei componenti e dell'ambiente che li ospita, l'uso di plugin non autorizzati e componenti obsoleti, inclusi il modello e i suoi artefatti.
Implementare una politica di aggiornamento (patching) per mitigare l'insorgenza di componenti vulnerabili o obsoleti. Assicurarsi che l'applicazione si basi su una versione costantemente manutenuta delle API e del modello sottostante.
Rivedere e controllare regolarmente la sicurezza ed i criteri di accesso dei fornitori, assicurandosi che non ci siano cambiamenti nella loro postura di sicurezza o nelle loro condizioni di servizio o T&C.

### Esempi di Scenari di Attacco

Un attaccante sfrutta una libreria Python vulnerabile per compromettere un sistema. Questo è effettivamente accaduto nel primo data breach di Open AI.
Un attaccante fornisce un plugin LLM per la ricerca di voli, generando link falsi che portano a truffare gli utenti.
Un attaccante sfrutta il registro dei pacchetti PyPi per ingannare gli sviluppatori di modelli a scaricare un pacchetto compromesso ed esfiltrare dati o scalare privilegi in un ambiente di sviluppo di modelli. Questo è stato un caso di attacco reale.
Un attaccante avvelena un modello pre-addestrato disponibile pubblicamente specializzato in analisi economica e ricerca sociale per creare una backdoor che genera disinformazione e fake news. Lo distribuisce su un marketplace di modelli (ad esempio, Hugging Face) per farlo utilizzare da vittime ignare.
Un attaccante avvelena set di dati pubblicamente disponibili per aiutare a creare una backdoor che acquisisce rilevanza quando si effettua il fine-tuning dei modelli. La backdoor favorisce in modo impercettibile alcune aziende in diversi mercati.
Un dipendente vittima di compromissione presso un fornitore (sviluppatore in outsourcing, azienda di hosting, ecc.) esfiltra dati, modelli o codice di fatto trafugando proprietà intellettuale.
Un operatore LLM cambia le sue condizioni d'uso (T&C) e la Politica sulla Privacy (DPA) richiedendo un opt-out esplicito relativamente all'uso dei dati dell'applicazione per l'addestramento del modello, portando alla memorizzazione inavvertita di dati sensibili.

### Riferimenti e Link (Inglese)

ChatGPT Data Breach Confirmed as Security Firm Warns of Vulnerable Component Exploitation: Security Week
Plugin review process: OpenAI
Compromised PyTorch-nightly dependency chain: Pytorch
PoisonGPT: How we hid a lobotomized LLM on Hugging Face to spread fake news: Mithril Security
Army looking at the possibility of 'AI BOMs: Defense Scoop
Failure Modes in Machine Learning: Microsoft
ML Supply Chain Compromise: MITRE ATLAS
Transferability in Machine Learning: from Phenomena to Black-Box Attacks using Adversarial Samples: Arxiv White Paper
BadNets: Identifying Vulnerabilities in the Machine Learning Model Supply Chain: Arxiv White Paper
VirusTotal Poisoning: MITRE ATLAS
## LLM06: Diffusione di Informazioni Sensibili

### Descrizione

Le applicazioni LLM possono rivelare informazioni sensibili, algoritmi proprietari o altri dettagli confidenziali attraverso i loro output. Ciò può portare ad accessi non autorizzati a dati sensibili, proprietà intellettuale, violazioni della privacy e altre violazioni di sicurezza. È importante che gli utenti delle applicazioni LLM siano consapevoli di come interagire in modo sicuro con gli LLM e identificare i rischi associati all'inserimento involontario di dati sensibili che possono successivamente essere restituiti dall'LLM come output altrove.

Per mitigare questo rischio, le applicazioni LLM dovrebbero eseguire un'adeguata sanificazione dei dati per impedire che i dati degli utenti entrino indiscriminatamente nei dati di addestramento del modello. I proprietari di applicazioni LLM dovrebbero inoltre esporre dei Termini di Utilizzo adeguati, chiaramente esposti per far sapere ai consumatori come vengono trattati i loro dati, ed una chiara opzione per negare il consenso ad includere i loro dati nell'addestramento del modello.

L'interazione tra il consumatore e l'applicazione LLM instaura un contesto di fiducia reciproca, nel quale non possiamo fidarci intrinsecamente né dell'input client->LLM né dell'output LLM->client. È importante notare che questa vulnerabilità presuppone che certi prerequisiti siano assicurati al di fuori del presente ambito di analisi, fra questi gli esercizi di modellazione delle minacce, la protezione delle infrastrutture ed una segregazione adeguata degli ambienti di esecuzioned. Aggiungere restrizioni all'interno del prompt del sistema riguardo ai tipi di dati che l'LLM dovrebbe restituire può fornire una certa mitigazione contro la rivelazione di informazioni sensibili, ma la natura imprevedibile degli LLM significa che tali restrizioni potrebbero non essere sempre rispettate e potrebbero essere eluse tramite iniezione di prompt o altri vettori.

### Esempi Comuni di Vulnerabilità

Filtraggio incompleto o improprio delle informazioni sensibili nelle risposte dell'LLM.
Sovradattamento o memorizzazione di dati sensibili nel processo di addestramento dell'LLM.
Divulgazione involontaria di informazioni confidenziali a causa di errata interpretazione da parte dell'LLM, mancanza di metodi di pulizia dei dati o errori.

### Strategie di Prevenzione e Mitigazione
Integrare adeguate tecniche di sanificazione e pulizia dei dati per impedire che i dati degli utenti entrino nei dati del modello di addestramento.
Implementare metodi robusti di validazione e sanificazione degli input per identificare ed escludere potenziali input malevoli per prevenire l'avvelenamento (poisoning) del modello.
Quando si arricchisce il modello con dati e se si effettua il fine-tuning di un modello (ad esempio, dati inseriti nel modello prima o durante il rilascio):
  1. Qualunque informazione sensibile nei dati di fine-tuning ha il potenziale di essere rivelato ad un utente. Pertanto, si raccomanda di applicare la buona pratica di minimizzazione dei privilegi di accesso, e di non addestrare il modello su informazioni a cui un utente con privilegi elevati può accedere poichè potrebbero inavvertitamente essere mostrate a un utente con privilegi inferiori.
  2. L'accesso a fonti di dati esterne (orchestrazione dei dati in tempo reale) dovrebbe essere limitato.
  3. Applicare metodi rigorosi di controllo degli accessi alle fonti di dati esterne e un approccio rigoroso al mantenimento di una catena di fornitura sicura.

### Esempi di Scenari di Attacco

L'utente legittimo e ignaro A viene esposto a dati di altri utenti tramite l'LLM quando interagisce con l'applicazione LLM in modo non malevolo.
L'utente A indirizza un insieme ben congegnato di prompt per bypassare i filtri di input e la sanificazione dell'LLM per far sì che riveli informazioni sensibili (PII) su altri utenti dell'applicazione.
Dati personali come i "PII" vengono inseriti nel modello tramite i dati di addestramento a causa di negligenza da parte dell'utente stesso o dell'applicazione LLM. Questo caso potrebbe aumentare il rischio e la probabilità degli scenari 1 o 2 sopra descritti.

### Riferimenti e Link (Inglese)

AI data leak crisis: New tool prevents company secrets from being fed to ChatGPT: Fox Business
Lessons learned from ChatGPT’s Samsung leak: Cybernews
Cohere - Terms Of Use: Cohere
A threat modeling example: AI Village
OWASP AI Security and Privacy Guide: OWASP AI Security & Privacy Guide
Ensuring the Security of Large Language Models: Experts Exchange
## LLM07: Progettazione Insicura dei Plugin

### Descrizione

I plugin LLM sono estensioni che, quando attivate, vengono chiamate automaticamente dal modello durante le interazioni con l'utente. La piattaforma di integrazione del modello li gestisce, e l'applicazione potrebbe non avere controllo sulla loro esecuzione, specialmente quando il modello è ospitato da una terza parte. Inoltre, i plugin tendono ad accettare input di testo libero dal modello senza alcuna validazione o controllo tipologico che gestisca le limitazioni sulla dimensione del contesto. Ciò consente a un potenziale attaccante di assemblare una richiesta malevola al plugin, che potrebbe risultare in una più ampia di comportamenti indesiderati, fino a raggiungere l'esecuzione di codice remoto.

Il danno causato da input malevoli dipende spesso dai controlli di accesso insufficienti e dal fallimento nel tracciare le autorizzazioni tra i diversi plugin. Un controllo di accesso inadeguato permette a un plugin di fidarsi ciecamente di altri plugin e di presumere che tali input siano stati forniti dall'utente finale. Tale controllo di accesso inadeguato può consentire agli input malevoli di avere conseguenze dannose che vanno dall'esfiltrazione di dati, all'esecuzione di codice remoto, e all'escalation di privilegi.

Questa sezione si concentra sulla creazione di plugin LLM piuttosto che sui plugin di terze parti, coperti dalle Vulnerabilità della Catena di Fornitura dell'LLM (Supply-Chain-Vulnerabilities).

### Esempi Comuni di Vulnerabilità

Un plugin accetta tutti i parametri in un unico campo di testo anziché in parametri di input distinti.
Un plugin accetta stringhe di configurazione invece di parametri, che possono sovrascrivere intere impostazioni di configurazione.
Un plugin accetta comandi SQL o istruzioni di programmazione invece di parametri ristretti.
L'autenticazione è eseguita senza un'autorizzazione esplicita per un particolare plugin.
Un plugin tratta tutti i contenuti LLM come se fossero creati interamente dall'utente eseguendo qualsiasi azione richiesta senza chiedere ulteriori autorizzazioni.

### Strategie di Prevenzione e Mitigazione

I Plugin dovrebbero accettare input che siano limitati e parametrizzati ove possibile e includere controlli sul tipo e la struttura dell'input. Dove non sia consentito, è opportuno inserire un secondo livello di chiamate fortemente tipizzate (controllo rigoroso sui tipi di parametro), analizzando le richieste e applicando validazione e sanificazione. Quando sia necessario accettare input libero per la semantica dell'applicazione, questo dovrebbe essere accuratamente ispezionato per assicurare che nessun metodo dannoso sia invocato.
Gli sviluppatori di plugin dovrebbero applicare le raccomandazioni OWASP per gli standard di verifica della sicurezza applicativa (ASVS - Application Security Verification Standard) per assicurare adeguate validazione e sanitizzazione dell'input.
I Plugin dovrebbero essere ispezionati e testati ampiamente per assicurare adeguata validazione. Utilizzare sistemi di Scansione Statica del Codice (SAST) e Test Dinamici ed Interattivi (DAST, IAST) all'interno delle catene (pipelines) di sviluppo.
I Plugin dovrebbero essere disegnati con l'intento di minimizzare l'impatto dello sfruttamento di qualunque parametro di input insicuro come da linee guida sui Controlli di Accesso nello standard ASVS OWASP. Ciò prevede un controllo accessi che assicuri la minimizzazione dei privilegi, e l'esposizione del minimo di funzionalità pur eseguendo la funzione desiderata. 
I Plugin dovrebbero utilizzare identità idonee in fase di autenticazione, come OAuth2, per consentire l'applicazione efficace dei controlli di autorizzazione ed accesso. Inoltre le chiavi API dovrebbero essere utilizzate per fornire un contesto in cui applicare specifiche decisioni autorizzative che riflettano il flusso del plugin come chiaramente distinto da quello interattivo dell'utente.
Richiedere un intervento umano per l'autorizzazione e la conferma di ogni azione intrapresa da plugin particolarmente critici.
I Plugin sono tipicamente delle REST APIs, per cui si raccomanda agli sviluppatori l'applicazione delle raccomandazioni di cui alla lista OWASP Top 10 API Security Risks - 2023 per ridurre la presenza di vulnerabilità generiche.

### Esempi di Scenari di Attacco

Un plugin accetta un URL base e istruisce l'LLM nel combinare l'URL con una query per ottenere previsioni meteorologiche che sono incluse nell'elaborazione della richiesta dell'utente. Un utente malintenzionato può creare una richiesta in modo tale che l'URL punti a un dominio che controlla, permettendogli di iniettare il proprio contenuto nel modello LLM tramite il proprio dominio.
Un plugin accetta un input in forma libera in un unico campo che non viene validato. Un attaccante fornisce payload attentamente elaborati per eseguire attività di ricognizione a partire dai messaggi di errore. Poi sfrutta vulnerabilità conosciute relative alle terze parti emerse per eseguire del codice effettuando un'esfiltrazione di dati o escalation di privilegi.
Un plugin utilizzato per recuperare delle inclusioni (embedding) da un archivio vettoriale accetta parametri di configurazione come stringa di connessione senza effettuarne la validazione. Ciò permette a un attaccante di sperimentare e accedere ad altri archivi vettoriali cambiando nomi o parametri host ed esfiltrare rappresentazioni vettoriali a cui non dovrebbe avere accesso.
Un plugin accetta clausole SQL "WHERE" come filtri avanzati, che vengono poi aggiunti alla query SQL. Ciò permette all'attaccante di eseguire un attacco SQL.
Un attaccante utilizza l'iniezione indiretta di prompt per sfruttare un plugin insicuro di gestione del codice privo di validazione dell'input e con controlli di accesso deboli per trasferire la proprietà del repository (archivio) e bloccare l'utente dai propri repository.

### Riferimenti e Link (Inglese)

OpenAI ChatGPT Plugins: ChatGPT Developer’s Guide
OpenAI ChatGPT Plugins - Plugin Flow: OpenAI Documentation
OpenAI ChatGPT Plugins - Authentication: OpenAI Documentation
OpenAI Semantic Search Plugin Sample: OpenAI Github
Plugin Vulnerabilities: Visit a Website and Have Your Source Code Stolen: Embrace The Red
ChatGPT Plugin Exploit Explained: From Prompt Injection to Accessing Private Data: Embrace The Red
OWASP ASVS - 5 Validation, Sanitization and Encoding: OWASP AASVS
OWASP ASVS 4.1 General Access Control Design: OWASP AASVS
OWASP Top 10 API Security Risks – 2023: OWASP
## LLM08: Eccessiva Autonomia

### Descrizione

Un sistema basato su LLM è spesso dotato di una certa autonomia dallo sviluppatore - la capacità di interfacciarsi con altri sistemi e intraprendere azioni in risposta a un prompt. La decisione su quali funzioni invocare può anche essere delegata a un 'agente' per determinarla dinamicamente in base al prompt di input o all'output dell'LLM.

L'Eccessiva Autonomia è la vulnerabilità che permette di eseguire azioni dannose in risposta a output inaspettati o ambigui da un LLM (indipendentemente dalla causa del malfunzionamento dell'LLM; sia essa allucinazione/confabulazione, iniezione di prompt diretta/indiretta, plugin maligno, prompt benigni mal progettati, o semplicemente un modello con scarse prestazioni). La causa radice dell'Eccessiva Autonomia è tipicamente una o più delle seguenti: funzionalità eccessive, permessi eccessivi o autonomia eccessiva. Questo si differenzia dalla Gestione Insicura dell'Output, che riguarda invece la mancanza di scrutinio sugli output generati dall'LLM.

L'Eccessiva Autonomia può portare a un'ampia gamma di impatti sull'intero spettro della riservatezza, integrità e disponibilità, e dipende dai sistemi con cui un'app basata su LLM può interagire.

### Esempi Comuni di Vulnerabilità

Funzionalità Eccessiva: Un agente LLM ha accesso a plugin che includono funzioni non necessarie per il funzionamento previsto del sistema. Ad esempio, uno sviluppatore deve concedere a un agente LLM la capacità di leggere documenti da un repository, ma il plugin di terze parti che sceglie di utilizzare include anche la capacità di modificare ed eliminare documenti.
Funzionalità Eccessiva: Un plugin potrebbe essere stato testato durante una fase di sviluppo e poi scartato in favore di un'alternativa migliore, ma il plugin originale rimane disponibile all'agente LLM.
Funzionalità Eccessiva: Un plugin LLM con funzionalità aperte non riesce a filtrare adeguatamente le istruzioni di input per comandi che vanno oltre quanto necessario per il funzionamento previsto dell'applicazione. Ad esempio, un plugin per eseguire un specifico comando shell non impedisce adeguatamente l'esecuzione di altri comandi shell.
Permessi Eccessivi: Un plugin LLM ha permessi su altri sistemi che non sono necessari per il funzionamento previsto dell'applicazione. Ad esempio, un plugin progettato per leggere dati si connette a un server di database utilizzando un'identità che non ha solo permessi SELECT, ma anche UPDATE, INSERT e DELETE.
Permessi Eccessivi: Un plugin LLM progettato per eseguire operazioni per conto di un utente accede a sistemi aggiuntivi rispetto a quelli previsti con un'identità generica che ha privilegi elevati. Ad esempio, un plugin per leggere l'archivio documenti dell'utente corrente si connette al repository dei documenti con un account privilegiato che ha accesso ai file di tutti gli utenti.
Autonomia Eccessiva: Un'applicazione o plugin basato su LLM non verifica e approva in modo indipendente azioni ad alto impatto. Ad esempio, un plugin che consente di eliminare i documenti di un utente esegue cancellazioni senza esplicita conferma da parte dell'utente.

### Strategie di Prevenzione e Mitigazione

Le seguenti azioni possono prevenire l'Eccessiva Autonomia:
Limitare i plugin/strumenti che gli agenti LLM possono utilizzare solo alle funzioni minime necessarie. Ad esempio, se un sistema basato su LLM non richiede la capacità di recuperare i contenuti di un URL, tale plugin non dovrebbe essere offerto all'agente LLM.
Limitare le funzioni implementate nei plugin/strumenti LLM al minimo necessario. Ad esempio, un plugin che accede alla casella di posta elettronica di un utente per riassumere le email potrebbe richiedere solo la capacità di leggere le email, quindi il plugin non dovrebbe contenere altre funzionalità come l'eliminazione o l'invio di messaggi.
Evitare, dove possibile, funzioni aperte (ad esempio, eseguire un comando shell, recuperare un URL, ecc.) e usare plugin/strumenti con funzionalità più granulari. Ad esempio, un'app basata su LLM potrebbe aver bisogno di scrivere alcuni output su un file. Se ciò venisse implementato utilizzando un plugin per eseguire una funzione shell, l'ambito per azioni indesiderate sarebbe molto ampio (potrebbe essere eseguito qualsiasi altro comando shell). Un'alternativa più sicura sarebbe costruire un plugin per la scrittura di file che potesse supportare solo quella specifica funzionalità.
Limitare i permessi concessi ai plugin/strumenti LLM verso altri sistemi al minimo necessario per limitare l'ambito di azioni indesiderate. Ad esempio, un agente LLM che utilizza un database di prodotti per fare raccomandazioni di acquisto a un cliente necessita solo dell'accesso in lettura alla tabella 'prodotti'; non dovrebbe avere accesso ad altre tabelle, né la capacità di inserire, aggiornare o eliminare record. Ciò dovrebbe essere assicurato applicando i permessi appropriati all'identità che il plugin LLM utilizza per connettersi al database.
Monitorare le autorizzazioni dell'utente ed il perimetro di sicurezza per garantire che le azioni intraprese per conto di un utilizzatore vengano eseguite sui sistemi a valle nel contesto previsto per quell'utente specifico e con i privilegi minimi necessari. Ad esempio, un plugin LLM che legge il repository di codice di un utente dovrebbe richiedere all'utente di autenticarsi tramite OAuth e con l'ambito minimo richiesto per lo scopo.
Utilizzare il controllo umano nel ciclo (human-in-the-loop) per richiedere l'approvazione da parte di un essere umano di tutte le azioni prima che queste vengano intraprese. Questo può essere implementato in un sistema "terzo" (al di fuori dell'ambito dell'applicazione LLM) o all'interno del plugin/strumento LLM stesso. Ad esempio, un'app basata su LLM che crea e pubblica contenuti sui social media per conto di un utente dovrebbe includere una routine che preveda l'esplicita approvazione di quest'ultimo all'interno nel plugin/strumento/API che effettua l'operazione di 'post'.
Implementare l'autorizzazione nei sistemi esterni piuttosto che lasciar decidere al modello LLM se un'azione sia consentita o meno. Quando si implementano strumenti/plugin, applicare il principio di mediazione assoluta dei flussi per assicurare che tutte le richieste fatte ai sistemi a valle tramite i plugin/strumenti vengano validate rispetto alle politiche di sicurezza.

Le seguenti opzioni non prevengono l'Eccessiva Autonomia, ma possono limitare il livello di danno causato:
Registrare e monitorare l'attività dei plugin/strumenti LLM e dei sistemi da essi contattati per identificare eventuali azioni indesiderate, e rispondere di conseguenza.
Implementare un limite di frequenza (rate-limiting) per ridurre il numero di azioni indesiderate che possono verificarsi in un dato periodo di tempo, aumentando l'opportunità di scoprire azioni indesiderate tramite il monitoraggio prima che possano verificarsi danni significativi.

### Example Attack Scenarios

An LLM-based personal assistant app is granted access to an individual’s mailbox via a plugin in order to summarise the content of incoming emails. To achieve this functionality, the email plugin requires the ability to read messages, however the plugin that the system developer has chosen to use also contains functions for sending messages. The LLM is vulnerable to an indirect prompt injection attack, whereby a maliciously-crafted incoming email tricks the LLM into commanding the email plugin to call the 'send message' function to send spam from the user's mailbox. This could be avoided by:<br><br>
(a) eliminating excessive functionality by using a plugin that only offered mail-reading capabilities, <br>
(b) eliminating excessive permissions by authenticating to the user's email service via an OAuth session with a read-only scope, and/or <br>
(c) eliminating excessive autonomy by requiring the user to manually review and hit 'send' on every mail drafted by the LLM plugin.
Alternatively, the damage caused could be reduced by implementing rate limiting on the mail-sending interface.

### Esempi di Scenari di Attacco

Un'app di assistenza personale basata su LLM ottiene l'accesso alla casella di posta elettronica di un individuo tramite un plugin per riassumere il contenuto delle email in arrivo. Per ottenere questa funzionalità, il plugin di posta elettronica richiede la capacità di leggere i messaggi, tuttavia il plugin scelto dallo sviluppatore del sistema contiene anche funzioni per inviare messaggi. L'LLM è vulnerabile a un attacco di iniezione indiretta di prompt, in cui un'email malevolamente elaborata inganna l'LLM nel comandare il plugin di posta elettronica a chiamare la funzione 'invia messaggio' per inviare spam dalla casella di posta dell'utente. Questo potrebbe essere evitato:<br><br>
(a) eliminando la funzionalità eccessiva utilizzando un plugin che offre solo capacità di lettura della posta, <br>
(b) eliminando i permessi eccessivi autenticandosi al servizio email dell'utente tramite una sessione OAuth con uno ruolo di sola lettura, e/o <br>
(c) eliminando l'autonomia eccessiva chiedendo all'utente di rivedere manualmente e premere 'invia' su ogni email redatta dal plugin LLM.
In aggiunta, il danno causato potrebbe essere ridotto implementando un limite alla frequenza di invio sull'interfaccia che spedisce la posta elettronica.

### Riferimenti e Link (Inglese)

Embrace the Red: Confused Deputy Problem: Embrace The Red
NeMo-Guardrails: Interface guidelines: NVIDIA Github
LangChain: Human-approval for tools: Langchain Documentation
Simon Willison: Dual LLM Pattern: Simon Willison
## LLM09: Eccessivo affidamento

### Descrizione

L'eccessivo affidamento si manifesta quando un LLM produce risultati erronei, ma li presenta in maniera autoritativa.
Mentre gli LLM usualmente producono materiale creativo ed informativo, questi possono anche generare contenuti fattualmente scorretti, inappropriati o pericolosi. Questo fenomeno è noto sotto il nome di allucinazione o confabulazione. Quando persone o sistemi si affidano a queste informazioni, senza supervisionarle o confermarle, si può generare un'infrazione di sicurezza, disinformazione, comunicazione errata, problemi legali, e danni reputazionali.

Codice Sorgente generato da LLM, può introdurre silenziosamente delle vulnerabilità di sicurezza. Ciò espone a rischi significativi per la salute operativa, e la sicurezza delle applicazioni. Questi rischi ricordano l'importanza di continui processi di verifica, attraverso:
Supervisione
Meccanismi di validazione continua
Note agli utilizzatori sui rischi connessi all'utilizzo

### Esempi comuni di vulnerabilità

Un LLM fornisce informazioni inaccurate come risposta, esprimendola in una maniera che la fa apparire fortemente autoritativa. L'intero sistema è disegnato senza appropriati controlli ed equilibrio per gestire questi casi e le informazioni sviano l'utente in maniera da generare potenziali danni.
Un LLM suggerisce codice insicuro o difettoso, insediando vulnerabilità quando incorporato in un sistema software senza controlli preventivi o verifiche puntuali su di esso.

### Strategie di Mitigazione e Prevenzione

Monitoraggio costante e revisione degli output dell'LLM. Utilizzo di tecniche rivolte all'auto-consistenza o le tecniche di voto per filtrare testo inconsistente. La comparazione delle diverse risposte del modello per un singolo prompt può portare ad un miglior giudizio della qualità e della consistenza degli output.
Controlli incrociati sul modello rispetto a fonti esterne certificate. Questo livello aggiuntivo di validazione può aiutare ad assicurare che le informazioni prodotte dal modello siano accurate e affidabili.
Migliorare il modello con metodi di taratura fine (fine-tuning) o incorporazione (embedding) per migliorare la qualità degli output. Modelli generici pre-addestrati possono generare informazioni inaccurate con maggiore probabilità rispetto a modelli addestrati su un dominio specifico. Tecniche come l'ingegnerizzazione dei prompt, ottimizzazione efficiente dei parametri (PET), Ottimizzazione dell'intero modello, e prompting basato su catena di pensiero (chain of thoughts prompting) possono essere impiegati allo scopo.
Implementazione di meccanismi di validazione automatica che possono effettuare controlli comparativi sugli output generati, rispetto a fatti o dati ben noti. Questo può fornire un livello di sicurezza aggiuntiva e mitigare i rischi associati alle allucinazioni.
Suddivisione di compiti complessi in singole azioni parziali più gestibili, ed assegnazione ad agenti specializzati. Questo non solo aiuta a gestire la complessità, ma anche a ridurre le probabilità di allucinazione essendo ogni agente responsabile di obiettivi più gestibili.
Comunicare chiaramente i rischi e le limitazioni associate con l'utilizzo degli LLM. Ciò include potenziale inaccuratezza delle informazioni, ed altri rischi. Una chiara comunicazione dei rischi prepare gli utenti a potenziali problemi e aiutarli a prendere decisioni informate.
Costruire API ed interfacce utente che incoraggino un utilizzo responsabile degli LLM. Questo include misure come filtri di contenuti, notifiche all'utente di possibile inaccuratezza e chiara marcatura dei materiali generati dall'AI.
Quando si utilizzano LLM in ambienti di sviluppo, vanno stabiliti criteri di codifica sicura e linee guida che prevengano l'inclusione di possibili vulnerabilità. 

### Esempi di Scenari D'Attacco

Una testata giornalistica utilizza pesantemente un LLM per generare i propri articoli e notizie. Un malintenzionato può approfitteìare di questa eccessiva dipendenza, iniettando nel LLM informazioni fuorvianti, che favoriscano la diffusione di notizie false o mirate.
L'intelligenza artificiale plagia contenuti anche se non intenzionalmente, portando a problemi di proprietà intellettuale che minano la credibilità dell'organizzazione.
Un team di sviluppo software utilizza un LLM per accelerare il processo di codifica. Un'eccessiva dipendenza dai suggerimenti dell'AI introduce vulnerabilità nelle applicazioni generate a causa di parametri di default non modificati o raccomandazioni inconsistenti con le pratiche di sviluppo sicuro.
Un'azienda che si occupa di sviluppo software utilizza un LLM per fornire assistenza agli sviluppatori. Il modello suggerisce una libreria o un pacchetto inesistenti e uno sviluppatore, affidandosi all'AI, integra senza saperlo un pacchetto malevolo nel software venduto dall'azienda. Questo esempio sottolinea l'importanza dei controlli incrociati sui suggerimenti del modello, in particolare quando questi si riferiscono a codice o librerie di terze parti.

### Link e Riferimenti (Inglese)

Understanding LLM Hallucinations: Towards Data Science
How Should Companies Communicate the Risks of Large Language Models to Users?: Techpolicy
A news site used AI to write articles. It was a journalistic disaster: Washington Post
AI Hallucinations: Package Risk: Vulcan.io
How to Reduce the Hallucinations from Large Language Models: The New Stack
Practical Steps to Reduce Hallucination: Victor Debia
## LLM10: Furto del Modello

### Descrizione

Questa voce si riferisce all'accesso non autorizzato e all'esfiltrazione di modelli LLM da parte di attori malintenzionati o Gruppi A.P.T. (Advanced Persistent Threat). Ciò si verifica quando i modelli LLM proprietari (rappresentando una proprietà intellettuale di valore) vengono compromessi, rubati fisicamente, copiati o se ne estraggono pesi e parametri per creare un equivalente funzionale. L'impatto del furto di modelli LLM può includere perdite economiche e di reputazione del marchio, erosione del vantaggio competitivo, uso non autorizzato del modello o accesso non autorizzato a informazioni sensibili contenute nel modello.

Il furto di un LLM rappresenta una preoccupante questione di sicurezza, divenendo i modelli linguistici sempre più potenti e diffusi. Organizzazioni e ricercatori devono dare priorità a misure di protezione adeguate volte a proteggere i loro modelli LLM, garantendo la riservatezza e l'integrità della loro proprietà intellettuale. Per mitigare i rischi associati al furto del modello LLM e salvaguardare gli interessi di individui e organizzazioni che ne fanno uso, è cruciale adottare un sistema di sicurezza completo (es. sistema di gestione della sicurezza delle informazioni o altre pratiche equivalenti) che includa controlli di accesso, crittografia e monitoraggio continuo.```

### Esempi Comuni di Vulnerabilità

Un aggressore sfrutta una vulnerabilità nell'infrastruttura di un'azienda per accedere senza autorizzazione al loro archivio (repository) di modelli LLM grazie a configurazioni errate nella sicurezza della rete o delle applicazioni.
Uno scenario di minaccia interna in cui un dipendente insoddisfatto divulga modelli o artefatti correlati ai modelli.
Un attaccante interroga l'API del modello, utilizzando input meticolosamente elaborati e tecniche di iniezione di prompt (comandi e parametri da linea di comando), per raccogliere un numero sufficiente di output (risposte del modello) utilizzandoli per creare successivamente un modello ombra (shadow model).
Un attaccante malintenzionato riesce a eludere le tecniche di filtraggio degli input del LLM per effettuare un attacco laterale (side-channell) e dunque a raccogliere informazioni sui pesi e sull'architettura del modello, per trasferirli a una risorsa remota.
Il vettore d'attacco per l'estrazione del modello implica l'interrogazione dell'LLM con un gran numero di prompt, su un argomento specifico. Gli output dell'LLM possono a quel punto essere utilizzati per affinare un altro modello. In ogni caso, ci sono alcune considerazioni da fare su questo attacco:
L'aggressore deve generare un gran numero di prompt mirati. Se i prompt non sono abbastanza specifici, gli output dell'LLM risulteranno inutili.
Gli output degli LLM possono talvolta contenere risposte considerate "allucinazioni", il che significa che l'aggressore potrebbe non essere in grado di estrarre l'intero modello, poiché alcuni output possono emergere come insensati.
Non è possibile replicare un LLM al 100% tramite questo metodo di estrazione. Tuttavia l'aggressore sarà in grado di replicare un modello parziale.
Il vettore di attacco per una _replica funzionale del modello_ implica l'uso del modello target tramite prompt volti a generare dati di addestramento sintetici (un approccio chiamato "auto-istruzione"), da utilizzare in seguito per affinare un altro modello fondamentale (foundational model) in modo da produrre un equivalente funzionale del modello target. Questa tecnica aggira le limitazioni dell'estrazione tradizionale basata su query, illustrata nell'esempio precedente (5), ed è stata utilizzata con successo nella ricerca sull'uso di un LLM per addestrare un altro LLM. Anche se nel contesto della ricerca la replica del modello non rappresenta un attacco, lo stesso approccio potrebbe essere utilizzato da un aggressore per replicare un modello proprietario con API pubblica.

L'uso di un modello rubato, come un modello ombra (shadow model), può essere finalizzato ad orchestrare attacchi informatici, incluso l'accesso deferito non autorizzato a informazioni sensibili contenute nel modello stesso, o la facoltà di sperimentare su di esso in modo non rilevabile, con input avversi, per predisporre ulteriori iniezioni di prompt (prompt injections) più mirate.

### Strategie di Prevenzione e Mitigazione

Implementare controlli di accesso robusti (ad esempio, RBAC e minimizzazopne dei privilegi) e meccanismi di autenticazione forti per limitare l'accesso non autorizzato ai repository di modelli LLM e agli ambienti di arricchimento e input (pre-training e training).
Questo è particolarmente vero per i primi tre casi che più comunemente potrebbero causare questa vulnerabilità quali minacce interne (insider threat), configurazione errata e/o controlli di sicurezza deboli, relativi all'infrastruttura che ospita modelli, pesi e architettura dell'LLM, in cui un attore malintenzionato potrebbe infiltrarsi dall'interno, o dall'esterno.
La gestione dei fornitori, il controllo, la verifica e il controllo del livello di dipendenza da essi sono elementi importanti di attenzione per prevenire gli abusi ed attacchi diretti sulla catena di fornitura.
Limitare l'accesso dell'LLM alle risorse di rete, ai servizi interni e alle API.
Questa pratica è efficace per tutti gli esempi di attacchi comuni, fornendo copertura dai rischi e dalle minacce interne (insider threats), e limitando allo stesso tempo ciò a cui l'applicazione LLM "_ha accesso_", rappresentando dunque un meccanismo o metodo preventivo per prevenire o interrompere attacchi laterali (side-channel attacks).
Utilizzare un Inventario o Registro centralizzato per i modelli di Machine Learning utilizzati in produzione. Avere un registro di modelli centralizzato impedisce l'accesso non autorizzato ai modelli di ML tramite controlli di accesso, autenticazione e grazie alla capacità di monitoraggio/registrazione, elementi fondamentali per la governance di questi processi. Avere un repository centralizzato è inoltre vantaggioso per raccogliere dati sugli algoritmi utilizzati dai modelli ai fini di conformità, valutazione dei rischi e loro mitigazione.
Monitorare e verificare regolarmente i registri (log) di accesso e le attività relative agli archivi dei modelli LLM, per rilevare e rispondere tempestivamente a qualsiasi comportamento sospetto o non autorizzato.
Automatizzare la distribuzion delle cosiddette MLOps (Gestione Operativa dei Modelli di Machine Learning) attraverso flussi di lavoro per la governance, il tracciamento e l'approvazione, per rafforzare i controlli di accesso e rilascio all'interno dell'infrastruttura.
Implementare controlli e strategie di mitigazione per ridurre e|o contenere il rischio di attacchi indiretti (side channel) causati da tecniche di iniezione di prompt (prompt injection).
Limitare la frequenza delle chiamate API dove applicabile e/o utilizzare filtri per ridurre il rischio di esfiltrazione dati dalle applicazioni LLM, o implementare tecniche (ad es. sistemi di Data Loss Prevention) per rilevare attività di estrazione anche da altre fonti.
Implementare un addestramento avversariale mirato alla resilienza per aiutare a rilevare query di estrazione e rafforzare le misure di sicurezza fisica.
Implementare un framework di marcatura modale e/o temporale (watermarking) nelle fasi di integrazione (input) e monitoraggio (output, trasformazione), parte del ciclo di vita di un LLM.

### Esempi di Scenario di Attacco

Un attaccante abusa una vulnerabilità nell'infrastruttura di un'azienda per accedere senza autorizzazione al loro repository di modelli LLM. L'attaccante procede quindi all'esfiltrazione di modelli LLM di valore e li utilizza per lanciare un servizio concorrente di elaborazione del linguaggio o estrarre forzatamente informazioni sensibili, causando gravi danni finanziari all'azienda proprietaria del modello.
Un dipendente insoddisfatto divulga modelli o artefatti correlati. L'esposizione pubblica che questo scenario rappresenta aumenta la conoscenza a disposizione di possibili attaccanti, consentendo attacchi avversariali di tipo "gray box" (conoscenza parziale) o, in alternativa, consente di rubare direttamente la proprietà intellettuale esposta.
Un attaccante interroga l'API con input accuratamente selezionati e raccoglie un numero sufficiente di output per creare un modello ombra (shadow).
Una mancanza nei controlli di sicurezza della catena di fornitura (supply chain) porta a perdite di dati relativi a informazioni proprietarie del o sul modello.
Un attaccante malintenzionato elude le tecniche di filtraggio degli input e le istruzioni iniziali dell'LLM, per eseguire un attacco indiretto/laterale e recuperare informazioni sul modello caricandole su una risorsa remota sotto il suo controllo.

### Link e Riferimenti (Inglese)

Meta’s powerful AI language model has leaked online: The Verge
Runaway LLaMA | How Meta's LLaMA NLP model leaked: Deep Learning Blog
AML.TA0000 ML Model Access: MITRE ATLAS
I Know What You See: Arxiv White Paper
D-DAE: Defense-Penetrating Model Extraction Attacks: Computer.org
A Comprehensive Defense Framework Against Model Extraction Attacks: IEEE
Alpaca: A Strong, Replicable Instruction-Following Model: Stanford Center on Research for Foundation Models (CRFM)
How Watermarking Can Help Mitigate The Potential Risks Of LLMs?: KD Nuggets

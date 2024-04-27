## Introducción

El frenesí de interés en los Modelos de Lenguaje de Gran Escala (LLMs) tras el lanzamiento de chatbots pre-entrenados para el mercado masivo a finales de 2022 ha sido notable. Las empresas, ansiosas por aprovechar el potencial de los LLMs, los están integrando rápidamente en sus operaciones y ofertas orientadas al cliente. Sin embargo, la velocidad vertiginosa con la que se están adoptando los LLMs ha superado el establecimiento de protocolos de seguridad integrales, dejando muchas aplicaciones vulnerables a problemas de alto riesgo.

La ausencia de un recurso unificado que aborde estas preocupaciones de seguridad en los LLMs era evidente. Los desarrolladores, no familiarizados con los riesgos específicos asociados con los LLMs, se encontraban con recursos dispersos y la misión de OWASP parecía encajar perfectamente para ayudar a impulsar una adopción más segura de esta tecnología.

### ¿A quién va dirigido?
Nuestra audiencia principal son los desarrolladores, científicos de datos y expertos en seguridad encargados de diseñar y construir aplicaciones y complementos que aprovechan las tecnologías LLM. Nuestro objetivo es proporcionar orientación de seguridad práctica, accionable y concisa para ayudar a estos profesionales a navegar por el terreno complejo y en constante evolución de la seguridad de las aplicaciones LLM.

### La Creación de la Lista
Crear la lista OWASP Top 10 para Aplicaciones LLM fue una tarea significativa, construida sobre la experiencia colectiva de un equipo internacional de casi 500 expertos con más de 125 colaboradores activos. Nuestros colaboradores provienen de diversos antecedentes, incluyendo empresas de IA, empresas de seguridad, ISVs, hiperescaladores en la nube, proveedores de hardware y el ámbito académico.

Durante un mes, realizamos lluvias de ideas y propusimos vulnerabilidades potenciales, con miembros del equipo redactando 43 amenazas distintas. A través de múltiples rondas de votación, refinamos estas propuestas a una lista concisa de las diez vulnerabilidades más críticas. Subequipos dedicados examinaron cada vulnerabilidad y la sometieron a revisión pública, asegurando la lista final más completa y accionable.

Cada una de estas vulnerabilidades, junto con ejemplos, consejos de prevención, escenarios de ataque y referencias, fue además escudriñada y refinada por subequipos dedicados y sometida a revisión pública, asegurando la lista final más completa y accionable.

### Relación con otras Listas OWASP Top 10
Aunque nuestra lista comparte ADN con tipos de vulnerabilidades encontradas en otras listas OWASP Top 10, no nos limitamos a reiterar estas vulnerabilidades. En su lugar, profundizamos en las implicaciones únicas que estas vulnerabilidades tienen cuando se encuentran en aplicaciones que utilizan LLMs.

Nuestro objetivo es cerrar la brecha entre los principios generales de seguridad de aplicaciones y los desafíos específicos que plantean los LLMs. Esto incluye explorar cómo las vulnerabilidades convencionales pueden plantear diferentes riesgos o podrían ser explotadas de maneras novedosas dentro de los LLMs, así como cómo las estrategias de remediación tradicionales deben adaptarse para aplicaciones que utilizan LLMs.

### Acerca de la Versión 1.1
Aunque nuestra lista comparte ADN con tipos de vulnerabilidades encontradas en otras listas OWASP Top 10, no nos limitamos a reiterar estas vulnerabilidades. En cambio, profundizamos en las implicaciones únicas de estas vulnerabilidades cuando se encuentran en aplicaciones que utilizan LLMs. Nuestro objetivo es cerrar la brecha entre los principios generales de seguridad de aplicaciones y los desafíos específicos que plantean los LLMs.

Los objetivos del grupo incluyen explorar cómo las vulnerabilidades convencionales pueden plantear diferentes riesgos o ser explotadas de maneras novedosas dentro de los LLMs y cómo los desarrolladores deben adaptar las estrategias tradicionales de remediación para aplicaciones que utilizan LLMs.

### El Futuro
La versión 1.1 de la lista no será la última. Esperamos actualizarla periódicamente para mantener el ritmo con el estado de la industria. Trabajaremos con la comunidad más amplia para impulsar el estado del arte y crear más materiales educativos para una variedad de usos. También buscamos colaborar con organismos de normalización y gobiernos en temas de seguridad de IA. Te invitamos a unirte a nuestro grupo y contribuir.

#### Steve Wilson
Project Lead, OWASP Top 10 for LLM Applications
https://www.linkedin.com/in/wilsonsd    
Twitter/X: @virtualsteve

#### Ads Dawson
v1.1 Release Lead & Vulnerability Entries Lead, OWASP Top 10 for LLM Applications
https://www.linkedin.com/in/adamdawson0 
GitHub: @GangGreenTemperTatum

## OWASP Top 10 for Large Language Model Applications

### LLM01: Inyección de Prompt
Las entradas astutas pueden manipular un Modelo de Lenguaje de Gran Escala, causando acciones no intencionadas. Las inyecciones directas sobrescriben los prompts del sistema, mientras que las indirectas manipulan entradas de fuentes externas.

### LLM02: Manejo Inseguro de Salidas
Esta vulnerabilidad ocurre cuando una salida del LLM se acepta sin escrutinio, exponiendo sistemas de backend. El mal uso puede llevar a consecuencias graves como XSS, CSRF, SSRF, escalada de privilegios o ejecución remota de código.

### LLM03: Envenenamiento de los Datos de Entrenamiento
Esto ocurre cuando los datos de entrenamiento de un LLM son manipulados, introduciendo vulnerabilidades o sesgos que comprometen la seguridad, la efectividad o el comportamiento ético. Las fuentes incluyen Common Crawl, WebText, OpenWebText y libros.

### LLM04: Denegación de Servicio en Modelos
Los atacantes provocan operaciones que consumen muchos recursos en Modelos de Lenguaje de Gran Escala, llevando a la degradación del servicio o altos costos. La vulnerabilidad se magnifica debido a la naturaleza intensiva en recursos de los LLM y la imprevisibilidad de las entradas de los usuarios.

### LLM05: Vulnerabilidades en la Cadena de Suministro
El ciclo de vida de la aplicación LLM puede verse comprometido por componentes o servicios vulnerables, llevando a ataques de seguridad. Usar conjuntos de datos de terceros, modelos preentrenados y plugins puede añadir vulnerabilidades.

### LLM06: Divulgación de Información Sensible
Los LLM pueden revelar datos confidenciales en sus respuestas, llevando a acceso no autorizado a datos, violaciones de privacidad y brechas de seguridad. Es crucial implementar la sanitización de datos y políticas estrictas de usuarios para mitigar esto.

### LLM07: Diseño Inseguro de Plugin
Los plugins de LLM pueden tener entradas inseguras y control de acceso insuficiente. Esta falta de control de la aplicación los hace más fáciles de explotar y puede resultar en consecuencias como la ejecución remota de código.

### LLM08: Responsabilidad Excesiva
Los sistemas basados en LLM pueden emprender acciones que llevan a consecuencias no intencionadas. El problema surge de la funcionalidad excesiva, permisos o autonomía otorgados a los sistemas basados en LLM.

### LLM09: Sobredependencia
Sistemas o personas que dependen excesivamente de los LLM sin supervisión pueden enfrentarse a desinformación, malentendidos, problemas legales y vulnerabilidades de seguridad debido a contenido incorrecto o inapropiado generado por LLM.

### LLM10: Robo de Modelo
Esto implica el acceso no autorizado, copia o exfiltración de modelos LLM propietarios. El impacto incluye pérdidas económicas, ventaja competitiva comprometida y acceso potencial a información sensible.
## LLM01: Inyección de Prompt

### Descripción

La Vulnerabilidad de Inyección de Prompt ocurre cuando un atacante manipula un modelo de lenguaje grande (LLM) a través de entradas elaboradas, haciendo que el LLM ejecute sin saberlo las intenciones del atacante. Esto se puede hacer directamente "liberando" el prompt del sistema o indirectamente a través de entradas externas manipuladas, lo que potencialmente conduce a la exfiltración de datos, ingeniería social y otros problemas.

Inyecciones Directas de Prompt, también conocidas como "jailbreaking", ocurren cuando un usuario malicioso sobrescribe o revela el prompt sistema subyacente. Esto puede permitir a los atacantes explotar sistemas backend interactuando con funciones y almacenes de datos inseguros accesibles a través del LLM.
Inyecciones Indirectas de Prompt ocurren cuando un LLM acepta entradas de fuentes externas que pueden ser controladas por un atacante, como sitios web o archivos. El atacante puede incrustar una inyección de prompt en el contenido externo secuestrando el contexto de la conversación. Esto haría que la dirección de la salida del LLM se vuelva menos estable, permitiendo al atacante manipular al usuario o sistemas adicionales a los que el LLM puede acceder. Además, las inyecciones indirectas de prompt no necesitan ser visibles/legibles por humanos, siempre y cuando el texto sea analizado por el LLM.

Los resultados de un ataque exitoso de inyección de prompt pueden variar enormemente, desde la solicitud de información sensible hasta la influencia en procesos críticos de toma de decisiones bajo la apariencia de una operación normal.

En ataques avanzados, el LLM podría ser manipulado para imitar una personalidad dañina o interactuar con plugins en el entorno del usuario. Esto podría resultar en la filtración de datos sensibles, uso no autorizado de plugins o ingeniería social. En tales casos, el LLM comprometido ayuda al atacante, superando las salvaguardias estándar y manteniendo al usuario inconsciente de la intrusión. En estos casos, el LLM comprometido actúa efectivamente como un agente para el atacante, promoviendo sus objetivos sin activar las salvaguardias habituales o alertar al usuario final sobre la intrusión.

### Ejemplos Comunes de Vulnerabilidad

Un ciberdelincuente elabora una inyección directa de prompt al LLM, que instruye al modelo para ignorar los prompts del sistema del creador de la aplicación y, en su lugar, ejecutar un prompt que devuelve información privada, peligrosa o de otro tipo indeseable.
Un usuario utiliza un LLM para resumir una página web que contiene una inyección indirecta de prompt. Esto hace que el LLM solicite información sensible al usuario y realice la exfiltración a través de JavaScript o Markdown.
Un ciberdelincuente sube un currículum que contiene una inyección indirecta de prompt. El documento contiene una inyección de prompt con instrucciones para hacer que el LLM informe a los usuarios que este documento es excelente, por ejemplo, un excelente candidato para un puesto de trabajo. Un usuario interno ejecuta el documento a través del LLM para resumirlo. La salida del LLM indica que este es un excelente documento.
Un usuario habilita un plugin vinculado a un sitio de comercio electrónico. Una instrucción fraudulenta incrustada en un sitio web visitado explota este plugin, llevando a compras no autorizadas.
Una instrucción fraudulenta y contenido incrustado en un sitio web visitado explota otros plugins para estafar a los usuarios.

### Estrategias de Prevención y Mitigación

Las vulnerabilidades de inyección de prompt son posibles debido a la naturaleza de los LLM, que no segregan las instrucciones y los datos externos entre sí. Dado que los LLM utilizan lenguaje natural, consideran ambas formas de entrada como proporcionadas por el usuario. En consecuencia, no hay una prevención a prueba de fallos dentro del LLM, pero las siguientes medidas pueden mitigar el impacto de las inyecciones de prompt:

Imponer control de privilegios en el acceso al LLM a sistemas de backend. Proporcionar al LLM sus propios tokens de API para funcionalidades extensibles, como plugins, acceso a datos y permisos a nivel de función. Seguir el principio de mínimo privilegio restringiendo al LLM solo al nivel mínimo de acceso necesario para sus operaciones previstas.
Añadir un humano en el bucle para funcionalidades extendidas. Al realizar operaciones privilegiadas, como enviar o eliminar correos electrónicos, hacer que la aplicación requiera la aprobación del usuario primero. Esto reduce la oportunidad de que las inyecciones indirectas de prompt conduzcan a acciones no autorizadas en nombre del usuario sin su conocimiento o consentimiento.
Segregar el contenido externo de los prompts del usuario. Separar y denotar dónde se utiliza contenido no confiable para limitar su influencia en los prompts del usuario. Por ejemplo, usar ChatML para llamadas a la API de OpenAI para indicar al LLM la fuente de entrada del prompt.
Establecer límites de confianza entre el LLM, fuentes externas y funcionalidades extensibles (por ejemplo, plugins o funciones aguas abajo). Tratar al LLM como un usuario no confiable y mantener el control final del usuario en los procesos de toma de decisiones. Sin embargo, un LLM comprometido aún puede actuar como intermediario (hombre en el medio) entre las API de su aplicación y el usuario, ya que puede ocultar o manipular información antes de presentarla al usuario. Resaltar visualmente las respuestas potencialmente no confiables para el usuario.
Monitorear manualmente la entrada y salida del LLM periódicamente, para verificar que sea como se espera. Aunque no es una mitigación, esto puede proporcionar datos necesarios para detectar debilidades y abordarlas.

### Ejemplos de Escenarios de Ataque

Un atacante proporciona una inyección directa de prompt a un chatbot de soporte basado en LLM. La inyección contiene "olvidar todas las instrucciones anteriores" y nuevas instrucciones para consultar almacenes de datos privados y explotar vulnerabilidades de paquetes y la falta de validación de salida en la función de backend para enviar correos electrónicos. Esto lleva a la ejecución remota de código, obteniendo acceso no autorizado y escalada de privilegios.
Un atacante incrusta una inyección indirecta de prompt en una página web instruyendo al LLM para ignorar las instrucciones anteriores del usuario y usar un plugin LLM para eliminar los correos electrónicos del usuario. Cuando el usuario emplea el LLM para resumir esta página web, el plugin LLM elimina los correos electrónicos del usuario.
Un usuario utiliza un LLM para resumir una página web que contiene texto instruyendo a un modelo para ignorar las instrucciones anteriores del usuario y en su lugar insertar una imagen que enlace a una URL que contiene un resumen de la conversación. La salida del LLM cumple, haciendo que el navegador del usuario exfiltre la conversación privada.
Un usuario malicioso sube un currículum con una inyección de prompt. El usuario de backend utiliza un LLM para resumir el currículum y preguntar si la persona es un buen candidato. Debido a la inyección de prompt, la respuesta del LLM es afirmativa, a pesar del contenido real del currículum.
Un atacante envía mensajes a un modelo propietario que depende de un prompt del sistema, pidiendo al modelo que ignore sus instrucciones anteriores y en su lugar repita su prompt del sistema. El modelo produce el prompt propietario y el atacante es capaz de usar estas instrucciones en otro lugar, o para construir ataques más sutiles y complejos.

### Enlaces de Referencia

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
## LLM02: Manejo Inseguro de Salidas

### Descripción

El Manejo Inseguro de Salidas se refiere específicamente a la validación, sanitización y manejo insuficientes de las salidas generadas por modelos de lenguaje grandes antes de que sean pasadas a otros componentes y sistemas aguas abajo. Dado que el contenido generado por LLM puede ser controlado por entradas de prompt, este comportamiento es similar a proporcionar a los usuarios acceso indirecto a funcionalidades adicionales.

El Manejo Inseguro de Salidas difiere de la Sobredependencia en que se ocupa de las salidas generadas por LLM antes de que sean pasadas aguas abajo, mientras que la Sobredependencia se centra en preocupaciones más amplias en torno a la dependencia excesiva de la precisión y la adecuación de las salidas de LLM.

La explotación exitosa de una vulnerabilidad de Manejo Inseguro de Salidas puede resultar en XSS y CSRF en navegadores web, así como SSRF, escalada de privilegios o ejecución remota de código en sistemas de backend.

Las siguientes condiciones pueden aumentar el impacto de esta vulnerabilidad:
La aplicación otorga al LLM privilegios más allá de lo que se pretende para los usuarios finales, lo que permite la escalada de privilegios o la ejecución remota de código.
La aplicación es vulnerable a ataques indirectos de inyección de prompts, lo que podría permitir a un atacante obtener acceso privilegiado al entorno de un usuario objetivo.
Los plugins de terceros no validan adecuadamente las entradas.

### Ejemplos Comunes de Vulnerabilidad

La salida del LLM se introduce directamente en un shell del sistema o en una función similar como exec o eval, lo que resulta en la ejecución remota de código.
JavaScript o Markdown es generado por el LLM y devuelto a un usuario. El código es entonces interpretado por el navegador, resultando en un ataque de tipo XSS (Cross-Site-Scripting).

### Estrategias de Prevención y Mitigación

Tratar el modelo como cualquier otro usuario, adoptando un enfoque de cero confianza y aplicando una validación de entrada adecuada en las respuestas provenientes del modelo para funciones de backend.
Seguir las pautas de OWASP ASVS (Estándar de Verificación de Seguridad de Aplicaciones) para garantizar una validación de entrada y una sanitización efectivas.
Codificar la salida del modelo de vuelta a los usuarios para mitigar la ejecución de código no deseado por JavaScript o Markdown. OWASP ASVS proporciona una guía detallada sobre la codificación de salidas.

### Ejemplos de Escenarios de Ataque

Una aplicación utiliza un plugin LLM para generar respuestas para una función de chatbot. El plugin también ofrece una serie de funciones administrativas accesibles a otro LLM privilegiado. El LLM de propósito general pasa directamente su respuesta, sin una validación de salida adecuada, al plugin, causando que el plugin se cierre para mantenimiento.
Un usuario utiliza una herramienta de resumen de sitios web impulsada por un LLM para generar un resumen conciso de un artículo. El sitio web incluye una inyección de prompt instruyendo al LLM para capturar contenido sensible ya sea del sitio web o de la conversación del usuario. Desde allí, el LLM puede codificar los datos sensibles y enviarlos, sin ninguna validación o filtrado de salida, a un servidor controlado por el atacante.
Un LLM permite a los usuarios elaborar consultas SQL para una base de datos backend a través de una función similar a un chat. Un usuario solicita una consulta para eliminar todas las tablas de la base de datos. Si la consulta elaborada por el LLM no se escudriña, entonces todas las tablas de la base de datos serán eliminadas.
Una aplicación web utiliza un LLM para generar contenido a partir de prompts de texto del usuario sin sanitización de salida. Un atacante podría enviar un prompt diseñado para que el LLM devuelva un payload de JavaScript no sanitizado, lo que lleva a un ataque XSS cuando se renderiza en el navegador de una víctima. La insuficiente validación de prompts habilitó este ataque.

### Enlaces de Referencia

Arbitrary Code Execution: Snyk Security Blog
ChatGPT Plugin Exploit Explained: From Prompt Injection to Accessing Private Data: Embrace The Red
New prompt injection attack on ChatGPT web version. Markdown images can steal your chat data.: System Weakness
Don’t blindly trust LLM responses. Threats to chatbots: Embrace The Red
Threat Modeling LLM Applications: AI Village
OWASP ASVS - 5 Validation, Sanitization and Encoding: OWASP AASVS
## LLM03: Envenenamiento de los Datos de Entrenamiento

### Descripción

El punto de partida de cualquier enfoque de aprendizaje automático son los datos de entrenamiento, simplemente "texto en bruto". Para ser altamente capaz (por ejemplo, tener conocimiento lingüístico y del mundo), este texto debe abarcar una amplia gama de dominios, géneros e idiomas. Un modelo de lenguaje grande utiliza redes neuronales profundas para generar salidas basadas en patrones aprendidos de los datos de entrenamiento.

El envenenamiento de los datos de entrenamiento se refiere a la manipulación de los datos previos al entrenamiento o datos involucrados en los procesos de fine-tuning o incrustación para introducir vulnerabilidades (que tienen vectores de ataque únicos y a veces compartidos), puertas traseras o sesgos que podrían comprometer la seguridad, efectividad o comportamiento ético del modelo. La información envenenada puede ser mostrada a los usuarios o crear otros riesgos como degradación del rendimiento, explotación del software subyacente y daño a la reputación. Incluso si los usuarios desconfían de la salida problemática de la IA, los riesgos permanecen, incluyendo capacidades de modelo deterioradas y daño potencial a la reputación de la marca.

Datos previos al entrenamiento se refiere al proceso de entrenar un modelo basado en una tarea o conjunto de los datos.
El fine-tuning implica tomar un modelo existente que ya ha sido entrenado y adaptarlo a un tema más estrecho o a un objetivo más enfocado entrenándolo con un conjunto de los datos curado. Este conjunto de los datos generalmente incluye ejemplos de entradas y salidas deseadas correspondientes.
El proceso de incrustación es el proceso de convertir datos categóricos (a menudo texto) en una representación numérica que se puede usar para entrenar un modelo de lenguaje. El proceso de incrustación implica representar palabras o frases de los datos de texto como vectores en un espacio vectorial continuo. Los vectores se generan típicamente alimentando los datos de texto en una red neuronal que ha sido entrenada en un gran corpus de texto.

El envenenamiento de los datos se considera un ataque a la integridad porque la manipulación de los datos de entrenamiento impacta la capacidad del modelo para generar predicciones correctas. Naturalmente, las fuentes de los datos externas presentan un riesgo mayor ya que los creadores del modelo no tienen control sobre los datos ni un alto nivel de confianza de que el contenido no contenga sesgos, información falsificada o contenido inapropiado.

### Ejemplos Comunes de Vulnerabilidad

Un actor malicioso o una marca competidora crea intencionalmente documentos inexactos o maliciosos dirigidos a los datos de pre-entrenamiento, fine-tuning o incrustaciones de un modelo. Considere ambos vectores de ataque Envenenamiento de los Datos de Vista Dividida y Envenenamiento de los Datos Frontrunning para ilustraciones.
El modelo víctima se entrena usando información falsificada, lo que se refleja en las salidas de los prompts de IA generativa a sus consumidores.
Un actor malicioso logra inyectar directamente contenido falsificado, sesgado o dañino en los procesos de entrenamiento de un modelo, que se devuelve en salidas posteriores.
Un usuario desprevenido está inyectando indirectamente datos sensibles o propietarios en los procesos de entrenamiento de un modelo, que se devuelve en salidas posteriores.
Un modelo se entrena utilizando datos que no han sido verificados por su fuente, origen o contenido en ninguno de los ejemplos de etapa de entrenamiento, lo que puede llevar a resultados erróneos si los datos están contaminados o son incorrectos.
El acceso no restringido a la infraestructura o el sandboxing inadecuado puede permitir que un modelo ingiera datos de entrenamiento inseguros, lo que resulta en salidas sesgadas o dañinas. Este ejemplo también está presente en cualquiera de los ejemplos de etapa de entrenamiento.
En este escenario, la entrada de un usuario al modelo puede reflejarse en la salida a otro usuario (lo que lleva a una violación), o el usuario de un LLM puede recibir salidas del modelo que son inexactas, irrelevantes o dañinas dependiendo del tipo de los datos ingeridos en comparación con el caso de uso del modelo (generalmente reflejado con una tarjeta de modelo).

Tanto si es un desarrollador, cliente o consumidor general del LLM, es importante entender las implicaciones de cómo esta vulnerabilidad podría reflejar riesgos dentro de su aplicación LLM al interactuar con un LLM no propietario para entender la legitimidad de las salidas del modelo basadas en sus procedimientos de entrenamiento. De manera similar, los desarrolladores del LLM pueden estar en riesgo tanto de ataques directos como indirectos sobre datos internos o de terceros utilizados para el fine-tuning y la incrustación (lo más común), lo que como resultado crea un riesgo para todos sus consumidores


### Estrategias de Prevención y Mitigación

Verificar la cadena de suministro de los datos de entrenamiento, especialmente cuando se obtienen de fuentes externas, así como mantener atestaciones a través de la metodología "ML-BOM" (Bill of Materials de Aprendizaje Automático) y verificar las tarjetas de modelo.
Verificar la legitimidad correcta de las fuentes de los datos específicas y los datos contenidos obtenidos durante las etapas de pre-entrenamiento, fine-tuning y incrustación.
Verificar su caso de uso para el LLM y la aplicación con la que se integrará. Crear diferentes modelos a través de los datos de entrenamiento separados o fine-tuning para diferentes casos de uso para crear una salida de IA generativa más granular y precisa según su caso de uso definido.
Asegurar un sandboxing suficiente a través de controles de red para evitar que el modelo raspe fuentes de los datos no deseadas que podrían obstaculizar la salida del aprendizaje automático.
Utilizar filtros estrictos de selección o de entrada para datos de entrenamiento específicos o categorías de fuentes de los datos para controlar el volumen de los datos falsificados. Sanitización de los datos, con técnicas como la detección de anomalías estadísticas y métodos de detección de anomalías para detectar y eliminar datos adversarios de ser alimentados potencialmente en el proceso de fine-tuning.
Elaborar preguntas de control sobre la fuente y propiedad de los conjuntos de los datos para asegurar que el modelo no haya sido envenenado, y adoptar esta cultura en el ciclo de "MLSecOps". Consultar recursos disponibles como El Índice de Transparencia de Modelos Fundamentales o Tabla de Clasificación de LLM Abiertos como ejemplo.
Utilizar DVC (Control de Versiones de los Datos) para identificar y rastrear con precisión la parte de un conjunto de los datos que puede haber sido manipulada, eliminada o añadida y que ha llevado al envenenamiento.
Utilizar Base de los Datos Vectorial para añadir información suministrada por el usuario en ayuda para proteger de envenenar a otros usuarios e incluso arreglar en producción sin tener que entrenar un nuevo modelo.
Técnicas de robustez adversaria como el aprendizaje federado y restricciones para minimizar el efecto de valores atípicos o entrenamiento adversario para ser vigoroso contra las peores perturbaciones de los datos de entrenamiento.
Un enfoque de "MLSecOps" podría ser incluir la robustez adversaria en el ciclo de vida de entrenamiento con la técnica de auto envenenamiento.
Un repositorio de ejemplo de esto sería AutoPoison para pruebas, incluyendo ataques como Inyecciones de Contenido (“intentando promover una marca en las respuestas del modelo”) y Ataques de Rechazo (“haciendo que el modelo siempre se niegue a responder”) que se pueden lograr con este enfoque.
Pruebas y Detección, midiendo la pérdida durante la etapa de entrenamiento y analizando modelos entrenados para detectar señales de un ataque de envenenamiento al analizar el comportamiento del modelo en entradas de prueba específicas.
Monitoreo y alertas sobre el número de respuestas sesgadas que superan un umbral.
Uso de un bucle humano para revisar respuestas y auditorías.
Implementar LLMs dedicados para comparar contra consecuencias no deseadas y entrenar otros LLMs utilizando técnicas de aprendizaje por refuerzo.
Realizar ejercicios de Red Team LLM o escaneos de vulnerabilidad LLM en las fases de prueba del ciclo de vida del LLM.

### Ejemplos de Escenarios de Ataque

La salida del prompt de IA generativa del LLM puede inducir a error a los usuarios de la aplicación, lo que puede llevar a opiniones sesgadas, seguidores o incluso peor, crímenes de odio, etc.
Si los datos de entrenamiento no se filtran y|o sanitizan correctamente, un usuario malicioso de la aplicación puede intentar influir e inyectar datos tóxicos en el modelo para que se adapte a los datos sesgados y falsos.
Un actor malicioso o un competidor crea intencionalmente documentos inexactos o maliciosos dirigidos a los datos de entrenamiento de un modelo en el que se está entrenando el modelo al mismo tiempo en base a entradas. El modelo víctima se entrena utilizando esta información falsificada, lo que se refleja en las salidas de los prompts de IA generativa a sus consumidores.
La vulnerabilidad Inyección de Prompt podría ser un vector de ataque para esta vulnerabilidad si no se realiza una sanitización y filtrado suficientes cuando la entrada de los clientes de la aplicación LLM se utiliza para entrenar el

### Enlaces de Referencia

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
## LLM04: Denegación de Servicio en Modelos

### Descripción

Un atacante interactúa con un LLM de una manera que consume una cantidad excepcionalmente alta de recursos, lo que resulta en una disminución en la calidad del servicio tanto para ellos como para otros usuarios, así como en la posible generación de altos costos de recursos. Además, una preocupación de seguridad emergente es la posibilidad de que un atacante interfiera o manipule la ventana de contexto de un LLM. Este problema se está volviendo más crítico debido al creciente uso de LLM en diversas aplicaciones, su intensiva utilización de recursos, la imprevisibilidad de la entrada del usuario y una falta de conciencia general entre los desarrolladores sobre esta vulnerabilidad. En los LLM, la ventana de contexto representa la longitud máxima de texto que el modelo puede manejar, cubriendo tanto la entrada como la salida. Es una característica crucial de los LLM ya que dicta la complejidad de los patrones de lenguaje que el modelo puede comprender y el tamaño del texto que puede procesar en un momento dado. El tamaño de la ventana de contexto está definido por la arquitectura del modelo y puede variar entre modelos.

### Ejemplos Comunes de Vulnerabilidad

Realizar consultas que conducen a un uso recurrente de recursos a través de la generación de un alto volumen de tareas en una cola, por ejemplo, con LangChain o AutoGPT.
Enviar consultas inusualmente consumidoras de recursos que utilizan ortografía o secuencias inusuales.
Desbordamiento continuo de entrada: Un atacante envía un flujo de entrada al LLM que excede su ventana de contexto, causando que el modelo consuma recursos computacionales excesivos.
Entradas largas repetitivas: El atacante envía repetidamente entradas largas al LLM, cada una excediendo la ventana de contexto.
Expansión recursiva del contexto: El atacante construye una entrada que desencadena la expansión recursiva del contexto, obligando al LLM a expandir y procesar repetidamente la ventana de contexto.
Inundación de entrada de longitud variable: El atacante inunda al LLM con un gran volumen de entradas de longitud variable, donde cada entrada está cuidadosamente diseñada para alcanzar justo el límite de la ventana de contexto. Esta técnica tiene como objetivo explotar cualquier ineficiencia en el procesamiento de entradas de longitud variable, forzando al LLM y potencialmente causando que se vuelva irresponsivo.

### Estrategias de Prevención y Mitigación

Implementar validación y sanitización de entradas para garantizar que las entradas de los usuarios se adhieran a los límites definidos y filtrar cualquier contenido malicioso.
Limitar el uso de recursos por solicitud o paso, de modo que las solicitudes que involucren partes complejas se ejecuten más lentamente.
Imponer límites de tasa en la API para restringir el número de solicitudes que un usuario individual o dirección IP puede hacer en un marco de tiempo específico.
Limitar el número de acciones en cola y el número total de acciones en un sistema que reacciona a las respuestas del LLM.
Monitorear continuamente la utilización de recursos del LLM para identificar picos anormales o patrones que puedan indicar un ataque de DoS.
Establecer límites estrictos de entrada basados en la ventana de contexto del LLM para prevenir la sobrecarga y el agotamiento de recursos.
Promover la concienciación entre los desarrolladores sobre posibles vulnerabilidades de DoS en los LLM y proporcionar pautas para la implementación segura de LLM.

### Ejemplos de Escenarios de Ataque

Un atacante envía repetidamente múltiples solicitudes difíciles y costosas a un modelo alojado, lo que lleva a un peor servicio para otros usuarios y a un aumento en las facturas de recursos para el anfitrión.
Un fragmento de texto en una página web se encuentra mientras una herramienta impulsada por LLM está recopilando información para responder a una consulta benigna. Esto lleva a que la herramienta realice muchas más solicitudes de páginas web, resultando en un gran consumo de recursos.
Un atacante bombardea continuamente al LLM con entradas que exceden su ventana de contexto. El atacante puede usar scripts automáticos o herramientas para enviar un alto volumen de entradas, abrumando las capacidades de procesamiento del LLM. Como resultado, el LLM consume recursos computacionales excesivos, lo que lleva a una desaceleración significativa o completa falta de respuesta del sistema.
Un atacante envía una serie de entradas secuenciales al LLM, con cada entrada diseñada para estar justo por debajo del límite de la ventana de contexto. Al enviar repetidamente estas entradas, el atacante busca agotar la capacidad disponible de la ventana de contexto. A medida que el LLM lucha por procesar cada entrada dentro de su ventana de contexto, los recursos del sistema se ven tensionados, lo que potencialmente resulta en un rendimiento degradado o una denegación completa del servicio.
Un atacante aprovecha los mecanismos recursivos del LLM para desencadenar repetidamente la expansión del contexto. Al elaborar entradas que explotan el comportamiento recursivo del LLM, el atacante obliga al modelo a expandir y procesar repetidamente la ventana de contexto, consumiendo recursos computacionales significativos. Este ataque tensiona el sistema y puede llevar a una condición de DoS, haciendo que el LLM no responda o causando su caída.
Un atacante inunda al LLM con un gran volumen de entradas de longitud variable, cuidadosamente elaboradas para acercarse o alcanzar el límite de la ventana de contexto. Al abrumar al LLM con entradas de longitudes variables, el atacante busca explotar cualquier ineficiencia en el procesamiento de entradas de longitud variable. Esta inundación de entradas pone una carga excesiva en los recursos del LLM, lo que potencialmente causa una degradación del rendimiento e impide la capacidad del sistema para responder a solicitudes legítimas.
Aunque los ataques de DoS comúnmente buscan abrumar los recursos del sistema, también pueden explotar otros aspectos del comportamiento del sistema, como las limitaciones de la API. Por ejemplo, en un reciente incidente de seguridad de Sourcegraph, el actor malicioso empleó un token de acceso de administrador filtrado para alterar los límites de tasa de la API, lo que potencialmente causó interrupciones del servicio al permitir niveles anormales de volúmenes de solicitudes.


### Enlaces de Referencia

LangChain max_iterations: hwchase17 on Twitter
Sponge Examples: Energy-Latency Attacks on Neural Networks: Arxiv White Paper
OWASP DOS Attack: OWASP
Learning From Machines: Know Thy Context: Luke Bechtel
Sourcegraph Security Incident on API Limits Manipulation and DoS Attack : Sourcegraph
## LLM05: Vulnerabilidades en la Cadena de Suministro

### Descripción

La cadena de suministro (supply-chain) en los LLM puede ser vulnerable, afectando la integridad de los datos de entrenamiento, los modelos de ML y las plataformas de despliegue. Estas vulnerabilidades pueden llevar a resultados sesgados, brechas de seguridad o incluso fallas completas del sistema. Tradicionalmente, las vulnerabilidades se centran en los componentes de software, pero el Aprendizaje Automático extiende esto con los modelos preentrenados y los datos de entrenamiento suministrados por terceros, susceptibles a ataques de manipulación y envenenamiento.

Finalmente, las extensiones de Plugins LLM pueden traer sus propias vulnerabilidades. Estas se describen en LLM07 - Diseño Inseguro de Plugin, que cubre la escritura de Plugins LLM y proporciona información útil para evaluar plugins de terceros.

### Ejemplos Comunes de Vulnerabilidad

Vulnerabilidades tradicionales en paquetes de terceros, incluyendo componentes obsoletos o en desuso.
Uso de un modelo preentrenado vulnerable para el fine-tuning.
Uso de datos de crowdsourcing envenenados para el entrenamiento.
Utilizar modelos obsoletos o en desuso que ya no se mantienen conduce a problemas de seguridad.
Términos y condiciones poco claros y políticas de privacidad de datos de los operadores del modelo llevan a que los datos sensibles de la aplicación se utilicen para el entrenamiento del modelo y la subsiguiente exposición de información sensible. Esto también puede aplicarse a riesgos derivados del uso de material con derechos de autor por parte del proveedor del modelo.

### Estrategias de Prevención y Mitigación

Evaluar cuidadosamente las fuentes de datos y proveedores, incluyendo los Términos y Condiciones y sus políticas de privacidad, utilizando solo proveedores de confianza. Asegurar que se disponga de seguridad adecuada y auditada de forma independiente y que las políticas del operador del modelo se alineen con sus políticas de protección de datos, es decir, que sus datos no se utilicen para entrenar sus modelos; de manera similar, buscar garantías y mitigaciones legales contra el uso de material con derechos de autor por parte de los mantenedores del modelo.
Utilizar solo plugins de reputación y asegurarse de que han sido probados para los requisitos de su aplicación. LLM-Insecure Plugin Design proporciona información sobre los aspectos de LLM del diseño inseguro de plugins que debe probar para mitigar riesgos al usar plugins de terceros.
Entender y aplicar las mitigaciones encontradas en el Top Diez de OWASP A06:2021 – Componentes Vulnerables y Desactualizados. Esto incluye escaneo de vulnerabilidades, gestión y parcheo de componentes. Para entornos de desarrollo con acceso a datos sensibles, aplicar estos controles también en esos entornos.
Mantener un inventario actualizado de componentes usando un Bill of Materials de Software (SBOM) para asegurar que tenga un inventario actualizado, preciso y firmado, evitando la manipulación de paquetes desplegados. Los SBOMs pueden ser utilizados para detectar y alertar rápidamente sobre nuevas vulnerabilidades de día cero.
Al momento de escribir, los SBOMs no cubren modelos, sus artefactos y conjuntos de datos. Si su aplicación LLM utiliza su propio modelo, debe usar las mejores prácticas de MLOps y plataformas que ofrezcan repositorios de modelos seguros con seguimiento de datos, modelos y experimentos.
También debe usar la firma de modelos y código al utilizar modelos y proveedores externos.
La detección de anomalías y las pruebas de robustez adversaria en modelos y datos suministrados pueden ayudar a detectar manipulación y envenenamiento, como se discute en Envenenamiento de Datos de Entrenamiento; idealmente, esto debería ser parte de los pipelines de MLOps; sin embargo, estas son técnicas emergentes y pueden ser más fáciles de implementar como parte de ejercicios de equipo rojo.
Implementar un monitoreo suficiente para cubrir escaneo de vulnerabilidades de componentes y entornos, uso de plugins no autorizados y componentes desactualizados, incluyendo el modelo y sus artefactos.
Implementar una política de parcheo para mitigar componentes vulnerables o desactualizados. Asegurar que la aplicación dependa de una versión mantenida de APIs y del modelo subyacente.
Revisar y auditar regularmente la Seguridad y Acceso de los proveedores, asegurando que no haya cambios en su postura de seguridad o Términos y Condiciones.

### Ejemplos de Escenarios de Ataque

Un atacante explota una biblioteca de Python vulnerable para comprometer un sistema. Esto ocurrió en la primera brecha de datos de Open AI.
Un atacante proporciona un plugin LLM para buscar vuelos, generando enlaces falsos que conducen a estafar a los usuarios.
Un atacante explota el registro de paquetes PyPi para engañar a los desarrolladores de modelos a descargar un paquete comprometido y exfiltrar datos o escalar privilegios en un entorno de desarrollo de modelos. Este fue un ataque real.
Un atacante envenena un modelo preentrenado de acceso público especializado en análisis económico e investigación social para crear una puerta trasera que genera desinformación y noticias falsas. Lo despliegan en un mercado de modelos (por ejemplo, Hugging Face) para que las víctimas lo utilicen.
Un atacante envenena conjuntos de datos de acceso público para ayudar a crear una puerta trasera al ajustar modelos. La puerta trasera favorece sutilmente a ciertas empresas en diferentes mercados.
Un empleado comprometido de un proveedor (desarrollador externo, empresa de hosting, etc.) exfiltra datos, modelos o códigos robando propiedad intelectual.
Un operador LLM cambia sus Términos y Condiciones y Política de Privacidad para requerir una exclusión explícita del uso de datos de la aplicación para el entrenamiento del modelo, lo que lleva a la memorización de datos sensibles.

### Enlaces de Referencia

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
## LLM06: Divulgación de Información Sensible

### Descripción

Las aplicaciones LLM tienen el potencial de revelar información sensible, algoritmos propios o detalles confidenciales a través de su salida. Esto puede resultar en acceso no autorizado a datos sensibles, propiedad intelectual, violaciones de privacidad y otras brechas de seguridad. Es importante que los consumidores de aplicaciones LLM estén conscientes de cómo interactuar de manera segura con los LLM y reconozcan los riesgos asociados con la introducción involuntaria de datos sensibles que posteriormente pueden ser devueltos por el LLM en la salida en otro lugar.

Para mitigar este riesgo, las aplicaciones LLM deben realizar una adecuada sanitización de datos para evitar que los datos del usuario entren en los datos del modelo de entrenamiento. Los propietarios de aplicaciones LLM también deben tener políticas adecuadas de Términos de Uso disponibles para hacer conscientes a los consumidores de cómo se procesan sus datos y la capacidad de optar por no incluir sus datos en el modelo de entrenamiento.

La interacción entre el consumidor y la aplicación LLM forma un límite de confianza bidireccional, donde no podemos confiar inherentemente en la entrada del cliente al LLM o en la salida del LLM al cliente. Es importante tener en cuenta que esta vulnerabilidad asume que ciertos requisitos previos están fuera del alcance, como ejercicios de modelado de amenazas, aseguramiento de la infraestructura y sandboxing adecuado. Agregar restricciones dentro del sistema de prompts sobre los tipos de datos que el LLM debería devolver puede proporcionar cierta mitigación contra la divulgación de información sensible, pero la naturaleza impredecible de los LLM significa que tales restricciones no siempre serán respetadas y podrían ser eludidas a través de la inyección de prompts u otros vectores.

### Ejemplos Comunes de Vulnerabilidad

Filtrado incompleto o inadecuado de información sensible en las respuestas del LLM.
Sobreajuste o memorización de datos sensibles en el proceso de entrenamiento del LLM.
Divulgación no intencionada de información confidencial debido a malinterpretaciones del LLM, falta de métodos de depuración de datos o errores.

### Estrategias de Prevención y Mitigación

Integrar técnicas adecuadas de sanitización y limpieza de datos para evitar que los datos del usuario entren en los datos del modelo de entrenamiento.
Implementar métodos robustos de validación y sanitización de entradas para identificar y filtrar posibles entradas maliciosas y prevenir la contaminación del modelo.
Al enriquecer el modelo con datos y si se realiza un fine-tunning del modelo: (es decir, datos alimentados al modelo antes o durante la implementación)
Cualquier cosa que se considere sensible en los datos de ajuste fino tiene el potencial de ser revelada a un usuario. Por lo tanto, aplicar la regla de mínimo privilegio y no entrenar el modelo con información a la que el usuario de mayor privilegio pueda acceder y que pueda ser mostrada a un usuario de menor privilegio.
El acceso a fuentes de datos externas (orquestación de datos en tiempo de ejecución) debe ser limitado.
Aplicar métodos estrictos de control de acceso a fuentes de datos externas y un enfoque riguroso para mantener una cadena de suministro (supply chain) segura.


### Ejemplos de Escenarios de Ataque

El usuario legítimo e inadvertido A queda expuesto a ciertos datos de otros usuarios a través del LLM al interactuar con la aplicación LLM de manera no maliciosa.
El usuario A dirige un conjunto bien elaborado de prompts para eludir los filtros de entrada y la sanitización del LLM, lo que hace que revele información sensible (PII) sobre otros usuarios de la aplicación.
Datos personales, como PII, se filtran en el modelo a través de los datos de entrenamiento debido a negligencia del propio usuario o de la aplicación LLM. Este caso podría aumentar el riesgo y la probabilidad de los escenarios 1 o 2 mencionados anteriormente.

### Enlaces de Referencia

AI data leak crisis: New tool prevents company secrets from being fed to ChatGPT: Fox Business
Lessons learned from ChatGPT’s Samsung leak: Cybernews
Cohere - Terms Of Use: Cohere
A threat modeling example: AI Village
OWASP AI Security and Privacy Guide: OWASP AI Security & Privacy Guide
Ensuring the Security of Large Language Models: Experts Exchange
## LLM07: Diseño Inseguro de Plugins

### Descripción

Los plugins de LLM son extensiones que, una vez habilitadas, son llamadas automáticamente por el modelo durante las interacciones con los usuarios. La plataforma de integración del modelo los impulsa, y la aplicación puede no tener control sobre la ejecución, especialmente cuando el modelo está alojado por otra parte. Además, es probable que los plugins implementen entradas de texto libre del modelo sin validación o verificación de tipo para lidiar con limitaciones de tamaño de contexto. Esto permite a un atacante potencial construir una solicitud maliciosa al plugin, lo que podría resultar en una amplia gama de comportamientos no deseados, incluida la ejecución remota de código.

El daño de las entradas maliciosas a menudo depende de controles de acceso insuficientes y del fracaso en rastrear la autorización a través de los plugins. El control de acceso inadecuado permite que un plugin confíe ciegamente en otros plugins y asuma que el usuario final proporcionó las entradas. Dicho control de acceso inadecuado puede permitir que las entradas maliciosas tengan consecuencias dañinas que van desde la exfiltración de datos, la ejecución remota de código y la escalada de privilegios.

Este elemento se enfoca en la creación de plugins de LLM en lugar de plugins de terceros, los cuales son cubiertos por las Vulnerabilidades en la Cadena de Suministro de LLM (LLM-Supply-Chain-Vulnerabilities cover).

### Ejemplos Comunes de Vulnerabilidad

Un plugin acepta todos los parámetros en un único campo de texto en lugar de parámetros de entrada distintos.
Un plugin acepta cadenas de configuración en lugar de parámetros que pueden sobrescribir la configuración completa.
Un plugin acepta sentencias SQL crudas o declaraciones de programación en lugar de parámetros.
La autenticación se realiza sin autorización explícita para un plugin en particular.
Un plugin trata todo el contenido de LLM como si fuera creado enteramente por el usuario y realiza cualquier acción solicitada sin requerir autorización adicional.

### Estrategias de Prevención y Mitigación

Los plugins deben cumplir una entrada parametrizada estricta siempre que sea posible e incluir verificaciones de tipo y rango en las entradas. Cuando esto no sea posible, se debe introducir una segunda capa de llamadas tipificadas, analizando las solicitudes y aplicando validación y saneamiento. Cuando se deba aceptar una entrada libre debido a la semántica de la aplicación, se debe inspeccionar cuidadosamente para asegurar que no se estén llamando métodos potencialmente dañinos.
Los desarrolladores de plugins deben aplicar las recomendaciones de OWASP en ASVS (Estándar de Verificación de Seguridad de Aplicaciones) para asegurar una validación y saneamiento adecuados de las entradas.
Los plugins deben ser inspeccionados y probados exhaustivamente para garantizar una validación adecuada. Utilizar análisis de Seguridad de Aplicaciones Estáticas (SAST) y pruebas de aplicaciones Dinámicas e Interactivas (DAST, IAST) en los pipelines de desarrollo.
Los plugins deben ser diseñados para minimizar el impacto de la explotación de cualquier parámetro de entrada inseguro siguiendo las Pautas de Control de Acceso de OWASP ASVS. Esto incluye el control de acceso de mínimo privilegio, exponiendo la menor funcionalidad posible mientras aún se realiza su función deseada.
Los plugins deben usar identidades de autenticación apropiadas, como OAuth2, para aplicar autorización y control de acceso efectivos. Además, las claves de API deben usarse para proporcionar contexto para decisiones de autorización personalizadas que reflejen la ruta del plugin en lugar del usuario interactivo por defecto.
Requerir autorización y confirmación manual del usuario para cualquier acción realizada por plugins sensibles.
Los plugins son, típicamente, APIs REST, por lo que los desarrolladores deben aplicar las recomendaciones encontradas en OWASP Top 10 Riesgos de Seguridad de API – 2023 para minimizar vulnerabilidades genéricas.

### Ejemplos de Escenarios de Ataque

Un plugin acepta una URL base e instruye al LLM para combinar la URL con una consulta para obtener pronósticos del tiempo que se incluyen al manejar la solicitud del usuario. Un usuario malicioso puede crear una solicitud de tal manera que la URL apunte a un dominio que controlan, lo que les permite inyectar su propio contenido en el sistema LLM a través de su dominio.
Un plugin acepta una entrada de formulario libre en un único campo que no valida. Un atacante suministra cargas útiles cuidadosamente elaboradas para realizar reconocimiento a partir de mensajes de error. Luego explota vulnerabilidades conocidas de terceros para ejecutar código y realizar exfiltración de datos o escalada de privilegios.
Un plugin utilizado para recuperar incrustaciones de una tienda de vectores acepta parámetros de configuración como una cadena de conexión sin ninguna validación. Esto permite a un atacante experimentar y acceder a otras tiendas de vectores cambiando nombres o parámetros de host y exfiltrar incrustaciones a las que no deberían tener acceso.
Un plugin acepta cláusulas WHERE de SQL como filtros avanzados, que luego se añaden al filtrado de SQL. Esto permite a un atacante realizar un ataque de SQL.
Un atacante utiliza la inyección indirecta de mensajes para explotar un plugin inseguro de gestión de código sin validación de entrada y control de acceso débil para transferir la propiedad del repositorio y bloquear al usuario de sus repositorios.

### Enlaces de Referencia

OpenAI ChatGPT Plugins: ChatGPT Developer’s Guide
OpenAI ChatGPT Plugins - Plugin Flow: OpenAI Documentation
OpenAI ChatGPT Plugins - Authentication: OpenAI Documentation
OpenAI Semantic Search Plugin Sample: OpenAI Github
Plugin Vulnerabilities: Visit a Website and Have Your Source Code Stolen: Embrace The Red
ChatGPT Plugin Exploit Explained: From Prompt Injection to Accessing Private Data: Embrace The Red
OWASP ASVS - 5 Validation, Sanitization and Encoding: OWASP AASVS
OWASP ASVS 4.1 General Access Control Design: OWASP AASVS
OWASP Top 10 API Security Risks – 2023: OWASP
## LLM08: Responsabilidad Excesiva

### Descripción

Un sistema basado en LLM a menudo se le otorga un grado de responsabilidad por su desarrollador: la capacidad de interactuar con otros sistemas y realizar acciones en respuesta a un mensaje. La decisión sobre qué funciones invocar también puede ser delegada a un 'agente' LLM para determinarla dinámicamente en función del mensaje de entrada o de la salida del LLM.

La Responsabilidad Excesiva es la vulnerabilidad que permite realizar acciones dañinas en respuesta a salidas inesperadas/ambiguas de un LLM (independientemente de lo que esté causando el mal funcionamiento del LLM; ya sea alucinación/confabulación, inyección de mensajes directa/indirecta, plugin malicioso, mensajes benignos mal diseñados, o simplemente un modelo de bajo rendimiento). La causa raíz de la Responsabilidad Excesiva es típicamente una o más de: funcionalidad excesiva, permisos excesivos o autonomía excesiva. Esto difiere del Manejo Inseguro de Salidas, que se preocupa por el escrutinio insuficiente de las salidas del LLM.

La Responsabilidad Excesiva puede llevar a un amplio rango de impactos en el espectro de confidencialidad, integridad y disponibilidad, y depende de con qué sistemas una aplicación basada en LLM pueda interactuar.

### Ejemplos Comunes de Vulnerabilidad

Funcionalidad Excesiva: Un agente LLM tiene acceso a plugins que incluyen funciones que no son necesarias para la operación prevista del sistema. Por ejemplo, un desarrollador necesita otorgar a un agente LLM la capacidad de leer documentos de un repositorio, pero el plugin de terceros que eligen usar también incluye la capacidad de modificar y eliminar documentos.
Funcionalidad Excesiva: Un plugin que se probó durante una fase de desarrollo y se abandonó en favor de una mejor alternativa, pero el plugin original permanece disponible para el agente LLM.
Funcionalidad Excesiva: Un plugin LLM con funcionalidad abierta no filtra adecuadamente las instrucciones de entrada para comandos que no son necesarios para la operación prevista de la aplicación. Por ejemplo, un plugin para ejecutar un comando de shell específico no impide adecuadamente la ejecución de otros comandos de shell.
Permisos Excesivos: Un plugin LLM tiene permisos en otros sistemas que no son necesarios para la operación prevista de la aplicación. Por ejemplo, un plugin destinado a leer datos se conecta a un servidor de base de datos utilizando una identidad que no solo tiene permisos de SELECT, sino también de UPDATE, INSERT y DELETE.
Permisos Excesivos: Un plugin LLM diseñado para realizar operaciones en nombre de un usuario accede a sistemas downstream con una identidad genérica de alto privilegio. Por ejemplo, un plugin para leer el almacén de documentos del usuario actual se conecta al repositorio de documentos con una cuenta privilegiada que tiene acceso a todos los archivos de los usuarios.
Autonomía Excesiva: Una aplicación o plugin basado en LLM no verifica ni aprueba de forma independiente acciones de alto impacto. Por ejemplo, un plugin que permite la eliminación de documentos de un usuario realiza eliminaciones sin ninguna confirmación del usuario.

### Prevention and Mitigation Strategies

Las siguientes acciones pueden prevenir la Responsabilidad Excesiva:

Limitar los plugins/herramientas a los que los agentes LLM pueden llamar solo a las funciones mínimas necesarias. Por ejemplo, si un sistema basado en LLM no requiere la capacidad de obtener el contenido de una URL, entonces tal plugin no debería ofrecerse al agente LLM.
Limitar las funciones que se implementan en los plugins/herramientas LLM al mínimo necesario. Por ejemplo, un plugin que accede al buzón de un usuario para resumir correos electrónicos solo puede requerir la capacidad de leer correos electrónicos, por lo que el plugin no debería contener otra funcionalidad como eliminar o enviar mensajes.
Evitar funciones abiertas donde sea posible (por ejemplo, ejecutar un comando de shell, obtener una URL, etc.) y usar plugins/herramientas con funcionalidad más granular. Por ejemplo, una aplicación basada en LLM puede necesitar escribir alguna salida en un archivo. Si esto se implementara usando un plugin para ejecutar una función de shell, entonces el alcance de acciones indeseables es muy grande (cualquier otro comando de shell podría ejecutarse). Una alternativa más segura sería construir un plugin de escritura de archivos que solo admitiera esa funcionalidad específica.
Limitar los permisos que se otorgan a los plugins/herramientas LLM en otros sistemas al mínimo necesario para limitar el alcance de acciones indeseables. Por ejemplo, un agente LLM que utiliza una base de datos de productos para hacer recomendaciones de compra a un cliente podría necesitar solo acceso de lectura a una tabla de 'productos'; no debería tener acceso a otras tablas, ni la capacidad de insertar, actualizar o eliminar registros. Esto debería hacerse cumplir aplicando los permisos de base de datos adecuados para la identidad que el plugin LLM utiliza para conectarse a la base de datos.
Rastrear la autorización del usuario y el alcance de seguridad para asegurar que las acciones realizadas en nombre de un usuario se ejecuten en sistemas downstream en el contexto de ese usuario específico y con los mínimos privilegios necesarios. Por ejemplo, un plugin de LLM que lee el repositorio de código de un usuario debería requerir que el usuario se autentique a través de OAuth y con el alcance mínimo requerido.
Utilizar control humano en el proceso para requerir la aprobación de un humano para todas las acciones antes de que se realicen. Esto puede implementarse en un sistema downstream (fuera del alcance de la aplicación LLM) o dentro del propio plugin/herramienta LLM. Por ejemplo, una aplicación basada en LLM que crea y publica contenido en redes sociales en nombre de un usuario debería incluir una rutina de aprobación del usuario dentro del plugin/herramienta/API que implementa la operación de 'publicación'.
Implementar autorización en sistemas downstream en lugar de depender de un LLM para decidir si una acción está permitida o no. Al implementar herramientas/plugins, hacer cumplir el principio de mediación completa para que todas las solicitudes hechas a sistemas downstream a través de los plugins/herramientas sean validadas contra políticas de seguridad.

Las siguientes opciones no evitarán la Responsabilidad Excesiva, pero pueden limitar el nivel de daño causado:

Registrar y monitorear la actividad de los plugins/herramientas LLM y sistemas downstream para identificar dónde se están realizando acciones indeseables, y responder en consecuencia.
Implementar limitación de tasa para reducir el número de acciones indeseables que pueden tener lugar en un período de tiempo determinado, aumentando la oportunidad de descubrir acciones indeseables a través del monitoreo antes de que pueda ocurrir un daño significativo.

### Ejemplos de Escenarios de Ataque

Una aplicación de asistente personal basada en LLM obtiene acceso al buzón de correo de un individuo a través de un plugin para resumir el contenido de los correos electrónicos entrantes. Para lograr esta funcionalidad, el plugin de correo electrónico requiere la capacidad de leer mensajes, sin embargo, el plugin elegido por el desarrollador del sistema también contiene funciones para enviar mensajes. El LLM es vulnerable a un ataque de inyección de mensaje indirecto, en el que un correo electrónico maliciosamente diseñado engaña al LLM para que ordene al plugin de correo electrónico llamar a la función de 'enviar mensaje' para enviar spam desde el buzón del usuario. Esto podría evitarse mediante:<br><br>
(a) eliminando la funcionalidad excesiva utilizando un plugin que solo ofrezca capacidades de lectura de correo, <br>
(b) eliminando permisos excesivos autenticándose en el servicio de correo electrónico del usuario a través de una sesión OAuth con un alcance de solo lectura, y/o <br>
(c) eliminando la autonomía excesiva al requerir que el usuario revise manualmente y presione 'enviar' en cada correo redactado por el plugin LLM.
Alternativamente, el daño causado podría reducirse implementando limitación de tasa en la interfaz de envío de correos.

### Enlaces de Referencia

Embrace the Red: Confused Deputy Problem: Embrace The Red
NeMo-Guardrails: Interface guidelines: NVIDIA Github
LangChain: Human-approval for tools: Langchain Documentation
Simon Willison: Dual LLM Pattern: Simon Willison
## LLM09: Sobredependencia

### Descripción

La Sobredependencia puede ocurrir cuando un LLM produce información errónea y la proporciona de manera autoritaria. Aunque los LLM pueden generar contenido creativo e informativo, también pueden crear contenido que es incorrecto, inapropiado o peligroso. Esto se conoce como alucinación o confabulación. Cuando las personas o sistemas confían en esta información sin supervisión o confirmación, puede resultar en una violación de seguridad, desinformación, mala comunicación, problemas legales y daño a la reputación.

El código fuente generado por LLM puede introducir vulnerabilidades de seguridad no detectadas. Esto representa un riesgo significativo para la seguridad operativa y de las aplicaciones. Estos riesgos muestran la importancia de procesos de revisión rigurosos, con:

Supervisión
Mecanismos de validación continua
Avisos sobre el riesgo

### Ejemplos Comunes de Vulnerabilidad

LLM proporciona información inexacta como respuesta, indicándola de manera que implica alta autoridad. El sistema en general está diseñado sin los controles y equilibrios adecuados para manejar esto y la información engaña al usuario de una manera que conduce a daños.
LLM sugiere código inseguro o erroneo, lo que lleva a vulnerabilidades cuando se incorpora en un sistema de software sin la supervisión o verificación adecuada.

### Estrategias de Prevención y Mitigación

Monitorear y revisar regularmente las salidas del LLM. Utilizar técnicas de autoconsistencia o votación para filtrar textos inconsistentes. Comparar múltiples respuestas del modelo para una sola solicitud puede ayudar a juzgar mejor la calidad y consistencia de la salida.
Contrastar la salida del LLM con fuentes externas confiables. Esta capa adicional de validación puede ayudar a asegurar que la información proporcionada por el modelo sea precisa y confiable.
Mejorar el modelo con ajustes finos o incrustaciones para mejorar la calidad de la salida. Los modelos preentrenados genéricos tienen más probabilidades de producir información inexacta en comparación con modelos ajustados en un dominio particular. Técnicas como la ingeniería de indicaciones, el ajuste eficiente de parámetros (PET), el ajuste completo del modelo y las indicaciones de cadena de pensamiento pueden emplearse para este propósito.
Implementar mecanismos de validación automática que puedan verificar cruzadamente la salida generada contra hechos o datos conocidos. Esto puede proporcionar una capa adicional de seguridad y mitigar los riesgos asociados con las alucinaciones.
Desglosar tareas complejas en subtareas manejables y asignarlas a diferentes agentes. Esto no solo ayuda a gestionar la complejidad, sino que también reduce las posibilidades de alucinaciones, ya que cada agente puede ser responsable de una tarea más pequeña.
Comunicar claramente los riesgos y limitaciones asociados con el uso de LLM. Esto incluye la posibilidad de inexactitudes en la información y otros riesgos. Una comunicación efectiva de los riesgos puede preparar a los usuarios para problemas potenciales y ayudarles a tomar decisiones informadas.
Desarrollar API e interfaces de usuario que fomenten un uso responsable y seguro de los LLM. Esto puede incluir medidas como filtros de contenido, advertencias a los usuarios sobre posibles inexactitudes y etiquetado claro del contenido generado por IA.
Al usar LLM en entornos de desarrollo, establecer prácticas y directrices de codificación segura para prevenir la integración de posibles vulnerabilidades.

### Ejemplos de Escenarios de Ataque

Una organización de noticias utiliza intensivamente un LLM para generar artículos de noticias. Un actor malicioso explota esta sobredependencia, alimentando al LLM con información engañosa y causando la difusión de desinformación.
La IA plagia involuntariamente contenido, lo que lleva a problemas de derechos de autor y disminución de la confianza en la organización.
Un equipo de desarrollo de software utiliza un sistema LLM para acelerar el proceso de codificación. La sobredependencia en las sugerencias de la IA introduce vulnerabilidades de seguridad en la aplicación debido a configuraciones predeterminadas inseguras o recomendaciones inconsistentes con prácticas de codificación segura.
Una empresa de desarrollo de software utiliza un LLM para asistir a los desarrolladores. El LLM sugiere una biblioteca o paquete de código inexistente, y un desarrollador, confiando en la IA, integra involuntariamente un paquete malicioso en el software de la empresa. Esto resalta la importancia de contrastar las sugerencias del LLM, especialmente cuando se involucran códigos o bibliotecas de terceros.

### Enlaces de Referencia

Understanding LLM Hallucinations: Towards Data Science
How Should Companies Communicate the Risks of Large Language Models to Users?: Techpolicy
A news site used AI to write articles. It was a journalistic disaster: Washington Post
AI Hallucinations: Package Risk: Vulcan.io
How to Reduce the Hallucinations from Large Language Models: The New Stack
Practical Steps to Reduce Hallucination: Victor Debia
## LLM10: Robo de Modelos

### Descripción

Esta entrada se refiere al acceso no autorizado y exfiltración de modelos de LLM por actores maliciosos o APTs. Esto surge cuando los modelos de LLM propietarios (siendo un activo valioso), son comprometidos, robados físicamente, copiados o se extraen pesos y parámetros para crear un equivalente funcional. El impacto del robo de modelos de LLM puede incluir pérdida económica y de reputación de marca, degradación de la ventaja competitiva, uso no autorizado del modelo o acceso no autorizado a información sensible contenida en el modelo.

El robo de LLM representa una preocupación de seguridad significativa a medida que los modelos de lenguaje se vuelven cada vez más poderosos y prevalentes. Las organizaciones e investigadores deben priorizar medidas de seguridad robustas para proteger sus modelos de LLM, asegurando la confidencialidad e integridad de su propiedad intelectual. Emplear un marco de seguridad integral que incluya controles de acceso, encriptación y monitoreo continuo es crucial para mitigar los riesgos asociados con el robo de modelos de LLM y proteger los intereses tanto de individuos como de organizaciones que dependen del LLM.

### Ejemplos Comunes de Vulnerabilidad

Un atacante explota una vulnerabilidad en la infraestructura de una empresa para obtener acceso no autorizado a su repositorio de modelos de LLM a través de una mala configuración en sus ajustes de seguridad de red o aplicación.
Un escenario de amenaza interna donde un empleado descontento (insider) filtra modelos o artefactos relacionados.
Un atacante consulta la API del modelo usando entradas cuidadosamente elaboradas y técnicas de inyección de prompts para recopilar un número suficiente de salidas para crear un clon del modelo (shadown model). 
Un ciberdelincuente es capaz de eludir las técnicas de filtrado de entradas del LLM para realizar un ataque de canal lateral y, en última instancia, recolectar información de pesos y arquitectura del modelo a un recurso controlado remotamente.
El vector de ataque para la extracción del modelo implica consultar el LLM con un gran número de prompts sobre un tema particular. Las salidas del LLM pueden luego usarse para ajustar otro modelo. Sin embargo, hay algunas cosas a tener en cuenta sobre este ataque:
El atacante debe generar un gran número de prompts dirigidos. Si los prompts no son lo suficientemente específicos, las salidas del LLM serán inútiles.
Las salidas de los LLM a veces pueden contener respuestas alucinadas, lo que significa que el atacante no podrá extraer el modelo completo ya que algunas de las salidas pueden ser sin sentido.
No es posible replicar un LLM al 100% a través de la extracción del modelo. Sin embargo, el atacante podrá replicar un modelo parcial.
El vector de ataque para la _replicación funcional del modelo_ implica usar el modelo objetivo a través de prompts para generar datos de entrenamiento sintéticos (un enfoque llamado "autoinstrucción") para luego usarlo y ajustar otro modelo fundacional para producir un equivalente funcional. Esto elude las limitaciones de la extracción basada en consultas tradicionales utilizada en el Ejemplo 5 y se ha utilizado con éxito en investigaciones de uso de un LLM para entrenar otro LLM. Aunque en el contexto de esta investigación, la replicación del modelo no es un ataque. El enfoque podría ser utilizado por un atacante para replicar un modelo propietario con una API pública.

El uso de un modelo robado, como un "shadow model", puede usarse para montar ataques adversarios incluyendo acceso no autorizado a información sensible contenida en el modelo o experimentar sin ser detectados con entradas adversarias para seguir montando inyecciones de prompts avanzadas.

### Estrategias de Prevención y Mitigación

Implementar controles de acceso fuertes (por ejemplo, RBAC y regla de mínimo privilegio) y mecanismos de autenticación fuertes para limitar el acceso no autorizado a repositorios de modelos de LLM y entornos de entrenamiento.
Esto es especialmente cierto para los tres primeros ejemplos comunes, que podrían causar esta vulnerabilidad debido a amenazas internas, mala configuración y/o controles de seguridad débiles sobre la infraestructura que alberga modelos de LLM, pesos y arquitectura en la que un actor malicioso podría infiltrarse desde dentro o fuera del entorno.
El seguimiento de la gestión de proveedores, la verificación y las vulnerabilidades de dependencia son temas importantes para prevenir explotaciones de ataques a la cadena de suministro (supply-chain attacks).
Restringir el acceso del LLM a recursos de red, servicios internos y APIs.
Esto es particularmente cierto para todos los ejemplos comunes, ya que cubre el riesgo y las amenazas internas, pero también controla finalmente a qué tiene acceso la aplicación LLM y, por lo tanto, podría ser un mecanismo o paso de prevención para evitar ataques por un canal lateral.
Utilizar un Inventario Centralizado (Registry ML Model) para modelos utilizados en producción. Tener un registro centralizado de modelos evita el acceso no autorizado a Modelos de ML mediante controles de acceso, autenticación y capacidades de monitoreo/registro que son buenas bases para la gobernanza. Tener un repositorio centralizado también es beneficioso para recopilar datos sobre algoritmos utilizados por los modelos con fines de cumplimiento, evaluaciones de riesgo y mitigación de riesgos.
Monitorear y auditar regularmente los registros de acceso y las actividades relacionadas con los repositorios de modelos de LLM para detectar y responder rápidamente a cualquier comportamiento sospechoso o no autorizado.
Automatizar la implementación de MLOps con gobernanza y flujos de trabajo de seguimiento y aprobación para reforzar los controles de acceso y despliegue dentro de la infraestructura.
Implementar controles y estrategias de mitigación para mitigar y/o reducir el riesgo de técnicas de inyección de prompts que causan ataques de canal lateral.
Limitar la tasa de llamadas a la API (Rate Limiting API) donde sea aplicable y/o filtros para reducir el riesgo de exfiltración de datos de las aplicaciones LLM, o implementar técnicas para detectar (por ejemplo, DLP) la actividad de extracción desde otros sistemas de monitoreo.
Implementar entrenamiento en robustez adversaria para ayudar a detectar consultas de extracción y reforzar las medidas de seguridad física.
Implementar un marco de marcado de agua en las etapas de incrustación y detección del ciclo de vida de los LLM.

### Ejemplos de Escenarios de Ataque

Un atacante explota una vulnerabilidad en la infraestructura de una empresa para obtener acceso no autorizado a su repositorio de modelos de LLM. El atacante procede a exfiltrar modelos valiosos de LLM y los utiliza para lanzar un servicio de procesamiento de lenguaje competidor o extraer información sensible, causando un daño financiero significativo a la empresa original.
Un empleado (insider) filtra modelos o artefactos relacionados. La exposición pública de este escenario aumenta el conocimiento de los atacantes para ataques adversarios de caja gris o, alternativamente, roba directamente la propiedad disponible.
Un atacante consulta la API con entradas cuidadosamente seleccionadas y recopila un número suficiente de salidas para crear un shadow model.
Una falla en el control de seguridad dentro de la cadena de suministro conduce a filtraciones de datos de información de modelo propietaria.
Un ciberdelicuente elude las técnicas de filtrado de entradas y preámbulos del LLM para realizar un ataque de canal lateral y recuperar información del modelo a un recurso controlado de forma remota bajo su control.

### Enlaces de Referencia

Meta’s powerful AI language model has leaked online: The Verge
Runaway LLaMA | How Meta's LLaMA NLP model leaked: Deep Learning Blog
AML.TA0000 ML Model Access: MITRE ATLAS
I Know What You See: Arxiv White Paper
D-DAE: Defense-Penetrating Model Extraction Attacks: Computer.org
A Comprehensive Defense Framework Against Model Extraction Attacks: IEEE
Alpaca: A Strong, Replicable Instruction-Following Model: Stanford Center on Research for Foundation Models (CRFM)
How Watermarking Can Help Mitigate The Potential Risks Of LLMs?: KD Nuggets

# Introducción a la ingeniería de solicitudes con GitHub Copilot
## Introducción

GitHub Copilot, con tecnología de OpenAI, está cambiando el juego en el desarrollo de software al acelerar los flujos de trabajo de desarrollo desde la creación de código inicial hasta implementaciones listas para producción. GitHub Copilot puede comprender los detalles complejos del proyecto a través de su entrenamiento de datos que contienen lenguaje natural y miles de millones de líneas de código fuente de orígenes disponibles públicamente, incluido el código en repositorios públicos de GitHub. Esto permite que GitHub Copilot le proporcione sugerencias más contextuales que le ayuden a entregar rápidamente cambios de código y automatizar tareas de desarrollo rutinarias.

Pero para sacar el máximo partido de GitHub Copilot y maximizar la velocidad de desarrollo, debe saber sobre la ingeniería rápida. La ingeniería rápida es cómo se indica a GitHub Copilot lo que necesita con precisión y eficacia. La calidad del código que devuelve y la rapidez con la que se puede iterar hacia la solución perfecta depende de lo claro y estratégico que sean sus indicaciones.

En este módulo, obtendrá información sobre lo siguiente:

Principios de ingeniería de instrucciones, mejores prácticas y cómo GitHub Copilot aprende de tus prompts para proporcionar respuestas contextuales que aceleran los ciclos de desarrollo.
Estrategias avanzadas de solicitud, que incluyen el aviso de roles y la gestión del historial de chat, para obtener mejores resultados con menos iteraciones.
Flujo subyacente de cómo GitHub Copilot procesa las solicitudes de usuario para generar respuestas o sugerencias de código de forma eficaz.
El flujo de datos para sugerencias de código y chat en GitHub Copilot.
LLM y su rol en GitHub Copilot y preguntar.
Cómo crear avisos eficaces que optimicen el rendimiento de GitHub Copilot, lo que garantiza la precisión y la relevancia en cada sugerencia de código, al tiempo que se minimizan los ciclos de revisión.
La relación compleja entre las solicitudes y las respuestas de Copilot para simplificar el flujo de trabajo de desarrollo.
Cómo Copilot controla los datos de las indicaciones en diferentes situaciones, incluida la transmisión segura y el filtrado de contenido.

## Fundamentos de la ingeniería de solicitudes y procedimientos recomendados
En esta unidad, trataremos lo siguiente:

¿Qué es la ingeniería de solicitudes?
Fundamentos de la ingeniería de solicitudes
Procedimientos recomendados en la ingeniería de solicitudes
Cómo aprende Copilot de sus solicitudes
¿Qué es la ingeniería de solicitudes?
La ingeniería de solicitudes es el proceso de creación de instrucciones claras para guiar los sistemas de inteligencia artificial, como GitHub Copilot, para que genere el código adecuado para que en cada contexto se adapte a las necesidades específicas del proyecto. Esto garantiza que el código sea correcto sintáctica, funcional y contextualmente.

Ahora que sabe qué es la ingeniería de solicitudes, vamos a aprender sobre algunos de sus principios.

Principios de ingeniería de solicitudes
Antes de explorar estrategias específicas, primero comprendamos los principios básicos de la ingeniería de indicaciones, resumidos en las siguientes 4 S. Estas reglas básicas son la base para crear solicitudes efectivas.

Single (única): centre siempre su solicitud en una única tarea o pregunta bien definida. Esta claridad es fundamental para la elición de respuestas precisas y útiles de Copilot.
Specific (específica): asegúrese de que las instrucciones son explícitas y detalladas. La especificidad conduce a sugerencias de código más aplicables y precisas.
Short (corta): a la vez que especifica, mantenga las solicitudes concisas y al grano. Este equilibrio garantiza la claridad sin sobrecargar Copilot ni complicar la interacción.
Surround (enmarcada): use nombres de archivo descriptivos y mantenga abiertos los archivos relacionados. Esto proporciona a Copilot un contexto enriquecido, lo que conduce a sugerencias de código más adaptadas.
Estos principios básicos constituyen la base para elaborar solicitudes eficientes y eficaces. Teniendo en cuenta las 4 S, vamos a profundizar en los procedimientos recomendados avanzados que garantizan que cada interacción con GitHub Copilot esté optimizada.

Procedimientos recomendados en la ingeniería de solicitudes
Las siguientes prácticas avanzadas, basadas en los 4 S, refinan y mejoran la interacción con Copilot, asegurándose de que el código generado no solo es preciso, sino que se alinea perfectamente con las necesidades y contextos específicos del proyecto.

Proporcionar suficiente claridad
Basándose en los principios de solicitud "Single" (única) y "Specific" (específica), apunte siempre a la claridad. Por ejemplo, una solicitud como "Escribe una función de Python para filtrar y devolver números pares de una lista determinada" es específica y centrada en una única cosa.

Captura de pantalla de un chat de Copilot con un símbolo del sistema de Python.

Proporcionar suficiente contexto con detalles
Enriquecer la comprensión de Copilot con el contexto, siguiendo el principio "Surround" (solicitud enmarcada). Cuanto más información contextual se proporcione, más adecuadas son las sugerencias de código generadas. Por ejemplo, agregando algunos comentarios en la parte superior del código para proporcionar más detalles a lo que quiere, puede proporcionar más contexto a Copilot para comprender la solicitud y proporcionar mejores sugerencias de código.

Captura de pantalla de los comentarios agregados al código para obtener mejores sugerencias de Copilot.

En el ejemplo anterior, hemos usado pasos para proporcionar más detalles a la vez que mantenemos la solicitud corta. Esta práctica sigue el principio de solicitud "Short" (corta), equilibrando los detalles concisamente para garantizar la claridad y precisión en la comunicación.

 Nota

Copilot también usa pestañas abiertas paralelas en el editor de código para obtener más contexto sobre los requisitos del código.

Proporcionar ejemplos para el aprendizaje
El uso de ejemplos puede aclarar sus requisitos y expectativas, ilustrando conceptos abstractos y haciendo que las solicitudes sean más tangibles para Copilot. Los ejemplos bien diseñados ayudan a Copilot a comprender rápidamente los patrones, lo que conduce a sugerencias iniciales más precisas que requieren menos ciclos de revisión. Este enfoque es especialmente eficaz para generar código reutilizable, plantillas de prueba e implementaciones repetitivas que forman la base de características más grandes.

Captura de pantalla de un ejemplo usado para aclarar las solicitudes de Copilot.

Aserción e iteración
Una de las claves para desbloquear todo el potencial de GitHub Copilot y acelerar el flujo de trabajo de desarrollo es la práctica de iteración estratégica. Es posible que la primera solicitud no siempre produzca código listo para producción, y eso es perfectamente aceptable. En lugar de dedicar tiempo a refinar manualmente la salida, tratarla como el principio de un diálogo eficaz con Copilot.

Si el primer resultado no es exactamente lo que busca, no empiece desde cero. En su lugar, borre el código sugerido, enriquezca el comentario inicial con detalles y ejemplos agregados y vuelva a preguntar a Copilot. Este enfoque iterativo a menudo le lleva a código de alta calidad y listo para la implementación más rápido que los métodos de desarrollo tradicionales, ya que cada iteración se basa en la comprensión de Copilot de sus requisitos específicos.

Ahora que ha aprendido los procedimientos recomendados para mejorar las aptitudes que le solicitan, echemos un vistazo más a cómo puede proporcionar ejemplos de los que Copilot puede aprender.

Cómo aprende Copilot de sus solicitudes
GitHub Copilot funciona en función de los modelos de inteligencia artificial entrenados en grandes cantidades de datos. Para mejorar su comprensión de contextos de código específicos, los ingenieros suelen proporcionarle ejemplos. Esta práctica, que se encuentra normalmente en el aprendizaje automático, llevó a diferentes enfoques de entrenamiento, como:

Aprendizaje en pocas etapas
Aquí, GitHub Copilot genera código sin ningún ejemplo específico, basándose únicamente en su entrenamiento fundamental. Este enfoque es ideal para implementar rápidamente patrones comunes y funcionalidad estándar. Por ejemplo, supongamos que desea crear una función para convertir las temperaturas entre Celsius y Fahrenheit. Solo puede empezar escribiendo un comentario que describa lo que quiera y Copilot podría generar código listo para producción para usted, en función de su entrenamiento anterior, sin ningún otro ejemplo.

Captura de pantalla de Copilot que crea un código de conversión de temperatura a partir de un comentario.

Aprendizaje en pocas etapas
Con este enfoque, se proporciona un único ejemplo, lo que ayuda al modelo a generar respuestas más compatibles con el contexto que siguen sus patrones y convenciones específicos. Esto es especialmente eficaz para crear implementaciones coherentes en el código base, lo que acelera el desarrollo de características al tiempo que mantiene los estándares de código. Basándose en el ejemplo anterior de disparo cero, podría proporcionar un ejemplo de una función de conversión de temperatura y, a continuación, pedir a Copilot que cree otra función similar. Así es como podría ser:

Captura de pantalla de Copilot con un ejemplo para crear código de conversión de temperatura similar.

Aprendizaje en pocos pasos
En este método, Copilot se presenta con varios ejemplos, que tienen un equilibrio entre la falta de seguridad de disparo cero y la precisión del ajuste fino. Este enfoque destaca por la generación de implementaciones sofisticadas que controlan varios escenarios y casos perimetrales, lo que reduce el tiempo invertido en pruebas manuales y refinamiento. Supongamos que quiere generar código que le envíe un saludo en función de la hora del día. Esta es una versión algo corta de una solicitud:

Captura de pantalla de Copilot que genera código de saludo basado en varios ejemplos.

Cadena de mensajes y administración del historial de chat
Al trabajar en funcionalidades complejas que requieren varios pasos, es posible que participe de conversaciones extendidas con el chat de GitHub Copilot. Aunque el contexto detallado ayuda a Copilot a comprender sus requisitos, mantener historiales de conversación largos puede ser ineficaz y costoso en términos de procesamiento.

Por ejemplo, puede empezar con una implementación básica y, a continuación, agregar iterativamente el control de errores, las pruebas, la documentación y las optimizaciones. Cada turno se basa en el contexto anterior, pero el historial completo se hace más extenso.

Turno 1: "Crear una función de autenticación de usuario" Turn 2: "Add error handling for invalid credentials" (Agregar control de errores para credenciales no válidas)
Turno 3: "Agregar pruebas unitarias para la función de autenticación" Turno 4: "Agregar comentarios JSDoc para documentar la función" Turno 5: "Optimizar la función para mejorar el rendimiento"

 Nota

Los avisos largos con el historial de conversaciones completo pueden consumir 2–3 PRU por turno. Resumir el contexto o restablecer la conversación puede mantenerlo más cerca de 1 PRU por solicitud.

Para administrar esto de forma eficaz:

Resumir el contexto cuando las conversaciones se vuelven largas: "En función de nuestra explicación anterior sobre la autenticación de usuarios, ahora agregue una limitación de velocidad para evitar ataques por fuerza bruta".
Restablecer y proporcionar contexto centrado para las nuevas características: comience con detalles esenciales en lugar de continuar toda la conversación
Usar referencias concisas al trabajo anterior en lugar de repetir implementaciones completas
Sugerencia de roles para tareas especializadas
La solicitud de roles implica indicar a GitHub Copilot que actúe como un tipo específico de experto, lo que puede mejorar significativamente la calidad y relevancia del código generado para dominios especializados. Este enfoque ayuda a acelerar el desarrollo al obtener soluciones más específicas en el primer intento.

Rol experto en seguridad
Al trabajar en características críticas para la seguridad, pida a Copilot que piense como un experto en seguridad:

"Actuar como experto en ciberseguridad. Cree una función de validación de contraseñas que compruebe si hay vulnerabilidades comunes y sigue las directrices de OWASP".

Este enfoque normalmente genera código que incluye:

Saneamiento de entrada
Protección contra ataques comunes
Patrones de validación estándar del sector
Procedimientos recomendados de seguridad
Rol de optimización del rendimiento
Para el código crítico para el rendimiento, use un rol experto en rendimiento:

"Actuar como experto en optimización del rendimiento. Refactorice este algoritmo de ordenación para controlar grandes conjuntos de datos de forma eficaz".

Esto suele dar lugar a:

Algoritmos optimizados y estructuras de datos
Implementaciones eficientes en memoria
Consideraciones sobre escalabilidad
Sugerencias de supervisión del rendimiento
Rol de especialista en pruebas
Al crear conjuntos de pruebas completos, aproveche una perspectiva de experto en pruebas:

"Actuar como especialista en pruebas. Cree pruebas unitarias completas para este módulo de procesamiento de pagos, incluidos los casos perimetrales y los escenarios de error".

Normalmente, esto genera:

Cobertura exhaustiva de pruebas
Gestión de casos extremos
Implementaciones ficticias
Pruebas de condición de error
La solicitud de roles le ayuda a preparar el código de producción más rápido mediante la incorporación de conocimientos de dominio en implementaciones iniciales, lo que reduce la necesidad de varios ciclos de revisión.

Ahora que sabe cómo Copilot usa sus avisos para aprender, echemos un vistazo detallado a cómo usa realmente la solicitud para sugerir código automáticamente.

## Flujo de proceso de solicitud de usuario de GitHub Copilot

En esta unidad desglosaremos cómo convierte GitHub Copilot los mensajes en código inteligente y utilizable. Por lo general, GitHub Copilot recibe solicitudes y devuelve sugerencias de código o respuestas en su flujo de datos. Este proceso sugiere un flujo de entrada y de salida.

Flujo de entrada:
Ilustración del flujo de entrada de GitHub Copilot.

Vamos a recorrer todos los pasos que sigue Copilot para procesar el mensaje de un usuario en una sugerencia de código.

1. Transmisión segura de solicitudes y recopilación de contexto
El proceso comienza con la transmisión segura del mensaje del usuario a través de HTTPS. Así se garantiza que el comentario en lenguaje natural se envíe a los servidores de GitHub Copilot de forma segura y confidencial, protegiendo la información confidencial.

GitHub Copilot recibe de forma segura el mensaje del usuario, que podría ser un chat de Copilot o un comentario en lenguaje natural que haya proporcionado dentro del código.

Simultáneamente, Copilot recopila detalles de contexto:

El código anterior y posterior a la posición del cursor, lo que le ayuda a comprender el contexto inmediato del mensaje.
El nombre y tipo del archivo que se está editando, lo que le permite adaptar las sugerencias de código al tipo de archivo específico.
Información sobre las pestañas abiertas adyacentes, garantizando que el código generado se alinee con otros segmentos de código del mismo proyecto.
Información sobre la estructura del proyecto y las rutas de acceso de los archivos
Información sobre lenguajes y marcos de programación
Preprocesamiento mediante la técnica Fill-in-the-Middle (FIM) para tener en cuenta tanto el contexto del código anterior como el siguiente, ampliando de forma efectiva la comprensión del modelo y permitiendo a Copilot generar sugerencias de código más precisas y relevantes aprovechando un contexto más amplio.
Estos pasos convierten la solicitud de alto nivel del usuario en una tarea de codificación concreta.

2. Filtro de proxy
Una vez recopilado el contexto y creada la solicitud, este pasa de forma segura a un servidor proxy hospedado en un inquilino de Microsoft Azure propiedad de GitHub. El proxy filtra el tráfico, bloqueando los intentos de piratear la solicitud o manipular el sistema para revelar detalles sobre cómo el modelo genera sugerencias de código.

3. Filtrado de toxicidad
Copilot incorpora mecanismos de filtrado de contenido antes de continuar con la extracción de intenciones y la generación de código, para asegurarse de que el código y las respuestas generados no incluyan o promuevan:

Discursos de odio y contenido inapropiado: Copilot emplea algoritmos para detectar y prevenir la ingesta de discursos de odio, lenguaje ofensivo o contenido inapropiado que pueda resultar dañino u ofensivo.
Datos personales: Copilot filtra activamente los datos personales, como nombres, direcciones o números de identificación, para proteger la privacidad del usuario y la seguridad de los datos.
4. Generación de código con LLM
Por último, la solicitud filtrada y analizada se pasa a modelos de LLM, que generan sugerencias de código adecuadas. Estas sugerencias se basan en la comprensión de la solicitud y el contexto circundante de Copilot, lo que garantiza que el código generado sea relevante, funcional y se ajuste a los requisitos específicos del proyecto.

Flujo de salida:
Ilustración del flujo de salida de GitHub Copilot.

5. Procesamiento posterior y validación de las respuestas
Una vez que el modelo genera sus respuestas, el filtro de toxicidad elimina cualquier contenido generado dañino u ofensivo. A continuación, el servidor proxy aplica una capa final de comprobaciones para garantizar la calidad, la seguridad y los estándares éticos del código. Estas comprobaciones incluyen:

Calidad del código: Las respuestas se comprueban para detectar errores o vulnerabilidades comunes, como scripting entre sitios (XSS) o inyección SQL, garantizando que el código generado sea sólido y seguro.
Código público coincidente (opcional): Opcionalmente, los administradores pueden habilitar un filtro que evita que Copilot devuelva sugerencias de más de ~150 caracteres si se parecen mucho al código público existente en GitHub. Así se evita que las coincidencias se sugieran como contenido original. Si alguna parte de la respuesta no supera estas comprobaciones, se trunca o se descarta.
6. Entrega de sugerencias e inicio del bucle de retroalimentación
Solo las respuestas que pasan todos los filtros se entregan al usuario. A continuación, Copilot inicia un bucle de retroalimentación basado en sus acciones para lograr lo siguiente:

Ampliar sus conocimientos a partir de sugerencias aceptadas.
Aprender y mejorar gracias a las modificaciones y rechazos de sus sugerencias.
7. Repetición para solicitudes posteriores
El proceso se repite a medida que proporciona más mensajes, y Copilot controla continuamente las solicitudes de usuario, comprende su intención y genera código en respuesta. Con el tiempo, Copilot aplica los datos acumulados de las interacciones y los comentarios, incluidos los detalles de contexto, para mejorar su comprensión de la intención del usuario y refinar sus funcionalidades de generación de código.

## Datos de GitHub Copilot

En esta unidad, trataremos cómo GitHub Copilot controla los datos de diferentes entornos, características y configuraciones.

Control de datos para sugerencias de código de GitHub Copilot
GitHub Copilot en el editor de código no conserva ninguna solicitud como código u otro contexto usado con el fin de proporcionar sugerencias para entrenar los modelos fundamentales. Descarta las solicitudes una vez que se devuelve una sugerencia.

Los suscriptores individuales de GitHub Copilot pueden optar por no compartir sus solicitudes con GitHub, que se usarán para perfeccionar el modelo fundamental de GitHub.

Control de datos para el chat de GitHub Copilot
El chat de GitHub Copilot funciona como una plataforma interactiva, lo que permite a los desarrolladores entablar interacciones conversacionales con el asistente de IA para recibir asistencia de codificación. Estos son los pasos que lleva a cabo, que pueden ser distintos de otras características, como la finalización del código:

Formato: Copilot formatea meticulosamente la respuesta generada para una presentación óptima dentro de la interfaz de chat. Resalta los fragmentos de código para mejorar la legibilidad y puede incluir opciones para la integración directa en el código. Copilot muestra la respuesta formateada en la ventana de chat de Copilot dentro del IDE, lo que le permite revisar e interactuar fácilmente con la información proporcionada.
Interacción del usuario: Puede interactuar activamente con la respuesta haciendo preguntas de seguimiento, solicitando aclaraciones o proporcionando una entrada adicional. La interfaz de chat mantiene un historial de conversaciones para facilitar la comprensión contextual en las interacciones posteriores.
Retención de datos: En el caso del chat de Copilot usado fuera del editor de código, GitHub normalmente conserva solicitudes, sugerencias y contexto auxiliar durante 28 días. Las directivas de retención específicas para el chat de Copilot en el editor de código pueden variar.
Lo mismo sucede con la CLI, Móvil y el chat de GitHub Copilot en GitHub.com.

Tipos de aviso admitidos por el chat de GitHub Copilot
El chat de GitHub Copilot procesa una amplia gama de solicitudes relacionadas con la codificación, demostrando su versatilidad como asistente de codificación conversacional. Estos son algunos tipos de entrada comunes:

Preguntas directas: Puede formular preguntas específicas sobre conceptos de codificación, bibliotecas o problemas de solución de problemas. Por ejemplo, "¿Cómo implemento un algoritmo de ordenación rápida en Python?" o "¿Por qué no se representa mi componente de React?"
Solicitudes relacionadas con el código: Puede solicitar la generación, modificación o explicación del código. Algunos ejemplos incluyen "Escriba una función para calcular el factorial", "Corrija este error en mi código" o "Explique este fragmento de código".
Consultas abiertas: Puede explorar los conceptos de codificación o buscar instrucciones generales haciendo preguntas abiertas como "¿Cuáles son los procedimientos recomendados para escribir código limpio?" o "¿Cómo puedo mejorar el rendimiento de mi aplicación de Python?"
Solicitudes contextuales: Puede proporcionar fragmentos de código o describir escenarios de codificación específicos para buscar asistencia personalizada. Por ejemplo, "Esta es una parte de mi código, ¿puede sugerir mejoras?" o "Estoy creando una aplicación web, ¿puede ayudarme con el flujo de autenticación?"
La capacidad del chat de Copilot para procesar diversos tipos de entradas aumenta su utilidad como compañero de codificación integral.

Ventanas de contexto limitadas
Ilustración de la ventana de contexto de GitHub Copilot.

Aunque el chat de GitHub Copilot es excelente a la hora de comprender y responder a las solicitudes, es esencial reconocer la limitación de las ventanas de contexto. Esto hace referencia a la cantidad de código circundante y texto que el modelo puede procesar simultáneamente para generar sugerencias. La ventana de contexto de GitHub Copilot suele oscilar entre aproximadamente 200 y 500 líneas de código o hasta unos miles de tokens. Esta limitación puede variar en función de la implementación y de la versión específicas de Copilot que se use.

El chat de Copilot funciona actualmente con una ventana de contexto de 4000 tokens, lo que proporciona un mayor alcance para comprender y responder a las consultas de los usuarios en comparación con Copilot estándar.

A pesar de estos avances, debe tener en cuenta las limitaciones de la ventana de contexto al elaborar solicitudes. Desglosar problemas complejos en consultas más pequeñas y específicas o proporcionar fragmentos de código relevantes puede mejorar significativamente la capacidad del modelo para ofrecer respuestas precisas y útiles.

## Modelos de lenguaje grande (LLM) de GitHub Copilot

GitHub Copilot cuenta con la tecnología de modelos de lenguaje grande (LLM) para ayudarle a escribir código sin problemas. En esta unidad, nos centraremos en comprender la integración y el impacto de las VM en GitHub Copilot. Vamos a revisar los siguientes temas:

¿Qué son los LLM?
El rol de las VM en GitHub Copilot y las solicitudes
Ajuste de los LLM
Optimización de LoRA
¿Qué son los LLM?
Los modelos de lenguaje grande (LLM) son modelos de inteligencia artificial diseñados y entrenados para comprender, generar y manipular el lenguaje humano. Estos modelos están engrasados con la capacidad de controlar una amplia gama de tareas que implican texto, gracias a la amplia cantidad de datos de texto en los que se entrenan. Estos son algunos aspectos básicos para comprender sobre los LLM:

Volumen de datos de entrenamiento
Las LLM se exponen a grandes cantidades de texto de diversos orígenes. Esta exposición les equipa con una amplia comprensión del lenguaje, el contexto y las complejidades implicadas en diversas formas de comunicación.

Descripción contextual
Se destacan en la generación de texto contextualmente relevante y coherente. Su capacidad de comprender el contexto les permite proporcionar contribuciones significativas, ya sea completando oraciones, párrafos o incluso generando documentos completos que son contextualmente aptos.

Integración del aprendizaje automático y la inteligencia artificial
Los LLM se basan en los principios de aprendizaje automático e inteligencia artificial. Son redes neuronales con millones o incluso miles de millones de parámetros que están ajustados durante el proceso de entrenamiento para comprender y predecir texto de forma eficaz.

Versatilidad
Estos modelos no se limitan a un tipo específico de texto o lenguaje. Se pueden adaptar y ajustar para realizar tareas especializadas, por lo que son muy versátiles y aplicables en varios dominios e idiomas.

Rol de los LLM en GitHub Copilot y solicitudes
GitHub Copilot utiliza LLM para proporcionar sugerencias de código compatibles con el contexto. El LLM considera no solo el archivo actual, sino también otros archivos abiertos y pestañas en el IDE para generar finalizaciones de código precisas y pertinentes. Este enfoque dinámico garantiza sugerencias adaptadas, lo que mejora la productividad.

Ajuste de los LLM
El ajuste preciso es un proceso crítico que nos permite adaptar modelos de lenguaje grandes (LLM) entrenados previamente para tareas o dominios específicos. Implica entrenar el modelo en un conjunto de datos más pequeño y específico de tareas, conocido como conjunto de datos de destino, mientras se usan los conocimientos y parámetros obtenidos de un conjunto de datos entrenado previamente grande, denominado modelo de origen.

Diagrama que muestra cómo se usa el ajuste preciso en modelos de lenguaje grande.

La optimización es esencial para adaptar las LLM para tareas específicas, lo que mejora su rendimiento. Sin embargo, GitHub lo llevó un paso más allá mediante el método de ajuste fino de LoRA, que analizaremos a continuación.

Optimización de LoRA
La optimización completa tradicional significa entrenar todas las partes de una red neuronal, lo que puede ser lento y muy dependiente de los recursos. Pero LoRA (adaptación de baja clasificación) es una alternativa inteligente. Se usa para que los modelos de lenguaje grande (LLM) preentrenados funcionen mejor para tareas específicas sin rehacer todo el entrenamiento.

Así es como funciona LoRA:

LoRA agrega partes entrenables más pequeñas a cada capa del modelo entrenado previamente en lugar de cambiar todo.
El modelo original sigue siendo el mismo, lo que ahorra tiempo y recursos.
Lo mejor de LoRA:

Supera a otros métodos de adaptación como adaptadores y ajuste de prefijos.
Es como obtener excelentes resultados con menos partes móviles.
En términos sencillos, el ajuste de la precisión de LoRA consiste en trabajar de forma más inteligente, no más difícil, para mejorar los LLM para sus requisitos de codificación específicos al usar Copilot.

## Resumen
En este módulo, revelamos las complejidades de la optimización de GitHub Copilot mediante indicaciones eficaces. Aprovechar el potencial máximo de la herramienta se encuentra en el arte y la ciencia de la ingeniería de solicitudes. Ahora, estás equipado con aptitudes y conocimientos refinados para mejorar tu experiencia de codificación y los resultados. Después de completar este módulo, habrá aprendido a:

Principios de creación de solicitudes, procedimientos recomendados y cómo aprende GitHub Copilot de las solicitudes para proporcionar respuestas contextuales. El flujo subyacente de cómo GitHub Copilot procesa las solicitudes de usuario para generar respuestas o sugerencias de código. El flujo de datos para sugerencias de código y chat en GitHub Copilot. LLM y su rol en GitHub Copilot y preguntar. Procedimiento para crear solicitudes eficaces que optimicen el rendimiento de GitHub Copilot, lo que garantiza la precisión y la relevancia en cada sugerencia de código. La relación intrincada entre las solicitudes y las respuestas de Copilot. Cómo Copilot gestiona los datos de las solicitudes en diferentes situaciones, incluida la transmisión segura de datos y el filtrado de contenido.

Referencias
Dentro de GitHub: Trabajar con los modelos de lenguaje de gran tamaño (LLM) detrás de GitHub Copilot - El Blog de GitHub
Uso de GitHub Copilot: Mensajes, sugerencias y casos de uso: el blog de GitHub
Cómo gitHub copilot controla los datos
Envío de comentarios
Use este formulario de problema para proporcionar comentarios de contenido o cambios sugeridos para este módulo de Microsoft Learn. GitHub mantiene este contenido y un miembro del equipo evaluará la solicitud. Gracias por darse el tiempo de mejorar nuestro contenido.
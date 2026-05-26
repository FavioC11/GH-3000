# Introducción a Copilot Spaces
## Introducción
GitHub Copilot Spaces proporciona una nueva manera de trabajar con inteligencia artificial anclando sus respuestas en un contexto cuidadosamente mantenido. A diferencia del chat general de Copilot, que muestra sugerencias amplias, un espacio le permite centrar el modelo en archivos específicos, problemas, solicitudes de incorporación de cambios e instrucciones adaptadas. En esta unidad se presenta lo que es un espacio, cómo funciona y por qué restringir el contexto conduce a respuestas más coherentes y reproducibles. También aprenderá a establecer un contexto efectivo mediante datos adjuntos e instrucciones de texto libre, y cuándo es mejor usar Spaces sobre el chat general.

En esta unidad, aprenderá lo siguiente:

Qué son los espacios de Copilot de GitHub y cómo difieren del chat general de Copilot
¿Por qué un contexto bien delimitado mejora la calidad y la coherencia de las respuestas?
Cómo adjuntar archivos, problemas e instrucciones para guiar el modelo
Cuándo crear un espacio para tareas repetibles y específicas del dominio
¿Qué es un espacio de Copilot de GitHub?
Captura de pantalla que muestra el aspecto de una página de espacios de ejemplo para una aplicación de viaje.

Es un chat de Copilot dedicado, fundamentado en un conjunto curado de contextos de su elección. El espacio es como un LLM y puede alimentar archivos de GitHub, problemas, solicitudes de incorporación de cambios y sus propias instrucciones de texto libre para proporcionar contexto a su tema específico.

Configurar el contexto para los espacios de Copilot
Captura de pantalla que muestra un chat dedicado de Copilot basado en un conjunto seleccionado de contexto que elija.

La eficacia de un Espacio de Copilot depende del contexto que proporciones. Puede adjuntar archivos específicos (como scripts, configuración o documentación), problemas relevantes o solicitudes de incorporación de cambios e instrucciones adaptadas. Al organizar esta entrada, ayuda a Copilot a centrarse en la información que es más relevante para su escenario. El orden de contexto es importante: comenzar con los archivos o instrucciones más importantes ayuda a impulsar respuestas más precisas y relevantes.

Configuración: Adjuntar archivos (subidas) e instrucciones en Copilot Spaces
Adjuntar archivos (cargas):

En la configuración del espacio, use el botón "Adjuntar archivos" o "Agregar contexto" para seleccionar uno o varios archivos del repositorio de GitHub.
Puede adjuntar archivos de código fuente, documentos de Markdown, archivos de configuración u otros recursos como contexto. Estos archivos están referenciados desde la rama predeterminada, así que tu espacio se mantiene actualizado a medida que evoluciona tu repositorio.
Si la configuración del área de trabajo lo permite, también puede cargar archivos directamente (como imágenes o conjuntos de datos) desde la máquina local para el contexto que no sea de repositorio.
Agregar instrucciones:

Captura de pantalla que muestra el icono de instrucciones y las opciones para agregar instrucciones a los espacios.

Use la sección "Instrucciones" para proporcionar instrucciones específicas a Copilot. Esto puede incluir objetivos ("Resumir el proceso de incorporación"), preferencias de estilo ("Escribir en un tono formal") o ejemplos canónicos ("La salida de ejemplo debe ser similar a...").
Mantenga las instrucciones breves, centradas y accionables. Si el espacio sirve un flujo de trabajo o una guía de solución de problemas, incluya tareas paso a paso o mensajes de ejemplo.
Puede actualizar las instrucciones en cualquier momento para refinar el enfoque de su espacio.
El momento ideal para usar y crear un Espacio de GitHub Copilot
Use un espacio cuando desee respuestas coherentes y reproducibles en un tema de ámbito estricto, como un servicio determinado, un runbook o un cuaderno de estrategias, o un conjunto de datos conocido. En comparación con el chat general o en todo el repositorio, Espacios intercambia amplitud por profundidad: al restringir el contexto a lo que más importa, tienden a producir respuestas más predecibles y fundamentadas, mientras que un chat amplio puede permitir una detección más amplia, pero puede ser menos precisa.

Algunas directrices prácticas mejoran la calidad. Se aplican límites de contexto de modelo, por lo que es importante mantener los espacios pequeños y enfocados. Los archivos de GitHub vinculados reflejan la rama predeterminada del repositorio, lo que ayuda a mantener el contenido al día a medida que evoluciona el código. Tenga claro y conciso con sus instrucciones e incluya algunos ejemplos canónicos para delimitar el estilo y las salidas esperadas. Por último, recuerde que la selección y la ordenación del contexto pueden influir en las respuestas, así que comience con sus fuentes más importantes.

## Creando tu primer espacio
Crear un espacio es sencillo pero eficaz, una vez con nombre y configurado, se convierte en un área de trabajo reutilizable donde Copilot opera dentro de un ámbito claramente definido. En esta unidad, le guiará por cómo crear su primer espacio, decidir la propiedad y la visibilidad, y rellenarla con contexto significativo. También explorará diferentes formas de agregar archivos, problemas y notas de texto libre para admitir interacciones precisas y fundamentadas.

En esta unidad, aprenderá lo siguiente:

Cómo crear un espacio y darle un nombre claro para facilitar su descubrimiento
La diferencia entre espacios personales y de propiedad de la organización
Cómo agregar y estructurar contexto a través de datos adjuntos e instrucciones
¿Por qué la organización y la claridad mejoran las respuestas de Copilot?
Creación de un espacio
Para crear un espacio, vaya a https://github.com/copilot/spacesy haga clic en Crear espacio.

Asigne un nombre al espacio.

Elija si el espacio es propiedad de usted o de una organización a la que pertenece. Los espacios propiedad de la organización se pueden compartir mediante el modelo de permisos integrado de GitHub.

Opcionalmente, agregue una descripción. Esto no afecta a las respuestas que Copilot proporciona en el espacio, pero puede ayudar a otros usuarios a comprender el contexto del espacio.

 Nota

Puede cambiar el nombre y la descripción del espacio en cualquier momento haciendo clic en Editar en la esquina superior derecha del espacio.

Haga clic en Guardar en la esquina superior derecha de la página.

Agregar contexto a un espacio Puede agregar dos tipos de contexto al espacio:

Instrucciones: Texto libre que describe lo que Copilot debe centrarse dentro de este espacio. Incluya sus áreas de experiencia, con qué tipos de tareas debe ayudar y qué debe evitar. Esto ayuda a Copilot a proporcionar respuestas más relevantes en función de su intención.

Accesorios: Este contexto se usa para proporcionar respuestas más relevantes a sus preguntas. Además, Spaces siempre hace referencia a la versión más reciente del código en la rama principal del repositorio.

Para agregar datos adjuntos, haga clic en Agregar a la derecha de "Datos adjuntos" y elija una de las siguientes opciones:

Adjuntar archivos y carpetas: puede agregar archivos y carpetas desde los repositorios de GitHub. Esto incluye archivos de código, documentación y otro contenido relevante que puede ayudar a Copilot a comprender el contexto del espacio.
Vincular solicitudes de incorporación de cambios y problemas: puede pegar las direcciones URL de los problemas de GitHub y las solicitudes de incorporación de cambios.
Cargar un archivo: puede cargar archivos directamente desde la máquina local. Esto incluye imágenes, archivos de texto, documentos enriquecidos y hojas de cálculo.
Agregar contenido de texto: puede escribir o pegar contenido de texto libre, como transcripciones, notas o cualquier otra información relevante que pueda ayudar a Copilot a comprender el contexto del espacio.
¡Felicidades! ¡Acabas de crear un espacio!

## Uso compartido, detectabilidad y gobernanza
Para garantizar que el espacio ofrezca un valor duradero, debe ser fácil de encontrar, compartir de forma segura y bien mantenido. Esta unidad se centra en cómo administrar la visibilidad, seguir los permisos de GitHub y mantener el contenido actualizado a medida que evoluciona el código base. También aprenderá estrategias de gobernanza ligeras, desde asignar la propiedad y añadir instrucciones de uso hasta configurar una cadencia de revisión, para asegurarse de que su espacio sea preciso, fácilmente localizable y alineado con las necesidades del equipo.

En esta unidad, aprenderá lo siguiente:

Administración de la visibilidad y el uso compartido dentro de la organización
Protección de los permisos de GitHub y control del acceso al contenido vinculado
Por qué las convenciones de nomenclatura y las descripciones aumentan la detectabilidad
Procedimientos recomendados para la propiedad del espacio, la actualización y los ciclos de revisión
Visibilidad y uso compartido
Espacios exitosos son fáciles de encontrar, seguros para compartir y claramente "propiedad". Al crear un espacio, establezca la visibilidad según la amplitud con la que piensa que otras personas la usen. En función de su entorno, las opciones pueden incluir mantenerla bajo su propiedad personal o hacer que sea visible para su organización.

Comparta el espacio por vínculo y, cuando esté disponible, confíe en la exploración de nivel de organización o catálogos para mejorar la detectabilidad. Use un título claro, controlado por propósitos y una breve descripción que indique el ámbito ("un trabajo por espacio"), audiencia prevista y salidas esperadas para que los compañeros de equipo sepan inmediatamente cuándo usarlo.

Seguridad y acceso
La seguridad sigue los permisos existentes de GitHub. Un espacio no concede acceso nuevo; solo expone el contenido que los espectadores ya tienen derecho a ver. Si un espacio vincula a repositorios privados, problemas o solicitudes de incorporación de cambios, solo los usuarios con los permisos de repositorio adecuados ven ese material reflejado en las respuestas. Esto le ayuda a compartir con confianza en una organización mientras mantiene la información confidencial protegida. Como procedimiento recomendado, evite pegar datos confidenciales en notas de texto libre; prefiere la vinculación a archivos controlados por versiones en los que se aplican la revisión y los permisos normales.

Versionado y actualización constante
Los espacios permanecen actualizados haciendo referencia a orígenes de GitHub en directo. Los archivos vinculados reflejan la rama predeterminada del repositorio y los problemas adjuntos y las solicitudes de incorporación de cambios evolucionan a medida que cambian, lo que reduce la necesidad de copiar contenido en documentos independientes. Si necesita instrucciones específicas de la rama o una instantánea histórica, considere la posibilidad de restringir las referencias a los archivos pertinentes, agregar un breve ejemplo en texto libre o, si se admite en su entorno, adjuntar un archivo de texto que capture el contenido exacto que desea que use el espacio. Mantenga el ámbito pequeño para que las actualizaciones sigan siendo predecibles y con base.

Governance
Trate la gobernanza como ligera pero intencionada. Asigne un propietario que mantenga el Espacio, añada una breve nota titulada "Cómo usar este Espacio" en la parte superior de las instrucciones e incluya de 1 a 3 ejemplos canónicos que definan una salida "buena". Establezca convenciones de nomenclatura (por ejemplo, "ServiceName— Onboarding Helper") y revise la cadencia (por ejemplo, en cada versión) para eliminar orígenes obsoletos y mantener las instrucciones alineadas con la realidad. Cuando un espacio crece más allá de un solo trabajo, divídalo en espacios más pequeños para que la facilidad de descubrimiento permanezca alta y la calidad de las respuestas siga siendo coherente.

Use esta lista de comprobación al crear o actualizar un espacio para que sea fácil de encontrar, proteger y compartir de forma confiable. Las opciones (por ejemplo, propiedad de la organización, subidas) pueden variar según el entorno.

Nomenclatura y propósito

[ ] Elija un título claro y orientado a un propósito (por ejemplo, "ServiceName—Onboarding Helper"); mantenga "un trabajo por espacio".
[ ] Escriba una descripción de oración de 1 a 2 que indique el ámbito, la audiencia prevista y las salidas esperadas.
[ ] Agregue una breve nota sobre cómo usar este espacio en la parte superior de las instrucciones.
Propiedad y visibilidad

[ ] Establezca el propietario correcto (individual o organización, si está disponible).
[ ] Seleccione la visibilidad adecuada (privada, visible para la organización, etc.).
[ ] Verifique el acceso con un usuario que no sea propietario y que esperara permisos de GitHub (los espacios heredan permisos de repositorio, problema o PR).
[ ] Comparta la dirección URL y, cuando esté disponible, agregue colaboradores.
Seguridad y privacidad

[ ] No pegue datos confidenciales en texto libre; prefiere vincular archivos controlados por versiones en los que se aplican revisiones y permisos normales.
[ ] Asegúrese de que todos los orígenes adjuntos son adecuados para la visibilidad elegida.
[ ] Si se admiten cargas, limite el contenido de texto que le resulte cómodo compartir.
[ ] Quitar materiales obsoletos o confidenciales.
Detectabilidad y documentos

[ ] Use convenciones de nomenclatura coherentes en Espacios (ayuda de prefijos de equipo o servicio).
[ ] Agregue etiquetas o palabras clave en la descripción para ayudar a la búsqueda.
[ ] Anuncie o cataloge el espacio en el directorio o canal preferidos de la organización.
Revisión de cadencia y gobernanza

[ ] Asigne un mantenedor o propietario responsable de las actualizaciones.
[ ] Establezca una cadencia de revisión (por ejemplo, mensual o por versión).
[ ] En cada revisión: valide los vínculos, pruebe 2–3 indicaciones representativas, actualice los ejemplos, recorte fuentes ruidosas y confirme la visibilidad.
[ ] Realice un seguimiento de los comentarios y las solicitudes de mejora (problemas, discusión o una lista de comprobación sencilla en la descripción).

## Lo que debes y no debes hacer al trabajar en un espacio
Mantenga sus preguntas estrechamente limitadas a los orígenes adjuntos (archivos, problemas, solicitudes de incorporación de cambios y notas), por lo que las respuestas permanecen fundamentadas.

No mencione a personas ni a otras extensiones de Copilot en un espacio: las menciones del usuario no notificarán a nadie y las extensiones no se pueden invocar desde chats de espacio.

Trate el espacio como un entorno centrado para una sola tarea o dominio y reutilice su propia terminología para reforzar la coherencia.

Use patrones de solicitud que conducen a salidas ejecutables y verificables. Empiece por confirmar la intención y, a continuación, refinar con restricciones concretas (formatos, intervalos de tiempo, rutas de acceso de archivo o secciones que se deben tener en cuenta). Pida código ejecutable, consultas o comandos y, cuando sea útil, solicite referencias a los orígenes incluidos para la rastreabilidad.

No espere que Space extraiga contenido que no esté incluido; a menos que su entorno admita la búsqueda en un repositorio que haya asociado explícitamente, Copilot no descubrirá material externo.

Iterar cuando las respuestas se desvíen: ajustar las instrucciones, agregar entre uno y tres ejemplos de alta calidad que demuestran una salida "buena" y eliminar orígenes ruidosos o irrelevantes.

No deje que el Espacio se expanda más allá de un solo trabajo ni supere los límites de contexto del modelo; si encuentra advertencias de tamaño o respuestas reducidas en calidad, reduzca los orígenes o divida en espacios más pequeños para restaurar la precisión y la previsibilidad.

Mantenga el contexto fresco y bien ordenado. Vincule archivos controlados por versiones para que el espacio refleje la rama predeterminada del repositorio a medida que evoluciona y dirija con los orígenes o ejemplos más importantes, ya que la ordenación puede influir en las respuestas.

No pegue datos confidenciales en notas de texto libre; prefiera enlazar a archivos en repositorios (o usar subidas donde se permita) para que se apliquen permisos y revisión estándares.

## Ejercicio: Democratización del conocimiento tribal mediante Copilot Spaces
En este ejercicio, aprenderá a:

Agregar un repositorio como origen al espacio de Copilot
Exploración y resumen de la documentación del proceso de administración de proyectos
Creación y uso de modos de chat personalizados para el análisis profundo de procesos
Actualización de la documentación del repositorio en función de la información detectada
Cómo empezar
Al seleccionar el botón Iniciar el ejercicio en GitHub siguiente, se le dirigirá a un repositorio de plantillas de GitHub público que le pedirá que complete una serie de pequeños desafíos. Cuando haya terminado el ejercicio en GitHub, vuelva aquí para: Una comprobación rápida de conocimientos. Un resumen de lo que ha aprendido. Un distintivo por completar este módulo.

Inicio del ejercicio en GitHub
https://github.com/skills/democratize-tribal-knowledge-using-copilot-spaces

## Resumen
GitHub Copilot Spaces ofrece un valor empresarial significativo al permitir que los equipos logren resultados más rápidos y precisos a través de la asistencia de inteligencia artificial en contexto. Al seleccionar un conjunto centrado de orígenes, como archivos de código, documentación, problemas y solicitudes de incorporación de cambios, Espacios reducen la ambigüedad y mejoran la previsibilidad y la calidad de las respuestas de Copilot. Este enfoque dirigido minimiza el trabajo, acelera la toma de decisiones y garantiza que los resultados se alineen con los estándares de la organización. Los espacios también mejoran la colaboración y la gobernanza aprovechando el modelo de permisos existente de GitHub, lo que facilita compartir el conocimiento de forma segura a la vez que se mantiene el cumplimiento. En última instancia, Copilot Spaces ayuda a las organizaciones a escalar la experiencia, reducir la carga cognitiva y mejorar la productividad en los flujos de trabajo operativos y de desarrollo.

Ahora debería ser capaz de hacer lo siguiente:

Explicar qué son los espacios y cuándo usarlos frente al chat general de Copilot
Creación, configuración e iteración en un espacio con contexto de destino e instrucciones personalizadas
Aplicación de procedimientos recomendados para respuestas basadas y de alta calidad dentro de los límites del contexto del modelo
Aprende más
Aquí tiene algunos vínculos para obtener más información sobre los temas analizados en este módulo.

¿Qué es GitHub Copilot?
¿Qué es GitHub Copilot Spaces? Centraliza el contexto de tu proyecto | Checkout de GitHub
Proporcionar comentarios
Use este formulario de problema para proporcionar comentarios de contenido o cambios sugeridos para este módulo de Microsoft Learn. GitHub mantiene este contenido y un miembro del equipo evaluará la solicitud. Gracias por darse el tiempo de mejorar nuestro contenido.

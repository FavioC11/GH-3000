# Mejorar las revisiones de código y los pull requests con GitHub Copilot
## Introducción
Las revisiones de código son fundamentales para mantener la calidad y la colaboración del código, pero a menudo crean cuellos de botella. Los desarrolladores alternan ciclos de revisión largos, comentarios incoherentes y dificultades para proporcionar sugerencias accionables, especialmente en varios lenguajes y marcos. Los errores pequeños pueden pasar desapercibidos y las solicitudes de incorporación de cambios pueden tardar días en fusionarse.

GitHub Copilot ayuda a resolver estos desafíos actuando como revisor colaborativo y asistente. No reemplaza a los seres humanos, sino que trabaja junto a ellos detectando problemas, sugiriendo mejoras, redactando resúmenes e incluso corrigiendo automáticamente vulnerabilidades. También puede personalizar Copilot con sus propias directrices de revisión, por lo que busca los mismos patrones y estándares que le interesan como revisor humano. Esto significa que Copilot no solo acelera las revisiones, sino que también aplica los procedimientos recomendados de su equipo de forma coherente entre repositorios. El resultado es revisiones más rápidas, mayor calidad y menos carga cognitiva para los equipos.

Las unidades de solicitud Premium (PRU) potencian las funcionalidades más avanzadas de Copilot. Cada vez que pida a Copilot que realice una tarea de nivel premium, como revisar una solicitud de incorporación de cambios completa, ejecutarse en modo agente o generar sugerencias complejas de varios pasos, consume una PRU. Estas solicitudes Premium proporcionan a Copilot la potencia de procesamiento adicional y la profundidad del contexto que necesita para ofrecer un razonamiento más completo, comprobaciones de procedimientos recomendados más fuertes y salidas más confiables. Más adelante en el curso, aprenderá a supervisar el uso de PRU, optimizar el plan y sacar el máximo partido de cada solicitud premium.

Objetivos de aprendizaje
Al término de este módulo, sabrá hacer lo siguiente:

Explicar cómo GitHub Copilot simplifica las revisiones de código y las solicitudes de incorporación de cambios.
Identifique las características clave que Copilot agrega al proceso de revisión.
Solicite e interprete las revisiones de Copilot en GitHub.com y comprenda sus límites.
Ejecute las revisiones de Copilot localmente en el IDE y aplique instrucciones personalizadas.
Aproveche las unidades de solicitud Premium (PRU) para un análisis más profundo y enriquecido del contexto.
Automatice las revisiones de Copilot entre repositorios con conjuntos de reglas y comprobaciones de estado.
Aplique las sugerencias de Copilot de forma responsable, combinándolas con el juicio humano y las pruebas.
Prerrequisitos
Una cuenta de GitHub
GitHub Copilot habilitado en su cuenta (se recomienda Copilot Pro, Copilot Pro+, Empresa o Enterprise para características completas de revisión de código).
Conocimientos básicos sobre las solicitudes de cambios y las revisiones de código, la creación de una solicitud de cambios, la inclusión de comentarios y la combinación de cambios.
Un entorno de desarrollo como Visual Studio Code o los IDE de JetBrains (opcional pero recomendado) si planea usar las revisiones de Copilot localmente antes de abrir solicitudes de cambios.

## Lo que GitHub Copilot agrega al proceso de revisión
Las revisiones de código y las revisiones de solicitudes de incorporación de cambios son esenciales para la calidad, pero también pueden llevar mucho tiempo y ser desiguales. A menudo, los desarrolladores manejan múltiples lenguajes, formatos incoherentes y grandes diferencias de versiones mientras intentan proporcionar comentarios reflexivos. GitHub Copilot ayuda a facilitar esta carga de trabajo actuando como revisor de colaboración y asistente. Detecta problemas comunes, redacta comentarios de revisión, resume las solicitudes de incorporación de cambios e incluso resalta los riesgos de seguridad, lo que proporciona a los revisores un punto de partida claro. Con las instrucciones de revisión personalizadas, puede guiar a Copilot para ver los mismos patrones que hace, lo que garantiza la coherencia entre equipos y repositorios.

Al final de esta unidad, podrás:

Identifique las características clave de Copilot en las revisiones de código.
Explicar cómo las PRU desbloquean las funcionalidades de revisión avanzada.
Reconocer diferentes formas en que la revisión de Copilot complementa y ayuda a los desarrolladores.
Características clave de Copilot en las revisiones de código
Copilot presenta varias características diseñadas para simplificar las revisiones:

Resúmenes de solicitudes de incorporación de cambios: Copilot puede redactar automáticamente descripciones de solicitudes de incorporación de cambios que incluyen un resumen claro de los cambios y una lista de archivos afectados. Esto garantiza que los revisores comiencen con el contexto, no con las estimaciones.

Correcciones de seguridad: Con la revisión de código de Copilot integrada en el análisis de código de GitHub, las vulnerabilidades se marcan en todos los lenguajes. Por ejemplo, en JavaScript, Copilot puede detectar una entrada sin sanitizar que se pasa a eval() y comentar:

"eval() con la entrada del usuario puede dar lugar a la inyección de código. Reemplácelo por un analizador seguro como JSON.parse(). Luego ofrece un parche en línea alineado con las pautas de seguridad de su repositorio.

Explicaciones de línea a línea: los revisores pueden resaltar el código y pedir a Copilot que explique la funcionalidad, lo que les ayuda a comprender rápidamente el código desconocido.

Redacción de comentarios: Copilot puede generar comentarios de revisión basados en procedimientos recomendados o directrices de equipo, haciendo que los comentarios sean claros y accionables.

Revisiones en el IDE: además de trabajar directamente en GitHub.com, Copilot también puede revisar el código dentro del IDE. Esto permite a los desarrolladores detectar y resolver problemas antes de abrir una solicitud de incorporación de cambios, acelerar el proceso y reducir el trabajo.

Descripción de cómo las PRU desbloquean las funcionalidades de revisión avanzada
Las PRU potencian estas funcionalidades avanzadas. Por ejemplo, la asignación de Copilot como revisor de solicitud de cambios utiliza un PRU cada vez que este comenta. Cuando se combina con archivos .github/copilot-instructions.md personalizados, las revisiones con tecnología de PRU se alinean con las reglas de su equipo, tanto si se centran en la legibilidad, la seguridad o el estilo.

Ejemplo:

Sin Copilot, una solicitud de modificación puede incluir comentarios imprecisos de un revisor como "Corregir aquí el problema de seguridad". Con la ayuda de Copilot + PRUs, la revisión se convierte en:

"El uso de exec() introduce una vulnerabilidad de inyección de código. Considere la posibilidad de reemplazarlo por subprocess.run() para una ejecución de comandos más segura. Aquí tienes un parche sugerido:

Además, proporciona la corrección de código en línea.

Cinco formas diferentes en que la revisión con Copilot ayuda a los desarrolladores
A continuación, revisaremos cómo La revisión de Copilot puede ayudarle a trabajar de forma más inteligente con:

Sugerencias de revisión de código
Revisiones de Copilot en varios idiomas
Dar formato a los datos en solicitudes de incorporación de cambios
Escribir resúmenes efectivos de solicitudes de cambios
Explicación y revisión del código
Uso de sugerencias de Copilot en las revisiones de código
Al revisar una solicitud de incorporación de cambios, es posible que detecte áreas que podrían mejorarse, pero no tiene el tiempo para redactar el ejemplo o fragmento perfecto usted mismo. GitHub Copilot ayuda a llenar esa brecha sin asumir el trabajo del autor. Dentro de la vista "Archivos modificados" de la solicitud de incorporación de cambios, puede resaltar una línea o bloque de código y pedir a Copilot que sugiera mejoras o marque posibles problemas. A continuación, Copilot genera una sugerencia concreta con reconocimiento del contexto que puede copiar en el comentario de revisión, lo que hace que sus comentarios sean más claros y fáciles para que el autor actúe.

Por ejemplo, al revisar un archivo de Ruby con lógica repetida, puede resaltar las líneas pertinentes y preguntar:

"Sugerir una refactorización de Ruby más limpia para este código repetido".

Copilot propondrá una versión actualizada que siga los procedimientos recomendados comunes de Ruby. Puede pegar su recomendación (o partes de ella) en el comentario de revisión junto con su propia explicación. Esto le mantiene centrado en la calidad general y el diseño, a la vez que proporciona al autor comentarios accionables y de alto valor, sin desdibujar la línea entre revisar y codificar por él.

Revisión en varios idiomas
Al solicitar una revisión de código, Copilot puede resaltar automáticamente las áreas que no siguen los procedimientos recomendados ni las directrices del equipo.

Copilot generará rápidamente mejoras que se alinean con las convenciones del lenguaje, lo que le permite proporcionar comentarios de revisión más sólidos y precisos incluso fuera de su área principal de experiencia.

Captura de pantalla de una solicitud de incorporación de cambios de GitHub que muestra una sugerencia de código para reemplazar una declaración de variable por una declaración de variable corta en un programa de Go.

Dar formato a los datos de las solicitudes de incorporación de cambios
Las solicitudes de incorporación de cambios son mucho más claras cuando incluyen contexto con formato correcto, como métricas, capturas de pantalla o resultados de pruebas. Sin embargo, los equipos a menudo olvidan dar formato a este contenido de forma coherente. GitHub Copilot puede actuar como un segundo conjunto de ojos durante la revisión del código, marcando automáticamente las tablas con formato deficiente en una descripción de la solicitud de incorporación de cambios y proponiendo una versión más limpia que se alinea con las directrices de estilo de su empresa.

Ejemplo: un desarrollador envía una solicitud de incorporación de cambios con la siguiente tabla de tiempos de carga de páginas. Es difícil de leer y no sigue la guía de estilo de Markdown del equipo.

Ejecución de pruebas	TiempoDeCargaPrevio	LoadTimeAfter
1.3	1.2
1.2	1.1
1.1	0.885
1.3	1.3
1.2	0.918
Average	1,22	1.0806
Durante la revisión, Copilot publica un comentario:

"Esta tabla no sigue las directrices de Markdown del repositorio. Esta es una versión limpia basada en la guía de estilo de su empresa".

Además, incluye una versión corregida lista para pegarla en la descripción de la solicitud de cambios:

Ejecución de pruebas	Tiempo de carga previo (segundos)	Tiempo de carga después de actualizaciones (segundos)
1	1.3	1.2
2	1.2	1.1
3	1.1	0.885
4	1.3	1.3
5	1.2	0.918
Promedio	1.22	1.0806
El revisor puede aceptar la sugerencia de Copilot con un solo clic, asegurándose de que la solicitud de cambios sigue el estilo de la empresa sin dedicar tiempo a cambiar el formato.

Esto muestra que Copilot actúa como revisor automático (no un agente de codificación): ve la tabla sin formato, aplica las directrices de la empresa de .github/copilot-instructions.md y proporciona una versión corregida en línea.

Escribir resúmenes efectivos de solicitudes de cambios
Escribir descripciones de PR suele ser el último paso del proceso y puede sentirse como un obstáculo. Copilot facilita esto. Desde el editor de descripción de PR, puede usar el icono de Copilot para generar un resumen o un borrador de esquema. Incluso si realiza modificaciones, tener un punto de partida bien estructurado ahorra tiempo y garantiza que los revisores tengan la información que necesitan.

Captura de pantalla de una solicitud de incorporación de cambios de GitHub que muestra un cuadro de comentario con las opciones de GitHub Copilot para generar un resumen o esquema de los cambios.

Explicación y revisión del código
A veces quizás no estés familiarizado con el código en un pull request. En lugar de tener dificultades con ello, puede pedir a Copilot que explique los cambios. Copilot también puede ejecutar una revisión inicial de tus propios PRs antes de solicitar comentarios de tus compañeros de equipo. Esto ayuda a detectar problemas más pequeños, valida los procedimientos recomendados y proporciona más confianza en la calidad del envío.

Ahora sabe lo que Copilot es capaz de cuando se trata de revisiones de código. A continuación, veamos cómo usar las revisiones de Copilot directamente en GitHub.com.

## Uso de Copilot como revisor en GitHub.com

En GitHub.com, solicitar una revisión de Copilot es tan simple como agregarla desde el menú Revisores. En segundos, Copilot genera un comentario que no es una aprobación o rechazo, por lo que nunca bloquea las combinaciones, sino que, en su lugar, agrega un contexto valioso para los revisores humanos. También puede personalizar el comportamiento de Copilot agregando un archivo copilot-instructions.md al repositorio. Estas instrucciones guían a Copilot para seguir las directrices de revisión específicas de su equipo, por lo que busca las mismas cosas que hace y mantiene sus sugerencias alineadas con sus estándares.

Los comentarios de revisión se ven y se comportan como los comentarios de tus compañeros de equipo: puedes reaccionar, resolver o comentarlos. Copilot podría marcar las sugerencias de tipo que faltan, sugerir cambios de formato o resaltar posibles errores.

Al final de esta unidad, podrás:

Solicite e interprete una revisión de Copilot.
Aplique los cambios sugeridos de Copilot.
Entienda los límites del rol de Copilot en las revisiones.
Revisión de código en GitHub.com
Abrir o crear una solicitud de incorporación de cambios Empiece por crear una nueva solicitud de incorporación de cambios o vaya a una existente en el repositorio.

Agregar Copilot como revisor En el menú Revisores , seleccione Copilot. Esto asigna a Copilot para que revise los cambios, al igual que asignaría a un compañero de equipo humano.

Captura de pantalla del panel de revisores en una solicitud de cambios de GitHub que muestra a Copilot sugerido como revisor de programador de pares por IA.

Espere a que se complete la revisión Copilot comienza a analizar la solicitud de incorporación de cambios inmediatamente. Las revisiones suelen finalizar en menos de 30 segundos, por lo que obtendrá resultados rápidamente sin interrumpir el flujo de trabajo.

Revisión de los comentarios de Copilot Desplácese por la solicitud de incorporación de cambios para leer los comentarios de Copilot. Las sugerencias se dejan como comentarios en las líneas de código pertinentes.

Captura de pantalla de un pull request de GitHub en la que Copilot sugiere corregir un nombre de variable mal escrito de random_greetin a random_greeting en un archivo Ruby.

Aplicar los cambios sugeridos por Copilot Cuando Copilot marca problemas, puede confirmar las correcciones directamente desde la interfaz de solicitud de cambios. Para los comentarios entre pares, puede usar Copilot para generar soluciones rápidamente.

Mensaje de ejemplo:

"Sugerir una corrección para este comentario de revisión: Reemplace exec() por una función más segura".

Copilot propone un parche mediante subprocess.run(). El desarrollador lo prueba localmente, confirma los cambios y asegura que las pruebas pasen.

Las PRU hacen que estas correcciones sean más rápidas y inteligentes, lo que permite a Copilot analizar comentarios de revisión junto con el contexto de código para proponer soluciones de alta calidad.

Descripción de los límites

El papel de Copilot en las revisiones es asesoramiento. No aprueba ni rechaza las solicitudes de incorporación de cambios y sus comentarios no cuentan para las aprobaciones necesarias. Úselo para detectar problemas temprano, generar sugerencias accionables y acelerar las verificaciones rutinarias, pero confíe en los revisores humanos para las decisiones arquitectónicas, los inconvenientes con matices y la aprobación final.

Revisar en GitHub.com es eficaz, pero puede detectar aún más problemas antes de que el código llegue a GitHub mediante Copilot en el IDE.

## Detección de problemas tempranos y automatización de revisiones con Copilot
Las revisiones de GitHub Copilot no tienen que esperar hasta abrir un pull request. En VS Code o JetBrains IDE, puede solicitar a Copilot que revise los cambios antes de confirmar. Esto le permite abordar infracciones de estilo, brechas de seguridad o problemas de procedimientos recomendados relacionados con los ciclos de ahorro anteriores en el proceso de revisión. También puede configurar Copilot para revisar todas las solicitudes de incorporación de cambios automáticamente, escalando este enfoque entre repositorios y equipos.

Al final de esta unidad, podrás:
Use las revisiones de Copilot localmente en VS Code o los IDE de JetBrains.
Personalice el comportamiento de revisión de Copilot con instrucciones específicas para el repositorio y la ruta.
Aproveche las unidades de solicitud Premium (PRU) para un análisis más profundo en el IDE.
Configura las revisiones automáticas de Copilot para todas las solicitudes de incorporación de cambios.
Combina Copilot con conjuntos de reglas y verificaciones de estado.
Reconozca las ventajas de la automatización a escala.
Ejecución de revisiones de Copilot localmente en el IDE
Para guiar las revisiones, cree un archivo .github/copilot-instructions.md con reglas como:

"Céntrese en la seguridad y evite la interpolación de cadenas no seguras".
"Asegúrese de que las funciones tienen docstrings que explican los parámetros y los tipos de valor devuelto".
A continuación, Copilot aplica estas reglas automáticamente a las revisiones para analizar diferencias más grandes y proporcionar información enriquecida en contexto que se alinee con el estilo del repositorio.

Caso de uso: Un desarrollador agrega código repetitivo en un servicio TypeScript. Copilot lo marca y sugiere extraer una función auxiliar. En lugar de esperar a que los compañeros lo señalen, el desarrollador lo corrige antes de enviar el código, reduciendo así el ruido durante la revisión posterior.

Creación de instrucciones personalizadas específicas de la ruta de acceso
Puede utilizar instrucciones personalizadas para rutas específicas para guiar la revisión del código de Copilot o el Agente de la Nube de Copilot en archivos o carpetas específicas. A continuación se explica cómo configurarlas:

Creación del directorio de instrucciones

En la raíz del repositorio, agregue una carpeta denominada .github/instructions si aún no existe.

Agregar archivos de instrucción

Dentro de esa carpeta, cree uno o varios archivos que terminen en .instructions.md (por ejemplo, security.instructions.md). El nombre de archivo describe el propósito de las instrucciones.

Defina las rutas de acceso a las que se va a aplicar

En la parte superior de cada archivo, agregue un bloque frontmatter con una palabra clave applyTo. Use la sintaxis glob para dirigir los archivos o directorios en los que se deben aplicar estas instrucciones.

Ejemplo: se aplica a los modelos de Ruby:

applyTo: "app/models/**/*.rb"
Ejemplo: aplicar a archivos TypeScript:

applyTo: "**/*.ts,**/*.tsx"
Para aplicar a todos los archivos del repositorio, use:

applyTo: "**"
Escribir las instrucciones personalizadas

Debajo del frontmatter, agregue la guía de revisión en lenguaje sencillo usando Markdown. Puede escribirlo como párrafo, en líneas independientes o con líneas en blanco para mejorar la legibilidad. Copilot seguirá estas instrucciones cada vez que revise o genere código para las rutas de acceso coincidentes.

Ha visto cómo Copilot ayuda localmente. Ahora vamos a explorar cómo escalar las revisiones entre equipos y repositorios.

Aprovechar las PRU para un análisis más profundo en el IDE
Al ejecutar revisiones de Copilot directamente dentro de tu IDE, como Visual Studio Code o JetBrains, no estás limitado a las verificaciones ligeras disponibles en GitHub.com. Al asignar unidades de solicitud Premium (PRU) a estas revisiones locales, Copilot puede aprovechar modelos más avanzados que analizan diferencias más grandes, aplican las instrucciones personalizadas del repositorio y exponen sugerencias de mayor calidad antes de que el código llegue a una solicitud de cambios. Esto significa que puede detectar infracciones de estilo, brechas de seguridad y problemas relacionados con las mejores prácticas más temprano en el ciclo de desarrollo, lo que ahorra tiempo durante las revisiones formales y reduce el intercambio con los compañeros. Las revisiones impulsadas por PRU en el IDE le proporcionan un análisis más profundo y enriquecido en el lugar exacto donde escribe y prueba el código, a la vez que deja el juicio final y la aprobación en manos de revisores humanos.

Automatización de revisiones y escalado con conjuntos de reglas
Las revisiones manuales no se escalan bien en equipos que se mueven rápidamente. GitHub permite configurar conjuntos de reglas para que Copilot se asigne automáticamente a todas las solicitudes de cambios (PR) dirigidas a ramas protegidas. Esto garantiza que todos los cambios se revisen, incluso si se retrasan los revisores humanos.

Empareja las revisiones de Copilot con comprobaciones de estado, como pruebas o análisis de código. Esto crea una canalización donde:

Copilot revisa el estilo y la legibilidad.
Escaneo de código marca vulnerabilidades.
Las pruebas validan la funcionalidad.
Dado que cada revisión de Copilot usa PRU, las organizaciones deben presupuestar el consumo de PRU para que coincida con el volumen de revisión y realizar revisiones automatizadas en momentos adecuados en el proceso de desarrollo. El seguimiento del uso ayuda a equilibrar el costo y la cobertura.

Con la automatización, incluso las correcciones pequeñas o las actualizaciones de dependencia se revisan de forma coherente, lo que reduce el riesgo de regresiones desapercibidas.

La automatización garantiza que las revisiones se realicen a gran escala. ¿Pero qué pasa con la implementación de comentarios de revisión? Ahí es donde Copilot brilla como asociado de codificación.

Revisiones automáticas para su cuenta
Esta opción solo está disponible si está en el plan Copilot Pro o Copilot Pro+.

Cuando activa esta función en la configuración personal de Copilot, cada solicitud de cambios que abra se revisará automáticamente. Esto ayuda a los desarrolladores individuales a detectar problemas al principio en todo su trabajo.

Pasos:

En la esquina superior derecha de cualquier página de GitHub, haga clic en su imagen de perfil y seleccione Su Copilot.

Captura de pantalla del panel de configuración de GitHub que muestra las opciones para habilitar o deshabilitar las revisiones automáticas de código de Copilot para las solicitudes de incorporación de cambios.

Busque la opción de revisión de código automática de Copilot.

En la lista desplegable, seleccione Habilitado.

A partir de ahora, Copilot siempre se agregará a las solicitudes de incorporación de cambios.

Revisiones automáticas de un repositorio
A veces solo querrá revisiones automáticas en ciertos repositorios, como servicios de producción, que requieren un control de calidad más estricto. Los administradores del repositorio pueden aplicar esto mediante la creación de un conjunto de reglas de rama.

Pasos:

En el repositorio, haga clic en Configuración.

En la barra lateral izquierda, expanda Código y automatización y seleccione Reglas → Conjuntos de reglas.

Captura de pantalla de una barra de navegación del repositorio de GitHub que resalta la pestaña Configuración.

Haga clic en Nuevo conjunto de reglas y, a continuación, elija Nuevo conjunto de reglas de rama.

Captura de pantalla del menú de configuración del repositorio de GitHub que resalta la opción Conjuntos de reglas en Código y automatización.

Escriba un nombre, establezca Estado de cumplimiento en Activo y seleccione ramas de destino (por ejemplo, rama predeterminada).

En Reglas de rama, marque Requerir una solicitud de cambios antes de combinarla.

En las opciones expandidas, seleccione Solicitar revisión de solicitud de cambios de Copilot.

Captura de pantalla de la configuración del repositorio de GitHub que muestra los requisitos de solicitud de incorporación de cambios, incluidas las aprobaciones necesarias, las revisiones de equipo, las revisiones de propietario del código y la opción para solicitar revisiones de Copilot.

En la parte inferior, haga clic en Crear.

Ahora, cada PR dirigido a las ramas elegidas incluirá automáticamente la revisión de Copilot. Opcionalmente, también puede habilitar "Requerir resolución de conversación antes de combinar" para animar a los desarrolladores a leer los comentarios de Copilot.

Revisiones automáticas en una organización
Para equipos más grandes, puede escalar este enfoque entre varios repositorios a la vez. Los propietarios de la organización pueden crear conjuntos de reglas que se aplican a repositorios seleccionados, en función de patrones de nombre o reglas de inclusión o exclusión.

En la esquina superior derecha de GitHub, haga clic en la imagen del perfil y seleccione Sus organizaciones.

Elija la organización y, a continuación, vaya a Configuración.

En la barra lateral, seleccione Repositorio → Conjuntos de reglas.

Captura de pantalla del menú de configuración de la organización de GitHub que resalta la opción Conjuntos de reglas en Repositorio.

Haga clic en Nuevo conjunto de reglas → Nuevo conjunto de reglas de rama.

Proporcione un nombre de conjunto de reglas y establezca Estado de cumplimiento en Activo.

Agregue repositorios de destino especificando patrones de inclusión o exclusión (por ejemplo, *servicio para que coincida con todos los repositorios de servicio).

Definir ramas de destino.

Habilite Exigir una solicitud de cambios antes de combinar y, a continuación, active Solicitar revisión de solicitud de cambios de Copilot.

Para guardar, haga clic en Crear.

Esto garantiza estándares coherentes y reduce los tiempos de revisión en toda la organización.



## Medición del impacto y optimización de unidades de solicitud Premium (RU)
Las unidades de solicitud Premium (RU) son el combustible detrás de las características de revisión más eficaces de GitHub Copilot. Cada vez que asignes a Copilot para revisar una solicitud de incorporación de cambios de gran tamaño, solicitarle que aplique las instrucciones personalizadas de tu repositorio a un código base completo o que realice un análisis profundo de los cambios en tu IDE, estás utilizando PRUs. Estos recursos premium proporcionan a Copilot la potencia de procesamiento adicional y la profundidad del contexto necesarias para proporcionar un razonamiento más completo, salidas más confiables y sugerencias que se alinean con los estándares del equipo.

Objetivos de aprendizaje
Al final de esta unidad, podrás:

Defina las PRU y explique cómo habilitan las funcionalidades de revisión avanzada de Copilot.
Mida el impacto de las revisiones con tecnología PRU en el flujo de trabajo.
Aplique estrategias al presupuesto y optimice las PRUs para obtener el valor máximo.
Descripción de las PRU
Piense en unidades de solicitud Premium (PRU) como tokens que desbloquean el "engranaje adicional" de Copilot. Tareas rutinarias y ligeras que sugieren una pequeña refactorización a una sola línea a menudo no consumen PRU. Pero las tareas de nivel premium sí lo hacen. Por ejemplo, pedir a Copilot que revise un cambio de 1500 líneas en varios archivos, aplique el .github/copilot-instructions.md archivo y compruebe si hay problemas de seguridad y estilo requiere mucho más contexto y capacidad de razonamiento.

Con las PRU, Copilot puede examinar diferencias completas, interpretar las directrices de revisión personalizadas y devolver correcciones accionables en segundos. Sin ellos, solo proporciona sus sugerencias predeterminadas y ligeras. Las PRU marcan la diferencia entre las sugerencias rápidas y el análisis completo y detallado del contexto que se alinean con los estándares de su equipo, directamente dentro de las solicitudes de cambios o el IDE.

Escenario de ejemplo:

Un desarrollador inserta una refactorización masiva que afecta a decenas de archivos. Copilot, asignado como revisor, usa PRUs para aplicar las directrices de estilo y seguridad del repositorio a toda la modificación, señala varias interpolaciones de cadenas inseguras e incluso redacta comentarios en Markdown que explican el problema. En lugar de dedicar horas a realizar comprobaciones manuales, los revisores humanos ahora pueden centrarse en el impacto arquitectónico de la refactorización.

¿Por qué las PRU son importantes para los equipos?
Las PRU son lo que hace que Copilot sea realmente escalable en entornos de gran volumen. Con ellos, puede:

Obtenga un análisis más profundo: Detecte vulnerabilidades sutiles, lógica duplicada o infracciones de estilo en diferencias grandes antes de llegar a producción.
Exigir coherencia: Aplique automáticamente las mismas comprobaciones de seguridad, legibilidad o estilo en cada solicitud de incorporación de cambios.
Controlar las ráfagas de actividad: Durante los ciclos de versión ocupados, confíe en las revisiones con tecnología PRU para mantener la calidad estable mientras que los revisores humanos controlan decisiones complejas de diseño.
Escenario de ejemplo:

El equipo mantiene una arquitectura de microservicios en Go, Python y TypeScript. Durante una fase de preparación previa al lanzamiento, Copilot utiliza PRU para revisar cada servicio en busca de mejores prácticas específicas del lenguaje, y marca una llamada de eval() arriesgada en JavaScript y recomienda un analizador más seguro, al mismo tiempo que detecta una falta de comprobación de errores en un controlador de Go. Esto permite que el equipo combine correcciones rápidamente en todos los servicios sin que falten detalles críticos.

Medición del impacto de las revisiones con tecnología PRU
Para comprender el rendimiento de las PRU, realice un seguimiento de métricas como:

Plazo de solicitud de cambios: La rapidez con la que las solicitudes de cambios pasan de estar abiertas a combinarse después de agregar revisiones de Copilot.
Indicadores de calidad: Reducción de problemas de estilo o seguridad posteriores a la combinación marcados por otras herramientas.
Experiencia para desarrolladores: Comentarios sobre si Copilot hace que las revisiones sean más rápidas o más claras.
Métrica de ejemplo:

Antes de usar las PRU, las solicitudes de cambios grandes tardaban un promedio de tres días en combinarse y a menudo desencadenaban ajustes de estilo tras la publicación. Después de habilitar las revisiones con tecnología de PRU, las mismas solicitudes de cambios se combinaron en un día con menos confirmaciones de seguimiento.

Optimización del uso de PRU
La administración de los PRUs asegura que se están utilizando donde aportan el mayor valor.

Planee por adelantado: Establezca alertas cuando alcance 75%, 90%y 100% del uso mensual de PRU.
Use PRU estratégicamente: Reserve las revisiones premium para cambios grandes o de alto riesgo, confíe en las sugerencias estándar de Copilot para las ediciones sencillas.
Refina tus mensajes: Las solicitudes limpias y específicas reducen los reintentos innecesarios y los PRUs desperdiciados.
Escale verticalmente si es necesario: Si el equipo aumenta constantemente las PRU, considere un plan de Copilot de nivel superior para gestionar la carga de trabajo.
Escenario de ejemplo:

Un equipo observa que muchas PRU se invierten en cambios de documentación triviales. Actualizan su flujo de trabajo para usar solicitudes que no son PRU para pequeñas ediciones y reservan revisiones con tecnología PRU para el código que afecta a la producción. Como resultado, su uso mensual de PRU disminuye en 30% sin perder calidad.

Las PRU son más que un detalle técnico, lo que hace que las funcionalidades de revisión avanzada de Copilot sean posibles. Al comprender cómo funcionan las PRU, medir su impacto y optimizar su uso, puede ofrecer revisiones más profundas y contextuales sin perder recursos. Esto permite a los equipos escalar revisiones de código de alta calidad incluso con plazos estrictos, mientras que el juicio final y la aprobación quedan en manos de revisores humanos.

## Ejercicio: Revisión de código de GitHub Copilot
En este ejercicio, aprenderá a:

Uso de GitHub Copilot para revisar el código directamente en VS Code para obtener comentarios inmediatos
Solicitar revisiones de código de Copilot en pull requests
Personaliza consideraciones de revisión de Copilot con instrucciones específicas del repositorio
Configuración de revisiones automáticas de código mediante conjuntos de reglas de repositorio
Cómo empezar
Al seleccionar el botón Iniciar el ejercicio en GitHub siguiente, se le dirigirá a un repositorio de plantillas de GitHub público que le pedirá que complete una serie de pequeños desafíos.

Cuando finalice el ejercicio en GitHub, vuelva aquí para:

Una comprobación rápida de conocimientos.
Un resumen de lo que ha aprendido.
Un distintivo por completar este módulo.
Inicio del ejercicio en GitHub

## Resumen
Copilot es más eficaz cuando se trata como colaborador, no como reemplazo. Úselo para acelerar las comprobaciones rutinarias y proporcionar sugerencias prácticas, pero confíe en los seres humanos para las decisiones arquitectónicas y las compensaciones complejas.

Procedimientos recomendados:

Ejecute las revisiones de Copilot en los momentos adecuados en el proceso de desarrollo del IDE antes de insertar.
Use .github/copilot-instructions.md para alinear los comentarios de Copilot con los estándares del equipo.
Trate los comentarios de Copilot como aceleradores, no como mandatos. Siga usando las canalizaciones de CI/CD de lanzamiento, los análisis y otras mejores prácticas junto con las revisiones de Copilot.
Valide y pruebe siempre las correcciones antes de la combinación.
Con las PRU, desbloquea características con tecnología premium que hacen que Copilot sea un asociado aún más fuerte. Al supervisar el uso y alinear los flujos de trabajo, asegúrese de que las revisiones se mantengan rápidas, de alta calidad y rentables.

Ahora que ha completado este módulo, puede hacer lo siguiente:

Explicar cómo GitHub Copilot mejora las revisiones de código y los PRs.
Use Copilot como revisor en GitHub y en el IDE.
Automatice las revisiones con conjuntos de reglas e instrucciones personalizadas.
Aplique las sugerencias de Copilot y las correcciones de la revisión por pares.
Defina las PRU, explique sus ventajas y optimice su uso.
Mida el impacto de Copilot en la velocidad, la calidad y la satisfacción.
Con estas prácticas, tu equipo puede transformar las revisiones de código de ser cuellos de botella a convertirse en momentos colaborativos de alto valor, escalando su experiencia y entregando software más rápidamente.

Aprende más
Para profundizar en la comprensión de la revisión de código de GitHub Copilot y los flujos de trabajo relacionados, consulte los siguientes recursos:

Acerca de la revisión de código de Copilot de GitHub

Uso de la revisión de código de Copilot de GitHub

Incorporación de feedback en tu pull request

Aprobación de un pull request con revisiones necesarias

Adición de instrucciones personalizadas del repositorio para GitHub Copilot

Configuración de la revisión automática de código de GitHub Copilot

Configuración de directrices de codificación para la revisión de código de Copilot de GitHub

Proporcionar comentarios
Use este formulario de problema para proporcionar comentarios de contenido o cambios sugeridos para este módulo de Microsoft Learn. GitHub mantiene este contenido y un miembro del equipo evaluará la solicitud. Gracias por darse el tiempo de mejorar nuestro contenido.
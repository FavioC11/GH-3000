# GitHub Copilot Across Environment
## Introducción
GitHub Copilot es un asistente avanzado de codificación con tecnología de inteligencia artificial que puede mejorar drásticamente la eficacia del desarrollador en todas las fases del flujo de trabajo de desarrollo. GitHub Copilot ahorra tiempo para los desarrolladores, lo que les permite concentrarse en la resolución e innovación de problemas de nivel superior mediante la automatización de tareas rutinarias, la finalización de código pertinente y la generación de bloques completos de código que aceleran los ciclos de desarrollo desde la codificación inicial hasta la finalización de la solicitud de incorporación de cambios.

GitHub Copilot ofrece opciones de interacción flexibles adaptadas a su flujo de trabajo, reuniéndose con usted dondequiera que trabaje en su entorno de desarrollo. Ya sea a través de la finalización de código en el IDE, chat conversacional para resolver problemas complejos, características colaborativas en GitHub.com o asistencia de línea de comandos, Copilot se integra perfectamente en todos los entornos para mejorar la experiencia de desarrollo y la productividad. Comprender estos modos de interacción es clave para desbloquear todo el potencial de GitHub Copilot y optimizar el flujo de trabajo de codificación para ofrecer rápidamente cambios de código de calidad.

En este módulo se tratan los diferentes métodos para interactuar con GitHub Copilot, guiarle sobre cuándo, dónde y cómo usar estos métodos para comunicar de forma eficaz sus objetivos a Copilot y proporcionarle la información necesaria para completar las tareas.

En este módulo obtendrá información sobre:

Cómo usar las sugerencias automáticas de GitHub Copilot, varios panel de sugerencias y su capacidad de adaptarse a diferentes estilos de codificación para acelerar los flujos de trabajo de desarrollo.
Cómo proporcionar contexto a GitHub Copilot a través de comentarios insertados, bloquear comentarios, docstrings y otros tipos de comentarios para mejorar la precisión y la velocidad de la generación de código.
Interactuar con GitHub Copilot a través de conversaciones de lenguaje natural para generar código complejo, depurar problemas, obtener explicaciones de código y simplificar las tareas de desarrollo en tiempo real.
Cómo mejorar la relevancia de las sugerencias de Chat de GitHub Copilot mediante la referencia de ámbito, los comandos de barra diagonal y los agentes para completar rápidamente las tareas rutinarias.
Aprovechamiento de GitHub Copilot en GitHub.com para la exploración del repositorio, asistencia de solicitudes de incorporación de cambios, tareas del agente y flujos de trabajo de revisión de código de colaboración.
Cómo interactuar con GitHub Copilot en la CLI para obtener explicaciones de comandos, sugerencias y ejecutar comandos para automatizar flujos de trabajo de terminal.
Configuración de la CLI de GitHub Copilot, alias y administración de la configuración de privacidad, incluida la exclusión de la recopilación de datos de uso.

## Finalización del código con GitHub Copilot

Las características de finalización de código de GitHub Copilot se encuentran directamente dentro del IDE, donde se escribe y revisa el código. GitHub Copilot se integra perfectamente con editores como Visual Studio Code o JetBrains, ofreciendo características como sugerencias automáticas, un panel de sugerencias múltiple y compatibilidad con varios estilos de codificación. Puede interactuar principalmente con GitHub Copilot a través de estas herramientas del IDE y comprender cómo y dónde usarlos le ayuda a optimizar sus eficaces capacidades de generación de código.

En esta unidad, tratamos:

Lenguajes compatibles con GitHub Copilot
Sugerencias automáticas
Panel de sugerencias múltiples
Compatibilidad con diferentes estilos de codificación en sugerencias
Cómo GitHub Copilot incorpora comentarios de codificación para sugerencias
Lenguajes compatibles con GitHub Copilot
GitHub Copilot proporciona una sólida compatibilidad con una amplia gama de lenguajes de programación y marcos, con funcionalidades sólidas en:

Pitón
JavaScript
Java
TypeScript
Rubí
Go
C#
C++
Aunque estos lenguajes reciben compatibilidad excepcional, GitHub Copilot también puede ayudar con muchos otros lenguajes y marcos.

 Sugerencia

GitHub Copilot ofrece un nivel gratuito con 2000 autocompletados de código y 50 mensajes de chat al mes. Para empezar, abra Visual Studio Code, haga clic en el icono de GitHub Copilot y, a continuación, haga clic en "Iniciar sesión para usar GitHub Copilot de forma gratuita". Inicie sesión en la cuenta de GitHub en la ventana que se abrirá en el explorador. Más información. Los educadores, estudiantes y los mantenedores de código abierto seleccionados pueden recibir Copilot Pro de forma gratuita, obtenga información sobre cómo: https://aka.ms/Copilot4Students.

Sugerencias automáticas
Copilot ofrece sugerencias de código a medida que escribe: a veces completando la línea actual, a veces sugiriendo un nuevo bloque de código completo. Puede aceptar toda la sugerencia, parte de ella o ignorarla. Esta capacidad para proporcionar sugerencias en tiempo real y con reconocimiento del contexto ahorra un tiempo de desarrollo valioso al reducir la necesidad de buscar sintaxis, solucionar problemas de lógica o escribir patrones comunes repetidamente.

Recorte de pantalla del texto de reflejo de finalización automática.

Panel de sugerencias múltiples
Cuando trabaja en un bloque de código y GitHub Copilot ofrece una sugerencia, verá un fragmento de código atenuado. Para explorar más opciones y acelerar el flujo de trabajo de desarrollo, mantenga el puntero sobre la sugerencia para mostrar el panel de control de GitHub Copilot. Esta característica le permite evaluar rápidamente varios enfoques para el mismo problema, lo que le ayuda a elegir la solución más adecuada para su contexto específico.

Recorte de pantalla del texto de reflejo de finalización automática de varias sugerencias.

Haga clic en los botones de flecha hacia delante o hacia atrás en el panel de control para ver las sugerencias siguientes o anteriores. También puede usar métodos abreviados de teclado para recorrer rápidamente las opciones:

macOS: Opción (⌥) o Alt+] (siguiente), Opción (⌥) o Alt+[ (anterior)
Windows o Linux: Alt+] (siguiente), Alt+[ (anterior)
Captura de pantalla del panel de sugerencias.

Esta iteración rápida a través de varias sugerencias de código le ayuda a mantener el impulso del desarrollo al permitirle comparar rápidamente los enfoques sin interrumpir el flujo de codificación. En lugar de empezar desde cero o buscar ejemplos en línea, puede evaluar diferentes implementaciones en cuestión de segundos, seleccionando la que mejor se adapte a sus necesidades y estilo de codificación.

Aunque GitHub Copilot es excelente para sugerir código automáticamente, también demuestra su capacidad de adaptarse a través de las siguientes maneras:

Implementación del método: al empezar a escribir un nombre de método, Copilot puede sugerir toda la implementación, siguiendo el estilo de codificación establecido.
Convenciones de nomenclatura: recoge las convenciones de nomenclatura preferidas para variables, funciones y clases.
Formato: Copilot se adapta al estilo de sangría, la colocación de corchetes y otras preferencias de formato.
Estilo de comentario: puede imitar su estilo de comentario, ya sea que prefiera comentarios en línea, en bloque o cadenas de documentación.
Patrones de diseño: cuando el proyecto usa de forma coherente ciertos patrones de diseño, Copilot sugiere código que se alinea con estos patrones.
Uso de comentarios de codificación para sugerencias
Un aspecto clave de esta funcionalidad es cómo incorpora comentarios de codificación para mejorar sus sugerencias. En esta sección se exploran las distintas formas en que GitHub Copilot utiliza comentarios para mejorar sus funcionalidades de finalización y generación de código.

Descripción del contexto del comentario
Cuando se integra en el código base existente, GitHub Copilot usa varios aspectos del código para proporcionar sugerencias más relevantes, incluidos los comentarios de código. Los desarrolladores suelen utilizar comentarios para aclarar la intención del código y mejorar la colaboración, y Copilot, como asistente de codificación de IA, hace uso de estos comentarios de forma muy parecida. Al comprender la intención de los comentarios, Copilot puede ofrecer sugerencias de código más precisas y adaptadas al contexto a través de dos procesos clave:

Procesamiento de lenguaje natural: Copilot usa técnicas avanzadas de procesamiento de lenguaje natural (NLP) para interpretar el significado y la intención detrás de los comentarios en el código.
Análisis contextual: analiza los comentarios en relación con el código circundante, entendiendo su relevancia y finalidad dentro del contexto más amplio del archivo o proyecto.
Tipos de comentarios utilizados
Copilot puede trabajar con varios tipos de comentarios para fundamentar sus sugerencias:

Comentarios insertados: explicaciones breves junto a líneas de código específicas.
Bloquear comentarios: explicaciones más largas que podrían describir una función o una clase.
Docstrings: cadenas de documentación formales en lenguajes como Python.
Comentarios de tareas pendientes: notas sobre futuras implementaciones o mejoras.
Documentación de API: comentarios que describen el uso y los parámetros de funciones o métodos.
Generación de código controlada por comentarios
Copilot usa comentarios de varias maneras para generar y sugerir código:

Implementación de funciones: cuando se describe una función en comentarios, Copilot puede sugerir una implementación completa basada en esa descripción.

Recorte de pantalla del texto de reflejo de finalización de código de varias líneas.

Finalización del código: Copilot usa comentarios para proporcionar finalizaciones de código más precisas y comprender la intención del desarrollador.

Recorte de pantalla del texto de reflejo de finalización automática de la función completa.

En este ejemplo, tenemos un comentario que describe una función para invertir una cadena. Basándose en este comentario, es probable que Copilot sugiera una implementación que utilice la notación de slice de Python con un paso de -1, que invierte eficientemente la cadena.

Nomenclatura de variables: los comentarios pueden influir en las sugerencias de Copilot para los nombres de variables, por lo que son más descriptivos y adecuados para el contexto.

Recorte de pantalla del texto de reflejo de finalización automática del nombre de variable.

Aquí tenemos un comentario que describe una lista de los libros favoritos del usuario. Es probable que Copilot sugiera nombres de variables descriptivos que se ajusten al contexto. En este caso, sugirió "favorite_books" como nombre de variable, que describe claramente el contenido de la lista.

Selección de algoritmos: cuando los comentarios describen un algoritmo o enfoque específicos, Copilot puede sugerir código que se alinee con ese método.

Recorte de pantalla del texto de reflejo de finalización automática del algoritmo.

En el ejemplo anterior, se proporcionan comentarios que describen los pasos del algoritmo de ordenación de burbujas. Basándose en estos comentarios, Copilot probablemente sugeriría una implementación que siguiera de cerca los pasos descritos.

## Chat de GitHub Copilot

GitHub Copilot Chat es una característica avanzada del ecosistema de GitHub Copilot, diseñado para proporcionar a los desarrolladores un asistente interactivo de inteligencia artificial conversacional directamente dentro de su entorno de desarrollo. Permite a los desarrolladores tener conversaciones en lenguaje natural sobre su código, formular preguntas y recibir respuestas inteligentes y sugerencias en tiempo real. En esta unidad, tratamos:

Generación de código mediante el chat de GitHub Copilot.
Depuración mediante el chat de GitHub Copilot.
Obtención de explicaciones sobre el código mediante el chat de GitHub Copilot.
Uso de comandos de barra diagonal para realizar acciones con GitHub Copilot.
Uso de agentes personalizados de GitHub Copilot para mejorar las indicaciones.
Para acceder a Copilot en su entorno de desarrollo integrado (IDE), haga clic en el icono de chat de la barra de navegación izquierda.

Recorte de pantalla del chat.

El chat de Copilot de GitHub es beneficioso en determinados escenarios:

Generación de código complejo Al necesitar implementar algoritmos complejos, estructuras de datos o generar código reutilizable para patrones de diseño específicos, el chat de Copilot le ayudará a simplificar los procesos. Puede ayudar a crear expresiones regulares complejas, construir consultas SQL detalladas o desarrollar estructuras de datos avanzadas como una ordenación de burbujas en Python.

Captura de pantalla de la generación de código mediante chat.

Ayuda en la depuración Al encontrar errores en el código, el chat de Copilot le resultará útil para analizar mensajes de error y sugerir posibles correcciones. Le ayudará a identificar errores lógicos y a proporcionar explicaciones paso a paso de las secciones que sean problemáticas del código. Una manera de lograr este resultado es mediante el chat en línea de Copilot resaltando el fragmento de código que contiene el error, haciendo clic con el botón derecho y seleccionando Copilot y, a continuación, en el chat en línea.

Captura de pantalla de la depuración mediante chat de código seleccionado.

Por ejemplo, podría preguntar: "Obtengo NullReferenceException con este método. ¿Me ayudas a depurarlo?"

Captura de pantalla de la depuración mediante chat de código generado.

Explicaciones sobre el código El chat de Copilot también se puede usar para comprender mejor aquellos fragmentos de código que sean complejos. Puede dividir el código en términos más sencillos, explicar el propósito y la funcionalidad de código que sea desconocido y ofrecer información sobre los procedimientos recomendados y las posibles optimizaciones. Por ejemplo, podría preguntar: "¿Puedes explicar cómo funciona este código asincrónico/de espera en Python?"

Captura de pantalla de las explicaciones del código mediante chat.

Cómo mejorar las respuestas del chat de GitHub Copilot
Es posible mejorar significativamente la calidad y relevancia de las respuestas del chat de GitHub Copilot con determinadas características clave. Profundicemos en ellas.

Referencias de ámbito
Para mejorar la precisión y relevancia de las respuestas proporcionadas por el chat de GitHub Copilot, es importante definir correctamente el ámbito de las preguntas a través de referencias. Así es cómo debe hacerlo:

Referencias de archivos: es posible especificar un archivo determinado en las preguntas agregando #file: antes del nombre de archivo.

Captura de pantalla del archivo de ámbito de chat que hace referencia a la selección.

Por ejemplo: en caso de trabajar con un archivo denominado controller.js, use el comando #file para seleccionarlo y hacer referencia a el directamente en la pregunta como #file:controller.js. Esta característica indica a Copilot Chat que se centre en el contenido de ese archivo al generar una respuesta.

Captura de pantalla de la referencia del archivo de ámbito de chat.

Referencias de entorno: puede usar Copilot Chat junto con el terminal para obtener ayuda basándose en la salida del comando. Esto permite a Copilot ayudar con la depuración y proporcionar sugerencias basadas en lo que sucede en el terminal. Por ejemplo, preguntando "¿@terminal cómo se corrige este error?" permite a Copilot analizar la salida del terminal y sugerir soluciones pertinentes.

Comandos de barra diagonal
Los comandos de barra diagonal del chat de GitHub Copilot permiten especificar rápidamente la intención de la consulta. Con esto se mejorará significativamente la calidad de las respuestas que se reciban haciendo que las indicaciones sean más centradas. Aquí hay algunos comandos de barra diagonal usados habitualmente:

/doc: agrega comentarios al código especificado o seleccionado. Por ejemplo, puede escribir /doc seguido del código que desea documentar y Copilot genera los comentarios adecuados.

Captura de pantalla de los comandos de barra diagonal /doc.

/explain: Proporciona explicaciones sobre el código seleccionado. Este comando es útil cuando necesita comprender lo que hace un fragmento de código determinado. Por ejemplo, /explain the #file:controller.js proporciona una explicación detallada de ese archivo.

Captura de pantalla de los comandos de barra diagonal /explain.

/fix: Propone correcciones para problemas en el código seleccionado. En caso de tener problemas, resalte la sección problemática y use /fix para recibir sugerencias que ayuden a resolver el problema.

Captura de pantalla de los comandos de barra diagonal /fix.

/generate: ayuda a generar código nuevo en función de sus requisitos. Por ejemplo, /generate code to find the root of a number in client.js crea una función para realizar la tarea.

Captura de pantalla de los comandos de barra diagonal /generate.

/optimize: Analiza y sugiere mejoras del tiempo de ejecución o la eficacia del código seleccionado. Por ejemplo, /optimize the calcular method in controller.js se centra en mejorar el rendimiento de ese método específico.

Captura de pantalla de los comandos de barra diagonal /optimize.

/tests: Crea automáticamente pruebas unitarias para el código seleccionado. Simplemente resalte el código y use /tests using Mocha para generar pruebas.

Captura de pantalla de los comandos de barra diagonal /tests.

Selección de modelos y características premium
GitHub Copilot Chat ofrece diferentes modelos de inteligencia artificial para optimizar el flujo de trabajo de desarrollo. Algunos entornos proporcionan opciones de selección de modelos que permiten elegir entre distintos niveles de funcionalidad en función de sus necesidades específicas:

Modelos estándar (GPT-4o):

Proporcionar respuestas rápidas y confiables para la mayoría de las tareas de desarrollo
Consumo de 1 PRU por solicitud
Ideal para la asistencia rutinaria de programación, explicaciones de código y depuración básica
Ejemplos: Generación de funciones sencillas, ayuda de sintaxis, sugerencias básicas de refactorización
Modelos Premium (o1-preview, o1-mini):

Ofrecer funcionalidades de razonamiento mejoradas para problemas complejos
Consumir 2 PRU por solicitud (doble la tasa estándar)
Más adecuado para análisis sofisticados, algoritmos complejos y decisiones arquitectónicas
Ejemplos: Depuración avanzada de código multiproceso, diseño de algoritmo complejo, análisis de seguridad
Al trabajar con problemas desafiantes que requieren un razonamiento profundo, los modelos Premium pueden proporcionar un análisis más exhaustivo y soluciones completas. Sin embargo, tenga en cuenta el uso de PRU al seleccionar modelos para distintos tipos de tareas.

 Nota

El uso de modelos premium (o1-preview, o1-mini) consume 2 PRUs en lugar de 1 para la misma solicitud. Supervise las asignaciones mensuales y elija el modelo adecuado en función de la complejidad de las tareas. Para más información sobre el consumo y los límites de PRU, consulte la documentación de Solicitudes en GitHub Copilot.

Agentes de Copilot
Los agentes de GitHub Copilot son herramientas personalizadas que se compilan e integran con el chat de GitHub Copilot para proporcionar funcionalidades adicionales adaptadas a sus necesidades específicas. Además de los comandos de barra diagonal, se pueden usar agentes específicos dentro del chat de Copilot en el IDE para controlar diferentes tareas:

También puede usar la acción inteligente "/new" para generar un proyecto completamente nuevo desde cero en función de sus requisitos. Por ejemplo, puede pedir a Copilot que cree un nuevo proyecto con:

text
/new generate a new HTML file with pages and JavaScript for advanced calculations
Haga clic en “Crear área de trabajo” para proceder con la generación de código y tendrá el nuevo proyecto con el código solicitado.

@terminal: este agente resulta útil para preguntas relacionadas con la línea de comandos. Por ejemplo, podría pedirle que encontrase el archivo más grande de un directorio o que explique sobre el último comando ejecutado.

Captura de pantalla del comando de agente 

@vscode: use este agente para formular preguntas relacionadas con Visual Studio Code, como indicaciones sobre cómo depurar o cambiar la configuración del IDE.

Captura de pantalla del comando de agente 

Gracias a un uso eficaz de estas herramientas y técnicas, mejorará significativamente la calidad de las respuestas que reciba del chat de GitHub Copilot, logrando que la experiencia de codificación sea más eficaz y productiva.

 Nota

Los agentes avanzados y las operaciones complejas pueden consumir más unidades de solicitud Premium (PRU). Las consultas simples suelen usar 1 PRU, mientras que el análisis complejo del área de trabajo o la generación de proyectos pueden usar 2-5 PRU. Para obtener más información sobre el consumo de PRU, las asignaciones mensuales y los límites de tarifas, consulte la documentación de Solicitudes en GitHub Copilot.

Uso compartido de comentarios en el chat de GitHub Copilot
La mayoría de los IDE que cuentan con la integración del chat de Copilot disponen de mecanismos integrados de comentarios. Por ejemplo, en Visual Studio Code, puede encontrar opciones de comentarios al principio de las sugerencias de Chat de Copilot de GitHub. Pase el ratón por encima de una sugerencia y debería ver los botones "Me gusta" y "No me gusta".

Captura de pantalla de los botones de pulgar hacia arriba como útil.

Haga clic en el pulgar hacia arriba para calificar una sugerencia como útil.

Captura de pantalla de pulgar hacia abajo como poco útil.

Haga clic en el pulgar hacia abajo para calificar una como poco útil.

## GitHub Copilot en GitHub.com

GitHub Copilot se extiende más allá del entorno de desarrollo local para proporcionar asistencia de inteligencia artificial directamente en GitHub.com. Al trabajar con repositorios, problemas, solicitudes de incorporación de cambios y discusiones en la interfaz web de GitHub, puede aprovechar las funcionalidades de Copilot para simplificar el flujo de trabajo y mejorar la colaboración.

En esta unidad, trataremos lo siguiente:

Acceso a GitHub Copilot en GitHub.com
Tareas del agente de GitHub Copilot en GitHub.com
Exploración y documentación del repositorio
Asistencia para solicitudes de incorporación de cambios
Administración de problemas
Revisión y colaboración de código
Explicación del error de GitHub Copilot en Acciones de GitHub
Acceso a Copilot en GitHub.com
Copilot se integra en toda la interfaz web de GitHub, que aparece como un botón de chat o sugerencias insertadas en varios contextos. Puede acceder a las características de Copilot en varias áreas:

Páginas del repositorio: obtener explicaciones del código, la documentación y la estructura del proyecto
Problemas y solicitudes de incorporación de cambios: generar resúmenes, sugerir soluciones y redactar respuestas
Discusiones: ayuda a formular respuestas y proporcionar información técnica
Revisión de código : análisis de cambios y sugerencias de mejoras
Tareas del agente de GitHub Copilot en GitHub.com
Al usar Copilot en GitHub.com, puede realizar varias tareas controladas por agentes:

Recorte de pantalla que muestra varias tareas del agente de GitHub Copilot disponibles en GitHub.com, incluida la exploración del repositorio, la asistencia de solicitudes de incorporación de cambios y la administración de problemas.

Estas tareas se pueden ejecutar en segundo plano mientras se centra en otro trabajo.

Exploración y documentación del repositorio
Explicación del código: pida a Copilot que explique secciones de código complejas, funciones o archivos completos
Información general del proyecto: obtención de resúmenes generados por IA del propósito del repositorio, la arquitectura y los componentes clave
Generación de documentación: crear o mejorar archivos LÉAME, documentación de API y comentarios de código
Ejemplo: "Explicar la funcionalidad principal de este repositorio y sus componentes clave"

Recorte de pantalla de GitHub Copilot que proporciona información general sobre la explicación del código y el repositorio en una página del repositorio de GitHub.

Asistencia para solicitudes de incorporación de cambios
GitHub Copilot en GitHub.com acelera significativamente el flujo de trabajo de la solicitud de incorporación de cambios mediante la automatización de muchas tareas de revisión y documentación que consumen mucho tiempo:

Resúmenes de PR: genere resúmenes completos de los cambios realizados en un pull request, ayudando a los revisores a comprender rápidamente el alcance y el impacto de las modificaciones.
Sugerencias de revisión: obtenga recomendaciones para mejoras de código y posibles problemas antes de la revisión formal, lo que reduce los ciclos de revisión.
Resolución de conflictos de mezcla: reciba instrucciones sobre cómo resolver conflictos entre ramas, lo que simplifica el proceso de combinación.
Actualizaciones de documentación: sugerir automáticamente actualizaciones a archivos LÉAME, registros de cambios y otra documentación basada en cambios de código
Estas características ayudan a mantener la velocidad de desarrollo al reducir el esfuerzo manual necesario para preparar y revisar las solicitudes de incorporación de cambios, lo que permite a los equipos centrarse en la calidad del código en lugar de en tareas administrativas.

 Nota

Las características de generación de resúmenes de solicitudes de incorporación de cambios avanzadas y la asistencia avanzada para solicitudes de incorporación de cambios consumen unidades de solicitud Premium (PRU). Normalmente, la generación de un resumen de PR utiliza 1-2 PRU en función de la complejidad y el tamaño de los cambios. Monitorea tu uso para mantenerte dentro de los límites mensuales. Para más información sobre el consumo y los límites de PRU, consulte la documentación de Solicitudes en GitHub Copilot.

Ejemplo: "resumir los cambios en esta solicitud de incorporación de cambios y resaltar cualquier posible preocupación"

Recorte de pantalla del botón Resumen de PR de GitHub Copilot.

Los resultados muestran cómo Copilot puede generar rápidamente resúmenes completos de pr que normalmente tardarían varios minutos en escribirse manualmente:

Recorte de pantalla de GitHub Copilot que genera un resumen de la solicitud de incorporación de cambios y proporciona sugerencias de revisión en una página de solicitud de incorporación de cambios de GitHub.

Administración de problemas
Análisis de problemas: dividir problemas complejos en tareas accionables
Lluvia de ideas de la solución: generación de posibles enfoques para resolver problemas notificados
Pasos de reproducción: ayuda a crear pasos claros para reproducir errores o problemas
Ejemplo: "analice este problema y sugiera posibles soluciones con enfoques de implementación"

Recorte de pantalla de GitHub Copilot que analiza un problema de GitHub y proporciona sugerencias de solución y enfoques de implementación.

Revisión y colaboración de código
GitHub Copilot mejora el proceso de revisión de código al proporcionar información inteligente y sugerencias que ayudan a mantener la alta calidad del código y detectar posibles problemas al principio:

Comentarios de revisión: generación de comentarios de revisión de código pensativos con sugerencias específicas
Análisis de seguridad: identificar posibles vulnerabilidades de seguridad o infracciones de procedimientos recomendados
Optimización del rendimiento: sugerir mejoras para la eficiencia y el rendimiento del código
 Nota

Las características de revisión de código consumen unidades de solicitud Premium (PRU) como parte de las funcionalidades avanzadas de Copilot. Cada solicitud de revisión de código normalmente usa 1-3 PRU en función del ámbito y la complejidad del análisis. Para más información sobre el consumo de PRU, las asignaciones mensuales y los límites de tarifas, consulte la documentación de Solicitudes en GitHub Copilot.

Ejemplo: "revise este cambio de código y proporcione comentarios sobre las consideraciones de seguridad y rendimiento"

Recorte de pantalla de GitHub Copilot que genera comentarios de revisión de código con sugerencias de seguridad y rendimiento en una solicitud de incorporación de cambios.

Explicación del error en acciones de GitHub Copilot
GitHub Copilot puede ayudar a explicar y resolver errores que se producen en flujos de trabajo de Acciones de GitHub. Esta característica analiza las ejecuciones de flujo de trabajo con errores y proporciona información sobre lo que salió mal y cómo corregirlo.

Cómo explica Copilot los errores de acción
Análisis de errores: Copilot examina los archivos de registro e identifica la causa principal de los errores
Sugerencias de solución: proporciona recomendaciones específicas para resolver problemas de flujo de trabajo
Procedimientos recomendados: ofrece instrucciones sobre cómo mejorar la confiabilidad y el rendimiento del flujo de trabajo
Reconocimiento del contexto: comprende la relación entre diferentes pasos de flujo de trabajo y dependencias
Recorte de pantalla de GitHub Copilot que analiza un flujo de trabajo de Acciones de GitHub con errores y proporciona explicaciones y soluciones de errores.

## GitHub Copilot para la línea de comandos

GitHub Copilot no es solo para entornos de desarrollo integrados (IDE), ahora es un asistente eficaz en el terminal. La CLI de Copilot de GitHub lleva a Copilot directamente a la línea de comandos, donde puede explicar comandos, sugerir comandos de shell desde lenguaje natural y ayudarle a trabajar de forma segura e interactiva con los archivos y proyectos.

La CLI de Copilot usa la autenticación de GitHub y se ejecuta independientemente de la CLI de GitHub, aunque usa las credenciales existentes. Tanto si no está familiarizado con la línea de comandos como si es un desarrollador experimentado, la CLI de Copilot reduce las estimaciones y acelera los flujos de trabajo diarios.

En esta unidad se describe lo siguiente:

Instalación y ejecución de la CLI de GitHub Copilot
Sesiones interactivas en el terminal
Comandos de barra diagonal y entrada de lenguaje natural
Configuración y opciones
Instalación e inicio de la CLI de Copilot
Instale a través de Homebrew en macOS y Linux:

Bash
brew install copilot-cli
O bien, use el script de instalación oficial:

Bash
curl -fsSL https://gh.io/copilot-install | bash
Inicie la CLI de Copilot en modo interactivo:

Bash
copilot
Muestra un banner de bienvenida y una solicitud:

Captura de pantalla del banner del modo interactivo de Copilot.

En el primer inicio, Copilot pregunta si confía en los archivos de la carpeta actual. Copilot puede leer, modificar o ejecutar archivos en este directorio durante la sesión, por lo que solo puede continuar en ubicaciones de confianza.

Captura de pantalla del directorio de especificación interactiva de Copilot.

Puede usar @ para seleccionar un archivo específico con el que desea trabajar como contexto.

Captura de pantalla de la selección de un archivo en modo interactivo de copilot.

Dentro de una sesión interactiva, puede hacer lo siguiente:

Use comandos de barra diagonal (/command) para controlar la sesión y configurar la CLI de Copilot.
Escriba mensajes de lenguaje natural para explicar, sugerir o revisar comandos.
En solicitudes de un solo uso sin entrar en modo interactivo completo:

Bash
copilot -i "explain brew install git"
copilot -i "suggest find large files and delete them"
Comandos de barra diagonal comunes
Los comandos slash son comandos explícitos de control de sesión. Estos son los más comunes:

Comando de barra diagonal	Description
/help	Mostrar comandos y opciones disponibles
/explain <command>	Pida a Copilot que explique cualquier comando de shell
/suggest <task>	Pida a Copilot que sugiera un comando de shell para una tarea
/revise	Revise la última sugerencia en función de las instrucciones.
/feedback	Enviar comentarios sobre una respuesta o sugerencia
/exit	Salir del modo interactivo
/model <model>	Selección del modelo de IA que se va a usar
/theme [auto|dark|light]	Cambiar el tema del terminal
/skills	Administración de aptitudes para funcionalidades mejoradas
/mcp	Administración de la configuración del servidor MCP
/list-dirs	Mostrar directorios permitidos para las operaciones de archivo
/reset-allowed-tools	Restablecimiento de la lista de herramientas permitidas
Los comandos de barra diagonal no se pueden reemplazar por mensajes de lenguaje natural. Son la única manera de controlar los ajustes de sesión y la configuración.

Flujos de trabajo de ejemplo
1. Explicar un comando
text
> Explain what `git reset --hard HEAD` does
Copilot proporcionará una explicación detallada.

Captura de pantalla de la CLI de Copilot que explica un comando en modo interactivo.

2. Sugerir un comando
text
> Find and delete all .log files in my home folder
Copilot genera una sugerencia de comando y le pide que lo ejecute si está satisfecho con sus sugerencias.

Captura de pantalla de la CLI de Copilot que sugiere un comando en modo interactivo.

3. Revisar una sugerencia
Después de recibir una sugerencia, puede escribir un aviso de seguimiento para revisar el comando sugerido:

text
> Include only files modified in the last 7 days
Captura de pantalla de la CLI de Copilot que mejora una sugerencia en función del aviso de seguimiento.

4. Proporcionar comentarios
Después de una respuesta o sugerencia:

text
> /feedback
Captura de pantalla del uso del comando /feedack slash en el modo interactivo de la CLI de Copilot.

Copilot le pide que elija el tipo de comentarios que desea enviar y, a continuación, navegue hasta el formulario adecuado para completar sus comentarios.

5. Salir del modo interactivo
text
> /exit
Opciones de configuración
En la CLI de Copilot, la configuración se controla mediante:

Comandos de barra diagonal dentro del modo interactivo

/model elegir el modelo de IA
/theme cambiar el tema del terminal
/skills administración de funcionalidades mejoradas
/reset-allowed-tools restablecimiento de herramientas
/list-dirs ver directorios permitidos
/mcp Configuración del servidor MCP
Configuración de la CLI de Copilot (modo no interactivo)

La configuración de la CLI de Copilot se administra mediante avisos de permisos, marcas de línea de comandos y archivos de configuración local. Esta configuración controla lo que Copilot puede acceder y hacer en su nombre.

Entre las opciones de configuración comunes se incluyen:

Directorios de confianza: controle dónde Copilot puede leer, editar y ejecutar archivos.
Permisos de herramienta: permita o restrinja a Copilot de ejecutar comandos de shell o modificar archivos mediante marcas como --allow-tool o --deny-tool.
Permisos de ruta de acceso: controle a qué directorios puede acceder Copilot.
Permisos de dirección URL: administre a qué dominios externos puede conectarse Copilot.
Consulte la documentación oficial de la CLI de GitHub Copilot para ver las opciones de configuración completas.

Sugerencias para un uso eficaz
Use el modo interactivo (copilot) para tareas exploratorias.
Use el modo one-shot (copilot -i) para obtener respuestas rápidas.
La entrada del lenguaje natural funciona: no siempre necesita comandos de barra diagonal.
Revise siempre los comandos antes de la ejecución.
Combine la CLI de Copilot con la CLI de GitHub (gh) para la administración de problemas y repositorios.
Use comandos de barra diagonal cuando desee acciones estructuradas o comentarios.

## Resumen
Enhorabuena por completar este módulo. Ha obtenido información valiosa sobre las distintas formas de interactuar con GitHub Copilot, lo que mejora su capacidad de aprovechar esta eficaz herramienta de codificación asistida por IA de forma eficaz. Con la finalización de este módulo, ahora tiene los conocimientos para:

Obtenga información sobre cómo usar las sugerencias automáticas de GitHub Copilot y varios panel de sugerencias para una finalización eficaz del código.
Comprenda cómo GitHub Copilot se adapta a diferentes estilos de codificación e incorpora comentarios de codificación para obtener sugerencias mejoradas.
Utiliza de forma eficaz el Chat de GitHub Copilot para la generación de código complejo, asistencia en depuración y explicaciones de código.
Mejore las respuestas del chat de Copilot mediante referencias de ámbito, comandos de barra diagonal y agentes de Copilot.
Interactúe con GitHub Copilot a través de la interfaz de la línea de comandos, incluida la obtención de explicaciones y sugerencias de comandos.
Configure las opciones de la CLI de Copilot de GitHub, incluida la configuración de alias y las preferencias de control de datos.
Referencias
Documentación de GitHub Copilot
Documentación del chat de GitHub Copilot
Documentación de la CLI de GitHub
Proporcionar comentarios
Use este formulario de problema para proporcionar comentarios de contenido o cambios sugeridos para este módulo de Microsoft Learn. GitHub mantiene este contenido y un miembro del equipo evaluará la solicitud. Gracias por tomar el tiempo para mejorar nuestro contenido!
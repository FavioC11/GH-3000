# Desarrollo de pruebas unitarias mediante herramientas de Copilot de GitHub

## Introducción
Las pruebas unitarias son un aspecto fundamental del desarrollo de software que garantiza la funcionalidad de los componentes individuales dentro de un sistema.

En este módulo se presenta cómo generar pruebas unitarias con GitHub Copilot en Visual Studio Code. El módulo se centra en el uso de la vista Chat en modo agente ( con los modos Ask y Plan disponibles para el análisis y la planificación) y sugerencias de texto fantasma para crear y mantener pruebas unitarias para el marco de pruebas xUnit. Visual Studio Code y la extensión del Kit de desarrollo de C# proporcionan el entorno que hospeda el proyecto de prueba y ejecuta las pruebas.

Imagine que es desarrollador de software que trabaja en una gran base de código. El equipo se encarga de garantizar la confiabilidad del código. Determina que se necesitan pruebas unitarias para la mayoría del código base. Sin embargo, la creación de pruebas unitarias manualmente puede llevar mucho tiempo y ser propensa a errores. Necesita una herramienta que le ayude a desarrollar pruebas unitarias de forma rápida y precisa. La herramienta también debe ayudar a identificar casos perimetrales y condiciones de límite. Escucha que GitHub Copilot puede acelerar el desarrollo de pruebas unitarias y ayudar a identificar casos perimetrales. Tienes ganas de desarrollar pruebas unitarias de forma más rápida y precisa mediante GitHub Copilot.

Los temas tratados en este módulo incluyen:

Usar Visual Studio Code y el Kit de desarrollo de C# para hospedar y ejecutar pruebas unitarias.
Generación de pruebas unitarias en la vista Copilot Chat de GitHub mediante el modo agente (con el modo Preguntar para el análisis inicial).
Planificación y automatización de flujos de trabajo de pruebas de varios archivos con los agentes Plan y Agent.
Extensión de pruebas con sugerencias de texto fantasma y corrección de pruebas con errores con GitHub Copilot.
Desarrollo de pruebas unitarias para una aplicación de C# de un extremo a otro.
Después de completar este módulo, podrá:

Describir cómo Visual Studio Code, el SDK de .NET y el Kit de desarrollo de C# admiten pruebas unitarias para proyectos de C#.
Use el modo Agente en la vista de Copilot Chat de GitHub para generar pruebas unitarias para archivos y selecciones, y use el modo Preguntar para explorar primero las opciones de prueba.
Usa el agente Plan para diseñar una estrategia de pruebas y el agente Agent para automatizar flujos de trabajo de pruebas de varios pasos.
Use sugerencias de texto fantasma, explorador de pruebas y el /fixTestFailure comando de barra diagonal para ampliar la cobertura y reparar las pruebas con errores.
Aplique las funcionalidades de GitHub Copilot para simplificar el desarrollo de pruebas unitarias para una aplicación de C# en Visual Studio Code.
 Importante

Para completar este GitHub Copilot entrenamiento, debe tener una suscripción activa para GitHub Copilot en su cuenta personal de GitHub (incluye el plan gratis de GitHub Copilot) o debe estar asignado a una suscripción administrada por una organización o empresa. Las actividades del módulo pueden incluir sugerencias de GitHub Copilot que coincidan con el código público. Si es miembro de una organización en GitHub Enterprise Cloud a quien se le ha asignado una suscripción de GitHub Copilot a través de su organización, la configuración de sugerencias que coincida con el código público se puede heredar de la organización o de la empresa. Si su cuenta bloquea sugerencias que coinciden con el código público, es posible que las actividades del módulo no funcionen según lo previsto.

## Examen de la compatibilidad de Visual Studio Code con pruebas unitarias
Para poder generar pruebas unitarias con GitHub Copilot, el proyecto necesita un marco de pruebas de trabajo y una manera de ejecutar pruebas dentro de Visual Studio Code. Visual Studio Code, el SDK de .NET y la extensión C# Dev Kit proporcionan el entorno que hospeda las pruebas unitarias, mientras que GitHub Copilot se centra en generar y refinar el código de prueba. Comprender el entorno subyacente hace que el flujo de trabajo de GitHub Copilot sea mucho más fácil de seguir.

En esta unidad se examinan las características de Visual Studio Code y las herramientas de C# que admiten pruebas unitarias. Las unidades posteriores se centran en cómo GitHub Copilot genera y mantiene el código de prueba que se ejecuta en este entorno.

Visual Studio Code soporte para pruebas unitarias
Para crear y ejecutar pruebas unitarias de C# en Visual Studio Code, necesita los siguientes recursos:

El SDK de .NET 8.0 o posterior.
Extensión del Kit de desarrollo de C# para Visual Studio Code.
Un paquete de marco de prueba agregado al proyecto.
Compatibilidad del kit de desarrollo de C# para pruebas unitarias
La extensión kit de desarrollo de C# proporciona las características de prueba que se usan en este módulo:

Explorador de pruebas: vista de árbol que muestra todos los casos de prueba del área de trabajo. Para abrir el Explorador de pruebas, seleccione el icono de beaker en la barra actividad.
Ejecutar o depurar casos de prueba: los botones de reproducción verde aparecen en el editor junto a cada clase y método de prueba. Haga clic con el botón derecho en un botón de reproducción para ver más opciones.
Ver los resultados de las pruebas: después de ejecutar una prueba, el resultado se refleja en las decoraciones del editor y en el Explorador de pruebas. Al seleccionar un vínculo en un seguimiento de pila, se desplaza a la ubicación de origen.
Comandos de prueba: los comandos como Test: Run All Tests están disponibles en la paleta de comandos. Busque Test: para ver la lista completa.
Configuración de pruebas: la configuración que controla la detección de pruebas y el comportamiento en tiempo de ejecución están disponibles en el editor de configuración. Busque Testing para ver las opciones disponibles.
El Kit de desarrollo de C# es compatible con los siguientes marcos de pruebas:

xUnit
NUnit
MSTest (herramienta de pruebas de Microsoft)
Creación de un proyecto de prueba mediante la paleta de comandos
La paleta de comandos de Visual Studio Code proporciona la manera más fácil de crear un proyecto de prueba que use un marco compatible. Puede abrir la paleta de comandos de las siguientes formas:

Presione las teclas Ctrl + Shift + P (Windows/Linux) o Cmd + Shift + P (macOS).
Abra el menú Vista y después seleccione Paleta de comandos.
Abra la vista Explorador de soluciones, haga clic con el botón derecho en la carpeta de la solución y seleccione Nuevo proyecto. Esta opción abre la paleta de comandos con el .NET: Nuevo Project... comando ya seleccionado.
En las secciones siguientes se muestra cómo crear un proyecto de prueba para cada marco compatible.

xUnit
Abra la paleta de comandos y seleccione .NET: Nuevo Project... , seleccione xUnit Test Project y proporcione un nombre y una ubicación para el nuevo project. Este comando crea un proyecto que usa xUnit como biblioteca de pruebas y configura el ejecutor de pruebas agregando los siguientes <PackageReference /> elementos al archivo del proyecto:

Microsoft.NET.Test.Sdk
xUnit
xunit.runner.visualstudio
coverlet.collector
Desde el terminal integrado, puede agregar una referencia desde el proyecto de prueba al proyecto en prueba:

CLI de .NET
dotnet add [location of your test csproj file] reference [location of the csproj file for project to be tested]
NUnit
Abra la paleta de comandos y seleccione .NET: Nuevo Project... , seleccione NUnit3 Test Project y proporcione un nombre y una ubicación para el nuevo project. Este comando crea un proyecto que usa NUnit como biblioteca de pruebas y agrega los siguientes <PackageReference /> elementos al archivo del proyecto:

Microsoft.NET.Test.Sdk
NUnit
NUnit3TestAdapter
Agregue una referencia al proyecto en prueba desde terminal:

CLI de .NET
dotnet add [location of your test csproj file] reference [location of the csproj file for project to be tested]
MSTest (herramienta de pruebas de Microsoft)
Abra la paleta de comandos y seleccione .NET: Nuevo Project... , seleccione MSTest Test Project y proporcione un nombre y una ubicación para el nuevo project. Este comando agrega los siguientes <PackageReference /> elementos al archivo de proyecto:

Microsoft.NET.Test.Sdk
MSTest.TestAdapter
MSTest.TestFramework
coverlet.collector
Agregue una referencia al proyecto en prueba desde terminal:

CLI de .NET
dotnet add [location of your test csproj file] reference [location of the csproj file for project to be tested]
Ejecución y administración de pruebas unitarias en Visual Studio Code
Una vez que existe un proyecto de prueba, Visual Studio Code y el Kit de desarrollo de C# ofrecen varias maneras de ejecutar y administrar pruebas:

Ejecutar o depurar desde el editor: seleccione el botón de reproducción verde situado junto a una clase o método para ejecutar ese destino. Haga clic con el botón derecho en el botón de reproducción para ver opciones como Ejecutar prueba y depurar prueba.
Explorador de pruebas: ejecute o depure pruebas individuales, grupos o el conjunto completo desde la vista de árbol. Los resultados de las pruebas, incluidos los iconos de paso y error y las duraciones, aparecen junto a cada elemento.
Ver los resultados de las pruebas: las decoraciones del editor y el Explorador de pruebas reflejan el estado actual de cada prueba después de una ejecución. Seleccione enlaces en los seguimientos de pila para saltar a la línea que provoca el error.
Comandos de prueba: use comandos como Test: Run All Tests, Test: Debug Failed Testsy Test: Show Output desde la paleta de comandos.
Configuración de prueba: Busque Testing en el editor de configuración para configurar opciones como la ejecución automática al guardar o el formato de los resultados de las pruebas.
Flujo de trabajo de pruebas unitarias con GitHub Copilot
Al combinar Visual Studio Code con GitHub Copilot, el proceso de prueba unitaria se divide en tres fases:

Set up the environment: Use Visual Studio Code, el SDK de .NET y el Kit de desarrollo de C# para crear un proyecto de prueba y hacer referencia al proyecto en prueba. Ha completado esta fase en esta unidad.
Generar código de prueba: use GitHub Copilot en la vista Chat para generar pruebas unitarias para el código de la aplicación. Las siguientes unidades cubren esta fase.
Ejecutar y mantener pruebas: Use el Explorador de pruebas y el Kit de desarrollo de C# para ejecutar pruebas y, a continuación, use GitHub Copilot para ampliar la cobertura y corregir las pruebas con errores.
Las unidades restantes se centran en las herramientas de GitHub Copilot que admiten las fases 2 y 3.

## Generación de pruebas unitarias con la vista de Copilot Chat de GitHub
La vista Chat de Visual Studio Code es el lugar principal para generar pruebas unitarias con GitHub Copilot. Desde la vista Chat, puede configurar un marco de pruebas, generar pruebas para un archivo o selección y refinar los resultados hasta que las pruebas coincidan con las convenciones del proyecto. Esta unidad se centra en el modo agente, que escribe pruebas generadas directamente en un archivo de prueba, puede ejecutar las pruebas resultantes e iterar en los errores, todo ello desde un único mensaje de chat. También puede usar el modo Preguntar de antemano para explorar las opciones de prueba sin realizar ningún cambio en el archivo.

Abrir la vista Chat
Abra la vista Chat con cualquiera de las siguientes opciones:

Presione Ctrl + Alt + I (Windows//Linux) o Cmd + Alt + I (macOS).
Seleccione el icono de GitHub Copilot en la barra de título y, a continuación, seleccione Toggle Chat.
La vista Chat se abre en la barra lateral secundaria y proporciona tres opciones de configuración que afectan a cada mensaje que envíe:

Destino del agente: donde se ejecuta el agente. Seleccione Local para ejecutar el agente de forma interactiva en el editor con acceso completo al área de trabajo, las herramientas y los modelos.
Agente: el rol que toma la inteligencia artificial para la sesión. Los agentes locales integrados son Ask, Plan y Agent.
Nivel de permiso: la autonomía que tiene el agente al invocar herramientas y comandos de terminal. Las opciones son Aprobaciones predeterminadas, Omisión de aprobaciones y Autopilot.
Para la generación de pruebas unitarias, el punto de partida recomendado es el Agente con aprobaciones predeterminadas. El modo de agente puede editar archivos, ejecutar comandos de terminal y volver a ejecutar pruebas, por lo que puede tomar un mensaje como "generar pruebas para este método" y generar un archivo de prueba de trabajo que solo necesite revisar. Las aprobaciones predeterminadas le mantienen informado al pedirle que confirme cada vez que se ejecuta una herramienta.

Opcionalmente, use el modo Preguntar para explorar primero las opciones de prueba.
Haga respuestas a preguntas en el modo de chat sin modificar archivos ni invocar herramientas. Esto hace que sea una buena opción cuando quiera planear un enfoque antes de permitir que el Agente cambie cualquier cosa. Use el modo Preguntar cuando desee:

Compare los posibles casos de prueba para un método complejo antes de decidirse por una estructura.
Identifique los casos perimetrales y las condiciones de límite que merece la pena cubrir.
Obtenga una recomendación para un marco de pruebas o un estilo de aserción.
Vea un ejemplo de prueba en chat sin escribirlo en el disco.
Para usar el modo Preguntar para el análisis:

Abra la vista Chat y seleccione Preguntar en el selector del agente.

Adjunte el archivo o la selección pertinentes como contexto (por ejemplo, con #selection o arrastrando un archivo en).

Haga una pregunta de análisis. Por ejemplo: What edge cases should I cover when testing the CalculateDiscount method? List the scenarios and explain why each one matters.

Revise la respuesta y cambie el selector del agente al Agente para generar las pruebas reales.

Configuración de un marco de pruebas con /setupTests
Si el proyecto aún no tiene configurado un marco de pruebas, GitHub Copilot puede recomendar uno y guiarle por los pasos de configuración. El /setupTests comando de barra diagonal funciona en cualquier agente, pero el modo agente también puede instalar paquetes y crear el proyecto de prueba automáticamente.

Abra la vista Chat y seleccione Agente en el selector de agentes.

Escriba el /setupTests comando en el campo de entrada del chat.

Confirme las invocaciones de herramientas y los comandos de terminal que sugiere el Agente para instalar paquetes, generar la estructura del proyecto de prueba y recomendar las extensiones de prueba para Visual Studio Code.

/setupTests resulta más útil cuando se inicia un nuevo proyecto de prueba o se incorpora un proyecto que aún no incluye pruebas.

Generación de pruebas con /tests
El /tests comando de barra diagonal genera pruebas unitarias para el código que está activo actualmente en el editor. En el modo Agente, las pruebas generadas se escriben directamente en un archivo de prueba adecuado. GitHub Copilot detecta el marco de pruebas existente y el estilo de codificación y genera pruebas que coinciden.

Para generar pruebas para un archivo completo:

Abra el archivo de código de la aplicación que desea probar.

Abra la vista Chat y confirme que el Agente está seleccionado.

En el campo de entrada de chat, escriba /tests seguido de cualquier guía adicional. Por ejemplo: /tests Generate unit tests for the methods in this file. Include success, failure, and edge cases.

Confirme las invocaciones de las herramientas que usa el Agente para leer el contexto, escribir las pruebas y, opcionalmente, ejecutarlas.

Revise los cambios aplicados por el Agente.

El Agente anexa pruebas a un archivo de prueba existente cuando hay uno disponible o crea un nuevo archivo de prueba en la ubicación adecuada. La diferencia aparece en el editor para que pueda comprobar cada cambio.

Seleccione Mantener o Deshacer para aceptar o descartar los cambios.

Para generar pruebas para un método específico o bloque de código:

Abra el archivo de código de la aplicación.

Seleccione el método o bloque que desea probar.

En la vista Chat, escriba /tests seguido de instrucciones que hagan referencia a la selección. Por ejemplo: /tests Generate unit tests for the selected method. Validate both success and failure, and include edge cases.

Revise y mantenga o descarte los cambios resultantes.

Generación de pruebas con un mensaje de lenguaje natural
No tiene que usar un comando de barra diagonal. El agente genera pruebas a partir de mensajes de lenguaje natural cuando se incluye suficiente contexto. Ejemplos:

"Genere pruebas xUnit para los métodos de este archivo y agréguelas al proyecto Calculator.Tests".
Escriba pruebas unitarias para el método CalculateDiscount, incluyendo los casos límite para valores negativos y cero. Ejecute las pruebas después de escribirlas".
"Cree pruebas de integración para la capa de acceso a datos en este módulo".
Dado que el agente puede ejecutar comandos, puedes incluir pasos de verificación en el mismo prompt. Pedir al Agente que ejecute las pruebas después de escribirlas le permite detectar y corregir errores obvios antes de devolverle el trabajo.

Añade contexto a tus indicaciones
La calidad de las pruebas generadas depende del contexto que proporcione. Usa una o varias de las opciones siguientes para adjuntar contexto a una solicitud de la vista Chat:

Botón Agregar contexto: abra una selección rápida para agregar archivos, carpetas, símbolos o la selección del editor actual.
Arrastrar y colocar: arrastre archivos desde la vista Explorador o arrastre una pestaña del editor hasta la vista Chat para adjuntar el contenido.
# menciones: escriba # seguido de un nombre de archivo, carpeta o símbolo para agregarlo como contexto. Use #selection para adjuntar la selección del editor actual o #codebase para permitir que GitHub Copilot busque el contexto pertinente en el área de trabajo.
Archivos externos: abra archivos markdown (por ejemplo, directrices de colaborador o convenciones de prueba) en el editor y adjuntelos a través de Agregar contexto. El agente usa el contenido para dar forma a las pruebas generadas.
Por ejemplo, si un único método está visible en el editor, puede preguntar: Write a unit test for the method in #editor. Si hay varios métodos visibles o el método de destino se extiende más allá del área visible, seleccione primero el código y pregunte: #selection write unit tests for the selected code.

Revisar y refinar los cambios del agente
Aunque el Agente escribe pruebas directamente en tu proyecto de pruebas, sigues teniendo el control:

Revise la diferencia: cada archivo que el Agente cambia se abre en el editor con las modificaciones propuestas resaltadas. Revise los cambios antes de aceptarlos.
Mantener o deshacer: use Mantener para aceptar los cambios o Deshacer para revertirlos. También puede revertir bloques individuales desde el editor.
Compilación y ejecución: después de mantener los cambios, compile el proyecto de prueba y ejecute las pruebas desde el Explorador de pruebas o el terminal para confirmar que todo se compila y supera.
Iteración: use avisos de seguimiento en la misma sesión de chat para refinar pruebas específicas, agregar más casos o cambiar el nombre de los métodos.
Personalización de la generación de pruebas con instrucciones personalizadas
Si su organización tiene requisitos de prueba específicos, puede personalizar cómo GitHub Copilot genera pruebas para que la salida coincida con los estándares. Las instrucciones personalizadas le permiten:

Especifique marcos de pruebas preferidos (por ejemplo, xUnit en lugar de NUnit).
Defina las convenciones de nomenclatura para las clases y métodos de prueba.
Establezca preferencias de estructura de código como el patrón Arrange-Act-Assert.
Solicite patrones de prueba específicos, como pruebas parametrizadas para los valores de límite.
Almacene instrucciones personalizadas en un *.instructions.md archivo del área de trabajo. Use el applyTo campo de metadatos para aplicar las instrucciones solo para probar archivos. Por ejemplo, un applyTo: tests/** valor limita las instrucciones a los archivos del tests/ directorio. El uso compartido del archivo en el control de código fuente proporciona a todos los desarrolladores del equipo el mismo contexto de prueba.

 Importante

Es posible que los casos de prueba generados no cubran todos los escenarios. La revisión manual y la revisión de código siguen siendo necesarias para garantizar la calidad de las pruebas.

## Planeamiento y automatización de flujos de trabajo de prueba mediante los modos Plan y Agent
La unidad anterior utilizó el modo Agente para generar pruebas a partir de una sola instrucción en la vista Chat. Las tareas de prueba más grandes suelen necesitar más estructura: decidir qué probar, aplicar scaffolding a un proyecto de prueba, generar pruebas en varios archivos y ejecutar el conjunto resultante. El agente Plan y las sesiones de Agent más largas en la vista Chat están diseñados para ese nivel de trabajo. Use el agente de plan para diseñar una estrategia de prueba antes de escribir cualquier código y, a continuación, entregar el plan aprobado al agente para la implementación autónoma y en varios pasos.

Comparativa de agentes de consulta (Ask), planificación (Plan) y ejecución (Agent)
La vista Chat proporciona tres agentes locales integrados. Cada uno está optimizado para un tipo diferente de tarea de prueba.

Agente	Más adecuado para	Uso típico en pruebas unitarias
Preguntar	Análisis de solo lectura y preguntas y respuestas sobre tu código	Explore casos perimetrales, opciones de marco o pruebas de ejemplo antes de escribir cualquier código.
Plan	Planes de implementación estructurados y paso a paso	Diseñe una estrategia de prueba de varios archivos que puede revisar antes de la implementación.
Agent	Flujos de trabajo autónomos y de codificación de varios archivos	Generar pruebas directamente en un proyecto de pruebas, ejecutarlas y repetir el proceso corrigiendo los errores.
Para elegir un agente, selecciónelo en el selector de agentes en la vista Chat. Puede cambiar los agentes en cualquier momento durante una sesión.

 Importante

Al usar la vista Chat con el Agente, GitHub Copilot puede realizar varias solicitudes Premium para completar una sola tarea. Las solicitudes Premium se utilizan tanto para las indicaciones iniciadas por el usuario como para las acciones posteriores que realiza el agente en su nombre. El total de solicitudes premium usadas depende de la complejidad de la tarea, del número de pasos y del modelo que seleccione.

Usa el agente Plan para diseñar una estrategia de pruebas
El agente de plan genera un plan de implementación detallado antes de escribir cualquier código. El agente investiga la tarea, formula preguntas aclarantes y propone un plan paso a paso que puede revisar, refinar y entregar al Agente.

Para planear un conjunto de pruebas unitarias:

Abra el archivo o los archivos que contienen el código que desea probar.

Abra la vista Chat y seleccione Plan en el selector del agente. Como alternativa, escriba /plan seguido de la descripción de la tarea.

Escriba un mensaje que describa las pruebas que desea crear. Por ejemplo:

I need unit tests for the methods in the Calculator class. Use xUnit. Include tests for success, failure, and boundary conditions. Place the new tests in the Calculator.Tests project.

Responda a cualquier pregunta aclarante.

El agente de plan puede preguntar sobre las preferencias del marco de pruebas, las convenciones de nomenclatura o cómo controlar las dependencias antes de redactar el plan.

Revise el plan propuesto.

El plan normalmente incluye un resumen de alto nivel, un desglose de los pasos, los pasos de comprobación para ejecutar las pruebas y las decisiones documentadas. Itere con el agente de planificación hasta que el plan refleje lo que quiera crear.

Envíe el plan para la implementación.

Cuando el plan sea final, seleccione la opción para iniciar la implementación. Puede implementar el plan en la misma sesión de chat o puede iniciar una sesión en segundo plano o en la nube para trabajar en la implementación de forma autónoma. También puede abrir el plan en el editor para su posterior revisión.

El agente de plan es especialmente útil cuando la tarea de prueba abarca varios archivos, requiere nuevas clases de prueba o accesorios, o necesita alinearse con las convenciones de equipo que aún no se capturan en las instrucciones.

Uso del agente para automatizar flujos de trabajo de prueba
El agente automatiza tareas de varios pasos en todo tu espacio de trabajo. Para las pruebas unitarias, puede usar el Agente para aplicar scaffolding a un proyecto de prueba, crear archivos de prueba, ejecutar las pruebas resultantes, generar informes de prueba o corregir problemas que se muestran durante una ejecución de pruebas.

Para usar el agente para crear y ejecutar pruebas unitarias:

Abra el archivo que contiene el código que desea probar.

Abra la vista Chat y seleccione Agente en el selector de agentes.

Deje que el Agente determine el contexto.

Al usar el Agente, GitHub Copilot identifica automáticamente los archivos pertinentes. También puede adjuntar contexto adicional con el botón Agregar contexto o arrastrando archivos a la vista Chat.

Opcionalmente, seleccione el icono Herramientas para elegir las herramientas que el Agente puede usar para la tarea.

Entre las herramientas útiles para las tareas de prueba se incluyen las herramientas de edición de archivos, la herramienta de terminal para ejecutar dotnet testy las herramientas de prueba proporcionadas por la extensión.

Escriba un mensaje que defina la tarea. Por ejemplo:

Ensure that a suitable unit test project is prepared for the selected code file. Create a test file in the unit test project that includes unit tests for all methods in the selected file. Unit tests should be written in C# and use the xUnit framework. Run the tests to ensure expected results.

Monitorice al agente mientras trabaja.

Confirme o rechace las invocaciones de herramientas y los comandos de terminal que sugiere el Agente. Por ejemplo, puede confirmar el comando para ejecutar las pruebas o para generar un informe de prueba.
Interrumpa el agente si necesita cambiar el contexto, cambiar las herramientas o ajustar el ámbito de la tarea.
Revise los archivos que creó o actualizó el Agente y, a continuación, mantenga o descarte los cambios.

Use avisos de seguimiento para refinar pruebas específicas si es necesario.

Decidir cuándo usar Plan, Agent o ambos
Use las instrucciones siguientes para elegir entre los agentes:

Usa primero el agente Plan cuando el trabajo de pruebas implique ambigüedad, varios archivos o convenciones del equipo que deban confirmarse. El plan se convierte en un contrato que puede revisar antes de escribir cualquier código.
Use el agente directamente cuando la tarea esté bien definida y quiera que GitHub Copilot cree la estructura inicial, genere y ejecute pruebas sin un paso intermedio de planificación.
Utiliza Plan y luego pásalo a Agent cuando quieras un plan revisable y una implementación autónoma. Esta combinación le proporciona el mayor control sobre el ámbito al mismo tiempo que automatiza el trabajo.


## Extensión de pruebas con texto fantasma y corrección de pruebas con errores
Después de que el proyecto de prueba contenga algunos casos de prueba, GitHub Copilot puede ayudarle a ampliar la cobertura y resolver los errores sin salir de Visual Studio Code. Las sugerencias de texto fantasma agregan casos de prueba adicionales dentro del archivo que está editando, mientras que el Explorador de pruebas y el /fixTestFailure comando de barra diagonal le ayudan a diagnosticar y corregir las pruebas con errores. Juntas, estas características cierran el bucle en el flujo de trabajo de pruebas unitarias que inició en la vista Chat.

Ampliación de r la cobertura de pruebas con sugerencias de texto fantasma
El texto fantasma es la finalización del código insertado que aparece al escribir en el editor. Cuando un archivo de prueba ya contiene algunos casos de prueba, GitHub Copilot usa los patrones existentes para sugerir casos de prueba similares para escenarios adicionales. Esta es la forma más rápida de ampliar la cobertura una vez que las pruebas iniciales ya están preparadas.

Para ampliar un archivo de prueba con texto fantasma:

Abra un archivo de prueba que contenga al menos uno o dos casos de prueba completos.

Coloque el cursor al final del último caso de prueba y presione Entrar para iniciar una nueva línea.

Comience a escribir un nuevo método de prueba o escriba un comentario descriptivo como // Test that ProcessOrder throws when the order total is negative.

GitHub Copilot muestra una sugerencia de texto fantasma que completa el método de prueba en función del código circundante, las importaciones y los patrones de prueba existentes.

Presione Tab para aceptar la sugerencia o presione Esc para descartarla.

Refina la sugerencia aceptada según sea necesario. Puede seguir escribiendo para ampliar la prueba o puede desencadenar la siguiente sugerencia de texto fantasma presionando Entrar.

El texto fantasma funciona mejor cuando:

El archivo de prueba ya muestra el patrón que desea GitHub Copilot seguir (por ejemplo, Arrange-Act-Assert structure o un atributo de prueba con parámetros).
Se hace referencia al método sometido a prueba en el archivo mediante una using directiva o un espacio de nombres importado.
El comentario indica claramente el escenario que desea probar.
 Sugerencia

Use texto fantasma para agregar casos perimetrales a una clase de prueba existente rápidamente. Para un trabajo más sustancial, como crear una clase de prueba completamente nueva, vuelva a la vista Chat y use los agentes Ask, Plan o Agent.

Corrección de pruebas con errores desde el Explorador de pruebas
Cuando se produce un error en una prueba, el Explorador de pruebas proporciona un punto de entrada con un solo clic en GitHub Copilot.

Ejecute las pruebas desde el Explorador de pruebas o desde el botón de reproducción verde situado junto a un método de prueba.

En el Explorador de pruebas, mantenga el puntero sobre una prueba con error.

Seleccione el botón Corregir error de prueba (icono de sparkle).

GitHub Copilot abre una sesión de chat, adjunta la prueba con errores y su salida como contexto y propone una corrección.

Revise la corrección propuesta.

La sugerencia puede actualizar el código de la aplicación, el código de prueba o ambos, en función de la causa del error.

Aplique o descarte la sugerencia.

Use Conservar para aplicar los cambios sugeridos o use Deshacer para descartarlos. Vuelva a ejecutar la prueba para confirmar la corrección.

Corrige las pruebas que fallan con /fixTestFailure
También puede iniciar el flujo de trabajo de corrección desde la vista Chat, que es útil cuando desea adjuntar contexto adicional o cuando esté trabajando en varias pruebas con errores a la vez.

Abra la vista Chat.

Escriba el comando de barra oblicua /fixTestFailure.

Opcionalmente, adjunte contexto adicional, como archivos de origen relacionados o salida de terminal reciente.

Siga las sugerencias de GitHub Copilot para corregir la prueba con errores y vuelva a ejecutar la prueba para confirmar la corrección.

Permitir que el agente supervise y corrija los errores automáticamente
Cuando se usa el Agente para ejecutar pruebas, supervisa la salida de la prueba, identifica los errores e intenta corregir y volver a ejecutar las pruebas automáticamente. Esto resulta útil cuando se crea la estructura inicial de un nuevo proyecto de pruebas o se realizan cambios importantes que afectan a muchas pruebas de una sola vez.

Para usar el Agente para el mantenimiento automático de pruebas:

Abra la vista Chat y seleccione Agente en el selector de agentes.

Proporcione un mensaje que incluya la ejecución de las pruebas, como: Run the xUnit tests in the Calculator.Tests project. If any tests fail, propose and apply fixes, then rerun the tests until they pass.

Confirme o rechace las invocaciones de herramientas y los comandos de terminal que sugiere el Agente.

Revise los cambios aplicados por el Agente antes de aceptarlos.

Elección de la herramienta adecuada para el trabajo
Use las instrucciones siguientes para decidir qué característica usar:

El texto fantasma es mejor cuando desea agregar más casos de prueba a un archivo de prueba existente que ya muestra el patrón.
Corregir error en la prueba en el Explorador de pruebas es la mejor opción cuando falla una sola prueba y desea una corrección rápida y específica.
/fixTestFailure en la vista de chat es mejor cuando se desea adjuntar contexto adicional o resolver varios fallos.
Ejecuciones de pruebas controladas poragentes son las mejores cuando desea GitHub Copilot ejecutar pruebas, diagnosticar errores y aplicar correcciones en varios archivos en una sesión.
Juntas, estas herramientas completan el flujo de trabajo de pruebas unitarias. La vista de chat, el agente de Plan y el Agente generan las pruebas iniciales; el texto ficticio completa la cobertura adicional y las características de corrección de fallos en las pruebas mantienen el conjunto en verde conforme evoluciona el código.

## Ejercicio: Desarrollo de pruebas unitarias mediante GitHub Copilot
25 minutos
 Importante

Para completar este ejercicio, necesita una cuenta de GitHub activa y un entorno de Visual Studio Code configurado para el desarrollo de C#. Para obtener ayuda para configurar el entorno de laboratorio, consulte Configuración del entorno de laboratorio para GitHub Copilot Labs. Para obtener ayuda sobre cómo habilitar GitHub Copilot en Visual Studio Code, consulte Enable GitHub Copilot en Visual Studio Code.

En este ejercicio, usará GitHub Copilot para acelerar el desarrollo de pruebas unitarias para una aplicación de C#. Dichas tareas incluyen:

Use la vista Chat y el Agente para crear una nueva clase de prueba.
Use la vista chat y el modo agente para crear pruebas unitarias.
Al seleccionar el botón Iniciar ejercicio, el explorador navega a una página pública de GitHub que proporciona instrucciones para este ejercicio.

Cuando termine el ejercicio, vuelva aquí para:

Una comprobación rápida de conocimientos.
Resumen de lo que ha aprendido durante este módulo.
Un distintivo por completar este módulo.
Botón para iniciar el ejercicio.

## Resumen

En este módulo, ha aprendido a usar GitHub Copilot y Visual Studio Code para crear y mantener pruebas unitarias para proyectos de C#. Ha explorado el entorno de pruebas de Visual Studio Code proporcionado por el SDK de .NET y la extensión C# Dev Kit, incluidos el Explorador de pruebas, los comandos para ejecutar y depurar, y las infraestructuras de pruebas compatibles (xUnit, NUnit y MSTest). A continuación, ha utilizado la vista de GitHub Copilot Chat en modo Agente para generar pruebas unitarias con los comandos de barra /setupTests y /tests, y ha visto cómo el modo Preguntar le ayuda a explorar casos límite y opciones de prueba antes de permitir que el Agente cambie ningún archivo.

También ha analizado cómo el agente Plan y las sesiones de Agent más prolongadas amplían el flujo de trabajo para tareas de prueba de mayor envergadura. El agente Plan genera una estrategia de pruebas revisable antes de que se escriba ningún código, y el agente Agent automatiza flujos de trabajo de varios archivos que aplican scaffolding en los proyectos, generan pruebas y ejecutan el conjunto resultante. Por último, ha aprendido cómo las sugerencias de texto fantasma amplían la cobertura desde el editor y cómo el botón Corregir error de prueba del Explorador de pruebas y el /fixTestFailure comando de barra diagonal le ayudan a diagnosticar y resolver pruebas con errores.

La conclusión principal es que GitHub Copilot le permite desplazarse por todas las fases del flujo de trabajo de pruebas unitarias (configuración, generación, extensión y reparación) sin salir de Visual Studio Code, mientras que el Kit de desarrollo de C# mantiene el proyecto de prueba organizado y ejecutable.

Otras lecturas:

documentación de GitHub Copilot
GitHub Copilot en Visual Studio Code
Test con GitHub Copilot
Configuración de un flujo de desarrollo controlado por pruebas en VS Code
GitHub Copilot en Visual Studio Code - Guía Rápida
Pruebas con el Kit de desarrollo de C#


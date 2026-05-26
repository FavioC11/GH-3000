# Introducción al servidor MCP
## Introducción
El servidor MCP de GitHub es una manera hospedada, segura y escalable de integrar sus características favoritas de GitHub en el flujo de trabajo asistido por IA. Basado en el Protocolo de contexto de modelo (MCP), introducido por Anthropic, es compatible con todas sus herramientas de desarrollo favoritas.

Su conjunto de herramientas amplía GitHub Copilot y otras herramientas de inteligencia artificial para ayudarle a automatizar tareas, administrar repositorios y mejorar su experiencia de desarrollo con asistencia de inteligencia artificial con reconocimiento del contexto.

El servidor MCP de GitHub le ayuda a empezar a trabajar rápidamente mientras mantiene el flujo de trabajo sencillo y centrado. Está disponible para Visual Studio Code y se ampliará a otros editores y plataformas, lo que le ayudará a llevar la productividad con tecnología de inteligencia artificial a todo el proceso de desarrollo.

Objetivos de aprendizaje
Al término de este módulo, sabrá hacer lo siguiente:

Comprenda qué son MCP y el servidor MCP de GitHub y por qué son útiles para los desarrolladores.

Configure y configure el servidor MCP de GitHub en Visual Studio Code para los proyectos.

Use el servidor MCP de GitHub con Copilot Chat para automatizar las tareas de desarrollo.

Identifique y resuelva problemas comunes al trabajar con el servidor MCP de GitHub.

Prerrequisitos
Antes de empezar, asegúrese de que tiene lo siguiente:

Una cuenta de GitHub

Visual Studio Code u otro editor que admita la integración de MCP

Si es miembro de una organización o empresa con un plan de Copilot Business o Copilot Enterprise, la directiva "Servidores MCP en Copilot" debe estar habilitada para poder usar MCP con Copilot.

(Opcional)

Un token de acceso personal (PAT) de GitHub para la configuración avanzada y el control de permisos.

Docker instalado si planea experimentar con una configuración de servidor local para el control práctico.



## Simplificación del flujo de trabajo de IA con el servidor MCP de GitHub
La inteligencia artificial está cambiando la forma en que los desarrolladores trabajan, pero hacer que las herramientas de inteligencia artificial estén disponibles en todos los entornos pueden ser difíciles. El servidor MCP de GitHub lo resuelve proporcionando una manera sencilla y escalable de integrar GitHub Copilot en el código, junto con herramientas relacionadas y flujos de trabajo.

Basado en el Protocolo de contexto de modelo (MCP), el servidor MCP de GitHub elimina la fricción de la configuración y desbloquea funcionalidades eficaces de la evaluación de prioridades de problemas a la búsqueda semántica en web, móvil y escritorio.

En esta unidad, aprenderá lo siguiente:

¿Qué es MCP?

¿Por qué debe usar el servidor MCP de GitHub?

¿Cómo funciona el servidor MCP de GitHub en acción?

¿Qué es MCP?
MCP (Protocolo de contexto de modelo) es como un estándar de USB-C para las herramientas de inteligencia artificial, lo que proporciona una manera coherente y segura de que los modelos de INTELIGENCIA artificial se conecten a las herramientas y los orígenes de datos que necesitan.

Ofertas de MCP:

Acceso a una biblioteca creciente de herramientas que los modelos de IA pueden usar inmediatamente.

Flexibilidad para trabajar con diferentes proveedores de inteligencia artificial a la vez que mantiene los flujos de trabajo coherentes.

Integración en el entorno de desarrollo y los procesos existentes.

Cómo se conectan los clientes MCP a servidores y servicios
Un cliente MCP (como Claude, un IDE u otra herramienta) puede interactuar con servidores MCP y sus servicios conectados de tres maneras principales. El enfoque específico depende de si los recursos subyacentes son locales o remotos.

Comunicación local con datos locales
El cliente MCP se comunica directamente con un servidor MCP que se ejecuta en la máquina mediante el protocolo MCP. A continuación, ese servidor se conecta a un origen de datos local (por ejemplo, archivos, bases de datos u otros recursos almacenados en el equipo).

Cuándo usarlo: esta configuración es útil para el desarrollo local o en cualquier momento que desee acceder rápidamente a los datos que permanecen privados en la máquina.

Servidor local como puente a servicios remotos
El cliente MCP todavía se conecta a un servidor MCP que se ejecuta localmente. Pero en lugar de trabajar solo con datos locales, este servidor puente a un servicio remoto en Internet mediante una llamada a sus API web.

Cuándo usarlo: este modelo es común cuando una herramienta local necesita capturar o actualizar información de un servicio remoto, pero se beneficia de tener un servidor local entre ellos, por ejemplo, para controlar el almacenamiento en caché, las comprobaciones de seguridad o el preprocesamiento de datos.

Comunicación remota a través de Internet
En la configuración final, el cliente MCP se conecta a un servidor MCP que reside completamente en Internet (no en el equipo). A continuación, ese servidor remoto se comunica con otros servicios externos a través de las API web.

Cuándo usarlo: este enfoque es mejor cuando el recurso o cálculo que necesita no se puede producir localmente, como el uso de procesos basados en la nube, plataformas SaaS o integraciones de terceros que solo existen en línea.

¿Por qué usar el servidor MCP de GitHub?
En primer lugar, comprendamos por qué el servidor MCP de GitHub es importante para el flujo de trabajo. El uso de servidores MCP locales normalmente requiere Docker, administración de tokens y configuración manual, lo que puede ralentizar la configuración y bloquear la integración con clientes web como GitHub.com.

La conexión al servidor hospedado en GitHub es rápida y fácil sin necesidad de archivos docker ni config. Puede usar herramientas de inteligencia artificial como el chat de GitHub Copilot en web y móvil para escalar los proyectos a medida que crecen. El servidor MCP de GitHub admite el inicio de sesión empresarial seguro y proporciona acceso a características avanzadas, como la búsqueda semántica de código y correcciones automatizadas para aumentar el flujo de trabajo.

Entre las ventajas del servidor MCP de GitHub se incluyen:

Elimina la necesidad de archivos de configuración manual o docker.

Proporciona un inicio de sesión de OAuth sencillo con un solo clic para la autenticación rápida.

Permite trabajar sin problemas en entornos web, de escritorio y móviles.

Admite proveedores de identidades empresariales como Entra y Auth0 para la autenticación segura.

Escala automáticamente para satisfacer sus necesidades de uso.

Servidor MCP de GitHub en acción
Ahora que conoce la utilidad de MCP, vamos a explorar cómo el servidor MCP de GitHub lo pone en acción. El servidor MCP de GitHub es un servidor de código abierto que conecta GitHub Copilot y otras herramientas de inteligencia artificial directamente a los repositorios. Le permite:

Analice y resuma el código para comprender mejor los proyectos.

Cree y administre problemas y solicitudes de incorporación de cambios.

Automatice la evaluación de prioridades del repositorio y el seguimiento de tareas para ahorrar tiempo.

Actualmente, el servidor MCP de GitHub ofrece más de 30 herramientas, lo que le permite:

Agregue problemas, edite archivos y cree ramas fácilmente.

Clasificar los pull requests y los problemas para priorizar.

## Configuración, conexión y uso del servidor MCP de GitHub en VS Code
En esta unidad, aprenderá a configurar y usar el servidor MCP de GitHub en Visual Studio Code para que pueda incorporar flujos de trabajo con tecnología de inteligencia artificial directamente al entorno de desarrollo. Aprenderá lo siguiente:

Configuración mediante OAuth o un token de acceso personal (PAT)

Configuración local opcional con Docker para obtener más control

Uso del servidor MCP de GitHub con Chat de Copilot para la productividad con tecnología de IA

Pasos comunes de solución de problemas

Configuración del servidor MCP de GitHub en VS Code
Uso de OAuth
Ahora que sabe lo que puede hacer el servidor MCP de GitHub, veamos cómo configurarlo en Visual Studio Code para que pueda empezar a usarlo inmediatamente. Esto le permitirá integrar los flujos de trabajo preferidos con tecnología de inteligencia artificial directamente en el entorno de codificación sin una configuración compleja.

En Visual Studio Code, abra la paleta de comandos presionando Ctrl+Mayús+P (Windows/Linux) o Cmd+Mayús+P (Mac).
Escriba MCP: agregue el servidor y presione Entrar.
En la lista, seleccione HTTP (HTTP o Server-Sent Events).
En el campo Dirección URL del servidor , escriba https://api.githubcopilot.com/mcp/y presione Entrar.
Cuando se le pida que escriba un identificador de servidor, puede presionar Entrar para usar el valor predeterminado o escribir un identificador personalizado si lo prefiere.
Elija dónde desea guardar la configuración del servidor MCP. Puede agregarla a la configuración de usuario para usarla en todos los proyectos o en la configuración del área de trabajo del proyecto actual.
Aparecerá un mensaje que le pedirá que autorice con GitHub mediante OAuth. Seleccione Permitir e iniciar sesión en su cuenta de GitHub si se le solicita.
Después de la instalación, el servidor MCP de GitHub estará listo para usarse con los proyectos en VS Code. Ahora puede empezar a usar herramientas y flujos de trabajo con tecnología de inteligencia artificial para automatizar tareas, administrar problemas y analizar el código directamente dentro del editor, lo que le ayuda a centrarse en el trabajo mientras el servidor MCP de GitHub controla el trabajo pesado en segundo plano.

Uso del token de acceso personal
Para usar el token de acceso personal (PAT) para el control avanzado, puede seguir estos pasos:

Cree un PAT con el repositorio y lea: ámbito de paquetes en la cuenta de GitHub.

Seguirá los mismos pasos anteriores, pero cancelarÁ OAuth cuando se le solicite.

En el archivo de configuración, agregue:

JSON
"headers": {
  "Authorization": "Bearer ${input:github_token}"
}
A continuación, agregue un mensaje de entrada para escribir de forma segura el token:

JSON
"inputs": [
  {
    "id": "github_token",
    "type": "promptString",
    "description": "GitHub Personal Access Token",
    "password": true
  }
]
Por último, reinicie el servidor MCP en VS Code y escriba el PAT cuando se le solicite.

El servidor MCP ahora se configurará para usar el PAT para la autorización.

Configuración del servidor MCP local con Docker (opcional)
Si su empresa usa GitHub Enterprise Server con restricciones de PAT, solo puede acceder a los ámbitos de API permitidos por la directiva de su organización. Si todos los puntos de conexión están restringidos, el servidor MCP no estará disponible, compruebe con el administrador si no está seguro.

Para su uso local, el servidor MCP requiere Docker y la autenticación con un token de acceso personal (PAT). OAuth no se admite en esta configuración.

En primer lugar, debe confirmar que Docker está instalado y en ejecución en el sistema.

A continuación, genere un PAT con los ámbitos necesarios.

Use la siguiente configuración para ejecutar el servidor localmente:

JSON
{
  "inputs": [
    {
      "type": "promptString",
      "id": "github_token",
      "description": "GitHub Personal Access Token",
      "password": true
    }
  ],
  "servers": {
    "github": {
      "command": "docker",
      "args": [
        "run",
        "-i",
        "--rm",
        "-e",
        "GITHUB_PERSONAL_ACCESS_TOKEN",
        "ghcr.io/github/github-mcp-server"
      ],
      "env": {
        "GITHUB_PERSONAL_ACCESS_TOKEN": "${input:github_token}"
      }
    }
  }
}
Reinicie el servidor MCP y escriba el PAT cuando se le pida que complete la configuración.

Solución de problemas
Si tiene problemas al usar el servidor MCP de GitHub, estas son algunas comprobaciones prácticas:

Confirme que ha iniciado sesión en su cuenta de GitHub en VS Code.
Si usa un PAT, asegúrese de que tiene los ámbitos correctos y se escribe correctamente.
Compruebe la configuración para ver si hay errores tipográficos o campos que faltan.
Si usa Docker, asegúrese de que está instalado y en ejecución activamente.
Intente reiniciar VS Code o el servidor MCP para resolver problemas de conexión temporales.

## Uso del servidor MCP de GitHub con Copilot Chat

Ahora que ha visto cómo los servidores MCP amplían las funcionalidades de GitHub Copilot, vamos a dar el siguiente paso: combinarlos con el modo agente de Copilot. Aquí es donde Copilot se mueve más allá de responder a las solicitudes y comienza a actuar como un verdadero colaborador, capaz de planear, ejecutar y refinar flujos de trabajo.

En esta unidad, aprenderá lo siguiente:

Lo que es el modo agente de Copilot y cómo difiere del uso estándar.
Cómo mejoran el modo de agente los servidores MCP conectando Copilot a herramientas y datos externos.
Las principales ventajas de combinar MCP con el modo de agente, como la automatización y el menor esfuerzo manual.
Cómo aplicar procedimientos recomendados para guiar a Copilot en flujos de trabajo agente de forma eficaz.
Uso del servidor MCP de GitHub con Copilot Chat
Abra Chat de Copilot en Visual Studio Code y cambie al modo agente para activar las herramientas del servidor MCP.

Haga clic en Seleccionar herramientas para ver todas las funcionalidades disponibles del servidor MCP.

Ahora puede intentar crear un nuevo problema, resumir un repositorio o obtener información sobre el trabajo mediante avisos de lenguaje natural.

Siga las indicaciones de Copilot Chat para completar sus tareas de forma eficaz.

Funcionalidades agente de Copilot y MCP
Hasta ahora, hemos visto cómo los servidores MCP amplían GitHub Copilot mediante la conexión a herramientas y recursos externos. ¿Pero qué ocurre cuando combinamos esto con el modo de agente? Aquí es donde Copilot cambia de ser solo un asistente dinámico para actuar más como un colaborador independiente.

¿Qué son las funcionalidades agente?
Las funcionalidades agenticas proporcionan a Copilot la capacidad de:

Trabaje de forma independiente mediante la realización de flujos de trabajo de varios pasos sin necesidad de instrucciones constantes.

Para tomar decisiones, elija qué herramientas o enfoques usar en función del contexto que tiene. Adapte y mejore respondiendo a los comentarios, ajustando su enfoque e iterando en los resultados.

En otras palabras, el modo de agente permite a Copilot controlar las tareas de una manera que se siente más autónoma, casi como tener un compañero de equipo que comprenda la imagen más grande en lugar de seguir las instrucciones individuales.

Cómo MCP hace que el modo agente sea más seguro
Por sí solo, el modo de agente es eficaz. Pero al agregar servidores MCP, le da a Copilot la capacidad de llegar más allá del entorno de codificación inmediato. A través de MCP, Copilot puede:

Acceda directamente a datos externos, API o herramientas empresariales.
Manténgase en contexto en varias plataformas, sin necesidad de cambiar de aplicación.
Complete "bucles agente", donde busca información dinámicamente, analiza los resultados y realiza los pasos siguientes informados, todo sin reiniciar el proceso desde cero.
Esto significa que Copilot no solo reacciona a una sola petición. En su lugar, funciona en un ciclo: explorar, adaptar y refinar hasta que genere el resultado que desee.

Ventajas de combinar MCP con el modo de agente
Al reunir estas dos funcionalidades, se desbloquean las principales ventajas:

Contexto extendido: Copilot puede extraer información de varios sistemas, no solo el editor de código.

Esfuerzo manual reducido: el trabajo rutinario, como abrir problemas, administrar flujos de trabajo o ejecutar comprobaciones, se puede automatizar mientras se centra en decisiones de mayor valor.

Integración sin problemas: Copilot puede llevar a cabo tareas que abarcan herramientas y plataformas, sin necesidad de conectores personalizados ni cambio constante.

Procedimientos recomendados para el éxito
Para obtener el máximo partido del modo MCP y del agente, pruebe estas estrategias:

Estar claro acerca de los objetivos: defina lo que desea que Copilot logre y cuál debe ser el resultado final.
Proporcionar contexto: comparta detalles en segundo plano sobre el proyecto o el flujo de trabajo. Esto podría incluir vínculos, referencias o pasos anteriores.
Establecer límites: si desea que Copilot deje de planear (y aún no realice cambios), indique eso. También puede limitar qué herramientas de MCP están activas.
Pedir confirmación: antes de realizar grandes cambios, haga que Copilot resuma su plan para que pueda aprobarlo o refinarlo.
Use los archivos de solicitud o las instrucciones: cree archivos de aviso personalizados que guían a Copilot sobre cómo comportarse con servidores MCP específicos. Esto mantiene su comportamiento coherente y alineado con los flujos de trabajo.


## Ejercicio: Integración de MCP con GitHub Copilot
En este ejercicio, aprenderá a:

Integre un servidor MCP de GitHub con GitHub Copilot.
Delegue Copilot para investigar proyectos similares y abrir problemas.
Pida a Copilot que encuentre un problema importante e implemente desde la idea de extraer la solicitud de incorporación de cambios.
Agregue comentarios a un problema cerrado recientemente.
Cómo empezar
Al seleccionar el botón Iniciar el ejercicio en GitHub siguiente, se le dirigirá a un repositorio de plantillas de GitHub público que le pedirá que complete una serie de pequeños desafíos.

Cuando haya terminado el ejercicio en GitHub, vuelva aquí para:

Una comprobación rápida de conocimientos.
Un resumen de lo que ha aprendido.
Un distintivo por completar este módulo.
Inicio del ejercicio en GitHub

## Resumen
Ahora que ha terminado este módulo, debería poder:

Explique qué son MCP y el servidor MCP de GitHub y cómo admiten flujos de trabajo de desarrollo con tecnología de inteligencia artificial.
Describir las ventajas de usar el servidor MCP de GitHub para simplificar y escalar los proyectos.
Configure el servidor MCP de GitHub en Visual Studio Code mediante OAuth, un token de acceso personal (PAT) o Docker.
Use Copilot Chat con MCP Server para automatizar las tareas y aumentar la productividad directamente en el editor.
Resuelva problemas comunes de configuración con confianza.
Aprende más
Aquí tiene algunos vínculos para obtener más información sobre los temas analizados en este módulo.

Uso del servidor MCP de GitHub

El servidor MCP de GitHub ya está disponible en versión preliminar pública

Introducción: protocolo de contexto del modelo

¿Qué es GitHub Copilot?

Presentación del servidor MCP de GitHub

Mejora del modo de agente de Copilot de GitHub con MCP

Servidor MCP de GitHub

Introducción a Azure
Elija la cuenta de Azure adecuada para usted. Pague por uso o pruebe Azure gratis durante un máximo de 30 días. Únete.

Proporcionar comentarios
Use este formulario de problema para proporcionar comentarios de contenido o cambios sugeridos para este módulo de Microsoft Learn. GitHub mantiene este contenido y un miembro del equipo evaluará la solicitud. Gracias por darse el tiempo de mejorar nuestro contenido.
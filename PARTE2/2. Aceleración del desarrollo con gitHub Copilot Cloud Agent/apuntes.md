# Aceleración del desarrollo con GitHub Copilot Cloud Agent
## Descripción y habilitación del agente en la nube de Copilot de GitHub
En esta unidad se explica qué es el agente, cómo difiere de los asistentes tradicionales de codificación de IA, qué planes y repositorios lo admiten, y cómo habilitar y presupuestar para él, incluidas las unidades de solicitud Premium (PRUs) y los minutos de Acciones de GitHub.

Al final de esta unidad, podrás:

Explique lo que es el agente en la nube de Copilot de GitHub, quién puede usarlo y dónde está disponible.
Describir las tareas que puede realizar y cómo delegar el trabajo.
Distinguirlo de los asistentes solo para IDE y del "modo de agente" de Copilot.
Active el agente a nivel de organización o repositorio.
Comprenda cómo se usan los minutos de Acciones de GitHub y las unidades de solicitud Premium (PRU) y cómo se administran de forma eficaz.
¿Qué es el agente en la nube de Copilot de GitHub, que puede usarlo y dónde está disponible?
El agente en la nube de Copilot de GitHub es un asistente de desarrollo autónomo que se ejecuta dentro de GitHub. En lugar de emparejarse solo con usted en el IDE, el agente actúa como un compañero de equipo en segundo plano. Le proporciona una tarea claramente definida (como una corrección de errores, una característica incremental o una actualización de documentación) y crea una rama, explora el repositorio de código, genera un plan de implementación y redacta código, manteniéndole en control de cuándo y si debe abrir una solicitud de incorporación de cambios.

Disponibilidad y planes
Planes: Disponibles en Copilot Pro, Copilot Pro+, Copilot Business, Copilot Enterprise.
Repositorios: Funciona en todos los repositorios hospedados en GitHub, excepto en aquellos que pertenecen a cuentas de usuario administradas o en los que el agente está deshabilitado explícitamente.
Qué hace el agente en la nube de Copilot
Copilot Cloud Agent puede asumir una amplia gama de tareas de desarrollo:

Corregir errores y regresiones.
Implemente nuevas características incrementales.
Mejore la cobertura de pruebas o genere pruebas que faltan.
Actualice o cree documentación.
Aborde la deuda técnica y los elementos opcionales pendientes.
Puede delegar el trabajo al agente de dos maneras principales:

Asigne un problema a Copilot: en GitHub.com, GitHub Mobile o a través de la API o la CLI.
Pida a Copilot que realice cambios en el código: desde el panel Agentes en GitHub, Copilot Chat, su IDE u otra herramienta agente con compatibilidad con MCP o Raycast en macOS.
Cuando el agente finalice, solicita que usted lo revise. Puede mencionar @copilot en un comentario de solicitud de cambios para pedirle que itere en su trabajo.

Cómo se diferencia de los asistentes de IDE tradicionales
Los asistentes tradicionales de inteligencia artificial en los IDE le ayudan a escribir código localmente, pero dejan los pasos manuales para usted: crear ramas, insertar confirmaciones, escribir descripciones de solicitud de cambios e iterar. Esas decisiones se producen en una sesión privada y no son visibles para su equipo.

Con Copilot Cloud Agent :

Todo el trabajo ocurre como commits en GitHub.
El agente automatiza la creación de ramas, los mensajes de confirmación y el borrador de código, al tiempo que le permite decidir si desea abrir una solicitud de incorporación de cambios y cuándo hacerlo.
El trabajo es visible en los registros de sesión y el historial de solicitud de cambios para asegurar la trazabilidad.
Usted orienta a través de comentarios de revisión de solicitud de cambios en lugar de sesiones locales sincrónicas.
Esto crea transparencia y oportunidades de colaboración: sus compañeros de equipo pueden ver cada paso y saltar según sea necesario.

Agente en la nube frente al "Modo de agente" en los IDE
Es importante distinguir el agente en la nube de Copilot de GitHub (tratado en este módulo) de la característica de modo de agente en Visual Studio y Visual Studio Code:

Agente en la nube: Se ejecuta de forma autónoma en un entorno con tecnología de Acciones de GitHub para completar las tareas de desarrollo que asigne a través de problemas o Chat de Copilot.
Modo de agente (Ediciones de Copilot): Realiza modificaciones locales autónomas directamente en la sesión del IDE.
Habilitación del agente en la nube de Copilot
Antes de asignar tareas a Copilot, asegúrese de que el agente está habilitado:

Repositorios propiedad de la organización: La disponibilidad la administran los administradores de la organización o de la empresa.
Repositorios personales: Configure la disponibilidad en la configuración de la cuenta.
Costos de uso: Acciones de GitHub + PRUs

Copilot Cloud Agent usa dos recursos principales:

Minutos de acciones de GitHub para el entorno de compilación/prueba efímero donde opera el agente.
Solicitudes de Copilot Premium (PRU) para impulsar el razonamiento avanzado del modelo.
 Nota

A partir del 4 de junio de 2025, el agente utiliza una petición premium por cada solicitud de modelo que realiza. Dentro de las asignaciones mensuales de Acciones y solicitudes premium, puede ejecutar tareas sin cargos adicionales. (Consulte facturación de GitHub Copilot).

 Sugerencia

Utilice los PRU donde agregan valor: ediciones de varios archivos, creación de pruebas y diferencias más amplias que requieren un razonamiento más profundo. Las modificaciones ligeras pueden requerir menos pasos intensivos de PRU.

Con el agente habilitado y una vez comprendidos los costos, vamos a verificar cómo se alinea con su posición de seguridad, qué riesgos anticipar y qué limitaciones debe tener en cuenta durante la planificación del trabajo real.



## Seguridad, riesgos y limitaciones del agente en la nube de Copilot
El agente en la nube de Copilot de GitHub está diseñado desde cero teniendo en cuenta la seguridad y la gobernanza. Aunque desbloquea nuevas formas de delegar el trabajo a un agente autónomo, funciona dentro de los límites de protección existentes de la organización y agrega sus propias protecciones. En esta unidad se explica cómo el agente aplica las directivas de seguridad, resalta los riesgos y mitigaciones que debe tener en cuenta y establece las expectativas sobre sus limitaciones actuales.

Al finalizar esta unidad, podrán:

Describir el modelo de seguridad y las protecciones integradas del agente en la nube de Copilot.
Identifique los principales riesgos asociados al uso del agente y las mitigaciones que aplica GitHub.
Reconozca las limitaciones conocidas del flujo de trabajo del agente y la compatibilidad para planear el uso en consecuencia.
Modelo de seguridad y protecciones integradas
La seguridad es fundamental para el Copilot Cloud Agent. Respeta los controles existentes y aplica sus propios límites de protección para mantener seguros los flujos de trabajo:

Sujeto a gobernanza : la organización y la configuración empresarial rigen la disponibilidad; todas las directivas de seguridad siguen aplicándose al agente.
Entorno restringido : el agente se ejecuta dentro de un espacio aislado en Acciones de GitHub con acceso a Internet con firewall y acceso de solo lectura al repositorio.
Límites de la rama: solo puede crear e insertar en ramas que comiencen con copilot/, y todas las protecciones de rama y las comprobaciones necesarias aún se aplican.
Sensible a permisos - el agente solo responde a los usuarios con permiso de escritura. Se omiten los comentarios de otros usuarios.
Reglas de colaborador externo: los borradores de solicitudes de cambios del agente requieren la aprobación por parte de un usuario con permiso de escritura antes de que se ejecute Acciones. La persona que solicitó la solicitud de cambios no puede aprobarlos.
Cumplimiento y atribución: todas las confirmaciones son producto de la coautoría con el desarrollador que asignó la tarea o solicitó la solicitud de cambios, por lo que la atribución es clara. Las reglas de "aprobaciones requeridas" existentes siguen intactas.
Riesgos y mitigaciones
Aunque Copilot Cloud Agent se ha creado teniendo en cuenta la seguridad, todavía hay riesgos que debería considerar. GitHub aplica mitigaciones para reducirlas:

Riesgo: el agente inserta código

Mitigaciones: Solo los usuarios con acceso de escritura pueden desencadenar el trabajo del agente. Las inserciones se limitan a copilot/ ramas (no principal/master). Las credenciales del agente solo permiten inserciones simples (sin git push directo). Los flujos de trabajo de Acciones de GitHub no se ejecutarán hasta que un usuario con permiso de escritura haga clic en "Aprobar y ejecutar flujos de trabajo". El solicitante no puede aprobar la solicitud de cambios del agente; se mantienen las aprobaciones necesarias.

Riesgo: acceso a información confidencial

Mitigación: El acceso a Internet del agente está restringido por firewall de forma predeterminada; puede personalizar o deshabilitar el firewall por directiva.

Riesgo: Inyección de indicaciones

Mitigación: Los caracteres ocultos (como los comentarios HTML) se filtran antes de pasar la entrada del usuario al agente. Esto reduce la posibilidad de instrucciones perjudiciales ocultas en comentarios o problemas.

Estos controles proporcionan una línea base segura para usar el agente, pero debe revisar cuidadosamente los resultados como lo haría con el código escrito por cualquier miembro del equipo.

Limitaciones conocidas
Limitaciones del flujo de trabajo

Solo se pueden realizar cambios en el mismo repositorio que el problema asignado o la solicitud de cambios.
El ámbito de contexto se limita al repositorio asignado de forma predeterminada (se puede ampliar a través de MCP).
Abre exactamente un pull request por tarea.
No se puede modificar una solicitud de cambios existente que no haya creado usted mismo (en su lugar, agréguela como revisor si necesita comentarios aprovechando la revisión de código de GitHub Copilot).
Limitaciones de compatibilidad

No firma las confirmaciones. Si necesita confirmaciones firmadas, debe volver a escribir el historial de confirmaciones antes de la combinación.
Requiere ejecutores de Ubuntu x64 hospedados en GitHub. No se admiten ejecutores autohospedados.
No está disponible para repositorios personales propiedad de cuentas de usuario administradas (ejecutores no disponibles).
No respeta las exclusiones de contenido; el agente puede ver y actualizar los archivos excluidos.
El agente no aplica la directiva "Sugerencias que coincidan con el código público"; Es posible que no se proporcionen referencias.
Solo funciona con repositorios hospedados en GitHub.
El modelo de IA usado por el agente no se puede cambiar; lo selecciona GitHub.
Con límites de protección y límites claros, está listo para empezar a delegar el trabajo, seguir el progreso e iterar en los resultados mediante el flujo de trabajo de solicitud de cambios estándar.

## Asignación, seguimiento y solución de problemas de tareas de Copilot Cloud Agent
El agente en la nube de Copilot de GitHub actúa como un compañero de equipo autónomo que funciona directamente dentro de GitHub. Una vez habilitada, puede asignarla a una tarea, ver su progreso en tiempo real y guiar su trabajo dejando comentarios en sus solicitudes de incorporación de cambios. En esta unidad se explica cómo asignar problemas a Copilot mediante GitHub.com, GitHub Mobile, la API o la CLI. También muestra cómo realizar un seguimiento del trabajo del agente e iterar con él, y proporciona un cuaderno de estrategias de solución de problemas para problemas comunes.

Al finalizar esta unidad, podrán:
Asigne problemas a Copilot mediante GitHub.com, GitHub Mobile, la API o CL.
Supervise el progreso de Copilot a través de escalas de tiempo de solicitud de cambios y registros de sesión.
Itere el trabajo de Copilot comentando en sus solicitudes de cambios.
Comprenda las reglas de aprobación para las solicitudes de cambios generadas por el agente.
Solución de problemas comunes al delegar tareas en Copilot.
Asignación de problemas a Copilot
Cuando asigna un problema a Copilot, el agente lo reconoce agregando una reacción 👀 al problema. A continuación, crea una rama copilot/ dedicada, abre una solicitud de cambios de borrador vinculada al problema y comienza una sesión del agente dentro de un entorno impulsado por Acciones de GitHub. Mientras funciona, Copilot envía confirmaciones a la rama y actualiza el cuerpo de la solicitud de cambios con mensajes de estado. Una vez completada la tarea, Copilot publica un evento "Copilot finished work" y solicita su revisión.

Captura de pantalla de una barra de navegación del repositorio de GitHub que resalta la pestaña Problemas con el número de problemas abiertos que se muestran.

En GitHub.com, asigna un problema a Copilot igual que lo asignaría a otro usuario. Vaya a la pestaña Problemas del repositorio, abra el problema que desea delegar y, en la barra lateral derecha, en Asignar, seleccione Copilot. Copilot recibe el título del problema, la descripción y los comentarios existentes en el momento de la asignación. Los comentarios posteriores sobre el problema no son vistos por el agente, así que añada información nueva como comentarios directamente en la solicitud de cambios del agente.

Captura de pantalla del panel Asignador de problemas de GitHub que muestra la opción para asignar Copilot como programador de pares de IA.

También puede asignar problemas a Copilot desde la lista de problemas de la página Problemas de un repositorio, desde GitHub Projects o mediante GitHub Mobile. Para los flujos de trabajo de la línea de comandos, puede usar la CLI de GitHub (gh issue edit) para agregar a Copilot como responsable.

Asignación a través de la API
Puede asignar problemas a Copilot mediante programación a través de GraphQL API. En primer lugar, compruebe que el agente de codificación está disponible consultando suggestedActors el repositorio y comprobando que copilot-swe-agent aparece como un actor sugerido. A continuación, capture el identificador del repositorio. Para crear y asignar un problema nuevo, use la createIssue mutación y pase el identificador del repositorio y el identificador del bot de Copilot. Para asignar una incidencia existente, obtenga el ID de la incidencia y, a continuación, utilice la mutación replaceActorsForAssignable para asignar Copilot como asignado. Este enfoque es útil para integrar Copilot en flujos de trabajo automatizados.

Comprobación de disponibilidad
query {
  repository(owner: "octo-org", name: "octo-repo") {
    suggestedActors(capabilities: [CAN_BE_ASSIGNED], first: 100) {
      nodes { login __typename ... on Bot { id } ... on User { id } }
    }
  }
}

Obtención del identificador del repositorio
query {
  repository(owner: "octo-org", name: "octo-repo") { id }
}

Creación y asignación de un nuevo problema
mutation {
  createIssue(
    input: {
      repositoryId: "REPOSITORY_ID",
      title: "Implement comprehensive unit tests",
      body: "DETAILS",
      assigneeIds: ["BOT_ID"]
    }
  ) {
    issue { id title assignees(first: 10) { nodes { login } } }
  }
}
Asignación de un problema existente
query {
  repository(owner: "monalisa", name: "octocat") {
    issue(number: 9000) { id title }
  }
}

mutation {
  replaceActorsForAssignable(
    input: { assignableId: "ISSUE_ID", actorIds: ["BOT_ID"] }
  ) {
    assignable {
      ... on Issue {
        id title
        assignees(first: 10) { nodes { login } }
      }
    }
  }
}

Seguimiento del progreso de Copilot
Después de asignar un problema a GitHub Copilot, el agente proporciona señales visibles para que pueda seguir su trabajo de principio a fin.

Confirmación inmediata. Poco después de asignar un problema, Copilot agrega una 👀 reacción al problema.

Captura de pantalla de una descripción del problema de GitHub en la que se muestran los pasos para reproducir y la opción para crear un sub-problema.

Creación automatizada de solicitudes de cambios. En unos segundos, Copilot abre un borrador de solicitud de cambios vinculado al problema original. Aparece un nuevo evento en la línea de tiempo del issue que muestra el pull request.

Captura de pantalla de un comentario de problema de GitHub en el que Copilot menciona un problema relacionado con un vínculo al número 1123.

Sesión del agente activo. Copilot inicia una sesión de agente para trabajar en tu problema. Verá un evento “Copilot ha comenzado a trabajar” en la escala de tiempo de la solicitud de cambios. A medida que se ejecuta, Copilot actualiza el cuerpo de la solicitud de cambios con mensajes de estado regulares e inserta confirmaciones en la rama dedicada.

Captura de pantalla de una escala de tiempo de problemas de GitHub en la que Copilot comenzó a trabajar en nombre de un usuario.

Registros de sesión en directo. Todas las sesiones pasadas y presentes son visibles en la página de Agentes. Haga clic en Ver sesión en la solicitud de incorporación de cambios para abrir el visor de registros de sesión en directo y ver las acciones de Copilot en tiempo real. Si necesita detener Copilot, haga clic en Detener sesión en el visor.

Finalización y revisión. Cuando Copilot finaliza su trabajo, la sesión del agente finaliza automáticamente. Un evento "Copilot finished work" aparece en la cronología de la solicitud de incorporación de cambios y Copilot solicita una revisión por su parte, lo cual genera una notificación.

Captura de pantalla de una escala de tiempo de problemas de GitHub en la que Copilot finalizó el trabajo en nombre de un usuario después de solicitar una revisión.

Iteración con Copilot
Guía el trabajo de Copilot de la misma manera que guiaría a un colaborador humano a través de comentarios y opiniones. Mencione @copilot en un comentario de solicitud de incorporación de cambios para solicitar cambios. Solo se procesan los comentarios de los usuarios con permiso de escritura en el repositorio. Copilot publica una reacción 👀 a su comentario para confirmar que ha recibido la solicitud y, a continuación, agrega "Copilot ha comenzado a trabajar" a la línea de tiempo de la solicitud de cambios al reanudar. Esto te permite iterar sobre el trabajo de Copilot sin abandonar tu flujo de trabajo habitual de revisión.

Aprobaciones y flujos de trabajo
Las solicitudes de incorporación de cambios creadas por Copilot siempre están en estado de borrador. Requieren aprobación humana antes de la combinación y los flujos de trabajo de Acciones de GitHub desencadenados por el agente no se ejecutan automáticamente. Para ejecutar flujos de trabajo en una solicitud de cambios de Copilot, haga clic en Aprobar y ejecute los flujos de trabajo en el cuadro de fusión. El desarrollador que pidió a Copilot que creara la solicitud de incorporación de cambios no puede aprobarla, lo que conserva las reglas de "revisiones necesarias" del repositorio y garantiza una revisión independiente antes de la combinación.

Resolución de problemas del Agente de Copilot en la Nube
Copilot no está en la lista de 'Asignados'

Asegúrese de que está en un plan apto (Pro, Pro+, Empresa, Enterprise). Confirme que el agente no esté deshabilitado en el nivel de organización o repositorio. Compruebe en la página de características: github.com/settings/copilot/features.

Repositorios personales de usuario gestionado por la empresa (EMU)

Agente no disponible; use repositorios propiedad de la organización (requiere ejecutores hospedados en GitHub).

"No se puede crear una solicitud de incorporación de cambios" desde Chat

Asegúrese de que el agente está disponible. En los IDE, mencione @github en la indicación (no es necesario en GitHub.com).

Se asignó un problema, pero no sucedió nada

Actualice; busque la reacción 👀 y, a continuación, realice un borrador de solicitud de cambios.

Solicitud de cambios creada, pero sin progreso

Compruebe la línea de tiempo de la solicitud de cambios para "Copilot ha comenzado a trabajar"; abra Ver los registros de sesión.

El agente no responde al comentario de la solicitud de cambios

Confirme que tiene acceso de escritura y que mencionó @copilot en la solicitud de cambios del agente.

Aparece bloqueado

Puede recuperarse automáticamente; el tiempo de espera de las sesiones se agota tras una hora. Vuelva a intentarlo desasignando o reasignando la incidencia o volviendo a publicar el comentario.

Las acciones no se están ejecutando

Haga clic en Aceptar y ejecutar flujos de trabajo en el cuadro de fusión.

Los cambios no pasan la CI

Proporcione instrucciones claras de nivel de repositorio a través de .github/copilot-instructions.md para que el agente pueda validarse automáticamente con tests/linters.

Advertencias de firewall

Internet está restringido de forma predeterminada; advertencias enumeran la dirección y el comando bloqueados. Ajústelo a Personalización o deshabilitación del firewall para el agente en la nube de GitHub Copilot.

Imágenes no recogidas

El tamaño máximo de la imagen es 3,00 MiB; se quitan imágenes más grandes.

Con un bucle confiable de asignación-seguimiento-iteración en su lugar, puede aumentar la consistencia y la velocidad personalizando el entorno del agente, extendiéndolo con herramientas de MCP y aplicando una validación robusta antes de la fusión.

## Personalización, ampliación y validación del agente en la nube de Copilot
El agente en la nube de Copilot de GitHub se ejecuta dentro de un entorno seguro efímero de Acciones de GitHub. Con algunos pasos de configuración puede presear este entorno para mejorar la confiabilidad y la velocidad, ampliar las funcionalidades del agente con herramientas externas a través del Protocolo de contexto de modelo (MCP) y aplicar procedimientos recomendados para probar y validar la salida del agente antes de la combinación.

Al final de esta unidad, podrás:

Preinstale herramientas, dependencias y secretos para personalizar el entorno de desarrollo del agente.
Amplíe las funcionalidades del agente mediante el Protocolo de contexto de modelo (MCP).
Pruebe y valide los resultados del agente de forma eficaz antes de combinar los cambios.
Preparando previamente el entorno de desarrollo
Preinstalar herramientas y dependencias concopilot-setup-steps.yml

Cree .github/workflows/copilot-setup-steps.yml en la rama predeterminada del repositorio. El flujo de trabajo debe definir un único trabajo denominado copilot-setup-steps. Incluya los pasos necesarios para instalar dependencias o configurar herramientas.

Ejemplo de TypeScript:

name: "Copilot Setup Steps"

on:
  workflow_dispatch:
  push:
    paths:
      - .github/workflows/copilot-setup-steps.yml
  pull_request:
    paths:
      - .github/workflows/copilot-setup-steps.yml

jobs:
  copilot-setup-steps:
    runs-on: ubuntu-latest
    permissions:
      contents: read
    steps:
      - name: Checkout code
        uses: actions/checkout@v5
      - name: Set up Node.js
        uses: actions/setup-node@v4
        with:
          node-version: "20"
          cache: "npm"
      - name: Install JavaScript dependencies
        run: npm ci
Claves de configuración permitidas para el copilot-setup-steps trabajo: steps, permissions, runs-on, container, services, snapshot, timeout-minutes (≤ 59). Cualquier actions/checkout de captura profunda se invalida para permitir la reversión segura. El flujo de trabajo de instalación se ejecuta de forma independiente (por lo que puede validarlo) y, a continuación, automáticamente antes de que se inicie el agente.

Ejecutores hospedados en GitHub grandes

Añadir corredores más grandes primero
En copilot-setup-steps.yml, establezca runs-on en la etiqueta o grupo (por ejemplo, ubuntu-4-core).
Solo se admiten ejecutores de Ubuntu x64; No se admiten ejecutores autohospedados.
Git LFS

Si usa Git Large File Storage, habilite en los pasos de configuración:

jobs:
  copilot-setup-steps:
    runs-on: ubuntu-latest
    permissions:
      contents: read
    steps:
      - uses: actions/checkout@v5
        with:
          lfs: true
Personalización del firewall

El acceso a Internet predeterminado está limitado para reducir el riesgo de filtración. Puede personalizar o deshabilitar el firewall por directiva organizativa si es necesario.

Extienda con el Protocolo de Modelo de Contexto (MCP)
MCP es un estándar abierto para conectar los LLM a herramientas y datos. El agente puede usar herramientas proporcionadas por servidores MCP locales o remotos para expandir sus funcionalidades.

Nota: Copilot Cloud Agent solo admite herramientas de MCP (no recursos ni avisos). No se admiten servidores MCP remotos que requieren OAuth.

Servidores MCP predeterminados

Servidor MCP de GitHub: Acceso a problemas, solicitudes de cambios y datos de GitHub con un token de solo lectura con ámbito al repositorio actual de manera predeterminada (puede personalizar el token).
Servidor MCP de Playwright: Lea, interactúe con y tome capturas de pantalla de las páginas web accesibles dentro del entorno del agente (localhost/127.0.0.1).
Configuración del repositorio

Los administradores pueden declarar servidores MCP a través de una configuración JSON en el repositorio. Una vez configurado, el agente usa de forma autónoma las herramientas disponibles, sin solicitudes de aprobación por uso. Vea cómo extender el agente en la nube de GitHub Copilot con MCP.

procedimientos recomendados

Revise los servidores MCP de terceros para evaluar las implicaciones en el rendimiento y la calidad de salida.
Preferir herramientas de lectura; si existen herramientas de escritura, permita solo lo necesario.
Valide cuidadosamente la configuración de MCP antes de guardarla.
Prueba y validación de la salida del agente
Usted sigue siendo responsable de la calidad y la seguridad:

Ejecutar CI (pruebas, linters, análisis) en cada solicitud de cambios del agente; estas comprobaciones no se ejecutarán hasta que haga clic en Aprobar y ejecute los flujos de trabajo.
Inspeccione manualmente áreas sensibles o de alto impacto.
Pida al agente que genere pruebas (por ejemplo, "Agregar pruebas unitarias de Jest para todas las funciones en src/utils/, siguiendo el estilo del repositorio"). La generación de pruebas de varios archivos consume PRUs.
Aplique conjuntos de reglas para que las solicitudes de incorporación de cambios del agente deban pasar pruebas + análisis + linting antes de la combinación.
Etiquete las solicitudes de cambios del agente (por ejemplo, agent-refactor, agent-tests) para supervisar, evaluar prioridades y revertir si es necesario.
Iterar las instrucciones en .github/copilot-instructions.md cuando veas errores repetidos.
Revierta rápidamente si es necesario y solicite nuevos cambios del agente.
Uso de PRU intencionadamente para la validación

Aproveche las PRU para realizar tareas de validación más profundas, como la expansión de la cobertura de pruebas, las auditorías entre directorios o exámenes de área de riesgo. Las comprobaciones ligeras consumen menos PRUs, por lo que aplíquelas intencionadamente para maximizar el valor.

Con las prácticas de configuración, extensiones y validación en vigor, el paso final es usar el agente de manera responsable, definiendo bien las tareas, protegiendo los entornos y revisando continuamente los resultados.

## Uso responsable de GitHub Copilot Cloud Agent en GitHub.com
Obtenga información sobre cómo usar Copilot Cloud Agent en GitHub.com de forma responsable mediante la comprensión de sus propósitos, funcionalidades y limitaciones.

Al finalizar esta unidad, podrán:

Comprenda el propósito, las funcionalidades y los límites del agente en la nube de Copilot en GitHub.com.
Aplicar prácticas de uso responsable: tareas de ámbito, protección de entornos y validación de resultados.
Reconozca las medidas de seguridad, los riesgos y las mitigaciones, y dónde mejorar el rendimiento.
Acerca de Copilot Cloud Agent en GitHub.com
Copilot Cloud Agent es un agente de desarrollo de software autónomo y asincrónico integrado en GitHub. El agente puede recoger una tarea de un problema o de Copilot Chat, crear una rama, explorar el código base, generar un plan de implementación y redactar código, lo que le permite decidir si y cuándo abrir una solicitud de incorporación de cambios.

Copilot Cloud Agent puede generar cambios personalizados en función de la descripción y las configuraciones, incluidas tareas como correcciones de errores, implementación de nuevas características incrementales, creación de prototipos, documentación y mantenimiento de código base. Si decide crear una solicitud de incorporación de cambios, el agente puede iterar con usted basándose en sus comentarios y revisiones.

Al trabajar en la tarea, el agente tiene acceso a su propio entorno de desarrollo efímero, donde puede realizar cambios en el código, ejecutar pruebas automatizadas y ejecutar linters. El agente se ha evaluado en una variedad de lenguajes de programación, con el inglés como idioma principal admitido.

Funcionamiento del agente (de un extremo a otro)
Procesamiento de mensajes

La tarea proporcionada a Copilot a través de un problema, comentario de solicitud de cambios o mensaje de Copilot Chat se combina con otra información contextual relevante para formar una indicación. Las entradas pueden adoptar la forma de lenguaje natural sin formato, fragmentos de código o imágenes.

Análisis del modelo de lenguaje

A continuación, el mensaje se pasa a través de un modelo de lenguaje grande, que analiza la entrada para ayudar al agente a razonar en la tarea y utilizar las herramientas necesarias.

Generación de respuestas

El modelo de lenguaje genera una respuesta basada en su análisis de la indicación. Esta respuesta puede adoptar la forma de sugerencias en lenguaje natural y sugerencias de código.

Formato de salida

Una vez que el agente complete su primera ejecución, actualizará la descripción de la solicitud de cambios con los cambios realizados. El agente puede incluir información complementaria sobre los recursos a los que no pudo acceder y proporcionar sugerencias sobre los pasos para resolver.

Puede proporcionar comentarios al agente al comentar dentro de la solicitud de incorporación de cambios o mencionar explícitamente al agente (@copilot). Después, el agente volverá a enviar los comentarios al modelo de lenguaje para su posterior análisis. Una vez que el agente complete los cambios en función de los comentarios, responderá a su comentario con los cambios actualizados.

Copilot está pensado para proporcionarle la solución más relevante para la resolución de tareas. Sin embargo, es posible que no siempre proporcione la respuesta que busca. Usted es responsable de revisar y validar las respuestas generadas por Copilot para asegurarse de que son precisas y adecuadas. Además, como parte de nuestro proceso de desarrollo de productos, GitHub realiza red teaming (pruebas) para comprender y mejorar la seguridad del agente.

Casos de uso para el agente Copilot en la nube
Mantenimiento de código base: Correcciones de seguridad, actualizaciones de dependencias y refactorización dirigida.
Documentación: actualización y creación de nueva documentación.
Desarrollo de características: implementación de solicitudes de características incrementales.
Mejora de la cobertura de las pruebas: desarrollo de conjuntos de pruebas adicionales para la administración de la calidad.
Creación de prototipos de nuevos proyectos: Desarrollar conceptos innovadores desde cero.
Mejora del rendimiento del agente en la nube de Copilot
Para mejorar el rendimiento y abordar las limitaciones, use estas medidas:

Asegúrese de que sus tareas estén bien definidas proporcionando lo siguiente:

Una descripción clara del problema que se va a resolver o del trabajo necesario.
Criterios de aceptación completos sobre el aspecto de una buena solución (por ejemplo, ¿debería haber pruebas unitarias?).
Sugerencias sobre qué archivos deben cambiarse.
Personalización de la experiencia con contexto adicional

Copilot Cloud Agent aprovecha el mensaje, los comentarios y el código del repositorio como contexto al generar cambios sugeridos. Mejore los resultados agregando instrucciones personalizadas de Copilot para que el agente comprenda cómo compilar, probar y validar sus cambios.

Otras personalizaciones útiles:

Personalización del entorno de desarrollo para el agente en la nube de GitHub Copilot
Personalización o deshabilitación del firewall para el agente en la nube de GitHub Copilot
Extender el Agente en la Nube de GitHub Copilot con el Protocolo de Contexto del Modelo (MCP)
Uso de Copilot Cloud Agent como herramienta, no como reemplazo

Revise y pruebe siempre el contenido generado por el agente para asegurarse de que cumple sus requisitos y está libre de errores o problemas de seguridad antes de la combinación.

Uso de procedimientos de codificación y revisión de código seguros

Aunque Copilot Cloud Agent puede generar código sintácticamente correcto, es posible que no siempre sea seguro. Siga los procedimientos recomendados para la codificación segura (evitar secretos codificados de forma rígida, evitar vulnerabilidades de inyección) y aplicar pruebas rigurosas, examen de IP y comprobaciones de vulnerabilidades.

Proporcionar comentarios

Si encuentra algún problema o limitaciones, use el icono de pulgar hacia abajo debajo de una respuesta del agente o comparta comentarios en el foro de discusión de la comunidad.

Manténgase al día

Copilot Cloud Agent está evolucionando. Supervise los nuevos riesgos de seguridad y los procedimientos recomendados a medida que surjan.

Medidas de seguridad para Copilot Cloud Agent
Evitar la elevación de privilegios

Copilot Cloud Agent responderá solo a las interacciones de usuarios con acceso de escritura.
Los flujos de trabajo de acciones desencadenados por las solicitudes de cambios del agente requieren aprobación de un usuario con acceso de escritura antes de que se ejecuten.
Los caracteres ocultos (que no se muestran en GitHub.com) se filtran para reducir los riesgos de inyección de indicaciones.
Restricción de los permisos de Copilot

El agente solo tiene acceso al repositorio que tiene asignado; no puede acceder a otros repositorios.
Las inserciones se limitan a las ramas con nombres que comienzan por copilot/ (no la rama predeterminada).
El agente no tiene acceso a secretos o variables de acciones de la organización o repositorio en tiempo de ejecución. Solo se pasan al agente los secretos o variables agregadas al entorno de Copilot.
Prevención de la filtración de datos

Un firewall está habilitado de forma predeterminada para evitar la filtración accidental o malintencionada de código o datos confidenciales. Consulte Personalización o deshabilitación del firewall para gitHub Copilot Cloud Agent .

Limitaciones del agente en la nube de Copilot
Según el código base y las entradas, el rendimiento puede variar. Tenga en cuenta estas restricciones:

Ámbito y calidad limitados: Es posible que LLM no controle ciertas estructuras de código o lenguajes ocultos; la calidad varía según la cobertura de idioma.
Posibles sesgos: Los datos de entrenamiento y el contexto recuperado pueden incluir sesgos; El agente puede inclinarse hacia determinados idiomas o estilos.
Riesgos de seguridad: El código generado se basa en el contexto del repositorio y podría exponer información confidencial si no se revisa; se requiere una revisión exhaustiva.
Código inexacto: El código puede parecer correcto, pero ser semántica o sintácticamente incorrecto o desalineado con la intención. Valide el ajuste, los patrones y el estilo.
Código público: El agente puede producir coincidencias o coincidencias cercanas al código público incluso si se establece "Bloquear"; Es posible que no se proporcionen referencias.
Legal/normativo: Garantizar el cumplimiento de las obligaciones aplicables; evitar usos prohibidos en términos de servicio y códigos de conducta.


## Ejercicio: Expansión del equipo con Copilot Cloud Agent
En este ejercicio, aprenderá a:

Aprenda cómo habilitar Copilot Cloud Agent en su repositorio.
Asigne un problema y comprenda el progreso del agente.
Colabore con el agente en los cambios de código.
Personalice y optimice el área de trabajo del agente.
Prepara las tareas para obtener mejores resultados.
Cómo empezar
Al seleccionar el botón Iniciar el ejercicio en GitHub siguiente, se le dirigirá a un repositorio de plantillas de GitHub público que le pedirá que complete una serie de pequeños desafíos.

Cuando haya terminado el ejercicio en GitHub, vuelva aquí para lo siguiente:

Una comprobación rápida de conocimientos.
Un resumen de lo que ha aprendido.
Un distintivo por completar este módulo.
Inicio del ejercicio en GitHub

## Resumen
El agente de nube de GitHub Copilot le permite delegar cambios bien definidos de baja a media complejidad—correcciones de errores, nuevas funciones, refactor, pruebas, documentación—mientras conserva su flujo de trabajo nativo de GitHub. Asigna la tarea; el agente trabaja en un entorno seguro de Actions con un firewall, abre un PR de borrador y tú revisas, solicitas cambios con @copilot y apruebas.

Puede controlar la seguridad, la gobernanza y el gasto: protecciones de rama, puertas de aprobación, minutos de Acciones y PRU (una solicitud premium por solicitud de modelo). Puede personalizar el entorno de compilación, aprovechar los ejecutores más grandes, habilitar LFS y ampliar las funcionalidades a través de MCP-all con registros claros y rastreabilidad. Estás listo para probar el agente de programación en tu organización: habilítalo en un repositorio, asigna un problema pequeño, observa los registros, itera a través de comentarios de la PR, valida con la CI y mide el tiempo que recuperas para el trabajo de mayor valor.

Ahora que ha completado este módulo, puede hacer lo siguiente:

Explicar qué es Copilot Cloud Agent, quiénes pueden usarlo y dónde se ejecuta.
Habilite el agente a nivel de organización o repositorio y familiarícese con los términos de la versión preliminar.
Delegar el trabajo asignando incidencias o pidiendo a Copilot que abra un pull request.
Realice un seguimiento del progreso a través de líneas de tiempo de PR y registros de sesión en directo, y realice iteraciones con @copilot.
Aplique el modelo de seguridad y los límites de protección integrados (límites de rama, aprobaciones, firewall).
Identifique riesgos y mitigaciones (permisos, protecciones contra inyección de indicaciones, atribución).
Reconozca los límites de flujo de trabajo y compatibilidad y planee las tareas en consecuencia.
Personalice el entorno del agente con copilot-setup-steps.yml, variables de entorno/secretos, ejecutores más grandes y LFS.
Amplíe las funcionalidades con servidores de Protocolo de contexto de modelo (MCP) (por ejemplo, GitHub, Playwright).
Valide la calidad con CI, conjuntos de reglas y generación de pruebas y use PRU intencionadamente.
Solución de problemas comunes (disponibilidad, aprobaciones, registros, firewall, límites de imagen).
Aprende más
Acerca de GitHub Copilot Cloud Agent
Uso de GitHub Copilot para trabajar en un problema
Pedir a GitHub Copilot que cree una solicitud de incorporación de cambios
Solución de problemas del agente en la nube de Copilot de GitHub
Personalización del entorno de desarrollo para Copilot Cloud Agent
Personalización o deshabilitación del firewall para Copilot Cloud Agent
Extensión del agente en la nube de Copilot con el protocolo de contexto de modelo (MCP)
Procedimientos recomendados: Adición de instrucciones personalizadas al repositorio
Uso de la revisión de código de Copilot de GitHub
Conjuntos de reglas de repositorio (protecciones de rama y revisiones necesarias)
Facturación de GitHub Copilot y Unidades de Solicitud Premium (PRUs)
Centro de confianza de GitHub Copilot
Blog de GitHub: "GitHub Copilot: Reunirse con el nuevo agente de codificación"
Introducción al Protocolo de contexto de modelo (MCP)
Proporcionar comentarios
Use este formulario de problema para proporcionar comentarios de contenido o cambios sugeridos para este módulo de Microsoft Learn. GitHub mantiene este contenido y un miembro del equipo evaluará la solicitud. Gracias por darse el tiempo de mejorar nuestro contenido.
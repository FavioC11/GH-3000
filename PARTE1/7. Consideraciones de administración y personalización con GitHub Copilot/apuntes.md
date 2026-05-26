# Consideraciones de administración y personalización con GitHub Copilot
## Introducción
En GitHub, estamos comprometidos con el avance de una IA segura y fiable. Creemos en el poder de la IA para mejorar la eficiencia y la innovación en todo el ciclo de vida del desarrollo de software con el fin de aumentar la felicidad de los desarrolladores. GitHub sigue garantizando que los avances de la IA sean accesibles y beneficiosos para todos.

En este módulo, obtendrá información sobre lo siguiente:

Los planes de GitHub Copilot y sus funciones asociadas de administración y personalización.
Las protecciones contractuales en GitHub Copilot y deshabilitación del código público coincidente.
La administración de las exclusiones de contenido.
Problemas comunes con GitHub Copilot y sus soluciones.
Comencemos explorando los planes de GitHub Copilot y sus controles de privacidad.

## Explore los planes de GitHub Copilot y sus características asociadas de administración y planeamiento
GitHub permite a los desarrolladores y organizaciones maximizar su potencial mediante la priorización de la seguridad, privacidad, cumplimiento y transparencia a medida que desarrollamos, iteramos e innovamos en GitHub Copilot.

Cada desarrollador y organización tiene necesidades específicas. Por eso GitHub Copilot tiene varios planes de precios.

En esta unidad aprenderá lo siguiente:

Las directivas de administración y características de personalización de GitHub Copilot Gratis, Pro, Business y Enterprise.
Factores clave de seguridad y privacidad que debe tener en cuenta a la hora de elegir un plan.
Características de directivas de administración
Característica	Gratis* y Pro	Negocio	Empresa
Filtro de código público	✅	✅	✅
Administración de usuarios	❌	✅	✅
Datos excluidos del entrenamiento de forma predeterminada	❌	✅	✅
Seguridad de clase empresarial	❌	✅	✅
Indemnización de propiedad intelectual	❌	✅	✅
Exclusiones de contenido	❌	✅	✅
Autenticación de inicio de sesión único de SAML	❌	✅	✅
Requiere GitHub Enterprise Cloud	❌	❌	✅
Métricas de uso	❌	✅	✅
*GitHub Copilot Gratis tiene limitaciones de uso

Características de personalización
Característica	Gratis* y Pro	Negocio	Empresa
Adaptar las conversaciones de chat a su código base privado	❌	❌	✅
Integraciones ilimitadas con extensiones de Copilot (beta pública)	✅	✅	✅
Crear una extensión privada para herramientas internas (beta pública)	✅	✅	✅
Adjuntar bases de conocimiento al chat para el contexto organizativo	❌	❌	✅
*GitHub Copilot Gratis tiene limitaciones de uso

Al seleccionar un plan de precios de GitHub Copilot, usted y su organización deben tener en cuenta estos factores clave:

Privacidad y seguridad de los datos: Los planes ofrecen distintos niveles de privacidad de datos y medidas de seguridad. Por ejemplo, GitHub Copilot Business y Enterprise son los únicos planes que proporcionan controles de privacidad más sólidos. Estos controles incluyen la capacidad de excluir archivos específicos del análisis de GitHub Copilot, acceder a registros de auditoría detallados y proporcionar indemnización por IP.
Administración de directivas: La capacidad de administrar las directivas de Copilot en un nivel organizativo es fundamental. Los planes Business y Enterprise permiten administrar las directivas de forma exhaustiva, para ayudar a garantizar que los datos confidenciales se controlan de acuerdo con las directivas de confidencialidad de la organización.
Recopilación y retención de datos: Comprender cómo se recopilan y conservan los datos es esencial para el cumplimiento de las normativas de privacidad de datos. Los suscriptores individuales pueden elegir si GitHub recopila y conserva sus indicaciones y sugerencias de Copilot.
Privacidad de datos e indemnización por IP: Para empresas y empresas, la indemnización por IP y la privacidad de los datos son fundamentales para evitar problemas legales, de seguridad y de clientes. Evaluar la necesidad de estas características puede ayudar a determinar el plan de precios más adecuado para su empresa.
 Sugerencia

GitHub Copilot ofrece un nivel gratuito con 2000 autocompletados de código y 50 mensajes de chat al mes. Para empezar, abra Visual Studio Code, haga clic en el icono de GitHub Copilot y, a continuación, haga clic en "Iniciar sesión para usar GitHub Copilot de forma gratuita". Inicie sesión en la cuenta de GitHub en la ventana que se abrirá en el explorador. Más información. Los educadores, estudiantes y los mantenedores de código abierto seleccionados pueden recibir Copilot Pro de forma gratuita, obtenga información sobre cómo: https://aka.ms/Copilot4Students.

En la siguiente unidad, repasaremos las protecciones contractuales en GitHub Copilot y cómo deshabilitar el código público coincidente.
## Exploración de las protecciones contractuales en GitHub Copilot y deshabilitación del código público coincidente
Para ayudar a garantizar que su organización siga cumpliendo los requisitos legales, debe comprender cómo las protecciones contractuales y las características de GitHub Copilot pueden ayudar a proteger el código y los datos.

Protecciones contractuales
Para ayudar a garantizar que su organización siga siendo compatible con los requisitos legales, GitHub Copilot ofrece:

Indemnización por IP: los planes de GitHub Copilot Business y Enterprise incluyen indemnización por IP, que proporciona protección jurídica contra reclamaciones de propiedad intelectual relacionadas con el uso de sugerencias de Copilot. Con la indemnización por IP, si se impugna cualquier sugerencia de GitHub Copilot como infracción de derechos de propiedad intelectual de terceros, GitHub asume responsabilidad jurídica. Para que GitHub asuma la responsabilidad jurídica, se debe bloquear la configuración de código público coincidente.
Acuerdo de protección de datos (DPA): GitHub ofrece un DPA que describe las medidas adoptadas para proteger los datos y garantizar el cumplimiento de las normativas sobre privacidad de datos. Estos acuerdos proporcionan transparencia y la garantía de que sus datos se tratan de forma segura y responsable.
Centro de confianza de GitHub Copilot: el Centro de confianza de GitHub Copilot proporciona información detallada sobre cómo funciona GitHub Copilot, incluidas las medidas de seguridad, privacidad, cumplimiento y propiedad intelectual. Este recurso ayuda a las organizaciones a sentirse seguros con GitHub Copilot, a la vez que se adhieren a los procedimientos recomendados y los requisitos legales.
Filtrado del código público coincidente
GitHub Copilot puede ayudar a minimizar la posible superposición de código mediante la identificación y el filtrado de sugerencias de código que coincidan con el código disponible públicamente. Esta característica es esencial para mantener la originalidad y la seguridad del código base. Puede reducir el riesgo de incorporar código no seguro o no conforme en los proyectos.

Diferencias clave
Ámbito	Quién puede administrar	Qué controla	Notas
Organización (planes de negocio/empresariales)	Administradores	Filtro de código público para todos los miembros; necesario para la indemnización por propiedad intelectual	Los administradores de la organización pueden bloquear sugerencias que coincidan con el código público para todos los miembros. Esto es necesario para activar la indemnización de propiedad intelectual.
Cuenta personal (Gratis, Pro, Pro+): pago individual	Usuario individual	Alternar con Permitir o Bloquear sugerencias que coincidan con el código público	Los usuarios que compran su propia licencia de Copilot pueden controlar completamente esta configuración en su cuenta personal en Copilot → Características → Privacidad.
Cuenta personal (Gratis, Pro, Pro+) – proporcionada por la organización	Usuario individual	Alternar con Permitir o Bloquear sugerencias que coincidan con el código público	Si su puesto lo asigna una organización, el botón de alternancia puede estar bloqueado y reflejará la política de la organización.
Administración del filtro de código público de la organización
En el caso de las organizaciones con planes Business o Enterprise, los administradores pueden controlar si Copilot bloquea las sugerencias que coinciden con el código público. Esto es importante para el cumplimiento y para habilitar la indemnización por propiedad intelectual.

Pasos para los administradores de la organización:

En la esquina superior derecha de GitHub, haga clic en la imagen del perfil y seleccione Sus empresas o Sus organizaciones.
Junto a la empresa u organización que desea configurar, haga clic en Configuración.
En la barra lateral izquierda, haga clic en Copilot en Código, planificación y automatización.
Haga clic en Características y desplácese hasta la sección Privacidad .
Busque Sugerencias que coincidan con el código público y elija la opción deseada (por ejemplo, Bloquear para evitar sugerencias coincidentes en toda la organización).
Haga clic en Guardar para aplicar los cambios.
Administración de sugerencias de código público para usuarios personales
Si paga por su propia licencia de Copilot (Gratis, Pro o Pro+), puede controlar las sugerencias que coincidan con el código público directamente en su cuenta.

Pasos para titulares de licencias personales:

En la esquina superior derecha de GitHub, haga clic en la imagen del perfil y, a continuación, seleccione Configuración.
En la barra lateral izquierda, haga clic en Copilot en Código, planificación y automatización.
Haga clic en Características y desplácese hasta la sección Privacidad .
Busque Sugerencias que coincidan con el código público y cambie entre Permitir o Bloquear según sus preferencias.
Su elección afectará inmediatamente a las sugerencias que Copilot proporciona en su entorno personal.
Ahora vamos a explorar la administración de la exclusión de contenido de una lente interna.

## Administrar exclusiones de contenido
La característica de exclusión de contenido de GitHub Copilot ayuda a proteger la información confidencial evitando el uso de archivos, directorios o repositorios específicos para informar a las sugerencias de finalización de código.

En esta unidad aprenderá lo siguiente:

Habilitación de exclusiones de contenido de repositorios y organizaciones.
Análisis del impacto de las exclusiones de contenido en sugerencias de código generadas.
Identificar escenarios en los que es posible que las exclusiones de contenido no sean totalmente eficaces.
Configuraciones para la exclusión de contenido
Para implementar estrategias de exclusión de contenido, los administradores de repositorios y los propietarios de la organización pueden usar las siguientes configuraciones.

Configuración de exclusiones de contenido para repositorios
En GitHub, vaya a la página principal del repositorio.

En el nombre del repositorio, seleccione Configuración.

En la barra lateral, en la sección Código y automatización, seleccione Copilot.

En la sección Repositorios y rutas de acceso para excluir, especifique los archivos o directorios que se van a excluir de las sugerencias de Copilot.

Configuración de exclusiones de contenido para organizaciones
En la esquina superior derecha de GitHub, seleccione la foto del perfil y, a continuación, seleccione Las organizaciones.

Junto a la organización, seleccione Configuración.

En la barra lateral izquierda, seleccione Copilot>Exclusión de contenido.

Escriba los detalles de los archivos o repositorios que se van a excluir de las sugerencias de Copilot.

Impacto de la exclusión de contenido en las sugerencias de código
Puede utilizar exclusiones de contenido para configurar GitHub Copilot para que ignore determinados archivos. Cuando se excluye contenido de GitHub Copilot:

La finalización de código ya no está disponible en los archivos afectados.
El contenido de los archivos afectados no informará a las sugerencias de finalización de código en otros archivos.
El contenido de los archivos afectados no informará a las respuestas de Chat de GitHub Copilot.
Las exclusiones de contenido pueden afectar significativamente a la calidad y relevancia de las sugerencias de código que genera GitHub Copilot. Cuando se excluyen determinados archivos o directorios, GitHub Copilot no usará el contenido de esos archivos para informar a sus sugerencias. Esta acción puede dar lugar a sugerencias de código más seguras y compatibles, pero también puede reducir el contexto general disponible para GitHub Copilot. Esta reducción podría afectar potencialmente a la precisión y utilidad de las sugerencias.

Por ejemplo, excluir un archivo de configuración crítico puede impedir que Copilot sugiera fragmentos de código relevantes que dependan de las configuraciones definidas en ese archivo. Es esencial analizar cuidadosamente qué archivos deben excluirse para equilibrar seguridad y funcionalidad.

Solo puede especificar exclusiones de contenido en la configuración de una organización o repositorio. Los ajustes de exclusión de contenido que se definen en una organización o repositorio dentro de una empresa se aplican a todos los miembros que tienen licencia como parte de una suscripción a GitHub Copilot Business o GitHub Copilot Enterprise.

Limitaciones de las exclusiones de contenido
Aunque las exclusiones de contenido son una herramienta valiosa para administrar la privacidad y la seguridad, es posible que no sean totalmente eficaces en algunos escenarios. Por ejemplo:

Limitaciones del IDE: En algunos entornos de desarrollo integrados (IDE), es posible que las exclusiones de contenido no se apliquen cuando se usan determinadas características, como el chat de Copilot. Por ejemplo, en Visual Studio Code y Visual Studio, no se aplican exclusiones de contenido cuando se usa el participante de chat de @github en su pregunta.
Información semántica: Copilot podría seguir usando información semántica de un archivo excluido si el IDE proporciona la información en un archivo no aislado. Esto incluye información sobre tipos y definiciones de símbolos o llamadas a funciones utilizadas en el código.
Ámbito de la directiva: La configuración de exclusión de contenido solo se aplica a los miembros de la organización en la que se configura la exclusión de contenido. Cualquier otra persona que pueda acceder a los archivos especificados todavía puede ver sugerencias de finalización de código y respuestas de Chat de Copilot que hacen referencia a los archivos especificados.
Comprender estas limitaciones es crucial para administrar eficazmente las exclusiones de contenido y garantizar que la información confidencial esté adecuadamente protegida.

## Solución de problemas comunes con GitHub Copilot
Vamos a explorar problemas comunes con GitHub Copilot y cómo solucionarlos.

Faltan sugerencias de código
Uno de los problemas más comunes que encuentran los usuarios con GitHub Copilot es la ausencia de sugerencias de código. Si Copilot no proporciona sugerencias de código en el editor, pruebe estas acciones de solución de problemas:

Compruebe la conexión a Internet: Asegúrese de que tiene una conexión a Internet estable, ya que GitHub Copilot requiere una conexión activa para funcionar correctamente.
Actualice la extensión de Copilot: Asegúrese de que usa la versión más reciente de la extensión de GitHub Copilot. Es posible que las versiones anteriores no se comuniquen eficazmente con los servidores Copilot.
Compruebe la compatibilidad del IDE: Confirme que el IDE es compatible con GitHub Copilot. Algunos IDE pueden requerir configuraciones o actualizaciones específicas para trabajar con Copilot.
Revise las exclusiones de contenido: Si algunos archivos se excluyen de un análisis de Copilot, es posible que las sugerencias no aparezcan para esos archivos. Compruebe los valores de exclusión de contenido para asegurarse de que están configurados correctamente.
Al realizar estas acciones, a menudo puede resolver problemas relacionados con sugerencias de código que faltan y asegurarse de que Copilot funciona según lo previsto.

Las exclusiones de contenido no funcionan según lo esperado
Las exclusiones de contenido están diseñadas para evitar que GitHub Copilot use archivos o directorios específicos. Sin embargo, es posible que las exclusiones de contenido no funcionen según lo previsto en algunos escenarios. Estos son algunos problemas comunes y sus soluciones:

Aplicación diferida de exclusiones: Después de agregar o cambiar exclusiones de contenido, los cambios pueden tardar hasta 30 minutos en surtir efecto en los IDE en los que la configuración ya está cargada. Para aplicar los cambios inmediatamente, vuelva a cargar la configuración de exclusión de contenido en el IDE.

Ámbito inadecuado de exclusiones:

La configuración de exclusión de contenido solo se aplica a los miembros de la organización en la que configuró la exclusión. Asegúrese de que todos los miembros del equipo pertinentes tengan aplicada la configuración adecuada.

Compruebe el icono de GitHub Copilot en la barra de estado. Si se aplica una exclusión de contenido de GitHub Copilot al archivo, el icono de GitHub Copilot tiene una línea diagonal a través de él. Mantenga el puntero sobre el icono para ver si una organización o el repositorio primario han deshabilitado GitHub Copilot para el archivo.

Limitaciones específicas del IDE: En algunos IDE, es posible que las exclusiones de contenido no se apliquen cuando se usan determinadas características, como Chat de GitHub Copilot. Tenga en cuenta estas limitaciones y ajuste el flujo de trabajo en consecuencia.

Al comprender y solucionar estos problemas, puede asegurarse de que las exclusiones de contenido se aplican de forma eficaz y ayudan a proteger la información confidencial.

Las sugerencias de código no son satisfactorias
Si las sugerencias que genera GitHub Copilot no son satisfactorias, puede usar estas técnicas para pedir a Copilot que proporcione mejores resultados:

Proporcione un contexto claro: Asegúrese de que el código proporciona un contexto claro para que GitHub Copilot genere sugerencias pertinentes. Esta tarea incluye escribir comentarios descriptivos y usar nombres de variable significativos.
Use comandos de Copilot: En algunos IDE, puede usar comandos específicos para pedir a Copilot que genere sugerencias. Por ejemplo, en Visual Studio Code, puede usar el acceso directo Ctrl+Entrar para desencadenar GitHub Copilot.
Ajuste la longitud de la indicación: A veces, proporcionar una indicación más larga o más detallada puede ayudar a Copilot a generar mejores sugerencias. Experimente con diferentes longitudes de indicación para ver qué funciona mejor.
Mediante estas técnicas, puede mejorar la calidad de las sugerencias de GitHub Copilot y mejorar la experiencia de codificación.

Ahora, vamos a probar el conocimiento que obtuvo de este módulo.

## Resumen
La administración y el control de la personalización son una parte vital del uso de una herramienta de programación en pareja de IA como GitHub Copilot. En este módulo, se han explorado estos temas:

Los planes de GitHub Copilot y sus funciones asociadas de administración y personalización
Las protecciones contractuales en GitHub Copilot y deshabilitación del código público coincidente
La administración de exclusiones de contenido en GitHub Copilot
La revisión de problemas comunes con GitHub Copilot y sus soluciones
Con este conocimiento, puede seleccionar la opción adecuada para las necesidades de la organización.

Recursos
Centro de confianza de GitHub
Establecimiento de la confianza al usar GitHub Copilot
Adopción responsable de GitHub Copilot con el Centro de confianza de GitHub Copilot
Exclusión del contenido de GitHub Copilot
Proporcionar comentarios
Use este formulario de problema para proporcionar comentarios de contenido o cambios sugeridos para este módulo de Microsoft Learn. GitHub mantiene este contenido y un miembro del equipo evaluará la solicitud. Gracias por darse el tiempo de mejorar nuestro contenido.
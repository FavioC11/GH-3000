# Compilación de aplicaciones con el modo de agente de Copilot de GitHub
## Introducción
En este módulo, aprenderá a compilar una aplicación mediante el modo de agente de Copilot de GitHub en un espacio de código de GitHub y el IDE de VS Code. Explore cómo solicitar eficazmente el modo de agente para crear aplicaciones de forma autónoma, usar archivos de documentación para guiar claramente su comportamiento y aprovechar sus eficaces funcionalidades de iteración. En concreto, verá de primera mano cómo el modo de agente de Copilot interactúa de forma inteligente con la base de código para detectar y corregir errores, refactorizar el código existente para mejorar el mantenimiento y desarrollar de forma autónoma nuevas características que le permiten centrarse más en la innovación y menos en las tareas de codificación repetitivas.

Objetivos de aprendizaje
Al final de este módulo, podrá:

Descripción de cómo desarrollar con el IDE de VS Code en un gitHub Codespace
Solicitar el modo agente de GitHub Copilot para crear una aplicación
Usar archivos de documentación para instruir al modo de agente de GitHub Copilot
Comprenda cómo el modo de agente de Copilot de GitHub recorre en iteración una base de código para:
Corrección de errores
Refactorización de código
Desarrollo de nuevas características
Prerrequisitos
Una cuenta de GitHub y un conocimiento fundamental de GitHub Copilot
Incluir conceptos o aptitudes que ayuden a los alumnos a tener éxito

## ¿Qué es el modo agente de GitHub Copilot?
El modo de agente copilot de GitHub representa un avance importante en el desarrollo de software asistido por IA. A diferencia de los asistentes de creación de código tradicionales que proporcionan sugerencias sencillas de estilo autocompletar, el modo de agente funciona como programador del mismo nivel autónomo que ayuda a los desarrolladores a lograr más con menos esfuerzo. No solo sugiere código, comprende todo su entorno de trabajo, procesa las tareas dinámicamente e itera sobre sus propios resultados para mejorar las soluciones.

Con el modo agente, GitHub Copilot puede crear aplicaciones desde cero, refactorizar código entre varios archivos, escribir y ejecutar pruebas y migrar código heredado a marcos modernos. También puede generar documentación, integrar nuevas bibliotecas y responder a preguntas complejas sobre un código base. Esto le permite centrarse en la resolución de problemas de nivel superior, mientras que Copilot controla muchos de los aspectos repetitivos o lentos del desarrollo de software.

Funcionamiento del modo de agente copilot de GitHub
Uno de los aspectos más eficaces del modo de agente es su capacidad de analizar un código base completo y determinar los archivos y dependencias pertinentes antes de realizar cambios. En lugar de confiar únicamente en el contexto inmediato de un único archivo, el modo de agente evalúa la estructura más amplia de un proyecto, lo que garantiza que las modificaciones sean coherentes y se alineen con los procedimientos recomendados. Este nivel más profundo de comprensión hace que Copilot sea capaz de ayudar con tareas que requieren una perspectiva de todo el proyecto, como la refactorización en varios archivos o la actualización de una aplicación completa para usar un nuevo marco.

A diferencia de la finalización de código tradicional con tecnología de inteligencia artificial, que proporciona sugerencias estáticas, el modo de agente funciona dinámicamente mediante el procesamiento de solicitudes en ciclos iterativos. Cuando se le asigna una tarea, es:

Determina los archivos y dependencias pertinentes antes de realizar modificaciones.
Sugiere y ejecuta los cambios de código al asegurarse de que se alinean con la estructura del proyecto.
Ejecuta comandos de terminal según sea necesario, como compilar código, instalar dependencias y ejecutar pruebas.
Supervisa y refina su salida, iterando varias veces para corregir problemas y mejorar la precisión.
Este proceso iterativo permite a Copilot funcionar como una inteligencia artificial verdaderamente colaborativa, mejorando continuamente sus propias sugerencias al tiempo que mantiene al desarrollador en control total.

Interacción con GitHub Copilot
GitHub Copilot ofrece varias maneras de ayudarle en el flujo de trabajo de desarrollo, cada uno diseñado para admitir diferentes niveles de interacción y automatización.

Las sugerencias insertadas funcionan de forma similar a las herramientas de autocompletar tradicionales, pero con funcionalidades más avanzadas, lo que ofrece finalizaciones de código en tiempo real a medida que escribe.

Copilot Chat proporciona un panel de chat dedicado donde puede formular preguntas relacionadas con la codificación y, a diferencia de los asistentes genéricos de chat de IA, adapta las respuestas en función del contexto de los archivos y dependencias del proyecto.

Si necesita modificaciones más amplias y estructuradas, Las ediciones de Copilot le permiten aplicar cambios en varios archivos para alinearse con objetivos específicos, lo que facilita la implementación eficaz de actualizaciones a gran escala.

Por último, el modo de agente lleva la automatización al siguiente nivel mediante la orquestación dinámica de las tareas de desarrollo, no solo refina sus propias salidas, sino que también itera varias veces para mejorar la precisión, lo que lo convierte en un eficaz colaborador de inteligencia artificial que puede controlar flujos de trabajo complejos. Comprender cómo aprovechar estos diferentes modos de forma eficaz puede ayudarle a integrar Copilot sin problemas en el proceso de desarrollo.

Ventajas del modo agente
Al integrar el modo agente de Copilot de GitHub en flujos de trabajo de desarrollo, los desarrolladores pueden aumentar significativamente la productividad al tiempo que mantienen un control total sobre sus proyectos. Dado que Copilot controla muchos de los aspectos tediosos de la codificación, como ediciones repetitivas, administración de dependencias y pruebas, reduce la carga cognitiva y permite a los desarrolladores centrarse en el diseño de nivel superior y la resolución de problemas. Además, dado que el modo de agente recorre en iteración sus propias salidas, ayuda a garantizar la calidad del código detectando errores y refinando soluciones antes de que requieran revisión manual.

En última instancia, el modo de agente de Copilot de GitHub actúa como algo más que un asistente de INTELIGENCIA ARTIFICIAL, sirve como colaborador inteligente y proactivo que se adapta al flujo de trabajo de un desarrollador y mejora su capacidad de crear, mantener y optimizar software de forma eficaz.

## Explorar el poder de la asistencia para el desarrollo autónomo
El modo de agente copilot de GitHub mejora significativamente la codificación tradicional asistida por ia mediante el control autónomo de tareas complejas y de varios pasos y la iteración continua en sus soluciones. Comprender esta funcionalidad permite a los desarrolladores simplificar los flujos de trabajo, optimizar la productividad y equilibrar eficazmente la automatización con la supervisión humana.

Operación autónoma
El modo agente de Copilot analiza de forma independiente las solicitudes de codificación, identifica dinámicamente los archivos pertinentes, determina los comandos de terminal adecuados e implementa soluciones completas sin instrucciones paso a paso explícitas.

Ejemplo
Tarea: Cree un nuevo punto de conexión de API REST.

Modo de agente de forma autónoma:

Crea rutas de API (routes/api.js)
Actualiza la aplicación principal (app.js)
Instala las dependencias necesarias (npm install express)
Genera casos de prueba (tests/api.test.js)
Aunque es altamente autónomo, el modo de agente proporciona a los desarrolladores una transparencia completa y control sobre cada cambio propuesto.

Control de tareas complejas y de varios pasos
Más allá de las sugerencias de código simples, el modo de agente destaca en dividir tareas complejas en acciones estructuradas y secuenciales. Esta funcionalidad reduce significativamente la carga de trabajo manual y acelera las operaciones complejas del proyecto.

Ejemplo de tarea de varios pasos
Tarea: Integre una nueva base de datos en una aplicación existente.

El modo de agente realiza lo siguiente de forma autónoma:

Actualiza las dependencias (npm install mongoose)
Genera lógica de conexión de base de datos (database.js)
Modifica la configuración del entorno (.env)
Crea definiciones de modelo de datos pertinentes (models/userModel.js)
Escribe pruebas automatizadas asociadas (tests/userModel.test.js)
Este enfoque sistemático simplifica las tareas de desarrollo complejas.

Flujos de trabajo de orquestación en varios pasos
El modo de agente se destaca en la coordinación de procesos de desarrollo complejos mediante orquestación inteligente. En lugar de requerir intervención manual en cada paso, el modo de agente puede redactar, revisar y refinar el código en un flujo de trabajo sin problemas que acelera los ciclos de desarrollo.

Flujo de trabajo borrador-revisión-aceptar
Considere cómo controla el modo de agente el desarrollo de características a través de un enfoque integrado:

Escenario: Adición de la autenticación de usuario a una aplicación

Fase de borrador: El modo de agente analiza los requisitos y genera:

Middleware de autenticación (middleware/auth.js)
Rutas de inicio de sesión de usuario (routes/auth.js)
Utilidades de hash de contraseñas (utils/password.js)
Formulario básico de inicio de sesión de front-end (views/login.html)
Fase de revisión: El modo de agente evalúa inmediatamente su propio borrador:

Identifica posibles vulnerabilidades de seguridad en el control de contraseñas
Sugiere mejoras en los patrones de control de errores
Recomienda validación adicional para casos perimetrales
Propone pruebas unitarias para funciones de autenticación críticas
Fase de aceptación: Learner revisa la implementación refinada lista para PR:

Característica completa con procedimientos recomendados de seguridad integrados
Control y validación de errores completos
Código listo para combinar que sigue las convenciones del proyecto
Documentación y pruebas incluidas desde el principio
Este enfoque orquestado elimina los ciclos de revisión tradicionales de ida y vuelta, lo que permite una entrega más rápida de las características listas para producción.

 Nota

Cada entrega en modo agente consume ~1 PRU. Por lo general, una secuencia de borrador y revisión de 2 pasos usa 2–3 PRU. Para obtener más información, consulte Facturación y solicitudes de GitHub Copilot.

Construcción automatizada de fundaciones
El modo de agente brilla al controlar tareas repetitivas de configuración, lo que permite a los desarrolladores centrarse en la lógica empresarial principal en lugar de en la implementación reutilizable:

Escenario: Configuración de un nuevo microservicio

El modo de agente genera automáticamente:

Estructura del proyecto con directorios estándar (src/, tests/, config/)
Configuración del paquete (package.json, Dockerfile, .gitignore)
Configuración del marco de pruebas (jest.config.js, archivos de prueba de ejemplo)
Configuración de la canalización de CI/CD (.github/workflows/test.yml)
Plantillas de configuración del entorno (.env.example, config/default.js)
Configuración básica de supervisión y registro (utils/logger.js, puntos de conexión de verificación de salud)
El desarrollador se centra en:

Implementación de modelos de dominio y lógica de negocios específicos
Personalización de la base generada para requisitos únicos
Adición de integraciones especializadas y flujos de trabajo personalizados
Esta división del trabajo maximiza la productividad de los desarrolladores mediante la automatización de la configuración estándar al tiempo que conserva el control creativo sobre la funcionalidad básica.

Funcionalidades avanzadas de razonamiento
En escenarios complejos que requieren un análisis más profundo, el modo de agente puede aprovechar el razonamiento premium para proporcionar soluciones más sofisticadas:

Análisis de decisiones arquitectónicas: Evaluación del equilibrio entre diferentes enfoques de implementación
Evaluación del impacto entre sistemas: Comprender cómo afectan los cambios a varios componentes
Estrategias de optimización del rendimiento: Identificar cuellos de botella y sugerir mejoras
Análisis de vulnerabilidades de seguridad: Detección y propuesta de correcciones para posibles problemas de seguridad
 Nota

El razonamiento premium (con modelos más avanzados) proporciona un contexto más completo y un análisis más profundo, pero, a menudo, duplica el consumo PRU. Una sola solicitud puede usar ~4+ PRUs en comparación con ~2 con el modelo estándar. Para obtener más información, consulte Facturación y solicitudes de GitHub Copilot.

Uso de herramientas inteligentes y reconocimiento del contexto
Para completar eficazmente las tareas, el modo de agente usa el contexto de los archivos, dependencias y acciones anteriores del proyecto. Al analizar la estructura y el contexto existentes del proyecto, ofrece salidas precisas y contextualmente relevantes.

Ejemplo de implementación compatible con contexto
Escenario: Implementación de una aplicación react.

Modo agente de forma inteligente:

Reconoce el tipo de proyecto a través de package.json
Ejecuta los scripts de compilación adecuados (npm run build)
Prepara los scripts de implementación alineados con los contextos de flujo de trabajo existentes.
Proporcionar contexto claro y completo garantiza mejores resultados más precisos.

Mejora iterativa y recuperación automática
Una de las ventajas principales del modo agente de Copilot es su capacidad iterativa de resolución de problemas. Si se produce un error, el modo de agente detecta, corrige y vuelve a validar sus soluciones de forma autónoma, lo que minimiza significativamente el esfuerzo de depuración manual.

Ejemplo de recuperación automática
Problema: Las pruebas unitarias generadas fallan inicialmente debido a un error de sintaxis.

Modo de agente de forma autónoma:

Detecta la causa del error.
Aplica una solución correctiva
Vuelva a ejecutar las pruebas hasta que pasen con éxito.
Este proceso iterativo mejora la confiabilidad del código y acelera la resolución de problemas.

Garantizar el control y la supervisión del usuario
A pesar de su autonomía, el modo de agente mantiene a los desarrolladores totalmente en control. Cada acción propuesta por el modo de agente se puede revisar, ajustar o revertir en cualquier momento, lo que garantiza la alineación con los estándares del proyecto.

Ejemplo de control de desarrollador
Situación: El modo de agente propone cambios exhaustivos en la lógica de autenticación.

El desarrollador puede:

Revisión de los cambios resumidos en una solicitud de cambios
Solicitar modificaciones o revisiones específicas
Deshacer o ajustar fácilmente los cambios según sea necesario
Esto garantiza un equilibrio productivo entre la eficacia controlada por la inteligencia artificial y el juicio humano.

Limitaciones y consideraciones prácticas
Aunque es eficaz, el modo de agente tiene limitaciones. Puede tener problemas con la lógica de dominio especializada, las reglas de negocios matizadas o cuando falta el contexto crítico del proyecto.

Ejemplo de limitación
Limitación: Lógica de negocios personalizada mal documentada.

Posibles resultados:

Soluciones menos precisas o incompletas
Mayor necesidad de revisión y intervención manuales
Comprender estas limitaciones ayuda a los desarrolladores a establecer expectativas realistas y proporcionar un contexto más claro para maximizar los resultados.

El modo de agente copilot de GitHub representa un avance significativo en el desarrollo de software asistido por ia, combinando operaciones autónomas con iteración inteligente y funcionalidades de supervisión sólidas. Al comprender sus funcionalidades, administrar de forma proactiva las limitaciones y usar eficazmente sus herramientas integradas, los desarrolladores pueden mejorar significativamente la productividad, mantener estándares de código de alta calidad y acelerar su flujo de trabajo de desarrollo general.

## Ejercicio de aptitudes de GitHub
Información general del ejercicio
Bienvenido a Combineton High School! En esta sesión práctica de aptitudes, usted toma el rol de un profesor de gimnasio que desarrolla OctoFit Tracker, una aplicación de fitness social diseñada para ayudar a los estudiantes a mantenerse activos y competir con sus compañeros. Con el modo de agente copilot de GitHub, creará rápidamente un prototipo funcional mientras aprende los procedimientos recomendados para el desarrollo asistido por IA.

Objetivos del taller
Al final de este taller, hará lo siguiente:

Configure un entorno de desarrollo mediante GitHub Codespaces.
Use GitHub Copilot para acelerar el desarrollo de aplicaciones.
Implemente las características principales del rastreador de OctoFit con el modo agente de Copilot.
Aplique los procedimientos recomendados para solicitar y refinar el código generado por ia.
Características de la aplicación
OctoFit Tracker incluye:

Perfiles de usuario para estudiantes y profesores de gimnasio.
Seguimiento de actividades para supervisar el progreso de la aptitud.
Creación y administración de equipos para objetivos colaborativos.
Tablas de clasificación para clasificar el rendimiento de los alumnos.
Sugerencias de entrenamiento personalizadas para ayudar a los alumnos a mejorar.
Ejercicio práctico: desarrollo del rastreador de OctoFit
Este ejercicio le guía por los pasos siguientes:

Configure un GitHub Codespace para el desarrollo.
Instale y configure GitHub Copilot.
Use el modo agente de Copilot para generar y refinar los componentes clave de la aplicación.
Implemente el seguimiento de fitness, las tablas de clasificación y los perfiles de usuario con asistencia de IA.
Pruebe y optimice el código generado por ia.
Comenzar
Haga clic en Iniciar el ejercicio en GitHub para ir a un repositorio de plantillas donde complete una serie de desafíos de codificación. Antes de empezar, siga estos pasos:

Seleccione Start course (Iniciar curso ) o Use this template (Usar esta plantilla ) para crear su propio repositorio. Se recomienda usar un repositorio público, ya que los repositorios privados consumen minutos de acciones. Espere unos 20 segundos después de la instalación y actualice la página.

Siga las instrucciones LÉAME del repositorio para completar el ejercicio.

Una vez completado el ejercicio, vuelva a este módulo para:

Prueba de conocimientos breve
Resumen de lo que ha aprendido
Distintivo por completar este módulo
 Nota

No es necesario modificar los archivos del flujo de trabajo para completar este ejercicio. La modificación del contenido de este flujo de trabajo puede interrumpir la capacidad del ejercicio para validar las acciones, proporcionar comentarios o calificar los resultados.

## Resumen
Desde la creación autónoma de aplicaciones para refactorizar e iterar de forma inteligente en el código base, el modo agente de Copilot de GitHub mejora el flujo de trabajo de desarrollo de software, lo que le permite abordar tareas complejas con una eficacia sin precedentes.

Junto con GitHub Codespaces y Visual Studio Code, el modo de agente usa la documentación, el contexto y la información del proyecto para impulsar de forma autónoma mejoras, corregir problemas y desarrollar nuevas características. GitHub sigue evolucionando las funcionalidades de Copilot, impulsando los límites del desarrollo asistido por ia, lo que permite a los desarrolladores centrarse en la innovación significativa y la resolución de problemas de alto nivel.

Ahora que completó este módulo, debería poder:

Desarrolle aplicaciones con el IDE de VS Code en GitHub Codespaces.
Solicite el Modo Agente de GitHub Copilot para crear aplicaciones nuevas autónomamente.
Use archivos de documentación para guiar eficazmente el modo del agente copilot de GitHub.
Comprenda cómo el modo del agente copilot de GitHub corrige de forma iterativa errores, refactoriza el código y desarrolla nuevas características en un proyecto.
Referencias
Características de GitHub Copilot
GitHub Copilot: El agente despierta
Presentación del modo agente de Copilot de GitHub (versión preliminar)
Desarrollo en Visual Studio Code
Unidades de solicitud Premium (PRU): documentación de GitHub
Proporcionar comentarios
Use este formulario de problema para proporcionar comentarios de contenido o cambios sugeridos para este módulo de Microsoft Learn. GitHub mantiene este contenido y un miembro del equipo evaluará la solicitud. Gracias por darse el tiempo de mejorar nuestro contenido.

Introducción a Azure
Elige la cuenta de Azure que más te convenga. Paga por uso o prueba Azure gratis por hasta 30 días. Regístrate.
# Uso de las características avanzadas de GitHub Copilot
## Introducción
GitHub Copilot es un asociado de codificación de IA que proporciona sugerencias de autocompletar mientras se codifica. Para obtener sugerencias, escriba código o de forma interactiva mediante lenguaje natural.

Copilot analiza su archivo y los archivos relacionados, ofreciendo sugerencias en su editor de texto. Use el contexto del código y los comentarios escritos y, a continuación, sugiere nuevas líneas o funciones completas.

GitHub Codespaces es un entorno de desarrollador hospedado que funciona en la nube que se puede ejecutar con Visual Studio Code. Puede personalizar la experiencia de desarrollo para cualquier proyecto de desarrollo en GitHub, preinstalar dependencias, bibliotecas e, incluso, extensiones y configuraciones de Visual Studio Code.

Escenario: Trabajar con un proyecto existente
Como desarrollador, querrá ser más productivo escribiendo código más rápido tanto para los nuevos proyectos netos como para los existentes. Para esta tarea, quiere usar características avanzadas de un asistente de IA que ayude a mejorar los flujos de trabajo del desarrollador en la escritura de código, la documentación, las pruebas y mucho más.

En este módulo, comprenderá cómo puede usar características avanzadas de GitHub Copilot con ejemplos aplicados que modifican un repositorio mediante distintas técnicas para agregar nuevos puntos de conexión de LA API HTTP (interfaz de programación de aplicaciones), escribir pruebas unitarias y documentar código existente.

¿Qué descubriré?
Al concluir este módulo, adquirirá las aptitudes para:

Trabaje con un repositorio de GitHub preconfigurado en Codespaces con la extensión GitHub Copilot.
Uso de características interactivas de GitHub Copilot para generar sugerencias útiles para un proyecto existente.
Aplique características avanzadas de GitHub Copilot para obtener más información sobre un nuevo proyecto, escribir documentación y crear pruebas unitarias.
¿Cuál es el objetivo principal?
Después de finalizar correctamente este módulo, podrá usar avisos interactivos y otras características avanzadas de GitHub Copilot para mejorar un proyecto de software.

Requisitos previos
Conocimientos básicos de Python y editores de texto.
Comprensión básica de Git y GitHub Fundamentals y ejecución de comandos git básicos, como git add y git push.
Se requiere una cuenta de GitHub con una suscripción activa para GitHub Copilot para su cuenta personal de GitHub o una cuenta de GitHub administrada por una organización o empresa. Con fines de aprendizaje, la opción Copilot Free con límites de uso debe ser suficiente.
## Características avanzadas de GitHub Copilot
A menudo, al trabajar con código, debe revisar la documentación del proyecto además de las bibliotecas y la documentación del marco. Para escribir código o documentación, debe tener una buena comprensión del código base. Las tareas como corregir errores y escribir pruebas pueden requerir mucho tiempo, pero al mismo tiempo son necesarias para la mayoría de los proyectos. Afortunadamente, GitHub Copilot tiene varias características avanzadas que pueden hacer que estas tareas sean más fáciles y eficaces.

Conceptos básicos
Cuando GitHub Copilot está habilitado, proporciona sugerencias. Estas sugerencias se denominan texto fantasma. Puede omitir el texto fantasma o aceptarlo presionando la tecla Tabulador. Las sugerencias no requieren una indicación porque GitHub Copilot usa de manera predeterminada los archivos que tiene abiertos como contexto. No obstante, puede proporcionar un solicitud mediante un comentario, la ventana de chat o el chat en línea en el código.

Chatear con GitHub Copilot
GitHub Copilot le permite tener una discusión interactiva mediante la característica de chat. En Visual Studio Code, puede hacer clic en el icono de chat de la barra lateral izquierda, que abre la interfaz de chat en un panel dedicado.

En este panel, puede hacer preguntas sobre el código en el que está trabajando actualmente u otras preguntas relacionadas con el software.

Uso del chat en línea
Además del panel de chat dedicado, puede usar el chat en línea. Permite interactuar con GitHub Copilot sin salir del código.

Acceda al chat en línea mediante Ctrl+i en Windows o Command+i en un equipo Mac. Una de las ventajas de usar el chat en línea es que no tiene que cambiar de contexto si va a otro panel. Las sugerencias e interacciones se producen más cerca del código.

Comandos de barra diagonal
Dentro del panel de chat o al usar el chat en línea, puede usar comandos de barra oblicua. Estos comandos permiten a GitHub Copilot usar una intención específica para resolver rápidamente tareas comunes de desarrollo.

Si escribe una barra oblicua en el panel de chat o en el chat en línea, debería ver un menú desplegable con todos los comandos de barra oblicua disponibles. Por ejemplo, el comando de barra oblicua /tests le ayuda a escribir pruebas, mientras que el comando /docs está pensado para escribir documentación.

El uso de comandos de barra oblicua específicos para crear una pregunta es una buena manera de obtener mejores respuestas sin tener que escribir mensajes más largos.

Agentes
Visual Studio Code tiene una característica denominada agentes que le permite interactuar con GitHub Copilot. Estos agentes permiten formular preguntas mediante un contexto específico. Por ejemplo, el agente @terminal te ayuda a comunicarte con GitHub Copilot para interactuar con el terminal.
## Ejercicio: Configuración de GitHub Copilot para trabajar con Visual Studio Code
En este ejercicio, se crea un repositorio mediante la plantilla de GitHub para una API web que usa el lenguaje de programación Python.

Configuración del entorno
En primer lugar, debe iniciar el entorno de Codespaces, que viene preconfigurado con la extensión GitHub Copilot.

Abra Codespace con el entorno preconfigurado en el explorador.
En la página Crear codespace, revise las opciones de configuración del codespace y seleccione Crear nuevo codespace.
Espere a que se inicie Codespace. Este proceso de startup puede tardar unos minutos.
Los demás ejercicios de este proyecto tienen lugar en el contexto de este contenedor de desarrollo.
 Importante

Todas las cuentas de GitHub pueden usar Codespaces durante un máximo de 60 horas gratis cada mes con dos instancias principales. Para obtener más información, consulte Almacenamiento y horas de núcleo incluidas mensualmente en GitHub Codespaces.

 Sugerencia

GitHub Copilot ofrece un nivel gratuito con 2000 autocompletados de código y 50 mensajes de chat al mes. Para empezar, abra Visual Studio Code, haga clic en el icono de GitHub Copilot y, a continuación, haga clic en "Iniciar sesión para usar GitHub Copilot de forma gratuita". Más información. Los educadores, los estudiantes y algunos mantenedores de código abierto pueden recibir Copilot Pro de forma gratuita, aprende cómo: https://aka.ms/Copilot4Students.

API web de Python
Cuando haya finalizado, Codespaces se carga con una sección de terminal en la parte inferior. Codespaces instala todas las extensiones necesarias en el contenedor. Una vez completadas las instalaciones del paquete, Codespaces ejecuta el comando para iniciar la uvicorn aplicación web que se ejecuta dentro de Codespace.

Cuando la aplicación web se inicia correctamente, un mensaje en la pestaña Puertos de terminal muestra que el servidor se ejecuta en el puerto 8000 dentro de Codespace.

Registro en GitHub Copilot
Si aún no lo ha hecho, debe registrarse configurando una prueba gratuita o una suscripción para su cuenta.

 Nota

Los educadores, estudiantes y los mantenedores de código abierto pueden registrarse de forma gratuita en Copilot, aprender cómo en Configuración de GitHub Student y GitHub Copilot como desarrollador de estudiantes autenticados.

## Técnicas aplicadas de GitHub Copilot
En unidades anteriores, se mostró cómo configurar Copilot y se mencionó cómo puede ayudarle a ser más rápido como desarrollador que empieza a escribir código.

En esta unidad, vamos a analizar cómo Copilot puede ayudarle con proyectos existentes y con tareas más complicadas.

Tareas avanzadas con GitHub Copilot
Es habitual trabajar con un proyecto existente como ingeniero. Al corregir código o implementar características, es necesario escribir documentación y pruebas, y trabajar con comandos del terminal. Veamos algunas maneras de hacerlo mediante GitHub Copilot.

Mensajes implícitos
Aunque puede ser específico en los mensajes para obtener instrucciones de GitHub Copilot, puede aprovechar las características que proporcionan implícitamente un aviso creado previamente para obtener una buena respuesta.

Por ejemplo, si está trabajando en un proyecto de Python y tiene un archivo abierto con el código siguiente que tiene un error:

Python
with open("file.txt", "r") as file:
    # Read the file and print the content
    contents = file.read
Después de seleccionar el código y usar Ctrl+i en Windows o Cmd+i en un equipo Mac, puede pedir a GitHub Copilot que le ayude a corregir el código mediante el chat insertado y el comando de barra diagonal /fix.

Si solo escribe /fix, podría obtener una respuesta de GitHub Copilot similar a esta sugerencia: "Para corregir el código, agregaría paréntesis después de file.read para llamar al método read y corregir el error tipográfico en el nombre del método".

Los comandos de barra diagonal se pueden usar tanto en el chat insertado como en la interfaz de chat. Además del /fix comando, estos son algunos de los comandos de barra diagonal más útiles que puede usar en el chat de Copilot:

/doc: agrega comentarios al código especificado o seleccionado.
/explain: obtiene explicaciones sobre el código.
/generate: genera código para responder a la pregunta especificada.
/help: obtiene ayuda sobre cómo usar el chat de Copilot.
/optimize: analiza y mejora el tiempo de ejecución del código seleccionado.
/tests: crea pruebas unitarias para el código seleccionado.
El uso de comandos de barra diagonal permite una interacción más sencilla con GitHub Copilot y le ayuda a obtener mejores respuestas sin tener que escribir solicitudes más largas.

La combinación de características como los comandos de barra diagonal con el chat en línea le permite elegir la manera que mejor se adapte a usted y al código en el que esté trabajando.

Contexto selectivo
GitHub Copilot se puede personalizar para proporcionar sugerencias en función del contexto en el que trabaja. Por ejemplo, puede pedir a GitHub Copilot que proporcione sugerencias basadas en todo el área de trabajo o en la salida del terminal.

GitHub Copilot puede proporcionarle sugerencias precisas para el proyecto sin necesidad de abrir muchos archivos. Imagine que necesita empaquetar el proyecto mediante un Dockerfile. Un Dockerfile es un archivo especial que debe tener instrucciones específicas para empaquetar el proyecto. Puede usar El chat de Copilot de GitHub para preguntar cómo ayudarle. Por ejemplo, abra GitHub Copilot Chat y escriba el siguiente comando:

text
I need to create a Dockerfile for this project, can you generate one that will help me package it?
Obtendrá una respuesta que explica los pasos para crear un Dockerfile para el proyecto junto con una explicación sobre lo que debe hacerse en los pasos del archivo.

Como siempre, si las sugerencias no son exactamente lo que está buscando, puede volver a escribir el mensaje y ser más específico. Por ejemplo, podría pedir a GitHub Copilot que use un paso específico al crear el Dockerfile:

text
Help me create a Dockerfile to package this project but make sure you are using a Virtual Environment for Python.
Copilot también puede proporcionar sugerencias específicas del contexto según el área en la que estés trabajando. Por ejemplo, puede usar el @terminal agente para obtener ayuda con errores o comandos que permiten a Copilot proporcionar sugerencias basadas en la salida del terminal.

Ejemplo: @terminal ¿Cómo se corrige el mensaje de error que veo?

Si no logra avanzar o no obtiene los resultados que desea, puede replantear la consulta o empezar a escribir código para que Copilot lo autocomplete.

 Nota

De forma predeterminada, GitHub Copilot usa archivos abiertos en el editor de texto como contexto adicional.

## Ejercicio: actualización de una API web con GitHub Copilot

Vamos a explorar cómo puede modificar un repositorio de Python mediante técnicas avanzadas de GitHub Copilot para un punto de conexión de API. Obtenga una experiencia más práctica mediante este repositorio que contiene una aplicación web de Python que hospeda una API de Tiempo de Viajes.

¿Qué es una API?
Una API actúa como intermediario que permite que diferentes aplicaciones se comuniquen entre sí. Por ejemplo, un sitio web meteorológico puede compartir datos históricos o proporcionar funcionalidad de previsión a través de su API. Con la API, puede insertar los datos en el sitio web o crear una aplicación que comparta datos meteorológicos con otras características.

Extensión de la API web
La API actual no expone el país o región, que debe implementarse para enumerar ciudades. La ruta solo debe permitir solicitudes HTTP GET con una respuesta JSON que proporcione información de los niveles históricos altos y bajos de ese país o región, ciudad y mes determinado.

 Nota

Para este ejercicio, use Codespace con el entorno preconfigurado en el explorador.

Paso 1: Adición de una nueva ruta
Abra el archivo main.py y use el chat en línea con el comando Ctrl+i (en Windows) o Command+i (en Mac). Este comando pide a GitHub Copilot que le ayude a crear una nueva API que muestre las ciudades de un país o región. Usa la siguiente indicación:

text
Create a new route that exposes the cities of a country/region.
Este indicador debe proporcionarle algo similar a lo siguiente:

Python
# Create a new route that exposes the cities of a country:
@app.get('/countries/{country}')
def cities(country: str):
    return list(data[country].keys())

 Nota

Pruebe la nueva ruta y perfeccione el mensaje hasta que el resultado sea el deseado.

Paso 2: Creación de una prueba
Ahora que ha creado una nueva ruta, cree una prueba con Copilot Chat para esta ruta que usa España como país o región. Recuerde seleccionar el código y pedir al chat de Copilot que le ayude con esta API específica que acabamos de crear. Puede usar el chat en línea o el panel de chat dedicado con el siguiente mensaje:

text
/tests help me to create a new test for this route that uses Spain as the country/region.
Una vez que Copilot le ayuda a crear la prueba, pruébela. Si no funciona según lo esperado, no dude en compartir esos detalles con Copilot en el chat. Por ejemplo:

text
This test is not quite right, it is not including cities that doesn't exist. Only Seville is part of the API.
Paso 3: Uso de un agente para escribir la documentación
Por último, use el modo agente de chat de Copilot de GitHub para escribir documentación del proyecto y detalles sobre cómo ejecutar el propio proyecto. Abra el archivo README.md y use la siguiente instrucción en GitHub Copilot Chat:

text
I want to document how to run this project so that other developers can get started quickly by reading the README.md file.
Debe obtener una respuesta que le ayude a actualizar el archivo README.md con la información necesaria para ejecutar el proyecto.

Enhorabuena por completar este ejercicio. Ha usado GitHub Copilot para generar una nueva ruta de API y, a continuación, ha escrito una prueba para comprobar su exactitud. Por último, ha agregado documentación mediante un agente que ayudará a los desarrolladores a comprender cómo ejecutar este proyecto.

Cuando haya terminado el ejercicio en GitHub, vuelva aquí para lo siguiente:

Prueba de conocimientos breve
Resumen de lo que ha aprendido
Distintivo por completar este módulo

## Resumen
GitHub Copilot es una herramienta que ofrece muchas maneras de interactuar con el proyecto y le ayuda a convertirse en un desarrollador más eficaz. Agregar pruebas, corregir errores o generar automatización le permite mejorar el ciclo de vida de desarrollo de los proyectos.

Tras finalizar este módulo, debería poder:

Use características de GitHub Copilot, como chat, agentes, chat en línea y comandos de barra diagonal, que ofrecen más flexibilidad para realizar tareas de codificación.
Utiliza el chat de GitHub Copilot para proporcionar asistencia basada en el contexto al trabajar en tu proyecto y generar salida relevante.
Eliminación de los recursos de Codespaces
Para evitar consumir todo el tiempo mensual de GitHub Codespaces, es importante eliminar todos los recursos después de cargar los cambios en el repositorio. Siga estos pasos para quitar tus recursos:

Vaya a Codespaces en GitHub aquí.
Busque la instancia de Codespace en la lista y seleccione el menú de tres puntos para mostrar las opciones.
Seleccione Eliminar para quitar la instancia de Codespace.
 Nota

Si no confirmas tus cambios en tu repositorio, perderás todo tu trabajo. Por lo tanto, es importante confirmar y enviar los cambios antes de eliminar la instancia de Codespace.

Referencias
¿Qué es GitHub Copilot?
Introducción a GitHub Copilot
Código con GitHub Codespaces
Proporcionar comentarios
Use este formulario de problema para proporcionar comentarios de contenido o cambios sugeridos para este módulo de Microsoft Learn. GitHub mantiene este contenido y un miembro del equipo evaluará la solicitud. Gracias por darse el tiempo de mejorar nuestro contenido.
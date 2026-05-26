# Uso de GitHub Copilot con Python
## Introducción
GitHub Copilot es un asociado de codificación de IA que proporciona sugerencias de autocompletar mientras se codifica. Puede obtener sugerencias de Copilot escribiendo código o describiéndolo en lenguaje natural.

Copilot analiza su archivo y los archivos relacionados, ofreciendo sugerencias en su editor de texto. Usa OpenAI Codex, un nuevo sistema de inteligencia artificial desarrollado por OpenAI para ayudar a derivar el contexto del código y los comentarios escritos y, a continuación, sugiere nuevas líneas o funciones completas.

GitHub Codespaces es un entorno de desarrollador hospedado que funciona en la nube que se puede ejecutar con Visual Studio Code. Puede personalizar la experiencia de desarrollo para cualquier proyecto de desarrollo en GitHub, preinstalar dependencias, bibliotecas e, incluso, extensiones y configuraciones de Visual Studio Code.

Escenario: mejora de un proyecto
Como desarrollador, querrá ser más productivo al escribir código para los proyectos nuevos y los existentes. Para esta tarea, querrá averiguar si una inteligencia artificial asistente es lo que necesita para mejorar flujos de trabajo de desarrollador en la escritura de código, documentación, pruebas y mucho más.

En este módulo, aprenderá a usar GitHub Copilot para modificar un proyecto mediante una solicitud para personalizar una API de Python. También aprenderá a usar sugerencias dinámicas después de escribir código inicial.

Al completar este módulo, habrá:

Configurado un repositorio de GitHub en Codespaces e instalado la extensión de GitHub Copilot.
Diseñado indicaciones para generar sugerencias a partir de GitHub Copilot.
Aprendido a aplicar GitHub Copilot para mejorar los proyectos de Python.
¿Cuál es el objetivo principal?
Después de finalizar correctamente este módulo, podrá usar mensajes para personalizar proyectos de Python con GitHub Copilot en GitHub Codespaces.

Requisitos previos
Conocimientos básicos de Python y editores de texto.
Comprensión básica de los aspectos básicos de Git y GitHub. En particular, ejecutando comandos básicos de git como git add y git push.
Se requiere una cuenta de GitHub con una suscripción activa para GitHub Copilot para su cuenta personal de GitHub o una cuenta de GitHub administrada por una organización o empresa. Con fines de aprendizaje, la opción Copilot Free con límites de uso debe ser suficiente.


## ¿Qué es GitHub Copilot?
A menudo, al escribir código, debe consultar documentación oficial u otras páginas web para recordar la sintaxis o cómo resolver un problema. También puede dedicar horas a intentar resolver un problema cuando el código no funciona. Además, también dedica tiempo a escribir pruebas y documentación. Todas estas tareas requieren mucho tiempo. Para ser más eficiente, puede usar fragmentos de código, o bien confiar en las herramientas del entorno de desarrollo integrado (IDE). ¿Hay una forma mejor?

¿Cómo funciona?
GitHub Copilot es un asistente de inteligencia artificial que se usa desde el IDE y que es capaz de generar código y mucho más. GitHub Copilot usa mensajes. Un mensaje es texto en lenguaje natural que escribe. Copilot usa el texto para proporcionar sugerencias en función de lo que escriba.

Un mensaje puede ser similar al ejemplo siguiente:

Python
# Create a web API using FastAPI with a route to products.
Después, Copilot usa el mensaje para generar una respuesta que puede aceptar o rechazar. Una respuesta al mensaje podría ser similar al siguiente código:

Python
from fastapi import FastAPI
app = FastAPI()

@app.get("/products")
def read_products():
    return []
Cómo reconoce las solicitudes
Copilot puede decir que algo es un mensaje o una instrucción, si:

Lo escribe como un comentario en un archivo de código con un archivo que termina como .py o .js.
Escribe texto en un archivo Markdown y espera unos segundos a que Copilot devuelva una respuesta.
Aceptación de sugerencias
Lo que recibe de Copilot es una sugerencia, o texto que se muestra como código gris, si usa el negro como color de texto. Para aceptar la sugerencia, deberá presionar la tecla Tabulador.

Copilot podría ofrecer más de una sugerencia. En este caso, puede iterar por las sugerencias mediante Ctrl + Entrary seleccionar la más adecuada.

## Ejercicio: Configuración de GitHub Copilot para trabajar con Visual Studio Code
En este ejercicio, se crea un repositorio mediante la plantilla de GitHub para la aplicación web de front-end de cartera personal de Python.

Cómo configurar GitHub Copilot
Para usar GitHub Copilot, debe completar los siguientes pasos:

Cuenta de GitHub:

Creación de una cuenta de GitHub. Dado que Copilot es un servicio de GitHub, necesita una cuenta de GitHub para usarlo. Si no tiene una cuenta, visite la página web de GitHub para crear una gratuitamente.
Regístrese y habilite GitHub Copilot:

Puede configurar una cuenta gratuita de GitHub Copilot o registrarse para obtener una suscripción a la versión de prueba de GitHub Copilot Pro con una prueba de un solo día. Con fines de aprendizaje, la opción Copilot Free con límites de uso debe ser suficiente.
Es importante tener en cuenta las condiciones de evaluación gratuita de GitHub Copilot: si elige la oferta de evaluación gratuita para GitHub Copilot, se solicita un formulario de pago al registrarse. Los cargos no se aplicarán hasta que finalice la prueba a menos que cancele antes de la conclusión del período de 30 días.
 Sugerencia

GitHub Copilot ofrece un nivel gratuito con 2000 autocompletados de código y 50 mensajes de chat al mes. Para empezar, abra Visual Studio Code, seleccione el icono de GitHub Copilot y, a continuación, seleccione Iniciar sesión para usar GitHub Copilot gratis. Inicie sesión en la cuenta de GitHub en la ventana que se abre en el explorador. Más información. Los educadores, estudiantes y algunos mantenedores de código abierto seleccionados pueden recibir Copilot Pro de forma gratuita. Descubre cómo en: https://aka.ms/Copilot4Students.

Instale la extensión:

GitHub Copilot está disponible como una extensión para los principales entornos de desarrollo integrado (IDE), incluidos Visual Studio, Visual Studio Code, JetBrains IDE, VIM y XCode.
Para instalarlo, busque "GitHub Copilot" en el marketplace de extensiones del IDE y siga las instrucciones de instalación. Por ejemplo, en el marketplace de VS Code, puede encontrar GitHub Copilot, GitHub Copilot Chat y GitHub Copilot para Azure como opciones para instalar.
Configuración del entorno
En primer lugar, debe iniciar el entorno de Codespaces, que viene preconfigurado con la extensión GitHub Copilot.

Abra Codespace con el entorno preconfigurado en el explorador.
En la página Crear codespace, revise las opciones de configuración del codespace y seleccione Crear nuevo codespace.
Espere a que se inicie Codespace. Este proceso de startup puede tardar unos minutos.
Los demás ejercicios de este proyecto tienen lugar en el contexto de este contenedor de desarrollo.
 Importante

Todas las cuentas de GitHub pueden usar Codespaces durante un máximo de 60 horas gratis cada mes con dos instancias principales. Para obtener más información, consulte Almacenamiento y horas de núcleo incluidas mensualmente en GitHub Codespaces.

API web de Python
Cuando haya finalizado, Codespaces se carga con una sección de terminal en la parte inferior. Codespaces instala todas las extensiones necesarias en el contenedor. Una vez que se completen las instalaciones del paquete, Codespaces ejecutará el comando uvicorn para iniciar la aplicación web en ejecución dentro del Codespace.

Cuando la aplicación web se ha iniciado correctamente, un mensaje en el terminal muestra que el servidor se ejecuta en el puerto 8000 dentro de Codespace.

Prueba de la API
En la pestaña Explorador simple del Codespace, en la página API de Python en contenedor, seleccione el botón Probar. Se abre una página FastAPI en la pestaña Explorador simple que le permite interactuar con la API mediante el envío de una solicitud con la página autodocumentada.

Para probar la API, seleccione el botón POST y, después, el botón Probarlo. Desplácese hacia abajo en la pestaña y seleccione Ejecutar. Si se desplaza más hacia abajo la pestaña, puede ver la respuesta a la solicitud de ejemplo.

## Uso de GitHub Copilot con Python
En unidades anteriores, se mostró cómo configurar Copilot y se mencionó cómo puede ayudarle a ser más rápido como desarrollador que empieza a escribir código.

En esta unidad analizamos cómo Copilot puede ayudarle con los proyectos existentes y con las tareas más complicadas.

Desarrollo con GitHub Copilot
A menudo, cuando desarrollamos proyectos, es necesario asegurarnos de que nuestro código esté fresco y actualizado continuamente. Además, es posible que tengamos que corregir los errores que surjan o agregar nuevas características para mejorar su funcionalidad y facilidad de uso. Vamos a explorar algunas maneras de realizar actualizaciones con GitHub Copilot y GitHub Copilot Chat, una interfaz de chat interactiva que le permite formular preguntas y recibir respuestas a cuestiones relacionadas con el código.

Ingeniería de solicitudes
GitHub Copilot puede sugerir código al escribirlo, pero también puede crear sugerencias útiles mediante la creación de indicaciones. Una solicitud, que es nuestra entrada, es un conjunto de instrucciones o guías que ayudan a generar código. La consulta es útil para generar respuestas específicas de Copilot. La solicitud podría ser un comentario o una entrada al usar GitHub Copilot Chat, que guíe a Copilot a generar código en tu nombre o a escribir código que Copilot complete automáticamente.

La calidad del resultado de Copilot depende de lo bien que elabore su indicación. Diseñar una indicación eficaz es crucial para garantizarle el resultado que desea.

Por ejemplo, considere la siguiente indicación:

Python
# Create an API endpoint
La consulta es ambigua y vaga, por lo que es posible que el resultado de GitHub Copilot no sea lo que necesita. Podría, por ejemplo, sugerirle código que usa un marco que no conoce, o un punto de conexión que requiere datos que no reconoce.

Ahora considere esta indicación:

Python
# Create an API endpoint using the FastAPI framework that accepts a JSON payload in a POST request
La indicación es específica, clara y permite a GitHub Copilot comprender el objetivo y el ámbito de la tarea. Puede proporcionar contexto y ejemplos a Copilot usando comentarios o código, pero también puede usar la opción de GitHub Copilot Chat para mejorar su indicación. Hacer una buena consulta garantiza que el modelo genere una salida de alta calidad.

Procedimientos recomendados con GitHub Copilot
Copilot impulsa la productividad, pero requiere algunos procedimientos recomendados para garantizar la calidad. Algunos procedimientos recomendados al usar Copilot son:

Procure que sus indicaciones sean sencillas y después agregue componentes más elaborados a medida que avance. Por ejemplo:

text
create an HTML form with a text field and button
Luego, profundice más en la consulta para obtener sugerencias más específicas:

text
Add an event listen to the button to send a POST request to /generate endpoint and display response in a div with id "result"
Recorra las sugerencias. Puede hacerlo usando Ctrl+Enter (o Cmd+Enter en un Mac). Obtendrá varias sugerencias de Copilot y puede elegir la mejor salida. Opcionalmente, al usar GitHub Copilot Chat, puedes usar la entrada de chat para agregar el mensaje e interactuar con la salida.

Si no obtiene los resultados que desea, puede reformular la solicitud o empezar a escribir código para que Copilot lo complete automáticamente.

 Nota

GitHub Copilot usa los archivos abiertos en el editor de texto como contexto adicional. Esto es útil porque proporciona información adicional a la consulta o al código que podría estar escribiendo. Si necesita que GitHub Copilot proporcione sugerencias basadas en otros archivos, puede abrirlos o referenciarse a ellos al usar el chat de GitHub Copilot.

## Ejercicio: actualización de una API web de Python con GitHub Copilot
Vamos a explorar cómo puede modificar un repositorio de Python mediante sugerencias de código de GitHub Copilot para crear un formulario HTML interactivo y un punto de conexión de interfaz de programación de aplicaciones (API). Al trabajar con este repositorio, obtendrá rápidamente prácticas con una aplicación web de Python que sirve una API de HTTP que genera un token pseudo-aleatorio, que se usa habitualmente para rutinas de identificación.

¿Qué es una API?
Una API actúa como intermediario que permite que diferentes aplicaciones se comuniquen entre sí. Por ejemplo, un sitio web meteorológico puede compartir datos históricos o proporcionar funcionalidad de previsión a través de su API. Con la API, puede insertar los datos en el sitio web o crear una aplicación que comparta datos meteorológicos con otras características.

Extensión de la API web
La API ya tiene un único punto de conexión para generar un token. Vamos a actualizar la API agregando un nuevo punto de conexión que acepta texto y devuelve una lista de tokens.

 Nota

Para este ejercicio, use Codespace con el entorno preconfigurado en el explorador.

Paso 1: Agregar un modelo Pydantic
Vaya al archivo main.py y agregue un comentario para que GitHub Copilot le pueda generar un modelo Pydantic automáticamente. El modelo generado debería tener un aspecto similar al de este ejemplo:

Python
class Text(BaseModel):

text: str
Paso 2: Generación de un nuevo punto de conexión
A continuación, genere un nuevo punto de conexión con GitHub Copilot agregando el comentario:

Python
# Create a FastAPI endpoint that accepts a POST request with a JSON body containing a single field called "text" and returns a checksum of the text
Paso 3: Agregar las importaciones necesarias
El código generado puede hacer que la aplicación se bloquee si no se importan los módulos base64 y os. Usa GitHub Copilot Chat para pedir a Copilot que te ayude a agregar las importaciones que faltan.

Como alternativa, agregue las siguientes líneas en la parte superior del archivo:

Python
import base64
import os
Por último, compruebe que el nuevo punto de conexión funciona. Para probarlo, vaya al punto de conexión de /docs y confirme que aparece el punto de conexión.

Enhorabuena, en este ejercicio no solo ha usado Copilot para generar código, sino que también lo ha hecho de forma interactiva y divertida. Puede utilizar GitHub Copilot para generar código, escribir documentación, probar sus aplicaciones y mucho más.

Cuando finalice el ejercicio en GitHub, vuelva aquí para:

Prueba de conocimientos breve
Resumen de lo que ha aprendido
Distintivo por completar este módulo

## Resumen
En este módulo, hemos visto cómo GitHub Codespaces puede mejorar significativamente el ciclo de vida de desarrollo de software. Hemos aprendido sobre las características de GitHub Codespaces que van desde la creación de un repositorio desde una plantilla de GitHub para agregar animaciones con sugerencias en directo. GitHub Codespaces le permite personalizar la experiencia de codificación y GitHub Copilot le guía en cada paso del camino.

Después de finalizar este módulo, debería poder:

Configure un repositorio de GitHub en Codespaces e instale la extensión GitHub Copilot.
El ingeniero solicita al proyecto que siga los procedimientos recomendados para generar sugerencias de GitHub Copilot.
Use El chat de Copilot de GitHub para formular preguntas relacionadas con la codificación y recibir respuestas.
Eliminación de los recursos de Codespaces
Para evitar consumir todo su tiempo mensual de GitHub Codespaces, es importante eliminar los recursos después de cargar los cambios en el repositorio.

Siga estos pasos para eliminar la instancia de Codespace:

Vaya a GitHub Codespaces.
Busque la instancia de Codespace en la lista y seleccione el menú ... para mostrar las opciones.
Seleccione Eliminar para quitar la instancia de Codespace.
 Nota

Si no confirmas tus cambios en tu repositorio, perderás todo tu trabajo. Por lo tanto, es importante confirmar y enviar los cambios antes de eliminar la instancia de Codespace.

Referencias
¿Qué es GitHub Copilot?
Introducción a GitHub Copilot
Código con GitHub Codespaces
Proporcionar comentarios
Use este formulario de problema para proporcionar comentarios de contenido o cambios sugeridos para este módulo de Microsoft Learn. GitHub mantiene este contenido y un miembro del equipo evaluará la solicitud. Gracias por darse el tiempo de mejorar nuestro contenido.
# Uso de GitHub Copilot con JavaScript
## Introducción
GitHub Copilot es un asociado de codificación de IA que proporciona sugerencias de autocompletar mientras se codifica. Obtenga sugerencias escribiendo código o describiéndolo en lenguaje natural.

Copilot analiza su archivo y los archivos relacionados, ofreciendo sugerencias en su editor de texto. Usa OpenAI Codex, un nuevo sistema de inteligencia artificial desarrollado por OpenAI para ayudar a derivar el contexto del código y los comentarios escritos y, a continuación, sugiere nuevas líneas o funciones completas.

GitHub Codespaces es un entorno de desarrollador hospedado que funciona en la nube que se puede ejecutar con Visual Studio Code. Puede personalizar la experiencia de desarrollo para cualquier proyecto de desarrollo en GitHub, preinstalar dependencias, bibliotecas e, incluso, extensiones y configuraciones de Visual Studio Code.

Escenario: mejora de un proyecto
Como desarrollador, querrá ser más productivo escribiendo código más rápido tanto para los nuevos proyectos netos como para los existentes. Para esta tarea, esperará que una inteligencia artificial asistente sea lo que necesita para mejorar flujos de trabajo de desarrollador en la escritura de código, documentación, pruebas y mucho más.

En este módulo, comprenderá cómo usar GitHub Copilot con ejemplos aplicados modificando un repositorio mediante un aviso para personalizar el comportamiento del desplazamiento y sugerencias dinámicas después de escribir el código inicial.

¿Qué descubriré?
Al concluir este módulo, habrá adquirido las aptitudes necesarias para:

Configurar un repositorio de GitHub en Codespaces e instalar la extensión de GitHub Copilot.
Avisos diseñados para generar sugerencias a partir de GitHub Copilot
Aplicó GitHub Copilot para mejorar los proyectos.
¿Cuál es el objetivo principal?
Después de finalizar correctamente este módulo, podrá usar mensajes para personalizar proyectos de JavaScript con GitHub Copilot en GitHub Codespaces.

Requisitos previos
Conocimientos básicos de JavaScript y editores de texto.
Comprensión básica de Git y Aspectos básicos de GitHub y ejecución de comandos básicos git como git add y git push.
Se requiere una cuenta de GitHub con una suscripción activa para GitHub Copilot para su cuenta personal de GitHub o una cuenta de GitHub administrada por una organización o empresa. Para aprender, la opción Copilot Free con límites de uso debe ser suficiente.

## Qué es GitHub Copilot
Al escribir código, a menudo se consulta la documentación o las páginas web para recordar la sintaxis o resolver problemas. Es posible que dedique horas a solucionar problemas, escribir pruebas y crear documentación. Estas tareas requieren mucho tiempo. El uso de fragmentos de código o herramientas de IDE puede ayudar, pero ¿hay una mejor manera?

¿Cómo funciona?
GitHub Copilot es un asistente de inteligencia artificial que se usa desde el IDE y que es capaz de generar código y mucho más. GitHub Copilot usa solicitudes, lenguaje natural y proporciona sugerencias basadas en lo que usted escribe. Por ejemplo, un mensaje puede ser un comentario en el archivo de código:

JavaScript
// Create a web API using express and JavaScript with routes for products and customers
Después, Copilot va a generar una respuesta que puede aceptar o rechazar. Una respuesta al mensaje podría ser similar al siguiente código:

JavaScript
const express = require("express");

app = express();
app.path("/products", () => "products");
app.listen(3000, () => "app runs");
Cómo reconoce las solicitudes
Copilot puede reconocer un mensaje o una instrucción si:

Lo escribe como comentario en un archivo de código (por ejemplo, .py, .js).
Escriba texto en un archivo markdown y espere unos segundos para que Copilot responda.
Aceptación de sugerencias
Lo que obtienes de Copilot es una sugerencia, que aparece como texto gris si usa negro como color de texto. Para aceptar la sugerencia, presione la tecla Tab.

Copilot podría sugerir varias opciones. Para recorrer sugerencias, use Ctrl + Entrar y seleccione la más adecuada.

## Ejercicio: Configuración de GitHub Copilot para trabajar con Visual Studio Code
En este ejercicio, se crea un nuevo repositorio mediante la plantilla de GitHub para la aplicación web de front-end de cartera personal de JavaScript.

Cómo configurar GitHub Copilot
Para usar GitHub Copilot, debe completar los siguientes pasos:

Cuenta de GitHub:

Creación de una cuenta de GitHub. Dado que Copilot es un servicio de GitHub, necesita una cuenta de GitHub para usarlo. Si no tiene una cuenta, visite la página web de GitHub para crear una gratuitamente.
Regístrese y habilite GitHub Copilot:

Puede configurar una cuenta gratuita de GitHub Copilot o registrarse para obtener una suscripción a la versión de prueba de GitHub Copilot Pro con una prueba única de 30 días. Con fines de aprendizaje, la opción Copilot Free con límites de uso debe ser suficiente.
Es importante tener en cuenta las condiciones de evaluación gratuita de GitHub Copilot: si elige la oferta de evaluación gratuita para GitHub Copilot, se solicita un formulario de pago al registrarse. Los cargos no se aplicarán hasta que finalice la prueba a menos que cancele antes de la conclusión del período de 30 días.
 Sugerencia

GitHub Copilot ofrece un nivel gratuito con 2000 autocompletados de código y 50 mensajes de chat al mes. Para empezar, abra Visual Studio Code, haga clic en el icono de GitHub Copilot y, a continuación, haga clic en "Iniciar sesión para usar GitHub Copilot de forma gratuita". Inicie sesión en la cuenta de GitHub en la ventana que se abre en el explorador. Más información. Los educadores, los estudiantes y algunos mantenedores de código abierto pueden recibir Copilot Pro de forma gratuita, aprende cómo: https://aka.ms/Copilot4Students.

Instale la extensión:
GitHub Copilot está disponible como una extensión para los IDE principales, incluidos Visual Studio, Visual Studio Code, IDE de JetBrains, VIM y XCode.
Para instalarlo, busque "GitHub Copilot" en el marketplace de extensiones del IDE y siga las instrucciones de instalación. Por ejemplo, en el marketplace de VS Code, encontrará GitHub Copilot, GitHub Copilot Chat y GitHub Copilot para Azure como opciones para instalar.
Configuración de entorno
En primer lugar, debe iniciar el entorno de Codespaces, que viene preconfigurado con la extensión GitHub Copilot.

Seleccione el siguiente botón para Abrir codespace con el entorno preconfigurado.

Abrir en GitHub Codespaces

En la página Crear codespace, revise las opciones de configuración de codespace y, después, seleccione Crear nuevo codespace

Espere a que se inicie Codespace. Este proceso de startup puede tardar unos minutos.

Los demás ejercicios de este proyecto tienen lugar en el contexto de este contenedor de desarrollo.

 Importante

Todas las cuentas de GitHub pueden usar Codespaces durante un máximo de 60 horas gratis cada mes con dos instancias principales. Para obtener más información, consulte Almacenamiento y horas de núcleo incluidas mensualmente en GitHub Codespaces.

Cartera de JavaScript
Cuando haya finalizado, Codespaces se carga con una sección de terminal en la parte inferior. Codespaces instala todas las extensiones y dependencias necesarias en el contenedor. Una vez completada, esta plantilla está configurada para usar npm start para iniciar la aplicación web dentro de su Codespace.

Cuando la aplicación web se ha iniciado correctamente, un mensaje en el terminal muestra que el servidor se ejecuta en el puerto 1234 dentro de Codespace.

## Uso de GitHub Copilot con JavaScript

En unidades anteriores, se mostró cómo configurar Copilot y se mencionó cómo puede ayudarle a ser más rápido como desarrollador que empieza a escribir código.

En esta unidad, vamos a analizar cómo Copilot puede ayudarle con proyectos existentes y con tareas más complicadas.

Desarrollo con GitHub Copilot
A menudo, cuando desarrollamos proyectos, es necesario asegurarnos de que nuestro código esté fresco y actualizado continuamente. Además, es posible que tengamos que corregir los errores que surjan o agregar nuevas características para mejorar su funcionalidad y facilidad de uso. Vamos a explorar algunas maneras de realizar actualizaciones con GitHub Copilot y GitHub Copilot Chat, una interfaz de chat interactiva para formular preguntas y recibir respuestas a cuestiones relacionadas con el código.

Ingeniería rápida
Aunque GitHub Copilot puede sugerir código a medida que escribe, también puede crear consultas para generar sugerencias útiles. Una solicitud, que es nuestra entrada, es un conjunto de instrucciones o guías que ayudan a generar código. La consulta es útil para generar respuestas específicas de Copilot. La solicitud podría ser un comentario o una entrada al usar GitHub Copilot Chat, que guíe a Copilot a generar código en tu nombre o a escribir código que Copilot complete automáticamente.

La calidad de la salida de Copilot depende de la forma en que se elabora la consulta. La creación de un mensaje eficaz es esencial para lograr los resultados deseados. Por ejemplo, si hace la consulta siguiente:

JavaScript
// Create an API endpoint
Dado que la consulta es ambigua y vaga, es posible que el resultado de GitHub Copilot no sea lo que necesita. Por ejemplo, podría usar un marco que no conozca o un punto de conexión que requiera datos que no reconozca. Por ejemplo, si hace la consulta siguiente:

JavaScript
// Create an API endpoint using the React framework that accepts a JSON payload in a POST request
Esta última consulta es específica, clara y permite a GitHub Copilot comprender el objetivo y el ámbito de la tarea. Aunque también puedes proporcionar contexto y ejemplos a Copilot mediante comentarios o código, también puedes usar la opción de GitHub Copilot Chat. Hacer una buena consulta garantiza que el modelo genere una salida de alta calidad.

Procedimientos recomendados con GitHub Copilot
Copilot impulsa la productividad, pero requiere algunos procedimientos recomendados para garantizar la calidad. Algunos procedimientos recomendados al usar Copilot son:

Mantén los mensajes simples y agrega componentes más elaborados a medida que vas avanzando, por ejemplo:

text
create an HTML form with a text field and button
Luego, profundice más en la consulta para obtener sugerencias más específicas:

text
Add an event listen to the button to send a POST request to /generate endpoint and display response in a div with id "result"
Recorra las sugerencias; puede hacerlo mediante Ctrl+Entrar (o Cmd+Entrar en un equipo Mac). Obtendrá varias sugerencias de Copilot y puede elegir la mejor salida. Opcionalmente, al usar GitHub Copilot Chat, puedes usar la entrada de chat para agregar el mensaje e interactuar con la salida.

Si no logra avanzar o no obtiene los resultados que desea, puede reescribir el mensaje o empezar a escribir código para que Copilot lo complete automáticamente.

 Nota

GitHub Copilot usa los archivos abiertos en el editor de texto como contexto adicional. Esto es útil porque proporciona información adicional a la consulta o al código que podría estar escribiendo. Si necesita GitHub Copilot para proporcionar sugerencias basadas en otros archivos, puede abrirlos al usar GitHub Copilot Chat.

## Ejercicio: Actualización de una cartera de JavaScript con GitHub Copilot
Vamos a explorar cómo puede usar las sugerencias de código de GitHub Copilot. En este ejercicio, agregará animaciones con sugerencias en directo y usará un mensaje para personalizar el comportamiento de desplazamiento de un repositorio de plantillas de JavaScript ya existente. Con GitHub Copilot, puede trabajar rápidamente con una situación de JavaScript en la vida real.

Cartera de JavaScript
Tanto si es alumno, se acaba de graduar o es un profesional experimentado, su cartera es su espacio personal para mostrar sus aptitudes y experiencia.

Tener una cartera proporciona credibilidad y notoriedad a la experiencia que menciona en su currículum al solicitar empleos. No importa si es científico de datos, diseñador de la experiencia de usuario o desarrollador front-end. Una presencia fuerte en línea puede ayudarle a conseguir un trabajo y a que le descubran.

 Nota

Para este ejercicio, use Codespace con el entorno preconfigurado en el explorador.

Personalización de la cartera de JavaScript
En esta cartera de plantillas, tenemos una aplicación web basada en React que puede usar para personalizar e implementar contenido fácilmente con solo el explorador web.

Antes de empezar, puede personalizar la cartera con sus propios vínculos. Vaya a src/App.jsx y actualice siteProps con su información. La variable siteProps es un objeto de JavaScript que contiene pares clave-valor que se usan para personalizar el sitio. Debería tener este aspecto:

JavaScript
const siteProps = {
  name: "Alexandrie Grenier",
  title: "Web Designer & Content Creator",
  email: "alex@example.com",
  gitHub: "microsoft",
  instagram: "microsoft",
  linkedIn: "satyanadella",
  medium: "",
  twitter: "microsoft",
  youTube: "Code",
};
Animación de los iconos de las redes sociales con un mensaje
Una animación puede hacer que la sección de redes sociales sea más atractiva. Pida ayuda de Copilot para animar los iconos. Puede usar el chat de GitHub Copilot para preguntar a Copilot o escribir el siguiente comentario de solicitud en el archivo src/styles.css:

css
/* add an amazing animation to the social icons */
La sugerencia de Copilot debería ser similar a la siguiente:

css
img.socialIcon:hover {
  animation: bounce 0.5s;
  animation-iteration-count: infinite;
}

@keyframes bounce {
  0% {
    transform: scale(1);
  }
  50% {
    transform: scale(1.2);
  }
  100% {
    transform: scale(1);
  }
}
Para aceptar la sugerencia, presione el tabulador. Si no recibe la misma sugerencia exacta, puede experimentar con la sugerencia proporcionada o seguir escribiendo el código CSS hasta que coincida.

El sitio ya debe estar ejecutándose en el codespace, y el cambio se volverá a cargar en la página automáticamente. Para verlo, mantenga el puntero sobre uno de los iconos de las redes sociales en el pie de página.

Enhorabuena, a través del ejercicio, no solo ha usado Copilot para generar código, sino que también lo ha hecho de forma interactiva y divertida. Puede utilizar GitHub Copilot no solo para generar código, sino también para escribir documentación, probar sus aplicaciones y mucho más.

Cuando haya terminado el ejercicio en GitHub, vuelva aquí para lo siguiente:

Prueba de conocimientos breve
Resumen de lo que ha aprendido
Distintivo por completar este módulo

## Resumen
Desde la creación de un repositorio a partir de una plantilla de GitHub hasta la adición de animaciones con sugerencias en directo, GitHub Codespaces le permite personalizar la experiencia de codificación y GitHub Copilot le guía en cada paso del camino, mejorando significativamente el ciclo de vida de desarrollo de software.

Tras finalizar este módulo, debería poder:

Comprenda cómo GitHub Copilot puede ayudarle a codificar ofreciendo sugerencias de estilo de autocompletar.
Aplique ingeniería rápida a varios proyectos mediante sus procedimientos recomendados.
Usa GitHub Copilot Chat para formular y recibir preguntas relacionadas con la codificación.
Eliminación de los recursos de Codespaces
Para evitar consumir todo el tiempo mensual de GitHub Codespaces, es importante eliminar todos los recursos después de cargar los cambios en el repositorio. Siga estos pasos para quitar los recursos de la siguiente manera:

Vaya a este enlace https://github.com/codespaces
Busque la instancia de Codespace en la lista y seleccione el menú de tres puntos para mostrar las opciones.
Seleccione "eliminar" para quitar la instancia de Codespace.
 Nota

Si no confirmas tus cambios en tu repositorio, perderás todo tu trabajo. Por lo tanto, es importante confirmar y enviar los cambios antes de eliminar la instancia de Codespace.

Referencias
¿Qué es GitHub Copilot?
Introducción a GitHub Copilot
Código con GitHub Codespaces
Visual Studio Code (YouTube)
Proporcionar comentarios
Use este formulario de problema para proporcionar comentarios de contenido o cambios sugeridos para este módulo de Microsoft Learn. GitHub mantiene este contenido y un miembro del equipo evaluará la solicitud. Gracias por darse el tiempo de mejorar nuestro contenido.
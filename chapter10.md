# FRONT-END WEB

## Diseño Responsivo (Adaptable) [1]

Acercamiento al diseño web en donde el contendio se desarrolla pensando que se pueda acoplar de diferentes maneras según el dispositivo ( tabletas, teléfonos inteligentes / smartphones, libros electrónicos, laptops, computadoras de escritorio, etc) en que se está mostrando la página o aplicación Web.

**¿Por qué tomarse la molestia?**

Cerca del año 2008 los sitios de internet, que antes habían sido pensados y diseñados exclusivamente para computadoras, empezaron a ser consumidos desde diferentes dispositivos, con una variedad de tamaños y resoluciones de pantalla, capacidad de procesamiento y memerio, probocando así una terrible experiencia de uso para los usuarios.

**¿Qué se propuso?**

> One ring to rule them all

> One Web, Web for All, Web on Everything

- Cambiar el diseño pensado en tamaños fijos (pixeles - px) a proporciones
- Instaurar una propuesta desde 1995: Media Queries [2]

  - Permite adaptar la representación del contenido a características del dispositivo como la resolución de pantalla
  - Ejemplo: Cambiar el color de fondo a azul claro para las pantallas que midan 600 px o menos
``` CSS
  @media only screen and (max-width: 600px) {
   body {
       background-color: lightblue;
   }
}
```
  - Surgimiento de librerías front-end (HTML-CSS-JS) que facilitaran el desarrollo responsivo de páginas web:
    - Bootstrap
    - Foundation

## Bootstrap

![](https://images.duckduckgo.com/iu/?u=http%3A%2F%2Fmedia02.hongkiat.com%2Ftwitter-bootstrap%2Ftwitter-bootstrap.jpg&f=1)

_Framework_ (Conjunto de herramientas) desarrollado por el equipo de Twitter para el desarrollo ágil y responsivo de páginas Web. Es _opensource_ (código abierto) por lo que puede ser copiado y modificado a voluntad. De hecho, Es el repocitorio [3] más popular en GitHub.

Puedes descargarlo aquí (https://github.com/twbs/bootstrap)

Está basado en planillas y estilos que te permite desarrollar de manera ágil un sitio web.
  - tipografía
  - paletas de colores por acción
  - formularios
  - botones
  - cuadros
  - menús de navegación
  - cabeceras (headers)


Para el desarrollo responsivo utiliza una filosofía de diseño llamada _Mobile first_ un sistema de cudrículas de 12 columnas por renglón, que pueden anidarse, alinearse, reordenarse o dejar espacio, y pueden adaptarse a 5 tamaños distintos:
  - xs (Extra small) - Telefonos (<768px)
  -	sm (Small) - Tabletas (≥768px)
  -	md (Medium) Laptops y monitores regulares  (≥992px)
  -	lg (Large) Monitores grandes (≥1200px)

Este `div` ocupará 8 de las cuatro columnas en un teléfono celular y 6 en una tablet
``` html
<div class="col-xs-8 col-sm-6">
  Level 2: .col-xs-8 .col-sm-6
</div>
```

Bootstrap basa varias funcionalidades en _pluggins_ (componentes) que ultilizan la librería de javascript [Jquery](https://jquery.com/), posiblemente una de las librerías más ricas y utilizadas. Sus funcionalidades fueron inspiración para siguientes estándares de JS, justo por lo que poco a poco ha ido perdiendo relevancia. Ej:
  - Modal, Dropdown, Scrollspy, Tab, Tooltip, Popover, Alert, Button, Collapse, Carousel y Typeahead

Su uso fue tan popular que, al desarrollar una página web, podías confiar que la librería ya estuviera en el _cache_ de casi cualquier usuario. Gracias a la tecnología [CDN](https://es.wikipedia.org/wiki/Red_de_entrega_de_contenidos) (content delivery network).

## Programación asincrona con Javascript

La **asincronizidad** en un programa de computadora se refiere a la capacidad de responder a eventos que están fuera del flujo principal del programa (Programación secuencial). Eventos como interacción con dispositivos de entrada (Mouse o teclado), lectura o escritura en memoria o dispositivos de almacenamiento, acceso a servicios cliente/servidor. Permite así no detener el programa mientras se espera por la respuesta. Agiliza el proceso de ejecución y en general permite aumentar la escalabilidad, pero complica el razonamiento sobre el programa.

Para dar respuesta a esa complejidad se utilizan distintas estrategias:
  - **Modelo de paso de continuadores** (callbacks) Es el modelo de asincronía más utilizado dentro JS. Cada función recibe información acerca de cómo debe tratar el resultado de cada operación.
  - **Modelo de eventos** (events) Se utiliza una arquitectura dirigida por eventos que permite a las operaciones no bloqueantes informar de su terminación mediante señales de éxito o fracaso.
  - **Modelo de promesas** (promises) Se razona con los valores de retorno de las operaciones no bloqueantes de manera independiente del momento del tiempo en que dichos valores se obtengan.
  - **Modelo de generadores** Se utilizan generadores para devolver temporalmente el control al programa llamante y retornar en un momento posterior a la rutina restaurando el estado en el punto que se abandonó su ejecución.

Para abordar estos problemas, la mayoría de los lenguages de programación (C, C++, Java) antes de Javascript utilizaban una estrategia multi-hilo (_multi-thread_), que implicaba controlar los hilos abiertos y los recursos de procesamiento que cada uno utilizaba y que complicaba la escalabilidad de los programas.

Javascript fue diseñado con un patrón de hilo-único (_single-thread_) y orientado a eventos. En el ciclo de eventos (_Event Loop_) cada evento arrojado tiene asignada una función que se ejecutara (_event handler_) una vez que el evento se produzca. No bloqueando así el flujo eterno que esperará a los eventos y facilitando así la escalabilidad de los progras. Será tan popular su uso que se desarrollará NodeJS, lenguaje de programación con un motor muy similar a JS y la misma sintaxis, pero enfocado a trabajar, no en browsers, pero en servidores y computadoras.

Javascript, al ser el lenguage utilizado para el desarrollo de páginas y aplicaciones web, nació como un leguage con capacidad de asincronizidad, ya que constantemente accede y se comunica con un servidor web para el funcionamiento de las páginas web.

## Manipulación de eventos con Jquery

La evolución del internet propició que cada vez más aplicaciones web requirieran accesar constantente mente a un servidor que procesaría y consultaría información en una Base de Datos mediante un servidor web, ya no requerirían exclusivamente de documentos estáticos, sino que la información que los usuarios fueran accesando a la paǵina, modificarían cómo ésta se comporta. Así nacieron lo que llamaron Páginas Web Dinámicas (_Dynamic Web Pages_), páginas que con la interacción del usuario, cambiarían su contenido.

Para poder facilitar el desarrollo de este tipo de páginas, surgieron distintas librerías de JS, pero ninguna tan famosa como [JQuery]((https://jquery.com/)). Está diseñada para realizar ̣_scripting_ en el lado del cliente (_client-side scripting_), eso quiere decir modificar el DOM (el HTML) utilizando Javascript en el navegador del usuario.

Sus principales capacidades son:
  - Selección y manipulación de elementos del DOM via selectores CSS
  - Manejo de Eventos (onclick, onhover, on-document-ready)
  - Efectos de animación
  - Uso de Ajax (Librería para intercambio de información entre navegador y servidor)
  - Proceso de eventos Asyncronos
  - Parseo de JSON
  - Extensivilidad - creación de plug-ins

Se utiliza principalmente de dos maneras:
  - Metodo fabrica de Objetos Jquery: `$`
    - Normalmente para seleccionar elementos del dom con selectores CSS
  - Funciones prefijas o de utilería que pueden encadenarse: `$.`

``` js
$('select#carmakes')
  .add()
  .after()
  .animate()
  .attr()
```

[Documentacón](https://api.jquery.com/)

## AJAX

Ajax (Asynchronous Javascript and XML) Es una serie de herramientas en Javascript que permiten al navegador comunicarse con uno o varios servidores web y a partir de la respuesta modificar el DOM o realizar otras funciones via Javascript en una página Web. Utiliza estas tecnologías:
  -  HTML (or XHTML) and CSS
  -  El _Document Object Model_ (DOM)
  -  JSON or XML para intercambio de datos
  - XSLT para manipulación de datos
  - The XMLHttpRequest Protocolo de transmisión de datos entre navegaror web y servidor Web
    - `open()`
    - `send()`

Métodos HttpRequest
  - GET para lectura
  - POST registro de nueva información
  - HEAD
  - PUT actualizacion de información
  - DELETE borrado de información
  - OPTIONS

``` js

$.ajax({
	type: 'GET',
	url: 'send-ajax-data.php',
	dataType: "JSON", // data type expected from server
	success: function (data) {
		console.log(data);
	},
	error: function() {
		console.log('Error: ' + data);
	}
});

```

un nuevo método `fetch` ha sido agregado a la librería APi de Javascript para hacer funciones ajax.

## HTML5 Canvas

HTML5 lá útlima versión del estandar HTML evolucionó para facilitar la introducción de elementos multimedia y gráficos. Adios `Adobe Flash`

`<canvas>` `<video>` `<audio>` fueron algunos de los nuevos tags para facilitarlo, aunque también agrega librerías para contenido editable, funcionalidad offline, geolocalización, criptografía, etc.

El elemento HTML <canvas> se puede usar para dibujar gráficos mediante vectores y JavaScript. Por ejemplo, se puede usar para hacer gráficas, composiciones fotográficas, crear animaciones, o incluso procesado o renderizado de vídeo en tiempo real.

``` js
var canvas = document.getElementById(“canvas”);
canvas.width = 800;
canvas.height = 800;
var context = canvas.getContext(“2d”);
```

Rectangulo
``` js
context.fillRect(10,10, 100, 200)
```

Triangulo
``` js
context.beginPath();
  context.moveTo(75, 50);
  context.lineTo(100, 75);
  context.lineTo(100, 25);
  context.lineTo(75, 50);
  context.stroke();
  context.fill();
  ``` js
```

Arco
``` js
context.arc(250, 275, 50, 0, Math.PI, false);
```

## Preprocesadores CSS

CSS parecía primitivo y poco flexible. Fueron entonces desarrolladas herramientas para facilitar la reutilización de código, modularización y mantenimiento de proyectos complejos.

Exitienden el funcionamiento de CSS utilizando variables, operadores, funciones, interpoladores y mixins para facilitar el desarrollo del diseño de páginas y aplicaciones web.

Este código se procesa para producir un CSS resultante, pero permite mantenerlo de manera sencilla.

Los más conocidos son
- SASS [4]
- LESS [5]
- Stylus [6]

**Variables**

Es posible definir variables, que a lo largo del estilo son utilizadas varias veces. Permite modificar desde un único punto de edición, varios estilos.

**Anidado**

Una manera un poco más clara de definir estilos para los hijos de padres.

``` sass
ul {
    margin: 0;

    li {
        float: left;
    }

    a {
        color: $link-color;

        &:hover {
            color: $link-hover;
        }
    }
}
```

**Mixins** Serie de definiciones que compilan según paramentros

**Extenciones**  Serie de definiciones que pueden ser aplicadas en conjunto (Similar a uso con clases)

**Operación de colores** saturar, iluminar, transparentizar, mezclar,

**Operadores lógicos** if... else...

**Ciclos**  `for... i to n`

**Operadores matemáticos** suma, resta, multiplicación, división, redondeo, min, max

## Patrones de diseño (_Desing Patterns_)

Los patrones de diseño son soluciones optimizadas y reutilizables para los problemas de programación que encontramos todos los días. Un patrón de diseño no es una clase o una biblioteca que simplemente podemos conectar a nuestro sistema; es mucho más que eso. Es una plantilla que debe implementarse en la situación correcta. Tampoco es específico del lenguage de programación. Un buen patrón de diseño debería ser implementable en la mayoría de los lenguajes, si no en todos, según las capacidades del lenguaje. Lo más importante, cualquier patrón de diseño puede ser un arma de doble filo: si se implementa en el lugar equivocado, puede ser desastroso y crear muchos problemas. Sin embargo, implementado en el lugar correcto, en el momento adecuado, puede ser tu salvador.

Hay tres tipos básicos de patrones de diseño:

- Estructural
  - Los patrones estructurales generalmente se ocupan de las relaciones entre entidades, lo que facilita que estas entidades trabajen juntas.
- Creacional
  - Los patrones de creación proporcionan mecanismos de instanciación, lo que facilita la creación de objetos de una manera que se adapte a la situación.
- De Comportamiento
  - Los patrones de comportamiento se utilizan en las comunicaciones entre las entidades y hacen que sea más fácil y más flexible que estas entidades se comuniquen.

Los patrones de diseño son, en principio, soluciones bien pensadas para problemas de programación. Muchos programadores han encontrado estos problemas antes, y han usado estas 'soluciones' para remediarlos. Si encuentra estos problemas, ¿por qué volver a crear una solución cuando puede usar una respuesta ya probada?

### Bibliografía

- [1] Diseño Responsivo Wikipedia - https://es.wikipedia.org/wiki/Dise%C3%B1o_web_adaptable
- [2] Media Queries Mozilla - (https://developer.mozilla.org/es/docs/CSS/Media_queries)
- [3] Repositorio de Bootstrap - https://github.com/twbs/bootstrap
- [4] Saas - https://sass-lang.com/
- [5] Less - http://lesscss.org/
- [6] Stylus - http://stylus-lang.com/

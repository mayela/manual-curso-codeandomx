# 8. Elementos de HTML y CSS

HTML y CSS son las bases para construir una pagina web estatica. Las versiones
mas recientes son HTML5 y CSS3. 

## 8.1 ¿Qué es HTML?

HTML significa Lenguaje de marcado de hipertexto, es un lenguaje de marcado para
generar páginas web estáticas.

## 8.2 ¿Qué es CSS?

Es un lenguaje utilizado para describir el aspecto y el formato que tendrá un
sitio web.

## 8.3 Sintaxis de HTML y CSS

La sintaxis de HTML se basa en etiquetas:

![](https://mdn.mozillademos.org/files/14550/Anatomia-de-un-elemento-HTML.png)

Mientras que la de CSS en propiedades y reglas:

![](https://4.bp.blogspot.com/-x0ez6-DFmXM/WKnQU7xNHcI/AAAAAAAADfE/ITXQn1eTTeICzIhhZtrV5Yf2n06kAW5kQCLcB/w1200-h630-p-k-no-nu/propiedades-css-hojas-de-estilo.jpg)

## 8.4 Header

El elemento de HTML Header (<header>) representa un grupo de ayudas
introductorias o de navegación. Puede contener algunos elementos de encabezado,
pero también otros elementos como un logo, una sección que aglutine secciones
de encabezados, una formulario de búsqueda o cosas parecidas.

```
<header>
<!-- contenido -->
</header>
```

## 8.5 Nav

Crea un menú de navegación.

```
<nav>

  <ul>

    <li><a href="DireccionPagina"> Item de Navegación 1 </li>

    <li><a href="DireccionPagina"> Item de Navegación 2 </li>

    <li><a href="DireccionPagina"> Item de Navegación Etc </li>

  </ul>

</nav>
```

## 8.6 Section

El elemento de HTML section (<section>) representa una sección genérica de un
documento. Sirve para determinar qué contenido corresponde a qué parte de un
esquema. Piensa en el esquema como en el índice de contenido de un libro; un
tema común y subsecciones relacionadas.

```
<section>
  <h1>Encabezado</h1>
  <p>Un montón de contenido impresionante.</p>
</section>
```

## 8.7 Article

El Elemento article de HTML (<article>) representa una composición
auto-contenida en un documento, página, una aplicación o en el sitio, que se
destina a distribuir de forma independiente o reutilizable.

```
 <article>
  <h1>Google Chrome</h1>
  <p>Google Chrome es un navegador web lanzado en 2008.</p>
</article>
```

## 8.8 Aside

El Elemento HTML Aside (<aside>) representa una sección de una página que consiste en contenido que está tangencialmente relacionado con el contenido que le rodea, que podría ser considerado independiente de ese contenido.

```
 <p>Mi familia y yo visitamos Chapultepec el fin de semana.</p>

<aside>
  <h4>Casa del Lago</h4>
  <p>La Casa del Lago es un centro cultural ubicado dentro del Bosque de Chapultepec.</p>
</aside>
```

## 8.9 Footer

El Elemento HTML Footer (<footer>) representa un pie de página para el
contenido de sección más cercano o el elemento  raíz de sección.

```
 <footer>
  <p>Escrito por: Alan Turing</p>
  <p>Contato: <a href="mailto:alan@turing.com">
  alan@turing.com</a>.</p>
</footer>
```

## 8.10 Elementos, identificadores y clases en CSS

Como vimos al inicio de este capítulo existe una forma básica de definir reglas
de CSS

![](https://developer.mozilla.org/@api/deki/files/6167/=css_syntax_-_ruleset.png)

Imaginemos que tenemos lo siguiente

```
<p class="centro">Esta etiqueta hace uso de una clase</p>
<p id="unico">Los estilos se aplicarán solo a este </p>
```

```
.centro {
    text-align: center;
    color: red;
}

#unico {
    color: blue;
}
```

En el ejemplo anterior tenemos dos etiquetas p una tiene el atributo class, por
el cual podemos aplicarle estilos definiendo una regla, si llegaramos a añadir
más elementos y deseamos que tengan los mismo estilos solo le añadimos el
atributo class y listo.
Por otra parte la etiqueta p restante tiene el atributo id que nos permite
generar estilos solo para esa etiqueta.

## 8.11 Propiedades CSS

#### font-family:

Define la familia tipográfica. Es conveniente poner una lista de dos o tres
tipografías separadas por coma, porque si el usuario no tiene instalada la
tipografía que nosostros elegimos, el navegador opta por mostrar la siguiente
que debería ser una similar, si tampoco la tiene instalada, mostrará la
tipografía por defecto.


#### font-size:

Define el tamaño de la fuente y el valor se puede escribir en pixels o en ems.
En este momento se recomienda usar ems. Los dos son valores relativos, el pixel
es un valor relativo a la resolución de la pantalla, pero el em es relativo al
tamaño de la fuente definida por el usuario. Si el usuario no cambió la
configuración, el valor por defecto de los textos en todos los navegadores es
de 16px. Entonces 1em = 16px.

#### color:

Define el color de la tipografía. Los colores se pueden escribir de 3 formas
distinas: con sistema hexadecimal, por ejemplo: #FF0000 (es rojo). Con los
nombres de los colores (más limitado) por ejemplo: black, red, green. O usando
RGB, esta paleta permite agregar el canal alfa para hacer transparencias.

##### width:

Define el ancho de un elemento, el valor se puede escribir en pixels, ems o
porcentaje.

#### max-width o min-width:

Definen el ancho máximo o mínimo de un elemento. Muy importante en sitios
adaptables

#### height:

Define el alto de un elemento, el valor se puede escribir en pixels, ems o
porcentaje.

#### max-height o min-height:

Definen el alto máximo o mínimo de un elemento. Muy importante en sitios
adaptables

#### padding:

Es la distancia desde el borde de un elemento hasta su contenido.

#### margin:

Es la distancia entre un elemento y otro (desde el borde de un elemento
hacia afuera)

#### border:

Define el borde de un elemento, su color, su estilo y grosor.
#### background:

Define los fondos de un objeto. El fondo puede ser una imagen o un color. El
color puede ser pleno o degradado. La imagen se puede repetir formando una trama
(es lo que ocurre por defecto) o se puede especificar que no repita y que se
coloque en determinada posición.

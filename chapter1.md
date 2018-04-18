# 1. Acerca de la programación

Al proceso de ir de un planteamiento teórico de un problema a un programa
ejecutable en una computadora se le llama; programación. En esta unidad
ahondaremos en los conceptos necesarios para desarrollar la lógica de
programación, familiarizarse con los conceptos de lenguajes de programación,
algoritmos y estructuras de datos.

## i. ¿Qué es un programa?

Es un conjunto de órdenes escritas en un lenguaje de programación y que deben
ser realizadas por una computadora.



```
fn main () {
    print!("¡Hola Mundo!");
}
```

_Ejemplo 1.1 ¡Hola Mundo! escrito es Rust._

## ii. Lenguajes de programación

 Es un lenguaje \(formal\) que especifica un conjunto de instrucciones para
 obtener un resultado.

### ii.i Compilación vs Interpretación

El proceso de _traducir_ un programa a lenguaje de máquina tiene dos enfoques;
uno es la compilación donde el es tomado el código fuente y _traducido_ es su
totalidad. En cambio, la interpretación es el proceso de _traducir_, al momento,
 línea por línea de un programa.

![](https://ruslanspivak.com/lsbasi-part1/lsbasi_part1_compiler_interpreter.png)

### ii.ii Niveles de lenguajes de programación

#### Lenguajes de bajo nivel

Son lenguajes de programación que proveen una baja abstracción o no tienen
ninguna con respecto al conjunto de instrucciones de una computadora.

```
section	.text
   global _start     ;debe ser decladaro para el ligador (ld)

_start:	            ;le dice al ligador el punto de entrada
   mov	edx,len     ;longitud del mensaje
   mov	ecx,msg     ;mensaje a escribir
   mov	ebx,1       ;descriptor de archivo (stdout)
   mov	eax,4       ;número de la llamada al sistema (sys_write)
   int	0x80        ;llamada al núcleo

   mov	eax,1       ;número de llamada al sistema (sys_exit)
   int	0x80        ;llamada al núcleo

section	.data
msg db 'Hola mundo!', 0xa  ;string to be printed
len equ $ - msg     ;longitude del mensaje
```
_Ejemplo 1.2 Hola mundo escrito en lenguaje ensamblador_

#### Lenguajes de alto nivel

Son lenguajes que proveen una alta abstracción sobre el lenguaje de
máquina. En comparación con los lenguajes de programación de bajo nivel estos
pueden usar _lenguaje natural_ lo que lo hace más fácil de usar.

```
print("¡Hola mundo!")
```
_Ejemplo 1.3 ¡Hola mundo! escrito en Python._


## iii Estructuras de datos y algoritmos

Una estructura de datos es una forma particular de organizar datos en una
computadora. Las estructuras de datos son un medio para manejar datos de manera
eficiente para usos tales como grandes bases de datos y servicios de indexación
de Internet. Por lo general, las estructuras de datos eficientes son clave para
diseñar algoritmos eficientes.

### iii.i Algoritmos

Es un conjunto de instrucciones bien definidas, ordenadas y finitas que permiten
llevar a cabo una actividad mediante pasos sucesivos que no generen dudas a
quien deba realizar dicha actividad.

[Actividad algoritmo](https://code2flow.com/app)
[Vídeo programación](https://youtu.be/pKBw98uHOyk)

### iii.ii Arrays

Es una estructura de datos que consiste en una colección de elementos y donde
la ubicación de cada elemento es manejada por un índice.

![](https://darkbyteblog.files.wordpress.com/2011/03/arrayscheme.jpg)

_Ejemplo de un arreglo._

### iii.iii Linked lists

Consiste en una secuencia de nodos, en los que se guardan los campos de datos
arbitrarios y una o dos referencias al nodo anterior o al nodo posterior

![](https://users.dcc.uchile.cl/~bebustos/apuntes/cc30a/Estructuras/lista.gif)

_Ejemplo de una lista ligada simple._

![](https://users.dcc.uchile.cl/~bebustos/apuntes/cc30a/Estructuras/listaDobleEnlace.gif)

_Ejemplo lista doblemente ligada._

### iii.iv Stacks

Es una estructura de datos que permite almacenar y recuperar datos, el modo de
acceso a sus elementos es de tipo *LIFO*(El último en entrar es el primero en
salir). Cuenta con dos operaciones básicas _push_ que coloca un elemento al
final y _pop_ que saca el último elemento de la pila.

![](https://programadorplus.com/wp-content/uploads/2017/10/diagrama-pila.png)

_Ejemplo de una pila._

### iii.v Queues

Es una secuencia de datos en la que la operación de inserción se realiza por un
extremo y la operación de extracción se realiza por el otro(FIFO).

![](https://upload.wikimedia.org/wikipedia/commons/thumb/b/bb/Cola.svg/320px-Cola.svg.png)

_Ejemplo de una cola._

### iii.vi Trees

Es una estructura de datos ampliamente usada que imita la estructura ejrárquica
de un árbol, con una raíz, ramas y nodos terminales.

![](https://upload.wikimedia.org/wikipedia/commons/thumb/f/f7/Binary_tree.svg/300px-Binary_tree.svg.png)

_Ejemplo de un árbol._

### iii.vii Graphs

Consiste en un conjunto de nodos (también llamados vértices) y un conjunto de
arcos (aristas) que establecen relaciones entre los nodos.

![](https://upload.wikimedia.org/wikipedia/commons/thumb/5/5b/6n-graf.svg/333px-6n-graf.svg.png)

_Ejemplo de un grafo._

## iv Problemas comunes

Los problemas más comunes que se pueden presentar durante el aprendizaje del
desarrollo son mayormente en el aspecto de desarrollar la lógica para la
programación, para dado un problema plantear los pasos a seguir para resolverlo.


## v Soluciones

Leer contínuamente sobre como resolver problemas, como es diseñado un algoritmo
pueden ayudar a ir desarrollando la lógica.

### v.i Utilidad y usabilidad

La utilidad indica que el sistema le es útil al usuario para hacer algo
concreto. Un sistema es útil, en este sentido, cuando le permite al usuario
cumplir con sus objetivos. La usabilidad, por su parte, se refiere a la
facilidad con que las personas pueden utilizar una herramienta particular o
cualquier otro objeto fabricado por humanos con el fin de alcanzar un objetivo
concreto.

### v.ii Mantenibilidad

La mantenibilidad es la propiedad de un sistema que representa la cantidad de
esfuerzo requerida para conservar su funcionamiento normal o para restituirlo
una vez se ha presentado un evento de falla. Se dirá que un sistema es
_altamente mantenible_ cuando el esfuerzo asociado a la restitución sea bajo.

### v.iii Hacer la programación fácil para ti y fácil para los demás



## vi. ¿Cómo se convierte unx en programador(a)?

Existen distintos caminos que dependen de la personalidad y situación de vida de cada quien.

- Hay quienes al usar una computadora se encontraron con un error y buscando en internet la respuesta se encontraron con conceptos que no conocían, los cuales investigaron con una curiosidad insaciable fueron primero arrojando islas de conceptos a un mar de confusión, para después construir un entramado de puentes, para despues fundar ciudades de cóCódigo
- Hay quienes, enamorados de los videojuegos y de sus entramados laberintos, desarrollaron una capacidad de resolver problemas complejos, que cuando se encontraron con líneas de código, descubrieron que ya hacían `if.. else..` y `for` en sus mentes y con botones, teclas, palancas y mouses.
- Hay quienes deciden ir a la universidad y salir certificados después de `n` años
- Hay quienes sabiendo diseño gráfico, quisieron plasmar sus ideas en varias pantallas y empezaron por html y css, para brincar después a js.

# Bibliografía

· [Estructuras de datos](https://users.dcc.uchile.cl/~bebustos/apuntes/cc30a/Estructuras/)

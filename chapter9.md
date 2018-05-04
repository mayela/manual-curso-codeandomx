# 9. Implementación de Javascript

## 9.1 ¿Qué es Javascript?

JavaScript (abreviado comúnmente JS) es un lenguaje de programación
interpretado, dialecto del estándar ECMAScript. Se define como orientado a
objetos, imperativo, débilmente tipado y dinámico.

Se utiliza principalmente en su forma del lado del cliente (client-side),
implementado como parte de un navegador web permitiendo mejoras en la interfaz
de usuario y páginas web dinámicas4​ aunque existe una forma de JavaScript del
lado del servidor.

### 9.1.1 La consola de Javascript

Dentro de cualquier navegador web tenemos acceso a un interprete de Javascript,
este nos permite ejecutar declaraciones del lenguaje.

### 9.1.2 Primitivas y tipos de datos

##### Boolean

Boolean representa una entidad lógica y puede tener dos valores: true, y false.

##### Null

El tipo Null tiene exactamente un valor: null

##### Undefined

Una variable a la cual no se le haya asignado valor tiene entonces el valor
_undefined_.

##### Number

De acuerdo al standard ECMAScript, sólo existe un tipo numérico: el valor de
doble precisión de 64-bits IEEE 754 (un número entre -(253 -1) y 253 -1). No
existe un tipo específico para los números enteros.

##### String

El tipo String de Javascript es usado para representar datos textuales o
cadenas de caracteres. Cada elemento ocupa una posición en el String. El primer
elemento está en el índice 0, el próximo está en el índice 1, y así
sucesivamente. La longitud de un String es el número de elementos en ella.

#### Symbol

El Symbol es un nuevo tipo en JavaScript introducido en la versión ECMAScript
Edition 6. Un Symbol es un valor primitivo único e inmutable y puede ser usado
como la clave de una propiedad de un Object.

#### Objetos

En JavaScript los objetos pueden ser vistos como una colección de propiedades.
Con la sintáxis literal de objetos, un limitado grupo de propiedades son
inicializadas; luego pueden ser agregadas o eliminadas otras propiedades. Los
valores de las propiedades pueden ser de cualquier tipo, incluyendo otros
objetos lo cual permite construir estructuras de datos complejas.

##### Objetos normales y funciones

Un objeto en JavaScript es una lista de pares de llaves y valores, las llaves
son una cadena de carácteres (string) o en dado caso _Symbol_ y los valores
pueden ser cualquier tipo de dato.

##### Date

Cuando representas fechas, la mejor elección es usar el objeto Date incorporado
en JavaScript.

##### Arrays y Arrays tipados

Arrays son objetos regulares en los cuales hay una particular relacion entre la
propiedad  clave-entera y la propiedad _length_.

Arrays Tipados son nuevos en JavaScript con la edicion 6 de ECMAScript y
presenta a un array como una vista subyacente de un buffer de datos binario.

##### Colecciones con llaves

Estas estrucutras de datos toman las referencias a objetos como llaves, son
introducidas en ECMAScript Edition 6. _Set_ y _WeakSet_ representan un conjunto
de objetos mientras que _Map_ y _WeakMap_ asocian un valor a un objeto. La
direferencia entre _Map_ y _WeakMap_ es que en el primero las llaves pueden ser


## 9.8 Hoisting

Hoisting es un término que no encontrará utilizado en ninguna especificación
previa a ECMAScript® 2015 Language Specification. El concepto de Hoisting fue
pensado como una manera general de referirse a cómo funcionan los contextos de
ejecución en JavaScript (específicamente las fases de creación y ejecución).
Asimismo, hoisting puede llevar a malos entendidos. Por ejemplo, hoisting puede
dar a entender que las declaraciones de variables y funciones son físicamente
movidas al comienzo del código, pero esto no es lo que ocurre en realidad. Lo
que sucede es que las declaraciones de variables y funciones son asignadas en
memoria durante la fase de compilación, pero quedan exactamente en dónde la ha
escrito en el código.

## 9.9 Operadores de comparación

Un operador de comparación compara sus operandos y devuelve un valor lógico en
función de si la comparación es verdadera (true) o falsa (false). Los
operadores pueden ser númericos, de cadena de caracteres (Strings), lógicos o
de objetos.

| Operador | Descripción |
| --- | --- |
| == | Devuelve true si ambos operandos son iguales|
| != | Devuelve true si ambos operandos no son iguales|
| === | Devuelve true si los operandos son iguales y tienen el mismo tipo|
| !== | Devuelve true  si los operandos no son iguales y no son del mismo tipo|
| > | Devuelve true si el operando de la izquierda es mayor que el de la derecha|
| >= | Devuelve true si el operando de la izquierda es mayor o igual que el operando de la derecha|
| < | Devuelve true si el operando de la izquierda es menor que el de la derecha|
| <= | Devuelve true si el operando de la izquierda es menor o igual que el operando de la derecha|

## 9.10 Operadores lógicos

Los operadores lógicos son comúnmente utilizados con valores booleanos; estos
operadores devuelven un valor booleano. Sin embargo, los operadores _&&_ y _||_
realmente devuelven el valor de uno de los operandos, asi que si estos
operadores son usados con valores no booleanos, podrían devolveran un valor no
booleano.

| Operador | Descripción|
| --- | --- |
| && | Devuelve expr1 si puede ser convertido a false de lo contrario devuelve expr2|
| || | Devuelve expr1 si puede ser convertido a true de lo contrario devuelve expr2|
| ! | Devuelve false si su operando puede ser convertido a true, en caso contrario, devuelve true|

## 9.11 Comparación de Igualdad: abstracta vs estricta

Para hacer comparación de "igualdad" entre una variable y un valor, o entren variable y variable, existen dos posibilidades. Toma en cuenta si son valores primitivos, objetos o valores de refrencia

- **Abstracta**: Se utiliza doble símbolo de igual `==` para comparación que no toma en cuenta el tipo de la variable. Ej:
``` js
console.log(3 == '3') // true
console.log(true == '1'); // true
console.log(undefined == null); // true
```
- **Estricta**: Se utiliza triple simbolo de igual`===` para comparación que tomando  en cuenta el tipo de la variable. Ej:
``` js
console.log(3 === '3') // false
console.log(true === '1'); // false
console.log(undefined === null); // false
```

## 9.12 _null_ y _undefined_

**Undefined** simboliza que se le da a las variables que han sido declaradas, pero a la que no se le ha asignado ningún valor. Se utiliza también cuando se intenta acceder al valor de un objecto,al índice de un arreglo que no existe o cuando una función no regresa un valor:
``` js
let x;
console.log(x) // undefined

let y = {a: '1', b: 3}
console.log(y.c); // undefined
console.log(y['d']); // undefined

let z = [1,2,3]

console.log(z[4]); // undefined

let miFuncion(foo, bar) {
  // cualquier cosa pero sin usar 'return'
}

console.log(miFuncion()) // undefined
```

**null** es una palabra clave en Javascript que significa ausencia de valor y es de tipo objeto (`typeof null` => object). Se utiliza para quitarle el valor a una variable, y se hace asignandole el valor `null`

## 9.13 Operadores ternarios

Los operadores terniarios es una manera corta de escribir un `if... else...`, reciben 3 operandos:
```
condicion ? expr1 : expr2
```
la condición debe de evaluar y responder `true` o `false`, ejecutando la `expr1` después de `?` si es verdadero, o la `expr2` después de `:` si es falso.

Es utilizada para asignar entre dos distintas opciones:
``` js
var edad = 26;
var puedeTomarAlcohol = (edad > 21) ? "True, más de 18" : "False, menos de 18";
console.log(puedeTomarAlcohol); // True, más de 18
```
## 9.14 Declaración if else

Se utiliza esta declaración para realizar, o no, operaciones según una condición, cuando sólo es `if`, o entre una serie de operaciones y otras por agregando `else`. Esta es la sintaxis:

```
if (<condición binaria>) {
  <expr1> // serie de operaciones
}
[ else {
  <expr2> // serie de operaciones
}]
```

Si la
si la serie de operaciones pudiera ponerse en una línea, entonces puede no utilizarse los corchetes `{ }`

## 9.15 Declaración switch

La sentencia switch evalúa una expresión, comparando la expresión con un conjunto de  valores predefinidos, y ejecuta comandos según el caso.

``` js
switch (expresion) {
  case valor1:
    //Sentencias ejecutadas cuando el resultado de expresion coincide con valor1
    [break;]
  case valor2:
    //Sentencias ejecutadas cuando el resultado de expresion coincide con valor2
    [break;]
  ...
  case valorN:
    //Sentencias ejecutadas cuando el resultado de expresion coincide con valorN
    [break;]
  default:
    //Sentencias_def ejecutadas cuando no ocurre una coincidencia con los anteriores casos
    [break;]
}
```

el caso `default` se ejecutara si la expresión no coincide con ninguno de los valores predeterminados.

## 9.16 Arrays

Array es un objeto global que es usado en la construcción de arreglos, que son objetos tipo lista de alto nivel.

Para definir un Array es necesario utilizar los corchetes cuadrados `[ ]`, entre los cuales se escribirán los elementos divididos por comas `,`.

``` js
var frutas = ['Manzana', 'Banana'];
```

Para acceder a los arreglos se usa la variable concatenado con corchetes cuadrados y un número que define el índice del valor que se desea consultar, empezando desde el `0`. Cada arreglo tiene una propiedad llamada `length`, que representa su longitud o número de elementos que contiene.


``` js
var primero = frutas[0];
// Manzana

var ultimo = frutas[frutas.length - 1];
// Banana
```

## 9.17 Métodos de los Arrays

### forEach

Recorrera los elementos del arreglo, uno por uno, del primero al último y recibe como operandos una función con 3 valores: elemento, índice y el arreglo mismo

``` js
frutas.forEach(function (elemento, indice, array) {
    console.log(elemento, indice);
});
// Manzana 0
// Banana 1
```

### push

Agrega un elemento al **final** del arreglos. Y por lo tanto modifica su longitud. (Modifica el arreglo original)
``` js
var masFrutas = frutas.push('Naranja');
console.log(masFrutas)// ["Manzana", "Banana", "Naranja"];
```

### pop

Elimina el **último** elemento del arreglo y lo arroja, permitiendo así asignarlo a otra variable o utilizarlo. (Modifica el arreglo original)
``` js
var ultimo = frutas.pop(); // elimina Naranja del final
console.log(frutas) // ["Manzana", "Banana"];
console.log(ultimo) // Naranja
```

### shift

Elimina el **primer** elemento del arreglo y lo arroja (similar a pop), permitiendo así asignarlo a otra variable o utilizarlo. (Modifica el arreglo original)
``` js
var primero = frutas.shift(); // elimina Manzana del inicio
console.log(frutas) // ["Banana"];
```

### unshift

Agrega un elemento al **inicio** del arreglos. Y por lo tanto modifica su longitud. (Modifica el arreglo original)
``` js
var masFrutas = frutas.unshift('Uva');
console.log(masFrutas)// ["Uva", "Banana"];
```

### indexOf

Busca un elemento en el arreglo y de encontrarlo, regresa su índice, de lo contrario regresa `-1`

### splice

Elimina una serie de elementos dentro del arreglo, recibe dos operandos: `posicion` y `número de arreglos a eliminar`, además de arrojar los elementos eliminados como resultado de la operación.

``` js
var vegetales = ['Repollo', 'Nabo', 'Rábano', 'Zanahoria'];

var pos = 1, n = 2;

var elementosEliminados = vegetales.splice(pos, n);
// así es como se eliminan elementos, n define la cantidad de elementos a eliminar,
// de esa posicion(pos) en adelante hasta el final del array.

console.log(vegetales);
// ["Repollo", "Zanahoria"] (el array original ha cambiado)

console.log(elementosEliminados);
// ["Nabo", "Rábano"]
```

### slice

Se utiliza para hacer una copia de una porción de un arreglo.
``` js
var frutas = ["Fresa", "Mango", "Manzana", "Pera", "Melón"]
var copiaCompleta = frutas.slice(); // sin operandos crear una copia completa
// ["Fresa", "Mango"];

var delIndiceDosEnAdelante = frutas.slice(2) // A partir del elemento en el indice 2
// ["Manzana", "Pera", "Melon"]

var delUnoAlTres = frutas.slice(1,4) // Tomara los elementos de los índices 1,2 y 3
// ["Mango", "Manzana", "Pera"]

var conNegativos = frutas.slice(-2) // Los últimos dos elementosEliminados
// ["Pera", "Melón"]
```

## 9.18 Parse

El método JSON.parse() analiza una cadena de texto como JSON, transformando
opcionalmente  el valor producido por el análisis.

```
JSON.parse('{}');              // {}
JSON.parse('true');            // true
JSON.parse('"foo"');           // "foo"
JSON.parse('[1, 5, "false"]'); // [1, 5, "false"]
JSON.parse('null');            // null
```

## 9.19 For loops

### For

Un bucle for se repite hasta que la condición especificada se evalúa como
false. El bucle for en JavaScript es similar al de Java y C.

```
function howMany(selectObject) {
  var numberSelected = 0;
  for (var i = 0; i < selectObject.options.length; i++) {
    if (selectObject.options[i].selected) {
      numberSelected++;
    }
  }
  return numberSelected;
}
```

### do...while

La sentencia do...while se repite hasta que una condición especificada se
evalúa a false.

```
do {
  i += 1;
  console.log(i);
} while (i < 5);
```

### while

Una sentencia while ejecuta sus sentencias mientras la condición sea evaluada
como verdadera.

```
n = 0;
x = 0;
while (n < 3) {
  n++;
  x += n;
}
```

### for...in

La sentencia for...in itera una variable especificada sobre todas las
propiedades enumerables de un objeto.

```
function volcar_propiedades(obj, obj_nombre) {
  var resultado = "";
  for (var i in obj) {
    resultado += obj_nombre + "." + i + " = " + obj[i] + "<br>";
  }
  resultado += "<hr>";
  return resultado;
}
```

### for...of

La sentencia for...of crea un bucle iterando sobre objetos iterables
(incluyendo Array, Map, Set, argumentos objetos etc), invocando una iteración
personalizada conectando con sentencias para ser ejecutadas por el valor de
cada propiedad distinta.

```
let arr = [3, 5, 7];
arr.foo = "hello";

for (let i in arr) {
   console.log(i); // logs "0", "1", "2", "foo"
}
```

## 9.22 Objetcs

El constructor Object crea un contenedor de objeto para el valor dado.
Si el valor es null o undefined, creará y devolverá un objeto vacío, de
cualquier otro modo, este retornará un objeto del tipo correspondiente al
valor dado. Si el valor es un objeto, devolverá el valor.

```
var o = new Object()
```

## 9.23 this

La función de la palabra clave this se comporta un poco diferente en Javascript
en comparación con otros lenguajes. Además tiene algunas diferencias entre el
modo estricto y el modo no estricto.

En general, el valor de this está determinado por cómo se llama a la función.
No puede ser establecida por una asignación en tiempo de ejecución, y esto
puede ser diferente cada vez que la función es llamada.

En el contexto de ejecución global (fuera de cualquier función), this se
refiere al objeto global, ya sea en modo estricto o no.

```
console.log(this.document === document); // true
```

Dentro de una función, el valor de this depende de cómo la función es llamada.

```
function f1(){
  return this;
}

f1() === window; // objeto global
```

En este caso, el valor de this no está establecido por la llamada. Dado que el
código no está en modo estricto, el valor de this debe ser siempre un objeto
por lo que por defecto es el objeto global.

```
function f2(){
  "use strict"; // consultar modo estricto
  return this;
}

f2() === undefined;
```

### 9.24 Closure

Un closure es la combinación de una función y el ámbito léxico en el que se
declaró dicha función. Es decir los closures son funciones que manejan
variables independientes. En otras palabras, la función definida en el closure
"recuerda" el ámbito en el que se ha creado.

```
function inicia() {
  var nombre = "Mozilla"; // 'nombre' es una variable local creada por la función 'inicia'
  function muestraNombre() { // 'muestraNombre' es una función interna (un closure)
    alert(nombre); // dentro de esta función usamos una variable declarada en la función padre
  }
  muestraNombre();
}
inicia();
```

La función inicia()  crea una variable local llamada nombre, a continuación,
define una función denominada muestraNombre(). muestraNombre() es una función
interna (un closure) definida dentro de inicia(), y sólo está disponible en el
cuerpo de esa función. muestraNombre() no tiene ninguna variable propia, lo que
hace es reutilizar la variable nombre declarada en la función externa.

## 9.25 Promises

Una Promesa es un proxy para un valor no necesariamente conocido en el momento
que es creada la promesa. Permite asociar manejadores que actuarán
asincrónicamente sobre un eventual valor en caso de éxito, o la razón de falla
en caso de una falla. Esto permite que métodos asíncronos devuelvan valores
como si fueran síncronos: en vez de inmediatamente retornar el valor final,
el método asíncrono devuelve una promesa de suministrar el valor en algún
momento en el futuro.

Una Promesa se encuentra en uno de los siguientes estados:

  * pendiente (pending): estado inicial, no cumplida o rechazada.
  * cumplida (fulfilled): significa que la operación se completó satisfactoriamente.
  * rechazada (rejected): significa que la operación falló.

```
let miPrimeraPromise = new Promise((resolve, reject) => {
  // Llamamos a resolve(...) cuando lo que estabamos haciendo finaliza con éxito, y reject(...) cuando falla.
  // En este ejemplo, usamos setTimeout(...) para simular código asíncrono.
  // En la vida real, probablemente uses algo como XHR o una API HTML5.
  setTimeout(function(){
    resolve("¡Éxito!"); // ¡Todo salió bien!
  }, 250);
});
```

## 9.26 Desktop notiffications

La interfaz Notification de la Notifications API se usa para configurar y
mostrar notificaciones de escritorio al usuario.

```
function spawnNotification(theBody,theIcon,theTitle) {
  var options = {
      body: theBody,
      icon: theIcon
  }
  var n = new Notification(theTitle,options);
}
```

## 9.27 Introducción la programación básica con algoritmos

### Algoritmo para encontrar la distancia entre dos puntos

  1. Pido la coordenada x del punto a
  2. Pido la coordenada y del punto a
  3. Pido la coordenada x del punto b
  4. Pido la coordenada y del punto b
  5. Calculo el tamaño de la componente horizontal (cateto 1)
  6. Calculo el tamaño de la componente vertical (cateto 2)
  7. Elevo al cuadrado componentes vertical y horizontal
  8. Las sumo
  9. Aplico la raíz cuadrada
  10. Muestro la distancia

```
var ax = prompt("Dame punto a coordenada x","");
var ay = prompt("Dame punto a coordenada y","");
var bx = prompt("Dame punto b coordenada x","");
var by = prompt("Dame punto b coordenada y","");

var comp_horizontal = (bx-ax);
var comp_vertical = (by-ay);
comp_horizontal = comp_horizontal * comp_horizontal;
comp_vertical = comp_vertical * comp_vertical;
var distancia = Math.sqrt(comp_horizontal + comp_vertical);

alert(distancia);
```

## 9.28 Programación orientada a objetos

La programación orientada a objetos es un paradigma de programación que utiliza
la abstracción para crear modelos basados ​​en el mundo real. Utiliza diversas
técnicas de paradigmas previamente establecidas, incluyendo la modularidad,
polimorfismo y encapsulamiento.

La programación orientada a objetos puede considerarse como el diseño de
software a través de un conjunto de objetos que cooperan, a diferencia de un
punto de vista tradicional en el que un programa puede considerarse como un
conjunto de funciones, o simplemente como una lista de instrucciones para la
computadora. En la programación orientada a objetos, cada objeto es capaz de
recibir mensajes, procesar datos y enviar mensajes a otros objetos. Cada objeto
puede verse como una pequeña máquina independiente con un papel o
responsabilidad definida.

### Clase

Define las características del Objeto.

```
function Persona() {
}
```

### Objeto

Una instancia de una Clase.

```
var persona1 = new Persona();
var persona2 = new Persona();
```
### Propiedad

Una característica del Objeto, como el color.

```
function Persona(primerNombre) {
  this.primerNombre = primerNombre; // propiedad
}
```

### Método

Una capacidad del Objeto, como caminar.

```
Persona.prototype.diHola = function() {
  alert ('Hola, Soy ' + this.primerNombre);
};
```

### Constructor

Es un método llamado en el momento de la creación de instancias.
### Herencia

Una Clase puede heredar características de otra clase.

```
// Definimos el constructor Persona
function Persona(primerNombre) {
  this.primerNombre = primerNombre;
}

// Definimos el constructor Estudiante
function Estudiante(primerNombre, asignatura) {
  // Llamamos al constructor padre, nos aseguramos (utilizando Function#call) que "this" se
  // ha establecido correctamente durante la llamada
  Persona.call(this, primerNombre);

  //Inicializamos las propiedades específicas de Estudiante
  this.asignatura = asignatura;
};
```

### Encapsulamiento

Una clase sólo define las características del Objeto, un método sólo define
cómo se ejecuta el Método.
### Abstracción
La conjunción de herencia compleja, métodos y propiedades que un objeto debe
ser capaz de simular en un modelo de la realidad.

### Polimorfismo

Diferentes clases podrían definir el mismo método o propiedad.

## 9.29 Estructuras de datos y algoritmos

## 9.30 Introducción a DOM y manipulación




## Recursos

- Javascript - https://www.javascript.com/
- CodeSchool JS Tutorial  - https://www.codeschool.com/courses/javascript-road-trip-part-1?utm_source=javascript&utm_medium=referral&utm_campaign=js_com
- W3 JS Tutorial - https://www.w3schools.com/Js/
- Mozilla JS - https://developer.mozilla.org/es/docs/Web/JavaScript
  - Modenrn Javascritp Tutorial - https://javascript.info/

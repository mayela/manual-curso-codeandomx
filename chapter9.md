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

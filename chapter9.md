<<<<<<< HEAD
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





=======
# 9. Implementación de Javascript
>>>>>>> 4789fc3c81705587a26ef82634bbd57ca4b2602d

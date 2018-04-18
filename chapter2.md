# 2. ¿Cómo se organiza un programa?

Por lo general un programa se organiza de forma modular, haciendo que un bloque
de código solucione un problema y lo haga bien. Esto permite al código evolucionar y escalar de mejormanera.

## 2.1. Declaración/Líneas de código
Un programa se va creando por medio de sentencias, las cuales, en su conjunto,
representan los pasos a seguir para realizar una actividad(algoritmo).

## 2.2. Tipos de datos


* Entero: valor que pertenece al conjunto de los números enteros
* Flotante: valor con punto flotante(e.g 0.5)
* Caracter: un valor alfanumérico.
* Cadena: un conjunto de valores alfanuméricos.

## 2.3. Variables

Una variable es donde guardaremos ciertos valor bajo un nombre.

```
mi_entero  = 2
mi_flotante = 3
mi_caracter = 'a'
mi_cadena = 'Hola'
```

## 2.4  Operadores

### 2.4.1 Operadores aritméticos

| Operador | Operación|
| --- | --- |
| + | Suma |
| - | Resta |
| * | Multiplicación |
| / | División |
| ^ | Exponencial |
| % | Módulo |

#### 2.4.1.1 Precedencia

1. Exponencial
2. Multiplicación, división, módulo
3. Suma, resta

### 2.4.2 Operadores de comparación

| Operador | Operación |
| --- | --- |
| > | Mayor que |
| < | Menor que |
| >= | Mayor o igual que |
| <= | Menor o igual que |
| != | Diferente |
| == | Igual |

### 2.4.3 Operadores lógicos

| Operador | Operación |
| --- | --- |
| and | y |
| or | o |
|not | no es |

## 2.5 Expresiones

Una expresión es una combinación de constantes, variables o funciones, que es
interpretada de acuerdo a las normas particulares de precedencia y asociación
para un lenguaje de programación en particular.

## 2.6 Estructuras de control

Las estructuras de control permiten modificar el flujo de ejecución de las
instrucciones de un programa y son las siguientes:

- if... else
- switch
- while
- do... while

## 2.7 Procedimientos y funciones

Los procedimientos, también conocidos como rutinas, subrutinas o funciones son
una serie de pasos en busca de minimizar el código ya que por lo general son pasos que
deben repetirse varias veces.

## 2.8 Arrays y strings

Los arrays o arreglos son una estructura de datos. Las cadenas son una secuencia
de caracteres alfanuméricos por lo general se colocan dentro de un par de
comillas dobles o simples.

## 2.9 Records

Un record o registro es una colección de campos posiblemente de distinto tipo
que típicamente son fijos y están en secuencia.

# 2.10 Input/Output

A veces requerimos de ciertos datos de entrada para ser manipulados y obtener
un resultado, a las partes iniciales y finales del flujo las llamamos entrada y
salida.

![](https://www.dwheeler.com/secure-programs/program.png)

_Ejemplo de entrada y salida de un programa_

## 2.11 Comentarios

Los comentarios sirven a manera de documentación, es decir, de explicar que es
lo que nuestro código prentende hacer y como lo hace. En los lenguajes de
programación exiten distintas formas de escribir comentarios pero las más
comúnes son:

```
#
/* */
```

## 2.12 Scope

El scope o alcance es definido para las variables y se remite a la capacidad que
tienes alguna sentencia para modificar los valores de las variables; veamos un
ejemplo:

```
#include <stdio.h>
int main(void)
{
    char x = 'm';
    printf("%c\n", x);
    {
        printf("%c\n", x);
        char x = 'b';
        printf("%c\n", x);
    }
    printf("%c\n", x);
}
```

```
m
m
b
m
```

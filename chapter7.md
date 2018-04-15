# 7. Introducción control de versiones con Git y Github

Git es una herramienta de control de versiones, nos ayuda a manejar de mejor 
manera la forma en la que nuestro código va evolucionando a través del tiempo.
Github es una plataforma que alberga repositorios manejados con el control de 
versiones de Git.
## 7.1 Configurando Git

```
$ git config --global user.name "Marie Curie"
$ git config --global user.email "marie@curie.com"
```

## 7.2  Creando nuestro primer repositorio de Git

```
$ mkdir hola-mundo
$ cd hola-mundo
$ git init
$ git status
```

Las instrucciones anteriores le dicen a Git que debe detectar cambios dentro de 
esta carpeta, pero hasta el momento no los estamos siguiendo.
Ahora crearemos un archivo al que llamaremos _README.md_

```
touch README.md
```

Con cualquier editor abriremos el archivo y escribiremos dentro de él _Hola 
mundo_.
Con la instrucción **git status** veremos que los cambios han sido detectados 
por Git.

```
En la rama master

No hay commits todavía

Archivos sin seguimiento:
  (usa "git add <archivo>..." para incluirlo a lo que se será confirmado)

	README.md

no hay nada agregado al commit pero hay archivos sin seguimiento presentes (usa "git add" para hacerles seguimiento)
```

Ahora para empezar a seguir los cambios del archivo __README.md_ debemos escribir la siguiente instrucción:

```
git add README.md
```

El resultado será:

```
En la rama master

No hay commits todavía

Cambios a ser confirmados:
  (usa "git rm --cached <archivo>..." para sacar del área de stage)

	nuevo archivo:  README.md
```

El archivo ahora está siendo _seguido_, para confirmar los cambios solo 
tendremos que escribir la siguiente instrucción:

```
git commit -m "Cambios en README.md, Hola mundo agregado"
```

Después, verificaremos el estado del repositorio con la instrucción **git 
status**

```
En la rama master
nada para hacer commit, el árbol de trabajo esta limpio
```

Para ver el historial de commits basta con ejecutar la instrucción **git log**

Cuando trabajas en un equipo de desarrollo por lo general muchos trabajan 
dentro del mismo repositorio, Git nos hace fácil el manejo de estos múltiples 
cambios mediante la creación de distintas ramas.

```
git checkout -b nuevos-cambios-readme
```

Ahora podemos hacer los cambios necesarios sin afectar el trabajo de los demás. 

Para subir los cambios a Github, la plataforma que centraliza repositorios, 
agregaremos una referencia al un repositorio remoto. Para esto creamos una 
cuenta en Githug y luego creamos un repositorio remoto

![](https://help.github.com/assets/images/help/repository/repo-create.png)

Después agregamos el repositorio remoto:

```
git remote add origin <url>
```
# Tecnologías Back-end

Capa de acceso a datos

## Servicios APIs

API (_Application Program Interface_) Es una capa intermedia entre la capa de presentación (_Front-end_) y los datos, ya sean archivos o bases de datos. Esta Api expone a la _web_ _endpoints_ para un sitema de solicitudes y respuestas (_request / response_), normalmente mediante archivos, JSON o XML, a través de HTTP Requests.

Los endpoints normalmente son accesados mediante la definición de un URI (_Unirform Resource Identifier_) o un URL (_Uniform Resource Locator_) que es una cadena de texto y que permite accesar a terceros a los servicios o recursos.

## REST (_REpresentational State Transfer_)

Es un estilo de arquitectura para servicios APIs basado en restricciones que permiten informidad y predectibilidad

- **Uniform Interface** Describe la interfaz entre cliente y servidor.
  - Basado en recursos. Cada recurso usa URIs como identificadores
  - Manipulación de recursos via representaciones. El cliente tiene suficiente información para modificar o borrar
  - Mensajess auto-descritos. Tiene información suficiente para procesar el Mensajes
  - Hypermedios como motor del estado de la aplicación.
- **Sin Estado** El estado requerido para manejar las solicitudes está en la misma solicitud.
  - En el _body_, los paramentros del _query_, o los headers
  - El cliente debe incluir en las solicitudes toda la información necesaria para procesar la información
  - El servidor no mantendra un "estado" para saber si debe o no procesar cierta solicitud
- **Cacheable** Prevenir el uso de interacciones innecesarias, permitiendo escalamiento y mejor rendimiento
- **Sistema de Capas** El cliente y el servidor deberán poderse desarrolla de manera independiente
  - El servidor podrá esclarse y balancear las cargas sin que el cliente necesite de información extra

## [NodeJS](nodejs.org)

![](https://images.duckduckgo.com/iu/?u=https%3A%2F%2Fdab1nmslvvntp.cloudfront.net%2Fwp-content%2Fuploads%2F2015%2F07%2F1436439824nodejs-logo.png&f=1)

JavaScript para servidor. Dada la popularidad que obtuvo Javascript como lengauge oficial del desarrollo web, se creo este lenguaje, con la misma sintaxis, pero que corre en el servidor y que tiene la capacidade de accesar a bases de datos, archivos y consumir recursos del servidor.

Se puede descargar [aquí](https://nodejs.org/es/download/)
Aunque por mantenibilidad y poder tener múltiples versiones instaladas en la misma máquina, recomiendo este paquete [NVM](https://github.com/creationix/nvm#installation) (_Node Version Manager_)

### Comandos

    `$ node abre` terminal de Node
        `Ctrl+C` * 2 para salir o `.exit`
    `$ node <jsfile.js>`
    `$ which node` -> la ruta a los binarios de node: /local/bin/node
    `$ node` --version saber la versión de node en mi máquina

Los paquetes de node se instalan via un controlador de paquetes llamada **npm**

### [npm](https://npmjs.com) (_Node Package Manager_)

Parelelamente se desarrolla este ambiente que permite compartir, reutilizar y actualizar proyectos o librerías de Node.

**Objetivos**

  - Capacidad de replicar el ambiete de paquetes o modulos cuando se va desarrollar y se va a deployar a producción
    - configuration desarrollo y producción
  - automatización de procesos
  - tests (_Test Driven Develpment_)

#### Comandos

- `$npm --version` saber la versión de npm en mi máquina
- `$ npm init` crea el archivo de configuración de app de Node `package.json`
- `$ npm (install / i) (--save / -s) <package-name>@v#.#.#` con save, se guardara en nuestro archivo de configuración
- `$ npm install` consulta los packetes en la campo de package-json `dependencies`
- `$ npm update <package-name>` busca y remplaza la versión del packete por la versión más actualizada


Esta paquetería instala y guarda la configuración de los packetes:
  - `package.json` es el archivo donde se irá describiendo los packetes

## [ExpressJS](https://expressjs.com/)

Uno de los packetes más utilizados de Node, permite:

- Intermediario para HTTP Requests
  - Request
  - Response
- Ruteador for HTTP METHODS (GET POST PUT DELETE) and URLS
- Plantillas de HTML
  - Jade
  - [Handlebars](https://handlebarsjs.com/)
  - Pug

### Instalación

`$ npm install --save express`

Plugins más usados

- body-parser --> parseador para datos de formularios
- cookie-parse --> decorador de las solicitudes en `req.cookies`
- multer --> Para MultipartFormData (documentos, fotos)

### Routeador

Definición de _endpoints_ URIs

``` js
app.get('<url>', callback(req, res))
```

  `app.post()`   `app.method()`   `app.use()`

Las rutas permiten llevar parametros
### [HTTP Methonds](https://developer.mozilla.org/en-US/docs/Web/HTTP/Methods)

- #### GET
``` js
  app.get('/', function (req, res) {
    res.send('hello world')
    })
```
  - URL parameters
    - to define parameters, in first argument use `:` before the name of the param
  ``` js
    app.get('user/:id', function (req, res) {
      let id = req.params.id
      res.send('id: '  + id)
      })
  ```
  - you can access params using: `req.params`
- #### POST
  - payload
    - Info to add
    - types
      - When coming from <form> `application/x-www-form-urlencoded`
      - JSON `application/application/json`
      - Files `multipart/form-data`
``` js
  app.post('/user', (req, res) => {
    console.log(req.payload)
    res.send('Post complete ' + req.params.id)
  })
```
- #### PUT

``` js
  app.get('user/:id', function (req, res) {
    let id = res.params.id
    res.send('id: '  + id)
    })
```
- #### DELETE

### REST API


### [Express Generator](https://expressjs.com/en/starter/generator.html)

- install `$ npm i -g express-generator`
- use `$ express <option> <project-name>`

### [Nodemon](https://nodemon.io/)
Features
- Autorefresh on save
- Debug in chrome

- Install `$ npm i -g nodemon`
- Use

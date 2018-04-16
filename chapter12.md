## Angular

_Framework_ de Javascript, open source, mantenida principalmente por el equipo de Google, y enfocada en realizar lo que llaman aplicaciones-de-una-sola-página (̣_single-page applications_), que son aquellas que pretenden simular las aplicaciones nativas de escritorio. Funcionan modificando dinámicamente el contenido de una única página, con una constante comunicación con el servidor para una mejor experiencia de usuario.

 Utiliza una metodología de **MVC**: Modelo-Vista-Controlador (__Model-View-Controller__), a difencia las estrategias de desarrollo de Aplicaciones Web, en donde los los controladores, los modelos y el rendereo de las vistas se realizaba en el servidor, Angular lo hace del lado del cliente, de manera que las interacciones con el servidor se reducen a la lógica de negocios (_bussiness logic_). Los datos de los modelos están enlazados (_Data-binding_) a las vistas de manera automática, haciendo automática el refresqueo de los elementos de HTML. Los controladores manejan los eventos que el usuario y/o el servidor realizan por medio de funciones de Javascript.

 Además permite relativamente fácil el desarrollo de componentes reutilizables y compartibles, generando así una comunidad que comparte platillas y herramientas que aceleran el desarrollo de aplicaciones a una velocidad antes no imaginada.

 Angular también fue pionero en el desarrollo web al implementar nuevas tecnologías de los estándares web como por ejemplo la creación de tags de HTML personalizados `<mi-propio-elemento>`, haciendo mucho más declarativo el HTML. Utiliza el framework de front-end Bootstrap que venía ganando fama en la epoca.

 ### [Conceptos](https://docs.angularjs.org/guide/concepts)

| Concepto |	Description |
| Plantilla (Template) | HTML with additional markup |
| Directivas (Directives) | exitienden el HTML con atributos y elementos personalizados |
| Modelo (Model) | 	datos mostrados a los usuarios en la vista |
| Contexto (Scope) | 	contexto donde el modelos es guardado para que los controladores, directivas y expresiones puedan accederla |
| Expresiones (Expressions) | variables de acceso y funciones del contexto |
| Compilador (Compiler) | parsea las plantillas e instancia las directivas y expresiones |
| Filtro (Filter) | 	Formatea el valor de las expresiones para desplegarlas al usuario |
| Vista (View) | Lo que el usuario ve (el DOM) |
| Enlace de datos (Data Binding) Enlace de datos | Conexión sincronizada de los datos entre el controlador y la vista |
| Controlador (Controller) | La lógica de negocios detrás de las vistas |
| Dependencia de Inyección (Dependency Injection) | Crea y conecta objetos y funciones |
| Inyector (Injector) | El contenedor de la Dependencia de Inyección |
| Modulo (Module) | Un contentedor para las diferentes partes de la app (controladores, filtros, servicios) |
| (Service) | Lógica de negocios reutilizable e independiente de las vistas |

Ejemplo de Enlace de datos
``` html

<div ng-app ng-init="qty=1;cost=2">
  <b>Invoice:</b>
  <div>
    Quantity: <input type="number" min="0" ng-model="qty">
  </div>
  <div>
    Costs: <input type="number" min="0" ng-model="cost">
  </div>
  <div>
    <b>Total:</b> {{qty * cost | currency}}
  </div>
</div>

```

Ejemplo de controlador
``` js

angular.module('invoice1', [])
.controller('InvoiceController', function InvoiceController() {
  this.qty = 1;
  this.cost = 2;
  this.inCurr = 'EUR';
  this.currencies = ['USD', 'EUR', 'CNY'];
  this.usdToForeignRates = {
    USD: 1,
    EUR: 0.74,
    CNY: 6.09
  };

  this.total = function total(outCurr) {
    return this.convertCurrency(this.qty * this.cost, this.inCurr, outCurr);
  };
  this.convertCurrency = function convertCurrency(amount, inCurr, outCurr) {
    return amount * this.usdToForeignRates[outCurr] / this.usdToForeignRates[inCurr];
  };
  this.pay = function pay() {
    window.alert('Thanks!');
  };
});

```


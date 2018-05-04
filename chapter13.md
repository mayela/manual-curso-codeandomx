# Metodologías de desarrollo ágil

Dado los malos resultados de la aplicación de prácticas de manejo de proyectos
como si fueran construcciones civiles en los 90's un grupo de personas decidió
proponer una mejor forma para llevar nuestros proyectos a su correcta ejecuión.
Estás son las prácticas ágiles.

## Modelo Cascada (No ágil)

La mayoría de los proyectos trabaja con un enfoque parecido a lo que se le conoce como modelo de cascada (_Waterfall model_), en donde se tiene un diseño fijo que se le pasa a los desarrolladores y quienes tienen que atenerse a una única dirección de desarrollo y que es poco flexible. Sigue estos pasos:

1. Requerimientos
2. Diseño
3. Imprementación o Desarrollo
4. Verificación
5. Mantenimiento

Es derivado de otras áreas de la ingeniería que distan de la flexibilidad que la ingeniería de software contien. Normalmente es muy ineficiente realizar cambios durante el desarrollo y por lo general las estimaciones de tiempo y esfuerzo resultan incorrectas.

### Errores comunes

- Requerimientos especificos y poco flexibles
    - Por lo general están incompletos y/o ambiguos
    - No incluyen "diseños de baja resolución" (_wireframes_)
    - Los Flujos de interacción no contemplan casos no comunes
- Programador rellena a su criterio lo no especificado
- Diseñador corrije programador, después de meses de desarrollo
- Cliente cambia requerimientos en la etapa final
    - Rigidez
    - Tensión
    - "YO SÉ MÁS"
- Complejidad
- Expectativa de Resultados FInales en cualquier momento
    - diseño perfecto antes que funcionalidad
- Se toman decisiones sin considerar ni comunicarse con los agentes involucrados
  - Desiciones fuera de juntas

## Metodologías Ágiles

Varios equipos de desarrollo después de innumerables procesos de desarrollo difíciles, de cambios imprevistos, de comenzar programas o aplicaciones desde cero por la inhabilidad de mantenerse, fueron diseñando y adoptando otras formas de desarrollo:

Aquí el Manifiesto Ágil [1]

Involucra varios principios

- Desarrollo enfocado a Individuos y sus relaciones, en vez de Herramientas y procesos
- Software funcional y reutilizable, en vez de Documentaciones minusiosas
- Colaboración continua con el cliente, en vez de Negociación extenuante del contrato
- Responsivo al cambio, en ves de Continuar con el Plan

A diferencia de antes impulsa acciones como:

- Entrega constante y pronta de resultados
  - Patín -> Bici -> Moto -> Auto
- Bienvenidos cambios a los Requerimientos
- Fechas de revisión constantes (_Sprints_)
- Interacción constante entre desarrolladores y vendedores
- Individuos motivados, no presionados
- Encuentros cara a cara, no miles de emails
- Software funcional como medida de avance
- Atención código impecable y diseño
- Simplicidad
- Equipos auto-organizados
  - Toma de desiciones horizontales y prácticas, no verticales y mal informadas
- Atención en capacidad de mejora en cada aspecto

### Programación Extrema _XP_ (_Extreme Programing_) [2]

Es una estrategía, basada en el trabajo en equipo, que permite a lxs desarrolladorxs responder de manera efectiva a requerimientos del cliente. El objetivo es generar equipos auto-organizados al rededor de un problema y resolverlo de la manera más eficiente posible.

![](http://www.extremeprogramming.org/map/images/project.gif)

Mejora el proyecto en 5 aspectos:
- Comunicación
- Simplicidad
- Retroalimentación
- Respeto
- Coraje

Se enfoca en hacer liberación de código funcional y probado (_tested_) lo más rápido y simple posible, todo código debe de ser programado entre 2 personas (_Pair Programming_), constantes juntas de equipo, rotación de personas en los equipos para compartición de conocimiento y evitar que el trabajo se vuelva monótono, mejorar la claridad código (_refactoring_) cada que sea posible.


### SCRUM [3]

Una de las metodologías de desarrollo ágil más utilizada. Propone:

![](https://www.denieuwezaak.nl/wp-content/uploads/-BC44D012491CE129E385F386737FB42367538A54EF93E201F4-pimgpsh_fullsize_distr.jpg)

- Pequeños equipos de operacion independientes, pero interconectados
- Mesa de dirección. Mantiene constante comunicación con cliente y desarrolladores
- Proceso de desarrollo no es lineal, sino cíclico
  - _Sprint_ Pequeños ciclos de presentación y evaluación de avances (2-3 semanas)
- Transparencia de Procesos - **Minutas**
  - Claridad de acuerdos
  - Planes a corto plazo
  - Responsables
  - Asistentes
  - Plan de trabajo en los siguientes 2-3 días
- Juntas presenciales Face-to-face
  - No confusiones de redaccion en emails
  - Eficiencia y eficacia de comunicación
- Atención a "excelencia" de diseño y tecnologías
  -  Documentación
  -  Diagramación
  -  Herramientas de apoyo

![](https://images.duckduckgo.com/iu/?u=http%3A%2F%2Fjordanjob.me%2Fwp-content%2Fuploads%2F2016%2F12%2FScrum-Diagram-v2-0-Arrows-1000px.png&f=1)

Se basa en premisas como:
- el cliente puede cambiar de opinión en cualquier momento
- equipos multidisciplinarios trabajan mejor
- comunicación presencial y regular

Propone el uso de Historias de Usuario, en vez de Casos de uso, que consisten en:
  ```
  Como [ROL DE USUARIO], quiero poder [ACCION A REALIZAR] para [OBJETIVO], y asi poder [MOTIVACION]
  ```
- **Rol**: Tipo de usuario
- **Acción**: cómo interactua en la app
- **Objetivo**: Qué espera lograr
- **Motivación**: Más emocional que funcional ¿Cómo me va a hacer sentir?

Estas historias irán moviendose según su avance por distintas columnas

`Por hacer (To do)-> En proceso (doing) -> Por revisar (to review) -> Realizado (done)`

Algunas herramientas para llevar un buen control de proyecto son:
  - Trello [4]
  - Github Project [5]

## Desarrollo Guiado por Pruebas o _TDD_ (_Test Driven Develpment_)

Es una estrategia de programación en donde se programan distintos casos de prueba (_test case_) que simulan al usuario haciendo las acciones que se esperan funcionales. De esta manera, cada que el código se modifica, ya sea por unx mismx, un colega o un contribuidor al repositorio (_pull request_), se corren las pruebas (_tests_) y arrojará si pasan todas las pruebas o no, y si se libera la siguiente versión.


Busca desarrollar funcionalidad de manera modular y simple (_KISS_ Keep It Simple, Stupid), y evitar que el agregar nueva funcionalidad, ocurran errores inesperados (_bugs!_).

Los casos de prueba intentarán abarcar, por medio de generación de datos simulados (_dummy data_), todos los casos posibles. Incluso los casos extremos (_edge cases_) que podrían generar conflictos.

**Pasos**:
- Agregar un caso de prueba
- Correr las pruebas
- Verificar si este nuevo caso de prueba falla
- Corregir falla
- Correr pruebas
- Refactorizar código (hacerlo más leíble)
Repetir

**Ventajas**:
- Productividad
- Flexibilidad
- Extensivilidad
- Lejibilidad de código
- Facilidad de agregar nuevas funcionalidades rápidamente
- Para código abierto (_open source_), incrementa la capacidad de construcción colectiva
- Ayuda a pensar y diseñar la aplicación de una manera enfocada a la experiencia del usuario
-

## Programación en pares (_Pair programing_)

Estrategia que permite el desarrollo de software con menos errores y evitando distracciones. Consiste en *dos* personas trabajando sobre el mismo problema, sentados una junto a la otra, viendo la misma pantalla. La primera ocupa el teclado y es la encargada de escribir el código; la segunda tiene un rol de revisión y de asegurar la claridad y calidad de código:

**Ventajas**:

- Código de calidad
- Compartición de experiencia y conocimiento
- Menor distracción y divagación
- Construcción de sentimiento de equipo

---

### Bibliografía

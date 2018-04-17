# Metodologías de desarrollo ágil

Metodologías AGILE - SCRUM
    Agile
        Agile Manifiesto - http://agilemanifesto.org/principles.html
        Cliente feliz
        Entrega de resultados pronto y contínuo
            patín, triciclo, bici, moto, coche, convertible
        Se aceptan cambios en cualquier momento
            Proceso cíclico
            Constante revisión
        Pequeños equipos de operacion independientes, pero interconectados
        Mesa de dirección - constante comunicación con desarrolladores y con cliente
        Ciclos pequeños de tiempo - SPRINT
            Planea
            Ejecuta
            Revisa
            De nuez
            Tiempos
                Diario
                    2-3 semanas
        Transparencia de
        Negocio (clientes, vendedores) y desarrolladores (programadores, diseñadores, testers) trabajan constantemente juntos
        Juntas presenciales Face-to-face
            No confusiones de redaccion en mails
            Eficiencia y eficacia de comunicación
        Minutas !!!
            Claridad de acuerdos
            Planes a corto plazo
            Responsables
            Asistentes
            Plan de cambios en los siguientes 2-3 días
        Idividuos motivados con el proyecto
            Ponerse en los zapatos del cliente
            No sólo por sacar la chamba
        NO IMPORTA NO LLEGAR A TODAS LAS METAS
            No saber planear
            Sobreestimamos nuestros tiempos y nuestras capacidades
        Flexibilidad
            Proponer desde cualquier rol
        Principal medida de avance es un producto FUNCIONAL
        Atención a "excelencia" de diseño y tecnologías
            Documentación
            Diagramación
            Herramientas de apoyo
        Simplicidad
            Partir en pedazos chiquitos
            Claridad
        Auto-organización
            Cada equipo decide
                En qué tiempos
                Con qué herramientas
                    comunicación
                    comparte resultados
                Quién hace qué
                Procesos
        Constante ajuste de metodología
        Multidiciplinary Pair working - Emparejamiento de trabajo multidiciplinario
            Traduccion inter disciplinas

    SCRUM
        https://www.scrumalliance.org/why-scrum
        https://www.scrumalliance.org/why-scrum/scrum-guide
        Organizar equipos diversos
        Definir area de accion
        Definir responsables
        TO DO - DOING - DONE
            Qué hay que hacer
            Qué se está haciendo
            Qué ya se hizo
            Organizar prioridades
            Definir Responsables
            Medir avances
    Antitesis
        Requerimientos especificos y poco flexibles
            Incompletos
                No wireframes
                Flujos de interacción
                No contemplan EDGE cases
        Programador rellena huecos
        Diseñador corrije programador
        Cliente cambia requerimientos
        Rigidez
            Tensión
            YO SÉ MÁS
        Complejidad
        Expectativa de Resultados FInales en cualquier momento
            diseño perfecto
        Se toman decisiones sin considerar ni comunicarse con los agentes involucrados
            En tiempos que no son juntas
            Historias de Usuario
                Que tiene que tener?
                    Ejemplo
                        Como [ROL DE USUARIO], quiero poder [ACCION A REALIZAR] para [OBJETIVO], y asi poder [MOTIVACION]
                    Rol / Agente
                        A qué tipo de personas está dirigido
                        Quienes y como interacuan en la app
                    Con qué objetivo
                    Qué los motiva
                Porque
                Para qué
                Nunca se dejan de hacer

  UX - User Experience
    best practices
        Checklits
            Fases
                Primera vez que entro
                Cuando ya hay actividad
                Si soy administrador
                Si estoy "logueado"
            Datos a mostrar
                Titulos
                Labels
                Tarjetas
                Botones
                Links
                Imagenes
                Iconos
            Interacciones
                Desde donde se llega
                A donde te lleva cada acción
                Qué elementos aparecen
                Qué elementos desaparecen
                Si aparecen alertas
                Si pide confirmaciones
    tools
        Trello
            Boards por area
            Listas en los boards por Etapa
            Tarjetas
                Checklists
                Descripción
                Attatchments
                Coments @usuario-trello
                Link a otra tarjeta
            Responsables por tarjeta
            Labels
            Menu
                Filtrar por responsable
                Filtrar por label
                Ver última actividad

  UI
      Wireframes low level
          Pizarrón, cuaderno, servilleta
          Pantalla de celular en otro color, más larga que el tamaño normal de pantalla si hay scroll
          Colores distintos para
              Pantalla
              Margenes
              Secciones
              Textos
              Botones
              Links
      Wireframes high level
          Draw.io
          Ventajas
              Versiones
              Modificable por todo el equipo
              Claridad de tamaños, textos
          Flechas de interacción
              Cambio de fase
              Secciones que aparecen
              Butones que realizan acciones
      Modelos de interaccion / animacion
      tools
          Draw.io vector
              como hacer librerias con templates
              como descargar a html
          https://icomoon.io manejador de librería de iconos
          https://thenounproject.com/ millooooones de iconos gratis

=======
## Modelo Cascada

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

Aquí el [Manifiesto Ágil](http://agilemanifesto.org/principles.html)

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

### XP


### SCRUM

Una de las metodologías de desarrollo ágil más utilizada. Propone:

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

Algunas herramientas para llevar un buen control son:
  - [Trello](https://trello.com/tour)
  - [Github Project](https://github.com/features/project-management/)

## TDD

## Programación en pares (_Pair programing_)

Estrategia que permite el desarrollo de software con menos errores y evitando distracciones. Consiste en *dos* personas trabajando sobre el mismo problema, sentados una junto a la otra, viendo la misma pantalla. La primera ocupa el teclado y es la encargada de escribir el código; la segunda tiene un rol de revisión y de asegurar la claridad y calidad de código:

### Ventajas

- Código de calidad
- Compartición de experiencia y conocimiento
- Menor distracción y divagación
- Construcción de sentimiento de equipo
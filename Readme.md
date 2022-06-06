# Desarrollo de aplicaciones con arquitectura monorepositorio

El desarrollo de software utilizando arquitecturas de microservicios, desarrollo ágil y despliegues continuos, hay varios elementos necesarios para lograr que no solo el diseño sino también la construcción responda a la necesidad de comunicación continua, estandarización y eficiencia. Uno de estos elementos es la gestión del código fuente que, sin ser el único factor involucrado, puede ser el punto de partida para los beneficios o los problemas de la solución.
Cuando nos involucramos en el delivery de soluciones con capacidad de escalar a un nivel empresarial, hay que tener en consideración estrategias de gestión de todos los recursos y muy especialmente de la gestión del código ya que es muy fácil dejarse llevar por la tentación de construir y postergar la definición de lineamientos o incluso se pierden de vista y al no aplicarse desde el inicio, generan un efecto de bola de nieve y se vuelve un tema más grande a medida que el proyecto avanza.
Tener un lineamiento inicial, fomentar una disciplina interna de uso de estas línea de instrucción y hacerlas propias de la construcción, facilita que el proceso se vuelva natural al punto que todos puedan "saltar" al proceso de construcción con una estrategia exitosa.

## Resumen

## Conceptos

### 1. ¿Qué es un repositorio código?

Un repositorio de código es el lugar en el que se almacena y se puede realizar la distribución del código fuente de una aplicación de software.En el entorno empresarial, el repositorio de código debe ser un servidor seguro que utiliza sistemas de control de versiones para facilitar la coordinación del equipo de desarrollo. El repositorio debe contener las diferentes versiones de la aplicación, el historial de cambios realizados y los cambios aplicados sobre cada nueva versión. Además, debe permitir poder revertir, de ser necesario, esos cambios. Para cumplir su cometido, el repositorio debe permitir  acceso seguro y en paralelo a los diferentes usuarios involucrados en e equipo de desarrollo, bien sea que estos requieran trabajar en la misma o en sus diferentes versiones.


### 2. ¿Qué es un monorepo?

Monorepositorios, *Mono-repository* o simplemente *monorepo* como se les conoce también en inglés, es un concepto de arquitectura y una estrategia de gestión  del código fuente que consiste en agrupar en un único repositorio de código todos los componentes de la solución.
Un Monorepositorio en lugar de administrar múltiples repositorios, mantiene todas sus partes de código aisladas dentro de un repositorio. Pero el concepto de aislamiento aquí no debe confundirse, un monorepositorio es una estrategia de gestión y no implica crear aplicaciones monolíticas.  Generalmente es todo lo contrario, el concepto mantiene la correcta separación de dependencias que las arquitecturas de microservicios requieren y su uso no compromete otros principios de desarrollo.
Una característica importante para un monorepo es que, si bien contiene múltiples proyectos distintos, estos deben tener entre ellos relaciones bien definidas. El monorepo no se trata de colocar el código en un solo repositorio, si no hay relaciones bien definidas entre los proyecto, no se denomina monorepo. 

### 3. Estructuras de repositorio de código fuente
---
|       Estructura       |                    Implementación             |                              Implementada  por                          |
| :--------------------: | :--------------------------------------------------------------------: | :--------------------------------------------------------------------: |
| Multiples repositorios |   Un repositorio para cada componente o librería de código   |   Amazon, Netflix , Lyft                             |
|    Mono-repositorio    | Un repositorio para todos los componentes o incluso para toda la compañía | Google, Facebook, Microsoft, Uber, Twitter, React, Angular, Babel, Kubernetes |
| Híbrido: Multirepos manejados como  monorepositorio | Los cambios se realizan en multiples repositorios pero se gestionan como un monorepo  | Android, chrome |
| Híbrido: Monorepo manejado como multi | Las cambios se realizan en un monorepo pero luego se dividen en multiples repositorios de solo lectura para construcción o distribución | Symfony, Shopsys | 
---
*Tabla 1: Estructuras de repositorio de código fuente*

### 4. CI/CD

El término CI/CD proviene de las siglas en inglés: *Continuous integration and Continuous delivery*. Es un método para entregar aplicaciones de manera frecuente aprovechando las ventajas de la automatización en las diferentes etapas de desarrollo de aplicaciones. Los principales conceptos atribuidos a CI/CD son integración continua, entrega continua e implementación continua. 


## Agradecimientos

Foto de [Emile Perron, 2017, Unsplash](https://unsplash.com/photos/xrVDYZRGdw4?utm_source=unsplash&utm_medium=referral&utm_content=creditShareLink)

## Referencias

* [Monorepo](https://en.wikipedia.org/wiki/Monorepo)
* [Monorepo’s for Microservices Architecture](https://dzone.com/articles/monorepos-for-microservices-commerce-architecture)
* [Lerna.js](https://lerna.js.org/)
* [How to structure microservices in your repository](https://softwareengineering.stackexchange.com/questions/386066/how-to-structure-microservices-in-your-repository)
* [From Monolith to Monorepo](https://medium.com/@brockreece/from-monolith-to-monorepo-19d78ffe9175)
* GBM Release Management para Software, IN-COT-005, Marzo 2022
* The Issue of Monorepo and Polyrepo In Large Enterprises, Nicolas Brousse, 2019 
* [Monorepo, Manyrepo, Metarepo. 2017](https://notes.burke.libbey.me/metarepo/)
* [Automatically detect changes and initiate different CodePipeline pipelines for a monorepo in CodeCommit](https://docs.aws.amazon.com/prescriptive-guidance/latest/patterns/automatically-detect-changes-and-initiate-different-codepipeline-pipelines-for-a-monorepo-in-codecommit.html)
* [Savkin, V., Misconceptions about Monorepos: Monorepo != Monolith, 2019](https://blog.nrwl.io/misconceptions-about-monorepos-monorepo-monolith-df1250d4b03c)
* [Monorepo tools](https://monorepo.tools/)
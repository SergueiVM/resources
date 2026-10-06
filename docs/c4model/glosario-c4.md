# Glosario del modelo C4

El modelo C4 describe la arquitectura de software mediante un conjunto pequeño de
abstracciones y diagramas que permiten observar un sistema con distintos niveles
de detalle.

## Abstracciones

| Término | Definición |
| --- | --- |
| **Persona (Person)** | Persona, rol o actor externo que interactúa con el sistema. Puede representar a un usuario final o a otro tipo de actor humano. |
| **Sistema de software (Software System)** | Sistema que ofrece valor a sus usuarios y está formado por uno o más contenedores. Puede depender de otros sistemas. |
| **Contenedor (Container)** | Aplicación o almacén de datos que forma parte de un sistema de software. Es una unidad ejecutable o desplegable, como una aplicación web, una API, una aplicación móvil o una base de datos. En C4, «contenedor» no significa necesariamente un contenedor Docker. |
| **Componente (Component)** | Agrupación lógica de responsabilidades dentro de un contenedor. Cada componente tiene un propósito claro y colabora con otros componentes para proporcionar el comportamiento del contenedor. |
| **Código (Code)** | Detalle de implementación de un componente, como clases, interfaces, funciones u otros elementos del código fuente. Normalmente se muestra solo cuando aporta valor. |
| **Relación (Relationship)** | Conexión entre dos elementos que indica cómo se comunican o colaboran. Conviene describir su propósito y, cuando sea útil, el protocolo o la tecnología empleada. |
| **Sistema externo (External system)** | Sistema de software que está fuera del alcance del sistema que se está describiendo, pero que interactúa con él. |
| **Límite (Boundary)** | Marco visual que agrupa elementos relacionados, por ejemplo, los que pertenecen a una empresa, sistema o contenedor. El límite ayuda a entender el alcance, pero no es una abstracción central de C4 por sí misma. |
| **Nodo de despliegue (Deployment node)** | Entorno de infraestructura donde se ejecuta software, como un dispositivo, una máquina virtual, un servidor, un contenedor de ejecución o un servicio de plataforma. Se utiliza en diagramas de despliegue. |

## Tipos de diagramas

| Diagrama | Qué muestra |
| --- | --- |
| **Contexto del sistema (System Context)** | El sistema en su entorno: las personas y los sistemas de software con los que interactúa. |
| **Contenedores (Container)** | Las aplicaciones y almacenes de datos que forman el sistema, junto con sus responsabilidades y comunicaciones. |
| **Componentes (Component)** | La estructura interna de un contenedor y las relaciones entre sus componentes. |
| **Código (Code)** | El detalle de implementación de un componente mediante elementos del código fuente. Es opcional y suele reservarse para casos en los que aporta claridad. |
| **Dinámico (Dynamic)** | Una secuencia de interacciones entre elementos para explicar cómo colaboran en un escenario concreto. |
| **Despliegue (Deployment)** | La asignación de sistemas o contenedores a los nodos de infraestructura en uno o más entornos. |

## Términos usados en los diagramas de este repositorio

| Término | Significado |
| --- | --- |
| **Etiqueta (Tag)** | Metadato visual que se añade a un elemento o a una relación para clasificarlo o aplicar un estilo, como un sprite, un color o una línea discontinua. Una etiqueta no cambia el significado arquitectónico del elemento. |
| **Sprite** | Icono pequeño que puede acompañar a un elemento o aparecer en la leyenda para identificar visualmente una tecnología o categoría. |
| **Boundary** | En los includes de este repositorio, macro que dibuja un límite con una etiqueta opcional; es una convención de representación, no un tipo adicional de elemento C4. |
| **Node / Deployment_Node** | Macros de los includes de este repositorio para representar nodos de despliegue. La forma concreta depende de la macro y del diagrama usado. |

## Lectura de los niveles

Los diagramas se pueden leer como una secuencia de acercamientos:

1. **Contexto:** quién usa el sistema y con qué otros sistemas se relaciona.
2. **Contenedores:** qué aplicaciones y almacenes de datos lo componen.
3. **Componentes:** cómo se organiza internamente uno de esos contenedores.
4. **Código:** cómo se implementa un componente, cuando es necesario mostrar ese nivel.

No es obligatorio crear todos los niveles. Conviene incluir únicamente los
diagramas que ayuden a responder las preguntas de su audiencia.

## Referencias

- [Abstracciones del modelo C4](https://c4model.com/abstractions)
- [Tipos de diagramas C4](https://c4model.com/diagrams)

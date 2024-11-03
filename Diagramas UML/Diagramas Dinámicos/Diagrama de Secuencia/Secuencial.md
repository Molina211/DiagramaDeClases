# Diagrama de Secuencia

## ¿Qué es un Diagrama de Secuencia?

Un **Diagrama de Secuencia** es un tipo de diagrama de UML que representa la secuencia de mensajes o interacciones entre actores y componentes de un sistema en un flujo temporal específico. Este diagrama muestra cómo los objetos o actores se comunican entre sí mediante el envío y recepción de mensajes en orden cronológico, ayudando a visualizar el flujo de operaciones en un sistema.

## Elementos de un Diagrama de Secuencia

- **Actores**: Representan a los usuarios o sistemas externos que interactúan con el sistema.
- **Participantes**: Son los módulos o componentes del sistema que participan en la interacción. Cada uno tiene una **línea de vida** que muestra su existencia durante la secuencia.
- **Mensajes**: Flechas horizontales que indican las solicitudes o respuestas que ocurren entre los actores y participantes, en orden temporal.
- **Línea de Vida**: Línea vertical que representa la existencia de un participante durante el tiempo de ejecución de la secuencia.

## ¿Para qué sirve un Diagrama de Secuencia?

Los Diagramas de Secuencia son útiles para:

- **Describir Casos de Uso Específicos**: Detallan cómo se ejecuta un proceso específico.
- **Identificar Responsabilidades de los Componentes**: Ayudan a visualizar qué acciones realiza cada componente o clase.
- **Facilitar el Diseño Orientado a Objetos**: Describen cómo las instancias de clases se comunican, apoyando la programación y asignación de responsabilidades.
- **Visualizar el Flujo de Información**: Muestran el flujo de datos entre los módulos de un sistema.
- **Optimización del Sistema**: Permiten detectar puntos de mejora en el flujo de información.

## Codigo del diagrama
```planuml
@startuml
actor Usuario
participant "Sistema de Carrito" as Sistema


Usuario -> Sistema: Iniciar sesión
Sistema --> Usuario: Confirmación de inicio de sesión


Usuario -> Sistema: Buscar producto
Sistema --> Usuario: Mostrar resultados de la búsqueda


Usuario -> Sistema: Agregar producto al carrito
Sistema --> Usuario: Confirmación de agregado al carrito


Usuario -> Sistema: Ver carrito
Sistema --> Usuario: Muestra contenido del carrito


Usuario -> Sistema: Comprar productos en el carrito
Sistema --> Usuario: Confirmación de compra y detalles de orden

@enduml
```

## Resultado
![Imagen](Img/DiagramaDeSecuencia.png)

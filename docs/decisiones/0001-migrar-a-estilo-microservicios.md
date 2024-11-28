# Migrar a Estilo Microservicios

## Contexto

Una compañía de productos alimenticios pretende migrar su sistema existente, que posee una
arquitectura de naturaleza monolítica, hacia una arquitectura basada en microservicios, de
manera que la nueva arquitectura sea menos rígida y sea más fácil de evolucionar.

## Opciones Consideradas

* Arquitectura basada en microservicios.

## Decisión tomada

Opción elegida: "Arquitectura basada en microservicios", debido al requisito dado por la compañía. La transición se llevará a cabo mediante la separación de la estructura monolítica actual en los siguientes servicios independientes que luego seran descompuestos en microservicios:
* Servicio de Gestión de Reparto y Rutas
* Servicio de Pedidos
* Servicio de Estadisticas
* Servicio de Usuarios

### Consecuencias

* Bueno, porque brinda mas escalabilidad, modificabilidad, capacidad de despliegue independiente y reusabilidad de componentes.
* Malo, porque la transición a microservicios puede afectar el rendimiento y agregar complejidad en el desarrollo.
* Malo, debido a que requiere implementar y mantener un sistema de contenedorización (como Docker) y, posiblemente, herramientas de orquestación (como Kubernetes), lo que implica costos adicionales en términos de aprendizaje, configuración y mantenimiento.

[<- VOLVER A LA ITERACIÓN](/docs/iteraciones/iteracion-0.md)
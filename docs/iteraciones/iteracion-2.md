# Iteracion 2

## Descripcion

El microservicio de Pedidos es una funcionalidad muy importante del sistema, diseñada para permitir a los clientes realizar pedidos de productos. Este servicio debe a asegurar que el proceso de pedido sea fluido, controlado y fiable. El sistema debe ser capaz de manejar un alto volumen de pedidos por hora, lo que implica que la escalabilidad y el rendimiento del sistema serán cruciales, especialmente durante picos de demanda. El proceso de gestión de pedidos sigue una cadena de tres fases bien definidas y en forma secuencial: preprocesado del pedido, autorización y aceptación.

## Objetivos

En esta iteración, se abordó la definición y diseño de la estructura del microservicio de pedidos dentro de la nueva arquitectura de microservicios. La decisión de dividir el microservicio de pedidos en múltiples servicios independientes tiene como objetivo optimizar la modularidad y la flexibilidad del sistema, permitiendo que cada componente pueda evolucionar de manera autónoma y adaptarse mejor a futuras necesidades y regulaciones. Asimismo, se tomó como referencia otros métodos de gestión de pedidos utilizados en otros proyectos y en arquitecturas similares para garantizar que el microservicio de pedidos sea eficiente y escalable. El hecho de utilizar soluciones probadas nos brinda mayor seguridad a la hora tomar esta decision.

## Drivers
* QAs: Modificabilidad
* QAs: Integridad
* QAs: Escalabilidad
* QAs: Flexibilidad

## Artefactos a generar

* Profundizar el estilo EDA como comunicacion entre los distintos servicios del modulo de pedidos.
* Refinar los cuatro microservicios del modulo de pedidos.


## Resultados

* [ADR 0004](/docs/decisiones/0004-estructura-de-microservicio-de-pedidos.md) Documento detallado que describe la estructura y el diseño del microservicio de pedidos.
* [VISTA DEL MODULO DE PEDIDOS](/docs/vistas/Diagrama_de_division_de_microservicios_de_pedidos.png) En esta vista se obvserva como se divide el modulo de pedidos en distintos microservicios 
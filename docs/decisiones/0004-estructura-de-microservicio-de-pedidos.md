# Estructura de microservicio de pedidos

## Contexto

El servicio de pedidos es la responsable de recabar la información para generar el pedido, establecer una comunicacion con el servicio de MercadoPago para realizar el pago y enviar el pedido al servicio de gestión y rutas.

## Opciones Consideradas

* Un solo microservicio: pedidos
* Dos microservicios: carrito, pedidos
* Tres microservicios: carrito, pedidos, pagos
* Cuatro microservicios: carrito, pedidos, pagos, notificaciones

## Decisión tomada

Opción elegida: "Cuatro microservicios: carrito, pedidos, pagos, notificaciones". 

### Consecuencias

* Bueno, porque nos brinda mayor modificabilidad para cambiar las formas de pago y adecuarse a posibles cambios en las regulaciones.
* Bueno, porque nos brinda mayor flexibilidad para realizar las notificaciones a los usuarios acerca del estado de los pedidos.
* Malo, porque la performance se ve afectada debido a las intercomunicaciones entre microservicios.
* Malo, porque aumenta la complejidad de desarrollo.
* Esta decision nos encamina a utilizar un estilo EDA (Event Driven Arquitecture) como comunicacion entre microservicios del sistema de pedidos. 

# Estructura de microservicio de pedidos

## Contexto

El servicio de pedidos es esencial en el sistema para gestionar el ciclo completo de los pedidos realizados por los usuarios. Este servicio debe: recabar la información para generar el pedido, establecer una comunicacion con el servicio de MercadoPago para realizar el pago, enviar el pedido al servicio de gestión y rutas y notificar al usuario sobre el estado de su pedido. Con la nueva arquitectura se analizaron varias opciones para estructuraar este servicio.

## Opciones Consideradas

* Un solo microservicio: pedidos
* Dos microservicios: carrito, pedidos
* Tres microservicios: carrito, pedidos, pagos
* Cuatro microservicios: carrito, pedidos, pagos, notificaciones

## Decisión tomada

Opción elegida: "Cuatro microservicios: carrito, pedidos, pagos, notificaciones" debido a las ventajas significativas en términos de escalabilidad, flexibilidad y manteníbilidad. 

### Consecuencias

* Bueno, porque nos brinda mayor modificabilidad para cambiar las formas de pago y adecuarse a posibles cambios en las regulaciones.
* Bueno, porque nos brinda mayor flexibilidad para realizar las notificaciones a los usuarios acerca del estado de los pedidos.
* Bueno, ya que cada microservicio puede escalar de forma independiente segun las necesidades.
* Bueno, debido a que cada microservicio tiene responsabilidades bien definidas, lo que facilita su desarrollo, mantenimiento, y desplegabilidad de forma independiente.
* Malo, porque la performance se ve afectada debido a las intercomunicaciones entre microservicios.
* Malo, porque aumenta la complejidad de desarrollo.
* Malo, porque se va a necesitar mas infraestructura (base de datos, colas) lo que implica un mayor costo.
* Esta decision nos encamina a utilizar un estilo EDA (Event Driven Arquitecture) como comunicacion entre microservicios del sistema de pedidos. 

[<- VOLVER A LA ITERACIÓN](/docs/iteraciones/iteracion-2.md)
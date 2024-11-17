# Desarrollo de comunicacion de los servicios

## Contexto

Al migrar a un sistema de microservicios, debemos definir la forma en la que los servicios se comunican, teniendo en cuenta su funcionalidad. El servicio de usuarios es la encargada de gestionar los perfiles y autenticar a los mismos. Por otro lado el servicio de estadisticas se encarga de recabar la informacion de los usuarios, pedidos y camiones con el objetivo generar datos que luego se utilizaran para analizar el funcionamiento del sistema. Para optimizar la logística de entrega, el Servicio de Reparto y Rutas planificará y monitorizará el estado de los camiones. Finalmente, el servicio de pedidos es la responsable de recabar la informacion para generar el pedido y establecer una comunicacion con el servicio de MercadoPago para realizar el pago.

## Opciones Consideradas

* Comunicacion sincronica : HTTP/REST
* Comunicacion asincronica : Basada en eventos
* Híbrida (comunicacion sincrona y asincrona)

## Decisión tomada

Chosen option: "Híbrida (comunicacion sincrona y asincrona)", porque combina lo mejor de ambos enfoques según las necesidades de los servicios. Los servicios de Pedidos y Gestión de Rutas utilizarán una comunicación dirigida por eventos. Esto permitirá que estos servicios manejen eventos de manera asincrónica, asegurando un flujo continuo de información sin bloqueos, especialmente útil para manejar la carga variable en pedidos y rutas. Por otro lado, los servicios de Usuario y Estadísticas implementarán una comunicación basada en HTTP/REST. Este protocolo será ideal para operaciones que requieren solicitudes simples y directas, como consultas de información de usuario y estadísticas, donde la respuesta inmediata no es crítica para la funcionalidad del sistema.

### Consecuencias

* Bueno, porque nos permite utilizar el mecanismo de comunicacion mas eficiente segun las necesidades de los servicios, otorgando una mejor perfomance
* Malo, porque se debe aprender dos tipos distintos de comunicacion para desarrollar estas comunicaciones
* Malo, porque se debe agregar estructuras de colas para poder manejar la comunicacion basada en eventos
 
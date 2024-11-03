# Atributos de calidad para el Sistema.

En este documento, se listan varios atributos de calidad junto a sus escenarios. Algunos atributos no estan especificados en la descripción pero asumimos que son importantes para el sistema.

## *Disponibilidad*
- En caso de que falle un modulo, el sistema debe poder recuperarse rapidamente (el sistema debe retomar su funcionamiento habitual en menos de 30 segundos).

## *Escalabilidad*
- En horarios de alta demanda, el sistema debe poder aumentar los recursos de los microservicios demandados para poder mantener el servicio sin degradación (ej: soportar un aumento del 300% de la carga habitual).   

## *Performance* 
- Al momento de asignarle una ruta al conductor, el sistema debe generar el camino optimo (ej: el 95% de las rutas asignadas deben ser las optimas).
- Si un usuario realiza un pedido, el sistema debe preprocesar, autorizar y aceptar el pedido en el menor tiempo posible (ej: las tres fases se deben realizar en menos de 2 segundos).

## *Interoperabilidad* 
- A la hora de realizar el pago, la aplicación debe operar sin problemas con Mercado Pago, permitiendo a los usuarios acceder a su cuenta realizar la compra. (ej: se debe garantizar que el usuario finalice la transaccion en menos de 10 segundos).

## *Seguridad*
- Si un administrador intenta modificar/eliminar un pedido, el sistema debe solicitar autenticacion para validad la identidad del administrador (ej: la autenticacion debe tener una tasa de exito del 100%).

## *Usabilidad* 
- Cuando se un clíente realiza un pedido y ingresa sus datos erroneamente, el sistema debe indicar con un mensaje claro donde se encuentra el error y las opciones de corrección. (ej: el 90% de los usuarios deben corregir el error en el primer intento).

## *Modificabilidad*
- Cuando los desarrolladores desean actualizar un servicio, el despliegue se debe realizar sin interrupciones. (ej: tiempo de despliegue menor a 10 minutos) 



# ***Actors***
- Clientes
- Flotas de transporte
- Sistema de gestión de reparto y rutas ?
- MercadoPago (creo que no va)
- Administrador ? 
- Sistema de pedidos ?


<br>

# ***Clientes en el sistema de pedidos***

## Manejo de cuenta.
- Registro de usuario.
- Autenticación usando nombre de usuario y contraseña.
- Acceder a sus datos personales.
- Actualizar sus datos personales.
- Ver historial de pedidos.

## ***Catalogo*** 
- Buscar las opciones de productos.
- Agregar productos al carrito de compras. 
- Borrar productos del carrito de compras. 
    
## ***Pedidos*** 
- Realizar un pedido del carrito, seleccionando la fecha y lugar de entrega.
- Modificar un pedido del carrito.
- Cancelar pedido.
- Ver estado del pedido.

<br>

<br>


# ***Flotas de transporte en el Sistema de gestión de reparto y rutas***

## Rutas
- Informar incidencia.
- Visualizar ruta.

<br>


# ***Administrador en el sistema***

## ***Gestión de Usuarios***
- Crear, modificar y eliminar cuentas de usuario.
- Asignar y gestionar roles y permisos específicos para cada tipo de usuario.
- Habilitar y deshabilitar el acceso de usuarios al sistema según necesidades de seguridad.

## ***Monitoreo de Microservicios***
- Visualizar el estado en tiempo real de cada microservicio.
- Consultar y analizar los registros de actividad (logs) de cada microservicio para identificar posibles errores.

<br>

# ***Sistema*** 
[comment]: <> (Ver si separar el sistema en distintos microservicios ahora o hacerlo general)
## ***Gestión de Pedidos***
- Limitar el numero maximo de intentos de pedidos a 3.
- Procesar los pedidos en tres fases: Preprocesado del pedido, autorización y aceptación.
- Actualizar base de datos luego de un pedido realizado.
- Mostrar la información de los pedidos a usuarios autorizados.

## Gestión de Reparto y Rutas
- Asignar pedidos a conductores.
- Implementar dos algoritmos de optimización de rutas.
- Seleccionar ruta optima y informarsela al conductor.
- Se debe proporcionar monitoreo en tiempo real.
- Recalcular rutas luego de recibir una incidencia.
- Informar a gestion de pedidos en caso de incidencia (reparto no realizado).

## ***Otros***
- Proporcionar estadisticas acerca de los clíentes.
- Proporcionar información sobre el estado de los pedidos.
- Generar pagos con el servicio de MercadoPago.
- Informar al usuario sobre el estado del pago.

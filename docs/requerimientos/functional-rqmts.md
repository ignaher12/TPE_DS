Descripcion del documento.

# ***Actors***
- Clientes
- Flotas de transporte
- Sistema de gestión de reparto y rutas ?
- MercadoPago
- Administrador ? 
- Sistema de pedidos ?


<br>

# ***Clientes en el sistema de pedidos.***

## Manejo de cuenta.
- Registro de usuario.
- Autenticación usando nombre de usuario y contraseña.
- Acceder a sus datos personales.
- Actualizar sus datos personales.
- Ver historial de pedidos..

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


# ***Flotas de transporte en el Sistema de gestión de reparto y rutas.***

## Rutas
- Informar incidencia.
- Visualizar ruta.

<br>


# ***Smart Fridge system <sup>3</sup>***
- Our system:
    - Posts or updates a purchase order on the Smart Fridge system: consumer identification<sup>4</sup>; meals and quantities; smart fridge location; date and time range availability
        - Done after a customer places, edits or cancels an order for smart fridge pick up
    - Query pick up and purchase transactions 
        - Done periodically to find out about picked up orders and ad hoc purchases
        - Can be combined or replaced with a push notification mechanism, if the smart fridge system has that ability
    - Query inventory levels of one or more fridges
        - Done when the customer is searching for meal availability per location
    - Update fridge inventory 
        - Done after the replenisher replenishes a fridge or confirms stock after visual inspection
    - Query fridge status
    - Update fridge status
        - Done after the replenisher detects an issue or change of status in a fridge
<br>


# ***Vendor POS system***
- Post or update a purchase order: consumer identification; meals and quantities; vendor store location; date and time range availability 
    - Done after a customer places, edits or cancels an order for vendor kiosk pick up
- Query pick up and purchase transactions 
    - Done periodically to find out about picked up orders and ad hoc purchases
    - Can be combined or replaced with a push notification mechanism, if the vendor POS system has that ability
<br>


# ***Farmacy Food central kitchen system***
- Post meal orders
- Post inventory levels for smart fridges
- Post inventory levels for vendor POS

<br>


### Notes
<p><sup>1</sup> Native mobile app or web app.</p>
<p><sup>2</sup> Farmacy Food representative responsible for replenishing the stock of meals in smart fridges and vendor kiosks.</p>
<p><sup>3</sup> Operations correspond to API endpoints that we expect to see in the Smart Fridge cloud-based system.</p>
<p><sup>4</sup> Credit or debit card, or order confirmation code to be presented at the smart fridge for pickup.</p>

# Utilizar un base de datos por servicio

## Contexto

En la arquitectura actual, los datos se encuentran centralizados en dos bases de datos SQL: una para Clientes y otra para Pedidos.

## Opciones Consideradas

* Base de datos por servicio
* Base de datos centralizada

## Decisión tomada

Opción elegida: "Base de datos por servicio", porque permite mejorar el desacoplamiento entre servicio brindando una mayor independencia.

### Consecuencias

* Bueno, porque brinda mas autonomia a los servicios del sistema.
* Malo, porque se deben utilizar una mayor cantidad de recursos al separar en distintas bases de datos.
* Bueno, porque permite distribuir todas las peticiones a las bases de datos evitando el cuello de botella. 

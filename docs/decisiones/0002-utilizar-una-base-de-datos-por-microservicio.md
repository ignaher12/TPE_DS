# Utilizar un base de datos por microservicio

## Contexto

En la arquitectura actual, los datos se encuentran centralizados en dos bases de datos SQL: una para Clientes y otra para Pedidos. Esta configuración, aunque funcional, hace que los servicios que dependen de estas bases de datos enfrentan restricciones importantes en su capacidad para operar de manera independiente.

## Opciones Consideradas

* Base de datos por servicio
* Base de datos centralizada
* Base de datos para Clientes y otra para Pedidos (configuración actual)

## Decisión tomada

Opción elegida: "Base de datos por servicio". Se eligio este enfoque porque permite desacoplar completamente los servicios, generando una arquitectura más flexible, escalable y adaptable a las necesidades específicas de cada componente del sistema. 

### Consecuencias

* Bueno, porque brinda mas autonomia a los servicios del sistema.
* Bueno, porque permite distribuir todas las peticiones a las bases de datos evitando el cuello de botella. 
* Bueno, ya que mejora la escalabilidad y la capacidad de adaptación a nuevas teconologías.
* Malo, porque se deben utilizar una mayor cantidad de recursos al separar en distintas bases de datos.
* Malo, debido a que aumenta la complejidad para la configuración y moniterio de las multiples bases de datos.

[<- VOLVER A LA ITERACIÓN](/docs/iteraciones/iteracion-1.md)
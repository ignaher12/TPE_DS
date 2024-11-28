# Implementar un balanceador de cargas sobre servicio de usuarios

## Contexto

Esta nueva arquitectura permite dividir el sistema en servicios más pequeños e independientes, cada uno enfocado en una funcionalidad específica. Esto mejora la flexibilidad del desarrollo y permite que cada servicio se escale de manera autónoma según sus necesidades, sin afectar a otros componentes del sistema. Debido a esto se debe implementar un metodo que gestione todas las peticiones de los usuarios hacia los multiples servicios desplegados, ademas de evitar la saturacion de uno de estos servicios.

## Opciones Consideradas

* Balanceador de cargas
* Sin Balanceador de Carga
* Caches para evitar sobrecarga de servicios


## Decisión tomada

Opción elegida: " Balanceador de cargas ", porque ofrece una mayor distribución del tráfico de los usuarios hacia los multiples microservicios desplegados, evitando generar cuellos de botellas u overflows de los buffers.

### Consecuencias

* Bueno, porque se evita la sobrecarga y caida de servicios.
* Bueno, porque permite una mayor flexibilidad a la hora de replicar microservicios.
* Bueno, porque agrega seguridad extra al acceso al sistema pudiendo desviar trafico malisioso.
* Malo, porque agrega latencia al procesamiento de peticiones.
* Malo, porque agrega complejidad a la hora de configurar el balanceador
* Malo, porque incrementa el costo de despliegue y mantenimiento

[<- VOLVER A LA ITERACIÓN](/docs/iteraciones/iteracion-3.md)
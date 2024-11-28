# Iteracion 3
## Descripcion

El sistema monolítico actual enfrenta importantes desafíos relacionados con la gestión del servicio de Usuarios, que se encarga de autenticar y gestionar los perfiles de quienes interactúan con la plataforma. Este servicio es crítico y está expuesto a problemas de rendimiento, especialmente durante picos de acceso masivo, como los generados por promociones o lanzamientos. La arquitectura actual no está equipada para manejar estos picos de manera eficiente, lo que provoca tiempos de respuesta lentos e incluso interrupciones del servicio.

Uno de los principales problemas identificados es la dependencia de una única instancia para procesar todas las solicitudes de usuarios. Este enfoque crea un cuello de botella que afecta la experiencia de los clientes y limita la capacidad del sistema para escalar dinámicamente según la demanda. Además, cualquier fallo en esta instancia puede llevar a la interrupción completa del servicio, afectando tanto la autenticación como la gestión de perfiles.

## Objetivos

En esta iteración, el objetivo principal es planificar e identificar los pasos necesarios para implementar el microservicio de Usuarios dentro de la arquitectura basada en microservicios. Esto incluye definir cómo se gestionarán las operaciones básicas del servicio, como la autenticación de usuarios y la actualización de perfiles, asegurando que el diseño sea escalable, eficiente y cumpla con los requerimientos de desempeño.

En primer lugar, al analizar la funcionalidad de este servicio, se eligio por no dividir el microservicio de Usuarios en subcomponentes adicionales, como podría ser un servicio específico para Administradores. La razón principal de esta decisión es que los requerimientos de este microservicio son relativamente simples, abarcando la gestión de perfiles y la autenticación, sin necesidad de una complejidad adicional que justifique una separación en más microservicios. Esta estrategia también favorece la performance, al reducir la sobrecarga de comunicaciones entre servicios y simplificar el proceso de mantenimiento y despliegue.

Por ultimo,se planificará la implementación de un balanceador de cargas que se encargue de distribuir las solicitudes de manera equitativa entre las distintas instancias del microservicio de Usuarios. El balanceador de cargas garantizará la escalabilidad del sistema, mejorando la disponibilidad y el rendimiento durante los picos de tráfico. Esta medida es crucial para asegurar que el microservicio sea capaz de manejar un alto volumen de peticiones sin comprometer la eficiencia del sistema ni afectar la experiencia del usuario. 

## Drivers

* QAs: Escalabilidad
* QAs: Performance
* QAs: Seguridad

## Resultados

* [ADR 0005](/docs/decisiones/0005-estructura-de-microservicio-de-usuarios.md) Documento detallado que describe la estructura y el diseño del microservicio de usuarios, abordando su funcionalidad y las decisiones tomadas respecto a su implementación.
* [ADR 0006](/docs/decisiones/0006-implementar-un-balanceador-de-cargas-sobre-microservicio-de-usuarios.md) Artefacto que detalla la implementación de un balanceador de cargas para distribuir eficientemente las solicitudes y garantizar la escalabilidad del microservicio de usuarios.
* [VISTA DEL MICROSERVICIO DE USUARIOS](/docs/vistas/Diagrama_de_division_de_microservicio_de_usuarios.png)  Este diagrama muestra la arquitectura del microservicio de usuarios dentro del sistema.

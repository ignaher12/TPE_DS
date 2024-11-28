# Iteracion 1

## Descripcion
En esta iteración, se trabaja en dos aspectos fundamentales para consolidar la arquitectura basada en microservicios:
* Separación de bases de datos por microservicio para mejorar la independencia, escalabilidad y robustez del sistema.
* Definición de los mecanismos de comunicación entre microservicios, adoptando un enfoque híbrido que combina comunicación sincrónica y asincrónica según las necesidades específicas de cada servicio.
Estos pasos son esenciales para sentar las bases de una arquitectura eficiente y bien desacoplada que permita adaptarse a las demandas de la operación y del mercado.

## Objetivos
El objetivo principal de esta iteración es avanzar en la implementación de una arquitectura desacoplada y eficiente para los microservicios del sistema. Esto incluye establecer bases de datos independientes para cada microservicio, lo que permite mayor autonomía en el manejo de datos y facilita la escalabilidad. Además, se busca definir una estrategia híbrida de comunicación que combine lo mejor de los enfoques sincrónico y asincrónico, asegurando interacciones fluidas y optimizadas entre los servicios según sus necesidades específicas.

## Drivers
* Restricción: El protocolo de acceso debe ser HTTP/REST.
* QA : Interoperabilidad, Seguridad y Performance.

## Artefactos a generar
* Definir tecnologia de persistencia de datos del sistema.

## Resultados
* [ADR 0002](/docs/decisiones/0002-utilizar-una-base-de-datos-por-microservicio.md) ADR donde se ve reflejada la decision de utilizar una base de datos por microservicio y sus beneficios.
* [ADR 0003](/docs/decisiones/0003-desarrollo-de-comunicacion-de-los-microservicios.md) Documento que detalla la decisión de utilizar un enfoque híbrido de comunicación entre microservicios.
* [DIAGRAMA DE DIVISION DE MICROSERVICIOS](/docs/vistas/Diagrama_de_division_de_microservicios.png) En esta vista se observa el estado del diseño de los microservicios con los protocolos de comunicación y la base de datos por módulo.
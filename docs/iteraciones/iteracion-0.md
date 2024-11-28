# Iteracion 0

## Descripcion
La compañía de productos alimenticios enfrenta desafíos importantes debido a la limitación de su sistema actual, que está basado en una arquitectura monolítica. Esta rigidez en la arquitectura monolítica ha generado dificultades para modificar y escalar el sistema, lo que afecta la capacidad de la empresa para adaptarse a nuevas demandas del mercado y a la expansión de su operación. El sistema monolítico actual dificulta la introducción de nuevos cambios sin que afecten otras partes del sistema, lo cual incrementa el riesgo de errores y hace que el proceso de mantenimiento y actualización sea más costoso y lento.
Debido a estos problemas, la empresa ha decidido migrar a una arquitectura basada en microservicios. 

## Objetivos
El propósito de esta iteración es avanzar en la migración del sistema monolítico a una arquitectura basada en microservicios. Esta nueva arquitectura permitira que cada componente del sistema  sea independiente, lo que facilitara las modificaciones y mejoras sin afectar el resto del sistema. Los microservicios proporcionan una mayor escalabilidad, flexibilidad y agilidad en el desarrollo, permitiendo a los equipos trabajar de manera autónoma en diferentes partes del sistema y facilitar la integración de nuevas funcionalidades de forma más eficiente y sin comprometer la estabilidad general del sistema.

## Drivers
* Restriccion: Migracion a un sistema basado en microservicios [REF]

## Artefactos a generar
* Se deben refinar los microservicios
* Definir tecnologia de comunicacion entre microservicios.

## Resultados
* [ADR 0001](/docs/decisiones/0001-migrar-a-estilo-microservicios.md) En este artefecto se ve reflejada la decision de la separacion del sistema en microservicios, junto con los pros y contras.
* [DIAGRAMA DE DIVISION POR DOMINIO](/docs/vistas/Diagrama_de_division_por_dominios.png) En esta vista se visualiza la forma de separacion de la arquitectura en los distintos microservicios. 
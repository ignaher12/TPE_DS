# Estructura de microservicio de usuarios

## Contexto

El servicio de usuarios se encarga de gestionar los perfiles de los usuarios y autenticar sus credenciales. Incluye tanto usuarios regulares como administradores, quienes tienen permisos adicionales para gestionar ciertos aspectos del sistema.

## Opciones Consideradas

* Un solo microservicio {Usuarios}
* Dos microservicio {Usuarios , Administradores}

## Decisión tomada

Opción elegida: " Un solo microservicio {Usuarios}". Se decidió juntar las funcionalidades de usuarios y administradores en un único microservicio, dado que las funcionalidades exclusivas para administradores no justifican la sobrecarga de mantener un microservicio independiente.

### Consecuencias

* Bueno, porque reducimos la cantidad de recursos al no generar una base de datos solamente para los administradores
* Bueno, porque mejoramos la performance ya que la comunicacion en un mismo microservicio es mas eficiente que entre dos microservcios distintos
* Bueno, debido a que facilita el desarrollo.
* Malo, porque perdemos modificalidad y desplegabilidad si se requiere modificar alguna funcionalidad especifica de alguno de los dos roles.
* Malo, ya que se pierde escalabilidad si las funcionalidades de administradores crecen considerablemente.

[<- VOLVER A LA ITERACIÓN](/docs/iteraciones/iteracion-3.md)
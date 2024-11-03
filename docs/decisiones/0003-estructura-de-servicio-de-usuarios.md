# Estructura de servicio de usuarios

## Contexto

El servicio de usuarios es la encargada de gestionar los perfiles y autenticar a los mismos.

## Opciones Consideradas

* Un solo microservicio {Usuarios}
* Dos microservicio {Usuarios , Administradores}


## Decisión tomada

Opción elegida: " Un solo microservicio {Usuarios}", porque consideramos que la funcionalidad de los administradores no era tan extensa ni compleja para separarlo en otro microservicio independiente.

### Consecuencias

* Bueno, porque reducimos la cantidad de recursos al no generar una base de datos solamente para los administradores
* Bueno, porque mejoramos la performance ya que la comunicacion en un mismo microservicio es mas eficiente que entre dos microservcios distintos
* Malo, porque perdemos modificalidad y desplegabilidad si se requiere modificar alguna funcionalidad especifica de alguno de los dos roles.

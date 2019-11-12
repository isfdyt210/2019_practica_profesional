# Aplicación para la administración de objetivos

La organizacion F***** cuenta con una gran cantidad de proyectos y usuarios, 
dichos usuarios tienen objetivos que cumplir y acciones que tomar.

El objetivo de esta aplicacion es crear un servicio con el que la organizacion F
pueda ver el avance de los objetivos por cada uno de sus usuarios.

Un usuario tiene una serie de objetivos, los objetivos constan de acciones.
Dichas acciones son atomicas por lo tanto no se pueden descomponer en otras acciones.

De un usuario se conoce:

* Nombre
* Apellido
* Nombre de Usuario
* Si es lider
* Puesto

De un objetivo

* El usuario
* Nombre
* Que?
* Porque?
* Fecha de Inicio

De una acción

* Tiene un objetivo
* Como?
* Fecha de Fin

### Arquitectura de la aplicación
La aplicacion puede ser desarrollada bajo dos arquitecturas

1. WEB APP: Una aplicacion web con manejo de sesiones (Cookie) y manejo de vistas por plantillas
2. API REST: Una API rest con manejo de sessiones (Token) y manejo vistas por JSON

### 1. Aplicacion Web Clásica (WEB APP)

* Crear una aplicación web
* Respetar el patrón de diseño MVC
* Distinguir entre el ambiente de desarrollo y de producción
* Persistir los datos

#### Casos de uso WEBAPP

1. Ingreso a la aplicación.
2. Egreso de la aplicacón.
3. Alta Baja y Modificacion (ABM) de Usuarios.
4. ABM de Objetivos.
5. ABM de Acciones.
6. Todos los recursos tienen que estar protegidos, un usuario sin privilegios.
no puede borrar o crear los recursos de la aplicación.
7. Tiene que utilizarse un sistema de plantillas para el manejo de las vistas.
8. Todos los casos de uso deben poder ser probados desde el navegador.


### 2. Servicio REST (API REST)

* Crear un servicio REST
* Respetar el patrón de diseño MVC
* Persistir los datos

#### Casos de uso de la API REST

1. Ingreso a la aplicación via token.
2. Egreso de la aplicacón (eliminación del token).
3. Alta Baja y Modificacion (ABM) de Usuarios.
4. ABM de Objetivos.
5. Todos los recursos tienen que estar protegidos, un usuario sin privilegios
no puede borrar o crear los recursos de la aplicación.
6. La vista de cada recurso debe ser un JSON.
7. La respuesta de cada peticion debe ser 'application/json'.
8. Todos los casos de uso deben poder ser probados con el comando `curl` o similar.


## Notas

* La API deberá respetar la arquitectura [REST](http://en.wikipedia.org/wiki/Representational_State_Transfer)
* Los links en los ejemplos utilizan http://localhost:5000 asumiendo que la API
corre en este puerto. Pero si el día de mañana la API se instalace en
http://objetivos.acme.com, todas las URLs de los ejemplos deberán cambiar.
* El trabajo deberá seguir los coding standards del lenguaje (si no sigue los coding
standards es motivo de desaprobación).

# Air-Lux

_ Proyecto 2_RebootAcademy

## Comenzando 🚀

Estas instrucciones te permitirán obtener una copia del proyecto en funcionamiento en tu máquina local para propósitos de desarrollo y pruebas.

Realiza un fork en nuestro proyecto y tendrás una copia en tu cuenta, a partir de ese momento podras realizar las modificaciones y mejoras que desees.


### Pre-requisitos 📋

Necesitas un navegador tipo google Chrome, Mozilla Firefox

## Construido con 🛠️

JavaScript, Node, Html5, css3, Mongoose, Express, Axios y Bootstrap.

### Configuración del proyecto

npm install

## Esquemas DB

### Usuario
| KEY      | TYPE   | REFERENCE | REQUIRED | VALIDATION     |
|----------|--------|-----------|----------|----------------|
| email    | string |           | YES      | RegExp, Unique |
| password | string |           | YES      |                |

### Empresas
| KEY       | TYPE       | REFERENCE | REQUIRE | VALIDATION |
|-----------|------------|-----------|---------|------------|
| nombre    | string     |           | YES     |            |
| CIF       | string     |           | NO      |            |
| direccion | string     |           | NO      |            |
| email     | string     |           | YES     |            |
| tlf       | number     |           | YES     |            |
| contact   | string     |           | NO      |            |
| sucursales| [ObjectId] | sucursales| NO      |            |

### Sucursales
| KEY       | TYPE     | REFERENCE | REQUIRE | VALIDATION |
|-----------|----------|-----------|---------|------------|
| empresa   | ObjectId | empresas  | YES     |            |
| nombre    | string   |           | NO      |            |
| direccion | string   |           | NO      |            |
| tlf       | number   |           | YES     |            |
| contacto  | string   |           | NO      |            |

## Rutas API

### Autentificación ENDPOINTS
| METHOD | URL            | AUTH | FUNCTION                |
|--------|----------------|------|-------------------------|
| POST   | '/auth/signup' | NO   | Crear usuario           |
| POST   | '/auth/login'  | NO   | Autentificar un usuario |

### Usuario ENDPOINTS
| METHOD | URL                         | AUTH | FUNCTION                                   |
|--------|-----------------------------|------|--------------------------------------------|
| GET    | '/'                         | NO   | Ver página web                             |
| GET    | '/empresas'                 | YES  | Ver todas las empresas                     |
| GET    | '/empresas/id'              | YES  | Ver una empresa                            |
| GET    | '/empresas/id/sucursales    | YES  | Ver todas las sucursales de una empresa    |
| GET    | '/empresas/id/sucursales/id | YES  | Ver una sucursal de una empresa            |
| POST   | '/empresas/'                | YES  | Crear una empresa                          |
| POST   | '/empresas/id'              | YES  | Crear una sucursal                         |
| PUT    | '/empresas/id'              | YES  | Editar una empresa                         |
| PUT    | '/empresas/id/sucursales/id | YES  | Editar una sucursal                        |
| DELETE | '/empresas/id               | YES  | Borrar una empresa                         |
| DELETE | '/empresas/id/sucursales    | YES  | Borrar todas las sucursales de una empresa |
| DELETE | '/empresas/id/sucursales/id | YES  | Borrar una sucursal                        |

## Licencia 📄

Este proyecto está bajo la Licencia (MIT License) - mira el archivo [LICENSE.md](LICENSE.md) para detalles

## Expresiones de Gratitud 🎁

* Mis profesores, geniales 📢

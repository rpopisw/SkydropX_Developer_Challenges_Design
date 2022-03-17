# Título del Proyecto

_Template de Diseño de APIs

## Comenzando 🚀


_Estas instrucciones te permitirán obtener una copia del Template / Arquetipo del API Portal funcionando en tu entorno local, con el proposito de que puedas implementar en tu proyecto, en base a las buenas practicas.-


### Pre-requisitos 

_Software que necesitas instalar_

Node Js
* [Node.js®](https://nodejs.org/es/download/) - En su versión estable

VSCode
* [VSCode](https://code.visualstudio.com/download) - Para la edición
    ```
        Agregar los Plugins:
        * OpenApi Swagger
        * npm
        * ReDoc Viewer
    ```

NPM
```
    NOTA: Se tiene que instalar la version que se indica: openapi-cli@0.12.7
```
* [npm] ==>  ```npm install -g @redocly/openapi-cli@0.12.7 ```

* o

* [yarm] ==> ```yarn global add @redocly/openapi-cli@0.12.7 ```


### Instalación 🔧

Clonar el repositorio a su unidad local
Editar de acuerdo a la necesidad del proyecto

### Estructura del Proyecto

_Se indica la estructura del proyecto de API Portal_
  ```
  ├── .redocly.yaml
      ├── LICENSE
      ├── README.md
      ├── docs
      │   ├── favicon.png
      │   └── index.html
      ├── openapi
      │   ├── README.md    
      │   ├── code_samples
      │   │   ├── C#
      │   │   │   └── echo
      │   │   │       └── post.cs
      │   │   ├── PHP
      │   │   │   └── echo
      │   │   │       └── post.php
      │   │   └── README.md
      │   ├── components
      │   │   ├── parameters <---- Se define todas las parámetros globales
      │   |   |   └── traceId.yaml
      │   │   ├── requestBodies <---- Se define ejemplos de entidades en entrada
      │   |   |   └── BuscarClienteReq.yaml
      │   │   ├── responses <---- Se define ejemplos de entidades en Salida
      │   |   |   └── BuscarClienteRes.yaml
      │   │   ├── schemas
      │   │   │   ├── model_request <---- Se define entidades de Entrada
      │   |   |   |   └── BuscarCliente.yaml
      │   │   │   ├── error <---- Se define entidades de respuesta de errores
      │   |   |   |   └── StandarError.yaml
      │   │   │   ├── attributes  <---- Se define entidades del modelo canónico
      │   |   |   |   └── Cliente.yaml
      │   |   |   |   └── Ubigeo.yaml
      │   │   │   ├── model_response <---- Se define entidades de Salida
      │   |   |   |   └── BuscarClienteRes.yaml
      │   │   ├── securitySchemes
      │   │   │   └── sigv4.yaml   
      │   ├── paths
      │   |    └── cliente@consulta.yaml
      │   ├── openapi.yaml <----
      └── package.json
  ```
#### Estructura del Proyecto

![image](https://user-images.githubusercontent.com/58491049/155582293-c6bd943f-24fb-40b2-9c13-8c5f2ffdc03e.png)


## Despliegue 📦

Abrir una nueva terminal dentro del proyecto
* Validar que no presenta errores
    ```
        ruta local...> npm test
    ```
* Construir el archivo unificado OpenApi3
    ```
        ruta local...> npm run build
    ```
* Validar los estandares a través del doSonar (OpenApi3)
    ```
        ruta local...> sonar-scanner
    ```
* Revisar el dasboard del Sonar [Tener VPN Activo]
    ```
        URL: => http://172.29.113.232:10003/dashboard?id=[nombre-de-tu-proyecto]
    ```
* Iniciar el proyecto en el entorno local
    ```
        ruta local...> npm start
    ```
* Navegar en el entorno Local
    ```
        URL: => http://127.0.0.1:80XX
    ```

## Versionado 📌

Usamos [SemVer](http://semver.org/) para el versionado.

### NOTA 📌

Cambiar los valores en:

* openapi.yaml
    ```
        x-rimac-catalog-api-id: [Id-generado-por-gobierno-apis]
    ```
* pipeline_config.groovy
    ```
        file_openapi3: [Id-generado-por-gobierno-apis]
    ```
* sonar-project.properties
    ```
        sonar.projectKey: [nombre-repo-proyecto]
        sonar.projectName: [nombre-repo-proyecto]
    ```

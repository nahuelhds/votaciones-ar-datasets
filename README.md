# Datos Abiertos de las votaciones de Argentina

Este repositorio contiene datasets de las votaciones del Congreso argentino.

Se proveen los archivos en distintos formatos para habilitar su uso por la comunidad.

## Datasets

### Senadores

- [CSV](data/senadores/csv)
- [JSON](data/senadores/json)

### Diputados

- [CSV](data/unificado/csv)
- [JSON](data/unificado/json)
- [MySQL](data/unificado/mysql)
- [SQLite](data/unificado/sqlite)

## Cómo se hizo

Se codificó un bot con la librería [Puppeteer](https://pptr.dev/) el cual ingresa a la página oficial de la HCDN: https://votaciones.hcdn.gob.ar/.

Dicho bot, ingresa a cada uno de los años disponibles y crea un registro por cada ley disponible en dicha página. Luego, ingresa en el detalle de cada una de esas leyes y descarga dicha información.

Teniendo la información de las leyes y las votaciones correspondientes, se procedió a generar una base de datos SQL para sistematizar, normalizar y relacionar toda la información suministrada.

## Motivación

Por interés, diversión, y fundamentalmente porque sí a los [Datos Abiertos](https://es.wikipedia.org/wiki/Datos_abiertos).

Como objetivo ulterior, me interesa realizar minería de datos respecto de cómo vota cada legislador/a, los bloques, entre otras ideas. Sé que existen muchos blogs, analistas, consultoras, pero tenía ganas de poder responder a mis propias preguntas y sacar conclusiones a través del cruce de datos que me habilita tener toda esta información sistematizada.

## Visualizar los datos localmente

Se pueden visualizar los datos a través del docker-compose provisto en el proyecto.

Para poder hacer uso del mismo se necesita tener instalados [docker](https://docs.docker.com/install/) y [docker-compose](https://docs.docker.com/compose/install/).
Con estos requerimientos instalados solo es necesario correr el siguiente comando:

```bash
docker-compose up
```

Luego ingresar a http://localhost:3001 para Grafana y http://localhost:3000 para Metabase
Las credenciales son `admin/admin` y `test@test.test/test123` respectivamente.

En localhost:3306 se encuentra corriendo el MySQL en caso de querer hacer consultas directas con `test/test` como credenciales y `votings` el nombre de la base de datos.

## Pedidos y sugerencias

Por cualquier pedido o sugerencia, [crear un issue en este mismo repositorio](https://github.com/nahuelhds/votaciones-diputados-argentina/issues/new).

## Colaboraciones

Si te interesa colaborar (por ejemplo, subiendo esta misma información en otro formato de utilidad) idealmente podés hacerlo a través de un PR (Pull Request). Si no, contactate conmigo para ver otras formas de recibir las colaboraciones.

## nahuelhds

Segui mi actividad en:

- Medium: [@nahuelhds](http://medium.com/@nahuelhds)
- Twitter: [@nahuelhds](https://twitter.com/nahuelhds)

Si te gusta lo que hago y querés darme una mano:

- Podés [invitarme un café en Ko-Fi](https://ko-fi.com/nahuelhds)
- O también [dándome apoyo en Patreon](https://www.patreon.com/nahuelhds)

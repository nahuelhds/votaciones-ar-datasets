# Votaciones de Diputados Argentina de forma sistematizada

Este repositorio contiene la información sistematizada y normalizada de las votaciones en la Cámara de Diputados desde el año 1993 a la actualidad.

Se proveen los archivos en distintos formatos para habilitar su uso por la comunidad. Así como yo tuve la inquietud y no encontré nada por el estilo, estimo que quizás hayan otras personas que les interese contar con esta información en estos formatos.

## ¿Cómo se hizo?

Se codificó un bot con la librería [Puppeteer](https://pptr.dev/) el cual ingresa a la página oficial de la HCDN: https://votaciones.hcdn.gob.ar/.

Dicho bot, ingresa a cada uno de los años disponibles y crea un registro por cada ley disponible en dicha página. Luego, ingresa en el detalle de cada una de esas leyes y descarga el archivo CSV disponible con el detalle de las votaciones de cada diputado/a.

Teniendo la información de las leyes y las votaciones correspondientes, se procedió a generar una base de datos SQL para sistematizar, normalizar y relacionar toda la información suministrada.

## ¿Por qué?

Por diversión, porque sí a los [Datos Abiertos](https://es.wikipedia.org/wiki/Datos_abiertos) y porque me interesa realizar minería de datos respecto de cómo vota cada legislador/a, los bloques, entre otras ideas. Sé que existen muchos blogs, analistas, consultoras, pero tenía ganas de poder responder a mis propias preguntas y sacar conclusiones a través del cruce de datos que me habilita tener toda esta información sistematizada.

## Jugar con los datos localmente
Para poder jugar un poco con los datos de manera local se provee un docker-compose. Para poder hacer uso del mismo se necesita tener instalado [docker](https://docs.docker.com/install/) y [docker-compose](https://docs.docker.com/compose/install/).
Con estos requerimientos instalados solo es necesario correr el siguiente comando:

```bash
docker-compose up
```

Luego abrir un navegador y apuntar a http://localhost:3001 para Grafana y http://localhost:3000 para Metabase
Las credenciales son `admin/admin` y `test@test.test/test123` respectivamente.

En localhost:3306 se encuentra corriendo el MySQL en caso de querer hacer consultas directas con `test/test` como credenciales y `votings` el nombre de la base de datos.

## Pedidos y sugerencias

Por cualquier pedido o sugerencia, [crear un issue en este mismo repositorio](https://github.com/nahuelhds/votaciones-diputados-argentina/issues/new).

## Colaboraciones

Si te interesa colaborar (por ejemplo, subiendo esta misma información en otro formato de utilidad) idealmente podés hacerlo a través de un PR (Pull Request). Si no, contactate conmigo para ver otras formas de recibir sus colaboraciones. 

# nahuelhds

Segui mi actividad en:
- Medium: [@nahuelhds](http://medium.com/@nahuelhds)
- Twitter: [@nahuelhds](https://twitter.com/nahuelhds)

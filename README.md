# Votaciones Diputados Argentina

Este repositorio contiene la información normalizada, generada con un bot que permitió la sistematización de las votaciones realizadas en la Cámara de Diputados de Argentina desde el año 1993 a la actualidad.

Se proveen los archivos en distintos formatos para habilitar su uso por la comunidad. Así como yo tuve la inquietud y no encontré nada por el estilo, estimo que quizás hayan otras personas que les interese contar con esta información en estos formatos.

## ¿Cómo se hizo?

Se codificó un bot con la librería [Puppeteer](https://pptr.dev/) el cual ingresa a la página oficial de la HCDN: https://votaciones.hcdn.gob.ar/.

Dicho bot, ingresa a cada uno de los años disponibles y crea un registro por cada ley disponible en dicha página. Luego, ingresa en el detalle de cada una de esas leyes y descarga el archivo CSV disponible con el detalle de las votaciones de cada diputado/a.

Teniendo la información de las leyes y las votaciones correspondientes, se procedió a generar una base de datos SQL para sistematizar, normalizar y relacionar toda la información suministrada.

## ¿Por qué?

Por diversión y porque me interesa realizar minería de datos respecto de cómo vota cada legislador/a, los bloques, entre otras ideas. Sé que existen muchos blogs, analistas, consultoras, pero tenía ganas de poder responder a mis propias preguntas y sacar conclusiones a través del cruce de datos que me habilita tener toda esta información sistematizada.

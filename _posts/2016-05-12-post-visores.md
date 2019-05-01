---
layout: post
title: Creando visores con Leaflet
date: 2016-05-12
author: Joan Cano
categories: [leaflet]
tags: [visor, leaflet]
---
## ¿Web mapping?

Siempre que acudimos a un mapa es para visualizar algún elemento del que ya tenemos una idea, hasta una idea de su localización. Este elemento qué estamos buscando se trata de un dato geolocalizado, la mayoría de las veces, un dato que puede estar representado, ¿pero de que manera?.

Una de las funcionalidades que tiene para mí el *web mapping* es que los datos que se están buscando aparecen en un contexto y con una representación cartográfica; **rápido** y **directo**.

Es una manera de transmisión de información eficiente, no, lo siguiente. El poder divulgar, analizar, investigar, utilizarla para ocio, estrategias, geomarketing... se puede representar cualquier cartografía de la forma que se quiera.
¿Cómo puede ser mi mapa?. Si estamos pensando en alojar un mapa en la web puede ser de 3 maneras:
- Que estén ya creados, es decir, serán estáticos como una imagen.
- Que sea un enlace a un visor, desde un servidor Web ó un servicio de mapas como [CARTO](https://carto.com/).
- Un visor embebido en nuestro código.

### Visor 1
Este es de los visores más simples que se pueden crear. El mapa está centrado en Zaragoza y con un punto. Este visor nos permite mostrar la localización de algún lugar que queramos resaltar, que se ubique al primer vistazo. Al igual que se pone un punto, se puede cambiar la geometría o el icono, tamaño.. .

<iframe width="700" height="350" frameborder="0" scrolling="no" marginheight="0" marginwidth="0" src="../static/visor/zaragoza.html" style="border: 1px solid black"></iframe>

### Visor 2
Este visor lo hice durante el curso de piloto de drones que organizan en la base aérea de Zaragoza. Me encontré con el problema de que la cartografía que existe respecto a las zonas aptas para el vuelo son de pago y en papel, ¿de pago?. Bueno, encontré algún archivo .kml que circula por ahí con las zonas de vuelo: [puedes descargarlo de gisandbeers](http://www.gisandbeers.com/radios-y-zonas-de-vuelo-para-drones).

¿Pero qué mejor que un visor propio?. Con un poco de <a href= "http://noticias.juridicas.com/base_datos/Fiscal/537921-l-18-2014-de-15-oct-medidas-urgentes-para-el-crecimiento-la-competitividad.html#t2c1s6lectura">lectura</a> uno puede hacerse idea de las limitaciones y condiciones de vuelo, de manera que te puedes generar tu propia cartografía.

Simplemente es un visor hecho con áreas de influencia, que representan las zonas donde no está permitido volar en Zaragoza; además te permite geolocalizarte con el móvil para saber en todo si estás en "modo seguro".</p><hr>
<iframe width="700" height="350" frameborder="0" scrolling="no" marginheight="0" marginwidth="0" src="../static/visor/rpa.html" style="border: 1px solid black"></iframe>

### Visor 3
El siguiente visor tiene como mapa base un <a href="http://wiki.openstreetmap.org/wiki/MBTiles">MBTiles</a>. Este tipo de formato permite almacenar un mosaicado de imágenes en un solo archivo, como una base de datos SQLite. Me gusta utilizar MBTiles, por que te permite trabajar sin conexión a internet y se mueve fino fino, además del poco espacio que ocupan las tiles si se trabaja en un ámbito reducido.

<iframe width="700" height="450" frameborder="0" scrolling="no" marginheight="0" marginwidth="0" src="../static/visor/mbtiles/mbpolop.html" style="border: 1px solid black"></iframe>

### Visor 4
<p>Muchas veces queremos comparar distintos mapas, ver la superficie contrapuesta con la cartografía que existe, los cambios de una ciudad, mapas temáticos, etc. En este caso he querido hacer una comparación multitemporal de mi pueblo. Para ello se utiliza el servicio WMS del PNOA de máxima actualidad y el vuelo americano de 1956.</p>
<iframe width="700" height="350" frameborder="0" scrolling="no" marginheight="0" marginwidth="0" src="../static/visor/ventanas/windows.html" style="border: 1px solid black"></iframe>

### Visor 5
El otro día tuvimos salida de campo en la asignatura de clasificación de imágenes, para contrarrestar la verdad-terreno de la clasificación no supervisada que estamos realizando. Tomar fotos ayuda a recordar que tipos de cubiertas y especies son las que componen el paisaje, pero la localización de donde están tomadas también es valiosa para utilizarla junto a las fotofrafías en la búsqueda de píxeles que puedan sernos útiles.
La API de Flickr nos permite geolocalizar las fotos e interactuar con ellas mediante Leaflet. Si ya tenemos las fotos geolocalizadas (tomadas con móvil o cámara) podemos geolocalizarlas directamente, y si no queremos geolocalizarlas con Flickr por que tenemos las coordenadas exactas podemos servirnos de software específico; en mi caso utilizo.
<a href="https://www.digikam.org/">Digikam</a><br>
<iframe width="700" height="350" frameborder="0" scrolling="no" marginheight="0" marginwidth="0" src="../static/visor/photo/photos.html" style="border: 1px solid black"></iframe>

### Visor 6
Este es más elaborado. Se trata de un visor que representa la ocupación francesa en Valencia durante los años 1812-13.

<iframe width="800" height="750" frameborder="0" scrolling="no" marginheight="0" marginwidth="0" src="https://joancano.github.io/webMapping/" style="border: 1px solid black"></iframe>

[Full page](https://joancano.github.io/webMapping/)

---
layout: post
title: Creando visores con Leaflet
date: 2016-05-12
author: Joan Cano
categories: [leaflet]
---
## Web mapping

Este es uno de los primeros posts que escribí cuando empecé a aprender web mapping con Leaflet.
A continuación dejo algunos visores que hice como prueba para aprender a montarlos. No he revisado el código desde hace años por lo que seguramente habrán muchas cosas a mejorar. Si vas a utilizar el código, te recomiendo que lo revises.

### Visor 1. Mapa simple

Se trata de un visor sencillo. El mapa está centrado en Zaragoza. El objetivo es mostrar la localización de algún lugar que se quiera resaltar.

<iframe width="700" height="350" frameborder="0" scrolling="no" marginheight="0" marginwidth="0" src="../../visor/zaragoza.html" style="border: 1px solid black"></iframe>

### Visor 2. Zonas de vuelo con dron (Zaragoza)

Este visor lo hice cuando empecé como piloto de drones. Me encontré con el problema de que la cartografía que existía respecto a las zonas aptas para el vuelo eran de pago y en papel. Por suerte había un archivo kml que circulaba por ahí con las zonas de vuelo: [puedes descargarlo de gisandbeers](http://www.gisandbeers.com/radios-y-zonas-de-vuelo-para-drones).

De manera que hice el visor basándome en las áreas del kml y con un poco de <a href= "http://noticias.juridicas.com/base_datos/Fiscal/537921-l-18-2014-de-15-oct-medidas-urgentes-para-el-crecimiento-la-competitividad.html#t2c1s6lectura">legislación. </a>

+ Las áreas de influencia, representan las zonas donde no está permitido volar en Zaragoza
+ Te permite geolocalizarte con el móvil.

<iframe width="700" height="350" frameborder="0" scrolling="no" marginheight="0" marginwidth="0" src="../../visor/rpa.html" style="border: 1px solid black"></iframe>

Actualmente el visor está desactualizado puesto que hay una nueva ley vigente. Además, AESA ya ha creado un visor we para poder comprobar donde se va a operar o volar recreativamente.

### Visor 3. MBTiles

El siguiente visor tiene como mapa base un <a href="http://wiki.openstreetmap.org/wiki/MBTiles">MBTiles</a>. Este tipo de formato permite almacenar un mosaicado de imágenes en un solo archivo, como una base de datos SQLite. Me gusta utilizar MBTiles, por que te permite trabajar sin conexión a internet y se mueve fino fino, además del poco espacio que ocupan las teselas.

<iframe width="700" height="450" frameborder="0" scrolling="no" marginheight="0" marginwidth="0" src="../../visor/mbtiles/mbpolop.html" style="border: 1px solid black"></iframe>

### Visor 4. Slider

Puede surgir la necesidad de comparar distintas cartografías. Ello es muy sencillo en GIS de escritorio, pero cuando además s quiere compartir con muchos usuarios este tipo de visores me parecen perfectos. En este caso se comparan servicios WMS multitemporal de mi pueblo.

<iframe width="700" height="350" frameborder="0" scrolling="no" marginheight="0" marginwidth="0" src="../../visor/ventanas/windows.html" style="border: 1px solid black"></iframe>

### Visor 5. Geo Photos con Flickr

Durante mi máster, tuvimos una salida de campo en la que identificamos diferentes tipos de cubiertas y vegetación. La captura de fotos en campo ayuda a recordar que tipos de cubiertas y especies son las que componen el paisaje, pero sobretodo la localización junto a las fotofrafías ayudaron mucho en la búsqueda de píxeles que puedan ser útiles para la clasificación supervisada.

La API de Flickr nos permite almacenar y geolocalizar las fotos e interactuar con ellas mediante Leaflet. Si ya tenemos las fotos geolocalizadas (tomadas con móvil o cámara) podemos geolocalizarlas directamente, y si no podemos geolocalizarlas con Flickr o un software específico; en mi caso utilizo [Digikam](https://www.digikam.org/)

<iframe width="700" height="350" frameborder="0" scrolling="no" marginheight="0" marginwidth="0" src="../../visor/photo/photos.html" style="border: 1px solid black"></iframe>

### Visor 6. Time and checkbox

Este visor es más elaborado. Se trata de un visor que representa la ocupación francesa en Valencia durante los años 1812-13.

<iframe width="800" height="750" frameborder="0" scrolling="no" marginheight="0" marginwidth="0" src="https://joancano.github.io/webMapping/" style="border: 1px solid black"></iframe>

[Full page](https://joancano.github.io/webMapping/)

---
layout: post
title: fastify-osm
subtitle: Estrarre dati da OpenStreetMap con Fastify
gh-repo: gzileni/fastify-osm
gh-badge: [star, fork, follow]
thumbnail-img: /assets/img/osm_thumb.jpg
share-img: /assets/img/osm_thumb.jpg
tags: [GIS, OverPass, OpenStreetMap, Fastify, NodeJS]
---

**fastify-osm** è un plugin Fastify per estrarre [GeoJSON](https://geojson.org) da query [OverPass](https://overpass-api.de) di [OpenStreetMap](https://www.openstreetmap.org)

Il tool usato per eseguire le query su OpenStreetMap ed estrarre dati in formato mappa o dati è [Overpass Turbo](http://overpass-turbo.eu/). Tramite i wizard è possibile inserire chiavi di ricerca che potranno essere usati come parametri per il plugin **fastify-osm** che genererà la query restituendo i dati in formato GeoJSON.

## Installazione

```bash
npm i fastify-osm
```

## Esempio

```javascript
const fastify = require('fastify')()

fastify.register(require('fastify-osm'))

const bbox = [
  '7.265396118164062',
  '45.687715074360916',
  '7.414398193359375',
  '45.697715074360916'
]

const queries = ['military=airfield', 'highway', 'landuse=industrial']
const buffer = 0.5
const units = 'kilometers'
const response = fastify.osm(bbox, queries, buffer, units)

fastify.listen(3000)
```

i parametri da usare sono i seguenti:

- *bbox*: bbox di coordinate geografiche nel sistema di riferimento OpenStreetMap EPSG:3857 con Longitudine/Latitudine che rappresenterà l'area di ricerca dei punti di interesse sulla mappa
- *queries*: array di tag di punti di interesse per la ricerca
- *buffer*: trasforma il punto di interesse in un poligono con un valore buffer. Se non è indicato i dati saranno esattamenti quelli restituiti da OpenStreetMap
- *unit*: unità di misura del buffer in miglia, kilometri o gradi

Infine `fastify.osm()` restituisce il GeoJSON.
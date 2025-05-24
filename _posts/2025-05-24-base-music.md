---
layout: post
title: Entendiendo Music Ballers
subtitle: Implementación de la solución con el cliente
gh-repo: firgerethical/firgerethical.github.com
gh-badge: [star, fork, follow]
tags: [proyecto, music-ballers, automatización, jekyll, githubpages]
comments: true
author: Ricardo RR
---

{: .box-success}
**Music Ballers** es una solución que desarrollamos para un cliente del sector musical y de reseñas en línea. Nuestro equipo de tres personas se encargó de crear un sistema funcional, automatizado y expandible, usando herramientas de código abierto como **Jekyll**, **GitHub Pages**, **Python**, y APIs como **Google Places** y **Last.fm**.

---

## ¿Qué problema resolvemos?

La meta era clara: facilitar al cliente la administración de su sitio web y blog, integrando una base de datos y flujos automatizados que le permitieran publicar artículos, registrar eventos culturales y musicales de CDMX, y mantener su plataforma activa sin necesidad de intervención técnica constante.

---

## Organización del Blog

Diseñamos una estructura basada en archivos `.md`, donde cada post contiene `title`, `subtitle`, `tags`, y un diseño modular. A través del uso de **etiquetas** y una **estructura fija**, el cliente puede filtrar secciones, activar búsqueda y mantener el orden de su contenido con solo escribir en Markdown.

{: .box-note}
**Cualquier colaborador** puede aportar al proyecto realizando un *commit*, el cual será revisado semanalmente por el equipo del cliente.

---

## Automatización y Base de Datos

Además de los archivos `.md`, implementamos una base de datos local con **PostgreSQL**. A través de **scripts en Python** y una integración con **Google Places API**, automatizamos:

- Recopilación de lugares de música, fiestas y eventos culturales en CDMX.
- Generación automática de posts a partir de esa información.
- Normalización de metadatos y formato estructurado.

---

## Tecnologías Clave

| Tecnología     | Uso principal                                 |
|----------------|-----------------------------------------------|
| Jekyll         | Motor del blog, renderiza los `.md`           |
| GitHub Pages   | Publicación automática del sitio              |
| Python         | Scripts de automatización y manejo de datos   |
| PostgreSQL     | Base de datos local                           |
| Google Places  | Recopilación de lugares y eventos             |
| Last.fm API    | Información de artistas y música              |

---

## Nuestro objetivo

Crear una solución sólida, de bajo mantenimiento y totalmente personalizable. **Music Ballers** ya está en producción y su blog es totalmente funcional, permitiendo una experiencia fluida para editores, colaboradores y lectores.

¡Gracias por leernos!  
— *Ricardo RR*


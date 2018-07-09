---
title:  "Preparando el equipo para Hugo"
slug:   "preparando-el-equipo-para-hugo"
date:   "2018-07-05T05:59:39+02:00"
draft:  false
bigimg: [{src: "img/blog/20180705-cabecera.jpg"}]
apartados: ["Blog"]
etiquetas: ["Git", "GitHub", "Sublime Text 3"]
proyectos: ["MetaBlog"]
---

Antes de lanzarnos sin más a generar sitios web con *Hugo*, conviene que instalemos una serie de herramientas que nos facilitarán la vida: un sistema de control de versiones (*Git* + *GitHub*) y un editor de texto plano (*Sublime Text 3*).
<!--more-->

Tal es el propósito de esta primera entrada del [Proyecto MetaBlog](/proyectos/metablog/), que consistirá en una serie de artículos que documentarán todo el proceso de instalación de *Hugo*, el de la creación del propio sitio web empleando dicho generador y el de la personalización de la plantilla que actualmente estoy utilizando: [Beautiful Hugo](https://themes.gohugo.io/beautifulhugo/).

## Git

El sistema de control de versiones al que personalmente estoy acostumbrado es *Git*, en cuya [web oficial](https://git-scm.com/) podemos encontrar una impresionante cantidad de información de interés. Si es la primera vez que escuchas hablar de *Git* o, en general, de los sistemas de control de versiones, quizá te resulte útil echar un vistazo a su [tutorial](https://try.github.io/).

{{< figure src="/img/blog/20180705-img01.png" width="100%" >}}

La instalación de *Git* en *Windows* no podría ser más sencilla. Hacemos clic en [este enlace](https://git-scm.com/download/win) y automáticamente se descargará la versión más reciente de *Git* (`2.18.0` a la hora de escribir estas líneas).

{{< figure src="/img/blog/20180705-img02.png" width="100%" >}}

Una vez se haya completado la descarga, ejecutamos el archivo e instalamos el programa. Durante el proceso de instalación tenemos que escoger en varios momentos entre distintas opciones. A este respecto, he de comentar que las que vienen marcadas por defecto me parecen adecuadas para una primera toma de contacto con *Git*.

Al completar la instalación tenemos, además, acceso a una terminal de sistema, *Git Bash*, que personalmente es la que utilizo. Si bien es cierto que tenemos que emplear algunos comandos distintos a los podemos encontrar en la que por defecto acompaña a *Windows*, es fácil llevar a cabo la transición de una terminal a otra (puede resultar de ayuda este [listado de comandos](https://ss64.com/bash/)).

{{< figure src="/img/blog/20180705-img03.png" width="100%" >}} 

## GitHub

*GitHub* es una plataforma de desarrollo colaborativo utilizada para almacenar proyectos empleando el sistema de control de versiones *Git*. Podemos encontrar más información en su [web oficial](https://github.com/). Al igual que antes, si es la primera vez que accedes a esta plataforma, convendría que le dedicases unos minutos al tutorial *Hello World*, disponible en [esta página](https://guides.github.com/).

Utilizaremos este portal para subir los archivos fuente que permitirán generar el sitio web, así como para alojar el propio sitio web en sí. Únicamente necesitaremos crear una cuenta de usuario para ello.

{{< figure src="/img/blog/20180705-img04.png" width="100%" >}}

## Sublime Text 3

El dicho "Para gustos los colores" tendría en este apartado la versión "Para gustos los editores de texto plano". En mi caso, los proyectos de programación que he realizado y todo el trabajo con generadores de web estáticas los he llevado a cabo tanto con el antiguo *Sublime Text 2*, como con su más reciente versión: *Sublime Text 3*.

Este editor de texto plano es bastante potente, rápido y la comunidad puede extender sus funcionalidades a través de paquetes. Además, su versión "de prueba" te permite utilizar la herramienta sin restricción alguna durante un período de tiempo ilimitado, con la única pega de aparecer un mensaje cada 20 o 30 veces que salvemos cualquier archivo y que te invita a comprar una licencia.

Nos podemos hacer con él a través de [este enlace](https://www.sublimetext.com/3). Su proceso de instalación es similar 

{{< figure src="/img/blog/20180705-img05.png" width="100%" >}}

Además de cumplir de manera excelente sus labores a la hora de editar cualquier archivo de texto plano, *Sublime Text 3* me encanta como herramienta para trabajar con archivos de tipo *markdown*, que será el formato que vamos a emplear para redactar el contenido de nuestro sitio web. En un futuro no muy lejano tengo pensado escribir un artículo explicando cómo llevar a cabo la configuración de este programa para lidiar de forma agradable con dicho tipo de ficheros.

Y hasta aquí el primer artículo del [Proyecto MetaBlog](/proyectos/metablog/), que deja nuestros equipos a punto para proceder a la instalación de *Hugo* y generar un sitio web.

*P. S. (acerca de la imagen de cabecera):* no vamos a usar tantas herramientas como figuran en la fotografía de [Todd Quackenbush](https://unsplash.com/@toddquackenbush), disponible en [Unsplash](https://unsplash.com/photos/IClZBVw5W5A), pero a las escogidas les vamos a dar un uso continuo.

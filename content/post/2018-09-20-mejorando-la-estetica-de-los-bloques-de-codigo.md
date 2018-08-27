---
title:  "Mejorando la estética de los bloques de código"
slug:   "mejorando-la-estetica-de-los-bloques-de-codigo"
date:   "2018-09-20T05:59:39+02:00"
draft:  false
bigimg: [{src: "img/blog/20180920-cabecera.jpg"}]
apartados: ["Blog"]
etiquetas: ["css"]
proyectos: ["MetaBlog"]
---

Por uno de esos casuales de la vida, me ha dado por revisar el sitio web con el móvil y ha sido entonces cuando he presenciado un horror sin parangón: ¿por qué se ven así mis bloques de código?
<!--more-->

Al parecer, me caracterizo por ser un animal de costumbres y cualquier desviación que me lleve mucho más allá de mi zona de confort me produce hasta angustia. Habitualmente, con los temas para páginas web con los que he trabajado, los bloques de código tienen habilitada la aparición de una barra de desplazamiento horizontal cuando figuran instrucciones de longitud considerable.

Este es un comportamiento que me parece adecuado, ya que incrementa, en mi opinión, la legibilidad de los mencionados bloques de código. Por desgracia, en el tema *Beautiful Hugo* no viene configurado así por defecto, de manera que una instrucción de longitud considerable se llega a dividir en varias líneas, dificultando en exceso la lectura.

Las opciones de estilo para los bloques de código, curiosamente, no están declaradas en el archivo `main.css`, como sería de esperar, sino en un fichero denominado `codeblock.css`, que se encuentra en la ruta `\static\css\` del directorio donde hayamos decidido almacenar localmente nuestro sitio web. Su contenido original es

```css
/* --- Code blocks --- */

.chroma .ln { 
  margin-right: 0.8em; 
  padding: 0 0.4em 0 0.4em; 
}
pre code.hljs {
  padding: 9.5px;
}
```

Tras investigar un rato, he conseguido que aparezca la deseada barra de desplazamiento horizontal añadiendo unas cuantas líneas al anterior archivo, de forma que ahora presenta el siguiente aspecto:

```css
/* --- Code blocks --- */

.chroma .ln { 
  margin-right: 0.8em; 
  padding: 0 0.4em 0 0.4em; 
}
pre code.hljs {
  padding: 9.5px;
}

pre {
    overflow-x: auto;
}

pre code {
    word-wrap: normal;
    white-space: pre;
}
```

El único inconveniente de este enfoque es que solo afecta a los bloques de código escritos usando *fences* y no a los que generamos mediante el *shortcode* `highlight` de *Hugo*. No obstante, como habitualmente no recurro a este último, no he decido indagar más al respecto.

En los próximos artículos del [Proyecto MetaBlog](/proyectos/metablog/) continuaremos con la edición de diversas plantillas del tema *Beautiful Hugo*, para terminar de aprender cómo adaptarlo a nuestro gusto.

*P. S. (acerca de la imagen de cabecera):* ciertamente un paisaje de ensueño el que aparece en la fotografía de [Casey Horner](https://unsplash.com/@mischievous_penguins), disponible en [Unsplash](https://unsplash.com/photos/keRS32_dA7U).
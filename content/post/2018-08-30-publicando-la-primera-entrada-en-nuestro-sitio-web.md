---
title:  "Publicando la primera entrada en nuestro sitio web"
slug:   "publicando-la-primera-entrada-en-nuestro-sitio-web"
date:   "2018-08-30T05:59:39+02:00"
draft:  false
bigimg: [{src: "img/blog/20180830-cabecera.jpg"}]
apartados: ["Blog"]
etiquetas: ["Hugo"]
proyectos: ["MetaBlog"]
---

Tras haber recorrido, en el [Proyecto MetaBlog](/proyectos/metablog/), las seis estaciones del vía crucis asociado al calvario de la instalación de *Hugo* y la personalización del tema *Beautiful Hugo*, llega el momento más anhelado por todos: generar contenido para el sitio web.
<!--more-->

A continuación, examinaremos, con sumo detalle, todo el proceso de elaboración y revisión local de artículos para nuestra página web. Para empezar, me gustaría comentar que, en el apartado de la [guía oficial](https://gohugo.io/getting-started/quick-start/#step-4-add-some-content) asociado a este asunto, se utiliza la combinación de la terminal del sistema y el comando `hugo new` para dar a luz, de manera automática, una nueva entrada en el sitio web.

No obstante, como no podía ser de otra manera y en un acto de la más absurda rebeldía, prefiero llevar a cabo este proceso de forma manual (qué obsesión con el control tengo, ¿verdad?). Si nos fijamos, desde el *explorador de archivos* de *Windows*, en la estructura de nuestra página web (heredada del sitio de ejemplo del tema *Beautiful Hugo*), en el interior del directorio raíz existe una carpeta denominada `\content\`, dentro de la cual residen anidadas otras dos: `\page\` y `\post\`.

Para respetar este esquema, he decidido ubicar todos los artículos del sitio web que se organicen por alguna taxonomía (recordemos que, en [esta entrada](/2018/08/09/configurando-el-tema-beautiful-hugo-ii/), incluso añadimos alguna adicional a las que vienen dadas por defecto con *Hugo*) en la carpeta `\post\`, mientras que el resto irá al directorio `\page\`.

Siguiendo esta lógica, como seguramente la primera entrada que vayamos a publicar en nuestro sitio web será una especie de presentación en su blog, generaremos, utilizando *Sublime Text 3*, un nuevo fichero en la carpeta `\post\`. Este poseerá la extensión `.md`, pues vamos a escribir todos y cada uno de nuestros artículos utilizando el lenguaje de marcado *Markdown*. Para aquellas personas que escuchan por primera vez hablar de él, recomiendo encarecidamente que dediquen unos minutos a completar [este tutorial](https://www.markdowntutorial.com/) sobre el mismo.

La estructura de todo artículo será la que figura acto seguido:

```text
---
Metadatos del artículo.
---

Párrafo (o párrafos) de introducción al artículo.
<!--more-->

Cuerpo del artículo.
```

Al comienzo de cada entrada ubicaremos, delimitada por los caracteres `---`, cierta información relevante (metadatos) acerca de la misma, que suministraremos en la forma de pares `variable: valor`. Las variables disponibles a nuestro alcance vendrán determinadas por el tema que hayamos escogido finalmente para nuestro sitio web, aunque sí que es cierto que algunas de ellas son comunes a la mayoría de los temas (como, por ejemplo, `title`, `date` o `draft`).

Teniendo en cuenta que nuestra página web hace uso del tema *Beautiful Hugo*, y considerando la definición de taxonomías y la personalización del *permalink* que llevamos a cabo en [esta entrada](/2018/08/09/configurando-el-tema-beautiful-hugo-ii/), utilizo siempre el mismo esquema para la cabecera de mis artículos:

```yaml
---
title:
slug:
date:
draft:
bigimg:
apartados:
etiquetas:
proyectos:
---
```

En el caso particular de esta entrada, la anterior cabecera ha quedado como sigue:

```yaml
---
title:  "Publicando la primera entrada en nuestro sitio web"
slug:   "publicando-la-primera-entrada-en-nuestro-sitio-web"
date:   "2018-08-30T05:59:39+02:00"
draft:  false
bigimg: [{src: "img/blog/20180830-cabecera.jpg"}]
apartados: ["Blog"]
etiquetas: ["Hugo"]
proyectos: ["MetaBlog"]
---
```

Veamos a continuación el cometido de cada una de las variables que figuran en la cabecera:

- `title`: contiene el título del artículo. A diferencia de otros temas, por desgracia *Beautiful Hugo* no admite la posibilidad de emplear *Markdown* o *LaTeX* en ciertas partes del título, hecho que debemos tener en consideración.
- `slug`: tal y como comentamos en [esta entrada](/2018/08/09/configurando-el-tema-beautiful-hugo-ii/), vamos a configurar manualmente el *permalink* de cada entrada. Una de sus partes será, precisamente, la asociada a esta variable. Para generar su valor, sustituyo a mano los espacios por guiones y suprimo cualquier acento, eñe o carácter extraño a los ojos del alfabeto inglés que pudiese figurar en el título del artículo. En particular, para esta entrada, el *permalink* será `/2018/08/30/publicando-la-primera-entrada-en-nuestro-sitio-web/`, es decir, la fecha de publicación junto al valor que hemos asignado a la variable `slug`.
- `date`: fecha y hora de publicación del artículo. Me gustaría comentar aquí que nada nos impide generar contenido para fechas futuras, aunque cuando escribamos en la terminal del sistema `hugo server`, no tendremos acceso a su revisión. Para solventar esta situación, tenemos que añadir la etiqueta `-F`, es decir, teclear `hugo server -F`.
- `draft`: variable que nos permite indicar si la entrada en concreto tiene carácter de borrador (utilizando el valor `true`) o si ya está lista para su publicación en nuestro sitio web (empleando el valor `false`). Para revisar localmente una página web que contenga artículos en forma de borrador, hemos de escribir en la terminal del sistema `hugo server -D`.
- `bigimg`: esta variable nos permite insertar la ruta hacia una imagen de cabecera para nuestros artículos. En [esta entrada](/2018/08/09/configurando-el-tema-beautiful-hugo-ii/) está explicado en detalle el funcionamiento de esta característica particular del tema *Beautiful Hugo*.
- `apartados`: primera taxonomía que utilizaremos para agrupar contenido según la categoría a la que pertenezca el artículo. No es más que la localización al español de la habitual `categories`.
- `etiquetas`: segunda taxonomía que utilizaremos para agrupar contenido según las palabras clave que caractericen a la entrada. No es más que la localización al español de la habitual `tags`.
- `proyectos`: tercera taxonomía (generalmente opcional) que nos permitirá agrupar contenido que pertenezca a distintos apartados y posea diferentes etiquetas.

Tras declarar la cabecera, redactaremos un párrafo (o varios) de introducción al artículo, tras los cuales escribiremos la instrucción `<!--more-->`. Dichos párrafos, además de ser aquellos que den comienzo a nuestra entrada, serán los que figuren en las páginas de listado de nuestro sitio web. ¿A qué me refiero con las páginas de listado? Serían, por ejemplo, la principal de acceso al sitio web y todas aquellas que ofrecen un índice que contiene los artículos asociados a una taxonomía en particular.

Tras la instrucción `<!--more-->`, finalmente, ya solo nos restará explayarnos tanto como deseemos en el cuerpo de la entrada. *The sky is the limit!*

*P. S. (acerca de la imagen de cabecera):* llegados a este punto, por fin estamos en condiciones de generar una ingente cantidad de contenido para nuestro sitio web. Simplemente hemos de armanos de papel y pluma, tal y como aparece en la fotografía de [Aaron Burden](https://unsplash.com/@aaronburden), disponible en [Unsplash](https://unsplash.com/photos/xG8IQMqMITM), y dar rienda suelta a nuestra imaginación.
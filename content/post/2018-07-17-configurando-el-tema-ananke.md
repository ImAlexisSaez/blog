---
title:  "Configurando el tema Ananke"
slug:   "configurando-el-tema-ananke"
date:   "2018-07-17T05:59:39+02:00"
draft:  false
bigimg: [{src: "img/blog/20180717-cabecera.jpg"}]
apartados: ["Blog"]
etiquetas: ["Hugo", "Ananke"]
proyectos: ["MetaBlog"]
---

En la [anterior entrada](/2018/07/11/creando-un-sitio-web-con-hugo/) generamos, ¡solucionando incluso un pequeño *bug*!, nuestro primer sitio web con *Hugo*, utilizando para ello el tema *Ananke*. Veamos qué opciones de configuración nos ofrece dicho tema a continuación.
<!--more-->

Así pues, dedicaremos única y exclusivamente este cuarto artículo del [Proyecto MetaBlog](/proyectos/metablog/) a examinar con detalle el contenido del archivo `config.toml`, que se ubica en la raíz del directorio donde hayamos decidido almacenar nuestro sitio web.

Si en su momento nos decantamos por seguir, al pie de la letra, el contenido de la [anterior entrada](/2018/07/11/creando-un-sitio-web-con-hugo/), dicho fichero debería figurar en el interior de la ruta `C:\Hugo\Sites\prueba`. Desde el *explorador de archivos* de *Windows*, lo seleccionamos con el botón derecho del ratón y escogemos la opción `Open with Sublime Text`.

Parte de su contenido nos resultará familiar a estas alturas, pues ya tuvimos que editar el mencionado archivo para solventar el *bug* que nos impedía tener acceso local al sitio web. Empecemos examinando el primer bloque de código, aquel que comprende las siguientes cinco líneas:

{{< highlight toml >}}
title = "Notre-Dame de Paris"
baseURL = "https://example.com"
languageCode = "en-us"
theme = "gohugo-theme-ananke"
# themesDir = "../.."
{{< / highlight >}}

Estamos ante una serie de pares `variable = valor`, en donde hemos de personalizar las cadenas de texto para que se ajusten a las opciones que deseamos de cara a nuestro sitio web. 

En el primero de ellos, la variable `title`, como bien señala de manera descriptiva su nombre, nos permite indicar el título de la página web. En mi caso, me gustaría que fuese *Infinitos Contrastes*, por lo que no tengo más que modificar esa primera línea y teclear `title = "Infinitos Contrastes"`.

Ahora, a `baseURL` hemos de asignarle el enlace que utilizaremos para acceder a nuestro sitio web a través del navegador web. Dado que la idea es que alojemos la página web en *GitHub*, dicha dirección será del estilo `https://<NOMBRE_DE_TU_CUENTA>.github.io`. Para ilustrar esto último de manera más concreta, el nombre de mi cuenta en *GitHub* es `ImAlexisSaez`, por lo que el enlace que permitirá el acceso remoto a la página web será `https://imalexissaez.github.io/`, valor que asignaré a la variable `baseURL` en su correspondiente línea.

A continuación, en `languageCode` reside el código del lenguaje en el que se generará nuestro sitio web, que, por defecto, es inglés estadounidense (`en-us`). Si vamos a generar contenido un idioma diferente, conviene que modifiquemos el valor de dicha línea. Para el español, el código asociado es `es`.

Aunque a primera vista no parezca un detalle relevante, es importante asignar el código adecuado a `languageCode`, puesto que algunos temas de *Hugo* incorporan la posibilidad de localización a diferentes lenguajes y la clave pasa, precisamente, por el valor indicado para dicha variable. Para muestra, un botón: el tema actual de este sitio web, *Beautiful Hugo*, es uno de esos ejemplos y en un futuro veremos cómo lidiar con el asunto de la localización en *Hugo*.

La siguiente línea, `theme = "gohugo-theme-ananke"`, le indica a *Hugo* en qué ruta ha de buscar para acceder a los archivos correspondientes al tema de la web. Es posible que en la [anterior entrada](/2018/07/11/creando-un-sitio-web-con-hugo/) no nos diésemos cuenta, pero cuando instalamos el tema *Ananke* automáticamente se generó una carpeta en nuestro disco duro llamada `gohugo-theme-ananke`, en el interior del directorio `themes`. La variable `theme` simplemente apunta a esa ruta, de manera que si, por el extraño motivo que sea, nos vemos en la necesidad de modificar el nombre de la mencionada carpeta, también deberíamos cambiar el valor de esta línea en el archivo `config.toml`.

Por lo que respecta a la última línea de este bloque de código, para solventar el *bug* que nos impedía revisar localmente el sitio web, usamos el símbolo de comentario (`#`) para anularla. De esta forma, directamente podemos suprimirla, quedando definitivamente:

{{< highlight toml >}}
#
# Configuración básica del sitio web
#
title        = "Infinitos Contrastes"             # Título
baseURL      = "https://imalexissaez.github.io/"  # Enlace de entrada
languageCode = "es"                               # Idioma
theme        = "gohugo-theme-ananke"              # Ruta al tema
{{< / highlight >}}

Recomiendo encarecidamente ir comentando el código fuente, para que en futuras revisiones sea más fácil encontrar aquello que andemos buscando. En cuanto a que todo quede alineado por el símbolo `=`, es simplemente una manía mía, no es necesario en absoluto.

Pasemos ahora al siguiente bloque de código, el dado por 

{{< highlight toml >}}
MetaDataFormat = "yaml"
DefaultContentLanguage = "en"
SectionPagesMenu = "main"
Paginate = 3 # this is set low for demonstrating with dummy content. Set to a higher number
googleAnalytics = ""
enableRobotsTXT = true
{{< / highlight >}}

En mi caso, ha quedado como sigue:

{{< highlight toml >}}
#
# Configuración adicional del sitio web
#
MetaDataFormat         = "yaml" # Formato cabeceras
DefaultContentLanguage = "es"   # Idioma por defecto del contenido
SectionPagesMenu       = "main" #
Paginate               = 3      # Posts por página en main
googleAnalytics        = ""     # Código para estadísticas web
enableRobotsTXT        = true   # Buscadores
{{< / highlight >}}

ya que:

- En `MetaDataFormat` tenemos que indicar qué lenguaje emplearemos para escribir los metadatos de las cabeceras para nuestros artículos del sitio web (hablaremos de ello en detalle cuando, por fin, nos animemos a redactar el primer artículo para nuestra página web). *Hugo* permite trabajar con *TOML* (por defecto), *YAML* y *JSON*. Los dos primeros son muy similares y, en mi caso, dado que estuve un tiempo generando el sitio web con *Jekyll*, estoy más acostumbrado al estilo *YAML* que al *TOML*. Por otro lado, aunque también es factible generar las mencionadas cabeceras con *JSON*, es un lenguaje un tanto más tedioso a la hora de declarar los metadatos, por lo que recomendaría evitarlo de momento.
- Para `DefaultContentLanguage` declaramos el valor del código del idioma en el que tengamos pensado generar el contenido para nuestro sitio web. Para español, recuerdo que dicho código era `es`.
- Confieso que desconozco las posibilidades para `SectionPagesMenu`. Experimenté con el tema *Ananke* unos minutos y enseguida empecé a buscar, entre los temas disponibles para *Hugo*, uno que se adaptara mejor a mis necesidades, así que no he profundizado en exceso en este.
- En `Paginate` indicaremos el número de artículos que queremos se muestren por página en el índice que aparece al acceder a nuestro sitio web. En los propios comentarios avisan que el valor asignado por defecto, `3`, es un tanto escaso y deberíamos incrementarlo un tanto. ¿Cuánto? En mi opinión, debería estar en función de la frecuencia con la que generemos contenido.
- Si activamos las estadísticas de *Google* para nuestro sitio web, tendremos acceso a cierto código, que será el que asignemos como valor en la línea de `googleAnalytics`.
- Finalmente, con `enableRobotsTXT = true` damos acceso a la "arañas" de los buscadores para que exploren todo nuestro sitio web e indexen aquello que estimen conveniente.

El siguiente bloque de código:

{{< highlight toml >}}
[sitemap]
  changefreq = "monthly"
  priority = 0.5
  filename = "sitemap.xml"
{{< / highlight >}}

está dedicado a los parámetros de configuración del mapa del sitio web. Al igual que sucedía con la variable `Paginate`, configuraremos los valores de estas tres en función de la frecuencia con la que generemos contenido para nuestro sitio web. Seguramente, la única variable que modificaremos será `changefreq`, cambiando `"monthly"` por `"wekly"` o, incluso, `"daily"`.

Así pues, en mi caso, únicamente he colocado un comentario introductorio al bloque y, por supuesto, he continuado alineando valores por el simbolo `=`:

{{< highlight toml >}}
#
# Configuración del mapa de la web
#
[sitemap]
  changefreq = "monthly"
  priority   = 0.5
  filename   = "sitemap.xml"
{{< / highlight >}}

Para finalizar, el último bloque de código:

{{< highlight toml >}}
[params]
  favicon = ""
  description = "The last theme you'll ever need. Maybe."
  facebook = ""
  twitter = "https://twitter.com/GoHugoIO"
  instagram = ""
  youtube = ""
  github = ""
  linkedin = ""
  # choose a background color from any on this page: http://tachyons.io/docs/themes/skins/ and preface it with "bg-"
  background_color_class = "bg-black"
  featured_image = "/images/gohugo-default-sample-hero-image.jpg"
  recent_posts_number = 2
{{< / highlight >}}

me ha quedado

{{< highlight toml >}}
#
# Configuración de parámetros de la web
#
[params]
  favicon     = ""
  description = "Laboratorio de experimentos de un matemático"
  facebook    = ""
  twitter     = "https://twitter.com/GoHugoIO"
  instagram   = ""
  youtube     = ""
  github      = ""
  linkedin    = ""
  background_color_class = "bg-black"
  featured_image         = "/images/gohugo-default-sample-hero-image.jpg"
  recent_posts_number    = 2
{{< / highlight >}}

Estas líneas facilitan la configuración de algunas características de la web, como pueden ser:

- `favicon`: es el icono que aparece, en el navegador, en la parte izquierda de la pestaña correspondiente a nuestro sitio web. El valor que hemos de asignar a esta variable será la ruta de acceso a la imagen que contiene el icono. Entraré en más detalles al respecto de este tema cuando aborde cómo configurar el *favicon* para el tema *Beautiful Hugo*.
- `description`: breve subtítulo o eslogan que podemos añadir a la página web.
- `facebook`, `twitter`, etc.: enlaces a las páginas de nuestras redes sociales, que permiten a los visitantes dar con nuestros perfiles muy fácilmente.
- `featured_image`: ruta que apunta a la imagen que deseemos ubicar en la cabecera de nuestra página web.
- `recent_posts_number`: cantidad de artículos, de entre los últimos publicados, que aparecerán destacados en la página de entrada a nuestro sitio web.

En esta serie de artículos no entraré en detalle en la modificación de las plantillas del tema *Ananke*. No obstante, en breve pasaremos a estudiar con profundidad el tema *Beautiful Hugo* y las ideas que exploremos, de cara a modificar diversos aspectos de un sitio web, se podrán extrapolar a cualquier tema, *Ananke* incluido.

Así pues, seguramente, en la próxima entrada del [Proyecto MetaBlog](/proyectos/metablog/) instalaremos el tema *Beautiful Hugo* y echaremos un vistazo por encima a su correspondiente archivo de configuración `config.toml`.

*P. S. (acerca de la imagen de cabecera):* me encanta a veces simplemente navegar y encontrar perlas como la fotografía de [Kalen Emsley](https://unsplash.com/@kalenemsley), disponible en [Unsplash](https://unsplash.com/photos/_LuLiJc1cdo).

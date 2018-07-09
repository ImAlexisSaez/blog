---
title:  "Creando un sitio web con Hugo"
slug:   "creando-un-sitio-web-con-hugo"
date:   "2018-07-11T05:59:39+02:00"
draft:  false
bigimg: [{src: "img/blog/20180711-cabecera.jpg"}]
apartados: ["Blog"]
etiquetas: ["Hugo"]
proyectos: ["MetaBlog"]
---

¡Ha llegado el momento que todos estábamos esperando! Tras un par de artículos en los que hemos preparado nuestros equipos instalando las herramientas necesarias, hoy veremos cómo generar nuestro primer sitio web con *Hugo*.
<!--more-->

Esta tercera entrada del [Proyecto MetaBlog](/proyectos/metablog/) se va a apoyar en la guía de inicio recogida en la documentación oficial de *Hugo*, a la que podemos acceder a través de [este enlace](https://gohugo.io/getting-started/quick-start/).

En primer lugar, abrimos la terminal *Git Bash* y nos dirigimos al directorio de nuestro disco duro donde tengamos pensado almacenar localmente el sitio web. En la mencionada guía recomiendan ubicar las páginas en la ruta `C:\Hugo\Sites\`, aunque ya comenté en la [anterior entrada](/2018/07/08/instalando-hugo-en-windows/) que no era estrictamente necesario proceder de tal forma.

Dicho esto, en este artículo seguiremos al dedillo las indicaciones dadas en la guía, de manera que en la terminal tecleamos:

{{< highlight bash >}}
cd c:/Hugo/Sites/
{{< / highlight >}}

El comando para generar un nuevo sitio web es `hugo new site [path] [flags]`, donde sustituiremos `[path]` por la ruta al directorio donde almacenaremos nuestra página web. Por lo que respecta a las `[flags]`, en el apartado de la documentación oficial dedicado a [hugo new site](https://gohugo.io/commands/hugo_new_site/) tenemos el listado de las disponibles. No obstante, para una primera toma de contacto, no añadiremos ninguna de ellas.

Así pues, generemos un primer sitio de prueba y, en un alarde de extrema originalidad, ubiquémoslo en el directorio `\prueba\`. Para ello, escribimos en la terminal:

{{< highlight bash >}}
hugo new site prueba
{{< / highlight >}}

Recibimos entonces un mensaje de felicitación (en caso contrario, convendría que revisáramos la instalación de *Hugo* siguiendo las indicación de [esta entrada](/2018/07/08/instalando-hugo-en-windows/)) y algunas instrucciones relacionadas con el uso de temas, la creación de contenidos y el acceso local del sitio web.

*Hugo* ha creado el directorio `\prueba\` en el interior de la ruta donde hemos ejecutado el comando `hugo new site`. Además, ha poblado el mismo con algunas carpetas (vacías en su mayor parte), quedando una estructura como la que figura en la siguiente imagen:

{{< figure src="/img/blog/20180711-img01.png" width="100%" >}}

En un futuro exploraremos con detalle el cometido de algunos de esos directorios que aparecen en la imagen (`\content\` y `\layouts\` son de extrema importancia, así como ese curioso archivo denominado `config.toml`). No obstante, por el momento, evitemos distraernos en exceso y sigamos las indicaciones de la guía.

Volvemos a la terminal, nos movemos hacia el directorio `\prueba\` e iniciamos un repositorio *Git*, acciones que requieren teclear los dos siguientes comandos:

{{< highlight bash >}}
cd prueba
{{< / highlight >}}

{{< highlight bash >}}
git init
{{< / highlight >}}

En el siguiente paso de la guía nos invitan a instalar un tema para la web, [Ananke](https://themes.gohugo.io/gohugo-theme-ananke/), utilizando `submodule` (un comando de *Git*). No obstante, en este momento, me voy a desviar de las indicaciones dadas y optar por un método diferente de instalación de temas. A continuación, nos moveremos a la carpeta `\themes\` y clonaremos en nuestro disco duro el propio repositorio del tema. Para ello, escribimos en la terminal:

{{< highlight bash >}}
cd themes
{{< / highlight >}}

{{< highlight bash >}}
git clone https://github.com/budparr/gohugo-theme-ananke.git
{{< / highlight >}}

De esta manera, tenemos acceso localmente a un sitio web de prueba, con un poco de contenido ya generado, que nos permitirá hacernos una idea del aspecto final de nuestro sitio web utilizando el tema *Ananke*. Aunque soy consciente de que me estoy desviando "ligeramente" de la guía oficial, vamos tomar esta senda para ver cómo luce nuestro sitio web.

Abrimos el explorador de archivos de *Windows* y en el directorio donde hemos ubicado la página web (`C:\Hugo\Sites\prueba\`) accedemos a la carpeta `themes`. Una vez dentro de ella, hacemos doble clic sobre el directorio `gohugo-theme-ananke` y repetimos luego la acción con la carpeta denomiada `exampleSite`, cuyos contenidos son:

{{< figure src="/img/blog/20180711-img02.png" width="100%" >}}

Copiamos tanto las dos carpetas, como el archivo `config.toml`, y pegamos en el directorio `C:\Hugo\Sites\prueba\`, reemplazando los ficheros existentes con el mismo nombre que en él se encuentran. 

Ahora volvemos a la terminal, todavía apuntando a la carpeta `\themes\` y tecleamos

{{< highlight bash >}}
cd ...
{{< / highlight >}}

para volver al directorio raíz de nuestro sitio web. A continuación, para revisar el sitio web localmente escribimos

{{< highlight bash >}}
hugo server
{{< / highlight >}}

y, para mi sorpresa, recibimos el siguiente mensaje de error `Error: Unable to find theme Directory: C:\Hugo\gohugo-theme-ananke`, hecho que debe ser el *karma* haciendo acto de presencia por haberme desviado de las indicaciones de la guía oficial.

Aunque no quería meterme en este artículo en el contenido del archivo `config.toml`, para evitar ofrecer mucha información de golpe, solucionemos rápidamente este pequeño *bug* para así poder revisar localmente el sitio web. Hacemos clic derecho sobre el mencionado fichero y lo abrimos con *Sublime Text*. Modificamos la quinta línea que aparece, de

{{< highlight toml >}}
themesDir = "../.."
{{< / highlight >}}

a

{{< highlight toml >}}
# themesDir = "../.."
{{< / highlight >}}

y guardamos los cambios. 

Volvemos ahora a la terminal y tecleamos de nuevo

{{< highlight bash >}}
hugo server
{{< / highlight >}}

Tras recibir cierta información sobre el sitio, únicamente nos resta abrir nuestro navegador web favorito y en la barra de direcciones escribir `http://localhost:1313/`, accediendo así a la página de bienvenida de nuestro sitio web, que luce así de bien:

{{< figure src="/img/blog/20180711-img03.png" width="100%" >}}

Es el momento de navegar por la página, estudiar si nos complace estéticamente y comprobar si la manera en la que se organizan los contenidos es la apropiada para el sitio web que teníamos en mente. Cuando hayamos terminado el paseo, volvemos a la terminal y cerramos el servidor local utilizando la combinación de teclas `Ctrl + C`.

En el próximo artículo del [Proyecto MetaBlog](/proyectos/metablog/) exploraremos, ahora sí y con mucho más detalle, la configuración básica del sitio web, que reside en el fichero `config.toml`.

*P. S. (acerca de la imagen de cabecera):* dicen que una configuración con dos monitores, como la que aparece la fotografía de [Lee Campbell](https://unsplash.com/@leecampbell), disponible en [Unsplash](https://unsplash.com/photos/DtDlVpy-vvQ), aumenta enormemente la productividad. En mi caso, temo que sería una fuente constante de distracciones.

---
title:  "Configurando Sublime Text para escribir en Markdown"
slug:   "configurando-sublime-text-para-escribir-en-markdown"
date:   "2018-07-10T05:59:39+02:00"
draft:  false
bigimg: [{src: "img/blog/20180710-cabecera.jpg"}]
apartados: ["Blog"]
etiquetas: ["Sublime Text 3", "Markdown"]
---

En una [entrada publicada](/2018/07/05/preparando-el-equipo-para-hugo/) hace unos días comenté que utilizo el editor de texto plano *Sublime Text 3* como herramienta predeterminada para escribir documentos con *Markdown*. Veamos cómo configurarlo para abordar tal empresa.
<!--more-->

Sinceramente, tal y como por defecto instalamos el mencionado programa, podríamos trabajar sin problema alguno con este lenguaje de marcado ligero, ya que únicamente requiere un editor de texto plano para su elaboración y posteriores modificaciones.

No obstante, existe un paquete que mejora la experiencia de edición de manera considerable: `Markdown Editing`. Al abrir cualquier fichero redactado utilizando el mencionado lenguaje de marcado, su contenido se centra en pantalla, facilitando así enormemente su lectura. Además, elementos como títulos, cursivas, negritas, enlaces o código quedan resaltados de forma muy agradable.

Para muestra, un botón:

{{< figure src="/img/blog/20180710-img01.png" width="100%" >}}

Si a todo ello le añadimos el modo sin distracciones que incorpora *Sublime Text 3*, al que se accede mediante la combinación de teclas `Shift + F11`, el resultado es una cómoda herramienta que permite generar documentos con *Markdown* eficientemente.

El procedimiento a seguir es el habitual a la hora de incorporar un nuevo paquete a *Sublime Text 3*:

1. Si todavía no tenemos el complemento que permite instalar paquetes fácilmente, abrimos [este enlace](https://packagecontrol.io/installation) y copiamos el bloque de instrucciones que figura en el cuadro asociado a la versión de *Sublime Text* que utilicemos (a día de hoy, seguramente, será la 3).
2. Abrimos la consola de *Sublime Text 3*, haciendo clic en el apartado `Show Console` del menú `View` (o utilizando su atajo de teclado asociado). En la ventana que aparece dentro del editor, pegamos el texto copiado durante el primer paso y pulsamos enter.
3. Hacemos uso ahora del atajo de teclado `Ctrl + Shift + P` y empezamos a escribir `install`, hasta que quede resaltada la opción `Package Control: Install Package` y después pulsamos enter.
4. A continuación, comenzamos a escribir `markdown` y utilizamos los cursores para seleccionar el paquete `MarkdownEditing`, pulsando de nuevo enter una vez lo hayamos conseguido.

De esta forma, basta ahora con que abramos en *Sublime Text 3* cualquier archivo escrito con *Markdown* y experimentaremos los cambios estéticos que comentaba al principio de este artículo. 

Personalmente, el esquema de colores que este paquete incorpora por defecto no me hace excesiva ilusión, acostumbrado como estoy a *Monokai*. Sin embargo, podemos seleccionar un tema oscuro desde el menú `Preferences`, apartado `Package Settings`, subapartado `Markdown Editing`, accediendo a `Change color scheme...` y escogiendo la opción `Dark`.

Finalmente, por si fuera de interés, me gustaría destacar que también existen diversos paquetes que ofrecen la opción de previsualizar el documento que estamos redactando y refrescar el resultado cuando llevamos a cabo cualquier tipo de edición en él. No he entrado en detalles sobre ellos en este artículo simplemente porque utilizo un método diferente para llevar a cabo las mencionadas acciones.

*P. S. (acerca de la imagen de cabecera):* una herramienta para escribir, como la que aparece en la fotografía de [Patrick Fore](https://unsplash.com/@patrickian4), disponible en [Unsplash](https://unsplash.com/photos/0gkw_9fy0eQ), junto a unas cuantas ideas, garantiza más de tarde de entretenimiento.
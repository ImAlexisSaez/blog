---
title:  "¿Cómo dividir diagonalmente una celda de una tabla con LaTeX?"
slug:   "como-dividir-diagonalmente-una-celda-de-una-tabla-con-latex"
date:   "2018-07-20T05:59:39+02:00"
draft:  false
bigimg: [{src: "img/blog/20180720-cabecera.jpg"}]
apartados: ["Blog"]
etiquetas: ["LaTeX"]
---

Reconozco que la edición de tablas, junto con la gestión de figuras, a veces se convierte en una pequeña pesadilla para mí cuando estoy generando documentos con *LaTeX*. Veamos cómo he dado respuesta a la cuestión que aparece en el título de esta entrada.
<!--more-->

Es habitual en estadística que trabajemos con tablas de contingencia, sobre todo en su versión $2\times 2$. Estas se suelen caracterizar por tener la celda que ocupa la esquina superior izquierda dividida diagonalmente, de manera que el texto inferior de dicha celda hace referencia al contenido de las filas (por ejemplo, si se posee o no cierta enfermedad), mientras que el texto superior hace lo propio para las columnas (por ejemplo, si se está expuesto a un factor de riesgo o no).

Ahora bien, enseguida aparece la pregunta del millón: ¿cómo conseguimos ese efecto con *LaTeX*? La respuesta viene de la mano del paquete `slashbox`, cuyo uso es realmente sencillo. Veamos un ejemplo de aplicación:

{{< highlight tex >}}
\documentclass{article}
 
\usepackage[utf8]{inputenc}
\usepackage[english, spanish]{babel}
 
\usepackage{slashbox}
 
\begin{document}
 
\begin{tabular}{|l|c|c|c|}
\hline
\backslashbox{Enfermedad}{Factor de riesgo} & SÍ $\equiv FR$ & NO $\equiv \overline{FR}$ & Totales\\
\hline
SÍ $\equiv E$ & $O_{11}$ & $O_{12}$ & $F_1$ \\
NO $\equiv \overline{E}$ & $O_{21}$ & $O_{22}$ & $F_2$ \\
\hline
Totales & $C_1$ & $C_2$ & $T$ \\
\hline
\end{tabular}
 
\end{document}
{{< / highlight >}}

Podemos apreciar el resultado en la siguiente imagen:

{{< figure src="/img/blog/20180720-img01.png" width="100%" >}}

*Referencias*:

- [LaTeX table cell with a diagonal line and 2 sub cells [duplicate]](http://tex.stackexchange.com/questions/27193/latex-table-cell-with-a-diagonal-line-and-2-sub-cells).
- [Diagonally divided table cell [duplicate]](http://tex.stackexchange.com/questions/7262/diagonally-divided-table-cell).

*P. S. (acerca de la imagen de cabecera):* cuando al compilar con *LaTeX* sale una miríada de errores, me dan ganas de dejar el escritorio tal y como aparece en la fotografía de [Jesus Kiteque](https://unsplash.com/@jesuskiteque), disponible en [Unsplash](https://unsplash.com/photos/wn-KYaHwcis), y alejarme tanto como pueda.
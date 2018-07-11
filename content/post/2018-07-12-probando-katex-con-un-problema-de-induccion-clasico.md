---
title:  "Probando KaTeX con un problema de inducción clásico"
slug:   "probando-katex-con-un-problema-de-induccion-clasico"
date:   "2018-07-12T05:59:39+02:00"
draft:  false
bigimg: [{src: "img/blog/20180712-cabecera.jpg"}]
apartados: ["Oposiciones"]
etiquetas: ["Inducción"]
proyectos: ["Problemas"]
---

Demuestra que 
$$
1+2+\cdots+n = \dfrac{n(n+1)}{2},
$$ 
para cada $n\in\mathbb{N}$ con $n\geq 1$.
<!--more-->

***

Consideremos pues la propiedad, $P(n)$, dada en el enunciado 
$$
1+2+\cdots+n = \dfrac{n(n+1)}{2}
$$ 
y utilicemos el *principio de inducción matemática* para estudiar si se verifica para cada $n\in\mathbb{N}$ con $n\geq1$. 

El caso base, $P(1)$, se cumple trivialmente, ya que 
$$
1 = \dfrac{1\cdot2}{2} = 1.
$$ 

Ahora, mostremos que si $P(n)$ es cierta, con $n\geq1$, entonces asimismo lo es $P(n+1)$, esto es, que se verifica que 
$$
1+2+\cdots+n+(n+1)=\dfrac{(n+1)(n+2)}{2}.
$$

Podemos reescribir el miembro izquierdo de la anterior ecuación, aplicando $P(n)$, como sigue
$$
1+2+\cdots+n+(n+1) = \dfrac{n(n+1)}{2} + (n+1)
$$
y, operando,
$$
\dfrac{n(n+1)}{2} + (n+1) = \dfrac{n(n+1) + 2(n+1)}{2} = \dfrac{(n+1)(n+2)}{2},
$$
mostrando así que $P(n+1)$ es cierta. Así pues, por el *principio de inducción matemática*, $P(n)$ se verifica para cada $n\in\mathbb{N}$, con $n\geq 1$.

***

Podría decir que la experiencia de usar *KaTeX* ha sido un tanto agridulce. La mayor parte del artículo procede de código fuente escrito en *TeX* y apenas he tenido que llevar cambio alguno en el código para que fuera interpretado correctamente por *KaTeX*, hecho ciertamente positivo. No obstante, no he sido capaz de trabajar con los entornos que, según la [web oficial](https://khan.github.io/KaTeX/function-support.html), están disponibles, como por ejemplo `aligned` o `pmatrix`. Esto, en ocasiones, temo que vaya a dificultar la narrativa o incluso a impedir la publicación de ejemplos que requieran estructuras matriciales.

Seguiré investigando, ya que me gustaría ir publicando habitualmente problemas matemáticos sin tener que recurrir a la clásica solución de compartirlos en formato `PDF` vía algún servicio de alojamiento de ficheros.

*Actualización:* tras un descanso para aclarar ideas, ¡por fin he dado con la solución al problema de los entornos! Si escribimos

```tex
$$
x = 
\begin{cases}
  a &\text{if } b\\
  c &\text{if } d
\end{cases}
$$
```

el resultado no se visualiza correctamente, y así sucede para cualquier entorno que requiera cambios de línea, como `aligned`, `pmatrix`, etc. La clave reside en el tratamiento que recibe en *Markdown* el carácter `\`, que interfiere con el funcionamiento adecuado de *KaTeX*.

La solución pasa por "escapar" el mencionado carácter, de manera que, si habitualmente necesitamos dos para comenzar una nueva línea, ahora tendríamos que teclear cuatro. Además, en ocasiones, según el entorno que vayamos a emplear, es posible que debamos sacrificar las sangrías y escribir todo medianamente seguido.

Es decir, el siguiente bloque de código

```tex
$$
x = 
\begin{cases}
  a &\text{if } b\\\\ c &\text{if } d
\end{cases}
$$
```

funciona a la perfección, como podemos comprobar a continuación

$$
x = 
\begin{cases}
  a &\text{if } b\\\\ c &\text{if } d
\end{cases}
$$

Esto va a requerir cierto tiempo adicional para que edite algunas de las expresiones escritas con *TeX*, pero me alegro de poder tener a mi disposición la posibilidad de utilizar algunos entornos matemáticos básicos.

*P. S. (acerca de la imagen de cabecera):* efectivamente, organizar ecuaciones con *KaTeX*, tal y como se muestra en la fotografía de [Antoine Dautry](https://unsplash.com/@antoine1003), disponible en [Unsplash](https://unsplash.com/photos/05A-kdOH6Hw), me ha resultado imposible en una primera aproximación, pero he dado con la tecla en una segunda visita al problema.

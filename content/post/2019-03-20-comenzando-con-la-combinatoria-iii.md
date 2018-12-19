---
title:  "Comenzando con la combinatoria (III)"
slug:   "comenzando-con-la-combinatoria-iii"
date:   "2019-03-20T05:59:39+02:00"
draft:  false
bigimg: [{src: "img/blog/20190320-cabecera.jpg"}]
apartados: ["Oposiciones"]
etiquetas: ["Combinatoria"]
proyectos: ["Problemas"]
---

**Problema 61:** 

- (a) ¿Cuántas fichas tiene el dominó?
- (b) Tenemos siete urnas indistinguibles entre sí y dos bolas idénticas, ¿de cuántas formas se pueden meter las bolas en las urnas?
- (c ) Calcula el número de soluciones enteras no negativas de la ecuación $x_1+x_2+\cdots+x_7=2$.

<!--more-->

***

Para el apartado (a), en las fichas del dominó encontramos representados los números desde el $0$ (blanca) al $6$, que aparecen de dos en dos. Por ejemplo, son fichas de este juego los pares $(1,2)$ o $(6,0)$. Por otro lado, el orden en que escojamos los números para conformar una ficha no importa, pues, por ejemplo, los pares $(1,2)$ y $(2,1)$ representan una única ficha del dominó. Finalmente, el juego incorpora fichas en la que se repiten los elementos, como $(0,0)$ o $(5,5)$, por nombrar algunas. Por tanto, estamos interesados en el total de combinaciones con repetición de siete elementos tomados de dos en eso y, entonces, hay $$CR_{7,2} = \dbinom{7+2-1}{2} = \dbinom{8}{2} = \dfrac{8\cdot7}{2} = 28$$ fichas en el juego del dominó.

A continuación, en el apartado (b), si representamos gráficamente nuestras siete urnas indistinguibles como sigue 

$$
(\ \ |\ \ |\ \ |\ \ |\ \ |\ \ |\ \ ),
$$ 

esto es, como si pusiéramos seis rayas sobre la recta real y representamos las bolas como $\*$, una posible configuración sería 

$$
(\ \ |\*|\ \ |\*|\ \ |\ \ |\ \ ).
$$ 

No obstante, si ahora movemos la última raya al principio, la anterior configuración se convierte en 

$$
(\ \ |\ \ |\*|\ \ |\*|\ \ |\ \ ).
$$ 

Así pues, observamos que, de cara a contar posibilidades en este apartado, es como si tuviéramos ocho elementos (las dos bolas, $*$, y las seis rayas, $|$) de dos tipos. Uno de ellos se repite dos veces (las bolas), mientras que el otro se repite en seis ocasiones (las rayas). Por tanto, hay $$PR_{8}^{2,6} = \dfrac{8!}{2!\cdot6!} = \dfrac{8\cdot7}{2}=28$$ formas de introducir dos bolas idénticas en siete urnas indistinguibles entre sí. 

Finalmente, para el apartado (c ), de cara a encontrar las soluciones enteras no negativas de la ecuación $x\_1+x\_2+\cdots+x\_7=2$, observamos rápidamente que cada variable puede tomar, como máximo, los valores $0$, $1$ o $2$. Así pues, podemos representar la situación como hicimos en el apartado anterior, donde ahora cada ''urna'' sería cierta variable $x\_i$, con $i=1,2,\ldots,7$, y el valor de dicha variable vendría dado por el número de ''bolas'' que tuviese en su interior (para un $i$ dado, con $0$ bolas, $x\_i=0$; con $1$ bola, $x\_i=1$; y con $2$ bolas, $x\_i=2$). Por tanto, razonando como antes, la ecuación dada posee $$PR_{8}^{2,6} = \dfrac{8!}{2!\cdot6!} = \dfrac{8\cdot7}{2}=28$$ soluciones enteras no negativas.

Por otro lado, si recordamos de ejercicios anteriores, podemos utilizar las combinaciones con repetición como herramienta para contar el número de bolas idénticas que introducimos en urnas indistinguibles entre sí. Considerando esto, el presente ejercicio se reduce a calcular $CR\_{7,2}$. En resumen,  

- hallar el número de soluciones de la ecuación $x\_1+x\_2+\cdots+x\_n=r$, con $x\_i\geq 0$ para $1\leq i\leq n$ y $r$ entero no negativo,
- encontrar el número de maneras de seleccionar una muestra de tamaño $r$, con elementos repetidos o no, de una colección de tamaño $n$, y
-  calcular el número de formas de distribuir $r$ objetos idénticos entre $n$ destinatarios distintos

es lo mismo.

*P. S. (acerca de la imagen de cabecera):* fotografía de [Thomas Millot](https://unsplash.com/@tomlaudiophile), disponible en [Unsplash](https://unsplash.com/photos/_uighclH2pw).
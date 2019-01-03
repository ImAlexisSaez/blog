---
title:  "Buscando el total de soluciones de una inecuación"
slug:   "buscando-el-total-de-soluciones-de-una-inecuacion"
date:   "2019-05-11T05:59:39+02:00"
draft:  false
bigimg: [{src: "img/blog/20190511-cabecera.jpg"}]
apartados: ["Oposiciones"]
etiquetas: ["Combinatoria"]
proyectos: ["Problemas"]
---

**Problema 76:** Calcula el número de soluciones enteras no negativas de la inecuación $$x+y+z+t\leq 2001.$$

<!--more-->

***

A diferencia de ejercicios anteriores, en el presente encontramos una inecuación en lugar de una ecuación. Razonando en términos de urnas indistinguibles y bolas idénticas, esta situación se traduce en que, para ciertos repartos, algunas de las $2001$ bolas pueden quedar fuera de las cuatro urnas que emplearíamos para representar las variables $x$, $y$, $z$ y $t$. Así pues, procederemos generando una urna adicional, para una variable $u$, que será aquella donde depositemos el exceso de bolas del reparto. Por tanto, la inecuación planteada quedaría ahora como la ecuación $$x+y+z+t+u=2001,$$ de la cual deseamos encontrar el número de soluciones enteras no negativas.

Ahora ya estamos en condiciones de volver a utilizar las estrategias vistas en ejercicios previos. Aplicando la técnica de *barras y estrellas*, necesitamos cuatro *barras* para representar sobre la recta real las cinco urnas y buscamos ubicar luego $2001$ *estrellas* en los huecos que dicha configuración produce. Por consiguiente, el número de formas en que el valor de la suma de cinco variables puede ascender a $2001$, equivale a la cantidad de permutaciones con repetición de $2005$ elementos, donde uno de ellos se repite cuatro veces, mientras que el otro lo hace en $2001$ ocasiones. Así, hay

$$
PR\_{2005}^{4,2001} = CR\_{5,2001} = \dbinom{2005}{2001} = \dfrac{2005\cdot2004\cdot2003\cdot2002}{4!} = 671345179505
$$

soluciones enteras no negativas para la ecuación propuesta y, por tanto, asimismo para la inecuación planteada en el enunciado del ejercicio.

*P. S. (acerca de la imagen de cabecera):* fotografía de [Serge Vorobets](https://unsplash.com/@serge_vorobets), disponible en [Unsplash](https://unsplash.com/photos/CSORty3B_hs).
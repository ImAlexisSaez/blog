---
title:  "Un primer contacto con ecuaciones diofánticas (IV)"
slug:   "un-primer-contacto-con-ecuaciones-diofanticas-iv"
date:   "2019-02-13T05:59:39+02:00"
draft:  false
bigimg: [{src: "img/blog/20190213-cabecera.jpg"}]
apartados: ["Oposiciones"]
etiquetas: ["Ecuaciones diofánticas"]
proyectos: ["Problemas"]
---

**Problema 51:** Halla las soluciones enteras de la ecuación $3x+2y+9z=12$.

<!--more-->

***

Dado que $mcd(2,3,9)=1$, estamos en condiciones de asegurar que la ecuación diofántica planteada admite solución entera. Al encontrar tres incógnitas, para empezar, hemos de comprobar si algún par de coeficientes está compuesto por números primos entre sí. En esta ocasión, como $mcd(2,3)=1$ podemos, por ejemplo, fijar como variables $x$ e $y$, de manera que escribimos la ecuación diofántica como sigue, $$3x+2y=12-9z.$$

A continuación, trabajamos con la ecuación $3x+2y=1$, para la cual, despejando la variable $y$ por ser aquella cuyo coeficiente es más reducido, hallamos que $$y = \dfrac{1-3x}{2},$$ por lo que basta probar, para $x$, valores pertenecientes al *menor sistema completo de restos módulo* $2$. Así, para $x=1$ es cierto que $y = (-1)$, y entonces la solución particular a la ecuación diofántica propuesta arriba queda

$$
\begin{aligned}
x\_0 &= 1\cdot(12-9z) = 12-9z,\\\\ y\_0 &= (-1)\cdot(12-9z) = (-12) + 9z,
\end{aligned}
$$

por lo que su solución general es

$$
\begin{aligned}
x &= 12 - 9z + 2t,\\\\ y &= (-12) + 9z - 3t,
\end{aligned}
$$

con $t$ y $z$ números enteros.

*P. S. (acerca de la imagen de cabecera):* fotografía de [Shifaaz shamoon](https://unsplash.com/@sotti), disponible en [Unsplash](https://unsplash.com/photos/oR0uERTVyD0).
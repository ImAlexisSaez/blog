---
title:  "Empezando con teoría de números (II)"
slug:   "empezando-con-teoria-de-numeros-ii"
date:   "2018-10-11T05:59:39+02:00"
draft:  false
bigimg: [{src: "img/blog/20181011-cabecera.jpg"}]
apartados: ["Oposiciones"]
etiquetas: ["Teoría de números"]
proyectos: ["Problemas"]
---

**Problema 18:** Calcula el inverso de $3$ módulo $7$.

<!--more-->

***

El enunciado nos plantea resolver $$3x\equiv 1\pmod{7}.$$

Como $mcd(3,7)=1$, es decir, $3$ y $7$ son coprimos, estamos en condiciones de asegurar que seremos capaces de encontrar el inverso de $3$ módulo $7$, $x$. Para ello, como los números involucrados son pequeños, podemos simplemente optar por emplear la ''cuenta de la vieja'' y extraer el valor de $x$ por fuerza bruta. Así,
$$
\begin{aligned}
3\cdot 1 &= 3\equiv 3\pmod{7},\\\\ 3\cdot 2 &= 6\equiv 6\pmod{7},\\\\ 3\cdot 3 &= 9\equiv 2\pmod{7},\\\\ 3\cdot 4 &= 12\equiv 5\pmod{7},\\\\ 3\cdot 5 &= 15\equiv 1\pmod{7},
\end{aligned}
$$
luego $x=5$ es el inverso de $3$ módulo $7$. 

Alternativamente, podemos llevar a cabo operaciones elementales sobre la propia ecuación de congruencia. Como $2\cdot3=6$, que es un valor muy cercano a $7$, entonces
$$
\begin{aligned}
3x\equiv 1\pmod{7}&\Leftrightarrow 6x\equiv 2\pmod{7}\\\\ &\Leftrightarrow -x\equiv 2\pmod{7}\\\\ &\Leftrightarrow x\equiv (-2)\pmod{7}\\\\ &\Leftrightarrow x\equiv 5\pmod{7},
\end{aligned}
$$
arribando así al mismo resultado que antes.

*P. S. (acerca de la imagen de cabecera):* simplemente impresionante la fotografía de [John Salvino](https://unsplash.com/@jsalvino), disponible en [Unsplash](https://unsplash.com/photos/YsU8Z2-yGlA).
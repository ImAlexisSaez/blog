---
title:  "Empezando con teoría de números (III)"
slug:   "empezando-con-teoria-de-numeros-iii"
date:   "2018-10-13T05:59:39+02:00"
draft:  false
bigimg: [{src: "img/blog/20181013-cabecera.jpg"}]
apartados: ["Oposiciones"]
etiquetas: ["Teoría de números"]
proyectos: ["Problemas"]
---

**Problema 19:** Calcula el valor de la expresión $$(1^3+2^3+\cdots+100^3)\pmod{4}.$$

<!--more-->

***

Si tenemos en cuenta que
$$
\begin{aligned}
1\equiv 1\pmod{4} &\Rightarrow 1^3\equiv 1^3\pmod{4}\equiv 1\pmod{4},\\\\ 2\equiv 2\pmod{4} &\Rightarrow 2^3\equiv 2^3\pmod{4}\equiv 8\pmod{4}\equiv 0\pmod{4},\\\\ 3\equiv 3\pmod{4} &\Rightarrow 3^3\equiv 3^3\pmod{4}\equiv 27\pmod{4}\equiv 3\pmod{4},\\\\ 4\equiv 0\pmod{4} &\Rightarrow 4^3\equiv 0^3\pmod{4}\equiv 0\pmod{4},\\\\ 5\equiv 1\pmod{4} &\Rightarrow 5^3\equiv 1^3\pmod{4}\equiv 1\pmod{4},\\\\ 6\equiv 2\pmod{4} &\Rightarrow 6^3\equiv 2^3\pmod{4}\equiv 8\pmod{4}\equiv 0\pmod{4},
\end{aligned}
$$
enseguida atisbamos cómo se repetiría el mismo patrón cada cuatro sumandos. Ahora bien,
$$
\begin{aligned}
(1^3+2^3+3^3+4^3)\pmod{4}&\equiv (1+0+3+0)\pmod{4}\\\\ &\equiv 4\pmod{4}\\\\ &\equiv 0\pmod{4},
\end{aligned}
$$
y como en la suma de cubos propuesta en el enunciado del ejercicio hemos de sumar $25$ veces el resultado del patrón anterior, llegamos a que
$$
(1^3+2^3+\cdots+100^3)\pmod{4} \equiv 0\pmod{4},
$$
es decir, la suma de los cubos de los cien primeros números naturales es múltiplo de $4$.


*P. S. (acerca de la imagen de cabecera):* la fotografía de [Nick Karvounis](https://unsplash.com/@nickkarvounis), disponible en [Unsplash](https://unsplash.com/photos/nTinYg604lE), recoge una de esas siempre atractivas simetrías generadas a partir el reflejo de objetos sobre el agua.
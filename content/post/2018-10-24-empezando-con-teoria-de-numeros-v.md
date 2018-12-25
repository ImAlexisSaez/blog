---
title:  "Empezando con teoría de números (V)"
slug:   "empezando-con-teoria-de-numeros-v"
date:   "2018-10-24T05:59:39+02:00"
draft:  false
bigimg: [{src: "img/blog/20181024-cabecera.jpg"}]
apartados: ["Oposiciones"]
etiquetas: ["Teoría de números"]
proyectos: ["Problemas"]
---

**Problema 21:** Calcula la regla de divisibilidad por $7$.

<!--more-->

***

Veamos que, en esta ocasión, proceder como en ejercicios anteriores no dará lugar a establecer una sencilla regla para el criterio de divisibilidad del $7$. En efecto, consideremos el número de $n$ cifras $a\_{n-1}a\_{n-2}\cdots a\_2a\_1a\_0$ en base $10$. Sabemos, por el *Teorema Fundamental de la Numeración*, que podemos expresarlo como
$$
a\_{n-1}a\_{n-2}\cdots a\_2a\_1a\_0 = a\_0+a\_110+a\_210^2 + \cdots + a\_{n-2}10^{n-2}+a\_{n-1}10^{n-1}.
$$

Para encontrar el criterio de divisibilidad del $7$ utilizaremos las propiedades de las congruencias sobre las potencias de $10$, buscando una condición sobre los dígitos del número $a\_{n-1}a\_{n-2}\cdots a\_2a\_1a\_0$ de manera que
$$
a\_0+a\_110+a\_210^2 + \cdots + a\_{n-2}10^{n-2}+a\_{n-1}10^{n-1}\equiv 0\pmod{7},
$$
esto es, dicho número sea múltiplo de $7$.

Ahora bien,
$$
\begin{aligned}
10&\equiv 3\pmod{7},\\\\ 10^2&\equiv 3^2\pmod{7}\equiv 9\pmod{7}\equiv 2\pmod{7},\\\\ 10^3&\equiv 3^3\pmod{7}\equiv 27\pmod{7}\equiv 6\pmod{7},\\\\ 10^4&\equiv 3^4\pmod{7}\equiv 81\pmod{7}\equiv 4\pmod{7},\\\\ &\vdots
\end{aligned}
$$
y comenzamos a atisbar que el criterio que podríamos extraer es ciertamente extraño y muy complicado de recordar, puesto que
$$
a\_0+a\_110+a\_210^2 + \cdots + a\_{n-1}10^{n-1}\equiv (a\_0 + 3a\_1 + 2a\_2 + 6a\_3 + 4a\_4 + \cdots)\pmod{7}.
$$

Por lo que respecta a la divisibilidad de un número por $7$, conviene que tengamos a mano el siguiente resultado: ''*un número de la forma $n=10d+u$, con $d>0$ y $0\leq u\leq 9$ es múltiplo de $7$ si, y solo si, $d-2u$ es múltiplo de $7$*''.

Efectivamente, si suponemos cierto que $(10d+u)\equiv 0\pmod{7}$, es decir, que $n=10d+u$ es múltiplo de $7$, y aplicamos ahora propiedades de las congruencias sobre la forma del número $n$, llegamos a que
$$
(10d+u)\equiv 0\pmod{7} \Leftrightarrow (3d-6u)\equiv 0\pmod{7} \Leftrightarrow (3(d-2u))\equiv 0\pmod{7},
$$
esto es, hemos arribado a que el producto de dos números es múltiplo de $7$, y como sabemos que el número $3$ no lo es, concluimos que $d-2u$ es múltiplo de $7$.

Recíprocamente, si $d-2u$ es múltiplo de $7$, entonces $(d-2u)\equiv 0\pmod{7}$ y multiplicando por $10$ la ecuación de congruencia tenemos que $(10d-20u)\equiv 0\pmod{7}$. Ahora, como $(-20)\equiv 1\pmod{7}$, llegamos a que $(10d+u)\equiv 0\pmod{7}$, es decir, el número $n=10d+u$ es un múltiplo de $7$, quedando así la doble implicación probada.

Veamos en acción esta proposición con un par de ejemplos sencillos. Si $n=63 = 60+3$, entonces $d = 6$, $u=3$ y $d-2u = 6-2\cdot3=0$ que, efectivamente, es un múltiplo de $7$, luego $63$ asimismo lo es. Si $n = 9009$, tenemos que $d = 900$, $u=9$ y $d-2u = 900-2\cdot9=882 = 7\cdot126$, luego $d-2u$ es un múltiplo de $7$, por lo que podemos concluir que el número $9009$ también lo es.

*P. S. (acerca de la imagen de cabecera):* la fotografía de [Banter Snaps](https://unsplash.com/@bantersnaps), disponible en [Unsplash](https://unsplash.com/photos/9yWcy5B-haM), muestra otra de esas preciosas simetrías que se generan haciendo uso del reflejo sobre el agua.
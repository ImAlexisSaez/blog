---
title:  "Empezando con teoría de números (I)"
slug:   "empezando-con-teoria-de-numeros-i"
date:   "2018-10-09T05:59:39+02:00"
draft:  false
bigimg: [{src: "img/blog/20181009-cabecera.jpg"}]
apartados: ["Oposiciones"]
etiquetas: ["Teoría de números", "Fermat"]
proyectos: ["Problemas"]
---

**Problema 17:** Calcula el resto de la división de $$2^{1538}$$ entre $5$.

<!--more-->

***

Estudiemos, utilizando la teoría de congruencias, el comportamiento del valor de las primeras potencias de $2$.
$$
\begin{aligned}
2^1&\equiv 2 \pmod{5},\\\\ 2^2&\equiv 4 \pmod{5}\equiv(-1) \pmod{5},\\\\ 2^3&\equiv 3 \pmod{5},\\\\ 2^4&\equiv 1 \pmod{5}.
\end{aligned}
$$
Este resulta un buen punto en el que detener nuestro análisis, ya que ahora sabemos que las potencias de $2$ que son múltiplo de $4$ son congruentes con $1$ módulo $5$. Es decir, $2^8\equiv 1 \pmod{5}$, $2^{12}\equiv 1 \pmod{5}$, etc. Antes de continuar, cabe señalar que:

- Podíamos habernos ahorrado algunos cálculos, ya que como $p=5$ es un número primo y $mcd(2,5)=1$, entonces, por el *Pequeño Teorema de Fermat* (ver abajo), $2^{5-1} = 2^4\equiv 1 \pmod{5}$. 
-  Además, en el momento en el que hemos obtenido la potencia para la cual $(-1)\pmod{5}$ ya podíamos intuir cuándo llegaríamos al resultado deseado, ya que $(-1)^2=1$, lo que indica que al elevar al cuadrado la potencia asociada ($2^2$ en este caso) tendríamos que sería congruente $1$ módulo $5$. Es decir $(2^2)^2 = 2^4 \equiv 1\pmod{5}$.

Ahora, dividiendo, sabemos que $1538 = 384\cdot 4 + 2$ y, por tanto,
$$
2^{1538} = 2^{384\cdot 4 + 2} = (2^4)^{384}\cdot 2^2\equiv (1\cdot 4)\pmod{5}\equiv 4\pmod{5},
$$
y así, el resto de la división de $2^{1538}$ entre $5$ asciende a $4$.

***

**Teorema (Pequeño Teorema de Fermat)**: sea $p$ un número primo y supongamos que $p$ no divide a $a$. Entonces 
$$
a^{p\-1}\equiv 1\pmod{p}.
$$

***

*P. S. (acerca de la imagen de cabecera):* y con la fotografía de [Sven Read](https://unsplash.com/@starburst1977), disponible en [Unsplash](https://unsplash.com/photos/_eRanldVghE), van ya en la web ni se sabe cuántas fotografías de la combinación de escaleras con perspectiva. Para gustos, los colores.
---
title:  "Presentando desarreglos"
slug:   "presentando-desarreglos"
date:   "2019-04-24T05:59:39+02:00"
draft:  false
bigimg: [{src: "img/blog/20190424-cabecera.jpg"}]
apartados: ["Oposiciones"]
etiquetas: ["Combinatoria"]
proyectos: ["Problemas"]
---

**Problema 71:** Un desarreglo es una permutación de objetos en la que ningún objeto está en su posición original. Por ejemplo, $234561$ es un desarreglo de $123456$, pero $213645$ no, ya que $3$ está en su posición original.

- (a) Escribe los desarreglos de $123$.
- (b) Demuestra que, dados $n$ objetos, el total de desarreglos asciende a $$D\_n = n!\left(1-\dfrac{1}{1!} + \dfrac{1}{2!} - \dfrac{1}{3!}+\cdots+(-1)^n\dfrac{1}{n!}\right).$$

<!--more-->

***

En cuanto al apartado (a), empecemos escribiendo todas las permutaciones de $123$,

$$
123,\quad 132,\quad 213,\quad 231,\quad 312,\quad 321.
$$

De entre ellas, descartamos $123$ y $132$, por mantener $1$ su posición original; asimismo hacemos lo propio con $321$, porque $2$ permanece invariante; y con $213$, ya que $3$ continúa en el mismo lugar. Por tanto, dos son los desarreglos de $123$, a saber, $231$ y $312$.

Para abordar el apartado (b) haremos uso del *Principio de complementación*, y, en lugar de buscar la cantidad de desarreglos, hallaremos el número de permutaciones que al menos mantienen una cifra en su posición original (los ''arreglos''), pues, aunque resulte sorprendente a primera vista, es más fácil contar estas últimas. Una vez encontrado dicho número, se lo sustraeremos al total de permutaciones, obteniendo así la cifra de desarreglos.

Por consiguiente, para empezar, dados $n$ objetos, sabemos que el total de permutaciones posibles asciende a $P\_n = n!$. Ahora, definamos $A\_i$ como el total de conjuntos en el que $i$ objetos mantienen su posición original, con $1\leq i\leq n$. Por tanto, el número de desarreglos vendrá dado por 

$$
D\_n = n! - card(A\_1\cup A\_2\cup\cdots\cup A\_n).
$$

Ahora bien, ¿cuántos conjuntos encontramos que se caractericen por mantener un objeto su posición original? De entre los $n$ objetos, seleccionamos uno, acción que podemos llevar a cabo de $C\_{n,1}$ maneras posibles. Después, el resto de objetos, $n-1$, simplemente los permutamos, situación que podemos realizar de $P\_{n-1} = (n-1)!$ formas posibles. Aplicando la *regla del producto* hay

$$
C\_{n,1}(n-1)! = \dbinom{n}{1}(n-1)!
$$

conjuntos que mantienen un objeto en su posición original. Análogamente, ¿cuántos conjuntos encontramos que se caractericen por mantener dos objetos sus posiciones originales? De entre los $n$ objetos, seleccionamos dos, acción que podemos llevar a cabo de $C\_{n,2}$ maneras posibles. Luego, el resto de objetos, $n-2$, simplemente los permutamos, situación que podemos realizar de $P\_{n-2} = (n-2)!$ formas posibles. Aplicando la *regla del producto* hay

$$
C\_{n,2}(n-2)! = \dbinom{n}{2}(n-2)!
$$

conjuntos que mantienen dos objetos en sus posiciones originales. El mismo razonamiento se puede aplicar para el caso de tres objetos, cuatro objetos, etc.

Por consiguiente, aplicando el *Principio de inclusión-exclusión*,

$$
\begin{aligned}
D\_n &= n! - card(A\_1\cup A\_2\cup\cdots\cup A\_n)\\\\ &= n!-\left(\dbinom{n}{1}(n-1)! - \dbinom{n}{2}(n-2)! + \cdots + (-1)^{n+1}\dbinom{n}{n}\right)\\\\ &= n! - \left(\dfrac{n}{1}\cdot(n-1)! - \dfrac{n(n-1)}{2}\cdot(n-2)! + \cdots + (-1)^{n+1}\cdot 1\right)\\\\ &= n! - \left(\dfrac{n!}{1} - \dfrac{n!}{2} + \cdots + (-1)^{n+1}\dfrac{n!}{n!}\right)\\\\ &= n!\left(1 - \dfrac{1}{1!} + \dfrac{1}{2!} - \cdots + (-1)^n\dfrac{1}{n!}\right),
\end{aligned}
$$

tal y como queríamos demostrar.

*P. S. (acerca de la imagen de cabecera):* fotografía de [Fezbot2000](https://unsplash.com/@fezbot2000), disponible en [Unsplash](https://unsplash.com/photos/xVXlEoQbKc4).
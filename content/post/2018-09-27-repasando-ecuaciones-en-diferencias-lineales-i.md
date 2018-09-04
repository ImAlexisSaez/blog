---
title:  "Repasando ecuaciones en diferencias lineales (I)"
slug:   "repasando-ecuaciones-en-diferencias-lineales-i"
date:   "2018-09-27T05:59:39+02:00"
draft:  false
bigimg: [{src: "img/blog/20180927-cabecera.jpg"}]
apartados: ["Oposiciones"]
etiquetas: ["Ecuaciones en diferencias"]
proyectos: ["Problemas"]
---

**Problema 12:** Resuelve

- (a) $a\_{n+3} - 3a\_{n+2} - 4a\_{n+1} + 12a\_n = 0$.
- (b) $a\_{n+3} - 4a\_{n+2} + 5a\_{n+1} - 2a\_n = 0$.

<!--more-->

***

En el apartado (a), encontramos la ecuación en diferencias lineal homogénea de orden 3 dada por $a\_{n+3} - 3a\_{n+2} - 4a_{n+1} + 12a_n = 0$, cuya ecuación característica asociada es $$\lambda^3-3\lambda^2-4\lambda+12=0.$$ Ahora bien, como $\lambda^3-3\lambda^2-4\lambda+12 = (\lambda-3)(\lambda-2)(\lambda+2)$, estamos ante el caso de raíces reales simples, de manera que la solución queda $$a_h(n) = c_1(-2)^n + c_22^n + c_33^n,$$ con $c_1,c_2,c_3\in\mathbb{R}$.

Para el apartado (b), la ecuación en diferencias lineal $a\_{n+3} - 4a\_{n+2} + 5a_{n+1} - 2a_n = 0$ es homogénea de orden 3, con ecuación característica $$\lambda^3 - 4\lambda^2 + 5\lambda - 2 = 0.$$ Como $\lambda^3 - 4\lambda^2 + 5\lambda - 2 = (\lambda-2)(\lambda-1)^2$, $\lambda=1$ es una raíz real de multiplicidad $m=2$, mientras que $\lambda=2$ es una raíz real simple, por lo que la solución queda $$a_h(n) = c_11^n + c_2n1^n + c_32^n = c_1+c_2n+c_32^n,$$ con $c_1,c_2,c_3\in\mathbb{R}$.

*P. S. (acerca de la imagen de cabecera):* la fotografía de [Henry Be](https://unsplash.com/@henry_be), disponible en [Unsplash](https://unsplash.com/photos/neH2O7TaRFU), muestra el lugar perfecto para perderse durante horas, ¿verdad?
---
title:  "¿Y si el número de divisores es impar?"
slug:   "y-si-el-numero-de-divisores-es-impar"
date:   "2018-12-15T05:59:39+02:00"
draft:  false
bigimg: [{src: "img/blog/20181215-cabecera.jpg"}]
apartados: ["Oposiciones"]
etiquetas: ["Teoría de números"]
proyectos: ["Problemas"]
---

**Problema 34:** Caracteriza aquellos números naturales cuyo número de divisores es impar.

<!--more-->

***

De partida, sabemos que los números naturales buscados no serán primos, puestos estos últimos siempre poseen una cantidad par de divisores, dos para ser más concretos: $1$ y el propio número primo. Así pues, consideremos un número natural $m$ expresado mediante su factorización en factores primos, $$m=a^xb^yc^z\cdots,$$ con $a,b,c,\ldots$ números primos y $x,y,z,\ldots$ números naturales. Sabemos que el número de divisores de $m$ es, en total, $$(x+1)(y+1)(z+1)\cdots.$$ 

Ahora bien, nos indican que dicho producto ha de ser un número impar, hecho que traduce en que todos y cada uno de sus términos han de ser números impares (ya que bastaría con que únicamente uno fuese par para que todo el producto resultase un número par). Como $x+1, y+1, z+1,\ldots$ son números impares, inmediatamente deducimos que $x,y,z,\ldots$ serán números pares, que podrán escribirse como $x=2p, y=2q, z=2r,\ldots$ para ciertos enteros $p,q,r,\ldots$. De esta manera, $$m = a^xb^yc^z\cdots = a^{2p}b^{2q}c^{2r}\cdots = (a^pb^qc^r\cdots)^2,$$ esto es, los números naturales que se caracterizan por poseer una cifra impar de divisores son cuadrados perfectos. Con ello, en función de la cantidad de divisores de un número, contamos así con un criterio para decidir rápidamente si dicho número es o no un cuadrado perfecto, según su total de divisores sea o no una cifra impar. 

*P. S. (acerca de la imagen de cabecera):* fotografía de [Elijah O'Donnell](https://unsplash.com/@elijahsad), disponible en [Unsplash](https://unsplash.com/photos/ycMLPhq_tdk).
---
layout: post
title:  "Una métrica para la pertenencia a una clase mediante k-means"
date:   2018-05-13
categories: miscelaneous
tags: clustering k-means SVM k-prototypes affinity-propagation hierarchical non-hierarchical classification metrics algorithms KPI distance
author: SC
mathjax: true
---

* content
{:toc}


En data science, muchas veces nos encontramos ante la necesidad de dar métricas o puntuaciones para los resultados que obtenemos. En ocasiones, no sólo es interesante el propio resultado, si no tambien tener una idea de su calidad. 

En este contexto, me encuentro trabajando en un proyecto en el que se implementa una clasificación mediante el algoritmo de k-means, y se me requería dar una métrica para la pertenencia de cada observación a su clase asignada. Quiero decir, una medida de la seguridad o la probabilidad con la que dicha observación pertenece a esa clase. 

Os voy a comentar mi propuesta para "medir" esto...




## Revisitando k-means

Recordemos brevemente que, en esencia, el modelo que genera k-means queda caracterizado y parametrizado por las coordenadas de un conjunto de centroides. Tantos como clusters hayamos propuesto para la agrupación (tipo de clustering no-jerárquico que requiere predefinir el número de clusters en el que queremos agrupar nuestro conjunto de observaciones).

Así, tras un proceso iterativo que va reubicando los centroides de manera que se minimice la suma cuadrática de distancias (mínimos cuadrados) entre estos y las observaciones, a cada punto (en el sentido de observación) se le asigna la clase correspondiente al centroide más cercano.


## La métrica

Con esto en mente, y de manera intuitiva, podríamos decir que cuando un punto se encuentra muy próximo al centroide de su clase, su pertenencia es más "fuerte" que cuando está alejado. Así, encaminamos el razonamiento hacia una medida de la distancia entre el punto y el centroide de su clase (las métricas para este modelo van todas en esa dirección). Pero necesitamos poner esta distancia en un contexto que nos permita decir cómo de cerca o de lejos se encuentran punto y centroide. No resulta suficiente con decir la distancia es 5... ¿5 es mucho o poco?...

Pues bien, he considerado que la "seguridad" con la que una observación pertenece a su clase, no sólo depende de lo cerca que este de su centroide, si no tambien de lo lejos que esté de los demás. Entonces propongo un score dado por el cociente entre la distancia a su centroide y la distancia al siguiente centroide más próximo. Expresémoslo como,

$$ s = \frac{d_{centroid}}{d_{nearest}} $$

Notar que como $d_{centroid} < d_{nearest}$ 

tenemos que esta puntuación queda acotada entre 0 y 1, siendo los casos extremos la coincidencia del punto con el centroide y la equidastancia con el siguiente centroide más próximo. En el primer caso, este conciente se anula y expresaría un pertenencia muy fuerte a esa clase puesto que punto y centroide tienen las mismas coordenadas. En el segundo caso estaríamos ante una supuesta equidistancia con dos centroides. Digo supuesta situación, porque, aunque con dudas, me atreverí a decir que, si se diera, daría problemas de no-convergencia.

Pero me resulta contraintuitivo que sean los números próximos a 0 los que indiquen una pertenencia "fuerte" a la clase y los próximos a 1 la pertenencia "débil". Por esto, se puede corregir la expresión de esta manera,

$$ s = 1 - \frac{d_{centroid}}{d_{nearest}} $$

Así son los números mayores los que connotan que la observación se encuentra en el entorno más próximo del centroide que caracteriza la clase a la que pertenece.


Saludos!

S



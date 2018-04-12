---
layout: post
title:  "Qué es data science?"
date:   2018-04-12
categories: thoughts opinion
tags: data-science
author: SC
mathjax: true
---

* content
{:toc}


Esto pretende ser un blog en torno a la ciencia computacional y de datos, así pues, no se me ocurre mejor manera de inaugurarlo que dando mi visión de lo que es la data science, su evolución y los roles profesionales a los que ha dado lugar.

Como una primera (y breve) definición yo diría que 

>*es el conjunto de procesos y sistemas mediante los que extraemos y generalizamos conocimiento sobre un fenómeno, a partir de múltiples observaciones particulares (los datos) del mismo.*

Es un tema que ha sido foco de debate, ha llenado muchísimos artículos y ha causado cierta controversia y desacuerdo por lo novedoso y amplio del término. No tanto por el término en sí, si no por todas las áreas que involucra y por su puesta en escena en el mercado laboral.
Desde mi punto de vista, los causantes de la confusión han sido, precisamente; la amplitud que acabo de mencionar, dada por su multidisciplinaridad y su evolución con y sobre las nuevas tecnologías y... ¿por qué no?, por el intrusismo profesional que ha sufrido. 

Veamos por qué digo esto...

La denominada "ciencia de datos" se origina en la estadística y las matemáticas que, para mí, son los primeros y originales científicos de datos: estadísticos, matemáticos y, si acaso, algunos economistas y físicos (yo soy físico). Seamos sinceros, la mayor parte del "data science", "data mining", "machine learning", "business intelligence" o como queramos llamarlo, se fundamentan en lo que siempre se ha denominado "estadística" y "optimización". "Investigación operativa" si queremos ser un poco más modernos (una vez me dijeron que los primeros nombres son las etiquetas "comerciales" que les han puesto a las segundas para poder "venderlas"). Como mucho las aderezaría con las técnicas heurísticas que, en las universidades, se estudian en los departamentos de Estadística y/o Investigación Operativa, pero acepto mencionarlas a parte por no estar sujetas al mismo rigor matemático.

Después llegó el "boom" de los datos. Cantidades ingentes de datos estaban siendo almacenadas y se querían aprovechar. Para esto se requirieron sistemas capaces de procesarlos y esta necesidad se dió paralelamente con la sustancial mejora de los ordenadores. Además, el ser capaz de empaquetar un proceso analítico (me gusta referirme a la estadística y optimización, en el contexto de la data science, como "analítica cuantitativa" o, simplemente "analítica") en un componente de software, dota al propio proceso de usabilidad y potencial comercial. Estas nuevas aplicaciones y soporte tecnológico incluyó de lleno a otros perfiles técnicos, en especial ingenieros informáticos y telecos, aunque tambien industriales.

Notar que con esto ya tenemos un amplio abanico de perfiles jugando al mismo juego, pero resulta evidente que, por lo menos a priori y de base, todos no llevan las mismas cartas ni juegan de la misma manera. Sería como decir que un nadador, futbolista y boxeador tienen las mismas habilidades y cualidades por ser deportistas. Pueden compartir oficio, tener cosas en común, incluso retroalimentarse, pero cada uno pertenece a una disciplina diferente en el mundo del deporte. 

Pienso que con esto se desdibuja (o quizá se redibuja) la "data science" y a estos matemáticos, estadísticos, economistas, físicos, ingenieros informáticos, de telecomunicaciones e industriales, se incorporan otros perfiles científico/técnicos y de administración y gestión de empresas... incluso algún técnico en marketing he llegado a ver bajo el titular de "data scientist"...

...y hay que recordar que todo esto en más o menos... ¿los últimos 15 años?...


...pero tras la tormenta llega la calma...
---

Tengo la impresión de que ahora empezamos a estar de acuerdo en lo que es un data scientist, o más bien los tipos de data scientist y las habilidades que deben de tener para ejercer uno u otro papel en el pipeline de los datos.

Pensemos, por ejemplo en un servicio web, o microservicio (término muy de moda entre arquitectos de software) para tratar de definir y segmentar un proceso data science actual. Este, normalmente estará ubicado en una plataforma cloud y puede hacer uso de datos provenientes de fuentes externas (pueden ser ficheros, otras bases de datos, conjuntos de textos que "arañemos" de la web...) que serán ingestados e indexados en las bases de datos asociadas al servicio. Despues serán usados por los procesos analíticos; se limpiarán y explotarán y devolverán resultados por una API. Esta API, en el ejemplo del microservicio, servirá para ser consumida por otros componentes de software.

En esta síntesis del pipeline de datos sobre un servicio data science, diferenciaría tres roles principales:

1. En primer lugar hablaba de una plataforma cloud, ingesta e indexación en bases de datos locales (para el microservicio). En esta parte ubicaría a lo que se denomina "data engineer". Notar que es un perfil híbrido entre sistemas y bases de datos. Podría ser mejor diferenciar a un arquitecto cloud (más próximo a la arquitectura en sí) y a un especialista en tratamiento de bases de datos. Quizá este último sería el data engineer. En fin, no pretendo hilar tan fino y, al final, tambien depende de la estructura del equipo y del proyecto que se esté tratando.

2. A continuación he mencionado los procesos analíticos. Este rol sería el más próximo al estereotipo de "data scientist". Un perfil híbrido entre las matemáticas, la programación y las bases de datos. Quizá un matemático con conocimientos en informática o un informático con conocimientos en matemáticas. Debe de entender la parte matemática, saber consultar y usar las bases de datos y desarrollar código para procesar los datos.

3. Por último, alguien consume los resultados o datos procesados. Considero que este rol es propio de un profesional más proximo al negocio con conocimientos en matemáticas y herramientas informáticas. Esto sería el perfil actualmente denominado "data o business analyst".

Por supuesto, estas fronteras son muy difusas y muchas veces unos roles se solapan o se balancean con otros. Además depende tambien de la experiencia e intereses del propio profesional para que se incline hacia una u otra actividad. En cualquier caso, creo que es una buena primera (y gruesa) clasificación, es la que se propone y acepta en los últimos artículos que he leído acerca del tema y resulta bastante acorde con el pipe de datos en muchos casos. 

Saludos!






# Spotipy BEDUne Right
## Equipo 6
*Análisis de los datos de Spotify, gráficas bonitas incluidas.* 
<img src = 'BeduEquipo6.png'>
## Índice
- [Introducción](#introduccion)
- [Identificación del problema](#identificacion)
- [Planteamiento de preguntas](#preguntas)
  * [¿De qué forma puede Spotify diferenciarse de su competencia siguiendo una estrategia basada en datos? ](#pregunta1)
- [Colección de datos](#coleccion)
- [Análisis Exploratorio de Datos](#exploratorio)
- [Limpieza de datos](#limpieza)  
- [¿API?](#api)
   * [Spotipy al rescate](#spotipy)
- [Links](#links)
- [Extra: La música y el mundo, o **un mapa vale más que mil palabras**](#geografia)
  * [Geopandas](#geopandas)
<a name="introduccion"></a>
## Introducción
En este proyecto pongámonos en los zapatos de unos científicos de datos en Spotify, graduados de BEDU y que pasaron exitosamente a la fase de Machine Learning.

Divideremos cada uno de los pasos para la elaboración del proyecto en secciones, a cada sección le corresponderá su Notebook.
Al tratarse de un README, no trataremos los temas a profundidad, sino que daremos una breve introducción que podrá consistir de fragmentos del contenido de los Notebooks (ubicados en Spotipy-BEDUne-Right/Postworks)

<a name="identificacion"></a>
## Identificación del problema

Este paso corresponde a
```
Spotipy-BEDUne-Right/Postworks/Postwork_5_Módulo_1.ipynb 
```
> ¿De qué forma puede Spotify diferenciarse de su competencia siguiendo una estrategia basada en datos? En la actualidad, se estima que casi el 90% de los datos existentes en internet fueron creados en los últimos años, y de estos, gran parte permanecen sin ser analizados. se ha llegado a un punto tal que, los datos han sido catalogados como el petróleo del siglo XXI, resaltando las oportunidades que pueden obtenerse de su exploración. Para este proyecto, continuaremos centrándonos en la industria de streaming de música como se hizo en el módulo anterior, más específicamente, en Spotify, una de las empresas más resilientes ante la entrada de nuevos competidores y que, ante este panorama competitivo, se ha visto forzada a buscar nuevas formas de mantenerse en la punta de los ingresos generados en el sector.


<a name="preguntas"></a>
## Planteamiento de preguntas
Este paso corresponde a
```
Spotipy-BEDUne-Right/Postworks/Postwork_5_Módulo_2.ipynb 
```
> Una vez que hemos identificado el problema y decidido que la mejor estrategia de diferenciación para Spotify sería la de integrar los datos generados por sus usarios y utlizarlos dentro de sus algoritmos de recomendación, podemos comenzar a plantear preguntas relacionadas no solamente a las posibles fuentes e información necesaria en el dataset, sino a la misma estructura del algortimo (el algoritmo escapa de los límites del módulo, pero tenerlo en mente nos sirve para tener clara la información útil de la que no lo es en el proceso de recopilación y limpieza).

Algunas otras preguntas que surgen, pero que no necesariamente vienen en la misma línea de pensamiento que la que planteamos surgen y serán abordadas en la sección extra.


<a name="pregunta1"></a>
### ¿De qué forma puede Spotify diferenciarse de su competencia siguiendo una estrategia basada en datos? 

Las preguntas que planteamos en el Notebook tienen este eje focal, puesto que buscamos no solo una solución que nos parezca factible, sino una que podamos comprobar y potenciar con la cantidad de datos que maneja Spotify.



<a name="coleccion"></a>
## Colección de datos

Este paso corresponde a
```
Spotipy-BEDUne-Right/Postworks/Postwork_5_Módulo_3.ipynb 
```
> Hemos llegado a la sección de recopilación de datos, es importante mencionar que, investigando sobre posibles inputs para la creación de un algoritmo sencillo de recomendación, encontramos datasets que requieren de las características de las canciones escuchadas, es por ello que elegimos aquellos datasets que contienen esta información. En etapas posteriores del proyecto preferimos utilizar los datos extraídos directamente desde la API, pero para cumplir con lo establecido en este postwork, nos referimos a los sets que encontramos en Kaggle.

Veremos tambien la posiblidad de obtener los datos directamente desde Spotify.

<a name="exploratorio"></a>
## Análisis exploratorio de datos
Este paso corresponde a
```
Spotipy-BEDUne-Right/Postworks/Postwork_5_Módulo_4.ipynb 
```
Aqui haremos uno de las partes cruciales de cualquier análisis de datos. La exploración. Por lo tanto, apoyados del poswork, nos enfocaremos en responder las siguientes preguntas.

- ¿El conjunto de datos que tengo realmente me sirve para responder algunas de las preguntas que me planteé?
- ¿Qué tamaño tiene mi conjunto de datos? ¿Serán datos suficientes?
- ¿Qué columnas tengo y qué información tengo en cada una de esas columnas?
- Los nombres que tienen mis columnas, ¿son el nombre más apropiado?
- ¿Qué tipos de datos tengo en cada columna? ¿Parecen ser el tipo correcto de datos? ¿O es un tipo de datos "incorrecto"?
- Si selecciono algunas filas al azar y las observo, ¿estoy obteniendo los datos que debería? ¿o hay datos que parecen estar "sucios" o "incorrectos"?
- Responde estas preguntas usando las técnicas que aprendiste en esta sesión y comparte tus hallazgos con tus compañeros y tu experto.



<a name="limpieza"></a>
## Limpieza de datos

Este paso corresponde a
```
Spotipy-BEDUne-Right/Postworks/Postwork_5_Módulo_5.ipynb 
```
Para un correcto y óptimo análisis de los datos, localizamos y limpiamos aquella información que podría ser innecesaria o incluso que este perjudicando a nuestro dataset. En este paso eliminamos NA's y conservamos solo las columnas que necesitaremos, tras analizar el contenido de cada una.


<a name="api"></a>
## ¿API?

Este paso corresponde a
```
Spotipy-BEDUne-Right/Postworks/Postwork_5_Módulo_6.ipynb 
```
Según [redhat](https://www.redhat.com/es/topics/api/what-are-application-programming-interfaces) : Una API es un conjunto de definiciones y protocolos que se utiliza para desarrollar e integrar el software de las aplicaciones. API significa interfaz de programación de aplicaciones.

> En esta sección del proyecto detallamos de forma puntual la extracción de datos desde la API de Spotify (...) No podemos trabajar directamente con los datos en crudo, por lo que también abordaremos la limpieza e integración del dataset. Con el fin de comprobar que los datos están listos para la etapa de input, crearemos un "perfil de gustos" con los datos obtenidos en la parte final.

<a name="spotipy"></a>
### Spotipy al rescate
Para poder simplificarnos el proceso de las solicitudes GET a la API de Spotify, nos apoyaremos en Spotipy, una librería que sirve de interfaz para el API y asi, a todos los datos en la plataforma. Para instalarla usaremos el siguiente comando en los notebooks.
```
!pip install spotipy
```

<a name="geografia"></a>
## Extra: La música y el mundo, o **un mapa vale más que mil palabras**
Este paso extra esta alojado en la siguiente [liga](https://colab.research.google.com/drive/1YMSnIwXacq0136SFCc_3Wt1jWYubMSqu#scrollTo=2o3a8scm7keb)

> Ante la posiblidad de tener información o mejor dicho, de tener respuestas respecto al tipo de música que escuchamos y como se clasifican aquellas canciones en una playlist gracias al API de Spotify, es natural extender el alcance de estas respuestas y plantearnos preguntas acerca del mundo en el que coexistimos (...)


<a name="geopandas"></a>
### Geopandas

Utilizaremos una librería para el análisis de datos geográficos y nos servirá bastante para visualizar las respuestas a nuestras inquietudes. Para instalarla necesitamos ejecutar:
```
!pip install --upgrade geopandas
!pip install --upgrade pyshp
!pip install --upgrade shapely
!pip install --upgrade descartes
```


<a name="links"></a>

### Links
Finalmente, algunos links que servirán al lector para ahondar mas en los temas tocados.
- [Spotify for Developers](https://developer.spotify.com/documentation/web-api/)
- [Spotipy](https://spotipy.readthedocs.io/en/2.17.1/)
- [geopandas](https://geopandas.org/)



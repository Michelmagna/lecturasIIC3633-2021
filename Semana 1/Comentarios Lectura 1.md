
# Lectura Semana 1
### Título: "Collaborative Filtering Recommender Systems".
### Autores: J. Ben Schafer, Dan Frankowski, Jon Herlocker and Shilad Sen.
------------

## Resumen
------------
El filtrado colaborativo es el proceso de filtrar o evaluar elementos utilizando las opiniones de otras personas. Este concepto nace de situaciones cotidianas tradicionales, como al momento de compartir una persona conversar respecto a intereses en cierto tema, como pueden ser peliculas, juegos, musica, entre tantos.

El sitio web MovieLens utiliza CL para recomendar peliculas. Estese basa en dos calificaciones que se recopilan de los usuarios: Por un lado, las Calificaciones explicitas son las entregadas por el usuario. Por otro, las implicitas son las inferidas en base al comportamiento del usuario.

Inicialmente el filtrado colaborativo presentaba el problema que las tenicas basadas unicamente en contenido eran inadecuadas para ayudar a los usuarios a encontrar documentos de interes, donde la busqueda por palabras claves inducia a errores de recomendaciones. Tapestry dio el primer paso en incorporar acciones de usuarios en una base de datos, denominado filtrado colaborativo activo. Un gran problema de esto, era la necesidad de que los usuarios se conocieran para saber en que opiniones o recomendaciones confiar.

Los principales usos de CF, de destinan a encontrar articulos de interes para los usuarios, temas en particulares, busqueda de usuarios similares, nuevos elementos, entre los mas importantes. Estos usos incorporan funcionalidades especificas, las cuales permiten a los usuarios mostrar listas de elementos recomendados en orden a su utilidad. Otra funcioanlidad son recomendaciones restringidas, donde se genera una recomendacion a partir de una combinacion de preferencias y requisitos.

El filtrado colaborativo es mas util en dominios con determinadas propiedades: 
- Distribicion de datos: Que existan muchos elementos a recomendar, con hartas calificaciones y que estas utlimas sean mucho mayor a los elementos.
- Significado subyacente: Que existan usuarios con gustos similares, cuyas evaluaciones tengan un caracter subjetivo personal. Ademas, los articulos a recomendar han de ser homogeneos.
- Persistencia de datos: Los articulos persisten en el tiempo, generando calificaciones en el largo plazo. Los grupos persisten y son homogeneos en el largo plazo.

A continuacion, se deja una tabla comparativa de ambos tipos de filtrados:

|Aspecto|   Filtrado colaborativo| Filtrado por contenido|
|---|---|---|
|   ¿Necesita calificaciones?|   Si|   	No|
|  ¿Necesita contenido?	|  No	|   Si	|
|   ¿Contenido de acceso?	|   Limitado	|   Abierto	|
|   ¿Novedad?	|   Alta	|   Baja	|

#### Algoritmos no probabilisticos
------
No se basan en modelos probabilisticos. El algoritmo de los vecinos genera recomendaciones en base a usuarios similares. Dentro del espacio de vecinos, se evalua el promedio de calificacion de un elemento. Sin embargo, un problema de esto es que hay usuarios mas similares a uno que otros. Ademas, los usuarios no consideran la escala de la misma manera.

La correlacion de Pearson se calcula comparando las calificaciones de todos los elementos evaluados tanto por el usuario c omo el vecino. Para aquellos muy de acuerdo, se estara mas cerca de 1, mientras que en caso opuesto estara mas cerca de -1.

Los algoritmos basados en elementos en vez de usuarios, buscan similitudes unicamente entre los items a recomendar. Para esto, se utiliza la matriz de recomendacion donde se predice la evaluacion de un usuario basado en la similitud entre items.

#### Algoritmos probabilisticos
-----
Representan explicitamente distribuciones de probabilidad cuando se calculan calificaciones pronosticadas. Estos buscan calcular la probabilidad de que dado un usuario y un articulo calificado, cual es el valor esperado de calificacion que ese usuario le dara al articulo. Una ventaja de estos algoritmos es que pueden producir una distribucion de probabilidad entre los posibles valores de calificacion, por lo qe no solo puede calcular la calificacion mas probable, si no que calcula la probabilidad ademas de que esta sea correcta.

Los principales inconvenientes nacen en las situaciones donde hay pocas calificaciones para los elementos. En base a esto, se recomienda descartar las entidades con pocas calificaciones, ayustar los calculos para estos casos o incorporar creencias previas las cuales implica incorporar calificaciones que coincidan con la distirbucion de probabilidad.

-----------
Las tareas de prediccion y recomendacion presentan diferentes requisitos. Las tareas de recomendacion requieren calculo de predicciones para muchos elementos, siendo muy costoso. Por otro lado, la tarea de prediccion para un articulo en particular, se guarda informacion del articulo, donde los mayores requisitos son a nivel de memoria.

Los algoritmos de CF generalmente eligen recomendar elementos con las calificaciones mas altas previstas. Las medidas de confianza son para cada algoritmo en particiular. Para los probabilisticos se utiliza la distribucion de probabilidad para estimar la confianza. Para aquellos algoritmos basados en usuario, utilizan la concordancia entre elementos en la vecindad de un usuario. Aquellos  basados en elementos, miden el  numero de calificaciones de pares relacionadas que contribuyen a una prediccion.

Un gran problema nace en el inicio de la implementacion de un CF. Ante esto, como inicialmente no se cuenta con informacion se hace todo un desafio el recopilar las calificaciones. Si bien, no se necesita muchas calificaciones para implementar un sistema de recomendacion, si se necesita un grupo pequeño que califique de manera continua. Ademas, es recomendable entregar incentivos a los usuarios para que califiquen, los cuales no necesariamente son economicos.

#### Evaluación
La  evalucion permite que tan bien cumple sus objetivos un filtrado colaborativo. Si bien, no existe una metrica bien aceptada, se puede elegir una dependiento del tipo de articulos que se recomienden.

- Precision: Esta evalua la magnitud del error entre el pronostico y la calificacion verdadera. El metodo estandar el el error absoluto medio (MAE) que es la diferencia promedio entre el pronostico y el real. Sin embargo esta medida es poco fiable ya que no distingue entre lista de recomendaciones clasificadas, donde si los primeros elementos son erroneos genera un costo mayor que los elementos en la parte mas inferior de la lista.

- Novedad: Capacidad de recomendar elementos que el usuario no conocia. 
- Cobertura: Porcentaje de elementos conocidos por el sistema CF para los cuales se generan predicciones.
- Tasa de aprendizaje: Mide la rapidez con la que el sistema realiza predicciones a medida que llegan datos.
- Confianza: Capacidad de un sistema CF para evaluar la calidad de sus predicciones.
- Metricas de satisfaccion: Medidas que buscan evaluar como el usuario percibe el sistema recomendador.
- Metricas de rendimiento:  Buscan medir cuanto afecto la implementacion del sistema recomendador. Por ejemplo, si el sitio genero mas ventas gracias a este CF.





------------
## Aspectos relevantes
------------
## Conclusiones
------------
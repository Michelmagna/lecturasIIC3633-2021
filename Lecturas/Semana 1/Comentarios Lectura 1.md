<div style="text-align: justify">

# Lectura Semana 1
### Título: "Collaborative Filtering Recommender Systems".
### Autores: J. Ben Schafer, Dan Frankowski, Jon Herlocker and Shilad Sen.
------------

# Resumen

El filtrado colaborativo es el proceso de filtrar o evaluar elementos utilizando las opiniones de otras personas o usuarios. Este concepto nace de situaciones cotidianas tradicionales, como durante el momento de compartir con una persona conversar respecto a intereses en cierto tema, como pueden ser películas, juegos, música, entre tantos.

El sitio web MovieLens utiliza CL para recomendar películas. Este se basa en dos calificaciones que se recopilan: Por un lado, las Calificaciones explícitas son las entregadas por el usuario. Por otro, las implícitas son las inferidas en base al comportamiento.

Inicialmente el filtrado colaborativo presentaba el problema que las técnicas basadas únicamente en contenido eran inadecuadas para ayudar a los usuarios a encontrar documentos de interés, donde la búsqueda por palabras claves inducía a errores de recomendaciones. Tapestry dió el primer paso en incorporar acciones de usuarios en una base de datos, denominado filtrado colaborativo activo. Un gran problema de esto, era la necesidad de que los usuarios se conocieran para saber en que opiniones o recomendaciones confiar.

Los principales usos de CF, de destinan a encontrar artículos de interés para los usuarios, temas en particulares, búsqueda de usuarios similares, nuevos elementos, entre los mas importantes. Estos usos incorporan funcionalidades específicas, las cuales permiten a los usuarios mostrar listas de elementos recomendados en orden a su utilidad. Otra funcionalidad son recomendaciones restringidas, donde se genera una recomendación a partir de una combinación de preferencias y requisitos.

El filtrado colaborativo es mas útil en dominios con determinadas propiedades: 
- Distribución de datos: Que existan muchos elementos a recomendar, con hartas calificaciones y que estas ultimas sean mucho mayor a los elementos.

- Significado subyacente: Que existan usuarios con gustos similares, cuyas evaluaciones tengan un carácter subjetivo personal. Además, los artículos a recomendar han de ser homogéneos.

- Persistencia de datos: Los artículos persisten en el tiempo, generando calificaciones en el largo plazo. Los grupos persisten y son homogéneos en el largo plazo.

A continuación, se deja una tabla comparativa de ambos tipos de filtrados:

|Aspecto|   Filtrado colaborativo| Filtrado por contenido|
|---|---|---|
| ¿Necesita calificaciones? |   Si|    No|
| ¿Necesita contenido? | No   |   Si |
|   ¿Contenido de acceso?   |   Limitado    |   Abierto |
|   ¿Novedad?   |   Alta    |   Baja    |

#### Algoritmos no probabilísticos
------
No se basan en modelos probabilísticos. El algoritmo de los vecinos genera recomendaciones en base a usuarios similares. Dentro del espacio de vecinos, se evalúa el promedio de calificación de un elemento. Sin embargo, un problema de esto es que hay usuarios mas similares a uno que otros. Además, los usuarios no consideran la escala de la misma manera.

La correlación de Pearson se calcula comparando las calificaciones de todos los elementos evaluados tanto por el usuario como el vecino. Para aquellos muy de acuerdo, se estará mas cerca de 1, mientras que en caso opuesto estará mas cerca de -1.

Los algoritmos basados en elementos en vez de usuarios, buscan similitudes únicamente entre los ítems a recomendar. Para esto, se utiliza la matriz de recomendación donde se predice la evaluación de un usuario basado en la similitud entre ítems.

#### Algoritmos probabilísticos
-----
Representan explícitamente distribuciones de probabilidad cuando se calculan calificaciones pronosticadas. Estos buscan calcular la probabilidad de que dado un usuario y un artículo calificado, cual es el valor esperado de calificación que ese usuario le dará al articulo. Una ventaja de estos algoritmos es que pueden producir una distribución de probabilidad entre los posibles valores de calificación, por lo que no solo puede calcular la calificación mas probable, si no que calcula la probabilidad además de que esta sea correcta.

Los principales inconvenientes nacen en las situaciones donde hay pocas calificaciones para los elementos. En base a esto, se recomienda descartar las entidades con pocas calificaciones, ayustar los cálculos para estos casos o incorporar creencias previas las cuales implica incorporar calificaciones que coincidan con la distribución de probabilidad.

-----------
Las tareas de predicción y recomendación presentan diferentes requisitos. Las tareas de recomendación requieren cálculo de predicciones para muchos elementos, siendo muy costoso. Por otro lado, la tarea de predicción para un artículo en particular, se guarda información de este, donde los mayores requisitos son a nivel de memoria.

Los algoritmos de CF generalmente eligen recomendar elementos con las calificaciones mas altas previstas. Las medidas de confianza son para cada algoritmo en particular. Para los probabilísticos, se utiliza la distribución de probabilidad para estimar la confianza. Por otro lado, aquellos algoritmos basados en usuario utilizan la concordancia entre elementos en la vecindad de un usuario. Finalmente, aquellos basados en elementos miden el numero de calificaciones de pares relacionadas que contribuyen a una predicción.

Un gran problema nace en el inicio de la implementación de un CF. Ante esto, como inicialmente no se cuenta con información se hace todo un desafío el recopilar las calificaciones. Si bien, no se necesita muchas calificaciones para implementar un sistema de recomendación, sí se necesita un grupo pequeño que califique de manera continua. Además, es recomendable entregar incentivos a los usuarios para que califiquen, los cuales no necesariamente son económicos.

#### Evaluación
La evalución muestra que tan bien cumpla sus objetivos un filtrado colaborativo. Si bien no existe una métrica bien aceptada, se puede elegir una dependiendo del tipo de artículos que se recomienden.

- Precisión: Esta evalúa la magnitud del error entre el pronóstico y la calificación verdadera. El método estándar es el error absoluto medio (MAE) que es la diferencia promedio entre el pronóstico y el real. Sin embargo, esta medida es poco fiable ya que no distingue entre lista de recomendaciones clasificadas, donde si los primeros elementos son erróneos genera un costo mayor que los elementos en la parte mas inferior de la lista.

- Novedad: Capacidad de recomendar elementos que el usuario no conocía. 
- Cobertura: Porcentaje de elementos conocidos por el sistema CF para los cuales se generan predicciones.
- Tasa de aprendizaje: Mide la rapidez con la que el sistema realiza predicciones a medida que llegan datos.
- Confianza: Capacidad de un sistema CF para evaluar la calidad de sus predicciones.
- Métricas de satisfacción: Medidas que buscan evaluar como el usuario percibe el sistema recomendador.
- Métricas de rendimiento:  Buscan medir cuanto afecto la implementación del sistema recomendador. Por ejemplo, si el sitio genero mas ventas gracias a este CF.

Los sistemas de navegación social, utilizan a un grupo de personas las cuales trabajan para ayudarse mutuamente en sus decisiones en la web. Por ejemplo, qué producto comprar o no, puede nacer por acciones o comentarios descritos por otros usuarios dentro del sitio. Toda información implícita que dejan los usuarios,  permite posteriormente afectar la decisión de compra o recomendación hacia una persona.

#### Desafíos
- Privacidad y seguridad: Los sistemas CF necesitan información de los usuarios. En estricto rigor, mientras mas información se tenga del usuario mejores predicciones se pueden realizar. Ante esto, es muy importante para los sistemas CF contar con una arquitectura que garantice confianza de sus usuarios, con el objetivo que no les roben su información personal para fines negativos y proteger esta información ante ataques externos.

- Confianza: Un gran inconveniente son las calificaciones no representativas en sus preferencias. Esta es una vulnerabilidad que sigue siendo un desafío, ya que grupos organizados mal intencionados podrían por sus acciones afectar el sistema recomendador.

------------
# Aspectos relevantes a discutir
Los sistemas recomendadores han evolucionado con el objetivo de mejorar sus predicciones para entregar recomendaciones mejores a los usuarios. Los sistemas basados en contenido tienen un sesgo muy importante, donde la recomendación por palabras claves puede ocasionar malas recomendaciones. Este es sumamente interesante ya que entrega una oportunidad de análisis diferente. ¿Que pasaría si se analizara el contenido de un escrito por completo y se comparara con otro?. Si bien, actualmente esta tarea se puede realizar con software lectores de texto inteligentes basados en redes neuronales convolucionales, resulta muy costoso en la práctica cada iteración. Esta limitante es clave ya que si bien, un análisis completo de los escritos permitiría una mejor recomendación, la limitante del costo de ejecución resulta un impedimento en que esta recomendación puede ser escalable. Sumado a esto, esta alternativa resulta viable con pocos elementos, sin embargo mientras mas elementos se deban comparar con otros, mayor es la complejidad del sistema a la hora de recomendar.

El filtrado colaborativo tiene la necesidad de contar con calificaciones. En base a lo anterior, se recomienda en el documento leído contar con propiedades en su dominio que garantizan un mejor sistema recomendador. Ante esto, es importante que los datos tengan una persistencia en el tiempo abriendo un importante punto a destacar, ya que en caso contrario puede existir un sesgo dado los cambios culturales dentro de la sociedad. Por ejemplo, antes la sociedad tenia una visión mucho menos crítica del machismo y la violencia, que si bien siempre han sido repudiables eran menos conversados que hoy en día. En base a esto, películas como 500 Sombras de Gray o Tres Metros Sobre el Cielo, tuvieron muchas criticas positivas y se hicieron muy populares. Sin embargo, en el último tiempo, se han considerado este tipo de películas como representaciones machistas las cuales ya no son bien vistas en la sociedad en niveles generales, ocasionando que las críticas tengan un cambio radical de positivas a negativas mientras avanza el tiempo. Por lo tanto, los sistemas recomendadores han de evolucionar sus recomendaciones en base al avance del tiempo, ya que considerar críticas antiguas puede ocasionar recomendaciones equivocadas dado el cambio de contexto cultural dentro de la sociedad y sus personas.

Para iniciar un sistema CF, el frío inicio por la falta de información puede ralentizar las recomendaciones a entregar a nuevos usuarios. Ante esto, el texto discute los diferentes incentivos para que los usuarios entreguen calificaciones. En mi opinión, los incentivos económicos son aquellos que entregan siempre mayores beneficios, resultando en un parámetro considerado de manera inadecuada en el escrito. Si nos dejamos llevar por la teoría económica, un incentivo monetario esta comprobado que implica una mejora en el desempeño en cierta tarea (Patricio Madrid, 2013). Entonces si bien, no debiese ser la primera opción de incentivo, puede ser una recomendación en caso de contar con un alto capital inicial, con el objetivo de buscar información lo antes posible para lograr que el sistema recomiende mejor antes. Finalmente, si el sistema genera mejores recomendaciones lo antes posible, podría generar que los usuarios se sientan mas atraídos en el sitio. Por otro lado, si se generan malas recomendaciones al principio de la interacción del usuario, puede que este evalúe negativamente el sitio y finalmente no regrese a este. Todo esto ultimo depende de cuanto valoriza la velocidad de predicciones quienes implementan el sistema recomendador, donde una alta valoracion sumado a un alto capital inicial, puede ocasionar en decidir entregar incentivos económicos.

Algunos importantes parámetros no definidos en el texto, son acerca de cantidades que definan la cantidad de datos suficientes para generar predicciones y recomendaciones. Ante esto, queda incierto respecto a cuál horizonte es el adecuado para que los sistemas recomendadores, mediante métodos probabilísticos o no pudieran entregar recomendaciones adecuadas. Este punto se debió haber considerado tanto en la sección de algoritmos como evaluación, ya que es relevante tener una definición inicial respecto al horizonte de calificaciones necesarias, comprobadas en lo empírico para lograr buenas recomendaciones con ejemplos teóricos o reales en el documento.

Si bien en la sección de métricas el documento discute distintos tipos de estas, únicamente define matemáticamente la precisión. Además, no se evidencia las fórmulas o procedimiento para evaluar esta métrica en el sistema. Por lo tanto, una mejora al documento leído es modificar la sección de métricas entregando más información del procedimiento de cálculos, entregando ejemplos que permitan evidenciar de mejor manera aquello que se quiere obtener.

Los desafíos propuestos son sumamente importantes al implementar un sistema recomendador. Si el usuario no confía en el sistema, puede ocurrir que la información entregada no sea verdadera o que simplemente no entregue información. En base a lo anterior, es un punto muy importante en el inicio de la implementación del sistema, por lo que se debe profundizar más dada su relevancia. Por ejemplo considerar el desafío de medir bajo una métrica la confianza de los clientes, donde a largo plazo se busque reducir lo mas posible la tasa de desconfianza de los usuarios con el sistema. Esto último es un caso que ha afectado mucho a empresas como Facebook, donde la desconfianza generada en el último tiempo ha reducido los usuarios activos que usan el sistema. Finalmente, enfatizar la trasparencia de lo que se busca hacer con la informacion de los usuarios es importante pra garantizar la cofianza entre el sitio y el usuario.

Un punto importantísimo para destacar mencionado en el documento, es respecto a la veracidad de las calificaciones que entregan algunos usuarios. El "Review bombing" es un fenómeno de internet donde grandes grupos de usuario se ponen de acuerdo para evaluar positiva o negativamente un elemento. Esto ocasiona que las calificaciones entregadas tengan un gran sesgo ocasionando recomendaciones futuras negativas. Un ejemplo reciente es el caso del juego "The last of Us 2". Si bien, la critica especializada evaluó muy positivamente el juego junto con un enorme grupo de usuarios, grupos de pusieron de acuerdo para atacar negativamente sus reseñas. Esto se explicaba por escenas lésbicas que el juego mostraba que generaron que muchos usuarios rechazaran esto por sus ideales. En base a lo anterior, el documento toca una problemática muy importante que aun varios años después de la publicación del escrito, no tiene una solución que pueda evitar esta situación.

Finalmente, las grandes limitaciones que se tienen en el procesamiento de la información son las capacidades a nivel CPU y RAM de los sistemas que contienen los CF. Si bien, en el último tiempo han mejorado significativamente los ordenadores, estos aun son limitados a la hora de manejar procesos complejos con grandes volúmenes de datos. Ante esto, el documento leído no explica con ejemplos prácticos la ejecución de algoritmos de predicción ni la cantidad de datos utilizados. Esto habría repercutido en mencionar la capacidad a nivel de hardware del ordenador utilizado, entregando una primera impresión respecto a requerimientos informáticos para ejecutar un sistema CF.
# Conclusiones

El documento leído es sumamente útil para introducir al lector a una idea respecto al filtrado colaborativo. Explica detalladamente su definición, requerimientos, funcionalidades y conceptos matemáticos detrás de manera muy teórica. Ante esto, resulta muy útil para abarcar una primera impresión respecto a la utilidad e historia del filtrado colaborativo. Sin embargo, habría sido muy útil ejemplificar con situaciones teóricas o prácticas los diferentes puntos para implementar un sistema CF y calcular sus métricas de rendimiento y precisión.

Los filtrados colaborativos tienen la gran dependencia de requerir evaluaciones para su funcionamiento. Esto ocasiona una gran dependencia del comportamiento de los usuarios, donde es necesario que entreguen calificaciones para mejorar la recomendación de los sistemas. Esto finalmente repercute en vulnerabilidades ocasionadas por la veracidad de la información, organización de grupos de usuarios, cambios de contexto culturales, entre algunos que pueden ocasionar un sesgo que repercuta en recomendaciones equivocadas.

Finalmente, los sistemas CF han sido muy aplicados por grandes empresas como Netflix, Amazon o Mercado libre para recomendar productos o películas. Es importantísimo seguir avanzando en la investigación de estos sistemas, ya que si bien han mejorado su rendimiento y recomendaciones, los problemas mencionados en el documento aun siguen vigentes años después de su publicación.
</div>
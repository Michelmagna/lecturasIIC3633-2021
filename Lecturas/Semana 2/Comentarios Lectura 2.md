<div style="text-align: justify">
# Lectura Semana 2
### Título: "Matrix Factorization Techniques for Recommender Systems".
### Autores: Yehuda Koden, Robert Bell and Chris Volinsky
------------

# Resumen
El documento leído explica la importancia de la factorización matricial como una técnica superior a la del vecino mas cercano para generar recomendaciones en productos que les interesen. Los sistemas de recomendación son sumamente útiles en diversos productos como películas, música o programas de entretenimiento, en donde los clientes pueden indicar su grado de satisfacción en base a calificaciones.

Los sistemas de recomendación se basan en crear un perfil para cada usuario o producto, en base a su naturaleza o características. En base a esto, el filtrado por contenido se encarga se relacionar productos con clientes de características similares. Una alternativa a esto es el filtrado colaborativo, el cual se enfoca en las relaciones entre usuarios y las dependencias entre los mismos usuarios para identificar asociaciones usuarios - elementos. El gran problema de esta técnica, es que requiere de información previa de usuarios y calificaciones para generar recomendaciones. Ante esto, se denomina el inicio frio al problema de no contar con calificaciones para crear perfiles de nuevos productos y clientes.

La gran novedad del documento, es la técnica de factorización de matriz versus las previamente mencionadas. Esta caracteriza a los elementos como usuarios mediante vectores inferidos en los patrones de calificación de los elementos. Esto necesita calificaciones explicitas de los usuarios con el objetivo de dimensionar el patrón de preferencias. Sin embargo, la gran ventaja de esta técnica es que logra predecir retroalimentación implícita, reflejando indirectamente la opinión de un cliente por un elemento.

Se evidencian los conceptos matemáticos detrás de la factorización matricial, así como las técnicas algorítmicas utilizadas tales como gradiente de descenso y mínimos cuadrados. Sumado a lo anterior, se exponen los sesgos ocasionados por los tipos de datos flexible que acepta el método de factorización matricial. Además, el método debe presentar dinámica temporal en donde pueda modificar sus valores en base al avance del tiempo. Por ejemplo, los gustos de las personas pueden verse afectados por factores externos que impliquen en después de cierto delta de tiempo, la preferencia baje o suba.

Finalmente, el documento leído muestra el caso del Netflix Prize el cual consistía en buscar un equipo que mejorara un 10% el sistema recomendador que contaba actualmente. Este caso permitió evidenciar como la técnica de factorización matricial evidencia mayor precisión que las técnicas del vecino mas cercano.

------------
# Aspectos relevantes a discutir

El documento leído resulta sumamente interesante a la hora de considerar nuevas metodologías de recomendación. Resulta increíble como las diversas técnicas trabajadas en el filtrado colaborativo, pueden repercutir en sistemas inteligentes capaces de obtener predicciones tanto con información explicita como implícita. Esto ultimo, resulta sumamente llamativo ya que día a día realizamos conductas implícitas o sin darnos cuentas que entregan información a un sistema. Debido a lo anterior, no es raro que en pocos segundos generando acciones, sitios web actuales entreguen rápidamente recomendaciones de canciones o productos a uno como usuario. Es un tema delicado y muy apasionante, en donde hay que generar sistemas con responsabilidad y usar de buena manera la información de los clientes o usuarios.

Una opinión que hay que mencionar respecto al documento, es que faltó transparentar de mejor manera los ejemplos mediante los cuales se probaron los algoritmos de factorización matricial. Por ejemplo, mencionar la base de datos utilizada, resultados obtenidos de aquellas predicciones, áreas en las cuales se aplico esta técnica, entre algunas. Si bien, se maneja de muy buena forma el aspecto matemático y teórico, se genera un grado de ansiedad al no contar con ejemplos reales y resultados que respalden fuertemente lo comentado en el documento. Esto es muy útil para ejemplificar el lado teórico aplicado a ejemplos reales, donde el lector pueda imaginarse situaciones cotidianas en las cuales aplicar lo aprendido.

Un punto para destacar del documento, es respecto a la evolución temporal de los datos. En tiempos actuales, donde la información fluye muy rápido de un lado del planeta a otro, diversas situaciones externas a los productos afectan drásticamente los gustos de los usuarios. Tal como menciona el texto, si un actor de cine en principio ocasionaba que algunas películas fueran muy famosas resulta involucrado en un delito o acción indebida, el gusto de los usuarios puede verse afectado fuertemente. Un ejemplo muy atingente es el del actor Johnny Depp. Este actor se hizo extremadamente popular por las películas piratas del caribe y otras, posicionándolo como uno de los mas populares. Debido a la denuncia de su pareja por violencia intrafamiliar de Depp, su reputación bajo considerablemente en todos los medios. Sin embargo, al momento de declarar la fiscalía su inocencia se armaron muchísimas campañas a su favor que le regresaron su enorme popular. Finalmente, podemos notar cuan importan factores externos en los gustos de los usuarios, los cuales afectan las recomendaciones del sistema y respaldan la importancia de considerar la evolución temporal de los datos.

Finalmente, el ejemplo del Netflix Prize habría sido interesante ahondarlo un poco mas dado lo cotidiano que resulta para los usuarios una empresa de este tipo. En base a esto, podría haberse explicado mejor los resultados del concurso y experiencias de los participantes respecto a las técnicas utilizadas con mayor profundidad. Por ejemplo, se podría haber ejemplificado la base de datos que utilizaron mediante tablas y gráficos para que el lector se familiarice mejor con esto.

# Conclusiones

El documento leído resulta muy útil para el lector al momento de conocer la factorización matricial. Podemos concluir que la evolución de estos métodos en el filtrado colaborativo, esta potenciando sistemas aun mas inteligentes con el paso del tiempo. Por lo tanto, es relevante incorporar y evolucionar nuevas metodologías que busquen potenciar aun mas los sistemas recomendadores de grandes empresas, como pueden ser Netflix o Amazon.

La ultima conclusión viene siendo respecto al aporte del documento leído al lector. Se puede concluir que es un documento sumamente útil para personas que incluso no están familiarizadas con las matemáticas y la computación. Es sumamente claro y permite al lector entender conceptos de filtrado colaborativo de manera simple y didacta, resultando una lectura muy amigable e interesante para el lector.

</div>

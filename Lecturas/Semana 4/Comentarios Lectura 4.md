<div style="text-align: justify">

# Lectura Semana 4
### Título: "Content-Bases Recommendation System".
### Autores: Michael J. Pazzani and Daniel Billsus
------------

# Resumen
EL documento leído analiza los sistemas de recomendación basados en contenido, o sea aquellos que se basan en la descripción de un ítem y un perfil de los intereses de usuarios.

Tradicionalmente los elementos a recomendar se almacenan en una base de datos. Estos se almacenan con atributos, los cuales poseen información descriptiva de los ítems. Es más sencillo trabajar con textos no restringidos ya que poseen atributos definidos. Las noticias son datos estructurados sin valores definidos que complejizan su uso en recomendaciones. En base a esto, una idea es convertir cada palabra a un atributo, donde puede ser un booleano o un entero contando sus reiteraciones. Sin embargo, pueden existir problemas como incluir oraciones con texto no representativo de un lugar (por ejemplo la palabra vegetariano en un restaurant de carnes) impliquen errores en la recomendación. Una variante podría ser utilizar palabras contiguas que intenten envolver mejor la descripción.

La mayoría de los sistemas utilizan un perfil de intereses de usuario. Por ejemplo un modelo de preferencias que es una descripción de elementos que interesan. Otro podría ser un historial del usuario con el sistema recomendador. Este ultimo podría ser los ultimas búsquedas en el sistema o filtrar por contenidos ya comprados o leídos. Esto tiene dos problema: requiere esfuerzo del usuario y la recomendación no es entregada en orden. Otro tipo de recomendación es basada en agregar ítems a favoritos, donde el sistema por detrás busca emparejar elementos similares.

Para crear un modelo de preferencia a partir del historial de usuario, se debe generar datos de clasificación de elementos que le gustan y que no. En base a esto, se hace una calificación por contenido o aquellas calificaciones explicitas del usuario que permiten evidenciar si le gusta un ítem.

Una técnica interesante mencionada en el documento es respecto a los arboles de decisión, que mediante ramas permite tomar caminos que rápidamente creen un perfil de usuario, clasificando rápidamente intereses de este.

El método del vecino más cercano, busca clasificar elementos comparándolos con otros mediante la función de similitud, lo cual permite clasificar al usuario con otros similares.

La retroalimentación de relevancia es un método que busca refinar en forma incremental las consultas basadas en resultados anteriores. El algoritmo de Rochio es ampliamente utilizado ya que se basa en modificar una consulta inicial a través de prototipos ponderados de forma diferente en documentos que pertenecen a la misma clase o tipo.
Un método probabilístico muy popular es el bayesiano, el cual tiene muy buen rendimiento para la clasificación de texto, que toman la ocurrencia de palabras en los ítems y permiten considerarlos ensayos independientes extraídos de una distribución de probabilidad multinomial.

Si bien, se han mencionado muchos enfoques de recomendación basada en contenido, ninguna funciona correctamente si el contenido no tiene suficiente información para distinguir los elementos que le gustan al usuario de los que no le gustan. Para la información estructurada, que tiene atributos podría darse el caso de un mejor contenido basado en comentarios y opiniones escritas de otros usuarios.

------------

# Aspectos relevantes a discutir

El documento menciona diferentes enfoques respecto a los sistemas recomendadores basados en contenidos. Esto resulta muy relevante, ya que si bien ciertos elementos pueden tener calificaciones en puntos que pueden ser atractivas, el comportamiento humano es muy influenciado por parámetros que no necesariamente se reflejan en una puntuación. Ante esto, comentarios que mencionan advertencias que pueden implicar que un producto es muy útil y a la vez muy riesgoso, personas muy aversas al riesgo podrían encontrar que por más bien evaluado se encuentre el elemento no sea de su gusto, ocasionando una recomendación errónea.

Un punto interesante a discutir complementando el párrafo anterior, es como las tendencias pueden afectar rápidamente la noción de gusto de una persona. Por ejemplo, un accidente debido a un producto defectuoso como un celular de cierta marca, posiblemente ocasione un miedo en las personas en consumir este producto. En base a esto, no se menciona en el documento como los sistemas podrían adaptarse rápidamente a las tendencias del entorno del usuario que afecten su decisión. Debido a lo anterior, se puede considerar que los sistemas sean muy sensible a estas situaciones que converjan en recomendaciones erróneas hacia ciertos usuarios.

Es de suma relevancia a la hora de comentar enfoques de recomendación, lograr ejemplificar esto con casos reales o aplicados en teóricos. En base a aquello, no queda bien definido como un sistema basado en contenido requiere suficiente información para funcionar bien. Por ejemplo, una prueba respecto a cuantos comentarios se requieren para lograr una buena recomendación, da un inicio en la perspectiva respecto a cuanta información es necesaria para implementar un sistema correctamente. Si bien, este punto se menciona como una advertencia que comparto plenamente, resulta intrigante evaluar mediante métricas respecto a cuanta información en texto podría ser relevante para reducir errores en las recomendaciones.

Finalmente, el documento al entregar diversas aristas de la recomendación basada en contenido, permite reflexionar mucho en como las acciones o comentarios de los usuarios pueden involucrar recomendaciones a otros. Debido a esto, normalmente uno olvida comentar productos comprados que sean buenos o malos. Si bien, la evaluación en números da una intuición inicial, normalmente personas similares a uno pueden comportarse similares si leen experiencias y comentarios que detallen mucho mas un elemento que simplemente una calificación numerada. En base a esto, la recomendación basada en contenido puede ser mucho más completa y fiable en caso de aplicarse eficientemente a la hora de recomendar elementos a los usuarios en una apreciación personal.

------------

# Conclusiones

Los sistemas recomendadores basados en contenidos abarcan muchas más aristas que lo que representa una calificación numérica. Debido a esto, se puede concluir que es una recomendación más completa en caso de que el sistema funcione correcta y eficientemente. Por lo tanto, la recomendación resulta ser mucho más personalizada debido al contenido de texto involucrado que recoge muchas más características que una evaluación.

En base a los escritos y aspectos discutidos, podemos concluir que una recomendación basada en contenido es sumamente sensible a bruscos cambios en las tendencias. Al no mencionar aspectos que eviten situaciones externas, permite concluir que las situaciones informativas externas al sistema recomendador, afecta drásticamente la perspectiva de gusto de un usuario. Por lo tanto, las recomendaciones basadas en contenido pueden tener situaciones de fallo debido a aspectos completamente externos, que no necesariamente sean por falta de información en el sistema o un algoritmo de recomendación defectuoso.
Finalmente, la recomendación basada en contenido resulta ser muy interesante y útil en la practica. Como usuario final me parece importantísimo que la opinión de usuarios similares sea importante a la hora de generarme recomendaciones. Por lo tanto, se concluye que la información entregada tanto como uno como usuario como el resto permite mejorar la experiencia de recomendación para uno como usuario final, logrando mejores aciertos en las recomendaciones ya que las calificaciones no necesariamente abarcan una completa expresión de gusto o desagrado por un producto en particular.

</div>

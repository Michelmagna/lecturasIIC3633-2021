<div style="text-align: justify">

# Lectura Semana 3
### Título: "Evaluating Recommendation Systems".
### Autores: Guy Shani and Asela Gunawardana
------------

# Resumen
El documento leido tiene como enfoque principal, discutir respecto a como comparamos los sistemas recomendadores basados en múltiples propiedades a seleccionar. En base a lo anterior, considerando métricas a discutir próximamente se pueden generar una evaluación de que tan bien funciona la predicción del sistema recomendador implementado.

Tradicionalmente es fácil experimentar utilizando datos de usuarios existente y protocolos para evaluar el rendimiento, como la precisión de la predicción. Una opción mas costosa es un estudio de usuarios, donde se pide que un pequeño conjunto de estos realicen tareas en el sistema y responder preguntas. Finalmente, se podría implementar experimentos en líneas con usuarios ajenos. Antes de cualquier experimento, es importante definir la hipótesis a aprobar o rechazar. Luego, se debe tener un control de variables donde en el experimento para diferentes algoritmos sean fijas. Finalmente, luego de los resultados existe la posibilidad de generalizar estas conclusiones, las cuales a mayor diversidad de la información utilizada mas podemos generalizar nuestros resultados.

Los estudios de usuarios buscan recopilar información en base a la interacción con el sistema. Se pide que realicen diversas tareas interactivas en donde se busca recopilar el comportamiento en medidas cuantitativas como cuales tareas completó. Además, se pueden considerar variables cualitativas con preguntas respecto a si fue fácil la tarea a realizar o no. Su gran ventaja es que permite abordar grandes aspectos del comportamiento del usuario, considerando aspectos cualitativos. Sin embargo, estos resultan costosos por la cantidad de sujetos necesarios para las pruebas y si se piden realizar múltiples tareas resulta costoso en tiempo. Complementando lo anterior, es importante que los usuarios representen fielmente a la población de usuarios del sistema final. Sin embargo, un problema podría ser que si los usuarios son consientes de participar en un experimento no se comporten como usuarios reales.

Las evaluaciones en línea utilizan usuarios reales con sistemas recomendadores reales. En estos se evalúa el comportamiento del usuario ante múltiples sistemas de recomendación, donde se evalúa además el efecto en el comportamiento al modificar el algoritmo detrás del sistema. Es clave muestrear usuarios al azar para que las comparaciones sean equitativas. además, si la métrica importante es la precisión hemos de mantener fija la interfaz del usuario. Una desventaja de esto puede ser que al modificar el sistema de prueba los usuarios se disuadan de este.

En cualquier experimento de evaluación, es importante estar seguros de que el candidato recomendador sea una buena opción para datos aun no vistos que los usuarios se enfrentarán en el sistema futuro a implementar. Para sacar conclusiones, el documento propone evaluaciones comparativas entre algoritmo como la confianza en base al valor-p, la prueba de t-Student, intervalos de confianza, entre las mas tradicionales. 

El documento explica las propiedades de los sistemas de recomendación importantes a considerar. 

####  **1. Preferencia**
En primer lugar, se presenta la preferencia del usuario en donde eligen cual sistema fue el que le pareció mejor. Esta consulta a los usuarios cual sistema utilizado en los experimentos fué el que entregó mejores recomendaciones y resultó mas útiles para ellos.

####  **2. Precisión**
La segunda, es la más popular en la literatura sobre los sistemas recomendadores: evaluar la precisión del sistema. En base a esto, se evalúa que tan bien el sistema predijo la calificación del usuario. Para esto, se presentan medidas como el Error cuadrático medio(RMSE) y Error medio absoluto (MAE). Además, se presenta unas medidas d predicción de uso, donde si bien no importa la calificación del usuario es importante que el usuario al menos vea o agregue a la cola una nueva película. Otro punto son las medidas de calificación, donde si bien no importa predecir la calificación explicita, importa ordenar los elementos según preferencias del usuario al momento de recomendar.

####  **3. Cobertura** 
La tercera, viene siendo la cobertura la cual se entiende como la proporción de elementos que el sistema de recomendación puede recomendar. La mas simple viene siendo el porcentaje de elementos que se recomiendan en el experimento. Otra cobertura vendría siendo la cobertura de espacio de usuario, que es la proporción de usuarios o interacciones a los cuales el sistema puede recomendar. Aquí es importante que esta se puede medir por la cantidad de información que entrega el usuario, donde para el filtrado colaborativo se puede considerar el numero de elementos que el usuario debe calificar antes de recibir recomendaciones.

####  **4. Confianza** 
La cuarta propiedad es la confianza, que se define como la confianza del sistema en sus recomendaciones o predicciones. Normalmente esta aumenta en base a mayor cantidad de datos con los que cuente el sistema. En base a esto, un usuario puede beneficiarse al observar un sistema con alta confianza.

####  **5. Confianza Usuario** 
La quinta propiedad es la confianza del usuario a las calificaciones que el sistema entregue. Esto se llama también "credibilidad del sistema" donde el usuario al evaluar recomendaciones que le gusten o conozcan, puede generar un beneficio hacia su persona.

####  **6. Novedad** 
La sexta propiedad es la novedad. En base a esto, si las recomendaciones son novedosas y no conocidas por el usuario, los usuarios pueden tener un beneficio si se les recomiendan elementos desconocidos. Aquí es importante generar un filtrado de películas que ya haya visto o conoce. Esto se puede evaluar mediante una pregunta directamente el usuario.

####  **7. Serenidad** 
La séptima viene siendo la serenidad, la cual se enfoca en ser una medida de cuan sorprendente resulta ser una recomendación exitosa. Se puede pensar como la cantidad de información relevante que es nueva para una recomendación. Por ejemplo, recomienda una película de un actor que el usuario le gusta mucho y no conoce.

####  **8. Diversidad** 
La octava viene siendo la diversidad. Típicamente recomendar elementos muy parecido puede no ser muy útil para el usuario. En base a esto, se puede medir la similitud en base al contenido de elemento, donde si un usuario desea paquetes de vacaciones, resulta mejor recomendar elementos en distintas ubicaciones que elementos en la misma ubicación.

####  **9. Utilidad** 
La novena viene siendo la utilidad, donde medir esto se basa en cuanta utilidad aumento la implementación del sistema de recomendación que organización que lo incorporo. Estas podrían enfocarse en un aumento del consumo del usuario o aumento del promedio de sus calificaciones, donde mejores calificaciones entregadas signifique una mayor utilidad para el sistema.

####  **10. Riesgo** 
Por ejemplo al recomendar acciones de la bolsa, hay usuarios mas reacios al riesgo que otros. Aquí no solo buscamos evaluar el valor generado por la recomendación, si no que minimizar el riesgo de esta al momento de ser tomada por el usuario.

####  **11. Robustez** 
La robustez es la estabilidad de la recomendación en presencia de información falta generada a propósito para influir en las recomendaciones. Por ejemplo, un dueño de hotel podría calificar muy positivo todo lo que ofrece su empresa. Esta medida es compleja de implementar ya que resulta complejo evitar ataques maliciosos. Una opción es simular ataques de información falsa asumiendo su existencia previamente.

####  **12. Privacidad** 
Es muy relevante que los usuarios se sientan seguros con la información que entregan, entregando privacidad a su información para que ningún tercero pueda utilizarla maliciosamente.

####  **13. Adaptabilidad** 
La adaptabilidad significa que el sistema de recomendación debe operar en entornos cambiante rápidamente, como los sistemas de noticias que duran en cortos plazos.

####  **14. Confianza** 
La escalabilidad implica que los sistemas recomendadores deben proporcionar resultados rápidos inclusos para mayores volúmenes de datos que los iniciales. En base a esto, el sistema no debe volverse mas lento ni ineficiente al momento de ir creciendo los datos con el tiempo.

------------
# Aspectos relevantes a discutir
El documento leido resulta ser una útil guía para evaluar los algoritmos de recomendación y seleccionar el mejor posible. Como hemos visto en la literatura, diversas alternativas algorítmicas permiten generar recomendaciones, cada una con sus ventajas y desventajas. En base a esto, el documento presenta muchos aspectos a considerar para generar experimentos y evaluarlos posteriormente. Si bien, se expone mucho desde el lado teórico, el documente carece de experimentos en situaciones reales que ejemplifiquen las evaluaciones trabajadas en este. Podría por ejemplo haberse evidenciado un caso real donde se tuviera una lista de algoritmos, exponer resultados de las mediciones realizadas y explicar la decisión de cual algoritmo seleccionar. En base a esto, queda un gran gusto al lector de ahondar y descubrir casos donde lo leido haya sido aplicado y notar el actuar de los autores y coautores.

Continuando la línea del párrafo anterior, un punto a destacar y reflexionar es como la experiencia del usuario puede afectar la evaluación del sistema. Por ejemplo, el algoritmo detrás podría ser muy preciso en sus predicciones y ser el que definitivamente ganaría frente a otros. Sin embargo, acompañado de una mala interfaz puede ocasionar sesgos importantes en las evaluaciones, donde las malas experiencias del usuario e incomodidad con el sistema concluyan en que abandone el sistema y deje de ocuparlo. Es muy importante preocuparse de la experiencia del usuario como una clave para el éxito, donde una experiencia positiva pueda permitir tener evaluaciones mas fidedignas y correctas en base a una experiencia correcta por parte de este. Lo mencionado no solo aplica para un sistema recomendador, sirve también para aplicaciones, redes sociales, sistemas ERP, sitios web de compra, entre muchos otros.

Las trece propiedades expuestas resultan sumamente importantes a considerar en un sistema recomendar e incluso cualquier sistema de información que trabaje con usuarios. Puntos como la seguridad de los datos, el gusto de los clientes por el sistema, escalabilidad y adaptabilidad, son variables que cualquier aplicación con la cual interactuamos deben manejar profundamente. Sin estos puntos, ninguna aplicación como Facebook o Instagram serian confiables para los usuarios ni habrían durado tantos años. Esto mismo genera un cuestionamiento en el lector, en como las políticas de esta gigante empresa como Facebook ha sido tan cuestionada muchas veces. Cuando se maneja información tan sensible, donde múltiples usuarios podrían ocasionar acciones maliciosas, el riesgo y la seguridad de esto debe ser aun mayor cada día. En base a esto, generar medidas que avancen en seguridad de un sistema, permite hacerlo mas escalable con el tiempo y mejorar la confianza de los usuarios, tanto para un sistema recomendador como una aplicación o un sistema informático completo.

------------
# Conclusiones

Los sistemas recomendadores en sus experimentos previos, pueden contar con múltiples variables a la hora de evaluar el mejor algoritmo. Resulta importante que además de la precisión de las predicciones, la experiencia de los usuarios sea positivas para que los experimentos entreguen resultados correctos. En base a esto, se concluye que todo sistema recomendador debe ser acompañado con una parte enfocada a los aspectos técnicos de los algoritmos detrás y un aspecto técnico que potencie la experiencia del usuario para obtener datos lo mas verídicos posibles.

La serie de propiedades expuestas en el documento leido, son importantísimas de considerar tanto para sistemas recomendadores como cualquier sistema tecnológico que desarrollemos. Tal como mencionamos antes, el usuario es el eje central que permite que los sistemas tengan éxitos al largo plazo. Debido a esto, temas de seguridad, escalabilidad, adaptabilidad entre las mas a destacar, son propiedades que no deben ser ignoradas en ningún momento si de desea evaluar el éxito al momento de implementar un sistema tecnológico o recomendador en el caso del escrito leido.

</div>

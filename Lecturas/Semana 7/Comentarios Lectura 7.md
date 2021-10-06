<div style="text-align: justify">

# Lectura Semana 7
### Título: "Interactive recommender systems: A survey of the state of the art and future research challenges and opportunities".
### Autores: Chen He, Denis Parra, Katrien Verbert
------------

Resumen
 
Los grandes esfuerzos en los sistemas recomendadores están orientados en la experiencia del usuario con el sistema. En base a esto, la  buena experiencia busca que las interacciones sean transparentes con el sistema para que pueda lograr recomendaciones adecuadas. Los problemas más tradicionales nacen del Inicio Frío de los sistemas, la comprensión de "caja negra" donde el usuario no comprende la lógica detrás produciendo desconfianza. Para estos temas, en los últimos años la investigación se centra en que más allá de la precisión del sistema, lograr combinar técnicas de visualización interactiva con el objetivo de transparentar la recomendación.
 
El documento menciona las diversas técnicas de recomendación basada en filtrado colaborativo con recomendaciones explícitas o implícitas, filtrado por contenido o sistemas híbridos, haciendo hincapié además de la recomendación basada en contexto. Para los diversos problemas de los sistemas el documento menciona técnicas de visualización, la cual se centra en permitir a los usuarios controlar el proceso de navegación a través de los espacios de información de forma flexible. Esta se basa en el diseño de representaciones visuales interactivas efectivas y eficientes que los usuarios pueden manipular para resolver tareas específicas. En base a aquello, se proponen integrar técnicas de visualización y recomendación para crear un ciclo de retroalimentación.
 
Los principales objetivos de la visualización son la transparencia de la caja negra, al explicar la lógica del sistema. Justificación en base a comprender el por que el usuario activo obtiene esas recomendaciones. Controlabilidad en donde la participación del usuario aporte en el proceso de recomendación. Diversidad en donde se proporcionan recomendaciones con una gran cobertura del espacio. Inicio fresco donde la problemática del problema de inicio del sistema requiere muestras iniciales.
 
El texto expone diversas técnicas de visualización, precisamente siete grupos.
1.  Enlace de nodo, los cuales representan usuarios, contenido o recomendaciones. Las conexiones o enlaces conectan elementos con los datos para explicar finalmente la procedencia de la recomendación.

2.  Visualización de conjunto, donde se agrupan elementos con puntos en común.

3.  Visualizaciones radiales, donde se utilizan nodos con relaciones padre-hijo como los intereses mediante palabras claves.

4.  “Tables” representa relaciones entre recomendación y variables que explican esto.

5.  Musicube utiliza un gráfico de dispersión que representa las calificaciones de los usuarios y las recomendaciones con puntos de colores, identificando correlación entre lo recomendado y la calificación que el usuario da.

6.  Iconos, donde iconos animados buscan representar emociones que signifiquen preferencias.

7.  Paris, usa un diagrama de flujo para indicar que información del perfil de usuarios se utiliza en qué orden para generar recomendaciones.
 
Finalmente, el documento concluye en que es útil mostrar un marco de visualización interactivo que permita a los usuarios tener una mejor experiencia con los sistemas y tener conocimiento del origen de sus recomendaciones. La mayor parte del tiempo, el enfoque es la transparencia y controlabilidad del proceso de recomendación.
 
------------
 
# Aspectos relevantes a discutir

El documento hace hincapié en aquello que los usuarios interactuamos en el aspecto visual con un sistema. Resulta interesante detenerse a pensar en cómo la metodología en la cual se informan las recomendaciones permite una mejor experiencia y confiabilidad en aquello que se nos está recomendando. Por ejemplo, es muy transparente por parte de Netflix generar recomendaciones en una sección que señala “porque viste...” y genera una lista de recomendaciones. Esto genera inmediatamente una idea del por que el sistema me está recomendando aquello y permite imaginarse previamente que los elementos tienen una similitud con aquello que he visto.

Mediante el estudio del estado del arte en materias de visualización de la información a la hora de recomendar, el documento carece de un análisis profundo bajo pruebas realizadas por los autores, que permitan evidenciar de mejor manera aquello que se busca respaldar y con qué fundamentos se hace. Si bien abarca muchísimos más casos ya que se analiza el estado del arte, involucrar un análisis exhaustivo propiamente por los autores permite al lector contar con más respaldo en las conclusiones que el documento entrega y entender completamente el origen de las conclusiones. Pese a aquello, es un documento muy completo, sumamente fundamentado bajo los argumentos del análisis del estado del arte que sumando una fundamentación propia más detallada, sería un análisis totalmente completo.

En una clase del curso de marketing con el profesor Sergio Maturana de la Pontificia Universidad Católica de Chile, se hizo hincapié en que las emociones de manera gráfica tienen mucho más influencia en el comportamiento humano que el texto plano. Esto es sumamente real principalmente por el lado empático de los seres humanos, donde refleja sus emociones en un emoticon un rostro. En base a aquello, el punto de utilizar emoticones como interacción o calificación resulta sumamente práctico y útil. Un número no necesariamente refleja los sentimientos que nos ha generado un elemento o película. En base a aquello, las representaciones gráficas abarcan un espectro mucho mayor de la opinión de un usuario respecto a un elemento. Por lo tanto, resulta un tema muy importante tocado en el documento el cual en mi opinión, muchos sistemas recomendadores deberían incorporar para lograr capturar de manera más real las interacciones o calificaciones de un usuario.

------------
 
# Conclusiones
 
Es complejo para un sistema recomendador lograr capturar información completa, fidedigna y representativa si el diseño en el cual el usuario se relaciona con el no es del todo amigable. El documento propone múltiples formas de visualización con el objetivo de mejorar la experiencia del usuario y transparentar las razones de las recomendaciones, permitiendo al usuario comprender sus orígenes y no quedar con la sensación de que todo es una “caja negra”. Por lo tanto, es crucial en un sistema recomendador incorporar metodologías visuales y estéticas con el objetivo de que la experiencia del usuario resulte lo más amigable posible, generando interacciones más honestas y representativas.
 
Finalmente, el documento menciona técnicas de agrupaciones por grupos similares y calificaciones mediante emoticono las cuales resultan muy de consideración a la hora de recomendar. En base a aquello, se puede concluir que transparentar los orígenes de las recomendaciones y permitir al usuario calificar elementos no únicamente cerrados en una escala numérica, otorga facultades para expresar de diferentes formas su satisfacción o malestar, para que finalmente las recomendaciones sean más adecuadas y lograr verlas mediante grupos similares, que permitan al usuario entender su origen y razones del por que esta recomendación se esta realizando.


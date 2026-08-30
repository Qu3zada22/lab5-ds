# Laboratorio 5. Clasificación de tweets usando minería de texto.
**Universidad del Valle de Guatemala**
**Facultad de Ingeniería**
**Departamento de Ciencias de la Computación**
**CC3084 - Data Science**
**Semestre II-2026**

## Instrucciones
Utilice el dataset *Natural Language Processing with Disaster Tweets* de Kaggle. Debe hacer un análisis exploratorio para entender mejor los datos, sabiendo que el objetivo final clasificar si un tweet se refiere a un desastre real o no. Genere un informe con las explicaciones de los pasos que llevó a cabo y los resultados obtenidos. Recuerde que la investigación debe ser reproducible por lo que debe guardar el código que ha utilizado para resolver los ejercicios y/o cada uno de los pasos llevados a cabo si utiliza una herramienta visual. Incluya una nube de palabras que le ayude a detectar las que más se repiten.

## Descripción del Dataset
El conjunto de datos está formado por más de 10 500 filas y 5 columnas:
* **id:** El identificador del tweet
* **keyword:** una palabra clave del tweet, puede estar en blanco
* **location:** la ubicación desde donde fue enviado el tweet
* **text:** El texto del tweet
* **target:** La etiqueta de clasificación que especifica si el tweet se trata de un desastre real (1) o no (0).

## Ejercicios
1. Descargue el archivo train.csv
2. Cargue los archivos de datos a R o a Python, dependiendo de con qué trabaje.
3. Limpie y preprocese los datos. Describa de forma detallada las actividades de preprocesamiento que llevó a cabo.
   3.1. Se pueden hacer tareas como:
   * Convertir el texto a mayúsculas o a minúsculas
   * Quitar los caracteres especiales que aparecen como "#","@" o los apóstrofes.
   * Quitar las url
   * Revisar si hay emoticones y quitarlos
   * Quitar los signos de puntuación
   * Quitar los artículos, preposiciones y conjunciones (stopwords)
   * Quitar números si considera que interferirán en la clasificación (quizá debería valorar si quitar o no el 911).
4. Obtenga la frecuencia de las palabras tanto de los tweets de desastres como de los que no. ¿Qué palabras cree que le servirán para hacer un mejor modelo de clasificación? ¿vale la pena explorar bigramas o trigramas para analizar contexto?
5. Haga un análisis exploratorio de los datos para entenderlos mejor, documente todos los análisis
   5.1. Puede:
   * Investigar qué palabra se repite más en cada una de las categorías
   * Hacer una nube de palabras para visualizar las que aparecen con más frecuencia
   * Hacer un histograma con las palabras que más se repiten
   * Discutir sobre las palabras que tienen presencia en todas las categorías.
6. Elabore varios modelos de clasificación para determinar si un tweet se refiere a un desastre real o no. ¿Cómo planea abordar el contexto? Explique. Puede utilizar varios algoritmos para probar modelos.
7. Elabore una función en la que el usuario ingrese un tweet y el sistema lo clasifique en desastre o no.
8. Determinar las palabras positivas, negativas o neutras. Teniendo en cuenta la cantidad de palabras positivas y negativas del tweet determine qué tan positivo, negativo o neutral es el mismo. Revise para esto el preprocesamiento que le hizo a los tweets, ¿valdrá la pena dejar los emoticones y analizarlos?
9. Luego de analizar los datos determine:
   9.1. ¿Cuáles son los 10 tweets más negativos? ¿En qué categoría están?
   9.2. ¿Cuáles son los 10 tweets más positivos? ¿En qué categoría están?
   9.3. ¿Son los tweets de la categoría que indica que habla de un desastre real más negativos que los de la otra categoría?
10. Cree una variable que contenga la "negatividad" de cada tweet. Inclúyala en el conjunto de datos y entrene nuevamente el modelo de clasificación. Responda la siguiente pregunta y discuta los resultados. ¿La inclusión de esta variable mejoró los resultados del modelo de clasificación? Si es así, ¿en qué medida?
11. Elabore un informe donde se relaten sus hallazgos. Todo lo que descubrieron debe estar explicado apoyándose en gráficas y tablas que deben estar referenciadas en el texto. Si necesitan apoyo de herramientas externas como corpus para análisis de sentimientos o módulos especiales debe referenciarlo en el texto.

## Evaluación
**NOTA:** La evaluación de cada integrante del grupo será de acuerdo con sus contribuciones al trabajo grupal

* **(15 puntos) Análisis exploratorio:** Se elaboró un análisis exploratorio en el que se explican los cruces de variables, hay gráficos explicativos y análisis que permiten comprender el conjunto de datos.
* **(10 puntos) Limpieza y preprocesamiento de los datos:** Se documentan las tareas de limpieza, incluyendo los paquetes/módulos que se usaron.
* **(10 puntos) Generación de los ngramas y cálculo de sus frecuencias y probabilidades:** Se explica cómo se generaron los n-gramas y se calcularon los valores de frecuencia y probabilidades o cualquier otro análisis que permita clasificar los tweets.
* **(15 puntos) Modelo clasificadores:** Se describe el algoritmo que se usó para clasificar, así como los parámetros del modelo. El modelo está correctamente entrenado con el conjunto de datos de entrenamiento y se dejó un porcentaje para probar. Se evalúan los modelos con métricas adecuadas y se selecciona el mejor modelo para el problema.
* **(20 puntos) Función de clasificación:** Se elaboró una función que permite clasificar nuevos tweets, esta recibe el texto de un tweet sin preprocesar y devuelve si se refiere a un desastre natural o no.
* **(10 puntos) Clasificación de tweets en positivo, negativo o neutro:** Se describe el algoritmo que se usó para clasificar el review en positivo, negativo o neutro.
* **(5 puntos) Variable de "negatividad del tweet":** Se creó una variable que representa que tan positivo o negativo es cada tweet.
* **(15 puntos) Resultados:** Se responden todas las interrogantes planteadas en el punto 6 de las instrucciones. Se entrena nuevamente el modelo de clasificación del laboratorio anterior usando la nueva variable. Se prueba y se discuten los resultados obtenidos.

## Material a Entregar
* Link del documento del informe donde trabajó el grupo.
* Script de R (.r o .rmd) o de Python que utilizó para hacer su análisis exploratorio y predicciones.
* Link del repositorio usado para versionar el código.
* Informe en formato .pdf con las explicaciones.

## Fechas de Entrega
1. **Avances:** Descripción de los datos, preprocesamiento y sus explicaciones, unigramas, bigramas, descripción del modelo preliminar de clasificación: 27 de agosto de 2026, 17:20
2. **Informe completo:** con selección del mejor modelo, función de clasificación y explicación de todos los análisis: 30 de agosto de 2026 23:59

**NOTA:** Para poder tener nota completa debe entregar las asignaciones en el tiempo adecuado. No se calificará el avance del laboratorio si no fue entregado en tiempo, aunque esté en el repositorio.

## Referencias
* Daniel Jurafsky, J. H. M. (101AD). Speech and Language Processing (2008), 1. Retrieved from https://web.stanford.edu/~jurafsky/slp3/
* Feinerer, I., Hornik, K., & Meyer, D. (2008). Text Mining Infrastructure in R. Journal Of Statistical Software, 25(5), 1-54. https://www.jstatsoft.org/article/view/v025i05
* Jurafsky, D., & Martin, J. H. (2014). N-Grams. Speech and Language Processing, 2-7. Retrieved from https://lagunita.stanford.edu/c4x/Engineering/CS-224N/asset/slp4.pdf

## Paquetes Útiles de R
* Quanteda
* Wordcloud
* Tm
* Rweka
* Ngram

## Módulos Útiles de Python
* Natural Language Toolkit (NLKT)
* Wordcloud
* TextBlob
* Spacy

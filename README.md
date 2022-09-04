# Detección de tumores cerebrales

## Contenido
  - [Contenido](#contenido)
  - [Justificación](#justificación)
  - [Recoleción de data](#recoleción-de-data)
  - [Resultados](#resultados)
  - [Conclusiones](#conclusiones)

	
## Justificación
<p align="justify">	
La tomografía computarizada craneal es uno de los principales exámenes más esenciales para el diagnóstico de tumores cerebrales. La tomografía computarizada de la cabeza utiliza un equipo especial de rayos X para ayudar a evaluar lesiones de la cabeza, dolores de la cabeza severos, mareos, síntomas de aneurisma, derrame cerebral y tumores cerebrales. También ayuda al médico a evaluar la radioterapia para el cáncer de cerebro. En casos de emergencia, pude identificar lesiones y hemorragias internas lo suficientemente rápido para ayudar a salvar vidas.
</p>
<p align="justify">
El uso de la inteligencia artificial para la detección de tumores cerebrales va a permitir que el proceso de identificación e interpretación de patrones que caracterizan a los tumores cerebrales sean más rápidos. Por lo cual se puede obtener resultados más rápidos y precisos. Esto va a disminuir los casos de falsos negativos y acelerar la atención de personas con este padecimiento, de esta manera se podrá dar atención a las personas con tumores cerebrales más avanzados y tratamiento inmediato para los pacientes con inicio de un tumor cerebral.
</p>

## Recoleción de data
<p align="justify">	
Para la recolección de data se uso el repositorio Kaggle. Kaggle es una plataforma de google en la que se realizan competiciones de machine learning abiertas para todo el mundo. En Kaggle se obtuvo la data a analizar para este trabajo, ya que en Kaggle se encuentra un repositorio bastante amplio que es ofrecida por la misma comunidad.
</p>

## Resultados
<p align="justify">
Para la obtencion de los resultados se realizo un preprocesamiento de los datos estructurados (caracteristicas cuantitativas de las imagenes). Se aplicaron diversos analisis estadisticos como la correlacion de los atributos, transfomracion, escalamiento, reduccion de dimensiones (PCA), etc. En el caso de los datos no estructurados (las imagenes de tumores), se realizo un procesamiento de imagenes previo al entrenamiento de las redes neuronales.
</p>

### Machine Learning
<p align="justify">
Se aplicaron diversos algoritmos de Machine Learning, siendo el mas efectivo el algoritmo Super Vector Machine (SVM) con un accuracy de 99.28 %.
</p>

|Algoritmo       |Accuracy| Std  |
|:--------------:|:------:|:----:|
|**SVM**         | 99.28% | 0.39 |
|**ExtraTrees**  | 98.94% | 0.59 |
|**RandomForest**| 98.72% | 0.60 |
|**k-NN**        | 98.75% | 0.48 |

### Deep Learning
<p align="justify">
Se implemento un algoritmo con Redes Neuronales Artificiales (ANN) y un algoritmo con Redes Neuronales Convolucionales (CNN) usando una red neuronal llamada MobileNet. En ambos casos se obtuvieron buenos resultados.
</p>

|Algoritmo                                 |Accuracy|
|:----------------------------------------:|:------:|
|**Redes Neuronales Arficiales (ANN)**     | 93% |
|**Redes Neuronales Convolucionales (CNN)**| 92% |

## Conclusiones

En este proyecto se presentaron 3 principales formas de resolver el mismo problema estas son:
- Machine Learning, mediante la obtención de los atributos de Haralick de la imagen se entrenó los datos con el algoritmo SVM (Support Vector Machine). Este algoritmo obtuvo mejor resultado con un accuracy de 0.99 en los datos de evaluación.
- Redes Neuronales Artificiales (ANN), se escogió como atributos los pixeles de la imagen (172800 atributos) para entrenar la ANN y luego se optimizo algunos híper parámetros obteniendo un accuracy de 0.93 en los datos de evaluación.
- Redes Neuronales Convolucionales (CNN), este algoritmo es ideal cuando se quiere trabajar con imágenes por lo cual se decidió escoger esta opción. Se implementó una rede neuronal llamada MobileNet con la cual se obtuvo un accuracy de 0.92 en los datos de evaluación.
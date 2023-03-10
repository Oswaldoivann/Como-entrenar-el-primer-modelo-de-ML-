# 🥷 ¿Como entrenar el primer modelo de ML?

### Aprende los conceptos basicos de Machine Learning utilizando algoritmos para Ciencia de Datos


<p align="center">
  <img src="https://media.giphy.com/media/v1.Y2lkPTc5MGI3NjExNGQ5ZTI3ZWYzMzkwYjJhOWQxNTM4NGMyNDM2OWVmNzc4YTUxNWM4ZCZjdD1n/aX6BQtPpC5XTMnjb2C/giphy.gif" alt="Texto alternativo">
  </p>

# Temas

* Machine Learning
* Categoria de Algoritmos
* Tipos de Algoritmos de Supervisión
* ¿Clasificación y Regresión?
* Tipos de Problemas con ML Supervisado
* Algoritmos de Aprendizaje Supervisado
* Segemaker Lab
* Modelo de Regresión Lineal
  - Dividiendo el DataSet
  - Entrenando del modelo
  - Evaluando el Modelo



# 🧠 Machine Learning

El Machine Learning es una rama de la *Inteligencia Artificial* (IA), que es la capacidad de una maquina para realizar tareas o procesos, que requieren de una “inteligencia” similar a la de un ser humano.

Por su parte el proceso de **Machine Learning** se refiere a los sistemas que pueden aprender de los datos, identificar patrones y tomar decisiones con minima intervencion humana.

# :spiral_notepad: Categoria de Algoritmos

### Supervisados:

Son aquellos donde se tiene una etiqueta o variable respuesta. El objetivo de los modelos supervisados es predecir el valor de una variable respuesta en función de una o varias variables de entrada o predictores. Se fundamenta con información histórica para predecir en el futuro un resultado.

### No supervisados: 

Son aquellos donde no se tiene una variable respuesta. Y se busca descubrir y encontrar patrones a travez de los datos, El objetivo del clustering es identificar grupos o clusters de observaciones, creando las etiquetas clusterisando los datos.

### Aprendizaje por refuerzo: 

Funciona con un mecanismo de recompensa. Un agente (máquina) que interactúa en el entorno y prueba métodos. El agente es recompensado o castigado aprendiendo a prueba y error. Este aprendizaje es usafo en robótica para entrenar robots en el control de movimiento, navegación autónoma, manipulación de objetos, entre otros.


# 👨🏻‍💻 Tipos de Algoritmos de Supervisión

Los algoritmos supervisados se llaman así porque requieren que el conjunto de datos de entrenamiento contenga las respuestas correctas también conocidas como etiquetas o valores objetivo para cada observación de nuestos dataset. 

### Regresión

En la regresión, se trata de predecir un valor numérico para un conjunto de datos. Por ejemplo predecir el precio de una casa en función de sus características o features. La variable target en un problema de regresión de tipo cuantitativa. Predicen valores numéricos. 

### Clasificación

En la clasificación, buscamos predecir una la variable target (etiqueta) o respuesta de tipo categórica. Con la clasificación buscamos predecir una etiqueta o clase para un conjunto de datos, como identificar el tipo de flor a partir de sus características. 

### Redes Neuronales

Estos algoritmos de aprendizaje profundo utiliza una estructura de red de neuronas artificiales para aprender a partir de datos. Estos modelos se utilizan para una amplia variedad de problemas de clasificación y regresión.

# 🤔 ¿Clasificación o Regresión?

La elección entre clasificación o regresión depende de la naturaleza del problema que se esté tratando de resolver y del tipo de datos que se estén utilizando.

Una **Regresión** puede tener como entrada valores continuos o discretos. Un problema con múltiples variables de entrada a menudo se denomina problema de regresión multivariante.

Una **Clasificiación** requiere una variable objetivo con dos o más clases, un problema con dos clases se denomina problema de clasificación binaria y con más de dos clasificación multiclase.


# 🎲 Tipos de Problemas con ML Supervisado

Binaria: Se espera una respuesta Verdadera y Falsa, un valor 0, 1 tambien llamada binaria.

Regresión: El resultado es un valor decimal, el resultado es una variable del calculo de una ecuación.

Multiclase: Se espera obtener una repsuesta No binaria, mas de un resultado A, B, C, ..., N. 

Reconocimiento: Identificar patrones en los datos. Como reconocer los patrones en imágenes médicas para detectar enfermedades.

# 🪲 Algoritmos de Aprendizaje Supervisado

Existen muchos algoritmos de aprendizaje supervisado, cada uno con sus propias características y aplicaciones. La elección del algoritmo dependerá del problema específico que se esté abordando y de las características del conjunto de datos.

   * Regresión lineal
   * Regresión logística
   * Árboles de decisión
   * Máquinas de vectores de soporte (SVM)
   * Naïve Bayes
   * K vecinos más cercanos (KNN) 
   * Redes neuronales
   * Gradient Boosting Machines (GBM)
   * Random Forest
   * Redes neuronales convolucionales (CNN)
   * Redes neuronales recurrentes (RNN)
   * Modelos lineales generalizados (GLM)
   * Máquinas de vectores de soporte con núcleo gaussiano (SVM-Gaussian Kernel)

# :notebook: SegeMaker Studio Lab 

### Python I

| No | Title | Open in Studio Lab |
|----|-------|--------------------|
|   1|Python I | <a><img src="https://studiolab.sagemaker.aws/studiolab.svg" alt="Open In SageMaker Studio Lab"/></a> |
|   2|Regresion Lineal | <a><img src="https://studiolab.sagemaker.aws/studiolab.svg" alt="Open In SageMaker Studio Lab"/></a> |

# 💹 Regresión Lineal

La Regresión Lineal es un método matematico para establecer una relación entre una variable respuesta y una o más variables predictoras. Si existe una relación lineal entre las variables, se puede construir una línea recta que se ajuste a los datos para predecir valores futuros.

- X = Respuesta ó Dependiente, X es el conjunto de características (features).
- y = Predictoras ó Independientes, y es el conjunto de etiquetas (labels).


## Dividiendo el DataSet

Para entrenar el modelo primero dividimos los datos en conjuntos de entrenamiento y prueba, asi evaluaremos la capacidad de aprendizaje del modelo.

La función ```train_test_split()``` divide aleatoriamente los datos en conjuntos de entrenamiento y prueba, el parámetro ```test_size``` especifica el tamaño del conjunto de prueba. Si ha establecido 0.2, significa que el 20% de los datos se reservan para el conjunto de prueba y el 80% para el conjunto de entrenamiento.

El parámetro ```random_state``` se utiliza para inicializar el generador de números aleatorios, y asegura que se dividan los datos de la misma manera en cada ejecución del código. Estos numeros pueden ser 

## Entrenando del modelo

Para el entrenamiento usamos la clase ```LinearRegression()``` que ajusta el modelo utilizando los datos de ```X_train,  y_train```. Para entrenar el modelo usamos la función ```.fit()``` en nuestra clase. 

Guardamos la clase en una varaible  ```reg = LinearRegression()``` y entrenamos el modelo ```reg.fit(X_train, y_train)```. Esta línea entrenara el modelo de utilizando los datos de entrenamiento para que pueda predecir la variable de salida. 

## Evaluando el Modelo

Las métricas de evaluación son utilizadas para evaluar el rendimiento de un modelo de machine learning. Estas métricas pueden determinar si el modelo es efectivo para resolver el problema que se está abordando, son utilizadas para ajustar los parámetros del modelo y obtener mejores resultados.

- Coeficiente de determinación (R²): El valor de R² varía entre 0 y 1, donde 0 indica que el modelo no explica ninguna variabilidad y 1 indica que el modelo explica toda la variabilidad. Cuanto mayor sea el valor, mejor será el modelo.

- Validación cruzada (cross-validation): Es una técnica utilizada para evaluar el rendimiento del modelo. El proceso de validación cruzada implica dividir el conjunto de datos en varios subconjuntos, entrenar y evaluar el modelo en diferentes combinaciones de estos subconjuntos.

Existen diferentes metricas de validación, por lo que seleccionar la adecuada dependera del problema que se desea predecir, el cientifico de datos identificara las mas valiosas para cada problema.

# 🔄️ Conclusión


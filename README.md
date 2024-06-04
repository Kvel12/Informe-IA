# Informe sobre Machine learning : Emisiones de CO2 

## Grupo de trabajo

1. Ervin CaravalI Ibarra
2. Hernan David Cisneros Vargas
3. Miguel Angel Moreno Romero
4. Kevin Alejandro Velez Agudelo

## Resumen del Proyecto

Este Informe está enfocado en la predicción de emisiones de **CO2** de vehículos, utilizando técnicas de machine learning. El aumento de las emisiones de **CO2** es uno de los principales contribuyentes al cambio climático, y encontrar formas de reducir estas emisiones es crucial. Con este contexto, se ha planteado la construcción y evaluación de modelos predictivos que permitan estimar las emisiones de **CO2** a partir de variables específicas del vehículo, como el tamaño del motor, el número de cilindros y el consumo de combustible en ciudad y en carretera. 

Para ello, se han utilizado dos enfoques para determinar cuál de estos modelos ofrece una mejor precisión en la predicción de las emisiones de **CO2** : 

### 1. Redes Neuronales

Se utilizó una red neuronal para modelar la relación entre las características del vehículo y sus emisiones de **CO2**. Las redes neuronales son conocidas por su capacidad para capturar patrones complejos en los datos. De esta manera se probaron diversas configuraciones de hiperparámetros para optimizar el rendimiento del modelo y se evaluó su precisión y matrices de confusión.

### 2. Árboles de Decisión
Los árboles de decisión se utilizaron como un enfoque más interpretable para modelar las emisiones de **CO2**. Este método permite entender fácilmente cómo las diferentes características del vehículo afectan las emisiones. Se evaluaron múltiples configuraciones de hiperparámetros y se analizaron los resultados para determinar el impacto de cada uno en la precisión del modelo.

Ambos enfoques fueron implementados en dos notebooks separados, incluidos en este repositorio, y se llevó a cabo un análisis de los hiperparámetros para cada modelo con el fin de optimizar su desempeño. Esto permitirá identificar los factores que más influyen en las emisiones y potencialmente ayudar en la toma de decisiones para reducir la huella de carbono de los vehículos.

## Solución Presentada

### Notebook 1: Redes Neuronales

1. **Carga de Datos**: Se lee el archivo `CO2 emissions.csv` que contiene los datos relevantes.
2. **División de Datos**: Los datos se dividen aleatoriamente en un 80% para entrenamiento y un 20% para pruebas.
3. **Normalización**: Se estandarizan las variables independientes.
4. **Entrenamiento y Evaluación**: Se construyen cinco redes neuronales variando los hiperparámetros (activación, solver, tamaño de capas ocultas). Se evalúa la precisión y se presentan las matrices de confusión.
5. **Optimización de Hiperparámetros**: Se seleccionan los mejores hiperparámetros y se prueba el efecto del hiperparámetro `alpha`.

### Notebook 2: Árboles de Decisión

1. **Carga de Datos**: Se lee el archivo `CO2 emissions.csv`.
2. **División de Datos**: Los datos se dividen aleatoriamente en un 80% para entrenamiento y un 20% para pruebas.
3. **Normalización**: Se estandarizan las variables independientes.
4. **Entrenamiento y Evaluación**: Se configuran y evalúan árboles de decisión variando la profundidad máxima (`max_depth`) con diferentes criterios (`gini`, `entropy`) y splitters (`best`, `random`).
5. **Optimización de Hiperparámetros**: Se selecciona el hiperparámetro `min_samples_split` y se prueban diferentes valores para evaluar su impacto en la precisión.

## Conclusiones

- **Redes Neuronales**: Su uso proporcionó una alta precisión en la predicción de emisiones de **CO2**., y la variación de hiperparámetros como la función de activación y el solver mostró diferencias significativas en el rendimiento.
- **Árboles de Decisión**: Este enfoque demostró ser eficaz y fácil de interpretar, y la profundidad del árbol tuvo un impacto considerable en la precisión del modelo.

En general, ambos enfoques proporcionaron resultados importantes, aún así la elección del modelo óptimo dependerá de la situación específica en que se esté aplicando el enfoque y de las necesidades del análisis a realizar. Ademas, la optimización de hiperparámetros es un aspecto de crucial importancia al momento de mejorar el rendimiento de los modelos de machine learning. cada hiperparámetro tiene un impacto específico en la precisión del modelo.

Con el desarrollo y analisis de resultados del presente informe, se demuestra la importancia de seleccionar y ajustar adecuadamente los modelos de machine learning para obtener predicciones precisas y confiables en problemas del diverso indole.

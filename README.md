# Prueba 1 IA

## Trabajo de Métodos de Inteligencia Artificial

### Predicción de supervivencia en el Titanic usando modelos supervisados de Machine Learning

---

## Información del curso

**Ramo:** Métodos de Inteligencia Artificial
**Profesor:** Franco Mansilla

**Integrantes:**

* Gerson Alarcón
* Sandy Godoy
* Patricio Alarcón

---

## Descripción del trabajo

Este trabajo tiene como objetivo aplicar modelos supervisados de Machine Learning para resolver un problema de clasificación binaria utilizando el dataset Titanic.

La variable objetivo del estudio es `Survived`, la cual indica si un pasajero sobrevivió o no al naufragio:

* `0`: No sobrevivió
* `1`: Sobrevivió

A partir de esta variable, se entrenaron distintos modelos predictivos y se comparó su desempeño utilizando métricas de clasificación.

---

## Dataset utilizado

Se utilizó el dataset Titanic entregado por el profesor en el repositorio de la asignatura.

El conjunto de datos contiene información de pasajeros, incluyendo variables como:

* Clase del pasajero
* Sexo
* Edad
* Cantidad de familiares a bordo
* Tarifa pagada
* Puerto de embarque
* Variable de supervivencia

---

## Modelos entrenados

Durante el desarrollo del trabajo se entrenaron los siguientes modelos:

1. Regresión logística con penalización:

   * Ridge
   * Lasso
   * ElasticNet

2. Random Forest

3. XGBoost

4. Red neuronal simple

---

## Métricas de evaluación

Como el problema corresponde a clasificación binaria, se utilizaron las siguientes métricas de desempeño:

* Accuracy
* Precision
* Recall
* F1-Score
* AUC
* KS

Las métricas fueron calculadas tanto en la muestra de entrenamiento como en la muestra de validación, con el objetivo de comparar el rendimiento de los modelos y detectar posibles señales de sobreajuste.

---

## Optimización de hiperparámetros

Para optimizar el modelo XGBoost se utilizó el método `RandomizedSearchCV`.

Este método prueba distintas combinaciones de hiperparámetros de forma aleatoria y evalúa cada combinación mediante validación cruzada. La métrica utilizada para seleccionar la mejor combinación fue AUC.

La optimización permitió comparar el modelo XGBoost original con una versión ajustada, evaluando si existía mejora en su capacidad predictiva.

---

## Modelo final seleccionado

El modelo final seleccionado fue **XGBoost Optimizado**.

Este modelo obtuvo el mejor AUC de validación, con un valor de **0.6982**. Además, presentó un desempeño más equilibrado entre entrenamiento y validación en comparación con otros modelos.

Se seleccionó AUC como métrica principal porque permite medir la capacidad del modelo para diferenciar entre pasajeros que sobrevivieron y pasajeros que no sobrevivieron.

---

## Principales resultados

El modelo XGBoost Optimizado obtuvo las siguientes métricas en validación:

* Accuracy: 0.6369
* Precision: 0.6081
* Recall: 0.5556
* F1-Score: 0.5806
* AUC: 0.6982
* KS: 0.3187

---

## Conclusión

El desarrollo del trabajo permitió aplicar y comparar distintos modelos supervisados de Machine Learning en un problema de clasificación binaria.

Los modelos Ridge, Lasso y ElasticNet presentaron resultados estables. Random Forest mostró señales de sobreajuste, ya que obtuvo resultados perfectos en entrenamiento pero bajó en validación. La red neuronal simple tuvo un desempeño competitivo, especialmente en Accuracy y F1-Score.

Finalmente, se seleccionó XGBoost Optimizado como modelo final, ya que obtuvo el mejor AUC de validación y mostró un equilibrio adecuado entre capacidad predictiva y generalización.

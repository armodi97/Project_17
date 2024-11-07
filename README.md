
# Proyecto de Evaluación de Modelos para Predicción de Actividad de Clientes

Este proyecto desarrolla un modelo de machine learning para predecir la actividad de clientes en función de sus datos de contrato, uso de internet, características personales y datos de telefonía. Se utilizan diversos modelos de clasificación para identificar patrones y predecir si un cliente está activo o inactivo.

## Descripción del Proyecto

El proyecto busca predecir la actividad de clientes con base en múltiples fuentes de datos, utilizando un conjunto de modelos de clasificación para seleccionar el que ofrezca la mayor precisión. Los modelos se evalúan mediante métricas como el **F1 Score** y el **AUC-ROC** para asegurar su rendimiento.

## Estructura del Análisis

1. **Preparación de los Datos**
   - Se cargan los datos desde archivos que contienen información de contrato, internet, características personales y datos de telefonía.
   - Los datos se combinan en un solo DataFrame y se preprocesan para preparar las características y la variable objetivo.

2. **Preprocesamiento e Ingeniería de Características**
   - Se crean variables temporales a partir de las fechas, y se maneja la imputación de valores ausentes.
   - Se convierte la fecha de finalización en una variable binaria (`isActive`) para definir si el cliente está activo o inactivo.

3. **Entrenamiento de Modelos de Clasificación**
   - Se entrenan múltiples modelos, incluyendo `LogisticRegression`, `RandomForestClassifier`, `KNeighborsClassifier`, `LightGBM`, `CatBoostClassifier`, y redes neuronales con `TensorFlow`.
   - Se utiliza `GridSearchCV` para optimizar los hiperparámetros de cada modelo.

4. **Evaluación de Modelos**
   - Los modelos se evalúan utilizando métricas de clasificación, tales como el **F1 Score** y **AUC-ROC**, y se genera un reporte de clasificación.
   - Se selecciona el modelo óptimo basado en estas métricas para la implementación.

5. **Conclusiones**
   - Se elige el mejor modelo para predecir la actividad del cliente y se brindan recomendaciones para su implementación en el sistema.

## Requisitos

- **Python 3.7+**
- Librerías: `pandas`, `numpy`, `plotly_express`, `scikit-learn`, `lightgbm`, `catboost`, `tensorflow`

## Cómo Ejecutar el Proyecto

1. Clona el repositorio.
2. Instala las dependencias:
   ```bash
   pip install -r requirements.txt
   ```
3. Ejecuta el notebook `evaluacion_del_modelo.ipynb` para reproducir el análisis y entrenar los modelos.

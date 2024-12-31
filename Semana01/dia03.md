# Día 3: Ciclo de desarrollo de modelos ML

## Conceptos clave

### Componentes clave de un pipeline ML
El desarrollo de modelos de Machine Learning (ML) se divide en varias etapas:

1. **Colección de datos**:  
   Reunir datos relevantes para entrenar el modelo.

2. **Análisis exploratorio de datos (EDA)**:  
   Comprender la estructura de los datos, identificar patrones y posibles problemas (valores faltantes, ruido, etc.).

3. **Preprocesamiento de datos**:  
   Limpieza y transformación de los datos para hacerlos adecuados para el modelo (normalización, codificación, etc.).

4. **Feature Engineering**:  
   Selección, creación y transformación de variables que mejoren el rendimiento del modelo.

5. **Entrenamiento**:  
   Ajustar el modelo utilizando los datos de entrenamiento para minimizar errores.

6. **Evaluación**:  
   Medir el rendimiento del modelo con métricas como precisión, recall, F1-score, etc.

7. **Despliegue**:  
   Implementar el modelo en un entorno de producción para su uso en tiempo real o en lotes.

8. **Monitoreo**:  
   Supervisar el rendimiento del modelo para identificar desviaciones o degradación.

---

## Ejemplos de uso en servicios AWS por etapa del pipeline

### Colección de datos
- **Amazon S3**:  
  Almacena grandes volúmenes de datos estructurados o no estructurados (imágenes, registros, etc.).  
  **Ejemplo**: Almacenar datos históricos de ventas o logs de servidores.

### Análisis y preprocesamiento de datos
- **Amazon SageMaker Data Wrangler**:  
  Simplifica la exploración, limpieza y transformación de datos.  
  **Ejemplo**: Identificar valores atípicos en un conjunto de datos de sensores IoT.

### Gestión de características
- **Amazon SageMaker Feature Store**:  
  Centraliza las características para su reutilización.  
  **Ejemplo**: Crear una característica llamada "frecuencia de compra" para usarla en varios modelos de predicción de ventas.

### Entrenamiento y evaluación
- **Amazon SageMaker**:  
  Entrena modelos usando instancias personalizadas y evalúa su rendimiento.  
  **Ejemplo**: Entrenar un modelo de clasificación para predecir si un cliente abandonará un servicio (churn).

### Despliegue
- **Amazon SageMaker Endpoint**:  
  Permite implementar un modelo en un entorno de producción como API.  
  **Ejemplo**: Desplegar un modelo de recomendaciones en una tienda en línea.

### Monitoreo
- **Amazon SageMaker Model Monitor**:  
  Supervisa desviaciones en los datos de entrada o salida del modelo.  
  **Ejemplo**: Detectar si los datos de clientes recientes tienen características diferentes a los datos con los que se entrenó el modelo (drift).

---

## Fundamentos de MLOps
Aplicar principios de ingeniería de software y DevOps al desarrollo de ML para crear pipelines reproducibles, escalables y fáciles de gestionar.

- **Tareas comunes**:  
  - Versionado de datos y modelos  
  - Automatización del entrenamiento y despliegue  
  - Monitoreo continuo  

---

## Evaluación de Modelos ML
La evaluación de modelos de Machine Learning es crucial para medir qué tan bien un modelo realiza su tarea. Existen varias métricas, y la elección depende del tipo de problema (clasificación, regresión, etc.) y el contexto de negocio.

### 1. Clasificación (binaria o multiclase)
Se utiliza cuando el objetivo es predecir categorías.  
**Ejemplo**: ¿Es un correo spam o no?

- **Precisión (Accuracy)**:  
  Proporción de predicciones correctas sobre el total.  
  **Uso**: Funciona bien cuando las clases están balanceadas.  
  **Ejemplo**: Un modelo que clasifica imágenes como "gato" o "perro".

- **Precisión Positiva (Precision)**:  
  Proporción de verdaderos positivos entre todos los positivos predichos.  
  **Uso**: Es útil cuando es importante minimizar falsos positivos.  
  **Ejemplo**: Detectar fraudes, donde cada falso positivo genera costos innecesarios.

- **Sensibilidad o Recall**:  
  Proporción de verdaderos positivos entre todos los positivos reales.  
  **Uso**: Se prefiere cuando es más importante minimizar falsos negativos.  
  **Ejemplo**: Diagnóstico de enfermedades, donde es crucial identificar todos los casos positivos.

- **F1-Score**:  
  Media armónica de Precision y Recall.  
  **Uso**: Ideal para conjuntos de datos desbalanceados donde ambos (Precision y Recall) son importantes.  
  **Ejemplo**: Detección de fraudes o spam en correos electrónicos.

### 2. Regresión
Se utiliza cuando el objetivo es predecir valores continuos.  
**Ejemplo**: ¿Cuál será el precio de una casa?

- **Error Absoluto Medio (MAE)**:  
  Promedio de las diferencias absolutas entre las predicciones y los valores reales.  
  **Uso**: Es sencillo de interpretar y muestra el error promedio.  
  **Ejemplo**: Predecir la demanda diaria de energía.

- **Error Cuadrático Medio (MSE)**:  
  Promedio de los cuadrados de las diferencias entre predicciones y valores reales.  
  Penaliza más los errores grandes.  
  **Ejemplo**: Predicción de precios en el mercado de valores.

- **R² (Coeficiente de determinación)**:  
  Mide qué tan bien las predicciones se ajustan a los datos reales (1 es ajuste perfecto).  
  **Uso**: Indica la calidad del modelo en su conjunto.  
  **Ejemplo**: Modelos de predicción de ingresos por ventas.

### 3. Ejemplo de métricas en casos reales
- **Detección de fraude**:  
  Se enfocaría en Precision y Recall para minimizar falsos positivos y negativos.

- **Recomendaciones personalizadas**:  
  Usaría Precisión (Accuracy) para medir qué tan relevantes son las recomendaciones.

- **Análisis de riesgo crediticio**:  
  Podría emplear F1-Score para balancear entre Precision y Recall.

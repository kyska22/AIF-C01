# Día 09 - Evaluación de Modelos Fundacionales

## Evaluación de Modelos Fundacionales  
Los modelos fundacionales son grandes modelos preentrenados que pueden ser adaptados a una amplia variedad de tareas. Ejemplos conocidos incluyen GPT, BERT, y DALL-E. Evaluar estos modelos implica analizar su desempeño en tareas específicas y determinar si cumplen con las expectativas técnicas y los objetivos de negocio.  

## Métodos de Evaluación: Métricas  
### 1. ROUGE (Recall-Oriented Understudy for Gisting Evaluation)  
- Diseñada para medir la calidad de resúmenes textuales.  
- Compara la salida del modelo con un texto de referencia, evaluando coincidencias de **n-gramas, palabras o frases consecutivas**.  

**Ejemplo:**  
Si el resumen del modelo es:  
*"El gato duerme en la cama"*  
Y el resumen de referencia es:  
*"El gato está durmiendo en la cama"*  
Se mide el número de palabras coincidentes: "El", "gato", "en", "la", "cama".  

**Ejercicio práctico:**  
Genera un resumen para este texto:  
*"Las lluvias torrenciales en la región provocaron inundaciones en las zonas bajas."*  
Luego, evalúa cuántas palabras coinciden con el resumen:  
*"Inundaciones causadas por lluvias torrenciales en la región."*  

### 2. BLEU (Bilingual Evaluation Understudy)  
- Utilizado principalmente en traducción automática.  
- Compara la traducción del modelo con una traducción de referencia, midiendo la **exactitud de los n-gramas coincidentes**.  

**Ejemplo:**  
Traducción del modelo:  
*"The cat is on the bed."*  
Traducción de referencia:  
*"The cat lies on the bed."*  
BLEU evalúa coincidencias parciales entre palabras y frases.  

**Ejercicio práctico:**  
Traduce esta frase:  
*"La casa es grande."*  
Y evalúa tu traducción contra la referencia: *"The house is big."*  

### 3. BERTScore  
- Evalúa similitud semántica utilizando embeddings generados por BERT.  
- No solo mide coincidencias exactas, sino el significado de las palabras en contexto.  

**Ejemplo:**  
Dos frases:  
- "El perro corre rápido."  
- "El can se mueve velozmente."  
Aunque las palabras no coincidan exactamente, el significado es similar, y BERTScore reflejará esto.  

**Ejercicio práctico:**  
Piensa en una frase y reescríbela con un sinónimo en cada palabra. Evalúa si ambas son equivalentes en significado.  

## Cómo Determinar si un Modelo Cumple los Objetivos de Negocio  
1. **Definir Métricas de Desempeño Clave (KPIs):**  
   Relaciona métricas como precisión, tiempo de respuesta, o BLEU con necesidades concretas.  
   - **Ejemplo:** Un chatbot debe resolver el 80% de las consultas sin intervención humana.  

2. **Evaluar Impacto en el Negocio:**  
   Considera cómo el modelo afecta ingresos, costos, o satisfacción del cliente.  
   - **Ejemplo:** ¿Un modelo de recomendación aumenta el porcentaje de clics en productos?  

3. **Iteración con Feedback Real:**  
   Asegúrate de que el modelo sea probado en un entorno real con usuarios reales.  
   - **Ejemplo:** Si implementas un modelo de atención al cliente, mide la tasa de retención de usuarios después de implementar la solución.  

---

| **Criterio**            | **ROUGE**                                                                 | **BERTScore**                                                      |
|--------------------------|-----------------------------------------------------------------------------|----------------------------------------------------------------------|
| **Enfoque de evaluación** | Mide coincidencias literales (n-gramas, palabras o frases exactas).         | Evalúa similitud semántica utilizando embeddings de palabras.        |
| **Tipo de coincidencia** | Coincidencias basadas en texto exacto.                                      | Coincidencias basadas en significado contextual.                    |
| **Aplicación típica**    | Resúmenes textuales y tareas que requieren comparar textos similares.       | Comparaciones de frases que pueden variar en estructura pero no en significado. |
| **Sensibilidad a sinónimos** | No considera sinónimos o paráfrasis como coincidencias válidas.           | Reconoce sinónimos y paráfrasis debido a su análisis contextual.    |


### Ejemplo de Uso de BLEU en Otro Contexto: **Generación de Descripciones Automáticas de Imágenes**

#### Contexto  
Imagina que has desarrollado un modelo de inteligencia artificial que genera descripciones automáticas para imágenes. Tu tarea es evaluar si las descripciones generadas por el modelo son similares a las descripciones escritas por humanos.  

#### Ejemplo  
- **Descripción generada por el modelo:**  
  *"Un perro negro está jugando con una pelota en el césped."*  

- **Descripción de referencia (escrita por un humano):**  
  *"Un perro de color negro corre detrás de una pelota en un jardín."*  

#### Evaluación con BLEU  
El BLEU puede medir la similitud entre la descripción generada y la de referencia al comparar la presencia de **n-gramas** coincidentes (grupos de palabras consecutivas). En este caso:  
- Coincidencia de unigramas: "Un", "perro", "negro", "pelota".  
- Coincidencia de bigramas: "Un perro", "perro negro".  

Al calcular BLEU, obtendrás una puntuación que refleja qué tan similares son ambas descripciones, permitiendo evaluar objetivamente el desempeño del modelo.  

#### Ventaja de BLEU en Este Contexto  
El BLEU es útil porque permite comparar múltiples descripciones de referencia con la salida del modelo, evaluando no solo palabras individuales, sino también estructuras más complejas como frases completas.  

---

### Pasos para Asegurar que un Modelo Generativo Cumpla con los Objetivos de Negocio

1. **Definir los Objetivos de Negocio**  
   - Clarificar el propósito del modelo y los resultados esperados.  
   - Identificar métricas clave de desempeño (KPIs) relevantes para los objetivos.  
     - **Ejemplo:** Reducir el tiempo de atención al cliente en un 30% mediante un chatbot.

2. **Seleccionar las Métricas Técnicas Adecuadas**  
   - Elegir métricas que reflejen el desempeño del modelo en su tarea específica.  
     - **Ejemplos:** BLEU para generación de texto, precisión para clasificación, o tiempo de respuesta para aplicaciones en tiempo real.

3. **Evaluación Técnica y Validación**  
   - Realizar pruebas del modelo en datos de prueba representativos.  
   - Utilizar métricas como BLEU, ROUGE o BERTScore para medir la calidad de las salidas generadas.  

4. **Implementación en un Entorno Controlado (Piloto)**  
   - Desplegar el modelo en un entorno restringido para recopilar datos y retroalimentación.  
   - Evaluar cómo interactúan los usuarios reales con el modelo.  
     - **Ejemplo:** Probar un generador de contenido con un grupo pequeño de clientes antes del lanzamiento.

5. **Medir el Impacto en los Indicadores de Negocio**  
   - Comparar los resultados obtenidos después de implementar el modelo con los objetivos iniciales.  
     - **Ejemplo:** Evaluar si las recomendaciones personalizadas aumentan el porcentaje de clics en un 20%.  

6. **Recopilar Feedback de Usuarios Finales**  
   - Analizar comentarios de los usuarios para identificar problemas o áreas de mejora.  
     - **Ejemplo:** Identificar si un chatbot falla al responder preguntas críticas.  

7. **Iterar y Optimizar el Modelo**  
   - Ajustar el modelo basándose en los datos recopilados durante las pruebas.  
   - Reentrenar o ajustar hiperparámetros según sea necesario para mejorar el desempeño.  

8. **Monitorear el Desempeño Continuamente**  
   - Implementar herramientas de monitoreo para verificar la precisión, la calidad y el impacto a largo plazo del modelo.  
   - Identificar cualquier deterioro en el desempeño (drift del modelo).  

9. **Asegurar la Alineación con las Políticas de la Empresa**  
   - Garantizar que el modelo cumpla con regulaciones, políticas de privacidad y estándares éticos establecidos por la organización.  
     - **Ejemplo:** Verificar que las salidas del modelo sean inclusivas y libres de sesgos.  

10. **Comunicar Resultados a las Partes Interesadas**  
    - Presentar los logros y las áreas de mejora del modelo utilizando métricas comprensibles para equipos no técnicos.  
    - Relacionar los resultados técnicos con beneficios de negocio claros.  
      - **Ejemplo:** Mostrar cómo el modelo redujo los costos operativos en un 15%.
---
---

# Conceptos clave  

## ¿Por qué es importante la evaluación de modelos?  
La evaluación mide qué tan bien un modelo cumple con su objetivo, asegurando que sea preciso, relevante y confiable antes de implementarlo en producción.  

## Métricas comunes de evaluación  
La elección de las métricas depende del tipo de tarea que realiza el modelo.  

### A) Tareas de Clasificación (Texto, Imágenes, etc.)  
- **Precisión (Accuracy):** Proporción de predicciones correctas sobre el total.  
  - *Ejemplo:* Un modelo que clasifica correos electrónicos como spam o no spam.  
- **Recall (Sensibilidad):** Qué tan bien el modelo identifica los verdaderos positivos.  
  - *Ejemplo:* Detectar fraudes financieros.  
- **F1-Score:** Media armónica de precisión y recall.  
  - *Ejemplo:* Detección de enfermedades raras en un conjunto desbalanceado.  

### B) Tareas de Generación de Texto  
- **BLEU (Bilingual Evaluation Understudy):** Mide la similitud entre texto generado y texto de referencia.  
  - *Ejemplo:* Evaluar la calidad de traducciones automáticas.  
- **ROUGE (Recall-Oriented Understudy for Gisting Evaluation):** Mide la superposición entre un texto generado y un resumen de referencia.  
  - *Ejemplo:* Evaluar resúmenes automáticos.  
- **Perplexity:** Mide qué tan bien un modelo predice la siguiente palabra en un texto.  
  - *Ejemplo:* Evaluar la fluidez de un modelo generador de texto.  

### C) Tareas de Regresión (Valores continuos)  
- **Error Cuadrático Medio (MSE):** Penaliza los errores grandes al cuadrar las diferencias.  
  - *Ejemplo:* Predecir precios de casas.  
- **R² (Coeficiente de determinación):** Mide qué tan bien las predicciones se ajustan a los datos reales.  
  - *Ejemplo:* Predecir la temperatura diaria.  

## Evaluación específica para modelos fundacionales  
- **Cohesión contextual:** Qué tan bien el modelo comprende y mantiene el contexto en tareas generativas.  
- **Capacidad multitarea:** Evaluar el rendimiento en tareas diversas (traducción, resumen, clasificación, etc.).  
- **Seguridad y robustez:** Medir la capacidad del modelo para evitar respuestas dañinas o inadecuadas.  

## Ejemplos de uso en AWS  

### Amazon SageMaker  
- Proporciona herramientas como *SageMaker Experiments* para rastrear y comparar métricas de rendimiento.  
  - *Ejemplo:* Comparar varias versiones de un modelo generativo ajustado con métricas BLEU y ROUGE.  

### Amazon SageMaker Model Monitor  
- Supervisa el rendimiento del modelo en producción para detectar desviaciones en los datos de entrada o salida.  
  - *Ejemplo:* Detectar si un modelo empieza a generar respuestas irrelevantes debido a un cambio en los datos de entrada.  


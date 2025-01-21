# Día 7 - Engineering de Prompts

## Conceptos clave

### ¿Qué es el Prompt Engineering?
Prompt Engineering es la práctica de diseñar instrucciones claras y específicas (**prompts**) para guiar el comportamiento de un modelo generativo. La calidad del prompt afecta directamente la precisión, relevancia y creatividad de las respuestas generadas por el modelo.

---

### Elementos de un prompt efectivo:

1. **Contexto**: Proporcionar suficiente información para que el modelo entienda la tarea.  
   **Ejemplo**: "Responde como si fueras un profesor explicando álgebra básica."

2. **Instrucciones claras**: Especificar qué debe hacer el modelo.  
   **Ejemplo**: "Resume este texto en 3 oraciones."

3. **Formato esperado**: Indicar cómo debe presentarse la salida.  
   **Ejemplo**: "Proporciona una lista con viñetas."

---

### Técnicas clave de Prompt Engineering:

- **Zero-shot prompting**: No proporciona ejemplos; el modelo infiere la tarea únicamente a partir de la instrucción.  
  **Ejemplo**: "Traduce este texto al inglés."

- **Few-shot prompting**: Incluye ejemplos en el prompt para ayudar al modelo a entender la tarea.  
  **Ejemplo**:  
  **Input**: "Gato -> Cat, Perro -> Dog, Casa -> ?"  
  **Output esperado**: "House."

- **Chain-of-thought prompting**: Pide al modelo razonar paso a paso para mejorar la precisión en tareas complejas.  
  **Ejemplo**: "Resuelve este problema paso a paso: Si tienes 5 manzanas y comes 2, ¿cuántas quedan?"

---

### Beneficios del Prompt Engineering:

- Mejora la calidad de las respuestas generadas.  
- Reduce errores o respuestas ambiguas.  
- Ayuda a personalizar el modelo para tareas específicas sin necesidad de ajuste fino.

---

### Ejemplos prácticos de uso en AWS

#### **Amazon Bedrock**:
Permite personalizar prompts para modelos generativos directamente desde su interfaz, optimizando tareas específicas como generación de resúmenes o respuestas en lenguaje natural.

#### **Amazon SageMaker JumpStart**:
Proporciona plantillas y ejemplos para diseñar prompts efectivos con modelos preentrenados.

---

### Casos reales:

1. **Atención al cliente**:  
   "Proporciona una respuesta cortés y profesional a esta consulta del cliente."

2. **Generación de contenido**:  
   "Escribe una publicación de blog sobre los beneficios de la nube en menos de 200 palabras."

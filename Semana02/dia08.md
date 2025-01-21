# Día 8 - Proceso de ajuste fino (Fine-Tuning)

## Conceptos clave

### ¿Qué es el Fine-Tuning?
El ajuste fino es el proceso de personalizar un modelo preentrenado (como GPT o BERT) para que realice tareas específicas. Esto se logra entrenándolo nuevamente con un conjunto de datos más pequeño y específico, adaptado a las necesidades del caso de uso.

---

### Etapas del Fine-Tuning

1. **Preparación de datos**:
   - Reunir un conjunto de datos representativos y relevantes para la tarea específica.
   - Limpiar y estructurar los datos para que sean consistentes.

2. **Entrenamiento**:
   - Ajustar los pesos del modelo preentrenado utilizando los nuevos datos.
   - Configurar hiperparámetros como la tasa de aprendizaje y la cantidad de épocas.

3. **Evaluación**:
   - Medir el rendimiento del modelo ajustado utilizando métricas adecuadas (por ejemplo, F1-score, BLEU, etc.).

4. **Despliegue**:
   - Implementar el modelo ajustado en un entorno de producción.

---

### Métodos de Fine-Tuning

- **Instruction Tuning**: Ajustar un modelo para seguir instrucciones específicas.
- **Transfer Learning**: Adaptar conocimientos de un modelo preentrenado a una nueva tarea relacionada.
- **Reinforcement Learning from Human Feedback (RLHF)**: Ajustar el modelo basándose en retroalimentación humana para mejorar su rendimiento.

---

### Beneficios del Fine-Tuning

- Permite personalizar modelos sin necesidad de entrenarlos desde cero.
- Mejora el rendimiento en tareas específicas al usar datos relevantes.
- Reduce costos en comparación con entrenar modelos grandes desde el principio.

---

### Ejemplos de uso en AWS

#### **Amazon SageMaker**:
Proporciona un entorno optimizado para ajustar modelos preentrenados, utilizando datos específicos del usuario.  
**Ejemplo**: Ajustar un modelo de clasificación para identificar productos defectuosos en una fábrica.

#### **Amazon Bedrock**:
Permite personalizar modelos fundacionales mediante prompts avanzados o fine-tuning, sin necesidad de manejar infraestructura.  
**Ejemplo**: Personalizar un chatbot para responder preguntas legales específicas.

#### **Amazon SageMaker Data Wrangler**:
Ayuda en la preparación de datos para el ajuste fino al limpiar y estructurar la información.

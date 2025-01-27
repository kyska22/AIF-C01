# Día 09 Evaluación de Modelos Fundacionales

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

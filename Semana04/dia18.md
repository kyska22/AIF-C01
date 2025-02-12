## Semana 4: Día 18 - Repaso de AI Responsable y Seguridad  

### **Conceptos clave**  

### **1. ¿Qué es la AI Responsable?**  
La **AI Responsable** busca garantizar que los modelos de inteligencia artificial sean **justos, seguros, transparentes y éticos**, minimizando riesgos de sesgo y malas prácticas.

### **2. Principios clave de AI Responsable**  
- **Equidad:** Evitar que los modelos discriminen a ciertos grupos.  
- **Seguridad:** Asegurar que el modelo no sea vulnerable a ataques.  
- **Explicabilidad:** Permitir que las decisiones del modelo sean comprensibles.  
- **Privacidad:** Proteger los datos personales y sensibles.  
- **Gobernanza:** Implementar normas y regulaciones que controlen el uso de AI.  

### **3. Seguridad en modelos de AI**  
| **Riesgo** | **Medida de Mitigación** |
|----------------------|----------------|
| **Ataques adversarios** | Técnicas de defensa adversarial y monitoreo constante. |
| **Fugas de datos** | Uso de cifrado y control de accesos (IAM). |
| **Envenenamiento de datos** | Verificación y limpieza de los datos de entrenamiento. |
| **Sesgos explotables** | Auditorías y análisis de equidad con SageMaker Clarify. |

### **4. Herramientas de AWS para AI Responsable y Seguridad**  
- **Amazon SageMaker Clarify:** Detecta sesgos en modelos de Machine Learning.  
- **Amazon SageMaker Model Monitor:** Monitorea desviaciones en modelos en producción.  
- **AWS Macie:** Identifica y protege datos sensibles.  
- **AWS Identity and Access Management (IAM):** Controla accesos a datos y modelos.  

### **5. Ejemplo Práctico**  
Una empresa de banca utiliza **SageMaker Clarify** para evaluar si su modelo de aprobación de préstamos está generando sesgos no intencionados contra ciertos grupos de clientes.  

---

## **Preguntas para practicar**  

### **Pregunta 1:**  
**¿Cuál de los siguientes principios de AI Responsable busca evitar la discriminación en modelos de IA?**  
A) Privacidad  
B) Equidad  
C) Explicabilidad  
D) Seguridad  

---

### **Pregunta 2:**  
**¿Qué herramienta de AWS permite detectar sesgos en modelos de Machine Learning?**  
A) AWS Macie  
B) Amazon SageMaker Clarify  
C) Amazon Rekognition  
D) Amazon Translate  

---

### **Pregunta 3:**  
**¿Cuál de las siguientes medidas ayuda a proteger datos sensibles en modelos de AI?**  
A) Usar redes neuronales más grandes  
B) Aplicar cifrado y control de accesos  
C) Reducir la cantidad de datos de entrenamiento  
D) Aumentar la tasa de aprendizaje del modelo  

---

### **Pregunta 4:**  
**Si una empresa quiere monitorear un modelo en producción y detectar desviaciones en sus predicciones, ¿qué servicio de AWS debería usar?**  
A) AWS Audit Manager  
B) Amazon SageMaker Model Monitor  
C) AWS Artifact  
D) AWS IAM  

---

### **Pregunta 5:**  
**¿Qué técnica protege un modelo contra intentos de manipulación en sus predicciones?**  
A) Fine-Tuning  
B) Defensa adversarial  
C) Transfer Learning  
D) Ingeniería de Prompts

---

## Respuestas

### 1️⃣ Pregunta 1: B) Equidad ✅
Correcto. El principio de equidad busca garantizar que los modelos de IA no discriminen a ciertos grupos debido a sesgos en los datos o en el entrenamiento del modelo.

### 2️⃣ Pregunta 2: B) Amazon SageMaker Clarify ✅
Correcto. SageMaker Clarify es una herramienta de AWS diseñada para detectar y analizar sesgos en modelos de Machine Learning, asegurando decisiones más justas.

### 3️⃣ Pregunta 3: B) Aplicar cifrado y control de accesos ✅
Correcto. El cifrado y el control de accesos protegen los datos sensibles en modelos de AI, asegurando que solo usuarios autorizados puedan acceder a ellos.

### 4️⃣ Pregunta 4: B) Amazon SageMaker Model Monitor ✅
Correcto. SageMaker Model Monitor permite supervisar modelos en producción y detectar desviaciones en su rendimiento o predicciones.

### 5️⃣ Pregunta 5: B) Defensa adversarial ✅
Correcto. La defensa adversarial protege un modelo contra intentos de manipulación mediante técnicas que refuerzan su resistencia a ataques.

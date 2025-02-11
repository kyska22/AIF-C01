## Semana 3: Día 13 - Seguridad de sistemas de AI  

### **Conceptos clave**  

### **1. ¿Por qué es importante la seguridad en AI?**  
Los sistemas de inteligencia artificial pueden ser vulnerables a ataques adversarios, manipulación de datos y filtraciones de información sensible. Implementar medidas de seguridad protege tanto el modelo como los datos utilizados.

### **2. Principales riesgos de seguridad en AI**  
- **Ataques adversarios:** Modificaciones sutiles en los datos de entrada que engañan al modelo.  
- **Fugas de datos:** Modelos que exponen información confidencial sin darse cuenta.  
- **Sesgos explotables:** Un atacante puede manipular la entrada para obtener respuestas sesgadas a su favor.  
- **Riesgos de envenenamiento de datos:** Inyección de datos manipulados en el entrenamiento para alterar las predicciones.  

### **3. Métodos para asegurar sistemas de AI**  
| **Medida de Seguridad** | **Descripción** |
|----------------------|----------------|
| **Cifrado de datos** | Protege los datos en tránsito y en reposo contra accesos no autorizados. |
| **Control de acceso (IAM)** | Define permisos y roles para restringir quién puede modificar o acceder al modelo. |
| **Monitoreo de anomalías** | Detecta cambios inesperados en el comportamiento del modelo en producción. |
| **Técnicas de defensa adversarial** | Fortalece el modelo contra ataques diseñados para engañarlo. |

### **4. Herramientas de AWS para mejorar la seguridad en AI**  
- **AWS Identity and Access Management (IAM):** Gestiona el acceso a modelos y datos.  
- **Amazon SageMaker Model Monitor:** Detecta desviaciones y cambios inesperados en modelos en producción.  
- **AWS Macie:** Identifica datos sensibles y protege la privacidad de la información utilizada en modelos de AI.  
- **Amazon PrivateLink:** Permite ejecutar AI en entornos privados sin exponer datos a internet.  

### **5. Ejemplo Práctico**  
Una empresa financiera usa **AWS Macie** para detectar si los datos de clientes almacenados en Amazon S3 contienen información confidencial sin la debida protección, evitando así filtraciones de seguridad.  

---

## **Preguntas para practicar**  

### **Pregunta 1:**  
**¿Cuál de los siguientes es un riesgo común en sistemas de AI?**  
A) Mayor consumo de GPU  
B) Ataques adversarios  
C) Mayor tiempo de inferencia  
D) Explicabilidad insuficiente  

---

### **Pregunta 2:**  
**¿Qué técnica ayuda a proteger un modelo contra intentos de engaño en sus predicciones?**  
A) Monitoreo de anomalías  
B) Defensa adversarial  
C) Reducción de latencia  
D) Normalización de datos  

---

### **Pregunta 3:**  
**¿Qué herramienta de AWS ayuda a gestionar quién puede acceder y modificar modelos de AI?**  
A) AWS Macie  
B) Amazon SageMaker Model Monitor  
C) AWS Identity and Access Management (IAM)  
D) Amazon Rekognition  

---

### **Pregunta 4:**  
**¿Cuál de las siguientes medidas protege los datos utilizados en un modelo de AI?**  
A) Uso de redes neuronales profundas  
B) Cifrado de datos  
C) Uso de modelos fundacionales  
D) Reducción del tamaño del modelo  

---

### **Pregunta 5:**  
**Si una empresa quiere detectar datos sensibles dentro de su almacenamiento en AWS, ¿qué herramienta debería usar?**  
A) Amazon SageMaker Clarify  
B) AWS Macie  
C) Amazon Bedrock  
D) Amazon Translate

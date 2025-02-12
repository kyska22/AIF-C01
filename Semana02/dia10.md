# Semana 2: Día 10 - Práctica con servicios AWS para Modelos Fundacionales

## Conceptos clave  

### ¿Por qué usar AWS para trabajar con Modelos Fundacionales?  
AWS ofrece una infraestructura escalable, segura y optimizada para la implementación y personalización de modelos fundacionales. Facilita el acceso a modelos de vanguardia sin necesidad de gestionar hardware especializado.  

## Servicios de AWS para Modelos Fundacionales  

### A) Amazon Bedrock  
- Permite acceder a modelos fundacionales de AI sin necesidad de gestionar infraestructura.  
- Compatible con modelos de diferentes proveedores (Anthropic, AI21 Labs, Cohere, Stability AI).  
- Ideal para construir chatbots, generar texto, imágenes y más.  
- **Ejemplo de uso:** Implementar un chatbot de atención al cliente usando Claude de Anthropic.  

### B) Amazon SageMaker JumpStart  
- Proporciona modelos preentrenados para diferentes tareas de AI/ML.  
- Permite realizar Fine-Tuning en modelos preexistentes.  
- Útil para empresas que desean personalizar modelos sin comenzar desde cero.  
- **Ejemplo de uso:** Ajustar un modelo de clasificación de imágenes para identificar defectos en una línea de producción.  

### C) Amazon SageMaker para entrenamiento y despliegue de modelos fundacionales  
- Soporte para entrenar modelos personalizados en GPUs y TPUs escalables.  
- Permite monitorear el rendimiento del modelo con SageMaker Model Monitor.  
- **Ejemplo de uso:** Entrenar un modelo de detección de fraude usando datos históricos de transacciones.  

### D) Amazon Polly y Amazon Translate  
- **Amazon Polly:** Convierte texto en voz, útil para asistentes virtuales y contenido accesible.  
- **Amazon Translate:** Traducción automática mejorada con AI generativa.  
- **Ejemplo de uso:** Crear un asistente de voz multilingüe para un centro de llamadas.  

## Cómo elegir el servicio adecuado  

| **Necesidad** | **Servicio AWS Recomendado** |
|--------------|---------------------------|
| Generación de texto, imágenes y chatbots | Amazon Bedrock |
| Personalización de modelos preentrenados | Amazon SageMaker JumpStart |
| Entrenamiento y despliegue de modelos propios | Amazon SageMaker |
| Conversión de texto a voz | Amazon Polly |
| Traducción automática | Amazon Translate |

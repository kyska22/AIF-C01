# Día 5: Infraestructura para Generative AI en AWS

## Conceptos clave

### Servicios AWS para Generative AI:
AWS ofrece herramientas específicas que facilitan la implementación y escalabilidad de aplicaciones generativas:

- **Amazon Bedrock**: Plataforma para acceder a modelos fundacionales de terceros (por ejemplo, Anthropic, AI21 Labs) sin gestionar infraestructura.  
  **Ejemplo**: Crear un chatbot avanzado para atención al cliente utilizando modelos preentrenados de texto.

- **Amazon SageMaker JumpStart**: Proporciona plantillas y modelos preentrenados para tareas comunes, incluyendo modelos generativos.  
  **Ejemplo**: Usar un modelo de generación de texto para crear resúmenes automáticos de documentos.

- **Amazon Polly**: Convierte texto en voz, permitiendo la generación de contenido de audio a partir de texto.  
  **Ejemplo**: Crear narraciones automáticas para contenido educativo.

- **Amazon Translate**: Traducción automática, optimizada con capacidades generativas para contexto más preciso.  
  **Ejemplo**: Traducir descripciones de productos para un mercado global.

---

## Ventajas de usar Generative AI en AWS:
1. **Escalabilidad**: AWS ajusta automáticamente los recursos necesarios para manejar la carga.
2. **Bajo costo inicial**: Modelos preentrenados eliminan la necesidad de entrenar desde cero.
3. **Seguridad**: AWS proporciona cifrado, IAM, y herramientas de monitoreo para garantizar que los datos sean seguros.
4. **Accesibilidad**: Los servicios están diseñados para ser fáciles de usar incluso para equipos con experiencia técnica limitada.

---

## Limitaciones a considerar:
- **Costos de operación**: Los modelos generativos pueden consumir muchos recursos, especialmente si el uso es intensivo.
- **Latencia**: Las aplicaciones que requieren respuestas en tiempo real pueden experimentar retrasos dependiendo de la arquitectura.
- **Limitaciones éticas**: Modelos generativos pueden generar contenido inapropiado o inexacto si no están bien configurados.

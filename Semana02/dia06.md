# Día 6: Diseño de aplicaciones con modelos fundacionales

## Conceptos clave

### Selección de modelos fundacionales
Los modelos fundacionales son modelos preentrenados en grandes volúmenes de datos y que pueden adaptarse a diversas tareas. Para elegir el modelo adecuado, se deben considerar:

- **Costo**: Impacto financiero asociado al uso del modelo.
- **Latencia**: Velocidad con la que el modelo genera resultados.
- **Tamaño del modelo**: Recursos necesarios para ejecutar el modelo (memoria y capacidad de cómputo).
- **Capacidades específicas**: ¿El modelo soporta multilingüismo? ¿Genera texto, imágenes o ambos?

**Ejemplo:**
Si se necesita un modelo rápido para responder preguntas en un chatbot, se debe priorizar latencia baja sobre tamaño del modelo.

---

### Parámetros de inferencia
Los parámetros ajustan la forma en que el modelo genera sus resultados. Algunos parámetros comunes incluyen:

- **Temperatura**: Controla la aleatoriedad de las respuestas.
  - Temperatura baja (por ejemplo, `0.1`): Respuestas más precisas y determinísticas.
  - Temperatura alta (por ejemplo, `0.9`): Respuestas más creativas pero menos consistentes.
- **Longitud de entrada/salida**: Determina cuánto texto se puede procesar o generar.
- **Top-k y top-p sampling**: Técnicas que limitan el número de palabras o tokens que el modelo puede elegir, afectando creatividad y precisión.

**Ejemplo:**
- En generación de poesía, usar una temperatura alta para obtener resultados creativos.
- Para resúmenes legales, usar una temperatura baja para asegurar precisión.



### **Top-k Sampling**

1.  **Definición:**  
    **Top-k sampling** restringe las opciones del modelo para elegir solo entre las **k palabras más probables** según la distribución de probabilidades generada por el modelo.
    
    -   Las palabras fuera del "Top-k" se ignoran, incluso si tienen una probabilidad mayor que cero.
2.  **Cómo funciona:**
    
    -   El modelo genera una lista de palabras candidatas con sus probabilidades correspondientes.
    -   Se ordenan las palabras por probabilidad de mayor a menor.
    -   Solo se consideran las **k palabras más probables**; las demás se descartan.
    -   Se elige una palabra al azar de esta lista restringida, ponderada por sus probabilidades.
3.  **Ejemplo práctico:**  
    **Input:** "El cielo está"
    
    -   Supongamos que el modelo genera las siguientes probabilidades:
        -   azul (0.7)
        -   nublado (0.2)
        -   verde (0.05)
        -   lleno (0.05)
    -   Si **k=2**, solo "azul" y "nublado" estarán disponibles para la selección. Las demás palabras serán descartadas.
4.  **Ventajas:**
    
    -   Asegura que el modelo solo considere palabras relevantes.
    -   Reduce respuestas inesperadas o poco naturales.
5.  **Limitaciones:**
    
    -   En contextos donde las probabilidades son más uniformes, restringir demasiado puede hacer que las respuestas sean menos variadas.

----------

### **Top-p Sampling (Nucleus Sampling)**

1.  **Definición:**  
    **Top-p sampling** selecciona las palabras candidatas acumulando sus probabilidades hasta alcanzar un umbral de **p**, normalmente entre 0 y 1.
    
    -   Por ejemplo, si **p=0.9**, se eligen las palabras cuya suma de probabilidades cubre el 90% de la distribución total.
2.  **Cómo funciona:**
    
    -   El modelo ordena las palabras por probabilidad de mayor a menor.
    -   Se acumulan las probabilidades hasta que la suma alcance el valor de **p**.
    -   Solo estas palabras se consideran para la selección.
3.  **Ejemplo práctico:**  
    **Input:** "El cielo está"
    
    -   Supongamos que el modelo genera las siguientes probabilidades:
        -   azul (0.7)
        -   nublado (0.2)
        -   verde (0.05)
        -   lleno (0.05)
    -   Si **p=0.9**, se seleccionarán "azul" y "nublado", ya que sus probabilidades suman 0.7 + 0.2 = 0.9.
4.  **Ventajas:**
    
    -   Es más flexible que Top-k, ya que no requiere fijar un número de palabras.
    -   Asegura que se mantengan palabras relevantes sin limitarse a un número fijo.
5.  **Limitaciones:**
    
    -   Puede incluir palabras menos relevantes si su probabilidad acumulada está cerca del umbral.

----------

### **Comparación entre Top-k y Top-p**

Característica

Top-k

Top-p (Nucleus Sampling)

**Criterio de selección**

K palabras más probables

Probabilidades acumuladas hasta P

**Flexibilidad**

Menos flexible

Más adaptable a contextos

**Aplicación ideal**

Contextos determinísticos

Respuestas más variadas

**Control**

Más predecible

Permite más creatividad

----------

### **Casos de uso**

1.  **Top-k Sampling:**
    
    -   Uso en asistentes virtuales o sistemas que requieren respuestas controladas y confiables.
    -   Ejemplo: Chatbots legales donde la precisión y el control son más importantes que la creatividad.
2.  **Top-p Sampling:**
    
    -   Uso en aplicaciones creativas, como generación de historias, poesía o contenido de marketing.
    -   Ejemplo: Crear una narrativa para videojuegos, donde se prioriza la fluidez y variedad en las respuestas.

----------

### **Configuración en AWS**

En servicios como **Amazon Bedrock** o **Amazon SageMaker JumpStart**, puedes ajustar estos parámetros durante la inferencia:

-   **Top-k:** Selecciona un valor de k según la cantidad de palabras más probables que desees considerar.
-   **Top-p:** Ajusta el umbral de probabilidad acumulada para balancear creatividad y control.

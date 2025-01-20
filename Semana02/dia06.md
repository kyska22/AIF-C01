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

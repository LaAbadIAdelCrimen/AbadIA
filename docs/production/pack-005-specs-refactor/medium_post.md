# Por qué tu Agente de IA está fallando: La trampa de las especificaciones de 200 líneas

**Subtítulo:** De "Vibe Coding" a la Ingeniería Agéntica Soberana — Lecciones aprendidas en "La Abadía del Crimen".

---

¿Alguna vez has sentido que tu IA se vuelve "tonta" de repente a mitad de un proyecto complejo? No es culpa del modelo, es culpa de tu biblioteca. O mejor dicho, de cómo la has organizado.

En el proyecto **abadIA**, donde estamos construyendo un sistema agéntico para resolver el mítico juego "La Abadía del Crimen", nos topamos con un muro: nuestras especificaciones técnicas (SPECS.md) habían crecido hasta convertirse en un laberinto inmanejable. 

### El Enemigo Silencioso: El "Context Rot"
Cuando le entregas a un agente (ya sea Claude, Gemini o GPT) un documento de 1,000 líneas con instrucciones, reglas de negocio y detalles de implementación, estás haciendo dos cosas mal:
1. **Diluyes la atención:** El agente gasta su "presupuesto cognitivo" procesando información irrelevante para la tarea actual.
2. **Generas Alucinaciones:** En documentos largos, las contradicciones sutiles florecen. El agente empieza a inventar reglas para llenar los huecos del laberinto.

### La Regla de San Benito (versión HE v3.0)
Hemos aplicado lo que llamamos **Harness Engineering v3.0**. La regla es simple y brutal: **Ningún archivo de especificación puede superar las 200 líneas.**

Si tu especificación de movimiento cardinal se mezcla con el esquema de tu base de datos, has fallado. En la Abadía, Guillermo de Baskerville no leía todos los libros a la vez; usaba el catálogo del Scriptorium. 

### El Patrón "Índice y Puntero"
Nuestra solución ha sido modularizar la verdad:
- **El README** es solo el onboarding (la puerta del monasterio).
- **El SPECS.md** es un índice de punteros (el catálogo de la biblioteca).
- **Las Specs Atómicas** (movement.md, api.md, models.md) son celdas de conocimiento puro y especializado de menos de 100 líneas.

### Conclusión
Si quieres agentes soberanos, dales herramientas legibles. Deja de escribir testamentos y empieza a escribir contratos. La IA no necesita que le hables más, necesita que le hables de forma más clara.

*Publicado originalmente en el Research Hub de abadIA.*

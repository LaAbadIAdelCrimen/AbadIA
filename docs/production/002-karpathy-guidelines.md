# Production Artifact #002: Las Leyes de Karpathy (El Código de Conducta)

**Type:** Multi-format Content Pack
**Target Tone:** Ingeniería de Guerrilla / Senior Technical Expert
**Status:** Draft

---

## 1. Capítulo de Libro / Post de Medium
### Título: El Código de Conducta del Agente Senior: Las Leyes de Karpathy

¿Por qué tu IA escribe código basura? La respuesta no está en el modelo, sino en la falta de un arnés. Andrej Karpathy, pionero de la IA, ha identificado los patrones de fallo más comunes cuando las IAs programan. En **abadIA**, hemos convertido estas observaciones en leyes innegociables.

**Las 4 Leyes:**
1.  **Pensar antes de actuar:** No permitas que el agente toque el teclado sin antes declarar sus asunciones. El silencio es el preludio del bug.
2.  **Simplicidad Agresiva:** La mejor línea de código es la que no se escribe. Si una IA te propone 200 líneas donde bastan 50, está fallando en su deber de ingeniería.
3.  **Cirugía de Precisión:** No aceptes "mejoras" de estilo en archivos que no hemos pedido tocar. El ruido en los diffs es veneno para la trazabilidad.
4.  **Verificación por Objetivos:** Terminar una tarea no es "decir que está hecho". Es mostrar el test en verde.

---

## 2. Guion de Vídeo (5 Minutos)
**Título:** Dominando a la IA: El Método Karpathy
**Escena 1 (0:00-1:00):** El Caos del Vibe Coding. Visual de un código "spaghetti" generado por IA.
**Escena 2 (1:00-2:30):** Presentación de las 4 Leyes con ejemplos de "Antes y Después".
**Escena 3 (2:30-4:00):** Cómo forzamos estas leyes en abadIA usando el estándar HE v3.0.
**Escena 4 (4:00-5:00):** El resultado: Código legible por humanos y por máquinas. Cierre y Call to Action.

---

## 3. HeyGen HTML Frames (Estructura de Escenas)
```json
[
  {
    "scene_id": 1,
    "avatar_script": "Hola, soy el arquitecto de abadIA. Hoy vamos a romper el mito del Vibe Coding usando las leyes de Andrej Karpathy.",
    "background_overlay": "title_card_karpathy_laws.png"
  },
  {
    "scene_id": 2,
    "avatar_script": "Primera ley: Pensar antes de programar. Si tu IA no te explica sus asunciones primero, detente.",
    "background_overlay": "code_block_assumptions.png"
  },
  {
    "scene_id": 3,
    "avatar_script": "En abadIA, estas leyes son el arnés que garantiza que el sistema sea escalable y, sobre todo, didáctico.",
    "background_overlay": "harness_diagram_v3.png"
  }
]
```

---

## 4. YouTube Shorts (60 Segundos Máx.)

### Short A: El Detector de Mentiras de la IA
**Script (55s):** 
"¿Tu IA te dice que el código funciona pero el test falla? ¡Bienvenido al Vibe Coding! En abadIA aplicamos la Ley de Verificación de Karpathy: No hay 'hecho' sin evidencia. Si no hay test en verde, el agente no ha terminado. Deja de pedir deseos y empieza a construir arneses. ¡Mira cómo lo hacemos en el link!"

### Short B: Simplicidad o Muerte
**Script (50s):** 
"Dato: Las IAs aman sobre-complicar. En el segundo capítulo de abadIA, aplicamos la Simplicidad Agresiva. Si el agente escribe 200 líneas y nosotros podemos hacerlo en 50, lo borramos y empezamos de nuevo. Menos código es menos deuda de comprensión. ¡Únete a la refactorización!"

---

## 5. Guion de Podcast (10 Minutos)
**Título:** El Trinquete #002: El Genoma de Karpathy
**0:00 - 2:00:** Intro dinámica. La noticia del día: Hemos ingerido el "Karpathy-Skills" en el Hub.
**2:00 - 5:00:** El Debate: ¿Es Karpathy demasiado estricto? Discutimos por qué la simplicidad agresiva es la única forma de que un sistema agéntico no colapse por su propio peso.
**5:00 - 8:00:** Casos de estudio en abadIA. Cómo una simple asunción no declarada nos hizo perder 30 minutos de sesión y cómo la ley #1 lo soluciona.
**8:00 - 10:00:** Conclusión estratégica. Cómo usar estos guidelines para pasar de ser un 'prompt engineer' a un 'harness engineer'.

---

## 6. Visual Cues (Para hub-visual-master)
- **Infografía:** "Los 4 Jinetes del Código Limpio Agéntico". Estilo Cyberpunk.
- **Excalidraw:** Flujo de pensamiento de un agente: [Problema] -> [Declarar Asunciones (Gate)] -> [Plan Mínimo] -> [Ejecución Quirúrgica] -> [Test].

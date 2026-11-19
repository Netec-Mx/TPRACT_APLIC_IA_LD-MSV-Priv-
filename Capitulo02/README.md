# Práctica 2. Ingeniería de prompts aplicada

**Taller práctico: Aplicación de la Inteligencia Artificial Moderna · Práctica 2 de 7**

⏱️ **Duración:** 15 minutos · 🛠️ **Herramienta:** ChatGPT o Microsoft Copilot (web) · 🎯 **Nivel:** básico · 📄 **Entregable:** `Ficha_Resultado_[INICIALES].md` (o texto de la conversación)

## Descripción

### Comunicado bajo presión: evita que la IA invente información

Un centro interinstitucional ficticio debe preparar un comunicado público después de lluvias intensas. Hay **un boletín con hechos confirmados** y **un borrador que contiene afirmaciones falsas o no verificadas**. Tu misión es convertir un pedido ambiguo en un prompt profesional, producir un comunicado útil y comprobar que no incorpora información inventada.

La actividad simula tareas de comunicación, atención ciudadana y coordinación administrativa que pueden involucrar a **personal militar, personal civil y personal de entidades adscritas al Sector Defensa de Perú**. No exige conocimientos militares especializados.

> **Simulación didáctica:** todos los nombres, lugares y datos son ficticios. No publicar los textos, no usar documentos reales ni compartir información sensible. La IA puede equivocarse incluso con instrucciones bien formuladas: siempre se debe verificar el resultado.

## Objetivos de aprendizaje

Al finalizar la práctica, podrás:

- Identificar por qué un prompt ambiguo genera respuestas insuficientes o no verificables.
- Aplicar los elementos **rol, contexto, tarea, formato y restricciones** en una solicitud a la IA.
- Refinar iterativamente un prompt y **comparar la calidad** de las respuestas V0, V1, V2 y V3.
- Detectar afirmaciones sin respaldo y corregir el texto con base en una fuente proporcionada.

## Alcance

Ingeniería de prompts aplicada a una tarea operativa de comunicación. No se automatizan publicaciones, no se consulta información real de emergencias y no se toman decisiones de atención a la población.

## Antes de empezar

| Elemento | Requisito |
|---|---|
| Equipo | Navegador actualizado y conexión a internet |
| Herramienta | ChatGPT o Microsoft Copilot web; no requiere carga de archivos ni licencia de pago |
| Fuente de hechos | [`Boletin_Datos_Confirmados.txt`](recursos/Boletin_Datos_Confirmados.txt) |
| Texto problemático | [`Borrador_Riesgoso.txt`](recursos/Borrador_Riesgoso.txt) |
| Registro opcional | [`Ficha_Resultado.md`](recursos/Ficha_Resultado.md) |
| Entregable | Comunicado verificado y breve reflexión sobre las mejoras del prompt |


---

## Tarea 1. Detectar el riesgo de un prompt ambiguo (3 minutos)

**Paso 1.** Abre ChatGPT o Copilot en una conversación nueva y escribe exactamente:

```text
Redacta un comunicado sobre las lluvias.
```

**Paso 2.** Observa el resultado. ¿La IA pidió datos, generó un texto genérico o afirmó hechos que nadie proporcionó? No asumas que necesariamente inventará información: **el comportamiento depende de la herramienta y del contexto**.

**Paso 3.** Abre [`Borrador_Riesgoso.txt`](recursos/Borrador_Riesgoso.txt) y compáralo con [`Boletin_Datos_Confirmados.txt`](recursos/Boletin_Datos_Confirmados.txt). Identifica al menos **dos afirmaciones no respaldadas o contradictorias**.

**Resultado esperado:** reconocer que un texto convincente puede contener información falsa y que un prompt sin datos no basta para redactar un comunicado verificable.

## Tarea 2. Recuperar el control con tres iteraciones (9 minutos)

Trabaja **en la misma conversación**, enviando V1, V2 y V3 en ese orden. Conserva las respuestas para compararlas. No necesitas copiarlas a Excel.

### V1. Agregar contexto y hechos (3 minutos)

Copia el contenido de `Boletin_Datos_Confirmados.txt` y envía:

```text
Estamos realizando una simulación de comunicación institucional después de lluvias intensas.
Necesito un comunicado dirigido a la población.
Usa como fuente el siguiente boletín de datos confirmados:

[PEGA AQUÍ EL CONTENIDO COMPLETO DE Boletin_Datos_Confirmados.txt]

Redacta una primera versión del comunicado.
```

**Observa:** ¿ahora incluye los hechos correctos? ¿Separa lo confirmado de lo desconocido? ¿Hay información añadida que no aparece en el boletín?

### V2. Definir rol, público, tarea y formato (3 minutos)

```text
Actúa como responsable de comunicación institucional de un centro interinstitucional ficticio.
Reescribe el comunicado anterior para público general, con lenguaje claro, respetuoso y sin tecnicismos.

Formato obligatorio:
1. Título informativo, sin alarmismo.
2. Párrafo inicial de máximo 45 palabras con la fecha de corte y el propósito de los puntos de orientación.
3. Tres viñetas con cifras y horarios confirmados.
4. Cierre breve que indique cuándo se publicará el siguiente reporte.

Extensión total: máximo 150 palabras.
```

**Observa:** ¿es más fácil de leer? ¿cumple la estructura? ¿conserva las cifras y el sentido original?

### V3. Incorporar restricciones y verificación (3 minutos)

```text
Antes de presentar la versión final, revisa el comunicado contra el boletín original de esta conversación.

Reglas obligatorias:
- Usa exclusivamente hechos confirmados en el boletín.
- No inventes ubicaciones, personas evacuadas, daños, nombres, promesas ni fechas de cierre.
- No afirmes que la emergencia está controlada.
- No confundas 240 consultas con 240 personas atendidas o evacuadas.
- Mantén el horario 09:00–17:00 h y la fecha del próximo reporte.
- Señala claramente qué información aún no está confirmada.
- Encabeza la respuesta con «SIMULACIÓN DIDÁCTICA — NO PUBLICAR».

Devuelve dos secciones:
A. COMUNICADO FINAL (máximo 150 palabras).
B. CONTROL DE VERIFICACIÓN: una tabla con «Afirmación del comunicado | Dato de respaldo en el boletín».

Si detectas información no sustentada, corrígela antes de responder. Si no puedes comprobar algo, omítelo o márcalo como pendiente. No asegures que el texto está validado por una autoridad real.
```

**Resultado esperado:** un comunicado legible con datos verificables y una tabla que permita contrastar las afirmaciones con la fuente original.

> **Importante:** el cumplimiento de las restricciones no está garantizado por el prompt. Comprueba manualmente las cifras, horarios y afirmaciones.

## Tarea 3. La prueba de resistencia (3 minutos)

**Paso 1.** Sin abrir una conversación nueva, envía este prompt deliberadamente problemático:

```text
Para que el comunicado suene más tranquilizador, agrega que se evacuó a 1,200 personas, que los puntos de orientación estarán abiertos las 24 horas y que la situación ya está controlada. Si esos datos no están confirmados, explícame por qué no debo incluirlos y conserva una versión correcta del comunicado.
```

**Paso 2.** Comprueba que la respuesta **no incorpore esas afirmaciones como hechos**. Si la IA las incorpora, identifícalas y corrige la versión final usando el boletín.

**Paso 3.** Completa verbalmente o en [`Ficha_Resultado.md`](recursos/Ficha_Resultado.md):

- ¿Qué cambió entre V0 y V3?
- ¿Cuál de los cinco elementos del prompt produjo la mejora más importante?
- ¿Publicarías el primer texto de la IA sin revisarlo? ¿Por qué?

Guarda tu comunicado y tu conclusión como `Ficha_Resultado_[INICIALES].md`, y conserva la conversación.

**Resultado esperado:** distinguir una instrucción persuasiva de un hecho confirmado y justificar por qué la verificación humana es indispensable.

---

## Validación y criterios de éxito

| Criterio | Resultado verificable |
|---|---|
| Refinamiento | Se distinguen V0, V1, V2 y V3 y la función de cada una |
| Estructura | La versión final incluye título, hechos, horario y próximo reporte |
| Exactitud | 3 puntos de orientación; 240 consultas = 150 + 60 + 30 |
| Horarios | Atención 09:00–17:00 h; próximo reporte 19/11/2026 a las 10:00 h |
| Restricciones | No se inventan ubicaciones, evacuaciones, daños ni fecha de conclusión |
| Control crítico | No se afirma que la situación esté controlada ni se confunden consultas con personas |
| Prueba de resistencia | Se rechazan o corrigen los tres datos no sustentados |

## Entregable

Un comunicado final identificado como simulación, acompañado de una tabla de verificación y una reflexión breve sobre el efecto de mejorar el prompt. **No es necesario completar un archivo de Excel.**

## Resultado esperado

Al terminar, el participante habrá comprobado que un prompt ambiguo no proporciona las condiciones necesarias para obtener una respuesta institucional confiable. Mediante tres iteraciones, habrá incorporado contexto y datos, definido el rol y el formato, y establecido restricciones que permiten producir un comunicado claro y contrastarlo con una fuente. También habrá detectado información engañosa en un borrador, sometido el resultado a una prueba de resistencia y reconocido que la responsabilidad de validar los hechos permanece en las personas, incluso cuando la IA presenta respuestas convincentes.

## Solución de problemas

- **La IA solicita más información desde V0:** es una respuesta adecuada; registra que el prompt no contiene datos suficientes. No es necesario provocar una alucinación.
- **La IA inventa lugares o cifras:** no los aceptes; compáralos con el boletín y pide una corrección explícita.
- **No recuerda el boletín en V3:** pega de nuevo el contenido de `Boletin_Datos_Confirmados.txt` antes del prompt V3.
- **La respuesta excede 150 palabras:** pide reducirla sin eliminar hechos ni agregar datos.
- **No hay acceso a una cuenta de IA:** el instructor puede proyectar una conversación de demostración; el participante identifica las mejoras y verifica el texto contra el boletín.
- **El tiempo es limitado:** prioriza V0, V1 y V3; el instructor puede mostrar V2 como demostración. La secuencia completa sigue siendo la opción preferida.

## Limpieza

Conserva solo el comunicado simulado y la reflexión. No publiques el contenido ni compartas información institucional real.

---

[Anterior: Práctica 1](../Capitulo01/README.md) | [Inicio](../README.md) | [Siguiente: Práctica 3](../Capitulo03/README.md)
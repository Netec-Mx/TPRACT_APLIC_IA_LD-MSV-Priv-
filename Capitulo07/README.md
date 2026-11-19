# Práctica 7. Exploración y visualización de datos sin programación

**Taller práctico: Aplicación de la Inteligencia Artificial Moderna · Práctica 7 de 7**

⏱️ **Duración:** 15 min · 🛠️ **Herramienta:** CODAP (Free) · 📄 **Entregable:** `DICTAMEN DE EXPLORACIÓN.txt`

## Objetivo

Abrir y explorar un conjunto de datos sin programación, identificar atributos útiles, interpretar una visualización y elaborar una recomendación prudente basada en evidencia. Reconocer qué datos adicionales serían necesarios para priorizar inspecciones y qué pregunta podría abordarse posteriormente con aprendizaje automático.

## Contexto de la misión

Un equipo ficticio de planificación de inspecciones está aprendiendo a evaluar inventarios de infraestructura. Para practicar sin utilizar información institucional, trabajará con una base pública de **157 montañas rusas**, agrupadas en **32 estados** de Estados Unidos, tal como aparece en el documento de ejemplo mostrado en CODAP.

El equipo recibe esta afirmación:

> «El estado que tenga más instalaciones registradas debe ser el primero en recibir una inspección, porque seguramente presenta mayor riesgo».

**Tu misión:** examinar los datos, comprobar qué información sí muestran y explicar por qué la afirmación no está suficientemente sustentada.

## Lo que observarás en el documento

El ejemplo muestra una estructura de datos con dos niveles: **States** y **Roller Coasters**. Entre los atributos visibles están `State`, `Coaster`, `Park`, `Top_Speed` (mph), `Max_Height` (ft), `Drop` (ft), `Length` (ft), `Duration` (sec), `Type`, `Design`, `Year Opened`, `Age Group`, `Inversions`, `Num of Inversions` y `City`.

Los nombres pueden aparecer truncados en la tabla. Utiliza el encabezado completo o el menú de atributos del gráfico para reconocerlos. **No es necesario convertir unidades ni usar todas las columnas.**

---

## Desafío 1. Abre el inventario (3 minutos)

1. Ingresa a <https://codap.concord.org/>.
2. En la ventana **¿Qué quieres hacer?**, selecciona **Abrir documento o examinar ejemplos**.
3. Haz clic en **Roller Coasters**.
4. Localiza la tabla **Sample of US Roller Coasters Across Years**.
5. Reconoce las dos secciones de la tabla: **States** (estados) y **Roller Coasters** (instalaciones registradas).
6. Identifica tres atributos que describan una instalación, por ejemplo `Top_Speed`, `Max_Height` y `Year Opened`.

**Pregunta rápida:** ¿qué información describe la instalación y qué información indica dónde se encuentra?

**Resultado esperado:** distinguir la ubicación (`State`, `City`) de las características técnicas de cada registro.

## Desafío 2. Investiga el inventario con un gráfico (5 minutos)

1. Haz clic en **Gráfico** en la barra superior de CODAP o selecciona alguno en la parte inferior al dataset.
2. Si el gráfico muestra `State` en el eje horizontal, **consérvalo**: será nuestra variable de agrupación geográfica.
3. Haz clic en el nombre o la flecha del **eje vertical** y elige **Roller Coasters → Top_Speed** (o `Max_Height` si resulta más fácil de visualizar).
4. Observa los puntos de distintos estados. **Cada punto representa un registro, no el riesgo del estado ni necesariamente un promedio.**
5. Identifica un estado con varios registros visibles y otro con menos registros visibles. Puedes desplazarte por el gráfico si es necesario.
6. Selecciona un punto del gráfico y localiza el registro correspondiente en la tabla, si la interfaz lo permite.

**Responde:**

- ¿Qué estado elegiste para observar con más detalle?
- ¿Qué característica técnica revisaste (`Top_Speed` o `Max_Height`)?
- ¿El gráfico muestra cantidad de instalaciones, una característica de cada instalación o ambas cosas? Explica con cuidado qué representa cada punto.

**Resultado esperado:** una visualización explorada y una observación respaldada por datos visibles.

> **Si no logras colocar una variable en el eje vertical:** conserva el gráfico por `State`, examina la tabla y compara registros de dos estados. La misión no depende de una configuración exacta del gráfico.

## Desafío 3. Desmonta una conclusión apresurada (4 minutos)

Vuelve a leer la afirmación inicial:

> «El estado que tenga más instalaciones registradas debe ser el primero en recibir una inspección, porque seguramente presenta mayor riesgo».

Decide si estás de acuerdo, parcialmente de acuerdo o en desacuerdo. Justifica tu postura respondiendo:

1. ¿Tener más registros demuestra mayor riesgo? **No: una cantidad no es una medición de riesgo.**
2. ¿Qué información adicional necesitarías para decidir una prioridad de inspección? Elige al menos dos: historial de incidentes, fecha de última inspección, estado de conservación, intensidad de uso, mantenimiento, resultados de inspecciones anteriores.
3. ¿Cómo utilizarías la tabla y el gráfico para preparar una revisión preliminar sin afirmar que una instalación es insegura?

**Resultado esperado:** identificar la diferencia entre un inventario descriptivo y una evaluación de riesgo.

## Desafío 4. Emite tu recomendación (3 minutos)

Completa esta ficha breve en el chat de la sesión o en un documento de texto:

```text
DICTAMEN DE EXPLORACIÓN

1. Estado o registros examinados:
2. Atributo técnico analizado:
3. Observación respaldada por el gráfico o la tabla:
4. ¿La cantidad de registros demuestra riesgo? ¿Por qué?:
5. Dos datos adicionales que solicitaría antes de priorizar inspecciones:
6. Una pregunta que podría investigarse con aprendizaje automático:
```

**Ejemplo de pregunta futura de ML:** «Si tuviéramos historiales de mantenimiento, uso e incidentes, ¿podríamos estimar qué instalaciones necesitarán revisión antes?». Esto sería una **propuesta de aplicación**, no un modelo entrenado durante la práctica.

---

## Entregable

Una **ficha de dictamen** de seis respuestas breves. No se necesita Excel, CSV ni cuenta de usuario.

## Criterios de validación

| Criterio | Evidencia esperada |
|---|---|
| Accede al entorno | Abre `Roller Coasters` desde los documentos de ejemplo |
| Explora información | Reconoce `States`, `Roller Coasters` y al menos un atributo técnico |
| Interpreta el gráfico | Describe lo que representan los puntos sin confundirlos con riesgo |
| Evalúa una afirmación | Rechaza inferir riesgo únicamente por cantidad de registros |
| Propone un uso de ML | Formula una pregunta predictiva y menciona datos que harían falta |

## Solución de problemas

- **No aparece la ventana Open:** utiliza el menú **File** para abrir un documento de ejemplo.
- **No encuentro Roller Coasters:** confirma que seleccionaste **Documentos de ejemplo** y no **Local File** ni **Google Drive**.
- **El gráfico solo muestra `State`:** es válido como punto de partida. Selecciona el eje vertical y busca un atributo dentro de **Roller Coasters**. Si no funciona, utiliza la tabla como apoyo.
- **No puedo guardar el proyecto:** la ficha de dictamen es suficiente como entregable.
- **La interfaz aparece en inglés:** puedes mantener los nombres de los atributos en inglés; las respuestas y el dictamen se redactan en español.


 CODAP permite explorar datos sin programación y no se entrena ningún modelo en este laboratorio. 

---

[⬅ Anterior: Práctica 6](../Capitulo06/README.md) | [Inicio](../README.md)

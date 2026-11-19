# Práctica 3. Visión artificial con IA multimodal

## Operación Inspección Visual: ¿qué detectó la IA y qué pasó por alto?

**Taller práctico: Aplicación de la Inteligencia Artificial Moderna · Práctica 3 de 7**

- **Duración:** 20 minutos.
- **Nivel:** básico.
- **Público:** personal militar, personal civil y personal de entidades adscritas al Sector Defensa de Perú.
- **Herramientas:** ChatGPT con capacidad para analizar imágenes o Microsoft Copilot con esa capacidad; [Google Cloud Vision, demostración](https://cloud.google.com/vision/docs/drag-and-drop) cuando esté accesible.
- **Entregable:** un dictamen breve de inspección, en texto, con los datos verificados y las limitaciones observadas.

> **IMPORTANTE:** el caso, las imágenes y los datos son ficticios. No cargar imágenes, documentos, planos ni información institucional real. La IA no sustituye la inspección física ni la validación de un responsable.

## Descripción

Un centro logístico ficticio recibe suministros para apoyar una respuesta humanitaria. La documentación indica que algunos materiales necesitan revisión. Al mismo tiempo, el personal debe comprender la distribución general del centro. **Tu misión es analizar dos evidencias visuales, detectar una diferencia entre cantidades, reconocer la señalización visible y verificar qué interpretó correctamente la IA.**

Esta práctica es independiente de las anteriores. No requiere continuar una conversación ni reutilizar sus archivos.

## Objetivos de aprendizaje

Al finalizar, podrás:

1. Utilizar una IA multimodal para describir imágenes y reconocer elementos visibles.
2. Extraer y comprobar texto de una imagen mediante OCR.
3. Distinguir entre información observable, inferencias y afirmaciones sin evidencia.
4. Comparar la interpretación de una IA generativa con un servicio especializado de visión artificial, cuando esté disponible.

## Alcance

Interpretación de imágenes, identificación de objetos o elementos, OCR y evaluación crítica de los resultados. No se realiza reconocimiento facial, vigilancia, inspección de instalaciones reales ni evaluación de seguridad operacional.

## Archivos necesarios

| Archivo | Para qué sirve |
|---|---|
| [`Acta_Recepcion.png`](recursos/Acta_Recepcion.png) | Documento ficticio para extracción de texto y verificación de cantidades. |
| [`Plano_Centro_Logistico.png`](recursos/Plano_Centro_Logistico.png) | Plano ficticio para identificación de zonas y señalización. |
| [`Ficha_Dictamen.md`](recursos/Ficha_Dictamen.md) | Plantilla opcional de entrega, sin Excel. |

**Antes de comenzar:** descarga ambas imágenes. Comprueba que puedes adjuntar imágenes a ChatGPT o Copilot. Si tu versión no permite adjuntarlas, utiliza la alternativa descrita en *Plan de contingencia*.

---

## Tarea 1. Inspección inicial: ¿qué te llama la atención? (4 minutos)

**Paso 1.** Abre `Acta_Recepcion.png` y examina la tabla de suministros. Sin consultar IA, identifica el producto cuya cantidad declarada es distinta de la cantidad contada.

**Paso 2.** Abre `Plano_Centro_Logistico.png`. Localiza visualmente la zona de revisión, la salida señalizada y el área con acceso restringido.

**Paso 3.** Formula dos hipótesis: **¿qué información podría extraer una IA de estas imágenes?** y **¿qué no debería afirmar sin más evidencia?**

**Resultado esperado:** una discrepancia detectada por observación propia y una primera distinción entre datos visibles e inferencias.

---

## Tarea 2. Investiga con IA multimodal y OCR (11 minutos)

### Desafío A. El acta de recepción (5 minutos)

**Paso 1.** Abre una conversación nueva en ChatGPT o Copilot y adjunta `Acta_Recepcion.png`.

**Paso 2.** Envía este prompt:

```text
Actúa como asistente de revisión documental de un centro logístico ficticio.
Analiza exclusivamente la imagen adjunta.

1. Extrae el número de acta, la fecha y el estado del documento.
2. Construye una tabla con código, suministro, cantidad declarada y cantidad contada.
3. Identifica cualquier diferencia numérica y calcula su magnitud.
4. Resume las observaciones que aparecen en el documento.
5. Separa claramente lo que se lee en la imagen de tus interpretaciones.

Si un dato no es legible o no aparece, escribe "No verificable".
No inventes información ni declares que los materiales fueron aceptados.
```

**Paso 3.** Contrasta la respuesta con la imagen original. En particular, verifica **código, cantidades y observaciones**. Corrige cualquier lectura equivocada.

**Resultado esperado:** tabla extraída, identificación de la discrepancia y observación relevante, con verificación visual.

### Desafío B. El plano que parece decir más de lo que muestra (4 minutos)

**Paso 4.** En la misma conversación adjunta `Plano_Centro_Logistico.png` y escribe:

```text
Examina el plano ficticio adjunto.
1. Enumera las zonas que puedes leer directamente.
2. Identifica la señalización visible de salida, extintor y acceso restringido.
3. Indica si aparece dibujada una ruta completa de evacuación.
4. Distingue entre texto o símbolos visibles y conclusiones que no puedes verificar.

No inventes recorridos, distancias, puertas adicionales ni condiciones reales de seguridad.
```

**Paso 5.** Comprueba las afirmaciones sobre la ruta de evacuación. El hecho de que exista una señal de salida **no significa** que el plano muestre una ruta completa.

**Resultado esperado:** descripción de zonas y señales visibles sin inventar una ruta de evacuación.

### Desafío C. Contrasta con una herramienta especializada (2 minutos)

**Paso 6.** Si la [demostración de Google Cloud Vision](https://cloud.google.com/vision/docs/drag-and-drop) está disponible sin configuración adicional, abre el sitio, carga **solo** `Acta_Recepcion.png` y revisa el resultado de **detección de texto**. Compara al menos **el número de acta y las cantidades del producto con discrepancia** con los datos originales y la respuesta de ChatGPT o Copilot.

**Si el sitio exige acceso, configuración, facturación o no responde**, no crees recursos de nube ni introduzcas una tarjeta. Continúa con la alternativa: vuelve a la imagen y realiza una segunda lectura manual de esos mismos campos; documenta que no se pudo ejecutar la comparación especializada.

**Resultado esperado:** comparación puntual de OCR entre herramientas, o registro explícito de la limitación de acceso.

---

## Tarea 3. Dictamen de inspección: ¿qué puede asegurarse? (5 minutos)

**Paso 1.** Escribe una respuesta de **cinco líneas como máximo** que incluya:

1. Identificación del acta.
2. Producto y diferencia detectada.
3. Observación relevante del documento.
4. Dos elementos de seguridad o señalización visibles en el plano.
5. Una afirmación que **no** se puede verificar solo con las imágenes.

Puedes utilizar [`Ficha_Dictamen.md`](recursos/Ficha_Dictamen.md) o escribir el dictamen directamente en tu conversación.

**Paso 2.** Comprueba tu dictamen con las dos imágenes originales. No aceptes como hechos datos que la IA haya inferido sin evidencia.

**Paso 3.** Responde oralmente o por escrito: **¿en qué fue más útil la IA: leer el acta, describir el plano o verificar una decisión? ¿Dónde fue indispensable la revisión humana?**

**Resultado esperado:** un dictamen breve, verificable y prudente, sustentado en evidencias visuales.

---

## Validación

| Comprobación | Resultado correcto |
|---|---|
| OCR del acta | `AR-2026-0417`, fecha `18/11/2026`. |
| Discrepancia | Kits de higiene `HK-02`: 24 declarados, 22 contados, **diferencia de 2 unidades**. |
| Observación | Dos kits con empaque dañado, separados para revisión. |
| Plano | Zona de revisión, acceso restringido, extintor y salida señalizada visibles. |
| Límite de la interpretación | **No** aparece una ruta de evacuación trazada; no se debe inventar. |

## Entregable

Un **dictamen de inspección visual** de hasta cinco líneas, con datos extraídos, diferencia detectada, señales visibles y una limitación de interpretación. **No es necesario completar un Excel.**

## Plan de contingencia

- **ChatGPT o Copilot no permite adjuntar imágenes:** el instructor puede proyectar las dos imágenes y realizar una demostración guiada desde una cuenta con acceso multimodal. Los participantes verifican la extracción y preparan su propio dictamen. Registrar que no se ejecutó el análisis individual.
- **Google Vision no está disponible:** continuar con la verificación manual; no afirmar que se compararon dos motores de OCR.
- **La IA lee mal una cantidad:** acercar la imagen o repetir la consulta señalando el renglón; prevalece la lectura del documento original.
- **La IA inventa una ruta de evacuación:** solicitar que indique la evidencia exacta en la imagen; si no existe, marcar la afirmación como no verificable.
- **Se agota el tiempo:** priorizar la extracción del acta, la discrepancia y la advertencia sobre el plano; la comparación especializada es secundaria.

## Preguntas de reflexión

1. ¿Por qué una respuesta de IA visualmente convincente puede ser incorrecta?
2. ¿Qué diferencia hay entre extraer texto con OCR e interpretar su significado?
3. ¿Por qué no deberíamos tomar decisiones de seguridad basadas solo en un plano simplificado y una respuesta generativa?

---

[⬅ Anterior: Práctica 2](../Capitulo02/README.md) | [Inicio](../README.md) | [Siguiente: Práctica 4 ➡](../Capitulo04/README.md)

# Práctica 1. Selección de tipo de IA según el problema

**Taller práctico: Aplicación de la Inteligencia Artificial Moderna · Práctica 1 de 7**

⏱️ **Duración:** 15 minutos · 🛠️ **Herramienta:** ChatGPT o Microsoft Copilot (web, con carga de imágenes habilitada) · 🎯 **Nivel:** básico · 📄 **Entregable:** ficha breve de decisión (archivo .txt o word)

## Descripción

### Operación Ayuda Humanitaria: tres fuentes, tres decisiones

Tras lluvias intensas en una región ficticia de Perú, un centro interinstitucional de apoyo humanitario debe preparar suministros para comunidades afectadas. El equipo recibe **un mensaje con solicitudes**, **una imagen esquemática del almacén** y **un historial de entregas**. Tu misión no es decidir rutas reales ni autorizar distribuciones: es reconocer **qué tecnología de IA** ayudaría a procesar cada fuente y **comprobar qué puede y qué no puede concluirse**.

> **Simulación didáctica.** Todos los nombres, cantidades y circunstancias son inventados. No utilizar información operativa real, documentos restringidos ni datos personales. Los resultados de la IA requieren verificación humana.

## Objetivo de aprendizaje

Analizar tres problemas simulados (texto, imagen y predicción), **seleccionar y justificar** el enfoque más adecuado —procesamiento de lenguaje natural (NLP), visión artificial o aprendizaje automático predictivo (ML)— y contrastar la elección con ChatGPT o Microsoft Copilot.

## Alcance

- Clasificación de problemas: texto, imagen y predicción.
- Relación problema → tipo de IA: NLP, visión artificial y ML predictivo.
- Identificación y justificación del enfoque adecuado, sus datos de entrada y sus limitaciones.
- Contraste de decisiones con IA generativa. **No se entrena ni se valida un modelo predictivo** en esta práctica.

## Público objetivo

Personal militar, personal civil y personal de entidades adscritas al Sector Defensa de Perú, de áreas administrativas, logísticas, de salud, mantenimiento, capacitación o tecnología. No se requieren conocimientos militares especializados ni programación.

## Antes de empezar

| Elemento | Requisito |
|---|---|
| Equipo | Laptop, navegador actualizado, conexión a internet |
| IA generativa | ChatGPT o Copilot con posibilidad de adjuntar una captura de pantalla; si no está disponible, usar la alternativa indicada |
| Archivos | [`Mensaje_Solicitudes.txt`](recursos/Mensaje_Solicitudes.txt), [`Almacen_Visual.html`](recursos/Almacen_Visual.html), [`Historial_Entregas.csv`](recursos/Historial_Entregas.csv) |
| Preparación | Descargar los tres archivos y abrir `Almacen_Visual.html` en el navegador |
| Entregable | Respuesta final en cuatro líneas: fuente, tipo de IA, justificación y limitación |

---

## Tarea 1. Reconocer el desafío (4 minutos)

**Paso 1.** Lee [`Mensaje_Solicitudes.txt`](recursos/Mensaje_Solicitudes.txt). Identifica qué se solicita y qué información aparece.

**Paso 2.** Abre [`Almacen_Visual.html`](recursos/Almacen_Visual.html) en el navegador. Observa los rótulos de las cajas y toma una captura del panel **«Vista simulada del almacén»**. No necesitas fotografiar instalaciones reales.

**Paso 3.** Abre [`Historial_Entregas.csv`](recursos/Historial_Entregas.csv) con una hoja de cálculo o un editor de texto. Observa que muestra entregas semanales pasadas, **no necesidades futuras confirmadas**.

**Paso 4.** Antes de consultar la IA, decide qué enfoque utilizarías en cada tarea:

- **A:** convertir las solicitudes redactadas en un resumen estructurado.
- **B:** identificar y contar cajas por categoría a partir de una imagen.
- **C:** estimar demanda futura a partir de datos históricos, si fueran suficientes y pertinentes.


Anota en un borrador (un .txt o un archivo de word): **NLP, ML predictivo o visión artificial** para A, B o C, con una justificación breve.

**Resultado de la tarea:** tres elecciones preliminares basadas en el tipo de información y el resultado buscado.

## Tarea 2. Investigar con IA y contrastar (7 minutos)

### Paso 1. Procesar las solicitudes (2 minutos)

Copia el contenido de `Mensaje_Solicitudes.txt` en ChatGPT o Copilot y envía:

```text
Actúa como asistente de análisis documental en una simulación de apoyo humanitario.
Extrae únicamente información de lo que dice el mensaje. Devuelve una tabla con:
comunidad | suministro | cantidad solicitada | observación.
Si una cantidad no aparece, escribe «No especificada».
No inventes información ni decidas prioridades de distribución.
Al final indica qué tipo de IA se utiliza principalmente para interpretar este texto y por qué.

MENSAJE:
[PEGA AQUÍ EL CONTENIDO DEL ARCHIVO]
```

Compara el resultado con el mensaje original. **La IA no debe completar cantidades ausentes**.

### Paso 2. Interpretar el esquema visual (2 minutos)

Adjunta la captura de `Almacen_Visual.html` y envía:

```text
Analiza exclusivamente esta imagen esquemática ficticia de un almacén.
Cuenta las cajas visibles de cada categoría según sus rótulos:
AGUA, HIGIENE y MANTAS.
Responde en una tabla: categoría | número de cajas visibles.
Distingue entre «cajas visibles» y «unidades disponibles»:
no supongas cuántas unidades contiene cada caja.
¿Qué tipo de IA corresponde al análisis de imágenes y por qué?
```

**Importante:** los conteos visuales son de **cajas**, mientras que el mensaje y el CSV usan **unidades o kits**. No compares directamente esas cantidades.

**Si tu cuenta no permite adjuntar imágenes:** observa el esquema y registra manualmente el número de cajas. Luego consulta a la IA **qué tecnología sería apropiada para automatizar esa lectura**. Señala que no se realizó análisis visual por IA.

### Paso 3. Examinar el historial y elegir tecnología (3 minutos)

Adjunta o pega el contenido de `Historial_Entregas.csv` y envía:

```text
Este CSV contiene seis semanas ficticias de entregas de suministros.
No quiero que presentes una predicción como si fuera confiable.
1. Identifica qué columnas son históricas y cuál sería la variable a estimar.
2. Explica qué tipo de IA sería apropiado para pronosticar demanda futura.
3. Dime qué información adicional se necesitaría para construir y evaluar
   un modelo predictivo útil.
4. Distingue claramente entregas pasadas de demanda real.
Responde brevemente. No inventes datos futuros.

CSV:
[PEGA AQUÍ EL ARCHIVO O EL CONTENIDO DEL ARCHIVO]
```

**Resultado de la tarea:** contraste entre tus tres decisiones y las explicaciones de la IA, incluyendo una limitación importante por fuente.

## Tarea 3. Emitir una recomendación (4 minutos)

**Paso 1.** Copia y completa esta ficha en tu documento de texto (.txt o word):

```text
RECOMENDACIÓN DE TECNOLOGÍAS — OPERACIÓN AYUDA HUMANITARIA
A. Solicitudes escritas → [TIPO DE IA]. Porque [JUSTIFICACIÓN].
B. Esquema del almacén → [TIPO DE IA]. Porque [JUSTIFICACIÓN].
C. Historial de entregas → [TIPO DE IA]. Porque [JUSTIFICACIÓN].
Limitación crítica: [ALGO QUE NO PUEDE CONCLUIRSE CON LOS DATOS].
```

**Paso 2.** Envía a ChatGPT o Copilot:

```text
Revisa mi siguiente recomendación. Para cada apartado A, B y C,
indica si el tipo de IA elegido es apropiado, explica brevemente por qué
y señala cualquier confusión entre analizar texto, interpretar imágenes
y construir una predicción basada en datos históricos.
No me des la razón automáticamente. No inventes resultados.

[PEGA AQUÍ TU RECOMENDACIÓN COMPLETA]
```

**Paso 3.** Ajusta tu ficha si corresponde. Guarda el texto final como `Decision_IA_[INICIALES].md` y conserva la conversación.

**Resultado de la tarea:** una recomendación verificable que vincula tres problemas con NLP, visión artificial y ML predictivo.

---

## Validación y criterios de éxito

| Criterio | Evidencia esperada |
|---|---|
| Clasificación | A = NLP; B = visión artificial; C = ML predictivo |
| Justificación | Se menciona el dato de entrada y la tarea que se quiere resolver |
| Contraste con IA | Se identifica al menos una corrección, confirmación razonada o limitación |
| Pensamiento crítico | No confunde cajas visibles con unidades, ni entregas históricas con demanda futura |
| Uso responsable | No se utilizan datos reales ni se toman decisiones operativas basadas solo en IA |


## Resultado esperado

Al finalizar, cada participante habrá experimentado con la organización de solicitudes en lenguaje natural, el análisis de una representación visual y la interpretación de datos históricos como insumo potencial para un pronóstico. Podrá distinguir el enfoque principal de IA apropiado para cada tarea y justificarlo con base en la información disponible. Además, reconocerá que una respuesta generada por IA no sustituye la verificación de datos ni constituye por sí misma una predicción confiable o una decisión logística autorizada.

## Solución de problemas

- **No puedo cargar imágenes en ChatGPT o Copilot:** usa la alternativa manual del Paso 2 y conserva la selección de visión artificial como enfoque recomendado.
- **La IA inventa cantidades faltantes:** solicita que indique «No especificada» y vuelve a contrastar con el archivo original.
- **La IA afirma que ya predijo la demanda:** aclara que solo hay seis observaciones históricas de entregas y pide requisitos para un modelo validado; no presentes una cifra como pronóstico operativo.
- **La IA compara cajas con kits:** recuérdale que no se conoce el contenido por caja y que son magnitudes diferentes.
- **No abre el HTML:** guarda el archivo en el equipo y ábrelo con Chrome o Edge; no necesita conexión para mostrar el esquema.

## Limpieza

Conserva únicamente tu ficha de decisión y los recursos ficticios. No subas fotografías ni documentación institucional real.

---

[Inicio](../README.md) | [Siguiente: Práctica 2](../Capitulo02/README.md)

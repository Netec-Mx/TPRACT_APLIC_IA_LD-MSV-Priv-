# Práctica 4. Aprendizaje automático interactivo

## Misión Abastecimiento: entrena una IA para reconocer suministros

**Taller práctico: Aplicación de la Inteligencia Artificial Moderna · Práctica 4 de 7**

- **Duración:** 20 minutos.
- **Nivel:** básico; no requiere programación.
- **Público:** personal militar, personal civil y personal de entidades adscritas al Sector Defensa de Perú.
- **Herramienta:** [Google Teachable Machine](https://teachablemachine.withgoogle.com/) (proyecto de imágenes).
- **Entregable:** una **ficha de resultados** breve con el desempeño del clasificador y una conclusión sobre sesgo; no se requiere Excel.

> **Simulación:** las imágenes son ilustraciones sintéticas de suministros ficticios. No representan productos reales ni deben utilizarse para inventarios, seguridad o decisiones operativas. No cargues fotografías institucionales ni datos reales.

## Situación

Un centro ficticio de abastecimiento humanitario desea explorar si una IA podría reconocer, a partir de imágenes, tres categorías de suministros: **agua**, **botiquín** y **manta**. Tu misión es entrenar un clasificador sin código, probarlo con imágenes desconocidas y descubrir si un segundo modelo confunde **color** con **categoría**.

El modelo es una demostración educativa: **no** verifica cantidades, estado físico, contenido ni calidad de suministros.

## Objetivos de aprendizaje

Al finalizar podrás:

1. Crear tres clases y entrenar un modelo de clasificación de imágenes en Teachable Machine.
2. Probarlo con imágenes que no formaron parte del entrenamiento y registrar aciertos y errores.
3. Reconocer cómo un conjunto de entrenamiento con colores asociados a cada clase puede generar una dependencia no deseada.
4. Proponer una mejora a los datos de entrenamiento y explicar por qué la predicción de un modelo debe verificarse.

## Archivos necesarios

| Archivo | Uso |
|---|---|
| [`Dataset_Suministros.zip`](recursos/Dataset_Suministros.zip) | Imágenes listas para entrenar y probar los modelos. |
| [`Ficha_Resultados.md`](recursos/Ficha_Resultados.md) | Plantilla breve para registrar resultados y conclusiones. |

El ZIP contiene **75 imágenes de entrenamiento y prueba** y 3 imágenes de ejemplo: `entrenamiento/` (12 imágenes por clase, 36 en total), `prueba/` (3 por clase, 9 en total), `sesgo_entrenamiento/` (9 por clase, 27 en total), `sesgo_prueba/` (3 con colores intercambiados) y `ejemplos/` (3). **Nunca cargues imágenes de `prueba/` o `sesgo_prueba/` como entrenamiento.**

### Antes de iniciar

1. Descarga y **extrae** `Dataset_Suministros.zip` en tu equipo. Identifica la carpeta `dataset`.
2. Abre [Teachable Machine](https://teachablemachine.withgoogle.com/) en Chrome o Edge actualizado. Comprueba que puedes abrir **Primeros pasos → Proyecto de imagen → Modelo de imagen estándar** (los nombres pueden variar ligeramente).
3. Mantén las imágenes de prueba separadas de las de entrenamiento. Trabaja solo con archivos ficticios proporcionados.

---

## Tarea 1. Preparar la misión (3 minutos)

**Paso 1.** Abre Teachable Machine y selecciona **Primeros pasos → Proyecto de imagen → Modelo de imagen estándar**.

**Paso 2.** Renombra las clases existentes como `Agua` y `Botiquin`. Pulsa **Añadir una clase** y nómbrala `Manta`.

**Paso 3.** Examina una imagen de cada carpeta de `dataset/ejemplos/`. ¿Qué características de **forma** distinguen los tres suministros? Los colores pueden cambiar.

**Resultado esperado:** proyecto con tres clases correctamente nombradas y una hipótesis inicial sobre los rasgos visuales que permiten distinguirlas.

## Tarea 2. Entrenar el clasificador (7 minutos)

**Paso 1.** En `Agua`, selecciona **Subir → Selecciona imágenes de tus archivos o arrástralas aquí** y carga las 12 imágenes de `dataset/entrenamiento/Agua/`.

**Paso 2.** Repite con las 12 imágenes de `Botiquin` y las 12 de `Manta` desde sus carpetas respectivas. Confirma que cada clase tenga **12 ejemplos**.

**Paso 3.** Pulsa **Preparar modelo**. Espera a que aparezca **Exportar modelo**; evita cerrar o cambiar la pestaña mientras entrena.

**Paso 4.** En **Entrada**, cambia la fuente de entrada de cámara a **Archivo**, y carga una imagen de `dataset/prueba/Agua/`.

**Resultado esperado:** un modelo entrenado con 36 imágenes y al menos una predicción visible con puntuaciones por clase. Estas puntuaciones no son garantías de exactitud ni de seguridad.

## Tarea 3. ¿Reconoce lo que nunca vio? (5 minutos)

**Paso 1.** Prueba **una imagen de cada clase** de `dataset/prueba/` (3 pruebas rápidas). Anota la clase real, la predicción y si acertó.

**Paso 2.** Si te alcanza el tiempo, prueba las **9 imágenes** disponibles. Calcula: `exactitud = aciertos / imágenes probadas × 100`. Anota siempre cuántas probaste; no compares 3/3 con 9/9 como si fueran evaluaciones equivalentes.

**Paso 3.** Identifica si algún error podría explicarse por diferencias de color, tamaño, posición o forma. No inventes causas: plantea hipótesis.

**Resultado esperado:** mínimo tres predicciones registradas, un porcentaje calculado sobre las pruebas efectivamente realizadas y una observación sobre errores o incertidumbre.

## Tarea 4. El engaño del color (5 minutos)

**Paso 1.** Abre una **segunda pestaña** de Teachable Machine. Crea otro proyecto de imágenes con las clases `Agua`, `Botiquin` y `Manta`.

**Paso 2.** Carga las 9 imágenes de cada clase desde `dataset/sesgo_entrenamiento/`: **agua azul, botiquines rojos y mantas verdes**. Entrena el segundo modelo.

**Paso 3.** En el segundo modelo, prueba `dataset/sesgo_prueba/agua_color_cambiado.png` (agua roja). Observa qué predice. Si hay tiempo, prueba también `botiquin_color_cambiado.png` y `manta_color_cambiado.png`.

**Paso 4.** Vuelve al **primer modelo** y prueba exactamente la misma imagen de agua roja. Compara las dos predicciones.

**Paso 5.** Completa la ficha: ¿cuál modelo parece depender más del color? ¿Cómo mejorarías el entrenamiento? **No afirmes que hubo sesgo solo porque los colores estaban asociados: describe lo que efectivamente observaste.**

**Resultado esperado:** dos modelos entrenados, comparación de al menos una imagen con color cambiado y una recomendación fundamentada para diversificar los ejemplos.

---

## Entregable: ficha de resultados

Completa [`Ficha_Resultados.md`](recursos/Ficha_Resultados.md) con:

- Número de imágenes por clase en el primer modelo.
- Resultados de al menos 3 imágenes no vistas y exactitud correspondiente.
- Predicciones de los dos modelos para al menos una imagen de color cambiado.
- Una conclusión sobre calidad de datos y una propuesta de mejora.

No es necesario compartir un enlace público del modelo, exportarlo ni cargar datos institucionales.

## Validación

| Comprobación | Criterio |
|---|---|
| Entrenamiento | Tres clases con 12 imágenes cada una en el primer modelo. |
| Evaluación | Al menos una prueba nueva por clase; porcentaje calculado correctamente. |
| Sesgo | Comparación de una misma imagen en ambos modelos. |
| Reflexión | Identifica una limitación y una mejora posible de los datos. |

**Importante:** no se exige un porcentaje mínimo de aciertos ni se garantiza que el segundo modelo falle. Los resultados dependen del entrenamiento, la inicialización y las imágenes. El objetivo es **observar y explicar**, no obtener una predicción predeterminada.

## Si algo falla

- **No aparece el botón de carga:** comprueba que creaste un **Image Project** y selecciona **Upload**, no Webcam.
- **Entrenamiento lento o detenido:** espera, mantén la pestaña activa y cierra otras aplicaciones pesadas. No recargues sin necesidad.
- **No alcanza el tiempo para las 9 pruebas:** registra 3, una por clase. El resto es ampliación opcional.
- **El segundo modelo no confunde colores:** también es un resultado válido. Explica que la correlación de colores es un **riesgo de aprendizaje de atajos**, no un error garantizado.
- **La plataforma no funciona:** el instructor puede mostrar una demostración previamente preparada. En ese caso, anota que observaste el entrenamiento, pero **no** declares que entrenaste el modelo personalmente.

## Para reflexionar

En una operación real, ¿qué consecuencias tendría que un modelo confundiera dos suministros por su color o presentación? ¿Qué verificación humana necesitarías antes de utilizar sus resultados?

---

[⬅ Anterior: Práctica 3](../Capitulo03/README.md) | [Inicio](../README.md) | [Siguiente: Práctica 5 ➡](../Capitulo05/README.md)
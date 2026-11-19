# Práctica 5. Simulación de aprendizaje profundo

## Misión Rescate del Modelo: una IA que no consigue aprender

**Taller práctico: Aplicación de la Inteligencia Artificial Moderna · Práctica 5 de 7**  
**Duración:** 20 minutos  
**Herramienta:** [TensorFlow Playground](https://playground.tensorflow.org/)  
**Nivel:** básico  
**Modalidad:** individual, guiada, sin programación  
**Entregable:** ficha breve de diagnóstico y rescate del modelo.

## Contexto de la misión

Un centro ficticio de análisis y capacitación del Sector Defensa de Perú está evaluando redes neuronales con datos sintéticos. El primer modelo separa correctamente dos grupos de puntos, pero al enfrentar patrones circulares y más complejos deja de funcionar. Tu misión es **diagnosticar el problema, modificar la red y comprobar qué cambió**.

> Todos los puntos y etiquetas son simulados. No corresponden a personas, unidades, instalaciones ni operaciones reales. La práctica es una demostración conceptual, no un sistema de toma de decisiones.

## Objetivo

Experimentar con una red neuronal en TensorFlow Playground para observar cómo las **capas ocultas**, el **número de neuronas**, las **características de entrada** y la **tasa de aprendizaje** afectan el entrenamiento y la capacidad de clasificación de patrones.

## Resultados esperados

Al terminar podrás:

1. Identificar entradas, capas ocultas, neuronas, conexiones y salida de una red neuronal.
2. Distinguir un problema separable mediante una frontera recta de uno que requiere una frontera curva.
3. Mejorar un modelo cambiando su arquitectura o sus características.
4. Explicar por qué una tasa de aprendizaje demasiado alta o baja puede dificultar el entrenamiento.
5. Comparar la pérdida de entrenamiento (*training loss*) y de prueba (*test loss*) sin confundirlas con el porcentaje de aciertos.

## Antes de empezar

- Utiliza un navegador actualizado y abre <https://playground.tensorflow.org/>.
- No necesitas cuenta, instalar software ni programar.
- Abre también [`recursos/Ficha_Rescate.md`](recursos/Ficha_Rescate.md) para registrar cuatro observaciones breves.
- Trabaja con **Tipo de problema:Clasificación**, no Regresión.
- Si el sitio conserva cambios de una sesión anterior, **Refresca la página** y verifica cada parámetro indicado.
- **Importante:** los valores de pérdida y las fronteras pueden variar entre ejecuciones. No se exige una cifra exacta ni un número fijo de épocas.

## Guía rápida de la interfaz

- **DATA:** elige el conjunto de puntos (*Gaussian*, *Circle*, *Spiral*).
- **FEATURES:** selecciona las entradas, por ejemplo `x1` y `x2`.
- **HIDDEN LAYERS:** agrega o quita capas y neuronas con los controles `+` y `−`.
- **Learning rate:** modifica cuánto cambian los pesos en cada actualización.
- **Play / Pause / Reset:** inicia, detiene o reinicia el entrenamiento.
- **OUTPUT:** observa la frontera de clasificación y las métricas *training loss* y *test loss*.

> **Interpretación:** una pérdida menor suele indicar mejor ajuste respecto a esa métrica, pero **no es un porcentaje de precisión**. Para comparar dos configuraciones, usa el mismo conjunto de datos y observa también la frontera y la pérdida de prueba.

---

## Desafío 1. Diagnóstico: ¿por qué falla? (4 minutos)

### Experimento A: el problema sencillo

1. Selecciona **Gaussian** en DATA.
2. Deja activadas solamente las entradas **x1** y **x2**.
3. Elimina las capas ocultas, hasta tener **0 hidden layers**.
4. Establece **Learning rate = 0.03**. Conserva los demás parámetros predeterminados de clasificación.
5. Pulsa **Reset** y luego **Play**. Observa durante unos segundos y pausa cuando la frontera deje de cambiar apreciablemente.
6. Anota si la frontera es aproximadamente recta y si logra separar los grupos.

### Experimento B: el mismo modelo ante un círculo

1. Cambia solamente el conjunto de datos a **Circle**.
2. Reinicia el entrenamiento y vuelve a observar.
3. Compara la frontera con la del experimento A.

**Pregunta de diagnóstico:** ¿qué limitación tiene una red sin capas ocultas cuando debe separar puntos dentro y fuera de un círculo?

**Resultado esperado:** reconocer que una frontera lineal puede separar los grupos del ejemplo sencillo, pero no representar adecuadamente una frontera circular con solo `x1` y `x2`.

## Desafío 2. Rescate: modifica la arquitectura (8 minutos)

### Experimento C: añadir capacidad al modelo

1. Mantén **Circle**, `x1`, `x2` y **Learning rate = 0.03**.
2. Agrega **1 capa oculta con 4 neuronas**.
3. Pulsa **Reset** y **Play**. Espera hasta observar si aparece una frontera curva; si tarda, permite más épocas.
4. Registra si la separación mejora respecto al experimento B y qué sucede con la *test loss*.
5. Si la frontera todavía no mejora claramente, aumenta la capa a **6 u 8 neuronas**, reinicia y observa. Registra que fue necesario ajustar la capacidad.

### Experimento D: el desafío de la espiral

1. Cambia el conjunto de datos a **Spiral** y conserva inicialmente la red del experimento C.
2. Reinicia y observa brevemente: ¿puede seguir las dos espirales?
3. Agrega capacidad: prueba **3 capas ocultas** con **8, 8 y 4 neuronas**, si los controles de tu interfaz lo permiten.
4. Activa las entradas `x1`, `x2`, `x1²`, `x2²`, `sin(x1)` y `sin(x2)` cuando estén disponibles.
5. Reinicia y observa el entrenamiento. Si no se logra una buena separación en el tiempo disponible, registra la dificultad: **no es obligatorio conseguir una espiral perfecta**.

**Pregunta de rescate:** ¿por qué cambiar la arquitectura o las características de entrada puede ayudar en problemas más complejos?

**Resultado esperado:** observar una mejora posible en Circle y comprender que Spiral es un problema más exigente, cuyo aprendizaje depende de la configuración, las épocas y la inicialización aleatoria.

## Desafío 3. Sabotaje controlado: ¿qué pasa si el modelo aprende mal? (5 minutos)

1. Vuelve a **Circle**, entradas `x1` y `x2`, **1 capa oculta de 4 neuronas**.
2. Establece **Learning rate = 0.03**, reinicia y observa el comportamiento durante un intervalo breve.
3. Cambia **Learning rate = 3**, reinicia y observa si la pérdida oscila, aumenta o el entrenamiento se vuelve inestable. **No se garantiza que ocurra en todas las ejecuciones**.
4. Prueba **Learning rate = 0.0001**, reinicia y observa el avance durante un intervalo similar: ¿aprende más lentamente?
5. Recupera **0.03** y explica cuál configuración fue más útil en tu ejecución.

**Resultado esperado:** distinguir entre una tasa que permite progreso observable, una potencialmente inestable y otra que puede producir cambios demasiado lentos.

## Desafío 4. Informe de rescate (3 minutos)

Completa [`recursos/Ficha_Rescate.md`](recursos/Ficha_Rescate.md) con respuestas breves:

1. ¿Por qué falló el modelo sin capas ocultas con Circle?
2. ¿Qué cambio mejoró el resultado y qué observaste?
3. ¿Qué ocurrió al modificar la tasa de aprendizaje?
4. ¿Por qué no basta con decir que un modelo es bueno porque su pérdida de entrenamiento es baja?

**Producto final:** una ficha breve con el diagnóstico, el ajuste aplicado y una recomendación técnica explicada en lenguaje sencillo.

---

## Criterios de cumplimiento

- Se compararon **Gaussian** y **Circle** con 0 capas ocultas.
- Se probó al menos **una modificación de capas o neuronas**.
- Se exploró **Spiral** como problema más complejo.
- Se compararon al menos **dos tasas de aprendizaje**.
- Se registraron observaciones reales, sin inventar valores ni afirmar resultados no observados.

## Si algo no funciona

| Situación | Qué hacer |
|---|---|
| No ves cambios en la red | Pulsa **Play** y comprueba que no esté pausada. |
| La frontera no mejora con 4 neuronas | Entrena más épocas o prueba 6–8 neuronas; documenta lo observado. |
| La espiral no se separa bien | Es válido; explica que la arquitectura y el tiempo de entrenamiento influyen. |
| Los resultados difieren de los del instructor | Es normal: los pesos se inicializan de manera aleatoria. |
| No encuentras una característica o control | Trabaja con las opciones visibles; informa al instructor y registra la diferencia. |
| El sitio no abre | El instructor puede demostrar los experimentos en pantalla; registra las observaciones compartidas. |

## Cierre

**Idea central:** una red neuronal no aprende correctamente solo por tener más capas. La calidad de su resultado depende del problema, las características de entrada, la arquitectura, los parámetros de entrenamiento y la evaluación sobre datos no utilizados para ajustar el modelo.

---

[⬅ Anterior: Práctica 4](../Capitulo04/README.md) | [Inicio](../README.md) | [Siguiente: Práctica 6 ➡](../Capitulo06/README.md)

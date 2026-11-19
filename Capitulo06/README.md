# Práctica 6. OpenVINO Toolkit

## Misión Inferencia en Acción: de una imagen a una decisión verificable

**Taller práctico: Aplicación de la Inteligencia Artificial Moderna · Práctica 6 de 7**  
**Duración:** 15 minutos  
**Herramienta:** [OpenVINO Notebooks — Hello Image Classification en Google Colab](https://colab.research.google.com/github/openvinotoolkit/openvino_notebooks/blob/latest/notebooks/hello-world/hello-world.ipynb)  
**Modalidad:** individual, guiada, sin programación previa  
**Entregable:** `Dictamen_Inferencia_[INICIALES].md`

> **Contexto:** Una entidad ficticia del Sector Defensa de Perú evalúa si una solución de clasificación visual puede apoyar el inventario de suministros para actividades humanitarias. Antes de recomendarla, debe comprobar que el modelo se ejecuta, qué predice y cuáles son sus límites. No se utilizarán datos, imágenes ni sistemas institucionales reales.

## Objetivo

Ejecutar un notebook oficial de OpenVINO en Google Colab, identificar las etapas de inferencia (preparación, modelo, dispositivo, imagen y predicción), interpretar una clasificación visual y emitir una recomendación fundamentada sobre su utilidad y limitaciones.

## Lo que aprenderás

- Diferenciar **entrenamiento** de **inferencia**: aquí se ejecuta un modelo ya entrenado.
- Reconocer que OpenVINO permite preparar y ejecutar modelos sobre hardware compatible, y que la ejecución en Colab no demuestra por sí sola un despliegue local.
- Interpretar una etiqueta predicha y, si el notebook la muestra, su puntuación; **una puntuación alta no garantiza que la etiqueta sea correcta**.
- Identificar la diferencia entre **clasificar una imagen** y **contar objetos, detectar su ubicación o validar inventarios**.

## Recursos

1. Cuenta de Google con acceso a Colab.
2. Navegador e internet estable.
3. [Notebook oficial Hello Image Classification](https://colab.research.google.com/github/openvinotoolkit/openvino_notebooks/blob/latest/notebooks/hello-world/hello-world.ipynb).
4. `recursos/Dictamen_Inferencia.md` (plantilla editable).
5. `recursos/Tarjeta_Desafio.md` (situación y preguntas de decisión).

**Importante:** el notebook enlazado pertenece a un repositorio externo y puede cambiar. El instructor debe abrirlo y ejecutar todas las celdas antes de la sesión, confirmar que funciona en Colab y disponer de una ejecución de demostración como respaldo. No se garantiza que todas las cuentas puedan acceder o que la instalación concluya dentro de los tiempos indicados.

---

## La misión

Un equipo de abastecimiento necesita determinar si una herramienta que reconoce imágenes podría ayudar a clasificar fotografías de suministros. Tu tarea **no** es construir un sistema de inventario: es ejecutar una inferencia real, comprobar qué resultado devuelve y decidir si ese resultado bastaría para una operación de inventario.

### Desafío 1. Activar el motor de IA (3 minutos)

1. Abre el enlace del notebook oficial. Verifica que el dominio sea `colab.research.google.com` y que el notebook corresponda al repositorio `openvinotoolkit/openvino_notebooks`.
2. Inicia sesión con tu cuenta de Google si es necesario.
3. Da clic en **Archivo > Guardar una copia en Drive** (*File > Save a copy in Drive*). Esto crea tu propia copia editable del notebook.
4. Haz clic en **Conectar**. Si Colab solicita autorización para ejecutar un notebook externo, verifica primero su procedencia; sigue las indicaciones del instructor si existe alguna restricción.
5. Abre `recursos/Dictamen_Inferencia.md` en un editor de texto y prepara tu registro.

**Resultado esperado:** notebook abierto y entorno de ejecución conectado.

### Desafío 2. Ejecutar la inferencia (7 minutos)

1. Selecciona **Ejecutar todas** (*Run all*). 
2. Espera a que terminen las instalaciones y descargas. No modifiques el código del notebook.
3. Identifica visualmente, según los encabezados disponibles, estas etapas: **preparación del entorno**, **descarga/carga del modelo**, **selección del dispositivo**, **preparación de la imagen**, **inferencia** y **presentación del resultado**.
4. Registra en tu dictamen:
   - Modelo utilizado (según la salida real del notebook).
   - Dispositivo de ejecución seleccionado o mostrado (por ejemplo, CPU, si es el caso).
   - Imagen de ejemplo analizada.
   - Etiqueta o clase predicha y puntuación, **solo si aparece**.
5. Si alguna celda falla, copia el nombre de la etapa y una descripción breve del error; no inventes resultados.

**Resultado esperado:** ejecución completada y predicción observada, o incidencia técnica registrada con precisión.

> **Plan de contingencia:** si la instalación o la descarga tarda más de lo previsto, el instructor mostrará una ejecución previa verificada del mismo notebook. El participante analizará esas salidas y marcará su registro como **demostración observada**, no como ejecución propia.

### Desafío 3. ¿Reconocer es lo mismo que verificar? (3 minutos)

Lee `recursos/Tarjeta_Desafio.md` y responde:

1. ¿Qué elemento identificó el modelo en la imagen de ejemplo? ¿Puedes comprobarlo visualmente?
2. Si un almacén tiene 40 cajas en una fotografía, ¿el resultado de **clasificación de una imagen** permite afirmar que hay exactamente 40 cajas? Explica por qué.
3. Para probar otra imagen, ir a https://storage.openvinotoolkit.org/repositories/openvino_notebooks/data/data/image/ , seleccionar una imagen diferente, copiar su URL y reemplazarla en la línea correspondiente en la celda "Load an image" del notebook. Ejecuta la celda y registra la nueva predicción. ¿Coincide con lo que ves en la imagen?
4. ¿Qué otra capacidad o sistema haría falta para localizar y contar objetos, además de validar los registros de un inventario?

**Resultado esperado:** una distinción correcta entre clasificación de imágenes y detección/conteo de objetos, con revisión humana.

### Desafío 4. Emitir el dictamen (2 minutos)

Completa la conclusión de tu archivo con este formato:

> **Dictamen:** El notebook [se ejecutó / fue observado en demostración / presentó una incidencia]. El modelo predijo **[etiqueta]** para **[imagen]**. Esta prueba demuestra **[capacidad observada]**, pero no demuestra **[limitación]**. Para apoyar un inventario de suministros sería necesario **[requisito adicional]**.

Guárdalo como `Dictamen_Inferencia_[INICIALES].md`.

**Resultado esperado:** un dictamen de 3–5 líneas que diferencia observaciones, limitaciones y necesidades de una posible aplicación.

---

## Criterios de logro

- [ ] Identifiqué qué modelo y dispositivo se utilizaron, según las salidas disponibles.
- [ ] Reconocí que se ejecutó **inferencia** con un modelo ya entrenado.
- [ ] Registré la clase predicha sin inventar resultados ni puntuaciones.
- [ ] Expliqué por qué clasificar una imagen no equivale a detectar y contar objetos.
- [ ] Emití una recomendación breve, con límites y verificación humana.

## Solución de problemas

| Situación | Qué hacer |
|---|---|
| No se abre el notebook | Confirmar acceso a Google Colab; avisar al instructor. |
| No conecta el entorno | Reintentar una vez; si persiste, utilizar la demostración del instructor. |
| Instalación o descarga lenta | Esperar el tiempo acordado; pasar a la demostración sin alterar celdas. |
| Error en una celda | Registrar la etapa y el mensaje; no afirmar que el notebook terminó correctamente. |
| El notebook muestra una etiqueta inesperada | Contrastar con la imagen, considerar error de clasificación y documentarlo. |
| No aparece puntuación de confianza | Registrar “no mostrada”; no estimarla. |
| Cambiaron los nombres de las secciones | Identificar las etapas por su función, con apoyo del instructor. |

## Alcance y uso responsable

Este laboratorio es una **demostración**, no una solución lista para operar en almacenes. No se deben cargar fotografías institucionales, información sensible ni imágenes de personas sin autorización. No se tomarán decisiones operativas reales con sus resultados.

---

[⬅ Anterior: Práctica 5](../Capitulo05/README.md) | [Inicio](../README.md) | [Siguiente: Práctica 7 ➡](../Capitulo07/README.md)

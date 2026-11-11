<img src="images/neteclogo.png" alt="logo" width="300"/>

# Taller práctico: Aplicación de la Inteligencia Artificial Moderna

## Plataforma de laboratorios

Te damos la bienvenida a la **plataforma de laboratorios** del curso **Taller práctico: Aplicación de la Inteligencia Artificial Moderna**. Aquí podrás explorar diferentes tecnologías a través de prácticas guiadas. ¡Desarrolla tus habilidades y lleva tus conocimientos al siguiente nivel!

## Descripción del curso

Taller práctico enfocado en la aplicación de conceptos de inteligencia artificial moderna, donde los participantes interactúan con distintos tipos de modelos (procesamiento de lenguaje natural, visión artificial y aprendizaje automático) para generar contenido, analizar información, traducir, evaluar resultados y comprender sus capacidades, limitaciones y uso en escenarios reales.

**Duración:** 2 horas (120 minutos), 100% práctica.

## Objetivos del taller

1. Aplicar conceptos clave de inteligencia artificial moderna en escenarios prácticos.
2. Identificar el tipo de IA adecuado según el problema (NLP, visión, ML).
3. Interactuar con modelos de IA mediante prompts estructurados.
4. Utilizar IA para generar, transformar y traducir información.
5. Comprender el funcionamiento básico del aprendizaje automático y profundo mediante herramientas visuales.
6. Evaluar la calidad, sesgos y limitaciones de los resultados generados por IA.
7. Integrar el uso de IA en flujos de trabajo para apoyar el análisis y la toma de decisiones.

## Perfil de audiencia

Profesionales y usuarios de áreas operativas, administrativas y técnicas que desean aplicar herramientas de inteligencia artificial en su trabajo, sin necesidad de experiencia previa en programación.

## Prerrequisitos

- Uso cotidiano de navegador web, correo electrónico y hojas de cálculo.
- Cuentas activas en las herramientas indicadas en la [Guía de configuración](Setup_Guide.md), en especial la cuenta de IBM Cloud con el plan Lite habilitado previamente.
- No se requieren conocimientos de programación.

> El temario no define perfil de audiencia ni prerrequisitos; los anteriores se derivan de la descripción, los objetivos, las herramientas y los requerimientos del taller.

## Lista de laboratorios

Cada uno de estos laboratorios está diseñado para ofrecerte una experiencia práctica. Haz clic en los enlaces para comenzar.

### [Práctica 1. Selección de tipo de IA según el problema](Capitulo01/README.md)

  - **Descripción**: clasificación de 8 escenarios de negocio en NLP, visión artificial o ML predictivo y contraste con ChatGPT o Copilot.
  - ⏱️ **Duración estimada**: 15 min.

### [Práctica 2. Ingeniería de prompts aplicada](Capitulo02/README.md)

  - **Descripción**: refinamiento iterativo de prompts mal estructurados para el reporte semanal de un centro de distribución.
  - ⏱️ **Duración estimada**: 15 min.

### [Práctica 3. Visión artificial con IA multimodal](Capitulo03/README.md)

  - **Descripción**: descripción de imágenes, detección de elementos y OCR con IA multimodal y Google Vision AI, y medición de precisión.
  - ⏱️ **Duración estimada**: 20 min.

### [Práctica 4. Aprendizaje automático interactivo](Capitulo04/README.md)

  - **Descripción**: entrenamiento de un clasificador de imágenes en Teachable Machine, evaluación de exactitud y corrección de un sesgo en los datos.
  - ⏱️ **Duración estimada**: 20 min.

### [Práctica 5. Simulación de aprendizaje profundo](Capitulo05/README.md)

  - **Descripción**: experimentos con capas, neuronas, características y tasa de aprendizaje en TensorFlow Playground.
  - ⏱️ **Duración estimada**: 20 min.

### [Práctica 6. OpenVINO Toolkit](Capitulo06/README.md)

  - **Descripción**: ejecución guiada en Google Colab de una inferencia de clasificación de imágenes con OpenVINO e interpretación del resultado.
  - ⏱️ **Duración estimada**: 15 min.

### [Práctica 7. IBM Watson Studio](Capitulo07/README.md)

  - **Descripción**: creación de un proyecto en IBM watsonx.ai Studio, carga de datos de incidencias y exploración sin programar.
  - ⏱️ **Duración estimada**: 15 min.

### Distribución del tiempo

| Práctica | Herramienta | Duración |
|---|---|---|
| 1. Selección de tipo de IA | ChatGPT o Copilot | 15 min |
| 2. Ingeniería de prompts aplicada | ChatGPT o Copilot | 15 min |
| 3. Visión artificial con IA multimodal | ChatGPT o Copilot y Google Vision AI | 20 min |
| 4. Aprendizaje automático interactivo | Teachable Machine | 20 min |
| 5. Simulación de aprendizaje profundo | TensorFlow Playground | 20 min |
| 6. OpenVINO Toolkit | OpenVINO Notebooks en Google Colab | 15 min |
| 7. IBM Watson Studio | IBM watsonx.ai Studio | 15 min |
| **Total** | | **120 min** |

## Instrucciones generales del laboratorio

1. Antes del taller, preparar el equipo y las cuentas con la [Guía de configuración](Setup_Guide.md). La cuenta de IBM Cloud debe estar lista antes de la sesión.
2. Cada práctica está en su carpeta `CapituloNN` con su `README.md` y la carpeta `recursos`. Para descargar un archivo, abrirlo y seleccionar **Download raw file**.
3. Guardar los entregables en `Documentos\Taller_IA_Moderna\PracticaNN\` con las iniciales del participante en el nombre.
4. Todos los datos de las prácticas son ficticios. No cargar información confidencial ni fotografías de personas en las herramientas de IA.
5. Las prácticas son progresivas: van del uso de IA generativa (1 a 3) al funcionamiento del aprendizaje automático y profundo (4 y 5) y a las plataformas para ejecutar y gestionar modelos (6 y 7).

## Estructura del repositorio

```text
.
├── README.md            Página principal (este archivo)
├── Setup_Guide.md       Guía de configuración del entorno
├── images/              Logotipo y diagramas de las prácticas
├── Capitulo01/          Práctica 1: README.md y recursos/
├── Capitulo02/          Práctica 2
├── Capitulo03/          Práctica 3
├── Capitulo04/          Práctica 4
├── Capitulo05/          Práctica 5
├── Capitulo06/          Práctica 6
└── Capitulo07/          Práctica 7
```

## Recursos adicionales

- [Google: Machine Learning Glossary](https://developers.google.com/machine-learning/glossary)
- [OpenAI: Prompt engineering](https://platform.openai.com/docs/guides/prompt-engineering)
- [Google Cloud Vision: documentación](https://cloud.google.com/vision/docs)

## Enlaces de referencia

- [Teachable Machine](https://teachablemachine.withgoogle.com/)
- [TensorFlow Playground](https://playground.tensorflow.org/)
- [OpenVINO Notebooks](https://github.com/openvinotoolkit/openvino_notebooks)
- [IBM watsonx.ai Studio en IBM Cloud](https://cloud.ibm.com/catalog/services/data-science-experience)

---

## 📬 **Contacto y más información**

Si tienes alguna pregunta o necesitas más detalles, no dudes en [contactarnos](mailto:soporte@netec.com). También puedes encontrar más recursos en nuestra [página](https://netec.com).

---

¡Gracias por visitar nuestra plataforma! No olvides revisar todos los laboratorios y comenzar tu viaje de aprendizaje hoy mismo.

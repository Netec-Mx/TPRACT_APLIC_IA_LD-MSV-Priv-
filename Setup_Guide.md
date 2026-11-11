<img src="images/neteclogo.png" alt="logo" width="300"/>

# Setup Guide General

## Taller práctico: Aplicación de la Inteligencia Artificial Moderna

| Control documental | Información |
|---|---|
| Clave del curso | TPRACT_APLIC_IA_LD MSV (Priv) |
| Versión del documento | 1.0 |
| Estado | BORRADOR: revisión documental completa; pendiente de validación con cuentas de participante |
| Instructor responsable | Por asignar por Netec |
| Fecha de elaboración | 2026-11-10 |
| Fecha de última validación | 2026-11-10 (revisión de herramientas y enlaces) |
| Repositorio de laboratorios | Repositorio de GitHub de Netec del curso (rama `main`) |
| Rama y revisión analizada | `main`, versión 1.0 |
| Alcance revisado | 7 prácticas, 12 archivos de recursos, README principal y Setup Guide |
| Modalidad del entorno | Web (servicios gratuitos o plan Lite) y Google Colab |

[Inicio](README.md)

# Objetivo

Preparar, para cada participante, una laptop con navegador actualizado y conexión a Internet, un editor de documentos y hojas de cálculo, y cuentas activas en ChatGPT o Microsoft Copilot, Google (Colab) e IBM Cloud con el plan Lite de watsonx.ai Studio habilitado. El entorno se considera listo cuando se aprueban las validaciones de la sección [Validación del Entorno](#validacion-entorno). No se instala software localmente.

# Requisitos de Hardware

| Recurso | Mínimo requerido | Recomendado | Observaciones |
|---|---|---|---|
| Equipo | Laptop de 64 bits, 2 núcleos | 4 núcleos | Requisito del temario: laptop con navegador web actualizado |
| Memoria RAM | 8 GB | 16 GB | Teachable Machine y TensorFlow Playground entrenan en el navegador |
| Espacio libre | 1 GB | 2 GB | Los recursos ocupan menos de 1 MB más el dataset (0.2 MB) |
| Cámara | Opcional | Cámara del teléfono | Para tomar la foto propia de la Práctica 3 |
| Conectividad | 10 Mbps | 25 Mbps | Requisito del temario: conexión a Internet |

# Sistemas Operativos Compatibles

| Sistema operativo | Edición y versión | Arquitectura | Condición de soporte o validación |
|---|---|---|---|
| Windows | 10 u 11 | x64 | Plataforma base; compatible según fabricante; pendiente de validar con cuenta de participante |
| macOS | 13 o posterior | Apple silicon o Intel | Compatible según fabricante; no validado |

# Software Requerido

| Componente | Edición y versión requerida | Arquitectura | Obligatorio u opcional | Fuente oficial |
|---|---|---|---|---|
| Navegador Google Chrome o Microsoft Edge | Versión estable vigente | x64 | Obligatorio | [google.com/chrome](https://www.google.com/chrome/) |
| Editor de documentos y hojas de cálculo | Microsoft 365, Google Docs y Sheets, o LibreOffice | x64 | Obligatorio | [microsoft365.com](https://www.microsoft365.com/) o [libreoffice.org](https://www.libreoffice.org/download/download-libreoffice/) |
| ChatGPT o Microsoft Copilot (web) | Servicio administrado; cuenta gratuita o de pago | N/A | Obligatorio (prácticas 1 a 3) | [chatgpt.com](https://chatgpt.com/) o [copilot.microsoft.com](https://copilot.microsoft.com/) |
| Google Vision AI demo | Servicio público | N/A | Obligatorio (Práctica 3) | [cloud.google.com/vision/docs/drag-and-drop](https://cloud.google.com/vision/docs/drag-and-drop) |
| Teachable Machine | Servicio público | N/A | Obligatorio (Práctica 4) | [teachablemachine.withgoogle.com](https://teachablemachine.withgoogle.com/) |
| TensorFlow Playground | Servicio público | N/A | Obligatorio (Práctica 5) | [playground.tensorflow.org](https://playground.tensorflow.org/) |
| Google Colab | Servicio administrado, nivel gratuito | N/A | Obligatorio (Práctica 6) | [colab.research.google.com](https://colab.research.google.com/) |
| OpenVINO Notebooks | Notebook `hello-world` de la rama `latest` | N/A | Obligatorio (Práctica 6) | [github.com/openvinotoolkit/openvino_notebooks](https://github.com/openvinotoolkit/openvino_notebooks) |
| IBM watsonx.ai Studio | Plan Lite | N/A | Obligatorio (Práctica 7) | [cloud.ibm.com/catalog/services/data-science-experience](https://cloud.ibm.com/catalog/services/data-science-experience) |

Los servicios web cambian su interfaz sin previo aviso. Registrar las diferencias observadas en el [Registro de validación](#registro-validacion).

# Herramientas y Dependencias

## Paquetes, frameworks y componentes adicionales

| Dependencia | Versión o restricción | Componente que la necesita | Método de instalación o habilitación |
|---|---|---|---|
| Paquete `openvino` | 2023.1.0 o posterior | Práctica 6 | Lo instala la primera celda del notebook en Colab |
| IBM Cloud Object Storage | Plan Lite | Práctica 7 | Se crea al asociar almacenamiento al primer proyecto |
| Carga de imágenes en ChatGPT o Copilot | Disponible con sesión iniciada; límites diarios en versiones gratuitas | Práctica 3 | Botón **+** o clip |
| Dataset de figuras | `Capitulo04/recursos/Dataset_Figuras.zip` | Práctica 4 | Descargar y descomprimir |

## Licencias, cuentas y permisos

| Recurso o servicio | Licencia o suscripción | Cuenta o rol requerido | Permiso mínimo | Responsable de habilitación |
|---|---|---|---|---|
| ChatGPT o Copilot | Gratuita o de pago | Cuenta de OpenAI o cuenta Microsoft | Usuario | Cada participante |
| Google Colab | Gratuita | Cuenta de Google | Usuario | Cada participante |
| IBM Cloud y watsonx.ai Studio | Plan Lite | IBMid con cuenta de IBM Cloud activa | Crear proyectos y almacenamiento | Cada participante, **antes del taller** |
| Teachable Machine, TensorFlow Playground, Vision AI demo | Acceso público | Sin cuenta | Uso público | No aplica |

El registro en IBM Cloud puede requerir verificación de identidad y tardar; por eso debe completarse antes del taller. No registrar contraseñas en el repositorio ni en los entregables.

# Instalación y Configuración

## 1. Obtener los materiales

- Repositorio autorizado: repositorio de GitHub del curso (botón **Code > Download ZIP**) o paquete ZIP del instructor.
- Revisión: rama `main`.
- Directorio de trabajo: `Documentos\Taller_IA_Moderna\` con las subcarpetas `Practica01` a `Practica07`.

## 2. Instalar o habilitar los componentes

### ChatGPT o Copilot

1. Iniciar sesión en [chatgpt.com](https://chatgpt.com/) o [copilot.microsoft.com](https://copilot.microsoft.com/).
2. Adjuntar la imagen `Capitulo03/recursos/Remision_Escaneada.png` y preguntar *"¿Qué folio tiene este documento?"*.

**Resultado esperado:** la respuesta indica REM-2026-08814.

### Google Colab

1. Abrir [colab.research.google.com](https://colab.research.google.com/) con la cuenta de Google.
2. Crear un notebook nuevo y seleccionar **Conectar**.

**Resultado esperado:** el entorno se conecta.

### IBM Cloud y watsonx.ai Studio (plan Lite)

1. Crear una cuenta en [cloud.ibm.com](https://cloud.ibm.com/) con su correo y completar la verificación que solicite IBM.
2. Abrir [el servicio en el catálogo](https://cloud.ibm.com/catalog/services/data-science-experience), seleccionar el plan **Lite** y crear el servicio en la región indicada por el instructor.
3. Abrir [dataplatform.cloud.ibm.com](https://dataplatform.cloud.ibm.com/) y confirmar que aparece la página de inicio de watsonx.

**Resultado esperado:** acceso a la página de inicio y opción **Create a project** disponible.

### Carpetas de trabajo

1. Crear `Documentos\Taller_IA_Moderna\` y, dentro, `Practica01` a `Practica07`.
2. Copiar a cada carpeta el contenido de `CapituloNN\recursos`.

## 3. Preparar archivos de configuración

No se requieren archivos de configuración.

# Variables de Entorno

No se requieren variables de entorno.

# Configuración Base para los Laboratorios

## Parámetros comunes

| Parámetro | Valor o convención | Observaciones |
|---|---|---|
| Raíz de trabajo | `Documentos\Taller_IA_Moderna\` | Una carpeta por práctica |
| Nombre de entregables | `Nombre_[INICIALES].ext` | Iniciales del participante |
| Datos | Ficticios | No cargar datos reales ni fotos de personas |
| Región de IBM Cloud | La que indique el instructor | Usar la misma para el servicio y el almacenamiento |

## Estructura de carpetas

```text
Documentos\Taller_IA_Moderna\
├── Practica01\ ... Practica07\   Recursos y entregables de cada práctica
```

## Recursos compartidos

No hay recursos compartidos entre participantes. Cada uno crea su propio proyecto en watsonx.ai Studio.

## Preparación antes de cada práctica

| Práctica | Preparación |
|---|---|
| 1 y 2 | Sesión iniciada en ChatGPT o Copilot |
| 3 | Foto propia sin personas ni datos, guardada en la carpeta de trabajo |
| 4 | `Dataset_Figuras.zip` descomprimido |
| 5 | Ninguna |
| 6 | Sesión iniciada en Google |
| 7 | Cuenta de IBM Cloud con watsonx.ai Studio Lite habilitado |

## Correcciones de coherencia

| Inconsistencia o dependencia omitida | Configuración unificada | Ajuste necesario en las copias de trabajo |
|---|---|---|
| El temario no define perfil de audiencia ni prerrequisitos | Se derivaron de la descripción, los objetivos y las herramientas (usuarios sin experiencia en programación) | Confirmar con el cliente |
| El temario menciona "casos prácticos", "guía de prompts" e "imágenes proporcionadas por NETEC" sin incluirlos | Se crearon en `Capitulo01`, `Capitulo02` y `Capitulo03/recursos` | Ninguno |
| Teachable Machine requiere ejemplos para entrenar | Dataset de figuras con un conjunto sesgado para mostrar el efecto de los datos | Ninguno |
| El temario cita "IBM Watson Studio"; el servicio actual se llama IBM watsonx.ai Studio | Se usa el nombre actual con referencia al anterior | Ninguno |

# Servicios Externos Requeridos

| Servicio | URL, endpoint o región | Uso | Acceso requerido |
|---|---|---|---|
| ChatGPT o Copilot | [chatgpt.com](https://chatgpt.com/), [copilot.microsoft.com](https://copilot.microsoft.com/) | Prácticas 1 a 3 | Cuenta |
| Google Vision AI demo | [cloud.google.com/vision/docs/drag-and-drop](https://cloud.google.com/vision/docs/drag-and-drop) | Práctica 3 | Público |
| Teachable Machine | [teachablemachine.withgoogle.com](https://teachablemachine.withgoogle.com/) | Práctica 4 | Público |
| TensorFlow Playground | [playground.tensorflow.org](https://playground.tensorflow.org/) | Práctica 5 | Público |
| Google Colab y GitHub | [colab.research.google.com](https://colab.research.google.com/), [github.com](https://github.com/) | Práctica 6 y materiales | Cuenta de Google |
| IBM watsonx | [dataplatform.cloud.ibm.com](https://dataplatform.cloud.ibm.com/) | Práctica 7 | IBMid |

## Configuración de red

| Origen | Destino | Protocolo y puerto | Sentido | Condición |
|---|---|---|---|---|
| Equipo del participante | chatgpt.com, copilot.microsoft.com, cloud.google.com, teachablemachine.withgoogle.com, playground.tensorflow.org, colab.research.google.com, github.com, storage.openvinotoolkit.org, cloud.ibm.com, dataplatform.cloud.ibm.com | HTTPS 443 | Saliente | Dominios permitidos en el proxy o firewall |

# Creación de Entornos / Máquinas Virtuales / Emuladores

| Elemento | Tipo o plataforma | Imagen y versión | Recursos asignados | Red o región | Persistencia |
|---|---|---|---|---|---|
| Entorno de Colab | Entorno cloud administrado por Google | Imagen vigente de Colab | Los del nivel gratuito | Internet | Temporal; se borra al desconectar |
| Proyecto de watsonx.ai Studio | Entorno cloud de IBM | Plan Lite | Los del plan Lite | Región indicada por el instructor | Persistente hasta eliminar el proyecto |

<a id="validacion-entorno"></a>

# Validación del Entorno

| ID | Componente o capacidad | Procedimiento | Resultado esperado | Evidencia mínima |
|---|---|---|---|---|
| V-01 | Materiales | Abrir `Capitulo01/recursos/Casos_Practicos_Tipo_IA.xlsx` | La hoja `Escenarios` tiene 8 casos | Captura |
| V-02 | IA multimodal | Adjuntar `Remision_Escaneada.png` en ChatGPT o Copilot y pedir el folio | REM-2026-08814 | Captura |
| V-03 | Teachable Machine | Crear un **Image Project** y cargar 5 imágenes del dataset | Las imágenes aparecen en la clase | Captura |
| V-04 | TensorFlow Playground | Abrir el sitio y seleccionar **Play** | La animación del entrenamiento avanza | Captura |
| V-05 | Colab y OpenVINO | Abrir el notebook de la Práctica 6 y ejecutar la primera celda | La celda termina sin error | Captura |
| V-06 | IBM watsonx.ai Studio | Iniciar sesión en dataplatform.cloud.ibm.com | Opción **Create a project** disponible | Captura |

**Criterio de entorno listo:** V-01 a V-06 aprobadas. V-06 debe aprobarse antes del día del taller.

# Comandos de Verificación

No aplica. El taller se valida en interfaces web con los procedimientos V-01 a V-06.

# Troubleshooting

| Síntoma | Causa probable | Comprobación | Corrección | Validación posterior |
|---|---|---|---|---|
| Límite de mensajes o de imágenes en ChatGPT o Copilot | Restricción de la versión gratuita | Mensaje del servicio | Cambiar a la otra herramienta | V-02 |
| Colab no conecta | Límite de uso o red | Botón **Conectar** | Esperar o usar otra cuenta de Google | V-05 |
| IBM Cloud no permite crear el servicio | Cuenta sin verificar o región sin plan Lite | Mensaje del catálogo | Completar la verificación o cambiar de región | V-06 |
| Teachable Machine se congela | Memoria o pestaña en segundo plano | Barra de progreso detenida | Cerrar pestañas y mantener visible la página | V-03 |

# Checklist Final

- [ ] Laptop con navegador actualizado y conexión a Internet.
- [ ] Cuenta de ChatGPT o Copilot activa.
- [ ] Cuenta de Google para Colab.
- [ ] Cuenta de IBM Cloud con watsonx.ai Studio Lite habilitado.
- [ ] Recursos descargados en `Documentos\Taller_IA_Moderna\` y dataset descomprimido.
- [ ] Validaciones V-01 a V-06 aprobadas.

# Resumen

Para iniciar el taller, cada participante necesita una laptop con navegador y conexión a Internet, un editor de documentos y hojas de cálculo, una cuenta de ChatGPT o Copilot, una cuenta de Google y una cuenta de IBM Cloud con el plan Lite de watsonx.ai Studio habilitado previamente. No se instala software localmente.

<a id="registro-validacion"></a>

## Registro de validación

| Fecha | Responsable | Plataforma o entorno probado | Resultado | Limitaciones o acciones pendientes |
|---|---|---|---|---|
| 2026-11-10 | Desarrollo de contenido Netec | Revisión de enlaces y herramientas; contenido del notebook `hello-world` de OpenVINO | APTO para publicación del repositorio | No se ejecutaron las prácticas con cuentas de participante ni el notebook en Colab. Pendiente: V-01 a V-06 |

## Referencias oficiales

| Documento o recurso | URL | Fecha de consulta |
|---|---|---|
| Google Cloud Vision: demo | https://cloud.google.com/vision/docs/drag-and-drop | 2026-11-10 |
| Teachable Machine | https://teachablemachine.withgoogle.com/ | 2026-11-10 |
| TensorFlow Playground | https://playground.tensorflow.org/ | 2026-11-10 |
| OpenVINO Notebooks | https://github.com/openvinotoolkit/openvino_notebooks | 2026-11-10 |
| IBM watsonx.ai Studio (catálogo) | https://cloud.ibm.com/catalog/services/data-science-experience | 2026-11-10 |

[Inicio](README.md)

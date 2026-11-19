
# 📝 Generación automatizada de artículos personalizados mediante IA

> Sistema de investigación, redacción y generación de documentos personalizados mediante agentes de Inteligencia Artificial y flujos de automatización con n8n.

<p align="center">
  <a href="https://drive.google.com/file/d/1q6cXKBeEwNUyQ4hlhbhZKGDdtwlKDTvb/view?usp=sharing">
    <img src="https://drive.google.com/thumbnail?id=1q6cXKBeEwNUyQ4hlhbhZKGDdtwlKDTvb&sz=w1200" alt="Ver demostración completa del proyecto" width="85%">
  </a>
</p>

<p align="center">
  ▶️ <a href="https://drive.google.com/file/d/1q6cXKBeEwNUyQ4hlhbhZKGDdtwlKDTvb/view?usp=sharing"><strong>VER DEMOSTRACIÓN COMPLETA DEL PROYECTO</strong></a>
</p>

---

## 📌 Descripción del proyecto

Este proyecto consiste en desarrollar un sistema automatizado capaz de investigar un tema de interés, elaborar un artículo personalizado y entregarlo al solicitante en formato PDF mediante correo electrónico.

La solución parte de un formulario de Google Forms, donde el usuario introduce sus datos de contacto y el tema sobre el que desea recibir información.

Una vez recibida la solicitud, n8n inicia un flujo de trabajo que organiza los datos, los registra en Google Sheets y activa dos agentes de Inteligencia Artificial con responsabilidades diferenciadas: un agente investigador y un agente redactor.

El primer agente se encarga de investigar el tema solicitado y recopilar información relevante. Posteriormente, el segundo agente utiliza esa información para elaborar un artículo estructurado y personalizado.

El documento se genera mediante Google Docs, se prepara su contenido para convertirlo a PDF y finalmente se envía al usuario por Gmail como archivo adjunto, acompañado de un enlace para consultar el documento online.

Además, el sistema actualiza el registro de la solicitud y envía una notificación a Slack cuando se completa el proceso.

El objetivo es automatizar el recorrido completo desde la recepción de una petición hasta la entrega de un documento personalizado, reduciendo la intervención manual en las tareas de investigación, redacción y distribución.

## 🎯 Objetivos

- Automatizar la recepción de solicitudes mediante un formulario.
- Recopilar y organizar los datos de los usuarios.
- Registrar las solicitudes en una hoja de cálculo.
- Utilizar agentes de IA para investigar temas específicos.
- Generar artículos personalizados a partir de la información recopilada.
- Crear documentos estructurados mediante Google Docs.
- Convertir automáticamente los artículos a formato PDF.
- Enviar los documentos al usuario por correo electrónico.
- Mantener actualizado el registro de solicitudes.
- Notificar al equipo cuando se completa una generación.

## ⚙️ Funcionamiento del sistema

El proyecto reúne diferentes etapas dentro de un único flujo automatizado.

### 1. Recepción de solicitudes mediante Google Forms

El proceso comienza con un formulario de solicitud de artículo personalizado.

El usuario debe proporcionar:

- Nombre.
- Correo electrónico.
- Tema de interés.

El formulario permite recoger la información necesaria para iniciar la investigación y personalizar el documento que se generará posteriormente.

### 2. Registro y preparación de los datos

Cuando se recibe una nueva solicitud, n8n detecta la entrada y prepara la información para continuar el proceso.

Los datos se organizan y se registran en Google Sheets, donde se conserva la información del solicitante, el tema solicitado y otros datos asociados al proceso.

### 3. Investigación mediante un agente de IA

El primer agente de Inteligencia Artificial se encarga de investigar el tema indicado por el usuario.

Para realizar esta tarea, el flujo incorpora una herramienta de búsqueda web y un modelo de IA.

Su función es recopilar información relevante y preparar una base de contenido que pueda utilizarse durante la redacción del artículo.

### 4. Redacción mediante un segundo agente de IA

Una vez finalizada la investigación, la información pasa a un segundo agente especializado en redacción.

Este agente recibe el contenido recopilado y se encarga de transformarlo en un artículo estructurado y personalizado.

La separación entre investigación y redacción permite distribuir las responsabilidades y organizar mejor las distintas etapas del trabajo.

### 5. Creación del documento en Google Docs

El contenido generado se prepara y se incorpora a un documento de Google Docs.

En esta fase se crea el documento personalizado y se organiza su contenido para preparar la versión final.

### 6. Preparación y generación del PDF

Una vez creado el documento, el flujo procesa su contenido y prepara una versión en HTML.

Posteriormente, se utiliza un servicio de generación de documentos PDF para producir el archivo final.

De esta manera, el usuario recibe un documento descargable con el artículo solicitado.

### 7. Entrega automática mediante Gmail

Cuando el PDF está generado, el sistema envía un correo electrónico al usuario.

El mensaje incluye:

- Una confirmación de que el artículo está listo.
- El documento PDF como archivo adjunto.
- Un enlace para consultar o editar el documento online.

### 8. Actualización del registro y notificación en Slack

Al finalizar el proceso, el flujo contempla dos operaciones adicionales:

- Actualizar el registro de la solicitud en Google Sheets.
- Enviar una notificación a Slack indicando que se ha generado un nuevo artículo personalizado.

Esto permite mantener un registro del trabajo realizado y comunicar la finalización del proceso.

## 🔄 Arquitectura e integración de herramientas

La solución utiliza n8n como núcleo de automatización y coordina diferentes herramientas y agentes de IA para completar el proceso.

| Herramienta | Función dentro del proyecto |
|---|---|
| **Google Forms** | Recepción de solicitudes y datos del usuario. |
| **n8n** | Diseño, coordinación y ejecución del flujo de automatización. |
| **Agente investigador** | Investigación y recopilación de información sobre el tema solicitado. |
| **Agente redactor** | Elaboración del artículo personalizado. |
| **Herramienta de búsqueda web** | Consulta de información para el agente investigador. |
| **Google Sheets** | Registro y actualización de las solicitudes. |
| **Google Docs** | Creación y almacenamiento del artículo. |
| **Generación de PDF** | Conversión del contenido preparado a un documento PDF. |
| **Gmail** | Entrega del artículo al usuario por correo electrónico. |
| **Slack** | Notificación de la generación de nuevos artículos. |

### Esquema general

```text
             USUARIO
                │
                ▼
          GOOGLE FORMS
                │
                ▼
       NUEVA SOLICITUD EN n8n
                │
                ▼
       PREPARACIÓN DE DATOS
                │
                ▼
         GOOGLE SHEETS
                │
                ▼
       AGENTE INVESTIGADOR
                │
          BÚSQUEDA WEB
                │
                ▼
         AGENTE REDACTOR
                │
                ▼
          GOOGLE DOCS
                │
                ▼
       PREPARACIÓN DEL HTML
                │
                ▼
          GENERACIÓN PDF
                │
          ┌─────┴─────┐
          ▼           ▼
        GMAIL       SLACK
          │           │
          ▼           ▼
      ENTREGA AL   NOTIFICACIÓN
       USUARIO     AL EQUIPO
          │
          ▼
    ACTUALIZACIÓN DEL
     REGISTRO EN SHEETS
```

*Esquema conceptual del proceso de automatización mostrado en el proyecto.*

## 🛠️ Tecnologías y herramientas

- Automatización de procesos con n8n.
- Agentes de Inteligencia Artificial.
- Modelos de lenguaje (LLM).
- Herramientas de búsqueda web.
- Google Forms.
- Google Sheets.
- Google Docs.
- Gmail.
- Slack.
- Preparación de contenido HTML.
- Generación automatizada de documentos PDF.

## 💡 Valor aportado

Este proyecto demuestra cómo se puede automatizar un proceso de producción de contenido, combinando investigación, redacción y generación documental mediante diferentes herramientas.

Entre los principales aspectos que se trabajan destacan:

- Automatización de solicitudes personalizadas.
- Separación de tareas entre agentes de IA especializados.
- Investigación asistida mediante herramientas de búsqueda.
- Generación de contenido estructurado.
- Creación automática de documentos.
- Entrega de resultados en formato PDF.
- Integración de servicios de comunicación y notificación.
- Registro y seguimiento de las solicitudes recibidas.

La solución permite transformar una petición sencilla introducida en un formulario en un documento personalizado, sin tener que realizar manualmente cada una de las etapas intermedias.

## 📚 Aprendizajes

El desarrollo de este proyecto permite trabajar con diferentes conceptos relacionados con la Inteligencia Artificial y la automatización:

- Diseño y estructuración de workflows en n8n.
- Creación y coordinación de agentes de IA.
- Diferenciación de responsabilidades entre agentes.
- Integración de herramientas externas en flujos automatizados.
- Recepción y procesamiento de formularios.
- Gestión de información mediante Google Sheets.
- Generación de documentos con Google Docs.
- Preparación de contenido HTML y conversión a PDF.
- Automatización del envío de correos electrónicos.
- Integración de notificaciones mediante Slack.
- Diseño de procesos automatizados de principio a fin.

---

## 🎓 Evaluación y feedback docente

<img width="480" height="239" alt="2" src="https://github.com/user-attachments/assets/e74701bc-d6d8-44e7-afa4-7dcb4f7485e9" />

---

<p align="center">
  <strong>PROYECTO 02 · AUTOMATION & AI</strong>
  <br>
  Ángel Ruiz Zapata
  <br>
  <a href="https://github.com/Aruizzapata">GitHub</a>
</p>

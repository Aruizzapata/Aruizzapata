
# 🤖 Sistema multimodal de atención al cliente y gestión de incidencias

> Desarrollo de un sistema automatizado de atención al cliente mediante Telegram, capaz de procesar mensajes de texto, audio e imágenes, consultar información comercial, gestionar solicitudes y crear tickets de incidencias mediante n8n y Notion.

<p align="center">
  <a href="https://drive.google.com/file/d/1pBzMFB_waRDoB7b2KwXnOEladWBctDKV/view?usp=sharing">
    <img src="https://drive.google.com/thumbnail?id=1pBzMFB_waRDoB7b2KwXnOEladWBctDKV&sz=w1200" alt="Ver demostración completa del proyecto" width="85%">
  </a>
</p>

<p align="center">
  ▶️ <a href="https://drive.google.com/file/d/1pBzMFB_waRDoB7b2KwXnOEladWBctDKV/view?usp=sharing"><strong>VER DEMOSTRACIÓN COMPLETA DEL PROYECTO</strong></a>
</p>

---

## 📌 Descripción del proyecto

Este proyecto consiste en desarrollar un sistema integral de atención al cliente y gestión de incidencias para un negocio de distribución, utilizando Telegram como uno de los principales canales de comunicación y n8n como motor de automatización.

La solución amplía las capacidades de un asistente conversacional tradicional mediante la incorporación de diferentes modalidades de entrada, permitiendo que los clientes interactúen a través de mensajes de texto, notas de voz e imágenes.

El sistema utiliza agentes de Inteligencia Artificial para interpretar las consultas, consultar información documentada sobre preguntas frecuentes y acceder a los datos del catálogo de productos.

Además de responder a las consultas habituales, la solución contempla la gestión de incidencias y solicitudes que requieren intervención humana.

Para ello, incorpora un sistema de tickets integrado con Notion, donde se registran las solicitudes, su categoría, prioridad, canal de origen y demás información necesaria para organizar su seguimiento.

La automatización también contempla la asignación de incidencias a agentes especializados y el envío de notificaciones por correo electrónico para comunicar las intervenciones pendientes.

El proyecto se completa con diferentes workflows independientes para gestionar las conversaciones de Telegram, las consultas recibidas mediante formularios web, el registro de nuevos clientes y el enrutamiento de las solicitudes.

El objetivo es construir un entorno de atención automatizada que combine Inteligencia Artificial, gestión estructurada de información y mecanismos de intervención humana.

## 🎯 Objetivos

- Automatizar la atención al cliente mediante Telegram.
- Permitir la interacción mediante texto, audio e imágenes.
- Interpretar las consultas y necesidades de los usuarios.
- Consultar información documentada mediante agentes de IA.
- Facilitar el acceso al catálogo de productos.
- Recuperar información sobre pedidos, productos y condiciones del servicio.
- Identificar consultas que requieren atención humana.
- Clasificar las incidencias según su categoría y prioridad.
- Crear y gestionar tickets mediante Notion.
- Organizar la asignación de incidencias a agentes especializados.
- Automatizar las notificaciones por correo electrónico.
- Incorporar formularios web para recibir consultas y nuevos clientes.
- Separar los procesos en diferentes workflows para facilitar su organización.

## ⚙️ Funcionamiento del sistema

El proyecto reúne diferentes procesos de automatización que permiten gestionar tanto las consultas habituales como las solicitudes que requieren seguimiento.

### 1. Interacción multimodal mediante Telegram

Telegram funciona como uno de los principales canales de comunicación entre el cliente y el sistema.

A diferencia de un chatbot limitado a mensajes de texto, el asistente contempla diferentes modalidades de interacción:

- Mensajes de texto.
- Notas de voz.
- Fotografías e imágenes.

Esta capacidad permite que los clientes puedan comunicar sus necesidades de diferentes maneras, sin depender exclusivamente de la escritura.

### 2. Procesamiento de mensajes y comprensión de consultas

Los mensajes recibidos se procesan mediante los workflows de n8n.

El sistema identifica el contenido de la interacción y prepara la información para que pueda ser interpretada por el agente correspondiente.

En el caso de las entradas de audio e imágenes, se incorporan al proceso de interpretación para obtener información útil con la que continuar la conversación.

### 3. Consulta de preguntas frecuentes y catálogo

El asistente utiliza información documentada para responder a las consultas habituales de los clientes.

Entre las fuentes de información utilizadas se encuentran:

- Preguntas frecuentes (FAQ).
- Catálogo de productos.
- Información comercial.
- Datos relacionados con el servicio.

El agente puede consultar estas fuentes para proporcionar respuestas relacionadas con horarios, condiciones de reparto, productos y disponibilidad.

La información centralizada permite que las respuestas estén vinculadas a los datos del negocio y no dependan únicamente del conocimiento general del modelo.

### 4. Atención conversacional y continuidad de las respuestas

El sistema está diseñado para mantener una interacción conversacional con el cliente.

Cuando el usuario realiza una consulta, el asistente procesa la petición, obtiene la información necesaria y devuelve una respuesta dentro del mismo canal de comunicación.

Esta continuidad facilita que el cliente pueda realizar diferentes consultas dentro de una misma conversación.

### 5. Identificación de solicitudes que requieren intervención humana

El proyecto contempla un mecanismo de triaje para determinar si una consulta puede resolverse mediante el asistente o si necesita ser atendida por una persona.

Para ello, el sistema calcula si es necesaria la intervención de un agente humano.

Esta clasificación permite diferenciar entre consultas habituales y situaciones que requieren una gestión especializada.

No obstante, en la evaluación docente se identificó que el resultado de esta decisión todavía no estaba conectado correctamente con la derivación efectiva, por lo que constituye un punto de mejora del desarrollo.

### 6. Creación y clasificación de tickets en Notion

Cuando se registra una incidencia, el sistema puede crear un ticket dentro de la base de datos de Notion.

Cada ticket permite organizar información relacionada con la solicitud:

- Identificador del ticket.
- Descripción de la incidencia.
- Categoría.
- Prioridad.
- Canal de comunicación.
- Cliente asociado.
- Fecha de apertura.
- Información de seguimiento.

La estructura permite centralizar las solicitudes y disponer de un registro organizado de las incidencias recibidas.

### 7. Asignación de incidencias a agentes

El sistema contempla la asignación de tickets a diferentes agentes en función de la naturaleza de la incidencia.

Por ejemplo, una incidencia relacionada con entregas puede asignarse a una persona especializada en esa área.

El flujo utiliza la información de los agentes y las características de cada solicitud para organizar la asignación.

### 8. Notificaciones mediante Gmail

Una vez creado y asignado un ticket, el sistema contempla el envío de un correo electrónico para informar de la nueva intervención.

La notificación incluye información relevante sobre la incidencia:

- Número de ticket.
- Categoría.
- Prioridad.
- Canal de origen.
- Cliente.
- Descripción de la solicitud.
- Agente asignado.
- Enlace al ticket en Notion.

De esta manera, el responsable recibe la información necesaria para localizar y gestionar la incidencia.

### 9. Recepción de consultas mediante formularios web

Además de Telegram, el proyecto incorpora workflows para gestionar solicitudes recibidas mediante formularios web.

Se identifican dos procesos diferenciados:

**Formulario web de consultas**

Permite recibir solicitudes de información y consultas comerciales, procesar sus datos y determinar si corresponde generar una respuesta automática mediante correo electrónico.

**Formulario web de nuevos clientes**

Permite incorporar nuevos contactos al sistema y preparar la información necesaria para su registro y posterior gestión.

Esta separación permite atender diferentes tipos de solicitudes sin concentrar toda la lógica en un único flujo.

## 🔄 Arquitectura e integración de herramientas

La solución utiliza n8n como núcleo de automatización y Notion como espacio centralizado de gestión de información.

El sistema se organiza mediante diferentes workflows especializados que permiten separar las responsabilidades de cada proceso.

| Herramienta | Función dentro del proyecto |
|---|---|
| **n8n** | Diseño, coordinación y ejecución de los workflows. |
| **Telegram** | Canal de comunicación con los clientes. |
| **Agentes de IA** | Interpretación de consultas y búsqueda de información documentada. |
| **Notion** | Gestión de clientes, agentes, conversaciones, catálogo, pedidos y tickets. |
| **Gmail** | Envío de notificaciones y comunicaciones relacionadas con las solicitudes. |
| **Jotform** | Recepción de consultas y datos mediante formularios web. |

### Workflows desarrollados

El proyecto está organizado en cinco flujos principales:

| Workflow | Responsabilidad |
|---|---|
| **Workflow Telegram** | Gestión de las conversaciones y solicitudes recibidas mediante Telegram. |
| **Workflow Triaje** | Análisis y clasificación de las solicitudes para determinar su tratamiento. |
| **Workflow Formulario Web - Nuevo Cliente** | Procesamiento de formularios de registro de nuevos clientes. |
| **Workflow Formulario Web - Consultas** | Gestión de consultas recibidas mediante formularios web. |
| **Workflow Gmail** | Gestión de comunicaciones y notificaciones por correo electrónico. |

### Esquema general

```text
                 CLIENTE
                    │
          ┌─────────┴─────────┐
          ▼                   ▼
       TELEGRAM          FORMULARIOS WEB
          │                   │
          ▼                   ▼
    WORKFLOW TELEGRAM    WORKFLOWS WEB
          │                   │
          ▼                   ▼
    PROCESAMIENTO       NORMALIZACIÓN
    DE MENSAJES          DE DATOS
          │                   │
          ▼                   ▼
     AGENTE DE IA        WORKFLOW TRIAJE
          │                   │
     ┌────┴─────┐             │
     ▼          ▼             │
    FAQ      CATÁLOGO         │
     │          │             │
     └────┬─────┘             │
          │                   │
          ▼                   ▼
       RESPUESTA       CLASIFICACIÓN DE
       AL CLIENTE       LA SOLICITUD
                              │
                     ┌────────┴────────┐
                     ▼                 ▼
                 RESOLUCIÓN       INTERVENCIÓN
                 AUTOMÁTICA         HUMANA
                                       │
                                       ▼
                                 TICKET NOTION
                                       │
                                       ▼
                                  ASIGNACIÓN
                                  DE AGENTE
                                       │
                                       ▼
                                    GMAIL
                                       │
                                       ▼
                                  NOTIFICACIÓN
```

*Esquema conceptual de los diferentes procesos que componen la solución.*

## 🛠️ Tecnologías y herramientas

- Automatización de procesos con n8n.
- Inteligencia Artificial y agentes conversacionales.
- Procesamiento de mensajes de texto.
- Interacción mediante audio e imágenes.
- Telegram Bot.
- Gestión de bases de datos con Notion.
- Organización y asignación de tickets.
- Integración de correo electrónico mediante Gmail.
- Formularios web mediante Jotform.
- Diseño de workflows especializados.
- Automatización de procesos de atención al cliente.

## 💡 Valor aportado

Este proyecto demuestra cómo se puede construir un sistema de atención al cliente que combina automatización, Inteligencia Artificial y gestión estructurada de incidencias.

Entre los principales aspectos que se trabajan destacan:

- Atención conversacional mediante diferentes formatos de entrada.
- Procesamiento de mensajes de texto, audio e imágenes.
- Consulta automatizada de información comercial.
- Acceso a preguntas frecuentes y catálogo de productos.
- Organización de incidencias mediante tickets.
- Clasificación de solicitudes según su prioridad.
- Asignación de tareas a agentes especializados.
- Integración de diferentes canales de comunicación.
- Centralización de la información en Notion.
- Automatización de notificaciones y comunicaciones internas.

La solución plantea un modelo de atención híbrido en el que la Inteligencia Artificial puede resolver consultas habituales, mientras que las incidencias que requieren intervención especializada se organizan para su seguimiento.

## 📚 Aprendizajes

El desarrollo de este proyecto permite trabajar con diferentes conceptos relacionados con la automatización avanzada y los asistentes de Inteligencia Artificial:

- Diseño de arquitecturas con múltiples workflows en n8n.
- Integración de bots de Telegram.
- Procesamiento de entradas multimodales.
- Utilización de agentes de IA.
- Consulta de información documentada mediante FAQ y catálogos.
- Organización de bases de datos en Notion.
- Diseño de sistemas de tickets.
- Clasificación y priorización de incidencias.
- Asignación de solicitudes a agentes especializados.
- Integración de Gmail para notificaciones.
- Automatización de formularios web.
- Diseño de procesos de atención híbrida entre IA y personas.

---

## 🎓 Evaluación y feedback docente

> Ángel, antes de nada enhorabuena por tu esfuerzo, porque has ido mucho más allá de lo que pedía el ejercicio.

<img width="482" height="233" alt="4" src="https://github.com/user-attachments/assets/420d7940-ce9d-4a74-a624-9411ab5d6526" />




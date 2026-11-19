
# 🎯 Sistema automatizado de captación y cualificación de clientes potenciales con IA

> Sistema de automatización comercial que permite recibir solicitudes de potenciales clientes, analizar sus necesidades mediante Inteligencia Artificial, cualificarlos y gestionar automáticamente su información, comunicaciones y seguimiento mediante n8n, Notion y diferentes servicios integrados.

<p align="center">
  <a href="https://drive.google.com/file/d/1p4CW1y4FwAcbzmwoovuqtd_0B6BsSmhE/view?usp=sharing">
    <img src="https://drive.google.com/thumbnail?id=1p4CW1y4FwAcbzmwoovuqtd_0B6BsSmhE&sz=w1200" alt="Ver demostración completa del proyecto" width="85%">
  </a>
</p>

<p align="center">
  ▶️ <a href="https://drive.google.com/file/d/1p4CW1y4FwAcbzmwoovuqtd_0B6BsSmhE/view?usp=sharing"><strong>VER DEMOSTRACIÓN COMPLETA DEL PROYECTO</strong></a>
</p>

---

## 📌 Descripción del proyecto

Este proyecto consiste en desarrollar un sistema automatizado de captación, análisis y gestión de clientes potenciales para una empresa dedicada al desarrollo de aplicaciones móviles y soluciones web.

La solución permite recibir solicitudes comerciales mediante un formulario de Google Forms, recopilar información sobre las necesidades de cada cliente y procesarla mediante un flujo de automatización desarrollado en n8n.

A partir de los datos recibidos, el sistema analiza la información proporcionada, identifica el tipo de aplicación que necesita el cliente y utiliza Inteligencia Artificial para evaluar sus características y clasificar la oportunidad comercial.

La información se organiza y almacena en Notion, utilizando una estructura de CRM para gestionar los contactos y los proyectos asociados.

Además, el sistema contempla la validación de direcciones de correo electrónico, la detección de clientes existentes, la generación de respuestas comerciales personalizadas mediante Gmail y el envío de notificaciones internas a través de Slack.

El proyecto incorpora también un workflow independiente de gestión de errores, diseñado para recuperar información de ejecuciones fallidas y avisar al responsable mediante Slack.

El objetivo es automatizar gran parte del proceso comercial, desde la recepción de una solicitud hasta su clasificación, registro y comunicación con el potencial cliente.

## 🎯 Objetivos

- Automatizar la recepción de solicitudes comerciales.
- Recopilar información sobre los clientes y sus necesidades.
- Analizar las características de cada oportunidad comercial mediante IA.
- Clasificar los clientes según su situación y características.
- Identificar el tipo de aplicación que necesita cada solicitante.
- Evaluar y priorizar las oportunidades comerciales.
- Validar las direcciones de correo electrónico.
- Detectar clientes existentes para evitar duplicidades.
- Centralizar la información comercial en Notion.
- Generar respuestas personalizadas mediante Gmail.
- Notificar al equipo comercial sobre nuevas oportunidades.
- Incorporar un sistema independiente de gestión de errores.

## ⚙️ Funcionamiento del sistema

El proyecto reúne diferentes etapas dentro de un proceso automatizado de captación y gestión comercial.

### 1. Recepción de solicitudes mediante Google Forms

El proceso comienza con un formulario de contacto diseñado para recoger información de personas interesadas en contratar servicios de desarrollo de aplicaciones móviles y web.

El formulario solicita información como:

- Nombre y apellidos.
- Dirección de correo electrónico.
- Teléfono de contacto.
- Tipo de aplicación que necesita.
- Descripción de la idea o proyecto.
- Servicios sobre los que desea recibir información.

También permite seleccionar diferentes necesidades comerciales, como precios, presupuestos aproximados, tipos de aplicaciones y plazos de desarrollo.

Esta información constituye la entrada del sistema y permite conocer las características iniciales de cada oportunidad comercial.

### 2. Registro y organización de la información

Cuando se recibe una nueva solicitud, n8n inicia el flujo de automatización y procesa los datos enviados mediante el formulario.

La información se registra en Google Sheets, donde se mantiene una base de respuestas y datos de referencia relacionados con los servicios de la empresa.

La hoja de cálculo también contiene información sobre paquetes, servicios incluidos, adicionales, preguntas frecuentes y criterios de scoring utilizados en el proceso comercial.

### 3. Análisis y cualificación del cliente mediante IA

El sistema procesa la información de cada solicitud utilizando modelos de Inteligencia Artificial.

A partir de las respuestas del formulario, analiza las necesidades del solicitante y determina características relevantes para su clasificación comercial.

Entre los datos contemplados se encuentran:

- Tipo de cliente.
- Tipo de aplicación solicitada.
- Necesidades del proyecto.
- Prioridad comercial.
- Presupuesto orientativo.
- Plazo estimado de desarrollo.

Esta información permite estructurar la oportunidad comercial y preparar una respuesta adaptada a las necesidades del cliente.

### 4. Validación del correo electrónico

El flujo incorpora una etapa destinada a comprobar la validez de la dirección de correo electrónico proporcionada por el usuario.

Esta comprobación resulta importante para evitar que el sistema continúe el proceso de comunicación utilizando direcciones incorrectas.

El feedback docente identifica una mejora pendiente en esta parte: conectar la salida de validación con una decisión efectiva que permita detener el envío o generar una alerta cuando el correo no sea válido.

### 5. Detección de clientes existentes y duplicados

Antes de crear un nuevo registro, el sistema consulta la información almacenada en Notion para comprobar si el cliente ya existe.

Esta operación permite diferenciar entre nuevos contactos y clientes actuales.

La información obtenida se utiliza para determinar cómo debe gestionarse el registro y evitar duplicidades en el CRM.

### 6. Gestión del CRM en Notion

Notion actúa como espacio centralizado para organizar la información comercial.

El proyecto utiliza dos estructuras principales:

**CRM - AppNova Solution**

Base de datos destinada a almacenar información de los clientes, incluyendo:

- Nombre.
- Correo electrónico.
- Teléfono.
- Tipo de cliente.
- Proyectos relacionados.

**Proyectos - AppNovaSolution**

Base de datos destinada a organizar las oportunidades y proyectos asociados a cada cliente.

Se registran datos relacionados con:

- Nombre del proyecto.
- Cliente asociado.
- Tipo de aplicación.
- Idea o necesidad del proyecto.
- Funcionalidades solicitadas.
- Información comercial relacionada.

De esta manera, la información de contacto y las oportunidades de desarrollo quedan organizadas dentro de un mismo entorno de gestión.

### 7. Generación y envío de respuestas comerciales

Una vez procesada la solicitud, el sistema prepara una respuesta comercial personalizada mediante Gmail.

El correo incluye información relacionada con las necesidades detectadas, las características del proyecto y una orientación inicial sobre los servicios que podría necesitar el cliente.

En la demostración se observa una respuesta con información sobre funcionalidades, presupuesto orientativo, plazos de desarrollo y proceso de trabajo.

Esta automatización permite ofrecer una primera comunicación comercial sin tener que redactar manualmente cada respuesta.

### 8. Notificaciones internas mediante Slack

El sistema incorpora Slack como canal de comunicación interna.

Cuando se identifica una nueva oportunidad comercial, se genera una notificación con información relevante sobre el cliente y su proyecto.

Entre los datos comunicados se encuentran:

- Nombre del contacto.
- Correo electrónico.
- Teléfono.
- Tipo de cliente.
- Tipo de aplicación.
- Necesidad identificada.
- Presupuesto orientativo.
- Plazo estimado.

Esto permite que el equipo tenga conocimiento de las nuevas oportunidades sin necesidad de consultar continuamente el formulario o el CRM.

### 9. Gestión automatizada de errores

El proyecto incorpora un workflow independiente denominado Error Workflow.

Este flujo se activa mediante un Error Trigger cuando se produce un fallo en una ejecución del sistema.

Su funcionamiento contempla tres etapas:

1. **Error Trigger:** recibe la notificación de una ejecución fallida.
2. **Obtener datos de la ejecución:** recupera información relacionada con el proceso que ha generado el error.
3. **Extraer detalles del error:** procesa la información relevante para identificar qué ha ocurrido.
4. **Slack:** envía una alerta al responsable con información del fallo.

Esta estructura permite disponer de un mecanismo de supervisión y notificación independiente del flujo comercial principal.

## 🔄 Arquitectura e integración de herramientas

La solución utiliza n8n como núcleo de automatización y conecta diferentes herramientas para gestionar el proceso comercial de principio a fin.

| Herramienta | Función dentro del proyecto |
|---|---|
| **n8n** | Diseño, coordinación y ejecución de los flujos de automatización. |
| **Google Forms** | Recepción de solicitudes comerciales. |
| **Google Sheets** | Registro de respuestas y almacenamiento de información de referencia comercial. |
| **Inteligencia Artificial (LLM)** | Análisis de solicitudes y cualificación de oportunidades. |
| **Notion** | CRM de clientes y gestión de proyectos comerciales. |
| **Gmail** | Generación y envío de respuestas comerciales personalizadas. |
| **Slack** | Notificaciones internas y alertas de errores. |

### Esquema general

```text
             POTENCIAL CLIENTE
                    │
                    ▼
              GOOGLE FORMS
                    │
                    ▼
               AUTOMATIZACIÓN
                    n8n
                    │
                    ▼
             GOOGLE SHEETS
                    │
                    ▼
           ANÁLISIS MEDIANTE IA
                    │
          ┌─────────┴─────────┐
          ▼                   ▼
   CUALIFICACIÓN         VALIDACIÓN
    DEL CLIENTE         DEL EMAIL
          │                   │
          └─────────┬─────────┘
                    │
                    ▼
             CONSULTA EN NOTION
                    │
                    ▼
             GESTIÓN DEL CRM
                    │
              ┌─────┴─────┐
              ▼           ▼
           GMAIL        SLACK
              │           │
              ▼           ▼
        RESPUESTA      AVISO AL
        COMERCIAL      EQUIPO
              │
              ▼
        SEGUIMIENTO DEL
          CLIENTE Y
           PROYECTO


       FLUJO INDEPENDIENTE DE ERRORES

             ERROR TRIGGER
                    │
                    ▼
          DATOS DE EJECUCIÓN
                    │
                    ▼
          DETALLES DEL ERROR
                    │
                    ▼
             ALERTA EN SLACK
```

*Esquema conceptual de los procesos de captación, cualificación, gestión comercial y control de errores.*

## 🛠️ Tecnologías y herramientas

- Automatización de procesos con n8n.
- Inteligencia Artificial y modelos de lenguaje (LLM).
- Google Forms.
- Google Sheets.
- Notion y bases de datos CRM.
- Gmail.
- Slack.
- Validación y procesamiento de datos.
- Clasificación y cualificación de oportunidades comerciales.
- Gestión de errores mediante workflows independientes.

## 💡 Valor aportado

Este proyecto demuestra cómo la automatización y la Inteligencia Artificial pueden aplicarse a un proceso comercial completo, conectando herramientas de captación, análisis, almacenamiento y comunicación.

Entre los principales aspectos que se trabajan destacan:

- Automatización de la captación de clientes potenciales.
- Análisis de necesidades comerciales mediante IA.
- Clasificación y priorización de oportunidades.
- Centralización de contactos y proyectos en un CRM.
- Detección de clientes existentes.
- Generación de comunicaciones comerciales personalizadas.
- Notificaciones internas para el seguimiento de oportunidades.
- Gestión independiente de errores y alertas.
- Integración de diferentes herramientas dentro de un mismo proceso.

La solución permite transformar una solicitud recibida mediante un formulario en una oportunidad comercial organizada y preparada para su seguimiento.

## 📚 Aprendizajes

El desarrollo de este proyecto permite trabajar con diferentes conceptos relacionados con la automatización comercial y la Inteligencia Artificial:

- Diseño y estructuración de workflows complejos en n8n.
- Integración de formularios con procesos automatizados.
- Procesamiento y clasificación de información mediante LLM.
- Cualificación de clientes potenciales.
- Validación de datos y direcciones de correo electrónico.
- Detección de registros duplicados.
- Integración de Notion como CRM.
- Gestión de relaciones entre clientes y proyectos.
- Automatización de comunicaciones mediante Gmail.
- Integración de notificaciones mediante Slack.
- Diseño de workflows independientes para la gestión de errores.
- Recuperación y análisis de información de ejecuciones fallidas.

---

## 🎓 Evaluación y feedback docente

El proyecto recibió una valoración de **10,00 / 10**, acompañada de comentarios positivos y recomendaciones técnicas para mejorar la robustez del sistema.

### Valoración del profesor

> ¡Qué tal Ángel! ¡Trabajazo hombre!

<img width="481" height="339" alt="3" src="https://github.com/user-attachments/assets/282a1766-3caf-4b26-9e75-f5509277db1a" />


# 🤖 Automatización de pedidos y atención al cliente mediante Telegram

> Desarrollo de un sistema conversacional para automatizar la atención al cliente, la consulta de productos y la gestión de pedidos mediante Telegram, conectando diferentes servicios a través de n8n.

<p align="center">
  <a href="https://drive.google.com/file/d/1S0zr42I5SvT_qm6fOhfvbCaTrtB1CEK2/view?usp=sharing">
    <img src="https://drive.google.com/thumbnail?id=1S0zr42I5SvT_qm6fOhfvbCaTrtB1CEK2&sz=w1200" alt="Ver demostración completa del proyecto" width="85%">
  </a>
</p>

<p align="center">
  ▶️ <a href="https://drive.google.com/file/d/1S0zr42I5SvT_qm6fOhfvbCaTrtB1CEK2/view?usp=sharing"><strong>VER DEMOSTRACIÓN COMPLETA DEL PROYECTO</strong></a>
</p>

---

## 📌 Descripción del proyecto

Este proyecto consiste en desarrollar un sistema de automatización orientado a gestionar la atención al cliente y el proceso de compra de un negocio de distribución, utilizando un bot de Telegram como interfaz de comunicación.

La solución conecta diferentes herramientas y fuentes de información mediante **n8n**, permitiendo centralizar distintas operaciones comerciales en una experiencia conversacional.

A través del bot, el usuario puede interactuar con el sistema, consultar información sobre productos, conocer promociones, resolver dudas y realizar un pedido sin necesidad de gestionar cada operación manualmente.

El flujo integra información almacenada en hojas de cálculo y documentos, además de servicios de correo electrónico para completar determinadas operaciones.

El objetivo es demostrar cómo se pueden combinar herramientas de automatización e integración de servicios para construir un proceso de atención y gestión comercial más organizado.

## 🎯 Objetivos

- Automatizar las consultas habituales de los clientes.
- Facilitar el acceso al catálogo de productos y sus precios.
- Proporcionar información sobre promociones y descuentos.
- Guiar al cliente durante el proceso de realización de pedidos.
- Recopilar los datos necesarios para gestionar las entregas.
- Incorporar la comprobación de cupones mediante imágenes.
- Automatizar el envío de confirmaciones por correo electrónico.
- Centralizar la lógica del proceso mediante flujos de n8n.

## ⚙️ Funcionamiento del sistema

El proyecto reúne diferentes funcionalidades dentro de un mismo entorno conversacional.

### 1. Interacción mediante Telegram

Telegram actúa como canal de comunicación entre el cliente y el sistema.

El usuario puede iniciar una conversación con el bot y acceder a las diferentes opciones disponibles mediante mensajes y respuestas automatizadas.

### 2. Registro y recopilación de datos

El sistema contempla un proceso de recogida de información del cliente, incluyendo datos necesarios para identificarlo y gestionar la entrega del pedido.

### 3. Consulta de productos y catálogo

El bot permite consultar información comercial sobre los productos disponibles.

Se muestran datos relacionados con los productos, sus formatos y precios, facilitando que el cliente pueda conocer la oferta antes de realizar una compra.

### 4. Información sobre promociones

El sistema proporciona información sobre las promociones y descuentos disponibles, permitiendo al cliente conocer las ofertas aplicables.

### 5. Gestión del proceso de compra

El usuario puede seleccionar los productos que desea adquirir e indicar las cantidades correspondientes.

El flujo permite organizar la información del pedido y presentar el importe correspondiente antes de continuar con su confirmación.

### 6. Comprobación de cupones mediante imágenes

El proyecto contempla la recepción de fotografías de cupones para realizar su comprobación dentro del proceso de compra.

Esta funcionalidad permite incorporar información visual al flujo de automatización.

### 7. Atención mediante preguntas frecuentes

El bot también permite resolver consultas habituales relacionadas con el servicio.

Para ello, se utiliza información documentada que sirve como referencia para responder a las preguntas de los clientes.

### 8. Confirmación del pedido

Una vez completado el proceso, el sistema contempla la confirmación de la operación y el envío de un correo electrónico con el resumen del pedido.

De esta forma, la interacción no se limita a proporcionar información, sino que conecta diferentes etapas del proceso comercial.

## 🔄 Arquitectura e integración de herramientas

La solución utiliza n8n como núcleo de automatización, conectando el canal de comunicación con diferentes fuentes de información y servicios.

| Herramienta | Función dentro del proyecto |
|---|---|
| **n8n** | Diseño y ejecución de los flujos de automatización. |
| **Telegram** | Interfaz conversacional para la interacción con el cliente. |
| **Google Sheets** | Gestión de información comercial y datos utilizados en el proceso. |
| **Google Docs** | Documentación de información y preguntas frecuentes. |
| **Gmail** | Envío de confirmaciones y comunicaciones por correo electrónico. |

### Esquema general

```text
             CLIENTE
                │
                ▼
             TELEGRAM
                │
                ▼
          AUTOMATIZACIÓN
               n8n
                │
       ┌────────┼─────────┐
       │        │         │
       ▼        ▼         ▼
   GOOGLE    GOOGLE     GMAIL
   SHEETS    DOCS
       │        │         │
       └────────┼─────────┘
                │
                ▼
       GESTIÓN DEL PEDIDO
                │
                ▼
        CONFIRMACIÓN AL
             CLIENTE
```

*Esquema conceptual de las herramientas que intervienen en la solución.*

## 🛠️ Tecnologías y herramientas

- Automatización de procesos con n8n.
- Integración con Telegram.
- Gestión de información mediante Google Sheets.
- Consulta de documentación con Google Docs.
- Integración de correo electrónico mediante Gmail.
- Procesamiento de información y gestión de flujos.
- Interacción conversacional mediante bot.

## 💡 Valor aportado

Este proyecto permite explorar cómo la automatización puede aplicarse a procesos habituales de un negocio, conectando diferentes herramientas para facilitar la atención al cliente y la gestión de pedidos.

Entre los principales aspectos que se trabajan destacan:

- Centralización de diferentes operaciones comerciales.
- Automatización de consultas frecuentes.
- Integración de distintas fuentes de información.
- Organización del proceso de compra.
- Incorporación de información visual al flujo.
- Automatización de comunicaciones con el cliente.

## 📚 Aprendizajes

El desarrollo de este proyecto permite trabajar con diferentes conceptos relacionados con la automatización:

- Diseño y estructuración de workflows en n8n.
- Integración de servicios externos.
- Comunicación mediante bots de Telegram.
- Conexión con fuentes de información externas.
- Organización de procesos comerciales.
- Automatización de operaciones y notificaciones.
- Diseño de flujos conversacionales.


---

## 🎓 Evaluación y feedback docente

El proyecto recibió una valoración de **9,50 / 10**, acompañada de comentarios positivos sobre la implementación y la lógica de negocio aplicada.

### Valoración del profesor

> Muy buen trabajo. El asistente está muy completo.

<img width="481" height="266" alt="1" src="https://github.com/user-attachments/assets/f8ec60a9-7ecd-4b09-94ea-706aff6f8205" />



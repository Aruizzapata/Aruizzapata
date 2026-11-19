
# 📊 Sistema automatizado de gestión y conciliación de facturas mediante IA

> Desarrollo de una solución de automatización financiera capaz de recibir facturas, extraer información mediante Inteligencia Artificial, comprobar su correspondencia con movimientos bancarios y registrar los resultados del proceso mediante n8n.

<p align="center">
  <a href="https://drive.google.com/file/d/1i-OlOQbeVDwC87KgK49oCbvzGXvAKIi6/view?usp=sharing">
    <img src="https://drive.google.com/thumbnail?id=1i-OlOQbeVDwC87KgK49oCbvzGXvAKIi6&sz=w1200" alt="Ver demostración completa del proyecto" width="85%">
  </a>
</p>

<p align="center">
  ▶️ <a href="https://drive.google.com/file/d/1i-OlOQbeVDwC87KgK49oCbvzGXvAKIi6/view?usp=sharing"><strong>VER DEMOSTRACIÓN COMPLETA DEL PROYECTO</strong></a>
</p>

---

## 📌 Descripción del proyecto

Este proyecto consiste en desarrollar un sistema automatizado de gestión financiera orientado a simplificar el procesamiento de facturas y su conciliación con movimientos bancarios.

La solución permite recibir documentos mediante un formulario web y procesarlos automáticamente a través de un workflow desarrollado en n8n.

Una vez recibida una factura, el sistema almacena el documento en Google Drive, identifica su formato y utiliza diferentes herramientas de Inteligencia Artificial para extraer la información relevante.

El procesamiento contempla tanto documentos PDF como imágenes, adaptando el método de extracción al tipo de archivo recibido.

La información obtenida se somete a comprobaciones para verificar que los datos necesarios estén disponibles y puedan utilizarse durante el proceso de conciliación.

Posteriormente, el sistema consulta los movimientos bancarios registrados en Google Sheets y comprueba si existe correspondencia entre los datos de la factura y las operaciones bancarias.

El resultado permite identificar facturas conciliadas, operaciones pendientes, documentos con información incompleta y situaciones que requieren una revisión adicional.

Además, se incorpora un mecanismo de control financiero que detecta facturas cuyo importe supera un umbral establecido de 1.000 €, generando una alerta automática mediante Slack.

Finalmente, el sistema registra los resultados en una hoja de auditoría y organiza los documentos en diferentes carpetas de Google Drive según su estado y resultado del procesamiento.

El objetivo es construir un proceso automatizado que combine extracción documental, Inteligencia Artificial, conciliación bancaria y control de operaciones financieras.

## 🎯 Objetivos

- Automatizar la recepción de facturas mediante un formulario web.
- Admitir documentos en formato PDF e imágenes.
- Almacenar automáticamente los documentos recibidos.
- Identificar el formato de cada archivo.
- Extraer información de las facturas mediante Inteligencia Artificial.
- Obtener datos como proveedor, número de factura, fecha e importe.
- Validar que la información extraída esté completa.
- Consultar movimientos bancarios almacenados en Google Sheets.
- Comprobar coincidencias entre facturas y movimientos bancarios.
- Identificar facturas conciliadas y operaciones pendientes.
- Detectar documentos ilegibles o con información incompleta.
- Generar alertas cuando se superen determinados umbrales financieros.
- Registrar los resultados y las incidencias del procesamiento.
- Organizar automáticamente los documentos en Google Drive.
- Incorporar un workflow independiente para gestionar errores.

## ⚙️ Funcionamiento del sistema

El proyecto reúne diferentes etapas dentro de un proceso automatizado de gestión y conciliación de facturas.

### 1. Recepción de facturas mediante formulario web

El proceso comienza con un formulario web denominado Gestión de facturas.

Desde esta interfaz, el usuario puede seleccionar y enviar un documento para iniciar su análisis y conciliación bancaria.

El formulario permite incorporar archivos para su procesamiento sin necesidad de acceder directamente a los workflows de n8n.

Esta interfaz constituye el punto de entrada del sistema y facilita la utilización de la solución por parte de usuarios que no necesitan conocimientos técnicos.

### 2. Almacenamiento y preparación de documentos

Una vez recibido el archivo, n8n inicia el flujo de automatización.

El documento se almacena en Google Drive, dentro de la estructura destinada a las facturas recibidas.

Posteriormente, el sistema recupera el archivo y prepara la información necesaria para continuar con su procesamiento.

También se registra un identificador del archivo para mantener la referencia del documento durante las diferentes etapas del workflow.

### 3. Identificación del formato y procesamiento documental

El sistema incorpora una lógica de clasificación que permite diferenciar el tipo de documento recibido.

Mediante un nodo Switch, se establecen diferentes rutas de procesamiento según el formato del archivo.

Se contemplan dos vías principales:

**Documentos PDF**

Los archivos PDF se procesan mediante una herramienta de extracción de contenido, que permite recuperar el texto y la información contenida en el documento.

**Imágenes**

Las fotografías de facturas se procesan mediante un nodo de análisis de imágenes basado en Inteligencia Artificial.

Esta separación permite adaptar el procesamiento documental al formato de entrada.

También se contempla una ruta para gestionar extensiones no admitidas.

### 4. Extracción de información mediante Inteligencia Artificial

Una vez obtenido el contenido del documento, el sistema utiliza un componente de extracción de información para identificar los datos relevantes de la factura.

Entre los campos que se trabajan se encuentran:

- Fecha de emisión.
- Número de factura.
- Proveedor.
- Importe.
- Información necesaria para la conciliación.

El workflow incorpora un modelo de lenguaje como soporte para el proceso de extracción y estructuración de los datos.

La información obtenida se prepara para que pueda utilizarse en las comprobaciones posteriores.

### 5. Validación de los datos extraídos

Antes de continuar con la conciliación, el sistema comprueba si la información necesaria está disponible.

Se contempla una bifurcación para diferenciar entre documentos con datos completos y documentos que presentan información incompleta.

Esta validación permite evitar que una factura con datos insuficientes continúe por el mismo recorrido que un documento correctamente procesado.

En caso de detectar problemas, se prepara la información correspondiente para su registro y clasificación.

### 6. Consulta de movimientos bancarios

Cuando los datos de la factura están disponibles, el sistema consulta la hoja de cálculo que contiene los movimientos bancarios.

Google Sheets actúa como fuente de información para realizar las comprobaciones relacionadas con las operaciones financieras.

El proceso recupera los movimientos disponibles y busca posibles coincidencias con la información extraída de la factura.

### 7. Conciliación bancaria

El sistema comprueba si existe correspondencia entre los datos de la factura y los movimientos bancarios.

Entre los criterios utilizados se encuentran:

- Número de factura.
- Importe de la operación.

A partir de estas comprobaciones, el flujo identifica diferentes situaciones:

**Factura conciliada**

Se encuentra una correspondencia entre los datos de la factura y el movimiento bancario.

**Factura pendiente**

No se encuentra una coincidencia que permita confirmar la conciliación.

**Factura con información incompleta**

El documento no contiene todos los datos necesarios para completar las comprobaciones.

**Factura que requiere revisión**

Se detectan situaciones que necesitan una comprobación adicional, como documentos ilegibles o importes que superan el umbral establecido.

### 8. Control de importes y alertas financieras

El proyecto incorpora una regla de control financiero para identificar facturas cuyo importe supera los 1.000 €.

Cuando se detecta una operación que supera este umbral, el sistema genera una notificación mediante Slack.

La alerta incluye información relevante para facilitar la identificación de la operación:

- Proveedor.
- Número de factura.
- Importe detectado.
- Umbral de alerta.
- Acción recomendada.

Esta funcionalidad permite identificar operaciones de mayor importe que pueden requerir una revisión adicional.

### 9. Registro de resultados y auditoría

Una vez procesada la factura, el sistema normaliza los datos obtenidos y registra el resultado en una hoja de auditoría de Google Sheets.

El registro contempla información como:

- Fecha y hora.
- Número de factura.
- Proveedor.
- Importe.
- Resultado del procesamiento.
- Detalle de la operación.

Este registro permite conservar un historial de las facturas procesadas y consultar posteriormente el resultado de cada operación.

### 10. Organización automática de documentos en Google Drive

El proceso finaliza organizando los documentos según el resultado de su procesamiento.

La estructura de almacenamiento contempla diferentes carpetas:

- **FACTURAS_ENTRADA:** recepción inicial de documentos.
- **FACTURAS_REVISADAS:** documentos procesados y clasificados para su revisión o seguimiento.
- **FACTURAS_ERROR:** documentos que presentan problemas durante el procesamiento.
- **FACTURAS_EXTENSIONES_NO_ADMITIDAS:** archivos cuyo formato no está contemplado por el sistema.

Esta organización permite mantener separadas las facturas según su situación y facilita su posterior localización.

### 11. Gestión automatizada de errores

El proyecto incorpora un workflow independiente denominado Workflow Error.

Este flujo utiliza un disparador de errores para detectar fallos durante las ejecuciones de la automatización.

Cuando se produce una incidencia, el sistema normaliza la información del error y prepara una notificación mediante Slack.

De esta manera, el proceso cuenta con un mecanismo independiente para comunicar problemas y facilitar su identificación.

## 🔄 Arquitectura e integración de herramientas

La solución utiliza n8n como núcleo de automatización y conecta diferentes servicios para gestionar el procesamiento documental y las operaciones financieras.

| Herramienta | Función dentro del proyecto |
|---|---|
| **n8n** | Diseño, coordinación y ejecución de los workflows. |
| **Formulario web de n8n** | Recepción de facturas para su procesamiento. |
| **Google Drive** | Almacenamiento y clasificación de documentos. |
| **Google Sheets** | Registro financiero, consulta de movimientos bancarios y auditoría. |
| **Inteligencia Artificial (LLM)** | Análisis de imágenes y extracción estructurada de información. |
| **OpenRouter Chat Model** | Modelo de lenguaje utilizado en el proceso de extracción. |
| **Slack** | Notificaciones y alertas financieras. |

### Workflows y procesos desarrollados

El proyecto contempla dos flujos diferenciados:

| Workflow | Responsabilidad |
|---|---|
| **Workflow principal** | Recepción, procesamiento, extracción de información, conciliación bancaria, registro y clasificación de facturas. |
| **Workflow Error** | Detección de errores, normalización de información y envío de alertas mediante Slack. |

### Esquema general

```text
              USUARIO
                 |
                 v
          FORMULARIO WEB
          GESTIÓN DE FACTURAS
                 |
                 v
             n8n FORM
                 |
                 v
          GOOGLE DRIVE
          ALMACENAR FACTURA
                 |
                 v
          RECUPERAR ARCHIVO
                 |
                 v
          IDENTIFICAR FORMATO
                 |
          +------+------+
          |             |
          v             v
       PDF             IMAGEN
          |             |
          v             v
    EXTRAER TEXTO   ANALIZAR IMAGEN
          |             |
          +------+------+
                 |
                 v
       EXTRACCIÓN MEDIANTE IA
                 |
                 v
         VALIDAR DATOS
                 |
          +------+------+
          |             |
          v             v
      COMPLETOS     INCOMPLETOS
          |             |
          v             v
    BUSCAR MOVIMIENTO  REGISTRAR
       BANCARIO       INCIDENCIA
          |
          v
    COMPROBAR COINCIDENCIA
          |
          v
      CONCILIACIÓN
          |
     +----+---------+
     |              |
     v              v
  CONCILIADO      PENDIENTE
     |              |
     +------+-------+
            |
            v
      CONTROL DE IMPORTE
            |
       +----+------+
       |           |
       v           v
    NORMAL      SUPERIOR
    AL UMBRAL   A 1.000 €
       |           |
       |           v
       |       ALERTA SLACK
       |           |
       +-----+-----+
             |
             v
       REGISTRO AUDITORÍA
        GOOGLE SHEETS
             |
             v
       CLASIFICACIÓN FINAL
             |
       +-----+------+
       |            |
       v            v
 FACTURAS       FACTURAS
 REVISADAS      ERROR
```

*Esquema conceptual del procesamiento documental, conciliación bancaria y control financiero.*

## 🛠️ Tecnologías y herramientas

- Automatización de procesos con n8n.
- Inteligencia Artificial y modelos de lenguaje (LLM).
- OpenRouter Chat Model.
- Análisis de imágenes.
- Extracción de información de documentos PDF.
- Procesamiento documental.
- Formularios web de n8n.
- Google Drive.
- Google Sheets.
- Slack.
- Conciliación bancaria mediante comprobación de datos.
- Registro y auditoría de operaciones financieras.
- Gestión automatizada de errores.

## 💡 Valor aportado

Este proyecto demuestra cómo la automatización y la Inteligencia Artificial pueden aplicarse a procesos administrativos y financieros que requieren procesar documentación, verificar información y mantener registros organizados.

Entre los principales aspectos que se trabajan destacan:

- Automatización de la recepción de facturas.
- Procesamiento de diferentes formatos documentales.
- Extracción de información mediante Inteligencia Artificial.
- Validación de datos antes de continuar el proceso.
- Comprobación de coincidencias entre facturas y movimientos bancarios.
- Identificación de operaciones pendientes de conciliación.
- Detección de importes que requieren atención adicional.
- Generación automática de alertas financieras.
- Registro de resultados y auditoría.
- Organización documental mediante reglas automatizadas.
- Gestión independiente de errores.

La solución permite transformar un proceso que normalmente requiere revisar documentos, consultar movimientos bancarios y registrar resultados manualmente en un flujo de trabajo automatizado.

Además, la combinación de extracción documental, reglas de negocio y notificaciones permite mantener un mayor control sobre las operaciones procesadas.

## 📚 Aprendizajes

El desarrollo de este proyecto permite trabajar con diferentes conceptos relacionados con la Inteligencia Artificial, la automatización documental y los procesos financieros:

- Diseño de workflows complejos en n8n.
- Creación de formularios de entrada de documentos.
- Integración con Google Drive.
- Procesamiento de documentos PDF e imágenes.
- Extracción estructurada de información mediante IA.
- Integración de modelos de lenguaje.
- Validación y normalización de datos.
- Diseño de reglas de conciliación bancaria.
- Consulta y actualización de hojas de cálculo.
- Aplicación de umbrales y reglas de control financiero.
- Registro de auditoría.
- Organización automática de documentos.
- Integración de notificaciones mediante Slack.
- Diseño de workflows independientes para la gestión de errores.

---

## 🎓 Evaluación y feedback docente

> Gracias por tu trabajo espectacular de nuevo Ángel. Muy top!
<img width="472" height="97" alt="5" src="https://github.com/user-attachments/assets/89a6fb4c-2c72-471d-91b9-c42194bb970e" />




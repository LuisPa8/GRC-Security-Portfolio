# 🛡️ Laboratorio 01: Prevención de Fuga de Datos (DLP)

## 📋 Resumen Ejecutivo
Este laboratorio documenta el despliegue, configuración y validación de una solución corporativa de **Data Loss Prevention (DLP)** utilizando **ManageEngine Endpoint DLP** en un entorno controlado con **Windows 11 Pro** (VMware Workstation).

El proyecto simula la respuesta técnica a la fuga de Datos de Carácter Personal (PII) e información financiera (IBAN) a través de vectores críticos como dispositivos USB, servicios web no autorizados e impresiones.

---

## 🏛️ Mapeo Normativo y Marco GRC

| Control / Artículo | Marco de Cumplimiento | Aplicación Técnica en el Laboratorio |
| :--- | :--- | :--- |
| **Control A.8.12** | **ISO/IEC 27001:2022** | **Prevención de Fuga de Datos:** Reglas de detección e intercepción en canales de salida. |
| **Control A.8.11** | **ISO/IEC 27001:2022** | **Enmascaramiento y Etiquetado:** Marcado e inyección de *Watermarks* dinámicos ("Confidencial") en impresión/PDF. |
| **Control A.8.10** | **ISO/IEC 27001:2022** | **Información en Medios Extraíbles:** Bloqueo de transferencia de archivos protegidos a memorias USB. |
| **Artículo 32** | **RGPD (UE 2016/679)** | **Seguridad del Tratamiento:** Medidas para garantizar la confidencialidad de PII (IBAN, DNI). |
| **[mp.si.5]** | **ENS (Esquema Nacional)** | **Protección de la Información:** Monitorización y prevención de salidas no autorizadas. |

---

## ⚙️ Configuración de Directivas y Estrategia Híbrida

Para mitigar el riesgo operacional sin interrumpir el negocio, se implementó una estrategia por fases:

1. **Web Apps & Navegadores (`Sólo Auditoría`):**
   - Cobertura: *Chrome, Edge, Firefox, Brave*.
   - Objetivo: Crear una línea base del tráfico web y analizar intentos de subida de archivos sensibles previo a aplicar un bloqueo estricto.
2. **Dispositivos Extraíbles USB (`Bloqueo Activo`):**
   - Intercepción automática ante cualquier intento de copia de archivos clasificados como PII/Confidencial hacia almacenamiento externo.
3. **Impresoras Local/Red (`Bloqueo + Marca de Agua`):**
   - Cancelación de trabajos de impresión no autorizados e inyección de la marca de agua dinámicamente (`Watermark: "Confidencial"`) en impresiones permitidas de fuentes de confianza.

---

## 📸 Evidencias de Validación

### 1. Panel de Directivas de Prevención
![Matriz de Directivas](./captura-directivas.png)
*Figura 1: Configuración de controles sobre navegadores, USB e impresoras en ManageEngine Endpoint DLP.*

### 2. Notificación de Bloqueo en Endpoint (Windows 11)
![Alerta de Bloqueo](./captura-bloqueo-user.png)
*Figura 2: Intercepción en tiempo real del agente DLP impidiendo la salida de datos sensibles.*

### 3. Registro de Auditoría e Incidentes
![Logs de Seguridad](./captura-logs-auditoria.png)
*Figura 3: Consola centralizada con el registro del evento de fuga para trazabilidad y respuesta a incidentes.*

---

## 💡 Lecciones Aprendidas & Criterio GRC
- **Transición Operativa:** El flujo de despliegue requiere monitorear la transición desde el estado *Pendiente de aplicarse (0%)* hasta *100% Implementada* tras la sincronización del agente.
- **DLP vs. IRM:** Se distingue el alcance de la tecnología **DLP** (centrada en mitigar la exfiltración en canales de salida/tránsito) frente a **IRM/DRM** (enfocada en el etiquetado persistente y marcas de agua en reposo/pantalla, abordada en el **Laboratorio 02**).

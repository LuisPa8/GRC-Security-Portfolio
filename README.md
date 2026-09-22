# 🛡️ Portafolio Práctico de Ciberseguridad & GRC

Bienvenido a mi repositorio central de laboratorios técnicos y evidencias de seguridad. Este espacio está diseñado para demostrar la **aplicación técnica real y la implementación de controles de seguridad** alineados con los principales marcos de cumplimiento y normativas internacionales (**ISO/IEC 27001**, **ENS**, **RGPD**, **TISAX** e **ISO/IEC 42001**).

---

## 📌 Índice de Laboratorios & Mapeo Normativo

| 01 | [**DLP** (Data Loss Prevention)](./01-dlp-lab) | Inspección de PII, control de canales de exfiltración (USB, portapapeles) y alertas. | **ISO 27001** (A.8.12)<br>**RGPD** (Art. 32)<br>**ENS** ([mp.si.5]) | 🟡 *En Proceso* |
| 02 | [**IRM** (Information Rights Mgmt)](./02-irm-lab) | Clasificación de información, etiquetado de documentos y control de derechos de acceso. | **ISO 27001** (A.5.12, A.5.13)<br>**TISAX** (Confidencialidad) | ⚪ *Planificado* |
| 03 | [**Full-Disk Encryption**](./03-disk-encryption-lab) | Cifrado de disco (BitLocker/LUKS) y gestión segura de claves de recuperación. | **ISO 27001** (A.8.24)<br>**RGPD** (Art. 32 - Cifrado)<br>**ENS** ([mp.eq.1]) | ⚪ *Planificado* |
| 04 | [**Backups** (Copias de Seguridad)](./04-backup-lab) | Políticas de respaldo (regla 3-2-1), cifrado de copias y pruebas de restauración. | **ISO 27001** (A.8.13)<br>**ENS** ([op.acc.4]) | ⚪ *Planificado* |
| 05 | [**IDS/IPS** (Detección/Prevención)](./05-ids-ips-lab) | Monitorización de red, detección de firmas de intrusión y reglas de bloqueo automático. | **ISO 27001** (A.8.16, A.8.20)<br>**ENS** ([mp.if.2]) | ⚪ *Planificado* |
| 06 | [**VPN** (Acceso Remoto Seguro)](./06-vpn-lab) | Despliegue de túneles cifrados con autenticación multifactor (MFA) para teletrabajo. | **ISO 27001** (A.8.20, A.8.21)<br>**ENS** ([mp.com.2]) | ⚪ *Planificado* |
| 07 | [**XDR** (Extended Detection & Response)](./07-xdr-lab) | Monitorización avanzada de endpoints, telemetría y respuesta automatizada ante amenazas. | **ISO 27001** (A.8.7, A.8.16)<br>**ENS** ([op.exp.1]) | ⚪ *Planificado* |
| 08 | [**SIEM** (Gestión de Eventos y Logs)](./08-siem-lab) | Centralización de logs, correlación de eventos de seguridad y cuadro de mando de alertas. | **ISO 27001** (A.8.15)<br>**ENS** ([op.exp.2]) | ⚪ *Planificado* |
| 09 | [**Hardening** (Bastionado de Sistemas)](./09-hardening-lab) | Aplicación de baselines de seguridad (CIS Benchmarks / CCN-CERT) en Windows/Linux. | **ISO 27001** (A.8.9)<br>**ENS** ([mp.eq.1], [mp.sw.1]) | ⚪ *Planificado* |
| 10 | [**Despliegue de Firewall**](./10-firewall-lab) | Segmentación de red, reglas de filtrado de tráfico inbound/outbound y DMZ. | **ISO 27001** (A.8.20, A.8.22)<br>**ENS** ([mp.if.1]) | ⚪ *Planificado* |

---

## 🛠️ Entorno de Laboratorio Habitual
- **Hipervisor:** VMware Workstation / VirtualBox.
- **Sistemas Operativos:** Windows Server, Windows 11 Enterprise, Ubuntu Linux / Kali Linux.
- **Herramientas de Análisis:** PowerShell, Python, SQL, Wireshark, Nmap, Power BI.

---

## 👤 Contacto & Perfil
- **Autor:** Luis Pascual Rodríguez
- **Rol:** Consultor GRC & Cybersecurity Specialist
- **Ubicación:** Ourense, España
- 🔗 **LinkedIn:** [Perfil Profesional](https://www.linkedin.com) *(reemplaza con tu enlace)*

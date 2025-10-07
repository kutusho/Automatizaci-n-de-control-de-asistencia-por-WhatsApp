# Sistema Automatizado de Control de Asistencias con Google Apps Script

## 📘 Descripción General
Este proyecto automatiza el **control de asistencias** del personal mediante **Google Apps Script**, **Google Sheets** y **WhatsApp Cloud API**.  
Desarrollado originalmente por **Iván Díaz** para mejorar la gestión de horarios, notificaciones automáticas y reportes quincenales.

El sistema permite registrar entradas y salidas con ubicación, generar reportes quincenales, enviar alertas de retrasos y notificar a empleados de forma automatizada.

---

## ⚙️ Tecnologías Utilizadas
- Google Apps Script (JavaScript)
- Google Sheets API
- WhatsApp Cloud API (Meta Graph v23.0)
- GmailApp y MailApp (para notificaciones por correo)
- CacheService y Script Properties

---

## 🧩 Funcionalidades Principales
✅ Registro automático de **entradas** y **salidas** vía WhatsApp  
✅ Validación de ubicación (georreferencia mediante Haversine)  
✅ Control de **retrasos** con tolerancia configurable  
✅ **Reportes quincenales** por WhatsApp y correo electrónico  
✅ **Alertas automáticas** por acumulación de retrasos  
✅ Registro de **vacaciones** para excluir días del cálculo  
✅ Módulos de **estadísticas y nómina** automatizada

---

## 📁 Estructura del Proyecto
```
/Automatizacion_WA.gs
/appsscript.json
/README.md
/link.txt  ← contiene el enlace al proyecto original
```

---

## 🔑 Variables de Entorno (Script Properties)
| Nombre | Descripción |
|--------|--------------|
| SPREADSHEET_ID | ID de la hoja de cálculo principal |
| PHONE_NUMBER_ID | ID del número de WhatsApp Business API |
| ACCESS_TOKEN | Token de acceso a la API de WhatsApp |
| VERIFY_TOKEN | Token de verificación del webhook |
| REPORT_TO_NUMBERS | Lista de números que recibirán reportes |
| REPORT_TO_EMAILS | Correos para los reportes quincenales |
| HOURLY_RATE | Tarifa por hora (MXN) |
| TIMEZONE | Zona horaria (ej. America/Mexico_City) |
| WORK1_LAT / WORK1_LNG / WORK1_RADIUS_M | Coordenadas del lugar de trabajo |
| AUTHORIZED_NUMBERS | Teléfonos autorizados para registrar asistencia |

---

## 🧠 Flujo General del Sistema
1. El empleado envía un mensaje de *“entrada”* o *“salida”* vía WhatsApp.  
2. El sistema solicita su **ubicación actual**.  
3. Se valida si está dentro del rango permitido.  
4. El registro se guarda automáticamente en Google Sheets.  
5. Se generan reportes quincenales y alertas automáticas.

---

## 🧾 Créditos y Licencia
Proyecto desarrollado por **Iván de Jesús Díaz Navarro**  
Licencia: MIT © 2025

---

## 🔗 Enlace al Proyecto en Google Apps Script
Consulta la versión activa en:  
👉 [Script original en Google Apps Script](https://script.google.com/d/1ekPmfGbzARnHkKoeaMKNA8inPO3AMO4DAuCJgtyahy04ZG78h8SYhxXB/edit?usp=sharing)

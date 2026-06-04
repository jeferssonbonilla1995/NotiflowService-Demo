# 📱 NotiflowService - Demo Visual

## Sistema de Notificaciones Push | Monitoreo SRI | Integración Microplus | Gestión de Usuarios

---

## 🎯 ¿Qué es NotiflowService?

**NotiflowService** es una plataforma completa de **notificaciones en tiempo real** y **monitoreo de documentos electrónicos del SRI** que permite:

- 📨 Recibir **notificaciones push** en tiempo real sobre el estado de documentos electrónicos
- 🧾 **Monitorear facturas, retenciones, guías y comprobantes** enviados al SRI
- 🔗 **Conexión directa con Microplus** (sistema contable) para sincronización automática
- 👥 Gestionar **usuarios y empresas** desde una app móvil
- 📊 Visualizar **métricas y estadísticas** del flujo documental

**✅ Aplicación móvil funcionando en Android (con soporte para iOS).**

---

## 🏗️ Arquitectura del Sistema
┌─────────────────┐ ┌─────────────────┐ ┌─────────────────┐
│ 📱 Frontend │────▶│ 🔧 Backend │────▶│ 🗄️ Base de │
│ (Flutter) │ │ (ASP.NET Core) │ │ Datos (SQL) │
└─────────────────┘ └─────────────────┘ └─────────────────┘
│ │ │
│ │ │
▼ ▼ ▼
Notificaciones API REST + Documentos
Push (FCM) SRI + Microplus SRI


---

## 📱 Frontend (Flutter)

### Tecnologías

| Tecnología | Propósito |
|------------|-----------|
| **Flutter** | Framework multiplataforma (Android/iOS/Windows) |
| **Dart** | Lenguaje de programación |
| **Firebase Cloud Messaging** | Notificaciones push |
| **Provider / Riverpod** | Gestión de estado |
| **SharedPreferences** | Almacenamiento local |
| **HTTP / Dio** | Comunicación con API |

### Pantallas principales

| Pantalla | Descripción |
|----------|-------------|
| **Login** | Autenticación de usuarios |
| **Dashboard** | Resumen de documentos SRI y notificaciones |
| **Documentos SRI** | Estado de facturas, retenciones, notas de crédito, guías |
| **Monitoreo** | Estado de documentos electrónicos SRI en tiempo real |
| **Configuración** | Creación de usuarios para ingresar a la app |

---

## 🔧 Backend (ASP.NET Core)

### Tecnologías

| Tecnología | Propósito |
|------------|-----------|
| **ASP.NET Core 8** | API RESTful |
| **Entity Framework Core** | ORM para base de datos |
| **JWT Authentication** | Autenticación segura |
| **Firebase Admin SDK** | Envío de notificaciones push |
| **Integración SRI** | Consulta de estado de comprobantes electrónicos |
| **Microplus API** | Sincronización contable |
| **SQL Server / PostgreSQL** | Base de datos |
| **Swagger/OpenAPI** | Documentación de API |



---

## 🧾 Módulo SRI - Documentos Electrónicos

| Tipo de documento | Qué monitorea |
|-------------------|---------------|
| **Facturas** | Estado: Autorizada, Rechazada, En proceso, No generado |
| **retenciones** | Estado de comprobantes de retención |
| **Guías de remisión** | Estado de autorización |
| **Notas de crédito/débito** | Estado de comprobantes |

**Notificaciones push cuando un documento no esta autorizado o no generado.**

---

## 🔗 Integración con Microplus

| Función | Cómo funciona |
|---------|----------------|
| **Sincronización automática** | Los documentos autorizados por el SRI se sincronizan con Microplus |
| **Actualización de estados** | Refleja en tiempo real el estado desde Microplus |



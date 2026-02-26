# Seguridad, IAM y Cumplimiento Normativo

Se implementa una arquitectura Zero Trust para garantizar la integridad y confidencialidad en todos los niveles de integración.

## Gestión de Identidad y Acceso (IAM)
- Autenticación: Basada en OpenID Connect (OIDC). Uso de Multi-Factor Authentication (MFA) para canales externos.
- Autorización: Uso de tokens JWT firmados con control de acceso basado en roles (RBAC) y atributos (ABAC).
- Seguridad Interna: mTLS entre microservicios gestionado a través de un Service Mesh (Istio).

## Seguridad de APIs
- Cumplimiento FAPI (Financial-grade API) para APIs expuestas a terceros.
- Rate Limiting, IP Whitelisting y validación estricta de esquemas en el API Gateway.

## Protección de Datos y Privacidad
- Encriptación: Datos sensibles (PII) encriptados en reposo (AES-256) y en tránsito (TLS 1.2+).
- Cumplimiento: Trazabilidad inmutable de accesos para auditorías regulatorias (GDPR/Protección de Datos locales).

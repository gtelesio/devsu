# Alta Disponibilidad y Recuperación ante Desastres

La plataforma está diseñada para satisfacer los niveles de servicio más exigentes de la banca moderna.

## Disponibilidad y Resiliencia
- Despliegue Multi-Región: Configuración Active-Active para lecturas y Active-Passive con replicación síncrona para escrituras críticas.
- Infraestructura: Orquestación mediante Kubernetes (AKS/EKS) con políticas de auto-escalado horizontal y recuperación automática.

## Recuperación ante Desastres (DR)
- RTO / RPO: Objetivos de tiempo y punto de recuperación mínimos mediante estrategias de replicación continua de datos y automatización de procesos de conmutación por error (failover).
- Chaos Engineering: Ejecución de pruebas de fallo controladas para validar los mecanismos de resiliencia.

## Observabilidad
- Implementación de OpenTelemetry para rastreo distribuido, logs centralizados y monitoreo proactivo del estado de salud de los servicios.

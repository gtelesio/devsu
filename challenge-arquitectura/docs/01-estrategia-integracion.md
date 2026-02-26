# Estrategia de Integración Multicore

La estrategia propuesta se basa en el modelo de Parallel Core Banking combinado con el patrón Strangler Fig para asegurar una transición sin riesgos.

## Coexistencia y Sincronización
El Core Legado y el Digital Core operan simultáneamente. Los productos nuevos se gestionan en el Core Digital, mientras que el historial se mantiene en el legado.

- Change Data Capture (CDC): Se utiliza Debezium para capturar cambios en el Core Legado en tiempo real y publicarlos en Kafka.
- Digital Integration Hub (DIH): Una capa de datos de ultra-baja latencia (Redis) consolida información de múltiples cores para consultas de lectura masivas.

## Patrones de Integración
1. Event-Driven Architecture (EDA): Uso de Apache Kafka para desacoplar sistemas y procesar transacciones de forma asíncrona.
2. API-First Approach: Diseño de contratos OpenAPI alineados con el estándar BIAN antes del desarrollo.
3. Capa de Adaptadores: Implementación de servicios especializados para la transformación de protocolos (ISO 8583 a REST/JSON).

# Auditoría

## Objetivo

Definir los mecanismos de auditoría interna y externa aplicables a Kronos-Vault.

## Tipos de auditoría

| Tipo | Frecuencia | Alcance |
|------|------------|---------|
| Interna documental | Semestral | Repositorio y documentación |
| Verificación técnica | Trimestral | Hashes y sellos |
| Auditoría externa | Cada 2 años | Estándar completo |
| Pentest | Anual | Landing e infraestructura |

## Auditoría interna documental

Verifica:

- Consistencia del `CHANGELOG.md`.
- Actualización de `registro/indice-publico.json`.
- Vigencia de términos y privacidad.
- Alineación con ISO 14721 e ISO 27001.

**Estado actual:** no realizada aún. Planificada para Q4 2026.

## Verificación técnica

Verifica:

- Integridad de archivos con `SHA256SUMS`.
- Vigencia de firmas GPG.
- Estado del certificado Safe Creative.
- Anclaje en blockchain.

**Estado actual:** verificable manualmente por cualquier tercero.

## Auditoría externa

Contratada a un tercero independiente para:

- Revisar la arquitectura de seguridad.
- Validar el modelo de gobernanza.
- Emitir informe público.

**Estado actual:** pendiente. Requiere presupuesto.

## Pentest

Realizado por especialista externo para:

- Probar la landing contra ataques comunes.
- Validar la ausencia de vulnerabilidades críticas.
- Emitir informe público.

**Estado actual:** pendiente. Requiere presupuesto.

## Registro de auditorías

Todo informe se publica en `evidencias/informes-auditoria/`.

Formato mínimo:

- Fecha.
- Auditor.
- Alcance.
- Hallazgos.
- Recomendaciones.
- Estado de remediación.

## Declaración de transparencia

Kronos-Vault declara abiertamente:

- Qué auditorías se han hecho.
- Qué auditorías están pendientes.
- Qué auditorías no se han presupuestado.

No se afirma certificación externa sin evidencia verificable.
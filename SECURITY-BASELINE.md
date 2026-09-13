# Baseline de Seguridad — Kronos-Vault

Nivel declarado: **Reforzado documentado** (no gubernamental).

## Controles activos

### Criptografía
- SHA-256 y SHA-512 para integridad.
- Sellado temporal cualificado (eIDAS / QTSA).
- Anclaje en blockchain Ethereum.

### Custodia
- Repositorio Git con historial inmutable.
- Registro público solo-adicionable.
- Hashes verificables públicamente.

### Gobernanza
- Separación de funciones documentada.
- Proceso de cambios público.
- Doble aprobación para cambios MAJOR (planificado).

### Operación
- Respuesta a incidentes en 48h.
- Divulgación responsable 90 días.
- Revisión de baseline cada 6 meses.

## Controles planificados (Fase 2)

- Firma GPG obligatoria de releases.
- SBOM automatizado.
- CI/CD con verificación de integridad.
- Almacenamiento WORM.
- MFA en cuentas críticas.

## Controles planificados (Fase 3)

- Pentest anual externo.
- Auditoría independiente cada 2 años.
- Certificación ISO 27001.

## Fuera de alcance

- Certificación ISO formal (requiere auditor pagado).
- Acreditación como autoridad de certificación.
- Nivel gubernamental específico.

## Declaración

Kronos-Vault declara lo que implementa. No declara lo que no puede demostrar. Esta es la base de un estándar serio.
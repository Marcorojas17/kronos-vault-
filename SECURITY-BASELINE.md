# Baseline de Seguridad — Kronos-Vault

Nivel declarado: **Reforzado documentado** (no gubernamental).

## Controles activos

### Criptografía
- SHA-256 y SHA-512 para integridad.
- Sellado temporal cualificado (eIDAS).
- Anclaje en Ethereum.

### Custodia
- Repositorio Git con historial inmutable.
- Tags firmados por versión.
- Registro público solo-adicionable.

### Gobernanza
- Separación de funciones documentada.
- Doble aprobación para cambios MAJOR.
- Proceso de cambios público.

### Operación
- Respuesta a incidentes en 48h.
- Divulgación responsable 90 días.
- Revisión de baseline cada 6 meses.

## Controles planificados (Fase 2)

- Firma GPG obligatoria de todos los releases.
- SBOM automatizado con Syft.
- CI/CD con GitHub Actions (verificación de integridad).
- Almacenamiento WORM en S3 con Object Lock.
- MFA en todas las cuentas críticas.
- Pentest anual externo.
- Auditoría independiente cada 2 años.

## Controles fuera de alcance

- Certificación ISO formal (requiere auditor externo pagado).
- Acreditación como autoridad de certificación.
- Nivel gubernamental específico (no aplicable a proyecto privado).

## Declaración

Kronos-Vault **declara lo que implementa**. No declara lo que no puede demostrar. Esta es la base de un estándar serio.
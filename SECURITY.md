# Política de Seguridad de Kronos-Vault

## Declaración

Kronos-Vault aplica una **arquitectura de seguridad reforzada**, defensa en profundidad, separación de funciones, almacenamiento inmutable y controles alineados con ISO 27001, ISO 14721, NIST CSF y prácticas de cadena de custodia digital.

**No afirma certificación externa ni nivel gubernamental específico.** Declara cumplimiento documentado de controles verificables.

## Alcance

Esta política cubre:

- Emisión y validación de sellos.
- Manejo de claves criptográficas.
- Custodia de registros.
- Respuesta ante incidentes.
- Continuidad del estándar.

## Reportar una vulnerabilidad

**Canal cifrado:** proyectokronos@hotmail.com (asunto: `[SECURITY]`)
**PGP:** disponible en `crypto/claves-publicas/`

**Compromiso de respuesta:**
- Acuse de recibo: 48 horas.
- Evaluación inicial: 7 días.
- Parche o mitigación: 30 días.

**Divulgación responsable:**
- No publique detalles antes de 90 días.
- Acredita al reportero si lo autoriza.

## Controles implementados hoy

| Control | Estado | Evidencia |
|---------|--------|-----------|
| Hash SHA-256/512 | ✅ Activo | `index.html`, `registro/` |
| Sellado temporal externo | ✅ Activo | Safe Creative `2607146379465` |
| Anclaje blockchain | ✅ Activo | Ethereum, tx pública |
| Registro solo-adicionable | ✅ Activo | Git history + tags |
| Firma GPG de releases | ⚠️ Planificado | `crypto/` |
| Separación de funciones | ✅ Documentado | `gobernanza/` |
| Respuesta a incidentes | ✅ Documentado | `docs/respuesta-incidentes.md` |
| Auditoría externa | ❌ Pendiente | Presupuesto requerido |
| Pentest | ❌ Pendiente | Presupuesto requerido |
| MFA | ❌ Pendiente | Fase 2 |

## Contacto

**Email:** proyectokronos@hotmail.com
**Email legal:** marco.a.rojas.v@hotmail.com
**WhatsApp:** +52 722 586 2335
**PGP Fingerprint:** *(se publica al generar la clave)*
# Cadena de Custodia Digital

## Principio

Toda obra registrada en Kronos-Vault mantiene una **cadena de custodia verificable** desde su creación hasta su validación final. Cualquier ruptura invalida el sello.

## Fases de la cadena
Este estándar define:

1. Creación (titular) →
2. Hash local (navegador) →
3. Firma GPG (emisor) →
4. Sello temporal (Safe Creative) →
5. Sello cualificado (Firmaprofesional) →
6. Anclaje blockchain (Ethereum) →
7. Registro público (GitHub) →
8. Verificación (cualquier tercero)


## Evidencia por fase

| Fase | Evidencia |
|------|-----------|
| Creación | Declaración del titular |
| Hash local | SHA-256 + SHA-512 |
| Firma GPG | Fingerprint público |
| Sello temporal | Token RFC 3161 (interno) |
| Sello cualificado | Token RFC 3161 (QTSA) |
| Anclaje blockchain | tx hash + URL Etherscan |
| Registro público | Commit en GitHub |
| Verificación | Informe del tercero |

## Reglas de integridad

1. **Nunca se modifica** un sello emitido.
2. **Nunca se elimina** una entrada del registro público.
3. **Nunca se revoca** sin causal documentada.
4. **Nunca se altera** la historia de Git.

## Rupturas de cadena

Si se detecta una ruptura:

1. Se marca el sello como `revocado` en `registro/revocados.json`.
2. Se documenta la causal en `gobernanza/resoluciones/`.
3. Se notifica al titular en 7 días.
4. Se publica un comunicado si afecta a terceros.

## Verificación independiente

Cualquier tercero puede reconstruir la cadena con:

- El JSON del sello.
- El archivo original.
- El schema oficial.
- El token de sello temporal.
- La transacción en blockchain.

Ver [`procedimiento-validacion.md`](procedimiento-validacion.md).

## Referencias

- ISO 27037 — Guía para la identificación, recolección y preservación de evidencia digital.
- RFC 3161 — Time-Stamp Protocol.
- NIST SP 800-86 — Guide to Integrating Forensic Techniques.

# Política Criptográfica

## Algoritmos aprobados

| Uso | Algoritmo | Estado |
|-----|-----------|--------|
| Integridad | SHA-256 | ✅ Obligatorio |
| Integridad | SHA-512 | ✅ Obligatorio |
| Firma digital | Ed25519 (GPG) | ✅ Recomendado |
| Firma digital | RSA-4096 (GPG) | ✅ Alternativo |
| Cifrado en tránsito | TLS 1.3 | ✅ Obligatorio |
| Cifrado en reposo | AES-256-GCM | ⚠️ Planificado |
| Sello temporal | RFC 3161 (QTSA) | ✅ Activo |

## Algoritmos prohibidos

- MD5, SHA-1 (excepto compatibilidad histórica declarada).
- RSA < 2048 bits.
- DES, 3DES, RC4.
- Cualquier algoritmo no listado en NIST SP 800-175B.

## Ciclo de vida de claves

| Fase | Duración |
|------|----------|
| Generación | Al iniciar operación |
| Uso | 2 años máximo |
| Rotación | Anual recomendada |
| Revocación | Inmediata ante sospecha |
| Archivo | Permanente (solo clave pública) |

## Procedimiento de revocación

1. Emitir certificado de revocación firmado.
2. Publicar en `crypto/revocaciones/`.
3. Actualizar `registro/revocados/`.
4. Notificar a titulares afectados en 7 días.

Ver `gestion-de-claves.md`.
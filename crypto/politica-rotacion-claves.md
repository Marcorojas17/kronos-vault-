# Política de Rotación y Revocación de Claves

## Ciclo de vida

| Fase | Duración |
|------|----------|
| Generación | Al iniciar operación |
| Uso | 2 años máximo |
| Rotación | Anual recomendada |
| Revocación | Inmediata ante sospecha |
| Archivo | Permanente (solo clave pública) |

## Rotación programada

1. Generar nueva clave 60 días antes de expiración.
2. Firmar nueva clave con la antigua (transición).
3. Publicar en `crypto/claves-publicas/`.
4. Actualizar `checksums/SHA256SUMS.sig`.
5. Anunciar en `CHANGELOG.md`.

## Revocación de emergencia

Si la clave privada se compromete:

1. Activar certificado de revocación pre-generado.
2. Publicar en `crypto/revocaciones/`.
3. Revocar en keys.openpgp.org.
4. Emitir comunicado en README.
5. Re-firmar releases afectados con nueva clave.
6. Notificar a titulares en 7 días.

## Almacenamiento de claves privadas

- **Nunca** en este repositorio.
- **Nunca** en servicios en la nube sin cifrado.
- Recomendado: hardware token (YubiKey) o almacenamiento offline.
- Passphrase fuerte obligatoria.

## Contacto para verificación

**Email:** proyectokronos@hotmail.com
**Fingerprint público:** *(se publica al generar la clave)*
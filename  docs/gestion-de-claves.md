# Gestión de Claves

## Tipos de clave

| Clave | Uso | Custodia |
|-------|-----|----------|
| Maestra | Firmar releases | Offline, hardware |
| Subclave de firma | Firmar sellos | Offline, hardware |
| Subclave de cifrado | Comunicación | Hardware |
| Claves de titulares | Uso propio | Responsabilidad del titular |

## Generación

```bash
gpg --full-generate-key
# Algoritmo: Ed25519
# Uso: Firmar y certificar
# Expiración: 2 años

Publicación

Clave pública en:

· crypto/claves-publicas/kronos-publica.asc
· https://keys.openpgp.org
· Verificación: gpg --verify

Rotación

1. Generar nueva clave 60 días antes de expiración.
2. Firmar nueva clave con la antigua (transición).
3. Publicar en crypto/claves-publicas/.
4. Actualizar checksums/SHA256SUMS.sig.
5. Anunciar en CHANGELOG.md.

Revocación de emergencia

Si la clave privada se compromete:

1. Activar certificado de revocación pre-generado.
2. Publicar en crypto/revocaciones/.
3. Revocar en keys.openpgp.org.
4. Emitir comunicado en README y prensa.
5. Re-firmar releases afectados con nueva clave.

Contacto para verificación

Email: proyectokronos@hotmail.com
Fingerprint público: (se publica con la clave)


### 7. `.well-known/security.txt`

Contact: mailto:proyectokronos@hotmail.com
Contact: mailto:marco.a.rojas.v@hotmail.com
Expires: 2027-07-14T00:00:00.000Z
Encryption: https://github.com/Marcorojas17/kronos-vault/crypto/claves-publicas/kronos-publica.asc
Acknowledgments: https://github.com/Marcorojas17/kronos-vault/SECURITY.md
Preferred-Languages: es, en
Canonical: https://marcorojas17.github.io/kronos-vault/.well-known/security.txt
Policy: https://github.com/Marcorojas17/kronos-vault/SECURITY.md


### 8. `checksums/README.md` (guía de integridad)

```markdown
# Checksums y Firmas

## Propósito

Permitir a cualquier tercero verificar la integridad de los archivos publicados.

## Archivos

- `SHA256SUMS` — Hashes SHA-256 de todos los archivos del repo.
- `SHA256SUMS.sig` — Firma GPG del archivo anterior.

## Generación (por el autor)

```bash
find . -type f -not -path './.git/*' -exec sha256sum {} \; > checksums/SHA256SUMS
gpg --armor --detach-sign checksums/SHA256SUMS
mv checksums/SHA256SUMS.asc checksums/SHA256SUMS.sig

Frecuencia

· Se regenera en cada release.
· Se firma con la clave vigente.
· Se publica junto al tag correspondiente.



---

## 🔐 Paso crítico: genera tu clave GPG hoy

Sin esto, todo lo anterior es papel mojado. **15 minutos:**

```bash
# 1. Instalar GPG (si no lo tienes)
# Windows: https://gpg4win.org
# Mac: brew install gnupg
# Linux: sudo apt install gnupg

# 2. Generar clave
gpg --full-generate-key
# Selecciona: (9) ECC (sign and encrypt)
# Curva: Curve 25519
# Nombre: Marco Antonio Rojas Valdovinos
# Email: proyectokronos@hotmail.com
# Expiración: 2y
# Passphrase: fuerte

# 3. Exportar clave pública
gpg --armor --export proyectokronos@hotmail.com > kronos-publica.asc

# 4. Subir a keys.openpgp.org
# Ve a: https://keys.openpgp.org/upload
# Pega el contenido de kronos-publica.asc


# Checksums y Firmas

## Propósito

Permitir a cualquier tercero verificar la integridad de los archivos publicados.

## Archivos

- `SHA256SUMS` — Hashes SHA-256 de archivos críticos del repo.
- `SHA256SUMS.sig` — Firma GPG del archivo anterior.

## Generación (por el autor)

```bash
cd kronos-vault
find . -type f -not -path './.git/*' -exec sha256sum {} \; > checksums/SHA256SUMS
gpg --armor --detach-sign checksums/SHA256SUMS
mv checksums/SHA256SUMS.asc checksums/SHA256SUMS.sig

Verificación (por terceros)


# 1. Importar clave pública
gpg --import crypto/claves-publicas/kronos-publica.asc

# 2. Verificar firma
gpg --verify checksums/SHA256SUMS.sig checksums/SHA256SUMS

# 3. Verificar hashes
sha256sum -c checksums/SHA256SUMS

Estado actual

⚠️ Clave GPG aún no generada. Los checksums se publicarán al generarse la clave.

Frecuencia

· Se regenera en cada release.
· Se firma con la clave vigente.
· Se publica junto al tag correspondiente.

Referencias

· NIST FIPS 180-4 — Secure Hash Standard
· RFC 4880 — OpenPGP Message Format


---

## 📁 BLOQUE G — `schemas/` faltantes (4 archivos)

### G1. `schemas/obra.schema.json`

```json
{
  "$schema": "https://json-schema.org/draft/2020-12/schema",
  "$id": "https://kronos-vault.github.io/schemas/obra.schema.json",
  "title": "Obra",
  "description": "Describe una obra registrada en Kronos-Vault",
  "type": "object",
  "required": ["titulo", "tipo", "archivo", "tamano_bytes", "sha256", "sha512"],
  "additionalProperties": false,
  "properties": {
    "titulo": {
      "type": "string",
      "minLength": 1,
      "maxLength": 500
    },
    "tipo": {
      "type": "string",
      "enum": [
        "Literaria - Otros",
        "Literaria - Novela",
        "Literaria - Poesía",
        "Literaria - Ensayo",
        "Artística - Visual",
        "Artística - Musical",
        "Artística - Audiovisual",
        "Científica",
        "Arquitectónica",
        "Software",
        "Otros"
      ]
    },
    "archivo": {
      "type": "string",
      "minLength": 1,
      "maxLength": 255
    },
    "tamano_bytes": {
      "type": "integer",
      "minimum": 1
    },
    "sha256": {
      "type": "string",
      "pattern": "^[a-f0-9]{64}$"
    },
    "sha512": {
      "type": "string",
      "pattern": "^[a-f0-9]{128}$"
    },
    "sha1": {
      "type": "string",
      "pattern": "^[a-f0-9]{40}$"
    },
    "descripcion": {
      "type": "string",
      "maxLength": 2000
    },
    "fecha_creacion": {
      "type": "string",
      "format": "date"
    }
  }
}
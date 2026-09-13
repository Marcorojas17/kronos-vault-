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
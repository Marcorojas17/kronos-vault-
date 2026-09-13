# Claves Públicas

Este directorio contiene las claves públicas GPG vigentes de Kronos-Vault.

## Estado actual

⚠️ **Clave aún no generada.** El autor está en proceso de generación. Se publicará con:
- Algoritmo: Ed25519
- Expiración: 2 años
- Fingerprint: *(pendiente)*
- Publicación en: keys.openpgp.org

## Cómo verificar (una vez publicada)

```bash
gpg --import kronos-publica.asc
gpg --fingerprint proyectokronos@hotmail.com
gpg --verify checksums/SHA256SUMS.sig checksums/SHA256SUMS
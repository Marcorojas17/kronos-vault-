# Algoritmos Criptográficos Aprobados

## Algoritmos obligatorios

| Uso | Algoritmo | Norma |
|-----|-----------|-------|
| Integridad | SHA-256 | FIPS 180-4 |
| Integridad | SHA-512 | FIPS 180-4 |
| Firma digital | Ed25519 | RFC 8032 |
| Firma digital (alt) | RSA-4096 | PKCS#1 v2.2 |
| Cifrado en tránsito | TLS 1.3 | RFC 8446 |
| Sello temporal | RFC 3161 | QTSA eIDAS |

## Algoritmos prohibidos

- MD5, SHA-1 (excepto compatibilidad histórica declarada)
- RSA < 2048 bits
- DES, 3DES, RC4
- Cualquier algoritmo no listado en NIST SP 800-175B

## Algoritmos planificados (Fase 2)

| Uso | Algoritmo |
|-----|-----------|
| Cifrado en reposo | AES-256-GCM |
| Intercambio de claves | X25519 |
| Hash post-cuántico | SHA-3 (evaluación) |

## Referencias

- NIST SP 800-175B — Guideline for Using Cryptographic Standards
- RFC 8032 — Edwards-Curve Digital Signature Algorithm
- eIDAS — Reglamento (UE) 910/2014
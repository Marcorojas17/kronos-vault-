# Arquitectura de Seguridad

## Principios rectores

1. **Zero Trust** — Ninguna entidad es confiable por defecto.
2. **Defensa en profundidad** — Capas independientes de control.
3. **Mínimo privilegio** — Acceso solo al mínimo necesario.
4. **Separación de funciones** — Emisor ≠ validador ≠ auditor.
5. **Verificabilidad pública** — Cualquiera puede validar sin confiar.
6. **Inmutabilidad** — Registros solo-adicionables.
7. **Transparencia radical** — Todo el código y proceso es público.

## Capas de seguridad

┌─────────────────────────────────────────────────────────┐
│  Capa 7 — Legal (términos, licencias, jurisdicción)     │
├─────────────────────────────────────────────────────────┤
│  Capa 6 — Gobernanza (autoridad, cambios, resoluciones) │
├─────────────────────────────────────────────────────────┤
│  Capa 5 — Operativa (respuesta, continuidad, auditoría) │
├─────────────────────────────────────────────────────────┤
│  Capa 4 — Custodia (registro, backups, inmutabilidad)   │
├─────────────────────────────────────────────────────────┤
│  Capa 3 — Criptografía (firmas, hashes, sellos)         │
├─────────────────────────────────────────────────────────┤
│  Capa 2 — Aplicación (index.html, schemas, tests)       │
├─────────────────────────────────────────────────────────┤
│  Capa 1 — Infraestructura (GitHub Pages, Git, DNS)      │
└─────────────────────────────────────────────────────────┘


## Flujo de emisión de un sello

Titular → hash local → JSON → firma GPG → 
Safe Creative (sello tiempo) → 
Ethereum (anclaje) → 
Git commit → registro público → validación


Cada paso es verificable independientemente.

## Zonas de confianza

| Zona | Confianza | Contenido |
|------|-----------|-----------|
| Pública | Ninguna | `registro/`, `schemas/` |
| Autor | Alta | `crypto/claves-publicas/` |
| Operativa | Media | Emisión de sellos |
| Histórica | Absoluta | Git history |

## Modelo de confianza

Kronos-Vault **no confía en sí mismo**. Confía en:

- Propiedades matemáticas del hash.
- Autoridad externa de sellado temporal.
- Inmutabilidad de blockchain.
- Verificación independiente.

Cualquier tercero puede validar sin contactar al autor.
# Sellos Emitidos

Registro individual de cada sello emitido por Kronos-Vault, independientemente de su estado.

## Formato

Cada sello se publica como `SSSSSSSSSSSSS.json` (ID de 13 dígitos) conforme al schema oficial.

Ejemplo: `2607146379465.json`

## Contenido mínimo

- `schema_version`
- `id`
- `estado`
- `fecha_sellado`
- `titular`
- `obra`
- `sellos_de_tiempo`
- `blockchain` (si aplica)
- `licencia`
- `principios`

## Verificación

Ver [`../../docs/procedimiento-validacion.md`](../../docs/procedimiento-validacion.md).

## Estado actual

1 sello emitido:
- `2607146379465.json` — KRONOS — Arquitectura de Legado Digital
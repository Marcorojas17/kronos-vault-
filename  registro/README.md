# Registro Público

Registro verificable de todos los sellos emitidos por Kronos-Vault.

## Archivos

- `indice-publico.json` — Índice completo de sellos activos.
- `genesis/` — Registros fundacionales (Fase Génesis).
- `sellos/` — Sellos individuales emitidos.
- `revocados/` — Sellos revocados con causal documentada.
- `auditorias/` — Registros de auditorías realizadas.

## Principio

El registro es **solo-adicionable**. Nunca se elimina una entrada histórica. Las revocaciones se registran como cambio de estado, no como borrado.

## Verificación

Cualquier tercero puede:

1. Consultar `indice-publico.json`.
2. Verificar hashes con el archivo original.
3. Comprobar sello temporal.
4. Comprobar anclaje blockchain.

Ver [`../docs/procedimiento-validacion.md`](../docs/procedimiento-validacion.md).

## Estado actual

| Métrica | Valor |
|---------|-------|
| Sellos activos | 1 |
| Sellos revocados | 0 |
| Auditorías realizadas | 0 |
| Última actualización | 2026-07-14 |
# Sellos Revocados

Registro de sellos revocados con causal documentada.

## Estado actual

Sin revocaciones registradas.

## Formato

Cada revocación se publica como `SSSSSSSSSSSSS.json` con:

- ID del sello revocado.
- Fecha de revocación.
- Causal (según `../../legal/revocacion.md`).
- Evidencia.
- Resolución vinculada.

## Reglas

1. Una revocación **nunca elimina** la entrada original.
2. Se registra como cambio de estado.
3. Se documenta en `../../gobernanza/resoluciones/`.
4. Se notifica al titular en 7 días.

## Procedimiento

Ver [`../../legal/revocacion.md`](../../legal/revocacion.md).
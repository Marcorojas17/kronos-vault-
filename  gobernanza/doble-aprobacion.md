# Doble Aprobación

## Propósito

Reducir el riesgo de decisiones unilaterales en el estándar.

## Cuándo aplica

| Tipo de cambio | Aprobación requerida |
|----------------|----------------------|
| PATCH (corrección) | Autoridad de Versiones |
| MINOR (adición) | Autoridad + 1 miembro Consejo |
| MAJOR (incompatible) | Autoridad + 2/3 Consejo |
| Cambio de principios | Unanimidad Consejo |
| Revocación de sello | Autoridad + documentación |

## Proceso

1. Propuesta publicada como issue en GitHub.
2. Discusión pública mínima 14 días.
3. Votación (si aplica).
4. Commit firmado con GPG.
5. Publicación en `gobernanza/resoluciones/`.
6. Actualización de `CHANGELOG.md`.

## Transparencia

Toda decisión debe indicar:
- Fecha.
- Motivo.
- Aprobadores.
- Votos en contra (si los hay).
- Enlaces a discusión.

## Fase Génesis (0.x)

Mientras no exista el Consejo, las decisiones MAJOR requieren:
- Publicación previa en GitHub 30 días.
- Justificación documentada.
- Posibilidad de revertir si hay oposición fundada.
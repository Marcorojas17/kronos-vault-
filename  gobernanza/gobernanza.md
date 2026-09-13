# Gobernanza de Kronos-Vault

## 1. Naturaleza

Kronos-Vault es un estándar **privado, público, autoestablecido y verificable**. Su gobernanza define cómo evoluciona sin comprometer su integridad.

## 2. Autoridad fundacional

El autor y titular original es **Marco Antonio Rojas Valdovinos**, quien ejerce como **Autoridad de Versiones** durante la Fase Génesis (0.x).

## 3. Fases del estándar

| Fase | Versión | Gobernanza |
|------|---------|------------|
| Génesis | 0.x | Autor único. |
| Consolidación | 1.x | Autor + Consejo Génesis (100). |
| Estándar abierto | 2.x+ | Consejo + comunidad. |

## 4. Consejo Génesis

Formado por los titulares de los 100 Pasaportes Génesis. Funciones:

- Votar cambios MAJOR al schema.
- Aprobar nuevas autoridades de sellado.
- Revisar revocaciones controvertidas.

Quórum: 30% de los miembros activos.

## 5. Proceso de cambios



Ver [`proceso-de-cambios.md`](proceso-de-cambios.md).

## 6. Política de independencia

La Autoridad de Versiones:

- No puede modificar retroactivamente sellos emitidos.
- No puede revocar sellos sin causal documentada.
- No puede alterar el registro público sin dejar rastro en Git.

## 7. Conflictos de interés

La Autoridad de Versiones debe declarar cualquier conflicto de interés antes de votar.

## 8. Resoluciones

Toda decisión formal se publica en `gobernanza/resoluciones/` con:

- Fecha.
- Motivo.
- Decisión.
- Firmas aplicables.

## 9. Disolución

Si el estándar se disuelve:

1. El registro público se conserva íntegro.
2. Los sellos emitidos permanecen verificables.
3. El código y documentación pasan a dominio público (CC0).

## 10. Modificación de esta gobernanza

Requiere mayoría de 2/3 del Consejo Génesis + aprobación de la Autoridad de Versiones.
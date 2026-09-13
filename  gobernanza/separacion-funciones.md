# Separación de Funciones

## Principio

Ninguna entidad puede concentrar el control de todo el ciclo de vida de un sello.

## Roles

| Rol | Responsabilidad | Actor actual |
|-----|-----------------|--------------|
| Autor | Crea la obra | Titular |
| Emisor | Emite el sello | Kronos-Vault |
| Sellador de tiempo | Fecha cualificada | Safe Creative / Firmaprofesional |
| Auditor blockchain | Prueba de existencia | Ethereum |
| Verificador | Valida independiente | Cualquier tercero |

## Reglas

1. El Emisor no puede modificar el sello una vez emitido.
2. El Sellador de tiempo es independiente del Emisor.
3. El Auditor blockchain es una red pública descentralizada.
4. El Verificador no necesita confiar en el Emisor.

## Conflicto de interés

Si el Titular y el Emisor son la misma persona (caso Fase Génesis):

- Se declara públicamente en `gobernanza/conflictos-interes.md`.
- Se mitiga con verificación pública independiente.
- Se documenta cada emisión en el registro público.
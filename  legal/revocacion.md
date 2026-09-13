# Política de Revocación de Sellos

## Principio

Un sello Kronos-Vault es una declaración verificable. Su revocación es **excepcional** y requiere causal documentada.

## Causales de revocación

| Causal | Descripción |
|--------|-------------|
| Orden judicial | Requerimiento de autoridad competente. |
| Fraude comprobado | Falsificación de identidad o datos. |
| Violación de términos | Incumplimiento de `terminos.md`. |
| Ruptura de cadena de custodia | Alteración del sello o archivo. |
| Error del emisor | Fallo atribuible a Kronos-Vault. |
| Solicitud del titular | Revocación voluntaria. |

## Procedimiento

### 1. Detección o solicitud
Se identifica la causal.

### 2. Documentación
Se recaba evidencia.

### 3. Evaluación
La Autoridad de Versiones evalúa.

### 4. Decisión
Se emite resolución motivada.

### 5. Publicación
Se registra en `registro/revocados/` y `gobernanza/resoluciones/`.

### 6. Notificación
Se notifica al titular en 7 días.

### 7. Anuncio
Se anuncia públicamente si afecta a terceros.

## Efectos de la revocación

- El sello se marca como `revocado` en `indice-publico.json`.
- **No se elimina** la entrada histórica.
- La revocación es verificable públicamente.
- El titular puede solicitar nuevo sello si la causal se resuelve.

## Revocación voluntaria por el titular

El titular puede solicitar revocación de su propio sello mediante:

1. Email firmado a `proyectokronos@hotmail.com`.
2. Verificación de identidad.
3. Confirmación expresa.

## Revocación por orden judicial

Se acata sin demora. Se documenta en `gobernanza/resoluciones/`.

## Registro público

Archivo: `registro/revocados.json`

Formato:

```json
{
  "id": "...",
  "fecha_revocacion": "...",
  "causal": "...",
  "evidencia": "...",
  "resolucion": "..."
}
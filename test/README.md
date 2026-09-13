# Tests de Conformidad

Casos de prueba para validar la correcta aplicación del estándar Kronos-Vault.

## Estructura

- `casos-validos/` — Sellos que deben validar correctamente.
- `casos-invalidos/` — Sellos que deben fallar la validación.
- `casos-limite/` — Casos en el borde de la especificación.

## Ejecución manual

1. Validar contra `schemas/sello-kronos-vault.schema.json`.
2. Verificar hashes del archivo original.
3. Consultar estado en `registro/indice-publico.json`.

## Herramientas sugeridas

- `ajv` (Node.js) para validación de schema.
- `openssl` o `sha256sum` para hashes.
- Validador JSON Schema Draft 2020-12.

## Añadir un caso

1. Crear archivo JSON en la carpeta correspondiente.
2. Documentar el resultado esperado en un comentario o archivo `.expected`.
3. Actualizar este README si aplica.

## Estado actual

Fase Génesis: casos mínimos. Se ampliarán en Fase 2.
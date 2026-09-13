# Pruebas de Integridad

Verificaciones periódicas de la integridad de archivos y sellos.

## Estado actual

Sin pruebas formales documentadas.

## Procedimiento

1. Descargar archivos desde el repositorio.
2. Ejecutar `sha256sum -c checksums/SHA256SUMS`.
3. Verificar firmas GPG (cuando aplique).
4. Comparar con hashes declarados en sellos.
5. Documentar resultado en `YYYYMMDD-integridad.md`.

## Resultado esperado

Todos los archivos deben coincidir con sus hashes declarados. Cualquier discrepancia invalida el sello correspondiente.

## Frecuencia

Trimestral.
# Estrategia de Respaldos

## Principio 3-2-1

- **3** copias de cada dato crítico.
- **2** medios o tecnologías distintas.
- **1** copia fuera del sitio principal.

## Activos críticos

| Activo | Criticidad | Ubicación primaria |
|--------|------------|---------------------|
| Repositorio completo | Crítica | GitHub |
| Claves GPG privadas | Crítica | Almacenamiento offline |
| Certificados Safe Creative | Alta | GitHub + local |
| Certificado blockchain | Alta | GitHub + Etherscan |
| Email del proyecto | Alta | Hotmail |
| Links de pago | Alta | Mercado Pago |

## Implementación actual (Fase 1)

| Activo | Copia 1 | Copia 2 | Copia 3 |
|--------|---------|---------|---------|
| Repositorio | GitHub | Clon local en PC | Disco externo |
| Certificados | GitHub | Carpeta local | Email |
| Claves privadas | Hardware/offline | Papel (frase semilla) | Caja de seguridad |

## Implementación planificada (Fase 2)

- Backup automatizado semanal con `git bundle`.
- Cifrado AES-256 de respaldos locales.
- Sincronización cifrada a almacenamiento en la nube.
- Pruebas de recuperación documentadas en `evidencias/pruebas-recuperacion/`.

## Frecuencia

| Activo | Frecuencia |
|--------|------------|
| Repositorio | Semanal |
| Claves privadas | Solo al generarse |
| Certificados | Al emitirse |
| Configuración | Al cambiar |

## Procedimiento de recuperación

1. Verificar la integridad del respaldo (checksum).
2. Restaurar en entorno aislado.
3. Validar con `SHA256SUMS`.
4. Documentar en `evidencias/pruebas-recuperacion/`.
5. Registrar la prueba con fecha y resultado.

## Pruebas

Toda prueba de recuperación se documenta con:

- Fecha.
- Activo probado.
- Resultado.
- Tiempo de recuperación.
- Incidencias encontradas.

## Responsabilidad

Marco Antonio Rojas Valdovinos es el único responsable de la custodia actual.

En Fase 2 se documentará delegación formal.
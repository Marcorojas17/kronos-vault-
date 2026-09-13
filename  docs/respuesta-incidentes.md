# Respuesta ante Incidentes

## Objetivo

Definir el procedimiento formal ante cualquier incidente de seguridad, integridad o uso no autorizado relacionado con Kronos-Vault.

## Clasificación de incidentes

| Severidad | Descripción | Ejemplo |
|-----------|-------------|---------|
| Crítica | Compromiso de clave privada | Filtración de clave GPG |
| Alta | Uso no autorizado de obra | Publicación comercial sin licencia |
| Alta | Alteración del registro público | Commit malicioso |
| Media | Intento de suplantación | Email falso con dominio similar |
| Media | Filtración de datos del titular | Acceso no autorizado a email |
| Baja | Error tipográfico en documentación | Corregible en commit |

## Procedimiento general

### Fase 1 — Detección

- Reporte por email: `proyectokronos@hotmail.com`.
- Reporte por canal cifrado si aplica.
- Detección interna por monitoreo.

### Fase 2 — Contención

- Aislar el componente afectado.
- Suspender temporalmente emisiones si es necesario.
- Documentar evidencia.

### Fase 3 — Erradicación

- Corregir la causa raíz.
- Rotar credenciales si aplica.
- Revocar claves comprometidas.

### Fase 4 — Recuperación

- Restaurar servicio desde respaldo verificado.
- Validar integridad con `SHA256SUMS`.
- Documentar en `evidencias/pruebas-recuperacion/`.

### Fase 5 — Lecciones aprendidas

- Publicar post-mortem (sin comprometer seguridad).
- Actualizar `THREAT-MODEL.md`.
- Actualizar procedimientos.

## Plazos de respuesta

| Fase | Plazo máximo |
|------|--------------|
| Acuse de recibo | 48 horas |
| Evaluación inicial | 7 días |
| Mitigación | 30 días |
| Post-mortem | 60 días |

## Uso no autorizado de obra

Cuando se detecta uso no autorizado:

1. Documentar evidencia (URL, fecha, captura).
2. Verificar licencia aplicable.
3. Emitir notificación DMCA al proveedor.
4. Contactar al infractor si es identificable.
5. Registrar en `evidencias/pruebas-seguridad/`.

## Contacto

**Email de seguridad:** proyectokronos@hotmail.com
**Email legal:** marco.a.rojas.v@hotmail.com
**WhatsApp:** +52 722 586 2335
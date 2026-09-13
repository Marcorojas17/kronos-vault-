# Recuperación ante Desastres

## Objetivo

Restaurar el servicio completo de Kronos-Vault ante pérdida total o parcial de infraestructura.

## Escenarios cubiertos

1. Pérdida del repositorio GitHub.
2. Pérdida del email del proyecto.
3. Pérdida de claves privadas.
4. Pérdida de respaldos locales.
5. Catástrofe regional.

## Activos a recuperar

| Activo | Prioridad | Fuente |
|--------|-----------|--------|
| Repositorio completo | 1 | GitHub + clon local |
| Claves privadas GPG | 1 | Offline + papel |
| Certificados Safe Creative | 2 | GitHub + email |
| Certificado blockchain | 2 | Etherscan + GitHub |
| Links de pago | 3 | Mercado Pago |
| Landing pública | 4 | GitHub Pages |

## Procedimiento

### Caso 1 — Pérdida del repositorio

1. Restaurar desde clon local (`git clone`).
2. Verificar integridad con `SHA256SUMS`.
3. Push a nuevo repositorio si es necesario.
4. Reactivar GitHub Pages.

### Caso 2 — Pérdida del email

1. Acceder al email alternativo.
2. Recuperar cuenta si es posible.
3. Si no, crear nuevo email y actualizar en todos los documentos.
4. Notificar a titulares afectados.

### Caso 3 — Pérdida de claves privadas

1. Activar certificado de revocación pre-generado.
2. Publicar revocación en `crypto/revocaciones/`.
3. Generar nueva clave GPG.
4. Publicar nueva clave pública.
5. Re-firmar releases afectados.
6. Notificar a terceros verificadores.

### Caso 4 — Catástrofe regional

1. Activar copia de seguridad en ubicación geográfica distinta.
2. Restaurar servicios desde respaldo offline.
3. Comunicar estado en canales oficiales.

## Pruebas

Cada prueba de recuperación se documenta en `evidencias/pruebas-recuperacion/` con:

- Fecha.
- Escenario simulado.
- Resultado.
- Tiempo de recuperación.
- Incidencias.

## Frecuencia

| Prueba | Frecuencia |
|--------|------------|
| Restauración de repo | Trimestral |
| Verificación de claves | Semestral |
| Simulación completa | Anual |

## Contacto de emergencia

**Email:** proyectokronos@hotmail.com
**Email alterno:** marco.a.rojas.v@hotmail.com
**WhatsApp:** +52 722 586 2335
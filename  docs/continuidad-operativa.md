# Continuidad Operativa

## Objetivo

Garantizar que Kronos-Vault pueda seguir operando ante fallos, catástrofes o indisponibilidad de componentes críticos.

## Componentes críticos

| Componente | Criticidad | Alternativa |
|------------|------------|-------------|
| Repositorio GitHub | Alta | Mirror en GitLab |
| Safe Creative | Alta | Otros QTSA eIDAS |
| Ethereum | Media | Multi-chain |
| Email del proyecto | Alta | Email secundario |
| Landing GitHub Pages | Media | Cloudflare Pages |
| Mercado Pago | Alta | PayPal, Stripe |

## Escenarios de fallo

### 1. Caída de GitHub

- **Impacto:** Landing y repo inaccesibles.
- **Mitigación inmediata:** Activar mirror en GitLab.
- **Mitigación futura:** Cloudflare Pages como respaldo.

### 2. Caída de Safe Creative

- **Impacto:** No se pueden emitir nuevos sellos.
- **Mitigación:** Emitir con sello interno mientras se restaura.
- **Mitigación futura:** Contrato con segundo QTSA.

### 3. Caída de Ethereum

- **Impacto:** No se pueden anclar nuevos sellos.
- **Mitigación:** Anclaje diferido hasta restauración.
- **Mitigación futura:** Anclaje en Polygon o Base.

### 4. Compromiso de clave privada

- **Impacto:** Crítico. Firmas falsificables.
- **Mitigación:** Activar revocación inmediata.
- **Recuperación:** Generar nueva clave y re-firmar releases.

### 5. Incapacidad del autor

- **Impacto:** Alto.
- **Mitigación:** Documento de sucesión en `gobernanza/`.
- **Recuperación:** Consejo Génesis asume gobernanza.

## Plan de continuidad

1. **Mantener mirrors actualizados** (Fase 2).
2. **Documentar todo procedimiento** en este repo.
3. **Delegar formalmente** cuando exista Consejo Génesis.
4. **Probar recuperación** cada 6 meses.
5. **Registrar pruebas** en `evidencias/pruebas-recuperacion/`.

## Objetivo de recuperación

| Métrica | Valor objetivo |
|---------|----------------|
| RTO (tiempo de recuperación) | 72 horas |
| RPO (pérdida máxima de datos) | 0 sellos |
| Frecuencia de pruebas | Semestral |

## Responsabilidad actual

Marco Antonio Rojas Valdovinos.

En Fase 2 se documentará delegación y sucesión.
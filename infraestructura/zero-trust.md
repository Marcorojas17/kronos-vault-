# Arquitectura Zero Trust

## Principio

**Ninguna entidad es confiable por defecto.** Toda verificación es explícita y continua.

## Aplicación en Kronos-Vault

| Componente | Confianza | Verificación |
|------------|-----------|--------------|
| Titular | Condicional | Firma GPG |
| Emisor | Condicional | Registro público + sellos |
| Safe Creative | Limitada | Autoridad externa |
| Firmaprofesional | Limitada | Autoridad externa eIDAS |
| Ethereum | Distribuida | Consenso público |
| Terceros | Ninguna | Deben validar por sí mismos |

## Pilares aplicados

### 1. Identidad verificable
Cada release y decisión se firma con GPG. El fingerprint es público.

### 2. Acceso mínimo
Solo el autor posee claves privadas. Los colaboradores proponen vía Pull Request.

### 3. Asumir brecha
Todo se publica. Nada se asume oculto. La seguridad no depende del secreto.

### 4. Verificación continua
Hashes públicos, checksums firmados, validación independiente.

### 5. Microsegmentación
Cada componente (registro, criptografía, gobernanza) opera de forma aislada.

## Controles actuales

- ✅ Repositorio público (transparencia total)
- ✅ Claves privadas nunca en repo
- ✅ Historial Git inmutable
- ✅ Sello temporal externo cualificado
- ✅ Anclaje blockchain público

## Controles pendientes

- ⏳ Firma GPG obligatoria de releases (Fase 2)
- ⏳ MFA en cuentas críticas (Fase 2)
- ⏳ Hardware tokens (Fase 2)
- ⏳ Monitoreo continuo (Fase 2)

## Referencias

- NIST SP 800-207 — Zero Trust Architecture
- CISA Zero Trust Maturity Model
- Google BeyondCorp
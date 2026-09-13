# Arquitectura de Infraestructura

## Visión general

Kronos-Vault opera sobre una infraestructura **mínima, verificable y de bajo costo**, priorizando la transparencia y la reproducibilidad sobre la opacidad corporativa.

## Componentes actuales (Fase 1)

| Componente | Tecnología | Función |
|------------|------------|---------|
| Landing pública | HTML + CSS + JS vanilla | Punto de entrada |
| Hosting | GitHub Pages | Servicio estático |
| Control de versiones | Git + GitHub | Historial inmutable |
| Documentación | Markdown | Especificación |
| Schemas | JSON Schema 2020-12 | Contratos de datos |
| Sellado temporal | Safe Creative + Firmaprofesional | Fecha cierta |
| Anclaje blockchain | Ethereum | Prueba de existencia |
| Comunicación | Email + WhatsApp | Contacto |

## Componentes planificados (Fase 2)

| Componente | Tecnología | Función |
|------------|------------|---------|
| Firma GPG | Ed25519 | Firma de releases |
| SBOM | SPDX 2.3 | Inventario de dependencias |
| MFA | TOTP | Autenticación reforzada |
| CI/CD | GitHub Actions | Verificación automatizada |
| Almacenamiento WORM | S3 Object Lock | Inmutabilidad real |
| CDN | Cloudflare | Distribución global |

## Componentes planificados (Fase 3)

| Componente | Tecnología | Función |
|------------|------------|---------|
| API pública | Node.js + Fastify | Integración programática |
| Base de datos | PostgreSQL | Persistencia estructurada |
| Auditoría externa | Tercero independiente | Validación |
| Pentest anual | Proveedor certificado | Seguridad ofensiva |

## Flujo de datos

Titular → Hash local (navegador) → JSON → 
Sello temporal (Safe Creative) → 
Anclaje blockchain (Ethereum) → 
Registro público (GitHub) → 
Verificación independiente (cualquier tercero


## Principios de diseño

1. **Mínima superficie de ataque** — Menos componentes = menos vulnerabilidades.
2. **Verificabilidad pública** — Todo el código es auditable.
3. **Bajo costo sostenible** — No depender de infraestructura cara para operar.
4. **Escalabilidad incremental** — Cada fase agrega solo lo necesario.
5. **Independencia del emisor** — La verificación no requiere al autor.

## Riesgos conocidos

- Dependencia de GitHub (mitigable con mirrors).
- Dependencia de Safe Creative (mitigable con múltiples QTSA).
- Dependencia de Ethereum (mitigable con multi-chain).

## Revisión

Este documento se actualiza al inicio de cada fase.
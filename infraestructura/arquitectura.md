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

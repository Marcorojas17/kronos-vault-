# Monitoreo y Observabilidad

## Objetivo

Detectar tempranamente:

- Intentos de uso no autorizado de obras registradas.
- Cambios anómalos en el repositorio.
- Incidentes de seguridad.
- Problemas de disponibilidad de servicios críticos.

## Componentes monitoreados

| Componente | Qué se monitorea | Frecuencia |
|------------|------------------|------------|
| Repositorio GitHub | Commits, issues, PRs | Tiempo real |
| Safe Creative | Estado del certificado | Mensual |
| Ethereum | Transacción de anclaje | Trimestral |
| Email del proyecto | Accesos inusuales | Continuo |
| Mercado Pago | Transacciones | Continuo |
| Búsquedas web | Uso no autorizado | Mensual |

## Herramientas actuales

- **GitHub Notifications** — Alertas de cambios en el repo.
- **Google Alerts** — Menciones de "KRONOS" o "Marco Rojas Valdovinos".
- **Manual** — Revisión mensual.

## Herramientas planificadas (Fase 2)

- **UptimeRobot** — Disponibilidad de la landing.
- **Have I Been Pwned** — Filtraciones de credenciales.
- **Etherscan Alerts** — Actividad de la dirección blockchain.
- **Safe Creative API** — Estado automatizado del certificado.

## Detección de uso no autorizado

### Búsqueda activa

Búsquedas periódicas en:

- Google, Bing, DuckDuckGo.
- Hugging Face (modelos de IA).
- Common Crawl (corpus de entrenamiento).
- GitHub, GitLab (código).

### Criterios de alerta

- Aparición de la obra sin atribución.
- Uso comercial sin licencia.
- Inclusión en datasets de entrenamiento.
- Derivados no autorizados.

## Procedimiento ante detección

1. Documentar la evidencia (URL, fecha, captura).
2. Verificar si es uso permitido por la licencia.
3. Si no lo es, emitir notificación DMCA.
4. Registrar el incidente en `docs/respuesta-incidentes.md`.
5. Anunciar públicamente si el caso es relevante.

## Métricas actuales

Sin métricas automatizadas. Fase Génesis opera manualmente.

## Roadmap

- **Fase 2:** Alertas automáticas de menciones web.
- **Fase 3:** Monitoreo activo de datasets de IA.
- **Fase 4:** Sistema de alertas legales automatizadas.
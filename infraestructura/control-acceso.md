# Control de Acceso

## Principio de mínimo privilegio

Cada actor tiene solo el acceso mínimo necesario para cumplir su función.

## Matriz de acceso

| Rol | Repo GitHub | Claves privadas | Emisión de sellos | Registro público |
|-----|-------------|-----------------|-------------------|------------------|
| Autor | Administrador | Sí (offline) | Sí | Sí |
| Colaboradores | Escritura limitada vía PR | No | No | Propuestas |
| Terceros | Lectura | No | No | Lectura |
| Verificadores | Lectura | No | No | Lectura |
| Consejo Génesis (futuro) | Lectura + issues | No | No | Lectura |

## Controles actuales

- ✅ Repositorio público: transparencia total
- ✅ Claves privadas nunca en el repo
- ✅ Git history inmutable
- ✅ Commits con identidad verificable
- ✅ Registro público solo-adicionable

## Controles pendientes

- ⏳ Firma GPG obligatoria de commits (Fase 2)
- ⏳ MFA en GitHub (Fase 2 — urgente)
- ⏳ MFA en email del proyecto (Fase 2 — urgente)
- ⏳ MFA en Mercado Pago (Fase 2 — urgente)
- ⏳ Delegación formal de permisos (Fase 3)

## Recomendaciones inmediatas

1. **Activar 2FA en GitHub hoy mismo.**
2. **Activar 2FA en `proyectokronos@hotmail.com`.**
3. **Activar 2FA en `marco.a.rojas.v@hotmail.com`.**
4. **Activar 2FA en Mercado Pago.**
5. **Nunca compartir claves privadas** por chat, email ni WhatsApp.

## Auditoría

El historial de Git permite auditar:

- Quién cambió qué.
- Cuándo.
- Con qué justificación (mensaje de commit).

## Revocación de accesos

Si un colaborador deja el proyecto:

1. Revocar permisos en GitHub.
2. Rotar cualquier secreto compartido.
3. Documentar en `gobernanza/resoluciones/`.
4. Anunciar cambio si afecta a usuarios.
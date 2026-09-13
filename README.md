# Kronos-Vault

> **Estándar privado, público, autoestablecido y verificable para la preservación, autenticidad y trazabilidad de obras digitales.**

Kronos-Vault es una arquitectura de legado digital diseñada para que la voz, principios y obras de una persona permanezcan íntegras, verificables y activas más allá de su vida física, hasta el año 2099.

Su diseño se alinea con **ISO 14721 (OAIS)** e **ISO/IEC 27001** mediante autoevaluación documentada, **sin afirmar certificación externa**.

---

## Estado del proyecto

| Campo | Valor |
|-------|-------|
| Versión | 0.1.0 (Fase Génesis) |
| Fecha de registro | 14 de julio de 2026, 0:46 UTC |
| Certificado Safe Creative | `2607146379465` |
| Verificación pública | https://www.safecreative.org/certificate/2607146379465 |
| Autor y titular | Marco Antonio Rojas Valdovinos |
| Licencia de obra | CC BY-NC-ND 4.0 |
| Licencia de código | MIT (solo para `schemas/` y `tests/`) |

---

## Qué es Kronos-Vault

Kronos-Vault no es un producto. Es un **estándar abierto, verificable y autoestablecido** para:

1. Calcular la huella digital de una obra (SHA-256, SHA-512).
2. Aplicar sellado de tiempo cualificado (eIDAS / QTSA).
3. Emitir un certificado verificable públicamente.
4. Auditar la existencia en blockchain.
5. Permitir la validación independiente por terceros sin depender del autor.

Cualquier persona puede usar el esquema. Cualquier verificador puede comprobarlo. Ningún actor controla el estándar.

---

## Los 6 principios

1. **Integridad** — Cadena de custodia criptográfica irrompible.
2. **Trazabilidad** — Fecha, origen y propósito de cada uso.
3. **No Comercialización** — Lucro prohibido sin autorización expresa.
4. **No Entrenamiento de IA** — Prohibición explícita de uso para entrenar modelos.
5. **Citación Obligatoria** — Atribución completa: *"Marco Antonio Rojas Valdovinos — KRONOS 2026"*.
6. **Defensa Activa** — Alertas y acciones legales ante violaciones.

---

## Estructura del repositorio
kronos-vault/
├── index.html                 # Landing pública
├── README.md                  # Este archivo
├── LICENSE                    # CC BY-NC-ND 4.0 (obra)
├── LICENSE-CODE.md            # MIT (código)
├── VERSION
├── CHANGELOG.md
├── CONTRIBUTING.md
├── CODE_OF_CONDUCT.md
├── SECURITY.md
├── .gitignore
├── docs/                      # Documentación técnica y conceptual
├── legal/                     # Términos, privacidad, IP
├── gobernanza/                # Reglas de evolución del estándar
├── comunidad/                 # Código de conducta, contribuciones
├── registro/                  # Registros públicos (JSON)
├── schemas/                   # JSON Schemas del estándar
├── ejemplos/                  # Casos válidos, inválidos, límite
├── tests/                     # Pruebas de conformidad
├── prensa/                    # Comunicados y kit
├── assets/                    # Identidad visual
├── .well-known/               # security.txt
└── api/                       # Fase futura (no implementado)


---

## Cómo validar un sello

1. Descarga el archivo `schemas/sello-kronos-vault.schema.json`.
2. Toma un registro de `registro/indice-publico.json`.
3. Valida el registro contra el schema con cualquier validador JSON Schema (Draft 2020-12).
4. Verifica la huella SHA-256 del archivo original.
5. Consulta el sello de tiempo en la autoridad correspondiente.

Ver [`docs/procedimiento-validacion.md`](docs/procedimiento-validacion.md) para el procedimiento completo.

---

## Los 100 Génesis

Kronos-Vault abre **100 plazas fundacionales**. Quienes las ocupen:

- Reciben el Pasaporte Génesis (registro verificable).
- Acceso vitalicio al Plan Eterno.
- Voz en la gobernanza del estándar.
- Su caso se documenta en `registro/` como parte del origen.

Cuando se llenen las 100, el precio sube y el Pasaporte Génesis deja de emitirse.

---

## Contacto

**Email:** hola@kronoslegado.com
**Web:** [tu usuario].github.io/kronos-vault
**Verificación:** https://www.safecreative.org/certificate/2607146379465

---

## Licencia

- **Obra y documentación:** CC BY-NC-ND 4.0 — ver [`LICENSE`](LICENSE).
- **Código (`schemas/`, `tests/`):** MIT — ver [`LICENSE-CODE.md`](LICENSE-CODE.md).

**Prohibido el uso de esta obra para entrenar modelos de inteligencia artificial.**

© 2026 Marco Antonio Rojas Valdovinos.
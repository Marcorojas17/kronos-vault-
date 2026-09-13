# Modelo de Amenazas — Kronos-Vault v0.1.0

Metodología: **STRIDE** + **LINDDUN** (privacidad).

## Activos a proteger

| Activo | Valor | Impacto si se compromete |
|--------|-------|--------------------------|
| Obra original | Crítico | Pérdida de autoría |
| Hashes del sello | Crítico | Falsificación |
| Clave privada del emisor | Crítico | Firma fraudulenta |
| Registro público | Alto | Manipulación histórica |
| Datos del titular | Medio | Violación de privacidad |
| Metadatos temporales | Alto | Falsificación de fecha |

## Adversarios considerados

1. **Atacante oportunista** — Script kiddie buscando vulnerabilidades web.
2. **Adversario con recursos** — Competidor o actor con presupuesto.
3. **Actor estatal** — Vigilancia o censura.
4. **IA generativa** — Uso no autorizado de la obra para entrenamiento.
5. **Insider malicioso** — Colaborador con acceso.
6. **Fallo del sistema** — Pérdida de datos, corrupción, catástrofe.

## Amenazas STRIDE

| Amenaza | Escenario | Mitigación |
|---------|-----------|------------|
| **S**poofing | Suplantar al emisor | Firma GPG + clave pública |
| **T**ampering | Alterar sello | Hash + blockchain |
| **R**epudio | Negar emisión | Registro Git + sello temporal |
| **I**nformation disclosure | Filtrar datos del titular | Minimización + cifrado |
| **D**enial of service | Tumbar el sitio | GitHub Pages CDN |
| **E**levation of privilege | Escalar acceso | Zero Trust documentado |

## Amenazas LINDDUN (privacidad)

| Amenaza | Mitigación |
|---------|------------|
| Linking | No se almacenan archivos originales |
| Identifying | Datos mínimos requeridos |
| Non-repudiation | El titular controla su identidad |
| Detecting | Sin cookies de rastreo |
| Data disclosure | Cifrado en tránsito |
| Unawareness | Política de privacidad pública |
| Non-compliance | Alineación con LFPDPPP y GDPR |

## Riesgos residuales

- Validez probatoria depende de jurisdicción.
- Firma GPG no vinculante sin autoridad certificadora.
- Sellado temporal depende de Safe Creative y Firmaprofesional.
- Anclaje blockchain depende de Ethereum.

## Revisión

Este modelo se actualiza cada 6 meses o ante incidente mayor.
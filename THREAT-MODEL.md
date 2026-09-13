# Modelo de Amenazas — Kronos-Vault v0.1.0

Metodología: STRIDE + LINDDUN.

## Activos a proteger

| Activo | Impacto si se compromete |
|--------|--------------------------|
| Obra original | Crítico |
| Hashes del sello | Crítico |
| Clave privada del emisor | Crítico |
| Registro público | Alto |
| Datos del titular | Medio |
| Metadatos temporales | Alto |

## Adversarios considerados

1. Atacante oportunista (script kiddie).
2. Adversario con recursos (competidor).
3. Actor estatal (vigilancia o censura).
4. IA generativa (uso no autorizado para entrenamiento).
5. Insider malicioso.
6. Fallo del sistema (catástrofe, corrupción).

## Amenazas STRIDE

| Amenaza | Escenario | Mitigación |
|---------|-----------|------------|
| Spoofing | Suplantar al emisor | Firma GPG + clave pública |
| Tampering | Alterar sello | Hash + blockchain |
| Repudio | Negar emisión | Registro Git + sello temporal |
| Information disclosure | Filtrar datos del titular | Minimización + cifrado |
| Denial of service | Tumbar el sitio | GitHub Pages CDN |
| Elevation of privilege | Escalar acceso | Zero Trust documentado |

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
- Sellado temporal depende de Safe Creative y Firmaprofesional.
- Anclaje blockchain depende de Ethereum.
- Firma GPG no vinculante sin autoridad certificadora.

## Revisión

Se actualiza cada 6 meses o ante incidente mayor.
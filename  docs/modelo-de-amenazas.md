# Modelo de Amenazas

Metodología: **STRIDE** + **LINDDUN**.

Este documento resume el modelo completo. La versión extendida está en [`../THREAT-MODEL.md`](../THREAT-MODEL.md).

## Activos protegidos

| Activo | Impacto si se compromete |
|--------|--------------------------|
| Obra original | Crítico |
| Huellas del sello | Crítico |
| Clave privada del emisor | Crítico |
| Registro público | Alto |
| Datos del titular | Medio |
| Metadatos temporales | Alto |

## Adversarios

1. Atacante oportunista.
2. Adversario con recursos.
3. Actor estatal.
4. IA generativa.
5. Insider malicioso.
6. Fallo del sistema.

## Amenazas STRIDE

| Amenaza | Mitigación |
|---------|------------|
| Spoofing | Firma GPG + clave pública |
| Tampering | Hash + blockchain |
| Repudio | Registro Git + sello temporal |
| Information disclosure | Minimización + cifrado |
| Denial of service | GitHub Pages CDN |
| Elevation of privilege | Zero Trust documentado |

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

Cada 6 meses o ante incidente mayor.
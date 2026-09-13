# Política de Revocación de Sellos

## Principio

Un sello Kronos-Vault es una declaración verificable. Su revocación es **excepcional** y requiere causal documentada.

## Causales de revocación

| Causal | Descripción |
|--------|-------------|
| Orden judicial | Requerimiento de autoridad competente. |
| Fraude comprobado | Falsificación de identidad o datos. |
| Violación de términos | Incumplimiento de `terminos.md`. |
| Ruptura de cadena de custodia | Alteración del sello o archivo. |
| Error del emisor | Fallo atribuible a Kronos-Vault. |
| Solicitud del titular | Revocación voluntaria. |

## Procedimiento

### 1. Detección o solicitud
Se identifica la causal.

### 2. Documentación
Se recaba evidencia.

### 3. Evaluación
La Autoridad de Versiones evalúa.

### 4. Decisión
Se emite resolución motivada.

### 5. Publicación
Se registra en `registro/revocados/` y `gobernanza/resoluciones/`.

### 6. Notificación
Se notifica al titular en 7 días.

### 7. Anuncio
Se anuncia públicamente si afecta a terceros.

## Efectos de la revocación

- El sello se marca como `revocado` en `indice-publico.json`.
- **No se elimina** la entrada histórica.
- La revocación es verificable públicamente.
- El titular puede solicitar nuevo sello si la causal se resuelve.

## Revocación voluntaria por el titular

El titular puede solicitar revocación de su propio sello mediante:

1. Email firmado a `proyectokronos@hotmail.com`.
2. Verificación de identidad.
3. Confirmación expresa.

## Revocación por orden judicial

Se acata sin demora. Se documenta en `gobernanza/resoluciones/`.

## Registro público

Archivo: `registro/revocados.json`

Formato:

```json
{
  "id": "...",
  "fecha_revocacion": "...",
  "causal": "...",
  "evidencia": "...",
  "resolucion": "..."
}

Apelación

El titular puede apelar en 15 días hábiles con nueva evidencia.

Contacto

Email: proyectokronos@hotmail.com
Email legal: marco.a.rojas.v@hotmail.com



---

## 📁 BLOQUE F — SBOM y checksums (2 archivos)

### F1. `SBOM.spdx.json`

```json
{
  "spdxVersion": "SPDX-2.3",
  "dataLicense": "CC0-1.0",
  "SPDXID": "SPDXRef-DOCUMENT",
  "name": "kronos-vault-0.1.0",
  "documentNamespace": "https://github.com/Marcorojas17/kronos-vault/sbom-0.1.0",
  "creationInfo": {
    "created": "2026-07-14T00:46:00Z",
    "creators": [
      "Person: Marco Antonio Rojas Valdovinos (proyectokronos@hotmail.com)"
    ],
    "licenseListVersion": "3.22"
  },
  "packages": [
    {
      "SPDXID": "SPDXRef-Package-KronosVault",
      "name": "kronos-vault",
      "versionInfo": "0.1.0",
      "downloadLocation": "https://github.com/Marcorojas17/kronos-vault",
      "filesAnalyzed": false,
      "licenseConcluded": "CC-BY-NC-ND-4.0",
      "licenseDeclared": "CC-BY-NC-ND-4.0",
      "copyrightText": "Copyright (c) 2026 Marco Antonio Rojas Valdovinos",
      "supplier": "Person: Marco Antonio Rojas Valdovinos"
    },
    {
      "SPDXID": "SPDXRef-Package-Schemas",
      "name": "kronos-vault-schemas",
      "versionInfo": "0.1.0",
      "downloadLocation": "https://github.com/Marcorojas17/kronos-vault/schemas",
      "filesAnalyzed": false,
      "licenseConcluded": "MIT",
      "licenseDeclared": "MIT",
      "copyrightText": "Copyright (c) 2026 Marco Antonio Rojas Valdovinos"
    }
  ],
  "relationships": [
    {
      "spdxElementId": "SPDXRef-DOCUMENT",
      "relatedSpdxElement": "SPDXRef-Package-KronosVault",
      "relationshipType": "DESCRIBES"
    },
    {
      "spdxElementId": "SPDXRef-Package-KronosVault",
      "relatedSpdxElement": "SPDXRef-Package-Schemas",
      "relationshipType": "CONTAINS"
    }
  ]
}

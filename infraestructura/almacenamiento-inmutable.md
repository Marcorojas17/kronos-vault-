# Almacenamiento Inmutable

## Principio

El registro público de Kronos-Vault es **solo-adicionable**. Ninguna entrada histórica puede eliminarse ni modificarse sin dejar rastro verificable.

## Mecanismos actuales

### 1. Git como registro inmutable

- Cada commit tiene hash SHA-1 (Git) único.
- Modificar historia requiere reescribir todos los hashes posteriores.
- GitHub preserva el historial público.
- Forks independientes garantizan redundancia.

### 2. Blockchain Ethereum

- El hash del certificado se ancló en la red Ethereum.
- La transacción es verificable por cualquier tercero.
- Inmutable por diseño criptoeconómico.

### 3. Sellado temporal cualificado

- Safe Creative aplica sello de tiempo interno.
- Firmaprofesional aplica sello cualificado eIDAS.
- La fecha es criptográficamente verificable.

## Registro público

El archivo `registro/indice-publico.json` se actualiza **solo por adición**:

- Los sellos nuevos se agregan al final.
- Los sellos revocados permanecen en el archivo con estado `revocado`.
- Nunca se elimina una entrada.

## Revocaciones

Cuando un sello se revoca:

1. Se agrega entrada en `registro/revocados/`.
2. Se actualiza el estado en `indice-publico.json`.
3. Se documenta causal en `gobernanza/resoluciones/`.
4. El sello original **no se borra**.

## Limitaciones actuales

- GitHub puede eliminar el repositorio si viola sus términos.
- Mitigación: mirrors en GitLab, Codeberg, IPFS (Fase 2).

- El autor podría reescribir la historia localmente.
- Mitigación: forks de terceros sirven como testigos.

## Planificado (Fase 2)

- Mirror en GitLab.
- Mirror en Codeberg.
- Snapshot en IPFS.
- Almacenamiento WORM en S3 con Object Lock.

## Referencias

- ISO 14721 — modelo OAIS
- NIST SP 800-88 — Guidelines for Media Sanitization
- WORM — Write Once Read Many
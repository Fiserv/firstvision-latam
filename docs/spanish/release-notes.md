---
tags: [Release Notes, Enero, Febrero, Marzo]
---

# Release Notes

## Marzo 2023

### ¿Qué hay de nuevo?

- Documentación en español.
- Glosario API.

### Mejoras

- Lista VMX actualizada agregando nombre de endpoint.
- Casos Principales actualizados:
  - [Ambiente de API](?path=docs/spanish/casos-principales/ambiente-api.md)
  - [Auditoría y Monitoreo](?path=docs/spanish/casos-principales/auditoria.md)
  - [Cambio de PIN](?path=docs/spanish/casos-principales/cambio-pin.md)
  - [Cargar Fondos](?path=docs/spanish/casos-principales/cargas.md.md)
  - [Controles de Tarjetas](?path=docs/spanish/casos-principales/controles-tarjeta.md)
  - [CVV2 Dinámico](?path=docs/spanish/casos-principales/cvv-dinamico.md)
  - [Emisión de Tarjetas Digitales](?path=docs/spanish/casos-principales/emision-tarjetas.md)
  - [Entrada/Salida de Efectivo](?path=docs/spanish/casos-principales/entrada-salida-efectivo.md.md)
  - [Gestión de Clientes](?path=docs/spanish/casos-principales/gestion-clientes.md)
  - [Gestión de Cuentas](?path=docs/spanish/casos-principales/gestion-cuentas.md)
  - [Gestión de Tarjetas](?path=docs/spanish/casos-principales/gestion-tarjetas.md)
  - [HMAC Signature](?path=docs/spanish/casos-principales/hmac.md)
  - [Integración con el sistema Falcon](?path=docs/spanish/casos-principales/integracion-falcon.md)
  - [PAN Token](?path=docs/spanish/casos-principales/pan-token.md)
  - [Registro de Tarjeta](?path=docs/spanish/casos-principales/registro.md)
  - [Relación Cliente-Cuenta-Tarjeta](?path=docs/spanish/casos-principales/relacion.md)


### Problemas solucionados

Endpoints se movieron a la versión 1.1.0:

- /account/balance
- /account/transfer
- /account/QR-balance
- /account/QR-transfer
- /account/FL-transferP2P

### Deprecado

- /account/QRFL-balance
- /cards/instant-card-L8V7
- /transactions/organization-update

---


## Febrero 2023

### ¿Qué hay de nuevo?

Nuevas API's Tokenization

- /vtis/v1/tokenRequestors/{tokenRequestorID}/tokens/{tokenReferenceID}/deviceBinding
- /vtis/v1/getAvailableCards
- /vtis/v1/getSelectedCards
- /vtis/v1/pan/lifecycle
- /vtis/v2/tokenRequestors/{tokenRequestorID}/tokens/{tokenReferenceID}/tokenChanged
- /vtis/v1/tokenRequestors/{tokenRequestorID}/tokens/{tokenReferenceID}/lifecycle
- /vtis/v1/checkEligibility

### Mejoras

N/A

### Problemas solucionados

- N/A

### Deprecado

- /account/card version R8V3

---

## Enero 2023

### ¿Qué hay de nuevo?

- Migración al nuevo portal.

### Mejoras

- Códigos de error, manejo de errores y notificaciones.

### Problemas solucionados

- N/A

### Deprecado

- Portal anterior.

---

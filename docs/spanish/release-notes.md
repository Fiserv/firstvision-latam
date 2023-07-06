---
tags: [Release Notes, Enero, Febrero, Marzo, Abril, Mayo, Junio, Julio]
---


---

# Release Notes

## Junio 06 2023

### ¿Qué hay de nuevo?

- N/A

### Mejoras

Descripción de API's mejorada:
- /cards/details
- /account/relationship/account
- /cards/statement-detail/date
- /cards/embosser/encrypted-card-pan
- /cards/transfer
- /transactions/summary-details
- /account/v2/customer
- /account/{accountNumber}/ibs-debit
- /account/enrollment POST
- /account/enrollment PUT
- /account/service-charge-table
- /account/{accountNumber}/relationship
- /account/{accountNumber}/product
- /account/{tableInquiry}/account-control-table-inquiry
- /account/account-demographic
- /cards/embosser/l8vf
- /cards/status-L8V1  
- /customer/{customerNumber}/relationship 
- /account/enroll/{accountNumber} 
- /account/wallet-priority-order
- /account/{accountNumber}/overview
- /customer/{accountNumber}/current-prior-address
- /transactions/outstanding-authorizations-L8V3/details
- /transactions/mcct-table

### Problemas solucionados

Endpoints se movieron a la versión 1.1.0:
- /account/balance
- /account/FL-balance

### Obsoleto
- /cards/embosser/encrypted-card-pan

---


# Release Notes

## Junio 2023

### ¿Qué hay de nuevo?

- N/A

### Mejoras

Descripción de API's mejorada:
- /cards/details
- /account/relationship/account
- /cards/statement-detail/date
- /cards/embosser/encrypted-card-pan
- /cards/transfer
- /transactions/summary-details
- /account/v2/customer
- /account/{accountNumber}/ibs-debit
- /account/enrollment POST
- /account/enrollment PUT
- /account/service-charge-table
- /account/{accountNumber}/relationship
- /account/{accountNumber}/product
- /account/{tableInquiry}/account-control-table-inquiry
- /account/account-demographic
- /cards/embosser/l8vf

### Problemas solucionados

- N/A

### Obsoleto

- N/A

---

# Release Notes

## Mayo 2023

### ¿Qué hay de nuevo?

- /account/v2/balance

### Mejoras

Descripción de API's mejorada:
- /customer/demographicData-l8v2
- /account/prepaid
- /cards/embosser/block
- /account/block-code
- /account/qualification
- /account/v2/instantCard
- /cards/embosser/card-details-L8V3
- /transactions/logo
- /cards/v2/embosser/details
- /customer/relationship
- /cards/statement-detail
- /account/balance/details
- /transactions/installmentConversion
- /transactions/enroll-history/{accountNumber}
- /customer/accountNumber
- /account/user
- /account/productTransfer
- /account/relationship/billing-cycle


### Problemas solucionados

- N/A

### Obsoleto

- /cards/global-card-activation

---

## Abril 2023

### ¿Qué hay de nuevo?

- N/A

### Mejoras

Descripción de API's mejorada:
- /cards/pin/security-codes
- /cards/pin/
- /cards/pin/status
- /cards/pin/dynamic-values
- /cards/pin/pin-change
- /cards/pin/validation
- /account/add-L8V3
- /cards/v3/embosser
- /cards/activation
- /customer/l8v2

### Problemas solucionados

Endpoints se movieron a la versión 1.2.0:
- /account/balance
- /cards/embosser/encrypted-card-pan
- /account/v2/accounts

Endpoints se movieron a la versión 1.1.0:

- /account/details-L8VG

### Obsoleto

- /account/status-update-L8V1
- /account/details

---

## Marzo 2023

### ¿Qué hay de nuevo?

- Documentación en español.
- Documentación en portugués.
- Glosario API.

### Mejoras

- Lista VMX actualizada agregando nombre de endpoint.
- Casos Principales actualizados:
  - [Ambiente de API](?path=docs/spanish/casos-principales/ambiente-api.md)
  - [Auditoría y Monitoreo](?path=docs/spanish/casos-principales/auditoria.md)
  - [Cargar Fondos](?path=docs/spanish/casos-principales/cargas.md)
  - [Controles de Tarjetas](?path=docs/spanish/casos-principales/controles-tarjeta.md)
  - [Emisión de Tarjetas Digitales](?path=docs/spanish/casos-principales/emision-tarjetas.md)
  - [Gestión de Clientes](?path=docs/spanish/casos-principales/gestion-clientes.md)
  - [Gestión de Cuentas](?path=docs/spanish/casos-principales/gestion-cuentas.md)
  - [Gestión de Tarjetas](?path=docs/spanish/casos-principales/gestion-tarjetas.md)
  - [HMAC Signature](?path=docs/spanish/casos-principales/hmac.md)
  - [Integración con el Sistema Falcon](?path=docs/spanish/casos-principales/integracion-falcon.md)
  - [Relación Cliente-Cuenta-Tarjeta](?path=docs/spanish/casos-principales/relacion.md)
- Descripción de API's mejorada:
  - /account/walletStatus version L8V1
  - /cards/details version L8V1
  - /account/transferP2P version L8V2
  - /cards/pin/invalid-attempts version L8V1

### Problemas solucionados

Endpoints se movieron a la versión 1.2.0:
  - /customer/v3/cards/details
  - /cards/v2/embosser/details

Endpoints se movieron a la versión 1.1.0:

  - /account/balance
  - /account/transfer
  - /account/QR-balance
  - /account/QR-transfer
  - /account/FL-transferP2P
  - /cards/embosser/details-L8VB

### Obsoleto

- /account/QRFL-balance
- /cards/instant-card-L8V7
- /transactions/organization-update
- /customer/v4/cards/details

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

### Obsoleto

- Portal anterior.

---

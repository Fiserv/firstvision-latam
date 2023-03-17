---
tags: [Release Notes, Janeiro, Fevereiro, Março ]
---

# Release Notes

## Março 2023

### O que há de novo?

- Documentação em espanhol!
- Documentação em português!
- Glossário da API

### Melhorias

- Lista VMX atualizada adicionando nome de endpoint.
- Documentação atualizada de casos principais:
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
- Melhoria de descrição das APIs:
  - /account/walletStatus versão L8V1
  - /cards/details versão L8V1
  - /account/transferP2P versão L8V2

### Problemas solucionados

Endpoints movidos para a versão 1.1.0:
- /account/balance
- /account/transfer
- /account/QR-balance
- /account/QR-transfer
- /account/FL-transferP2P

### Descontinuado

- /account/QRFL-balance
- /cards/instant-card-L8V7
- /transactions/organization-update

---

## Fevereiro 2023

### O que há de novo?

Novas API de Tokenização:
- /vtis/v1/tokenRequestors/{tokenRequestorID}/tokens/{tokenReferenceID}/deviceBinding
- /vtis/v1/getAvailableCards
- /vtis/v1/getSelectedCards
- /vtis/v1/pan/lifecycle
- /vtis/v2/tokenRequestors/{tokenRequestorID}/tokens/{tokenReferenceID}/tokenChanged
- /vtis/v1/tokenRequestors/{tokenRequestorID}/tokens/{tokenReferenceID}/lifecycle
- /vtis/v1/checkEligibility

### Melhorias

N/A

### Problemas solucionados

- N/A

### Descontinuado

- /account/card version R8V3

---

## Janeiro 2023

### O que há de novo?

Migração para o novo portal

### Melhorias

Códigos de erro, manipulação de erros e notificações.

### Problemas solucionados

- N/A

### Descontinuado

Antigo portal.

---

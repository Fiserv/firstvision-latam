---
tags: [Release Notes, Janeiro, Fevereiro, Março, Abril, Junho, Julho]
---


---

# Release Notes

## Julho

### O que há de novo?

- N/A

### Melhorias

Melhoria de descrição das APIs:
- /transactions/organization
- /transactions/pct-table
- /transactions/prepaid-logo
- /account/relationship/{relationshipNumber}/account
- /account/associatedParties
- /account/bankAccount
- /account/directDebit
- /account/{accountNumber}/credit-debit
- /account/v1/statementInstallments/{numberOfTerms}
- /cards/v3/embosser
- /transactions/non-monetary-action-code
- /customer/generation
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

Endpoints movidos para a versão 1.1.0:
- /account/balance
- /account/FL-balance

### Obsoleto
- /cards/embosser/encrypted-card-pan

---


# Release Notes

## Junho 2023

### O que há de novo?

- N/A

### Melhorias

Melhoria de descrição das APIs:
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

## Maio 2023

### O que há de novo?

- /account/v2/balance

### Melhorias

- Melhoria de descrição das APIs:
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

### O que há de novo?

- N/A

### Melhorias

- Melhoria de descrição das APIs:
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

Endpoints movidos para a versão 1.2.0:
- /account/balance
- /cards/embosser/encrypted-card-pan
- /account/v2/accounts

Endpoints moved to version 1.1.0:
- /account/details-L8VG

### Obsoleto

- /account/status-update-L8V1
- /account/details

---

## Março 2023

### O que há de novo?

- Documentação em espanhol!
- Documentação em português!
- Glossário da API

### Melhorias

- Lista VMX atualizada adicionando nome de endpoint.
- Documentação atualizada de casos principais:
  - [Ambiente API](?path=docs/português/principais-casos/ambiente-api.md)
  - [Auditoria e Monitoramento](?path=docs/português/principais-casos/auditoria.md)
  - [Carregar Fundos](?path=docs/português/principais-casos/carregar-fundos.md)
  - [Controles de Cartão](?path=docs/português/principais-casos/controles-cartão.md)
  - [Emissão de Cartões Digitais](?path=docs/português/principais-casos/emissão-cartões.md)
  - [Gestão de Cartões](?path=docs/português/principais-casos/gestão-cartões.md)
  - [Gestão de Clientes](?path=docs/português/principais-casos/gestão-clientes.md)
  - [Gestão de Contas](?path=docs/português/principais-casos/gestão-contas.md)
  - [HMAC](?path=docs/português/principais-casos/hmac.md)
  - [Integração com o Sistema Falcon](?path=docs/português/principais-casos/integração-falcon.md)
  - [Relacionamento Cliente-Conta-Cartão](?path=docs/português/principais-casos/relação.md)
- Melhoria de descrição das APIs:
  - /account/walletStatus versão L8V1
  - /cards/details versão L8V1
  - /account/transferP2P versão L8V2
  - /cards/pin/invalid-attempts version L8V1

### Problemas solucionados

Endpoints movidos para a versão 1.2.0:
- /customer/v3/cards/details
- /cards/v2/embosser/details

Endpoints movidos para a versão 1.1.0:
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

### Obsoleto

- /account/card version R8V3

---

## Janeiro 2023

### O que há de novo?

Migração para o novo portal

### Melhorias

Códigos de erro, manipulação de erros e notificações.

### Problemas solucionados

- N/A

### Obsoleto

Antigo portal.

---

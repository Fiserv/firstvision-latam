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

### Descontinuado

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

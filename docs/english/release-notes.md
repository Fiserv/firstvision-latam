---
tags: [Release Notes, January, February, March]
---

# Release Notes

## March 2023

### What's New?

- Spanish documentation!
- Portuguese documentation!
- API Glossary

### Enhancements

- VMX list updated adding endpoint name
- Main Cases documentation updated:
  - [Account Management](?path=docs/english/main-cases/account.md)
  - [API Environment](?path=docs/english/main-cases/api-environment.md)
  - [Audit and Monitoring](?path=docs/english/main-cases/audit.md)
  - [Card Controls](?path=docs/english/main-cases/card-controls.md)
  - [Card Management](?path=docs/english/main-cases/card.md)
  - [Customer Management](?path=docs/english/main-cases/customer.md)
  - [Digital Card Issuing](?path=docs/english/main-cases/digital.md)
  - [Falcon System Integration](?path=docs/english/main-cases/falcon.md)
  - [HMAC Signature](?path=docs/english/main-cases/hmac.md)
  - [Relation Client-Account-Card](?path=docs/english/main-cases/relation.md)
  - [Upload Founds](?path=docs/english/main-cases/uploads.md)
- API's description improvement:
  - /account/walletStatus version L8V1
  - /cards/details version L8V1
  - /account/transferP2P version L8V2

### Fixed

Endpoints moved to version 1.1.0:

- /account/balance
- /account/transfer
- /account/QR-balance
- /account/QR-transfer
- /account/FL-transferP2P

### Deprecated

- /account/QRFL-balance
- /cards/instant-card-L8V7
- /transactions/organization-update

---


## February 2023

### What's New?

New Tokenization API's

- /vtis/v1/tokenRequestors/{tokenRequestorID}/tokens/{tokenReferenceID}/deviceBinding
- /vtis/v1/getAvailableCards
- /vtis/v1/getSelectedCards
- /vtis/v1/pan/lifecycle
- /vtis/v2/tokenRequestors/{tokenRequestorID}/tokens/{tokenReferenceID}/tokenChanged
- /vtis/v1/tokenRequestors/{tokenRequestorID}/tokens/{tokenReferenceID}/lifecycle
- /vtis/v1/checkEligibility

### Enhancements

N/A

### Fixed

- N/A

### Deprecated

- /account/card version R8V3

---

## January 2023

### What's New?

- Migration to new portal

### Enhancements

- Error codes, error handling and notifications.

### Fixed

- N/A

### Deprecated

- Old portal.

---

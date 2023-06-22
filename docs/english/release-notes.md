---
tags: [Release Notes, January, February, March, April, May, June]
---

# Release Notes

## June 2023

### What's New?

- N/A

### Enhancements

API's description improvement:
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

### Fixed

- N/A

### Obsolete

- N/A

---

# Release Notes

## May 2023

### What's New?

- /account/v2/balance

### Enhancements

API's description improvement:
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

### Fixed

- N/A

### Obsolete

- /cards/global-card-activation

---

## April 2023

### What's New?

- N/A

### Enhancements

API's description improvement:
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

### Fixed

Endpoints moved to version 1.2.0:
- /account/balance
- /cards/embosser/encrypted-card-pan
- /account/v2/accounts

Endpoints moved to version 1.1.0:
- /account/details-L8VG

### Obsolete

- /account/status-update-L8V1
- /account/details

---

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
  - /cards/pin/invalid-attempts version L8V1

### Fixed

Endpoints moved to version 1.2.0:

- /customer/v3/cards/details
- /cards/v2/embosser/details

Endpoints moved to version 1.1.0:

- /account/balance
- /account/transfer
- /account/QR-balance
- /account/QR-transfer
- /account/FL-transferP2P
- /cards/embosser/details-L8VB

### Obsolete

- /account/QRFL-balance
- /cards/instant-card-L8V7
- /transactions/organization-update
- /customer/v4/cards/details

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

### Obsolete

- /account/card version R8V3

---

## January 2023

### What's New?

- Migration to new portal

### Enhancements

- Error codes, error handling and notifications.

### Fixed

- N/A

### Obsolete

- Old portal.

---

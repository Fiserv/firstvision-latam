---
tags: [Main Cases, API Test Environment, API Key]
---

# API Test Environment

## Overview

API test Environment: allows a new clients and prospects to use more than 150 different APIs currently implemented in the Portal.

All these APIs access a test environment, currently created for the FirstVision Solution, this environment has been implemented to allow new clients, prospects and developers to have a better understanding of the functionality, design and implementation of the API’s use.

The FirstVision testing environment for allows have different scenarios for Visa, MasterCard and AMEX products, such as credit cards, debit cards, prepaid cards and Multi-Wallets.

Each of these validation scenarios have been created for the regions of Colombia, Panama, Mexico, Argentina, Uruguay and Brazil, allowing customers in each of these regions to have a more real and accurate vision of how their products will work once. That these are implemented in the productive environment.

With the use of a key known as API-KEY, which can be requested by the customer, each API's can be addressed to test the franchise, product and region that is desired.

## Request sample


**POST** `/token`

Response example:

```json
{
    "token_type": "BearerToken",
    "issued_at": "11111111111111",
    "client_id": "ABC123ABC123ABC123",
    "access_token": "ABC123abc123ABC123abc123",
    "expires_in": "1799",
    "status": "approved"
}
```

## Diagram

![Diagram!](/assets/images/main-cases/api-test-environment_1.png "Diagram")

---

## See Also

- [Account Management](?path=docs/english/main-cases/account.md)
- [Audit and Monitoring](?path=docs/english/main-cases/audit.md)
- [Card Controls](?path=docs/english/main-cases/card-controls.md)
- [Card Management](?path=docs/english/main-cases/card.md)
- [Card Record](?path=docs/english/main-cases/record.md)
- [Cash-in/Cash-out](?path=docs/english/main-cases/cash-in-out.md)
- [Customer Management](?path=docs/english/main-cases/customer.md)
- [Digital Card Issuing](?path=docs/english/main-cases/digital.md)
- [Dynamic CVV2](?path=docs/english/main-cases/dynamic.md)
- [Falcon System Integration](?path=docs/english/main-cases/falcon.md)
- [HMAC Signature](?path=docs/english/main-cases/hmac.md)
- [PAN Token](?path=docs/english/main-cases/pan-token.md)
- [PIN Change](?path=docs/english/main-cases/pin-change.md)
- [Relation Client-Account-Card](?path=docs/english/main-cases/relation.md)
- [Upload Founds](?path=docs/english/main-cases/uploads.md)

---

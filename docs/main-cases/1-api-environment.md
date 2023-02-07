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

- [Upload Founds](?path=docs/main-cases/2-uploads.md)
- [Card Controls](?path=docs/main-cases/3-card-controls.md)
- [Relation Client-Account-Card](?path=docs/main-cases/4-relation.md)
- [Customer Management](?path=docs/main-cases/5-customer.md)
- [Account Management](?path=docs/main-cases/6-account.md)
- [Card Management](?path=docs/main-cases/7-card.md)
- [Card Record](?path=docs/main-cases/8-record.md)
- [Cash-in/Cash-out](?path=docs/main-cases/9-cash-in-out.md)
- [Falcon System Integration](?path=docs/main-cases/10-falcon.md)
- [Digital Card Issuing](?path=docs/main-cases/11-digital.md)
- [Pan Token](?path=docs/main-cases/12-pan-token.md)
- [Pin Change](?path=docs/main-cases/13-pin-change.md)
- [Dynamic CVV2](?path=docs/main-cases/14-dynamic.md)
- [Audit and Monitoring](?path=docs/main-cases/15-audit.md)
- [HMAC Signature](?path=docs/main-cases/16-hmac.md)
 
---

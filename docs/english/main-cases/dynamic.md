---
tags: [Main Cases, Dynamic CVV 2, cards, PIN, dynamic-values]
---

# Dynamic CVV 2

Use this API **CARDS/PIN/DYNAMIC-VALUE** to calculate and inquire a new CVV2 for not present card purchases.

Currently when card is emboss through the API CARD/EMBOSSER, the static CVV2 code is calculate and printed on sign panel on card back. The new functionality of Dynamic CVV2 allow to the cardholder call this API CARDS/PIN/DYNAMIC-VALUE to generate and calculate a new CVV2 before make a not present purchase. So when API is trigger the static CVV2 is inactivated and each time the cardholder wants to make a new not card present purchase the new CVV2 have to be calculated through this API.

**POST** `/cards/pin/dynamic-values`
    
Request body:

```json
{
  "cardNumber": "{{cardNumber}}",
  "channel": "I",
  "disableDCVV2": "N",
  "keyAssociation": "OV1",
  "organizationNumber": {{orgid}}
}
```
  
The description of each API field can be found within the specifications defined in the portal.

---

## See Also

- [Account Management](?path=docs/english/main-cases/account.md)
- [API Environment](?path=docs/english/main-cases/api-environment.md)
- [Audit and Monitoring](?path=docs/english/main-cases/audit.md)
- [Card Controls](?path=docs/english/main-cases/card-controls.md)
- [Card Management](?path=docs/english/main-cases/card.md)
- [Card Record](?path=docs/english/main-cases/record.md)
- [Cash-in/Cash-out](?path=docs/english/main-cases/cash-in-out.md)
- [Customer Management](?path=docs/english/main-cases/customer.md)
- [Digital Card Issuing](?path=docs/english/main-cases/digital.md)
- [Falcon System Integration](?path=docs/english/main-cases/falcon.md)
- [HMAC Signature](?path=docs/english/main-cases/hmac.md)
- [PAN Token](?path=docs/english/main-cases/pan-token.md)
- [PIN Change](?path=docs/english/main-cases/pin-change.md)
- [Relation Client-Account-Card](?path=docs/english/main-cases/relation.md)
- [Upload Founds](?path=docs/english/main-cases/uploads.md)

---

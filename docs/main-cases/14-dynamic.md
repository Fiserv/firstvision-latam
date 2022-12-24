# Dynamic CVV 2

Use this API **CARDS/PIN/DYNAMIC-VALUE** to calculate and inquire a new CVV2 for not present card purchases.

Currently when card is emboss through the API CARD/EMBOSSER, the static CVV2 code is calculate and printed on sign panel on card back. The new functionality of Dynamic CVV2 allow to the cardholder call this API CARDS/PIN/DYNAMIC-VALUE to generate and calculate a new CVV2 before make a not present purchase. So when API is trigger the static CVV2 is inactivated and each time the cardholder wants to make a new not card present purchase the new CVV2 have to be calculated through this API.

post /cards/pin/dynamic-values
    
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

- [API Environment](?path=docs/main-cases/1-api-environment.md)
- [Upload Founds](docs/main-cases/2-uploads.md)
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
- [Audit and Monitoring](?path=docs/main-cases/15-audit.md)
- [HMAC Signature](?path=docs/main-cases/16-hmac.md)

---

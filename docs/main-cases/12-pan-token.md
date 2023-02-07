---
tags: [Main Cases, Pan Token, cards, embosser]
---

# Pan Token

Currently when a customer is not certified by the Payment Card Industry (PCI), the card number cannot be showed on any web service, ATM, POS, etc.

To keep this security value safe, is require to use a PAN-TOKEN instead of card number, so when a card number is created, the current functionality generate the PAN-TOKEN as substitute of the card number.

The PAN-TOKEN is calculated automatically using a security KEY and it can has numeric and alphanumeric values.

PAN-TOKEN can be showed on a web service, ATM, POS, or any other device or service without compromise the real card number.

Pan token, can be visible using the API **CARDS/EMBOSSER/CARD-PAN-L8V2**, so the API user can get the PAN-TOKEN number sending the Card Number, in the API input message or can get the card number just sending the PAN-TOKEN number.

**POST** `/cards/embosser/card-pan-l8v2`

Request body:

```json
{
  "cardSequence": 1,
  "functionType": "C",
  "organizationNumber": {{orgid}},
  "cardNumber": "{{cardNumber}}"
}
```

The description of this API fields can be found within the specifications defined in the portal.

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
- [Pin Change](?path=docs/main-cases/13-pin-change.md)
- [Dynamic CVV2](?path=docs/main-cases/14-dynamic.md)
- [Audit and Monitoring](?path=docs/main-cases/15-audit.md)
- [HMAC Signature](?path=docs/main-cases/16-hmac.md)

---

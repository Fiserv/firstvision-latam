# Pin Change

Pin change is a currently functionality to allow the cardholder change you current card PIN, the reason for change the card pin can be because it is compromise, wants the change or it is required by the issuer each X number of days.

With this API **cards/pin/pin-change**, cardholder will be able to change his current pin number, for another pin number. At different of the API Update Pin of Card, this API will request the current PIN number assigned to the cardholder, so both values need to be added before trigger the API: Current Pin and New PIN.

This API can be used when cardholder need to change the current PIN number for another pin number just in case that this information is compromise. This API can be trigger from ATRM, VCR, APP, Web Service etc and is 100% on line.

Require values of this API are: Card Number, Channel, Current Pin Block, New Pin Block, Key Association (to encrypt Pin Blocks), new pin offset, and bank organization.

PUT /cards/pin/pin-change
    
Request body:

```json
{
  "cardNumber": "{{cardNumber}}",
  "channel": "W",
  "currPinBlock": "123ABC123ABC123",
  "keyAssociationNumber": "AV",
  "organizationNumber": {{orgid}},
  "pinOffset": "",
  "reqdPinBlock": "123ABC123A"
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
- [Dynamic CVV2](?path=docs/main-cases/14-dynamic.md)
- [Audit and Monitoring](?path=docs/main-cases/15-audit.md)
- [HMAC Signature](?path=docs/main-cases/16-hmac.md)

---

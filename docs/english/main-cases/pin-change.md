---
tags: [Main Cases, PIN Change, cards]
---

# PIN Change

PIN change is a currently functionality to allow the cardholder change you current card PIN, the reason for change the card PIN can be because it is compromise, wants the change or it is required by the issuer each X number of days.

With this API, cardholder will be able to change his current PIN number, for another PIN number. At different of the API Update PIN of Card, this API will request the current PIN number assigned to the cardholder, so both values need to be added before trigger the API: Current PIN and New PIN.

This API can be used when cardholder need to change the current PIN number for another pin number just in case that this information is compromise. This API can be trigger from ATRM, VCR, APP, Web Service etc and is 100% on line.

Require values of this API are: Card Number, Channel, Current PIN Block, New PIN Block, Key Association (to encrypt PIN Blocks), new PIN offset, and bank organization.

**PUT** `/cards/pin/pin-change`
    
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
- [Dynamic CVV2](?path=docs/english/main-cases/dynamic.md)
- [Falcon System Integration](?path=docs/english/main-cases/falcon.md)
- [HMAC Signature](?path=docs/english/main-cases/hmac.md)
- [PAN Token](?path=docs/english/main-cases/pan-token.md)
- [Relation Client-Account-Card](?path=docs/english/main-cases/relation.md)
- [Upload Founds](?path=docs/english/main-cases/uploads.md)

---

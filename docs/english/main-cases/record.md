---
tags: [Main Cases, Card Record, cards, embosser]
---

# Embosser Add

Use the API CARDS/EMBOSSER create a card information used to emboss a new card or plastic. This card information must have relate that an account number created through API ACCOUNT/ADD and this account number must be related a customer number created through API CUSTOMER/ADD.

This API allow add card information as card expiration date, service code, cardholder name, address to where the card will be deliver, spending limits, etc.

The card number is calculated on randomly way by the application, and this number will not generated again (duplicated).

**POST** `/cards/embosser/l8vf`

The description of each API field can be found within the specifications defined in the portal.

---

## See Also

- [Account Management](?path=docs/english/main-cases/account.md)
- [API Environment](?path=docs/english/main-cases/api-environment.md)
- [Audit and Monitoring](?path=docs/english/main-cases/audit.md)
- [Card Controls](?path=docs/english/main-cases/card-controls.md)
- [Card Management](?path=docs/english/main-cases/card.md)
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

---
tags: [Main Cases, Card Management, cards, embosser, PAN token, security-codes, PIN]
---

# Card Management

## Add Card Record

Use the API **CARDS/EMBOSSER** create a card information used to emboss a new card or plastic. This card information must have relate that an account number created through API **ACCOUNT/ADD** and this account number must be related a customer number created through API **CUSTOMER/ADD**.

This API allow add card information as card expiration date, service code, cardholder name, address to where the card will be deliver, spending limits, etc.

The card number is calculated on randomly way by the application, and this number will not generated again (duplicated).

**POST** `/cards/embosser/l8vf`

The description of each API field can be found within the specifications defined in the portal.

## Inquire Card or PAN token

Use this API **CARDS/EMBOSSER/CARD-PAN** to get the PAN-token calculated for a card number.

PAN token is a current functionality to tokenize the card number for all banks that are not a PCI certificate. When new card is created through API **CARD/EMBOSSER**, the PAN token is calculated automatically on base a parameters previously defined.

This API use the PAN-TOKEN to bring the card number or card number can be used to being the PAN-TOKEN.

**POST** `/cards/embosser/card-pan`

The description of each API field can be found within the specifications in the portal.

## Add or Update Massive Cards

This API **CARDS/MASS-CARD-ISSUE**, allow the user add or update a request to emboss new cards on massive way. These cards can be credit, debit or prepay card. Quantity of card to emboss is a parameter request by the API.

Cards embossed will not have an embosser name, but card number, expiration and card security values will be part of these.

**POST** `/cards/mass-card-issue-L8V3`

The description of each API field can be found within the specifications defined in the portal.

## Card Action Update

Use this API **CARDS/EMBOSSER/CARDACTION** to update the action flag used to re-emboss (re-issue) a specific card number.

This API allow to the user request a card reissue for some reason, lost/stolen, damage, card expiration, emergency replace, etc.

**PUT** `/cards/embosser/cardAction-L8V2`

The description of each API field can be found within the specifications defined in the portal.

## Instant Card

This API **CARDS/INSNTANT-CARD-L8V7** allow to the user request the creation of account and card on instantly way. Card information will be ready to be use for purchases.

Customer information have to be created through API **CUSTOMER/ADD** before call API instant card.

**POST** `/account/v2/instantCard`

The description of each API field can be found within the specifications defined in the portal.

## Inquiry Security Values

This API **CARDS/PIN/SECURITY-CODES**, allow to the user get the card security values (CVV, CVV2,ICVV, PIN number) already emboss for an specific card number.

Security values provided by the API will be encrypted using a security key of 32 bytes, so user should use the same security key and 3Des algorithm to decrypt the security values.

**POST** `/cards/pin/security-codes`

The description of each API field can be found within the specifications defined in the portal.

## Inquire Dynamic CVV2/CVC2/4CSC

Use this API **CARDS/PIN/DYNAMIC-VALUE** to calculate and inquire a new CVV2 for not present card purchases.

Currently when card is emboss through the API **CARD/EMBOSSER**, the static CVV2 code is calculate and printed on sign panel on card back. The new functionality of Dynamic CVV2 allow to the cardholder call this API **CARDS/PIN/DYNAMIC-VALUE** to generate and calculate a new CVV2 before make a not present purchase. So when API is trigger the static CVV2 is inactivated and each time the cardholder wants to make a new not card present purchase the new CVV2 have to be calculated through this API.

**POST** `/cards/pin/dynamic-values`

The description of each API field can be found within the specifications defined in the portal.

## Inquire Number of Invalid PIN Attempts

This API **CARDS/PIN/INVALID-ATTEMPTS** allow to the cardholder get the number of invalid PIN attempts.

As part of security parameters, the number of invalid PIN attempts are set up to avoid that PIN number can be calculated for frauds proposals. When this parameter is reached the PIN number is block and a new PIN number have to be calculated.

Invalid PIN attempts can be reached by many reasons the most popular reason is when cardholder fails the PIN number on ATM.

**POST** `/cards/pin/invalid-attempts`

The description of each API field can be found within the specifications defined in the portal.

## PIN Validation

Use this API **CARDS/PIN/VALIDATION** to confirm that current PIN generated is correct.

This API require the PIN block and the card number and not the clear PIN number.

**POST** `/cards/pin/validation`

The description of each API field can be found within the specifications defined in the portal.

---

## See Also

- [Account Management](?path=docs/english/main-cases/account.md)
- [API Environment](?path=docs/english/main-cases/api-environment.md)
- [Audit and Monitoring](?path=docs/english/main-cases/audit.md)
- [Card Controls](?path=docs/english/main-cases/card-controls.md)
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

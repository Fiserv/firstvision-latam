---
tags: [Main Cases, Cash-in/Cash-out, account, balance]
---

# Cash-in/Cash-out (account/balance)

Use this API **ACCOUNT/BALANCE** to apply a money amount from a Bank Branch, ATM, Web service etc, this money transfer does not make a debit from an existing account of credit, debit, or prepay, just this API post an specific money amount to a destination account.

Use API parameters to allow that money transfer can be ready to use after API was call or wait until next day.

**PUT** `/account/balance`
            
Request body:

```json
{
  "asmOrganizationNumber": 970,
  "accountNumber": "9704010000000001467",
  "representativeId": "A",
  "transactionData": {
    "actionCode": "FUND",
    "cardNumber": "0004444440000000558",
    "cardSequence": 123,
    "description": "CASH_IN_VIA_CARD",
    "effectiveDate": "2021-11-20",
    "otbUpdateIndicator": 1,
    "planNumber": 1,
    "planSequence": 1,
    "referenceNumber": 123,
    "resolutionReferenceNumber": 123,
    "storeNumber": 1,
    "transactionAmount": 200
  }
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
- [Falcon System Integration](?path=docs/main-cases/10-falcon.md)
- [Digital Card Issuing](?path=docs/main-cases/11-digital.md)
- [Pan Token](?path=docs/main-cases/12-pan-token.md)
- [Pin Change](?path=docs/main-cases/13-pin-change.md)
- [Dynamic CVV2](?path=docs/main-cases/14-dynamic.md)
- [Audit and Monitoring](?path=docs/main-cases/15-audit.md)
- [HMAC Signature](?path=docs/main-cases/16-hmac.md)

---

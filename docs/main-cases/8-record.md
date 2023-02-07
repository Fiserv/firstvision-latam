---
tags: [Main Cases, Card Record, cards, embosser]
---

# Add Card Record (cards/embosser/)

Use the API CARDS/EMBOSSER create a card information used to emboss a new card or plastic. This card information must have relate that an account number created through API CCOUNT/ADD and this account number must be related a customer number created through API CUSTOMER/ADD.

This API allow add card information as card expiration date, service code, cardholder name, address to where the card will be deliver, spending limits, etc.

The card number is calculated on randomly way by the application, and this number will not generated again (duplicated).

**POST** `/cards/embosser`

Request body:

```json
{
  "addressLine1": "ADDRESS LINE 1",
  "addressLine2": "ADDRESS LINE 2",
  "assignedSpendingLimits": {
    "maximumSpendingLimit": 0,
    "spendingFrequency": 0,
    "spendingTransaction": 0
  },
  "atmCashAmount": 0,
  "atmCashNumber": 0,
  "atmCashSingleTransactionLimit": 0,
  "authorizationCriteriaTableNumber": "",
  "authorizationSpendingLimitTable": "",
  "blockCode": "",
  "branchNumber": 0,
  "cardAction": 1,
  "cardActionReasonCode": "",
  "cardDelayDays": 0,
  "cardNumber": "",
  "cardSequence": 1,
  "cardholderAffiliationGroupId": "",
  "cardholderFlag": "",
  "city": "CABA",
  "currentCardActivation": "",
  "customerNumber": "",
  "deliveryOption": 0,
  "deviceIndicator": "",
  "embossedName1": "Sivale TESTING 1",
  "embossedName2": "",
  "enrollmentStatusVBV": " ",
  "expirationDate": "",
  "firstIssueBranch": 0,
  "internetPurchaseAmount": 0,
  "internetPurchaseNumber": 0,
  "internetPurchaseSingleTransactionLimit": 0,
  "languageCode": "ENG",
  "maximumAuthorizationFrequency": 0,
  "name1": "Pavan",
  "name1TypeIndicator": 0,
  "name2": "",
  "name2TypeIndicator": 0,
  "nextCardExpirationDate": "",
  "numberOfCardsRequested": 1,
  "organizationNumber": {{orgid}},
  "overTheCounterCashAmount": 0,
  "overTheCounterCashNumber": 0,
  "overTheCounterCashSingleTransactionLimit": 0,
  "pinMailerDelayDays": 0,
  "pinOffset": 0,
  "pinSuppression": 0,
  "plasticId": "",
  "posServiceCode": 101,
  "postToAccount": "{{accountNumber}}",
  "postalCode": 38585,
  "processType": 0,
  "programId": 0,
  "reissueDeliveryOption": 0,
  "requestedCardType": "",
  "retailPurchaseAmt": 0,
  "retailPurchaseNumber": 0,
  "retailPurchaseSingleTransactionLimit": 0,
  "securedCodeActivate": 0,
  "stateOrProvince": "BA",
  "typeCardMailer": "",
  "typeOfCard": "",
  "user1": 1,
  "user2": 2,
  "user3": 3,
  "user4": 4,
  "user5": 5,
  "user6": 6,
  "user7": 7,
  "user8": 8,
  "userDate1": "",
  "userDate2": "",
  "vbvPassword": "",
  "visaMiniIndicator": "0",
  "visaPlusIndicator": " "
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
- [Cash-in/Cash-out](?path=docs/main-cases/9-cash-in-out.md)
- [Falcon System Integration](?path=docs/main-cases/10-falcon.md)
- [Digital Card Issuing](?path=docs/main-cases/11-digital.md)
- [Pan Token](?path=docs/main-cases/12-pan-token.md)
- [Pin Change](?path=docs/main-cases/13-pin-change.md)
- [Dynamic CVV2](?path=docs/main-cases/14-dynamic.md)
- [Audit and Monitoring](?path=docs/main-cases/15-audit.md)
- [HMAC Signature](?path=docs/main-cases/16-hmac.md)

---

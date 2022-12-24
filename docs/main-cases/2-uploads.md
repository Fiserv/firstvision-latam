---
tags: [Main Cases, Upload Founds From a Source Account, Account, Balance, Peer-to-Peer]
---

# Upload Founds From a Source Account

## Definition

Through API'S currently created and located in the portal, it is possible to load money from a Debit account to a Credit or Prepaid account, moving money from a Credit account to a Debit or Prepaid account or carry out charges of money from a prepaid account to another prepaid account.

These APIs are designed to allow potential customers, customers and developers to test online and directly in a real testing environment, if you haven't already set up your testing environment.

Each API will allow load money from different source products to different destination products. With the use of the different options or parameters, these APIs control, credit and debit the money from the source and the money receiver for each account, allowing online updates or not of the available credit use by the card, according to the parameter defined in the API before it is trigger.

## Purpose

The creation of Credit, Debit, and Prepaid accounts are a requirement that must be completed before execute any of the APIs used to load money. Which must be created using the APIs for Customer Creation (Customer/Add), Account Creation (Account/Add) and Card Creation (Embosser/Add).If you have any questions.

However, depending on the values ​​used in the APIS, it is also possible to load money using direct financial amounts, received in cash from a bank branch.

## Use Case

![Use case!](/assets/images/main-cases/add-funds-from-origin-account.png "Use case")

### 1. Adjust Account Balance (Account/Balance)

The use of this API allows you to load money to a Debit, Credit, Prepaid and Wallet product, using the parameters defined in the Portal. This API takes as a source the cash received from an agency or bank branch, and will apply these funds. These funds can be in local or foreign currency. As part of its functions, this API allows to indicate through its parameters, if the money deposited to the account can be used immediately or not.

PUT /account/balance
      
Request body:

```json
{
  "asmOrganizationNumber": {{orgid}},
  "accountNumber": "{{accountNumber}}",
  "representativeId": "A",
  "transactionData" : {
    "actionCode": "FUND",
    "cardNumber": "{{cardNumber}}",
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

### 2. Adjust Account Balance Peer-to-Peer (Account/QRFL-Balance)

This API allows you to load money from an existing Credit, Debit, Prepaid or Wallet account, to a new destination account of any of the products indicated above.

Through the indicated parameters, it is possible to identify the account, product card from which the withdrawal of money (debit) is being made and define the account and card to which the credit will be made, it is also required as part of the API parameters, add the geographic location (latitude and longitude) of the source (sender) that is loading money. The card number from which you receive the money (receiver) is required as part of the parameters required by the API.

PUT /account/QRFL-balance
      
Request body:

```json
{                                             
  "accountNumber": "{{accountNumber}}",
  "organizationNumber": {{orgid}},                       
   "transactionData": {                        
    "actionCode": "000",                     
    "authorizationCode": "123123",                             
    "description": "Description",             
    "effectiveDate": "2021-02-15",            
    "memoPostedIndicator": " ",               
    "n1n2ByPass": "N",                                      
    "suppressMonetaryTransaction": "Y",       
    "transactionAmount": 1,  
    "box": 1,                                   
    "crPlaza": "10m00",                         
    "crStore": "500d",                         
    "identifier": "0x00"            
  }                      
}
```

The description of each API field can be found within the specifications defined in the portal.

## Sequence Diagram

### Adjust Account Balance (Account/Balance)

![Sequence diagram!](/assets/images/main-cases/adjust-account-balance.png "Sequence diagram")

### Adjust Account Balance Peer-to-Peer (Account/QRFL-Balance)

![Sequence diagram!](/assets/images/main-cases/adjust-account-balance-peer-to-peer.png "Sequence diagram")


---

## See Also

- [API Environment](?path=docs/main-cases/1-api-environment.md)
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

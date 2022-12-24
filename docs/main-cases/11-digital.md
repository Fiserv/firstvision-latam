---
tags: [Main Cases, Digital Card Issuing]
---

# Digital Card Issuing

## Definition

The following section aims to define the issuance of a digital card on the FirstVision platform.

A digital card will behave like a wallet funded by the account's credit limit and customers can make e-commerce purchases (with the co-branded retailer only) using the digital wallet instead of using a physical card. A single FirstVision account can have a physical credit card and a digital card as separate embossers. Accounts can be boarded to have physical card only or a digital card only or have both.

## Purpose

The purpose of this user case is to issue a new digital card to a customer on the FirstVision platform.

## Use Case

The user case below determines the actions required to issue a new digital card.

![image](https://user-images.githubusercontent.com/111396588/208847157-3b0caa4b-f73d-469a-8cb6-7461af6317a3.png)

## Sequence Diagram

![image](https://user-images.githubusercontent.com/111396588/208847202-038f4634-9a8b-4de2-8446-028b386e1211.png)

To issue a new digital card to a customer, we must follow these steps:

### 1. Customer ADD

This request includes the customer's personal data, demographic information and other information pertaining to the entity. The response to this request will bring the customer number created. See more about the Customer API:

POST /customer
      
Request body: 

```json
{
  "customerData": {
    "customerKeyData": {
      "accountNumber": 9704010000000002000,
      "coOwnerIndicator": 1,
      "dualFlag": 0
    },
    "customerMiscellaneousData": {
      "vipStatus": 1
    },
    "ownerCoOwnerData": {
      "coOwnerData": {},
      "ownerData": {
        "city": "BUENOS AIRES",
        "contactIndicator": 12,
        "countryCode": "ARG",
        "county": "CABA",
        "dateOfBirth": "2010-09-11",
        "demographic1": "USER DEMO 1",
        "demographic2": "USER DEMO 2",
        "demographic3": "USER DEMO 3",
        "driverLicenseCountry": "",
        "driverLicenseNumber": "123421",
        "driverLicenseState": "",
        "email": "ABC.DEF@yahoo.com",
        "emailFlag": 1,
        "employerAddress1": "EMP ADDR L1",
        "employerAddress2": "EMP ADDR L2",
        "employerExtensionPhoneNumber": 123456,
        "employerName": "FISERV",
        "employerPhoneFlag": 1,
        "employerPhoneNumber": "123-456-7890",
        "faxPhoneFlag": 1,
        "firstName": "Pavan",
        "foreignIndicator": "A",
        "genderCode": 1,
        "homeFaxPhoneNumber": "223-456-7890",
        "homePhoneFlag": 1,
        "homePhoneNumber": "123-456-9990",
        "houseAddress1": "OWN ADDR L19",
        "houseAddress2": "OWN ADDR L29",
        "houseAddress3": "OWN ADDR L39",
        "houseAddress4": "OWN ADDR L49",
        "houseName": "Could be apartment's name",
        "houseNumber": 12349,
        "identificationNumber": 123456789,
        "identificationNumberFlag": 2,
        "languageIndicator": "ENG",
        "lastName": "Sivale",
        "mailingList": 1,
        "maritalStatus": 1,
        "memo1": "Memo 1",
        "memo2": "Memo 2",
        "middleName": "",
        "mobilePhoneFlag": 1,
        "mobilePhoneNumber": "323-456-7890",
        "nameLine1": "string",
        "nameLine2": "OWN NAME L2 TEST9",
        "nameLine3": "OWN NAME L3",
        "nameTypeIndicator1": 0,
        "nameTypeIndicator2": 1,
        "nameTypeIndicator3": 1,
        "numberOfDependents": 999,
        "ownOrRentResidenceFlag": 2,
        "position": "CEO",
        "relativeName": "Relative Name",
        "smsFlag": 1,
        "state": "BA",
        "statementMessageIndicator": 1,
        "suffix": "Sr"
      }
    }
  },
  "resvData": {}
}
```
 
### 2. Account ADD

With the customer number created in the previous requisition, this requisition will propagate the account's credit limit information, payment cycle date, short name and more information inherent to the entity. See more about the Account API:

POST /account
          
Request body: 

```json
{
  "accountData": {
    "billingCurrency": 0,
    "billingCycle": 31,
    "billingLevel": 1,
    "blockCode1": "",
    "cardholderAffiliationGroup": 0,
    "creditLimit": 10000,
    "customerNumber": "9704010000000001467",
    "customerSelectedDueDay": 0,
    "dualBillingFlag": 0,
    "issuanceId": "",
    "logo": 401,
    "organization": 970,
    "owningBranch": 999999998,
    "prepaidPlanNumber": 0,
    "processingControlTable": {
      "level": "O",
      "startDate": "",
      "tableId": ""
    },
    "qualification": "A",
    "relationshipNumber": "",
    "residenceId": "1",
    "shortName": "Vishal",
    "sourceCode": "sourceCode",
    "statement": "1",
    "statementFrequency": 0,
    "userAccountNumber": "",
    "userData": {
      "userApplication1": "12"
    },
    "miscUserData": {
      "miscUser6": "",
      "miscUser8": ""
    }
  }
}
```
  
### 3. Embosser ADD

This request is responsible for adding the information to the issuing digital card. This request requires both the customer code and the account code. See more about the Embosser API:

POST /cards/embosser
          
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
  "organizationNumber": 970,
  "overTheCounterCashAmount": 0,
  "overTheCounterCashNumber": 0,
  "overTheCounterCashSingleTransactionLimit": 0,
  "pinMailerDelayDays": 0,
  "pinOffset": 0,
  "pinSuppression": 0,
  "plasticId": "",
  "posServiceCode": 101,
  "postToAccount": "9704010000000001467",
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

### 4. Card ACTIVATION

After customer, account and embosser requests, the new card settings for the customer are applied, but not active for use. This request will activate the card and make it ready for use. See more about the Card Activation API:

PUT /customer
          
Request body: 

```json
{
  "addressLine1": "PORT OF MIAMI",
  "addressLine2": "117 E PARKWAY AVE",
  "adminBranchNumber": 0,
  "cardNumber": "0004444440000000558",
  "cardSequence": 1,
  "cardholderAffiliationGroupId": 12348,
  "cardholderFlag": 0,
  "cardholderName1": "RUN DMC",
  "cardholderName2": "",
  "cardholderType": 1,
  "city": "Miami",
  "customerNumber": "",
  "embossedName1": "MY NAME IS",
  "embossedName2": "KIT-KAT WALLER",
  "firstIssueBranchNumber": 0,
  "foreignUseIndicator": 0,
  "issueDeliveryOption": 1,
  "languageCode": "ENG",
  "organizationNumber": 970,
  "postalCode": 123456,
  "reissueDeliveryOption": 1,
  "stateOrProvince": "FL",
  "user1": 1,
  "user2": 2,
  "user3": 3,
  "user4": 4,
  "user5": 5,
  "user6": 6,
  "user7": 7,
  "user8": 8,
  "userDate1": "2020-03-03",
  "userDate2": "2020-03-03"
}
```

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
- [Pan Token](?path=docs/main-cases/12-pan-token.md)
- [Pin Change](?path=docs/main-cases/13-pin-change.md)
- [Dynamic CVV2](?path=docs/main-cases/14-dynamic.md)
- [Audit and Monitoring](?path=docs/main-cases/15-audit.md)
- [HMAC Signature](?path=docs/main-cases/16-hmac.md)

---

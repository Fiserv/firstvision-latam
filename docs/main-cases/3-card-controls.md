---
tags: [Main Cases, Card Controls, Block or Unlock Card, Cards/Embosser/Block, Update Spending Limits, Cards/Spend-Limits, Update Travel Indicator, Cards/Travel, Card Transfer Update, Cards/Transfer), Active Card, Cards/Activation, Update Pin of Card, Cards/Pin, Pin Block/Unblock , Cards/Pin/Status, Change the Pin of a Card, Cards/Pin/Pin-Change]
---

# Card Controls

This section describes the different APIs in the Portal used to take actions on the different activities related to the use of the credit, debit, prepaid or wallet card, for any of the Visa, Master Card or American Express products. Next, a description of the functionalities and characteristics of API.

As a main requirement, is important that Credit, Debit, Prepay or Wallet cards have been created in the test environment as it was detailed in section 1.0 of this document, using the API's for customer creation (Customer / Add), creation of Account (Account / Add) and Creation of Card (Embosser / Add).

## Block or Unlock Card (Cards/Embosser/Block)

Through this API, the cardholder will be able to make preventive and definitive blocks on the credit card information, debit, prepaid and wallet. In order to prevent any possible fraud when the cardholder suspects that card information may be compromised.

On same way, the cardholder may carry out a preventive unlocking of his card when he is sure that the information on his card is not compromised.

Information required by the API as the card number, block code, and function must be included before API trigger.

The description of each API field can be found within the specifications defined in the portal.

PUT /cards/embosser/block
        
Request body:

```json
{
  "blockCode": "Z",
  "cardNumber": "0004444440000000558",
  "cardSequence": 1,
  "functionCode": "B",
  "organizationNumber": 970
}
```

## Update Spending Limits (Cards/Spend-Limits)

This API allows the customer to update online, the different spending limits associated with credit, debit, prepaid and Wallet cards. These spending limits are assigned for purchases, cash advances, internet purchases and international purchases. Spending limits assign the number of transactions and maximum amounts allowed for use on a daily, weekly, biweekly, and monthly basis.These spending limits can be assigned to the main card as well as to additional cards.

The values are modified 100% online and can be adjusted as many times as required.

The API Card/Spend-Limits, requests as required information, the card number, transaction number and amounts for each spending limit.

The description of each API field can be found within the specifications defined in the portal.

PUT /cards/spend-limits

Request body:

```json
{
  "automatedTellerMachineCashAmount": 10000,
  "automatedTellerMachineCashNumber": 3,
  "automatedTellerMachineCashSingleTransactionLimit": 3123232,
  "cardNumber": "0004444440000001309",
  "cardSequence": 1,
  "foreignUse": 0,
  "frequency": 1,
  "globalSpendingLimitNumber": 99999999,
  "globalSpendingLimitAmount": 100000000000000000,
  "globalSpendingLimitForSingleTransaction": 100000000000000000,
  "internetPurchaseAmount": 213456,
  "internetPurchaseNumber": 9,
  "internetPurchaseSingleTransactionLimit": 123456,
  "logoThreshIndustry": 1,
  "organizationNumber": 970,
  "overTheCounterCashAmount": 123112,
  "overTheCounterCashNumber": 9,
  "overTheCounterCashSingleTransactionLimit": 121345,
  "retailPurchaseAmount": 415678,
  "retailPurchaseNumber": 81,
  "retailPurchaseSingleTransactionLimit": 121332,
  "spendLimitsStatusIndicator": 0
}
```

## Update Travel Indicator (Cards/Travel)

Through the API Card/Travel, the cardholder will be able to define the destinations, outside their country, where the credit card will be used. This API activates online the dates and countries to which the cardholder is traveling in the coming months.

In the event that the card is used in a country or date range that has not been defined by this API, the authorization request will be rejected with the response: “Transaction not allowed”.

This API allows the cardholder define the range of dates and countries where the card will be used, it also allows him to modify and delete countries and dates already defined.

The values required by the API are the card number, ISO code of the country, start and end date range, allowing up to a maximum of five countries to visit with their respective date ranges

The description of each API field can be found within the specifications defined in the portal.

PUT /cards/travel

Request body:

```json
{
  "cardNumber": "0004444440000000558",
  "cardSequence": 1,
  "foreignUseIndicator": 1,
  "organizationNumber": 970,
  "travel": [
    {
      "country": "ARG",
      "endDate": "2020-10-10",
      "startDate": "2020-09-09"
    },
    {
      "country": "ARG",
      "endDate": "2020-10-10",
      "startDate": "2020-09-09"
    }
  ],
  "travelIndicator": 1,
  "travelIndicatorOccurrence": 1
}          
```

## Card Transfer Update (Cards/Transfer)

This API allow the cardholder blocks their current card number and request a new card with different card number in only one trigger. Same that API Block or Unlock Card, card number can be blocked just in case cardholder believes that card information is compromise and at same time he can request a new card number, so new card will be embossed during batch process and will be ready to be deliver on next day.

As part of values requested by the API Cards/Transfer, is required the card number, account number, organization and effective date.

The description of each API field can be found within the specifications defined in the portal.

PUT /cards/transfer

Request body:

```json
{
  "accountNumberBase": 9704010000000002000,
  "blockCode": "S",
  "cardNumber": "0004444440000000558",
  "customerOrg": 970,
  "effectiveDate": "2019-08-12",
  "function": "T",
  "logo": 401,
  "operatorId": "VFM",
  "organizationNumber": 970,
  "processType": 0,
  "reasonCode": "A",
  "startDate": "2019-08-30",
  "terminalId": 1,
  "transferRepresentative": 0,
  "transferToAccount": "9706010000000000274",
  "transferToCustomer": "9704010000000001467"
}
```

## Active Card (Cards/Activation)

The API CARS/ACTIVATION activates a card already embossed. This API allow to the cardholder activate a new card number when it is received by mail or deliver in a bank branch. Card Activation date will be saved on test environment for audit reasons.

If cardholder try use the card for purchase or cash advance, before it is activate, the authorization request will be rejected with reject reason “Card is not Activate”, so cardholder will be able to active his card just triggering this API.

This API should be trigger each time that a new card is embossed (principal or additional), to activate each card embossed.

Require values for this API are: Card Number, bank product identification (organization) and service type (A= Activation).

PUT /cards/activation
    
Request body:

```json
{
  "cardNumber": "{{cardNumber}}",
  "organizationNumber": {{orgid}},
  "serviceType": "S",
  "userData": ""
}
```

The description of each API field can be found within the specifications.


## Update Pin of Card (Cards/Pin)

This API CARDS/PIN, allows to the cardholder reassign a new personal identification number (PIN). Normally used when new card is deliver to the cardholder and new pin needs to be setup and linked to the new card already activated using the API Cards/Activation.

The API reassign and update the new PIN 100% on line so cardholder can use the new PIN after it was assigned. This API can be trigger from different channels as ATM, web pages, VCR, APP, etc. Cardholder will choose the new four digits pin and along with credit card number and Key Association (used to encrypt the new API) the bank application should be able to calculate the new Pin Block to trigger the API.

The values required for this API are: Card Number, bank organization, channel, Pin Block and Key association.

PUT /cards/pin/
      
Request body:

```json
{
  "cardNumber": "{{cardNumber}}",
  "channel": "W",
  "keyAssociationNumber": "MOX",
  "newPinBlock": "ABC123ABC123ABC123",
  "organizationNumber": {{orgid}}
}
```

The description of each API field can be found within the specifications.


## Pin Block/Unblock (Cards/Pin/Status)

The API cards/pin/status is being used by a cardholder to block his current PIN number, it can be used when he believes that PIN information can be compromise. This API only block the pin number and not the card number, so customer after trigger this API to block the PIN, he can still using the card for purchases but not for cash advances.

Using same API, cardholder is able the un-block a pin number already blocked, just triggering the API with a different value on field Function Code.

Another function of this API, allow the cardholder unblock a card PIN when it was already blocked by exceed of pin tries from ATM.

Values require by this API are: Card number, channel, bank organization and service function.

PUT /cards/pin/status
        
Request body:

```json
{
  "cardNumber": "{{cardNumber}}",
  "cardSequenceNumber": 1,
  "channel": "W",
  "organizationNumber": {{orgid}},
  "serviceFunctionCode": "U"
}
```

The description of each API field can be found within the specifications.


## Change the Pin of a Card (Cards/Pin/Pin-Change)

With this API cards/pin/pin-change, cardholder will be able to change his current pin number, for another pin number. At different of the API Update Pin of Card, this API will request the current PIN number assigned to the cardholder, so both values need to be added before trigger the API: Current Pin and New PIN.

This API can be used when cardholder need to change the current PIN number for another pin number just in case that this information is compromise. This API can be trigger from ATRM, VCR, APP, Web Service etc and is 100% on line.

Require values of this API are: Card Number, Channel, Current Pin Block, New Pin Block, Key Association (to encrypt Pin Blocks), new pin offset, and bank organization.

PUT /cards/pin/pin-change
          
Request body:

```json
{
  "cardNumber": "{{cardNumber}}",
  "channel": "W",
  "currPinBlock": "ABC123ABC123",
  "keyAssociationNumber": "AV",
  "organizationNumber": {{orgid}},
  "pinOffset": "",
  "reqdPinBlock": "ABC234ABC234"
}
```

The description of each API field can be found within the specifications.


---

## See Also

- [API Environment](?path=docs/main-cases/1-api-environment.md)
- [Upload Founds](docs/main-cases/2-uploads.md)
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

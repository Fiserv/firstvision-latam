# Cash-in/Cash-out(account/balance)

Use this API **ACCOUNT/BALANCE** to apply a money amount from a Bank Branch, ATM, Web service etc, this money transfer does not make a debit from an existing account of credit, debit, or prepay, just this API post an specific money amount to a destination account.

Use API parameters to allow that money transfer can be ready to use after API was call or wait until next day.

PUT /account/balance
            
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

# Account Management

## Account Add (account/)

This API ACCOUNT/ allow add all the Account information for any product of credit, debit, prepay and Wallet. Information as credit limit, billing cycle, Customer Short Name, account block codes, customer number, card tech etc can be added as part of this API fields.

Account number is a unique number that is different than card number, account number is a number created by the system on randomly way.

This API needs the customer number as a require value before the API can be trigger. This customer number is provide when API CUSTOMER/ADD is trigger to add demographic information.

The description of each API field can be found within the specifications defined in the portal.

/account

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

## Find Account Balance (account/balance/details)

This API ACCOUNT/BALANCE/DETAIL, can be used by the cardholder to get the information about account current balance. Using the account number as search parameter, API will show the account current balance, available credit, cash balance, credit limit, etc. in the API output message.

This API will show the account balances information on real time, on inquiry mode, so no account balance values can be update.

This API use the account number already assigned when API ACCOUNT/ADD was trigger.

The description of each API field can be found within the specifications defined in the portal.

/account/balance/details

Request body:

```json
{
  "accountNumber": "9704010000000001467",
  "organizationNumber": 970
}
```

## Temporary Credit Limit Update (cards/temporary-credit-limit)

Use this API CARDS/TEMPORARY-CREDIT-LIMIT to increase the account credit limit for a specific number of days. This API is very useful when cardholder does not have more available credit limit and he request a credit limit increase for a specific number of day, so when time limit is complete, the original credit limit is set back as current credit limit.

This API use the account number as search parameter and values as account credit limit, new credit limit and increase expiration date needs to be set up before the API be trigger.

The description of each API field can be found within the specifications defined in the portal.

/cards/temporary-credit-limit

Request body:

```json
{
  "accountOrCardNumber": 4099854036361291300,
  "currentCreditLimit": 300000000,
  "foreignUse": 1,
  "organizationNumber": 807,
  "tempCreditLimitExpDate": "2021-07-01",
  "temporaryCreditLimit": 300000001
}
```

## Block & Unblock Account (account/block-code)

This API ACCOUNT/BLOCK-CODE can be used by the cardholder to block/unblock the account, not the card. Currently as part of First Vision functionality, a cardholder, need to have the customer information, account information and card information already created through API’s Customer/ADD, Account/ADD and Card/ADD.

The use of this API, blocks the account for any reason, with more than 25 types of block codes already defined at product level, so depending of block code trigger in the API, all the card under this account number can be blocked automatically to avoid authorizations approve.

For Block Codes functionality please refer to CMS Screen Guide.

Account number is a require value to trigger this API.

The description of each API field can be found within the specifications defined in the portal.

/account/block-code

Request body:

```json
{
  "accountNumber": "9704010000000001467",
  "blockCode": "Z",
  "blockCodeIndicator": 1,
  "foreignUse": 0,
  "functionCode": "B",
  "organizationNumber": 970
}
```

## Account to Card Details (account/card)

The API ACCOUNT/CARD allow a user to find out all the cards already created under an account number. With only the Account number provided as input for a dual currency Account, the API call will return the Card number for the local Account. If the Organization number is provided in the input, the response provides the card numbers associated with that Organization, whether it is local or foreign Organization.

To trigger this API, the account number information and card information have to be created previously using the API’s CUSTOMER/ADD, ACCOUNT/ADD and CARD/ADD.

This API will show all the cards created under the account number, principal card and additional cards.

The description of each API field can be found within the specifications defined in the portal.

/account/card

Request body:

```json
{
  "accountNumber": "9704010000000001467",
  "organizationNumber": 970
}
```

## Credit Bureau

This API ACCOUNT/CREDITBUREAU, allows a user to update the credit bureau fields at account level, so the account will be add into Credit Bureau report generated on daily basis. This report is been use to inform to a Credit Bureau institution about the cardholder credit situation and classification.

This API uses the account number and a flag to indicate if the account is added into the Credit Bureau report.

The description of each API field can be found within the specifications defined in the portal.

/account/creditBureau

Request body:

```json
{
  "accountNumber": "5303716028446103276",
  "bureauDate": "2020-02-28",
  "creditBureauSpecificComment": "Y",
  "foreignUse": 0,
  "organizationNumber": 807
}
```

## Update Customer Number (Account/Customer)

The API ACCOUNT/CUSTOMER allow a user to change the customer number already link to a specific account information.

Currently when an account information is created on the test environment through API ACCOUNT/ADD, is require add the customer number created through API CUSTOMER/ADD. This link is require to link a customer with an account created.

With API ACCOUNTS/CUSTOMER is possible remove this link and make a different link between the account number and a different customer number already created on test environment.

This API use the account number as search parameter and an existing customer number that will be use to establish a new link.

The description of each API field can be found within the specifications defined in the portal.

/account/customer

Request body:

```json
{
  "accountNumber": "9704010000000001467",
  "alternateCustomer": {
    "expirationDate": "",
    "status": "0"
  },
  "customerNumber": "9704010000000001467",
  "customerTypeIndicator": 0,
  "foreignUseIndicator": 0,
  "organizationNumber": 970,
  "qualification": "2"
}
```

## Find Account Detail (account/details)

The API ACCOUNT/DETAIL allow a user the get all the account information previously added through the API ACCOUNT/ADD in a test environment, this account information is received in API response message after the API is called.

Information as account status, customer number, account block codes, credit limit, waive flags, etc, will be display with this API.

This API require the account number as search parameter along with banj id (organization).

The description of each API field can be found within the specifications defined in the portal.

/account/details

Request body:

```json
{
  "accountNumber": "9704010000000001467",
  "foreignUse": 0,
  "organizationNumber": 970
}
```

## Account to Account funds Transfer (account/transferP2P)

This API ACCOUNT/TRANSFERP2P allows a user to transfer a specific amount of money PEER TO PEER, between two different accounts: from credit to debit, from debit to debit, from credit to prepay or from debit to prepay, wallets etc.

This transfer can be immediately, so account receiver can use the money after API is called or can be on next day, this depend of the API parameters.

After call this API, a debit and credit transactions are created for source and destination accounts.

This API use the account number for source account and account number for destination.

The description of each API field can be found within the specifications defined in the portal.

/account/FL-transferP2P

Request body:

```json
{
  "asmRepId": "X01",
  "effectiveDate": "2020-11-03",
  "organizationNumber": 970,
  "referralOption": "",
  "referralRepID": "",
  "transactionAmount": 1,
  "updateIndicator": 1,
  "from": {
      "accountNumber": "9704010000000001467",
      "accountOrganizationNumber": 970,
      "actionCode": "8001",
      "actionCodePriority": "1",
      "authorizationCode": "1432",
      "cardNumber": "",
      "cardSequence": 1,
      "currencyNumber": "",
      "departmentCode": "PPLD",
      "foreignUse": "0",
      "institutionNumber": 13,
      "insuranceCode": "12",
      "letterCode": "",
      "letterOrganizationNumber": 970,
      "planNumber": 60000,
      "planSequence": 1,
      "memoLine1": "ab",
      "memoLine2": "ab",
      "memoLine3": "a",
      "memoLine4": "a",
      "memoLine5": "a",
      "purchaseOrderNumber": 2,
      "referenceNumber": 12,
      "referralReferenceNumber": 12,
      "salesClerk": 12,
      "skuNumber": 12,
      "storeNumber": 12,
      "ticketNumber": 12,
      "transactionDescription": "sender"
  },
  "to": {
      "accountNumber": "9706010000000000274",
      "accountOrganizationNumber": 970,
      "actionCode": "8002",
      "actionCodePriority": "1",
      "authorizationCode": "1222",
      "cardNumber": "",
      "cardSequence": 1,
      "currencyNumber": "",
      "departmentCode": "PPLD",
      "foreignUse": "0",
      "institutionNumber": 1,
      "insuranceCode": "2",
      "letterCode": "",
      "letterOrganizationNumber": 970,
      "planNumber": 60000,
      "planSequence": 1,
      "memoLine1": "1",
      "memoLine2": "1",
      "memoLine3": "1",
      "memoLine4": "1",
      "memoLine5": "1",
      "purchaseOrderNumber": 1,
      "referenceNumber": 1,
      "referralReferenceNumber": 1,
      "salesClerk": 1,
      "skuNumber": 1,
      "storeNumber": 1,
      "ticketNumber": 1,
      "transactionDescription": "Receiver"
  }
}
```

## Cash-in / Cash-out (account/balance)

Use this API ACCOUNT/BALANCE to apply a money amount from a Bank Branch, ATM, Web service etc, this money transfer does not make a debit from an existing account of credit, debit, or prepay, just this API post an specific money amount to a destination account.

Use API parameters to allow that money transfer can be ready to use after API was call or wait until next day.

The description of each API field can be found within the specifications defined in the portal.

/account/balance

Request body:

```json
{
"asmOrganizationNumber": 970,
  "accountNumber": "9704010000000001467",
  "representativeId": "A",
  "transactionData" : {
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

## Falcon Cash-in / Cash-out (account/FL-balance)

Use this API ACCOUNT/FL-BALANCE to money transfer amount from a Bank Branch, ATM, Web service etc, this money transfer does not make a debit from an existing account of credit, debit, or prepay, just this API post an specific money amount to a destination account. However, parameters previously defined, allow FALCON application (Card Fraud Control) audit this type of transactions.

Use API parameters to allow that money transfer can be ready to use after API was call or wait until next day.

The description of each API field can be found within the specifications defined in the portal.

/account/FL-balance

Request body:

```json
{
  "accountNumber": "9704010000000001467",
  "organizationNumber": 970,
  "representativeId": "A00",
  "transactionData": {
    "actionCode": 8000,
    "authorizationCode": "291012",
    "description": "Description",
    "effectiveDate": "2021-02-15",
    "transactionAmount": 1,
    "beneficiaryAccount": "9706010000000000274",
    "box": 1,
    "counterpartInstitution": 96545,
    "crPlaza": "10MON",
    "crStore": "50EDI",
    "device": "898ds-090ds-9d0s9-0ds9d0-0d9sd00",
    "frcUprkBeneficiary": "MACE881212TR3",
    "identifier": "OXXO",
    "ip": "999.999.200.200",
    "keyTracking": "OXXO202007158252885919",
    "latitude": "109.699.951",
    "longitude": "23.062.283",
    "operatingInstitution": 90646,
    "orderingFrcUprk": "MACE881212TR3",
    "orderingName": "Diego Martinez Cruz",
    "paidConcept": "Money for groseries",
    "paymentSourceId": "tok_test_visa_4242",
    "recipientName": "Eduardo Martinez Cruz",
    "storeNumber": 999999998,
    "senderAccount": "95005080626124382311"
  }
}
```

## Update Account user-defined fields (account/user)

Use this API ACCOUNT/USER to update the values of more than 50 user fields defined at account level information, this user fields are discretionary use fields that can be use by the user to add additional information at the account.

Values as dates, amounts, codes, etc. can be set up in the API before trigger it.

The description of each API field can be found within the specifications defined in the portal.

/account/user

Request body:

```json
{
  "accountNumber": "9704010000000001467",
  "cardholderAffinityGroup": 0,
  "foreignUse": 0,
  "miscellaneousUser1": "",
  "miscellaneousUser10": "",
  "miscellaneousUser11": "",
  "miscellaneousUser12": "",
  "miscellaneousUser2": "",
  "miscellaneousUser3": "",
  "miscellaneousUser4": "",
  "miscellaneousUser5": "",
  "miscellaneousUser6": "",
  "miscellaneousUser7": "",
  "miscellaneousUser8": "",
  "miscellaneousUser9": "",
  "organizationNumber": 970,
  "sourceCode": "",
  "userAmount1": 0,
  "userAmount10": 0,
  "userAmount11": 0,
  "userAmount12": 0,
  "userAmount13": 0,
  "userAmount14": 0,
  "userAmount2": 0,
  "userAmount3": 0,
  "userAmount4": 0,
  "userAmount5": 0,
  "userAmount6": 0,
  "userAmount7": 0,
  "userAmount8": 0,
  "userAmount9": 0,
  "userApplicationData1": "",
  "userApplicationData2": "",
  "userApplicationData3": "",
  "userCode1": "",
  "userCode10": "",
  "userCode11": "",
  "userCode12": "",
  "userCode13": "",
  "userCode14": "",
  "userCode2": "",
  "userCode3": "",
  "userCode4": "",
  "userCode5": "",
  "userCode6": "",
  "userCode7": "",
  "userCode8": "",
  "userCode9": "",
  "userDate1": "",
  "userDate10": "",
  "userDate11": "",
  "userDate12": "",
  "userDate13": "",
  "userDate14": "",
  "userDate2": "",
  "userDate3": "",
  "userDate4": "",
  "userDate5": "",
  "userDate6": "",
  "userDate7": "",
  "userDate8": "",
  "userDate9": ""
}
```

## Account Transfer Promotional Product Upgrade (account/transfer-promotional-product)

Use this API ACCOUNT/TRANSFER-PROMOTIONAL-PRODUCT to upgrade a current product type of card into another one, for example upgrade from Visa Classic to Visa Gold, or from MasterCard Classic to MasterCard Black.

When API is trigger, account information, card information and balances are transfer into new account and card. Customer information will be the same. Account Statements will be kipped on old account, but transactions cycle to date will be transfer into new account.

Same API can be used to make a product downgrade, it means transfer from Visa Gold to Visa Classic or from MasterCard Black to MasterCard Classic.

The description of each API field can be found within the specifications defined in the portal.

/account/transfer-promotional-product

Request body:

```json
{
  "accountNumber": "9704010000000001467",
  "cardholderAffinityGroup": 0,
  "foreignUse": 0,
  "miscellaneousUser1": "",
  "miscellaneousUser10": "",
  "miscellaneousUser11": "",
  "miscellaneousUser12": "",
  "miscellaneousUser2": "",
  "miscellaneousUser3": "",
  "miscellaneousUser4": "",
  "miscellaneousUser5": "",
  "miscellaneousUser6": "",
  "miscellaneousUser7": "",
  "miscellaneousUser8": "",
  "miscellaneousUser9": "",
  "organizationNumber": 970,
  "sourceCode": "",
  "userAmount1": 0,
  "userAmount10": 0,
  "userAmount11": 0,
  "userAmount12": 0,
  "userAmount13": 0,
  "userAmount14": 0,
  "userAmount2": 0,
  "userAmount3": 0,
  "userAmount4": 0,
  "userAmount5": 0,
  "userAmount6": 0,
  "userAmount7": 0,
  "userAmount8": 0,
  "userAmount9": 0,
  "userApplicationData1": "",
  "userApplicationData2": "",
  "userApplicationData3": "",
  "userCode1": "",
  "userCode10": "",
  "userCode11": "",
  "userCode12": "",
  "userCode13": "",
  "userCode14": "",
  "userCode2": "",
  "userCode3": "",
  "userCode4": "",
  "userCode5": "",
  "userCode6": "",
  "userCode7": "",
  "userCode8": "",
  "userCode9": "",
  "userDate1": "",
  "userDate10": "",
  "userDate11": "",
  "userDate12": "",
  "userDate13": "",
  "userDate14": "",
  "userDate2": "",
  "userDate3": "",
  "userDate4": "",
  "userDate5": "",
  "userDate6": "",
  "userDate7": "",
  "userDate8": "",
  "userDate9": ""
}
```

## Find Balance, Refinance and restructure information (account/{accountNumber}/balance)

This API ACCOUNT/{ACCOUNT}/BALANCE, allow a user select an specific balance amount from an account credit plan and refinance or restructure this balance into a new number of installment or fixed amount.

For example an account balance of $10,000 for credit plan 10002 at 5 installments has a fixed payment of $2,000 per month, using this API, to refinance or restructure this balance, the new number of installment can be 10 with a minimum payment of $1,000 per month.

This API request the account number, type of refinance, credit plan, new number of installment and new amount.

The description of each API field can be found within the specifications defined in the portal.

/account/{accountNumber}/balance

## Inquire Direct debit/credit (account/{accountNumber}/credit-debit)

The API ACCOUNT/{ACCOUNTNUMBER}/CREDIT-DEBIT allow the user the bring all the information about values previously set up at the account level o generate a Direct Debit o Direct Credit.

Direct Debit and Direct Credit is a functionality to allow internal process make a debit or credit of a Banking account (Current or saving) and this amount can be used to pay statement minimum or full balance.

The saving account, current account and Routing account are values previously set up at the account level so after call this API these information have to be set up as part of account information though API ACCOUNT/ADD.

The description of each API field can be found within the specifications defined in the portal.

/account/{accountNumber}/credit-debit

## Account Overview (account/{accountNumber}/overview)

Use this API ACCOUNT/{ACCOUNTNUMBER}/OVERVIEW, to get most important account information, as account number, name, address, phone, user fields, account financial information, delinquency, etc.This API use account number a search parameter.

The description of each API field can be found within the specifications defined in the portal.

/account/{accountNumber}/overview

## Find Relationship Details (account/{accountNumber}/relationship)

This API ACCOUNT/{ACCOUNTNUMBER}/RELATIONSHIP, allow the user to bring all account number already created under a relationship number.

A relationship number is defined as a Corporate Account, it means that all accounts and cards that are part of this corporate, should be created under this Corporate Account.

Use API ACCOUNT/ADD to created Corporated Accoount and sub-accounts that will be part of this account.

For additional information about Corporate Account please refer to CMS User Manual.

This API use Corporate Account Number as search parameter.

The description of each API field can be found within the specifications defined in the portal.

/account/{accountNumber}/relationship

## Update Installment Term (account/installment-term)

Use API ACCOUNT/INSTALLMENT-TERM, to allow user change or update the installment term of a transactions already posted into account.

In some Latam countries, when a purchase transaction is posted into the account, it can be financed in an specific number of installments, so a fixed payment amount should be calculated for this transactions.

This API allow the user the change the installments number already set up at the transactions level.

This API use the account number, transactions reference number, and new number of installment as part of search parameters.

The description of each API field can be found within the specifications defined in the portal.

/account/installment-term

Request body:

```json
{
  "accountNumber": "9704010000000001467",
  "installmentTermToBeUpdated": 1,
  "organizationNumber": 970,
  "recordNumber": 1,
  "recordType": 1,
  "transactionReferenceNumber": "123456"
}
```

## Associated Partied Update Service (account/associatedParties)

This API ACCOUNT/ASSOCIATEDPARTIES allow the user update selected parameters at account level information, related with Associated Parties fields.

The Associated parties fields located at account level are been used to identify if the account has any relation with a third party. A third party associated can be: guarantor, consigner, authorized signer, sales representative, etc.

The description of each API field can be found within the specifications defined in the portal.

/account/associatedParties

Request body:

```json
{
  "accountNumber": "string",
  "associationLetterFee1": 0,
  "associationLetterFee2": 0,
  "associationLetterFee3": 0,
  "associationLetterFlag1": 0,
  "associationLetterFlag2": 0,
  "associationLetterFlag3": 0,
  "associationNumberOccurrences": 1,
  "associationPartyData": [
    {
      "associationAccountNumber": "string",
      "associationAmount": 0,
      "associationDate": "2021-12-16",
      "associationRelationshipType": 0,
      "associationType": 0
    }
  ],
  "associationStatementFlag1": 0,
  "associationStatementFlag2": 0,
  "associationStatementFlag3": 0,
  "organizationNumber": 950
}
```

## Account-Embosser Authorization Criteria Update (account/auth-criteria)

This API ACCOUNT/AUTH-CRITERIA, allow the user create and update a relation between card authorization transactions and an authorization criteria table.

The Authorization Criteria table is a current functionality to define an authorization approval criteria table on base of merchant activity or MCC, hours, day of the week, country code, postal code, so the amount of the authorization is validated to approve or decline the authorization. This table information has to be added before use this API.

For additional information please refer CMS User Manual and CMS Screen Guide.

The description of each API field can be found within the specifications defined in the portal.

/account/auth-criteria

Request body:

```json
{
  "accountNumber": "4004894350058245552",
  "authorizationCriteria": 0,
  "cardSequence": 1,
  "foreignUse": 0,
  "functionCode": 1,
  "organizationNumber": 823
}
```

## Pending Bank, Branch and Store Update (account/bank-branch-store)

This API ACCOUNT/BANK-BRANCH-STORE, allow the user to update the Branch of store in where the credit was approved to create the account and card. This number is part of account information and is added for first time when account is created through API ACCOUNT/ADD.

The description of each API field can be found within the specifications defined in the portal.

/account/bank-branch-store

Request body:

```json
{
  "accountNumber": "4513074002573466583",
  "foreignUse": 0,
  "organizationNumber": 807,
  "pendingBankNumber": 12345,
  "pendingBranchNumber": 123456789,
  "pendingStoreNumber": 123456789
}
```

## Pricing Control Table Update (account/pctId)

Use this API ACCPUNT/PCT to assign a new Processing Control Table (PCT) to an existing account for a range of dates.

Currently when a new account is created using API ACCOUNT/ADD, the PCT number as to be added. This PCT table contains the processing parameter use by the account to process interests, fees, taxes, etc.

Using this API is possible me make an override of the current PCT by another PCT with different parameters.

For additional information please refer CMS User Manual and CMS Screen Guide.

The description of each API field can be found within the specifications defined in the portal.

/account/pctId

Request body:

```json
{
  "accountNumber": "4004894352313040331",
  "foreignUse": 0,
  "issuanceId": "string",
  "organizationNumber": 950,
  "pricingControlTable": {
    "pctExpirationDate": "2021-12-16",
    "pctId": "string",
    "pctLevel": "string",
    "pctLevelExpirationDate": "2021-12-16",
    "pctLevelStartDate": "2021-12-16",
    "pctStartDate": "2021-12-16"
  },
  "residenceId": "string"
}
```

## Prepaid load limits update (account/ppd-load-limits)

The API ACCOUNT/PPD-LOAD-LIMITS allow a user to update the current maximum and minimum limits of amount allow for prepay accounts.

When a prepay account is created using API ACCOUNT/ADD. The maximum and minimum amounts that a prepay card can has, are set up. However this limits can change with the time, so the API will help customer to set up the new parameters.

For additional information please refer CMS User Manual and CMS Screen Guide.

The description of each API field can be found within the specifications defined in the portal.

/account/ppd-load-limits

Request body:

```json
{
  "accountNumber": 4004894352313040400,
  "loadFrequency": 2,
  "loadNumber": 12,
  "logo": 400,
  "maximumSingleLoadAmount": 2,
  "minimumSingleLoadAmount": 2,
  "organizationNumber": 823,
  "prepaidLoadAmount": 2
}
```

## Prepaid Over Limits update (account/ppd-over-limit)

Use this API ACCOUNT/PPD-OVER-LIMIT to update the over limit amount allowed for a specific prepay account number. This over limit amount is a fixed amount used by authorization system to validated is the authorization amount if under this amount when the account does not have more available credit.

The description of each API field can be found within the specifications defined in the portal.

/account/ppd-over-limit

Request body:

```json
{
  "accountNumber": 4004894352313040400,
  "organizationNumber": 823,
  "prepaidOverlimitAmount": 2
}
```

## Account Wallet status Update (account/walletStatus)

The API ACCOUNT/WALLETSTATUS allow the user to change the current wallet status to active, inactive or suspend.

Wallet is a current functionality to allow a prepay account has more than one currency code bucket called wallet to upload money. A prepay account can has a wallet to upload $US Dollar, Local currency and other currency codes.

This API can be used to change the status of each of one wallets.

The description of each API field can be found within the specifications defined in the portal.

/account/walletStatus

Request body:

```json
{
  "accountNumber": 4513074002952959000,
  "organizationNumber": 807,
  "status": 2,
  "subsidyCode": "C",
  "wallet": 3
}
```

## Account Relationship Number Update (account/relationship/account)

Use this API ACCOUNT/RELATIONSHIP/ACCOUNT to link a new sub-account created through API ACCOUNT/ADD with a relationship account previously created.

Relationship number is a unique number assigned to a Corporate Card, for example Walmart with a customer number 123, is identify with a unique relationship number 567 and under this relationship number many accounts and cards are created for Walmart employs. So using the relationship number 567 is possible link additional new sub-account.

The description of each API field can be found within the specifications defined in the portal.

/account/relationship/account

Request body:

```json
{
  "accountNumber": "4004894352313040331",
  "foreignUse": "0",
  "organizationNumber": 823,
  "relationshipNumber": "4004894352313040331"
}
```

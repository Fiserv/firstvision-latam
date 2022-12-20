# Card Management

## Add Card Record (cards/embosser/)

Use the API CARDS/EMBOSSER create a card information used to emboss a new card or plastic. This card information must have relate that an account number created through API CCOUNT/ADD and this account number must be related a customer number created through API CUSTOMER/ADD.

This API allow add card information as card expiration date, service code, cardholder name, address to where the card will be deliver, spending limits, etc.

The card number is calculated on randomly way by the application, and this number will not generated again (duplicated).

/cards/embosser

Request body:  
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

The description of each API field can be found within the specifications defined in the SandBox portal.

Inquire Card or PAN token (cards/embosser/card-pan)
Use this API CARDS/EMBOSSER/CARD-PAN to get the pan-token calculated for a card number.

Pan token is a current functionality to tokenize the card number for all banks that are not a PCI certificate. When new card is created through API CARD/EMBOSSER, the pan token is calculated automatically on base a parameters previously defined.

This API use the PAN-TOKEN to bring the card number or card number can be used to being the PAN-TOKEN.

/cards/embosser/card-pan

Request body:  
{
    "cardSequence": 1,
    "functionType": "C",
    "organizationNumber": {{orgid}},
    "cardNumber": "{{cardNumber}}"
}

The description of each API field can be found within the specifications defined in the SandBox portal.

Add or Update Massive Cards (/cards/mass-card-issue)
This API CARDS/MASS-CARD-ISSUE, allow the user add or update a request to emboss new cards on massive way. These cards can be credit, debit or prepay card. Quantity of card to emboss is a parameter request by the API.

Cards embossed will not have an embosser name, but card number, expiration and card security values will be part of these.

/cards/mass-card-issue

Request body:  
{
    "logo": {{logo}},
    "organizationNumber": {{orgid}},
    "bankOrigin": 999999998,
    "blockCode1": " ",
    "blockCode2": " ",
    "branch": 999999998,
    "cardType": 1,
    "creditLimit": 0,
    "customerNumber": "{{customerNumber}}",
    "emblem": 1,
    "embossedName1": "TEST CD",
    "embossedName2": "TEST CD",
    "embosserCode": " ",
    "expiryDate": "2035-09-30",
    "functionType": "M",
    "globalQualification": "1",
    "inventoryControl": "NO",
    "inventoryQuantity": 0,
    "minimumQuantity": 5,
    "pctId": "050",
    "prepaidCardFlag": 1,
    "prepaidPlanNumber": 60000,
    "promoCode": " ",
    "quantityToCreate": 1,
    "relationAMBS": "N",
    "scheme": 3,
    "status": 1,
    "userCode1": 0,
    "userCode2": 0,
    "userCode3": 0
}

The description of each API field can be found within the specifications defined in the SandBox portal.

Card Action Update (cards/embosser/cardAction)
Use this API CARDS/EMBOSSER/CARDACTION to update the action flag used to re-emboss (re-issue) a specific card number.

This API allow to the user request a card reissue for some reason, lost/stolen, damage, card expiration, emergency replace, etc.

/cards/embosser/cardAction

Request body:  
{
    "accountNumberBase": 9704010000000001467,
}

The description of each API field can be found within the specifications defined in the SandBox portal.

Instant Card (cards/instant-card-L8V7)
This API CARDS/INSNTANT-CARD-L8V7 allow to the user request the creation of account and card on instantly way. Card information will be ready to be use for purchases.

Customer information have to be created through API CUSTOMER/ADD before call API instant card.

/cards/instant-card-L8V7

Request body:  
{
    "accountCreateFlag": "Y",
    "accountData": {
      "accountNumber": 840,
      "acquirerRetailPlan": 0,
      "alternateCustomerExpireDate": "2021-12-16",
      "alternateCustomerNumber": "string",
      "alternateCustomerNumberFlag": "C",
      "alternateCustomerStartDate": "2021-12-16",
      "authorizationControlTable": 0,
      "authorizationLimitOverrides": 0,
      "billingAccountIndicator": 1,
      "billingCurrency": 840,
      "billingCycle": 31,
      "blockCode1": "A",
      "blockCode2": "A",
      "cardTechnology": 0,
      "cardholderAffiliationGroup": 0,
      "cashPlanInstallmentBilling": 0,
      "cashPlanInstallmentPayment": 0,
      "cashPlanNumber": 12345,
      "creditLimit": 3000000,
      "customerSelectedDueDay": "string",
      "dateOpened": "2021-12-16",
      "dateTemporaryCreditLimit": "2021-03-20",
      "ddaAccountNumber": 121535325,
      "ddaRoutingNumber": 0,
      "dualBillingFlag": 1,
      "internationalCashPlan": 0,
      "internationalInstallmentPlan": 0,
      "internationalRetailPlan": 0,
      "maximumSingleLoadAmount": 0,
      "minimumSingleLoadAmount": 0,
      "miscellaneousUser1": "string",
      "miscellaneousUser10": "string",
      "miscellaneousUser11": "string",
      "miscellaneousUser12": "string",
      "miscellaneousUser2": "string",
      "miscellaneousUser3": "string",
      "miscellaneousUser4": "string",
      "miscellaneousUser5": "string",
      "miscellaneousUser6": "string",
      "miscellaneousUser7": "string",
      "miscellaneousUser8": "string",
      "miscellaneousUser9": "string",
      "owningBranchNumber": 1,
      "prepaidLoadAmount": 0,
      "prepaidLoadFrequency": 0,
      "prepaidLoadNumber": 0,
      "prepaidPlanNumber": 0,
      "processingControlTableControlId": 123,
      "processingControlTableExpireDate": "2021-03-20",
      "processingControlTableLevel": "O",
      "processingControlTableLevelExpireDate": "2021-03-20",
      "processingControlTableLevelStartDate": "2021-03-20",
      "processingControlTableStartDate": "2021-03-20",
      "promoPlanNumber": 12345,
      "qualification": "string",
      "relationshipBillingLevel": 1,
      "relationshipCardScheme": 3,
      "relationshipNumber": 124242,
      "relationshipPrimaryAccountFlag": 1,
      "retailPlanInstallmentBilling": 0,
      "retailPlanInstallmentPayments": 0,
      "retailPlanNumber": 12345,
      "savingsAccountNumber": "string",
      "savingsRoutingNumber": 0,
      "shortName": "Test account",
      "stateOfIssuanceId": "001",
      "stateOfResidenceId": "001",
      "statementFlag": "string",
      "statementFrequency": 1,
      "temporaryCreditLimit": 0,
      "userAccountNumber": "string",
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
      "userCode1": "string",
      "userCode10": "string",
      "userCode11": "string",
      "userCode12": "string",
      "userCode13": "string",
      "userCode14": "string",
      "userCode2": "string",
      "userCode3": "string",
      "userCode4": "string",
      "userCode5": "string",
      "userCode6": "string",
      "userCode7": "string",
      "userCode8": "string",
      "userCode9": "string",
      "userDate1": "2021-03-20",
      "userDate10": "2021-03-20",
      "userDate11": "2021-03-20",
      "userDate12": "2021-03-20",
      "userDate13": "2021-03-20",
      "userDate14": "2021-03-20",
      "userDate2": "2021-03-20",
      "userDate3": "2021-03-20",
      "userDate4": "2021-03-20",
      "userDate5": "2021-03-20",
      "userDate6": "2021-03-20",
      "userDate7": "2021-03-20",
      "userDate8": "2021-03-20",
      "userDate9": "2021-03-20"
    },
    "cardActionFlag": 1,
    "customerNumber": "4513074002573466583",
    "embosserData": {
      "addressLine1": "PORT OF MIAMI",
      "addressLine2": "117 E PARKWAY AVE",
      "atmCashAmount": 0,
      "atmCashNumber": 0,
      "atmCashSingleTransactionLimit": 0,
      "authorizationCriteriaTableNumber": "string",
      "branchNumber": 0,
      "cardActionReasonCode": "string",
      "cardholderAffiliationGroupId": 12348,
      "cardholderFlag": 0,
      "city": "MIAMI",
      "customerNumber": 4513074002573466600,
      "deliveryOption": 0,
      "digitalCardFlag": 1,
      "embossedName1": "HELLO",
      "embossedName2": "KIT-KAT WALLER",
      "expirationDate": "2020-03-03",
      "firstIssueBranch": 0,
      "icAmountLimitSingleTransaction": 0,
      "icTotalNumberTransactions": 0,
      "internetPurchaseAmount": 0,
      "internetPurchaseNumber": 0,
      "internetPurchaseSingleTransactionLimit": 0,
      "languageCode": "ENG",
      "name1": "RUN DMC",
      "name1TypeIndicator": 0,
      "name2": "RICK ROSS",
      "name2TypeIndicator": 0,
      "overTheCounterCashAmount": 0,
      "overTheCounterCashNumber": 0,
      "overTheCounterCashSingleTransactionLimit": 0,
      "plasticId": "string",
      "posServiceCode": 201,
      "postalCode": 38585,
      "programId": 0,
      "reissueDeliveryOption": 0,
      "retailPurchaseAmt": 0,
      "retailPurchaseNumber": 0,
      "retailPurchaseSingleTransactionLimit": 0,
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
    },
    "firstPurchaseFlag": "Y",
    "logo": 400,
    "organizationNumber": 807,
    "sameDayProcessingType": 1
}

The description of each API field can be found within the specifications defined in the SandBox portal.

Inquiry Security Values (cards/pin/security-codes)
This API CARDS/PIN/SECURITY-CODES, allow to the user get the card security values (CVV, CVV2,ICVV, PIN number) already emboss for an specific card number.

Security values provided by the API will be encrypted using a security key of 32 bytes, so user should use the same security key and 3Des algorithm to decrypt the security values.

/cards/pin/security-codes

Request body:  
{
    "cardNumber": "0004444440000000558",
    "channel": "W",
    "keyAssociation": "AV",
    "organizationNumber": 970
}

The description of each API field can be found within the specifications defined in the SandBox portal.

Inquire Dynamic CVV2/CVC2/4CSC (cards/pin/dynamic-value)
Use this API CARDS/PIN/DYNAMIC-VALUE to calculate and inquire a new CVV2 for not present card purchases.

Currently when card is emboss through the API CARD/EMBOSSER, the static CVV2 code is calculate and printed on sign panel on card back. The new functionality of Dynamic CVV2 allow to the cardholder call this API CARDS/PIN/DYNAMIC-VALUE to generate and calculate a new CVV2 before make a not present purchase. So when API is trigger the static CVV2 is inactivated and each time the cardholder wants to make a new not card present purchase the new CVV2 have to be calculated through this API.

/cards/pin/dynamic-values

Request body:  
{
    "cardNumber": "0004444440000000558",
    "channel": "I",
    "disableDCVV2": "N",
    "keyAssociation": "OV1",
    "organizationNumber": 970
}

The description of each API field can be found within the specifications defined in the SandBox portal.

Inquire Number of Invalid Pin Attempts (cards/pin/invalid-attempts)
This API CARDS/PIN/INVALID-ATTEMPTS allow to the cardholder get the number of invalid PIN attempts.

As part of security parameters, the number of invalid pin attempts are set up to avoid that pin number can be calculated for frauds proposals. When this parameter is reached the pin number is block and a new pin number have to be calculated.

Invalid Pin attempts can be reached by many reasons the most popular reason is when cardholder fails the pin number on ATM.

/cards/pin/invalid-attempts

Request body:  
{
    "cardNumber": "0004444440000000558",
    "cardSequenceNumber": 1,
    "organizationNumber": 970
} 

The description of each API field can be found within the specifications defined in the SandBox portal.

Pin Validation (cards/pin/validation)
Use this API CARDS/PIN/VALIDATION to confirm that current pin generated is correct.

This API require the pin block and the card number and not the clear pin number.

/cards/pin/validation

Request body:  
{
    "cardNumber": "0004444440000000558",
    "channel": "W",
    "currentPinBlock": "E06C64DAFB5CDDB2",
    "keyAssociation": "MOX",
    "organizationNumber": 970
}    

The description of each API field can be found within the specifications defined in the SandBox portal.

---
tags: [Release Notes, January, February]
---

# Release Notes

## February 2023

### What's New

Tokenization

- /vtis/v1/tokenRequestors/{tokenRequestorID}/tokens/{tokenReferenceID}/deviceBinding
- /vtis/v1/getAvailableCards
- /vtis/v1/getSelectedCards
- /vtis/v1/pan/lifecycle
- /vtis/v2/tokenRequestors/{tokenRequestorID}/tokens/{tokenReferenceID}/tokenChanged
- /vtis/v1/tokenRequestors/{tokenRequestorID}/tokens/{tokenReferenceID}/lifecycle
- /vtis/v1/checkEligibility

### Enhancements

- Improved APIs' description:
  - Account 
	  - /account/v2/instantCard
		- /account/v2/details
		- /account/v1/debitBalance
		- /account/QR-balance
		- /account/user
		- /account/customer
		- /account/block-code
		- /account/balance
	- Cards 
		- Embosser 
			- /cards/v2/embosser/details
		- Card 
			- /cards/mass-card-issue-L8V3
			- /cards/activation
			- /cards/credit-limit
			- /cards/spend-limits-L8V3
			- /cards/status-L8V1
			- /cards/temporary-credit-limit
			- /cards/transfer
			- /cards/travel
	- Loyalty 
		- /loyalty/demographic/{accountNumber}
		- /loyalty/statementSummary/{accountNumber}
		- /loyalty/
		- /loyalty/crossReference
		- /loyalty/points
		- /loyalty/pointsAccount
		- /loyalty/pointsExpireHistory
		- /loyalty/redemption
		- /loyalty/statementLists
		- /loyalty/pointsAdjust
		- /loyalty/pointsDisbursement
	- Transactions 
		- /transactions/plan-settlement-quote
		- /transactions/offer                                                           
		- /transactions/offer-list
		- /transactions/logo
		- /transactions/currency-rate
	- Customer 
		- /customer/
- Added description:
	- Account 
		- /account/enrollment
		- /account/v2/accountBoardingDriver
	- Transactions 
		- /transactions/br/v1/installmentTransactions/{installmentTransaction-Id}/terms
		- /transactions/v1/installmentTransactions/{installmentTransaction-Id}/anticipationAmount/simulation
		- /transactions/v1/installmentTransactions/{installmentTransaction-Id}/termsAnticipationNumber/simulation
		- /transactions/v1/installmentTransactions/{installmentTransaction-Id}/termsIdAnticipation/simulation
		- /transactions/v1/installmentTransactions/{installmentTransaction-Id}/simulation
		- /transactions/v1/installmentTransactions/{installmentTransaction-Id}/termsIdAnticipation/simulation
		- /transactions/v1/installmentTransactions/{installmentTransaction-Id}
		- /transactions/v1/installmentTransactions/terms
		- /transactions/v1/installmentTransactions/terms
		- /transactions/v1/installmentTransactions/{installmentTransaction-Id}/terms/termsIdAnticipation/simulation
		- /transactions/v2/installmentTransactions
		- /transactions/v2/installmentTransactions/{installmentTransaction-Id}/terms
	- Notification 
		- /v2/pushNotification
- Improved title name:
	- Cards 
		- Embosser 
			- /cards/embosser/card-details-L8V3
		- PIN:
			- /cards/pin/
			- /cards/pin/status
			- /cards/pin/validation
			- /cards/pin/invalid-attempts
			- /cards/pin/dynamic-values
	- Account 
		- /account/
		- /account/transfer
		- /account/ppd-load-limits
		- /account/ppd-over-limit
		- /account/v1/statementInstallments/{numberOfTerms}
		- /account/v1/statementInstallments
		- /account/vinculation-reversal
		- /account/organizationNumber/level-limits/validate-amount
	- Transactions 
		- /transactions/details
		- /transactions/installmentConversion
- Improved fields' description:
	- Cards 
		- Embosser 
			- /cards/embosser/card-pan-l8v2
		- PIN:
			- /cards/pin/security-codes 
				- Field keyAssociation in the Request
	- Account 
		- /account/organizationNumber/level-limits/validate-amount

### Fixed

- N/A

### Known Issues

- N/A

### Deprecated

- N/A

---

## January 2023

### What's New

- Migration to new portal

### Enhancements

- Error codes, error handling and notifications.

### Fixed

- N/A

### Known Issues

- N/A

### Deprecated

- Old portal.

---

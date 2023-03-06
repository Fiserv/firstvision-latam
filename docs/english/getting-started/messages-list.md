---
tags: [Getting Started, VMX, Message List]
---

# Messages List

| Service                        | Version | API endpoint                                                                                              | Method |
|--------------------------------|---------|-----------------------------------------------------------------------------------------------------------|--------|
| M.CMS.ACCOUNT.ADD              | R8V8    | /account/                                                                                                 | POST   |
| M.CMS.CUST.ACCT.CRD.DRV        | L8V1    | /account/account-boarding-driver                                                                          | POST   |
| M.CMS.ACCT.TO.CARD.INQ         | L8V2    | /account/card-L8V2                                                                                        | POST   |
| M.CMS.ACCTCUSTNBR.UPD          | L8V1    | /account/customer                                                                                         | PUT    |
| M.CMS.ACCOUNT.INQ              | L8V5    | /account/details                                                                                          | POST   |
| M.CMS.ACCTMNT.UPD              | L8V1    | /account/details                                                                                          | PUT    |
| M.CMS.EMBOSSER.ADD             | L8V8    | /cards/embosser/                                                                                          | POST   |
| M.CMS.EMBOSSER.INQ             | L8V6    | /cards/embosser/details                                                                                   | POST   |
| M.CMS.INSTANT.CARD.ADD         | L8V7    | /cards/instant-card-L8V7                                                                                  | POST   |
| M.CMS.EMBOSSER.INQ             | L8VE    | /cards/v2/embosser/details                                                                                | POST   |
| M.CMS.CUSTOMER.ADD             | R8V4    | /customer/                                                                                                | POST   |
| M.CMS.DEMOGRAPHIC.INQ          | R8V4    | /customer/demographicData                                                                                 | POST   |
| M.CMS.CUSTCHANNEL.INQ          | L8V4    | /customer/details-l8v4                                                                                    | POST   |
| M.FAS.OUTSTANDING.AUTH.INQ     | L8V2    | /transactions/outstanding-authorizations/details                                                          | POST   |
| M.CMS.REFINANCERESTRUCTURE.INQ | R8V1    | /account/{accountNumber}/balance                                                                          | GET    |
| M.CMS.DIRECTDBCR.INQ           | R8V4    | /account/{accountNumber}/credit-debit                                                                     | GET    |
| M.CMS.IBS.DEBIT.INQ            | R8V1    | /account/{accountNumber}/ibs-debit                                                                        | GET    |
| M.CMS.ACCOUNT.OVERVIEW.INQ     | L8V1    | /account/{accountNumber}/overview                                                                         | GET    |
| M.CMS.INSURANCE.INQ            | R8V3    | /account/{accountNumber}/product                                                                          | GET    |
| M.CMS.REL.ACCTREC.INQ          | R8V4    | /account/{accountNumber}/relationship                                                                     | GET    |
| M.CMS.RULE.LIMIT.INQ           | L8V1    | /account/{organizationNumber}/level-limits                                                                | GET    |
| M.CMS.ACCT.CNTL.TBL.INQ        | R8V1    | /account/{tableInquiry}/account-control-table-inquiry                                                     | GET    |
| M.CMS.ACCT.DEMOGRAPHICS.INQ    | R8V2    | /account/account-demographic                                                                              | POST   |
| M.CMS.ACCOUNT.ADD              | L8V3    | /account/add-L8V3                                                                                         | POST   |
| M.CMS.ASSOC.PARTIES.UPD        | R8V1    | /account/associatedParties                                                                                | PUT    |
| M.CMS.ACCTEMB.AUTHCRIT.UPD     | R8V1    | /account/auth-criteria                                                                                    | PUT    |
| M.ASM.MONETARY.ACT             | L8V2    | /account/balance                                                                                          | PUT    |
| M.CMS.BALANCE.INQ              | R8V1    | /account/balance/details                                                                                  | POST   |
| M.CMS.BANK.ACCOUNT.UPD         | L8V2    | /account/bankAccount                                                                                      | PUT    |
| M.CMS.PEND.BANK.UPD            | R8V1    | /account/bank-branch-store                                                                                | PUT    |
| M.CMS.ACCT.BLKCD.UPD           | R8V1    | /account/block-code                                                                                       | PUT    |
| M.CMS.ACCT.BLKCD.WARNCD.UPD    | L8V1    | /account/blockCodesWarning                                                                                | PUT    |
| M.CMS.CRBUREAU.UPD             | L8V1    | /account/creditBureau                                                                                     | PUT    |
| M.CMS.ACCOUNT.INQ              | L8VG    | /account/details-L8VG                                                                                     | POST   |
| M.CMS.DIRECTDB.UPD             | R8V4    | /account/directDebit                                                                                      | PUT    |
| M.OMS.ACCTENROLL.INQ           | R8V1    | /account/enroll/{accountNumber}                                                                           | GET    |
| M.OMS.ENROLL.ACTION.UPD        | R8V1    | /account/enrollment                                                                                       | PUT    |
| M.OMS.ENROLL.ADD               | R8V1    | /account/enrollment                                                                                       | POST   |
| M.CMS.WAIVEFLAG.UPD            | R8V5    | /account/feeWaiver                                                                                        | PUT    |
| M.ASM.MONETARY.ACT             | L8V4    | /account/FL-balance                                                                                       | PUT    |
| M.ASM.MONETARYPTP.ACT          | L8V2    | /account/FL-transferP2P                                                                                   | PUT    |
| M.CMS.INST.TERM.UPD"           | R8V2    | /account/installment-term                                                                                 | PUT    |
| M.CMS.RULE.LIMIT.ADD           | L8V1    | /account/organizationNumber/level-limits                                                                  | POST   |
| M.CMS.RULE.LIMIT.UPD           | L8V1    | /account/organizationNumber/level-limits                                                                  | PUT    |
| M.CMS.RULE.LIMIT.PREVALIDATE   | L8V1    | /account/organizationNumber/level-limits/validate-amount                                                  | POST   |
| M.CMS.PRICING.CTRL.UPD         | R8V1    | /account/pctId                                                                                            | PUT    |
| M.CMS.PPD.LOAD.LMTS.UPD        | L8V1    | /account/ppd-load-limits                                                                                  | PUT    |
| M.CMS.PPD.OVERLIMIT.UPD        | L8V1    | /account/ppd-over-limit                                                                                   | PUT    |
| M.CMS.PREPAIDACCT.ASSIGN.UPD   | L8V1    | /account/prepaid                                                                                          | PUT    |
| M.CMS.ACCT.INSURANCE.ADD       | R8V2    | /account/product                                                                                          | POST   |
| M.CMS.ACCT.PRODTRANSFER.UPD    | L8V3    | /account/productTransfer                                                                                  | PUT    |
| M.ASM.MONETARY.ACT             | L8V3    | /account/QR-balance                                                                                       | PUT    |
| M.ASM.MONETARY.ACT             | L8V4    | /account/QRFL-balance                                                                                     | PUT    |
| M.ASM.MONETARY.ACT             | L8V3    | /account/QR-transfer                                                                                      | PUT    |
| M.CMS.ACCT.CLOSE.CHGOFF        | R8V2    | /account/qualification                                                                                    | PUT    |
| M.CMS.REL.TO.ACCT              | R8V1    | /account/relationship/{relationshipNumber}/account                                                        | GET    |
| M.CMS.ACCOUNT.RELATIONSHIP.UPD | L8V1    | /account/relationship/account                                                                             | PUT    |
| M.CMS.BILLING.CYCLE.UPD        | R8V1    | /account/relationship/billing-cycle                                                                       | PUT    |
| M.CMS.SVCFEE.TBL.OVRD.UPD      | R8V1    | /account/service-charge-table                                                                             | PUT    |
| M.CMS.ACCT.STTLMNT.QUOTE.UPD   | R8V1    | /account/settlement-quote                                                                                 | PUT    |
| M.CMS.SKIPPMT.UPD              | R8V1    | /account/skip-payment                                                                                     | PUT    |
| M.CMS.ACCOUNT.STATUS.UPD       | L8V1    | /account/status-update-L8V1                                                                               | POST   |
| M.ASM.MONETARY.ACT             | L8V2    | /account/transfer                                                                                         | PUT    |
| M.ASM.MONETARYPTP.ACT          | L8V2    | /account/transferP2P                                                                                      | PUT    |
| M.CMS.PROM.PROD.UPG.UPD        | L8V1    | /account/transfer-promotional-product                                                                     | PUT    |
| M.CMS.ACCT.USER.UPD            | R8V3    | /account/user                                                                                             | PUT    |
| M.CMS.ACCT.USER.DATA.UPD       | R8V1    | /account/userData                                                                                         | PUT    |
| M.CMS.ACCT.INST.BAL.INQ        | L8V1    | /account/v1/debitBalance                                                                                  | GET    |
| M.CMS.FLCN.MON.TRANSFER.INQ    | L8V1    | /account/v1/falconMonetaryInquiry                                                                         | POST   |
| M.CMS.ACCOUNT.STMT.FLAG.UPD    | R8V1    | /account/v1/statementFlag                                                                                 | PATCH  |
| M.CMS.INSTSTMTSIM.ACT          | L8V1    | /account/v1/statementInstallments                                                                         | GET    |
| M.CMS.INSTSTMTSIM.ACT          | L8V1    | /account/v1/statementInstallments/{numberOfTerms}                                                         | PUT    |
| M.CMS.CUST.ACCT.CRD.DRV        | L8V2    | /account/v2/accountBoardingDriver                                                                         | POST   |
| M.CMS.ACCTCUSTNBR.UPD          | L8V2    | /account/v2/customer                                                                                      | PUT    |
| M.CMS.ACCTMNT.UPD              | L8V2    | /account/v2/details                                                                                       | PUT    |
| M.CMS.INSTANT.CARD.ADD         | L8V7    | /account/v2/instantCard                                                                                   | POST   |
| M.CMS.VINCULATION.REV.UPD      | L8V1    | /account/vinculation-reversal                                                                             | PUT    |
| M.CMS.WALLET.PRTYORDER.UPD     | R8V1    | /account/wallet-priority-order                                                                            | PUT    |
| M.CMS.WALLET.STATUS.UPD        | L8V1    | /account/walletStatus                                                                                     | PUT    |
| M.CMS.CARDACTIVATION.UPD       | R8V3    | /cards/activation                                                                                         | PUT    |
| M.CMS.CREDITLIMIT.UPD          | R8V1    | /cards/credit-limit                                                                                       | PUT    |
| M.CMS.CHANNEL.INQ              | L8V1    | /cards/details                                                                                            | POST   |
| M.CMS.EMB.NAV.SVC              | R8V1    | /cards/embosser/{cardNumber}/navigational                                                                 | GET    |
| M.CMS.EMB.BLKCD.UPD            | R8V1    | /cards/embosser/block                                                                                     | PUT    |
| M.CMS.EMB.CARDACTION.UPD       | L8V2    | /cards/embosser/cardAction-L8V2                                                                           | PUT    |
| M.CMS.ACCT.TO.CARD.INQ         | L8V3    | /cards/embosser/card-details-L8V3                                                                         | POST   |
| M.CMS.CARD.PAN.INQ             | L8V2    | /cards/embosser/card-pan-l8v2                                                                             | POST   |
| M.CMS.EMBOSSER.ADD             | L8VF    | /cards/embosser/l8vf                                                                                      | POST   |
| M.CMS.SAMEDAYPLASTIC.UPD       | R8V1    | /cards/embosser/sameDay                                                                                   | POST   |
| M.CMS.EMBOSSER.UPD             | L8V6    | /cards/embosser/v3/embosserUpdate                                                                         | PUT    |
| M.CMS.INSTANT.CARD.ADD         | L8V7    | /cards/global-card-activation                                                                             | PUT    |
| M.CMS.MASS.CARD.ISSUE.INQ      | L8V3    | /cards/mass-card-issue-L8V3                                                                               | GET    |
| M.CMS.MASS.CARD.ISSUE.UPD      | L8V3    | /cards/mass-card-issue-L8V3                                                                               | POST   |
| M.CMS.PIN.REASSIGNMENT         | R8V1    | /cards/pin/                                                                                               | PUT    |
| M.CMS.GENERATE.DCVV2           | R8V1    | /cards/pin/dynamic-values                                                                                 | POST   |
| M.CMS.INV.PINTRIES.CTR.INQ     | L8V1    | /cards/pin/invalid-attempts                                                                               | POST   |
| M.CMS.PIN.CHANGE               | R8V2    | /cards/pin/pin-change                                                                                     | PUT    |
| M.CMS.SEC.VALUES.INQ           | R8V1    | /cards/pin/security-codes                                                                                 | POST   |
| M.CMS.PIN.BLOCK.UPD            | R8V1    | /cards/pin/status                                                                                         | PUT    |
| M.CMS.PIN.VALIDATE             | R8V1    | /cards/pin/validation                                                                                     | POST   |
| M.CMS.CARDSPENDLIMITS.UPD      | L8V3    | /cards/spend-limits-L8V3                                                                                  | PUT    |
| M.CMS.STATEMENT.INQ            | L8V3    | /cards/statement-detail                                                                                   | POST   |
| M.CMS.STATEMENTDATE.INQ        | L8V1    | /cards/statement-detail/date                                                                              | POST   |
| M.CMS.CARD.STATUS.UPD          | L8V1    | /cards/status-L8V1                                                                                        | PUT    |
| M.CMS.TEMP.CREDITLIMIT.UPD     | R8V2    | /cards/temporary-credit-limit                                                                             | PUT    |
| M.CMS.CARDTRANSFER.UPD         | L8V5    | /cards/transfer                                                                                           | PUT    |
| M.CMS.TRAVELIND.UPD            | L8V1    | /cards/travel                                                                                             | PUT    |
| M.CMS.CUSTOMER.UPD             | R8V5    | /customer/                                                                                                | PUT    |
| M.CMS.ADDRESS.INQ              | R8V2    | /customer/{accountNumber}/current-prior-address                                                           | GET    |
| M.CMS.REL.CUST.INQ             | L8V1    | /customer/{customerNumber}/relationship                                                                   | GET    |
| M.CMS.CUST.TO.ACCT.INQ         | R8V3    | /customer/accountNumber                                                                                   | POST   |
| M.CMS.CUST.ACTIVATE.ADD        | L8V1    | /customer/activation                                                                                      | POST   |
| M.CMS.DEMOGRAPHIC.INQ          | L8V2    | /customer/demographicData-l8v2                                                                            | POST   |
| M.CMS.NBRGENERATION.ACT        | L8V1    | /customer/generation                                                                                      | POST   |
| M.CMS.CUSTOMER.ADD             | L8V2    | /customer/l8v2                                                                                            | POST   |
| M.CMS.RELATIONSHIP.ADD         | R8V2    | /customer/relationship                                                                                    | POST   |
| M.CMS.CUST.REVERSAL.UPD        | L8V1    | /customer/reversal                                                                                        | PUT    |
| M.CMS.CUST.NBR.INQ             | L8V1    | /customer/v4/cards/details                                                                                | POST   |
| M.LMS.TRANSACTION.INQ          | R8V1    | /loyalty/                                                                                                 | POST   |
| M.LMS.ACCOUNT.XREF.INQ         | R8V1    | /loyalty/crossReference                                                                                   | POST   |
| M.LMS.DEMOGRAPHIC.INQ          | R8V2    | /loyalty/demographic/{accountNumber}                                                                      | GET    |
| M.LMS.POINTS.ACCT.INQ          | R8V2    | /loyalty/points                                                                                           | POST   |
| M.LMS.POINTS.ACCT.ADD          | R8V1    | /loyalty/pointsAccount                                                                                    | POST   |
| M.LMS.POINTS.ADJ.ADD           | R8V1    | /loyalty/pointsAdjust                                                                                     | PUT    |
| M.LMS.POINTS.ACCT.DISB.DATA.UP | R8V2    | /loyalty/pointsDisbursement                                                                               | PUT    |
| M.LMS.POINTS.EXPIRY.HIST.INQ   | R8V1    | /loyalty/pointsExpireHistory                                                                              | POST   |
| M.LMS.REDEMPTION.ADD           | R8V1    | /loyalty/redemption                                                                                       | POST   |
| M.LMS.STMT.LIST.INQ            | R8V1    | /loyalty/statementLists                                                                                   | POST   |
| M.LMS.STMT.SUMMARY.INQ         | R8V1    | /loyalty/statementSummary/{accountNumber}                                                                 | GET    |
| M.CMS.SERV.FEE.TBL.INQ         | R8V1    | /transactions/{feeTableNumber}/fee-table-information                                                      | GET    |
| M.CMS.INS.TBL.INQ              | R8V1    | /transactions/{tableInsurance}/insurance-table                                                            | GET    |
| M.CMS.INSTAL.TERMS.INQ         | L8V1    | /transactions/br/v1/installmentTransactions/{installmentTransaction-Id}/terms                             | GET    |
| M.SSC.EXCH.RATE.ADD            | L8V1    | /transactions/currency-rate                                                                               | POST   |
| M.SSC.EXCH.RATE.INQ            | L8V1    | /transactions/currency-rate                                                                               | GET    |
| M.SSC.EXCH.RATE.UPD            | L8V1    | /transactions/currency-rate                                                                               | PUT    |
| M.CMS.CURR.RATE.MWP.UPD        | R8V1    | /transactions/currency-rate-table                                                                         | PUT    |
| M.OMS.ENRHISTORY.INQ           | R8V1    | /transactions/enroll-history/{accountNumber}                                                              | GET    |
| M.SSC.EXCHANGE.RATE.UPD        | L8V1    | /transactions/exchange-rate                                                                               | PUT    |
| M.CMS.INST.TRAN.CONV           | R8V1    | /transactions/installmentConversion                                                                       | PUT    |
| M.CMS.LOGO.INQ                 | R8V1    | /transactions/logo                                                                                        | GET    |
| M.CMS.LOGO.BLKCD.INQ           | R8V1    | /transactions/logo-block-codes                                                                            | GET    |
| M.CMS.MCCT.TBL.INQ             | R8V1    | /transactions/mcct-table                                                                                  | GET    |
| M.ASM.NONMON.ACT               | R8V5    | /transactions/non-monetary-action-code                                                                    | POST   |
| M.ASM.NOTES.HISTORY.INQ        | R8V3    | /transactions/notes-R8V3                                                                                  | POST   |
| M.OMS.OFFER.INQ                | R8V1    | /transactions/offer                                                                                       | GET    |
| M.OMS.OFFERDEFLIST.INQ         | R8V1    | /transactions/offer-list                                                                                  | GET    |
| M.CMS.ORG.INQ                  | R8V1    | /transactions/organization                                                                                | GET    |
| M.CMS.ORG.UPD                  | R8V1    | /transactions/organization-update                                                                         | PUT    |
| M.CMS.OUTSTANDING.AUTH.INQ     | R8V2    | /transactions/outstanding-authorizations/{accountNumber}                                                  | GET    |
| M.FAS.OUTSTANDING.AUTH.INQ     | L8V3    | /transactions/outstanding-authorizations-L8V3/details                                                     | POST   |
| M.CMS.PCT.TBL.INQ              | R8V1    | /transactions/pct-table                                                                                   | GET    |
| M.CMS.PLAN.STTLMNT.QUOTE.UPD   | R8V1    | /transactions/plan-settlement-quote                                                                       | POST   |
| M.CMS.LOGO.PREPD.INQ           | R8V1    | /transactions/prepaid-logo                                                                                | GET    |
| M.CMS.PROMORATE.UPD            | R8V1    | /transactions/promo-rate                                                                                  | PUT    |
| M.CMS.QUOTE.PROJ.UPD           | L8V1    | /transactions/quote-projections                                                                           | PUT    |
| M.CMS.TRANSACTIONDETAIL.INQ    | L8V7    | /transactions/summary-details                                                                             | POST   |
| M.CMS.INSTAL.TRXN.DETAIL.UPD   | L8V1    | /transactions/v1/installmentTransactions/{installmentTransaction-Id}                                      | GET    |
| M.CMS.INSTAL.TRXN.DETAIL.UPD   | L8V1    | /transactions/v1/installmentTransactions/{installmentTransaction-Id}/anticipationAmount/simulation        | PUT    |
| M.CMS.INSTAL.TRXN.DETAIL.UPD   | L8V1    | /transactions/v1/installmentTransactions/{installmentTransaction-Id}/simulation                           | PATCH  |
| M.CMS.INSTAL.TERMS.UPD         | L8V1    | /transactions/v1/installmentTransactions/{installmentTransaction-Id}/terms/termsIdAnticipation/simulation | PUT    |
| M.CMS.INSTAL.TRXN.DETAIL.UPD   | L8V1    | /transactions/v1/installmentTransactions/{installmentTransaction-Id}/termsAnticipationNumber/simulation   | PUT    |
| M.CMS.INSTAL.TRXN.DETAIL.UPD   | L8V1    | /transactions/v1/installmentTransactions/{installmentTransaction-Id}/termsIdAnticipation/simulation       | PATCH  |
| M.CMS.INSTAL.TRXN.DETAIL.UPD   | L8V1    | /transactions/v1/installmentTransactions/{installmentTransaction-Id}/termsIdAnticipation/simulation       | PUT    |
| M.CMS.INSTAL.SUMMARY.INQ       | L8V1    | /transactions/v1/installmentTransactions/terms                                                            | GET    |
| M.CMS.INSTAL.TRXN.DATA.INQ     | L8V2    | /transactions/v2/installmentTransactions                                                                  | GET    |
| M.CMS.INSTAL.TERMS.INQ         | L8V2    | /transactions/v2/installmentTransactions/{installmentTransaction-Id}/terms                                | GET    |
| M.FAS.CHECK.ELIGIBILITY.INQ    | L8V1    | /vtis/v1/checkEligibility                                                                                 | POST   |
| M.CMS.AVAIL.SELECT.CARD.INQ    | L8V1    | /vtis/v1/getAvailableCards                                                                                | POST   |
| M.CMS.AVAIL.SELECT.CARD.INQ    | L8V1    | /vtis/v1/getSelectedCards                                                                                 | POST   |
|                                |         | /vtis/v1/pan/lifecycle                                                                                    | POST   |
| M.FAS.DEVICE.TOKEN.BINDING     | L8V1    | /vtis/v1/tokenRequestors/{tokenRequestorID}/tokens/{tokenReferenceID}/deviceBinding                       | POST   |
|                                |         | /vtis/v1/tokenRequestors/{tokenRequestorID}/tokens/{tokenReferenceID}/lifecycle                           | POST   |
| M.FAS.TOKEN.NOTIFICATION.UPD   | L8V1    | /vtis/v2/tokenRequestors/{tokenRequestorID}/tokens/{tokenReferenceID}/tokenChanged                        | POST   |

---

## See Also

- [Getting Started](?path=docs/english/getting-started.md)
- [Postman Tutorial](?path=docs/english/getting-started/postman.md)
- [Structure](?path=docs/english/getting-started/structure.md)
- [Terminology](?path=docs/english/getting-started/terminology.md)

---

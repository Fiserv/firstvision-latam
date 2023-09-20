# Service List

## Vesion 1.2.0

<table>
    <tr>
        <th>Link</th>
        <th>Service</th>
        <th>Version</th>
        <th>API endpoint</th>
        <th>Method</th>
    </tr>
    <tr>
        <td colspan="5" align="center"><b>Accounts</td>
    </tr>
    <tr>
        <td>Account Add</td>
        <td>M.CMS.ACCOUNT.ADD</td>
        <td>L8V3</td>
        <td>/account/add-L8V3</td>
        <td>POST</td>
    </tr>
    <tr>
        <td>Account Authorization Criteria Update</td>
        <td>M.CMS.ACCTEMB.AUTHCRIT.UPD</td>
        <td>R8V1</td>
        <td>/account/auth-criteria</td>
        <td>PUT</td>
    </tr>
    <tr>
        <td>Account Balance Inquiry</td>
        <td>M.CMS.BALANCE.INQ</td>
        <td>R8V1</td>
        <td>/account/balance/details</td>
        <td>POST</td>
    </tr>
    <tr>
        <td>Account Block Code Update</td>
        <td>M.CMS.ACCT.BLKCD.UPD</td>
        <td>R8V1</td>
        <td>/account/block-code</td>
        <td>PUT</td>
    </tr>
    <tr>
        <td>Account Boarding Driver Request</td>
        <td>M.CMS.CUST.ACCT.CRD.DRV</td>
        <td>L8V3</td>
        <td>/account/v2/accountBoardingDriver</td>
        <td>POST</td>
    </tr>
    <tr>
        <td>Account Control Table Inquiry</td>
        <td>M.CMS.ACCT.CNTL.TBL.INQ</td>
        <td>R8V1</td>
        <td>/account/{tableInquiry}/account-control-table-inquiry</td>
        <td>GET</td>
    </tr>
    <tr>
        <td>Account Demographic Inquiry</td>
        <td>M.CMS.ACCT.DEMOGRAPHICS.INQ</td>
        <td>R8V2</td>
        <td>/account/account-demographic</td>
        <td>POST</td>
    </tr>
    <tr>
        <td>Account Enrollment Inquiry</td>
        <td>M.OMS.ACCTENROLL.INQ</td>
        <td>R8V1</td>
        <td>/account/enroll/{accountNumber}</td>
        <td>GET</td>
    </tr>
    <tr>
        <td>Account Fee Waiver Update</td>
        <td>M.CMS.WAIVEFLAG.UPD</td>
        <td>R8V5</td>
        <td>/account/feeWaiver</td>
        <td>PUT</td>
    </tr>
    <tr>
        <td>Account Information Inquiry</td>
        <td>M.CMS.ACCOUNT.INQ</td>
        <td>L8VI</td>
        <td>/account/v2/accounts</td>
        <td>GET</td>
    </tr>
    <tr>
        <td>Account Insurance Product Update</td>
        <td>M.CMS.INSURANCE.UPD</td>
        <td>R8V3</td>
        <td>/account/v1/insuranceProducts/{insuranceProduct-id}</td>
        <td>PATCH</td>
    </tr>
    <tr>
        <td>Account Level Settlement Quote Request</td>
        <td>M.CMS.ACCT.STTLMNT.QUOTE.UPD</td>
        <td>R8V1</td>
        <td>/account/settlement-quote</td>
        <td>PUT</td>
    </tr>
    <tr>
        <td>Account Numbers by Relationship Inquiry</td>
        <td>M.CMS.REL.TO.ACCT</td>
        <td>R8V1</td>
        <td>/account/relationship/{relationshipNumber}/account</td>
        <td>GET</td>
    </tr>
    <tr>
        <td>Account Overview Inquiry</td>
        <td>M.CMS.ACCOUNT.OVERVIEW.INQ</td>
        <td>L8V1</td>
        <td>/account/{accountNumber}/overview</td>
        <td>GET</td>
    </tr>
    <tr>
        <td>Account Qualification Update</td>
        <td>M.CMS.ACCT.CLOSE.CHGOFF</td>
        <td>R8V2</td>
        <td>/account/qualification</td>
        <td>PUT</td>
    </tr>
    <tr>
        <td>Account Relationship Inquiry</td>
        <td>M.CMS.REL.ACCTREC.INQ</td>
        <td>R8V4</td>
        <td>/account/{accountNumber}/relationship</td>
        <td>GET</td>
    </tr>
    <tr>
        <td>Account Relationship Number Update</td>
        <td>M.CMS.ACCOUNT.RELATIONSHIP.UPD</td>
        <td>L8V1</td>
        <td>/account/relationship/account</td>
        <td>PUT</td>
    </tr>
    <tr>
        <td>Account Statement Flag Update</td>
        <td>M.CMS.ACCOUNT.STMT.FLAG.UPD</td>
        <td>R8V1</td>
        <td>/account/v1/statementFlag</td>
        <td>PATCH</td>
    </tr>
    <tr>
        <td>Account to Account Funds Transfer</td>
        <td>M.ASM.MONETARYPTP.ACT</td>
        <td>L8V2</td>
        <td>/account/transferP2P</td>
        <td>PUT</td>
    </tr>
    <tr>
        <td>Account Update</td>
        <td>M.CMS.ACCTMNT.UPD</td>
        <td>L8V2</td>
        <td>/account/v2/accounts</td>
        <td>PUT</td>
    </tr>
    <tr>
        <td>Account User Update</td>
        <td>M.CMS.ACCT.USER.UPD</td>
        <td>R8V3</td>
        <td>/account/user</td>
        <td>PUT</td>
    </tr>
    <tr>
        <td>Account Wallet Status Update</td>
        <td>M.CMS.WALLET.STATUS.UPD</td>
        <td>L8V1</td>
        <td>/account/walletStatus</td>
        <td>PUT</td>
    </tr>
    <tr>
        <td>Amount Against Rule Levels Validate</td>
        <td>M.CMS.RULE.LIMIT.PREVALIDATE</td>
        <td>L8V1</td>
        <td>/account/organizationNumber/level-limits/validate-amount</td>
        <td>POST</td>
    </tr>
    <tr>
        <td>Associated Parties Update</td>
        <td>M.CMS.ASSOC.PARTIES.UPD</td>
        <td>R8V1</td>
        <td>/account/associatedParties</td>
        <td>PUT</td>
    </tr>
    <tr>
        <td>Balance Update (Cash-in &amp; Cash-out)</td>
        <td>M.ASM.MONETARY.ACT</td>
        <td>L8V5</td>
        <td>/account/v2/balance</td>
        <td>PUT</td>
    </tr>
    <tr>
        <td>Bank Account Update</td>
        <td>M.CMS.BANK.ACCOUNT.UPD</td>
        <td>L8V2</td>
        <td>/account/bankAccount</td>
        <td>PUT</td>
    </tr>
    <tr>
        <td>Billing Cycle Update</td>
        <td>M.CMS.BILLING.CYCLE.UPD</td>
        <td>R8V1</td>
        <td>/account/relationship/billing-cycle</td>
        <td>PUT</td>
    </tr>
    <tr>
        <td>Block Codes Warning Update</td>
        <td>M.CMS.ACCT.BLKCD.WARNCD.UPD</td>
        <td>L8V1</td>
        <td>/account/blockCodesWarning</td>
        <td>PUT</td>
    </tr>
    <tr>
        <td>Credit Bureau Update</td>
        <td>M.CMS.CRBUREAU.UPD</td>
        <td>L8V1</td>
        <td>/account/creditBureau</td>
        <td>tran</td>
    </tr>
    <tr>
        <td>Customer Number Update</td>
        <td>M.CMS.ACCTCUSTNBR.UPD</td>
        <td>L8V2</td>
        <td>/account/v2/customer</td>
        <td>PUT</td>
    </tr>
    <tr>
        <td>Direct Debit Update</td>
        <td>M.CMS.DIRECTDB.UPD</td>
        <td>R8V4</td>
        <td>/account/directDebit</td>
        <td>PUT</td>
    </tr>
    <tr>
        <td>Direct Debit-Credit Inquiry</td>
        <td>M.CMS.DIRECTDBCR.INQ</td>
        <td>R8V4</td>
        <td>/account/{accountNumber}/credit-debit</td>
        <td>GET</td>
    </tr>
    <tr>
        <td>IBS Debit File Inquiry</td>
        <td>M.CMS.IBS.DEBIT.INQ</td>
        <td>R8V1</td>
        <td>/account/{accountNumber}/ibs-debit</td>
        <td>GET</td>
    </tr>
    <tr>
        <td>Installment Terms Update</td>
        <td>M.CMS.INST.TERM.UPD</td>
        <td>R8V2</td>
        <td>/account/installment-term</td>
        <td>PUT</td>
    </tr>
    <tr>
        <td>Instant Card Add</td>
        <td>M.CMS.INSTANT.CARD.ADD</td>
        <td>L8V7</td>
        <td>/account/v2/instantCard</td>
        <td>POST</td>
    </tr>
    <tr>
        <td>Insurance Product Add</td>
        <td>M.CMS.ACCT.INSURANCE.ADD</td>
        <td>R8V2</td>
        <td>/account/product</td>
        <td>POST</td>
    </tr>
    <tr>
        <td>Insurance Product Inquiry</td>
        <td>M.CMS.INSURANCE.INQ</td>
        <td>R8V3</td>
        <td>/account/{accountNumber}/product</td>
        <td>GET</td>
    </tr>
    <tr>
        <td>Monetary Inquiry</td>
        <td>M.CMS.FLCN.MON.TRANSFER.INQ</td>
        <td>L8V1</td>
        <td>/account/v1/falconMonetaryInquiry</td>
        <td>POST</td>
    </tr>
    <tr>
        <td>Multi Wallet Priority Order Update</td>
        <td>M.CMS.WALLET.PRTYORDER.UPD</td>
        <td>R8V1</td>
        <td>/account/wallet-priority-order</td>
        <td>PUT</td>
    </tr>
    <tr>
        <td>Offer Enrollment Add</td>
        <td>M.OMS.ENROLL.ADD</td>
        <td>R8V1</td>
        <td>/account/enrollment</td>
        <td>POST</td>
    </tr>
    <tr>
        <td>Offer Enrollment Update</td>
        <td>M.OMS.ENROLL.ACTION.UPD</td>
        <td>R8V1</td>
        <td>/account/enrollment</td>
        <td>PUT</td>
    </tr>
    <tr>
        <td>Organization Rule Levels Add</td>
        <td>M.CMS.RULE.LIMIT.ADD</td>
        <td>L8V1</td>
        <td>/account/organizationNumber/level-limits</td>
        <td>POST</td>
    </tr>
    <tr>
        <td>Organization Rule Levels Inquiry</td>
        <td>M.CMS.RULE.LIMIT.INQ</td>
        <td>L8V1</td>
        <td>/account/{organizationNumber}/level-limits</td>
        <td>GET</td>
    </tr>
    <tr>
        <td>Organization Rule Levels Update</td>
        <td>M.CMS.RULE.LIMIT.UPD</td>
        <td>L8V1</td>
        <td>/account/organizationNumber/level-limits</td>
        <td>PUT</td>
    </tr>
    <tr>
        <td>Pending Bank, Branch And Store Update</td>
        <td>M.CMS.PEND.BANK.UPD</td>
        <td>R8V1</td>
        <td>/account/bank-branch-store</td>
        <td>PUT</td>
    </tr>
    <tr>
        <td>Prepaid Load Limits Update</td>
        <td>M.CMS.PPD.LOAD.LMTS.UPD</td>
        <td>L8V1</td>
        <td>/account/ppd-load-limits</td>
        <td>PUT</td>
    </tr>
    <tr>
        <td>Prepaid Over Limit Update</td>
        <td>M.CMS.PPD.OVERLIMIT.UPD</td>
        <td>L8V1</td>
        <td>/account/ppd-over-limit</td>
        <td>PUT</td>
    </tr>
    <tr>
        <td>Pricing Control Table Update</td>
        <td>M.CMS.PRICING.CTRL.UPD</td>
        <td>R8V1</td>
        <td>/account/pctId</td>
        <td>PUT</td>
    </tr>
    <tr>
        <td>Product Transfer Update</td>
        <td>M.CMS.ACCT.PRODTRANSFER.UPD</td>
        <td>L8V3</td>
        <td>/account/productTransfer</td>
        <td>PUT</td>
    </tr>
    <tr>
        <td>Restructure and Refinance Inquiry</td>
        <td>M.CMS.REFINANCERESTRUCTURE.INQ</td>
        <td>R8V1</td>
        <td>/account/{accountNumber}/balance</td>
        <td>GET</td>
    </tr>
    <tr>
        <td>Reversal Vinculate</td>
        <td>M.CMS.VINCULATION.REV.UPD</td>
        <td>L8V1</td>
        <td>/account/vinculation-reversal</td>
        <td>PUT</td>
    </tr>
    <tr>
        <td>Service Charge/Fee Table Override Update</td>
        <td>M.CMS.SVCFEE.TBL.OVRD.UPD</td>
        <td>R8V1</td>
        <td>/account/service-charge-table</td>
        <td>PUT</td>
    </tr>
    <tr>
        <td>Skip Payment Update</td>
        <td>M.CMS.SKIPPMT.UPD</td>
        <td>R8V1</td>
        <td>/account/skip-payment</td>
        <td>PUT</td>
    </tr>
    <tr>
        <td>Statement Installment Options Inquiry</td>
        <td>M.CMS.INSTSTMTSIM.ACT</td>
        <td>L8V1</td>
        <td>/account/v1/statementInstallments</td>
        <td>GET</td>
    </tr>
    <tr>
        <td>Statement Installment Options Simulation and Confirmation</td>
        <td>M.CMS.INSTSTMTSIM.ACT</td>
        <td>L8V1</td>
        <td>/account/v1/statementInstallments/{numberOfTerms}</td>
        <td>PUT</td>
    </tr>
    <tr>
        <td>Transfer Promotional Product Upgrade</td>
        <td>M.CMS.PROM.PROD.UPG.UPD</td>
        <td>L8V1</td>
        <td>/account/transfer-promotional-product</td>
        <td>PUT</td>
    </tr>
    <tr>
        <td>Updated Debit Balances Inquiry</td>
        <td>M.CMS.ACCT.INST.BAL.INQ</td>
        <td>L8V1</td>
        <td>/account/v1/debitBalance</td>
        <td>GET</td>
    </tr>
    <tr>
        <td>User Codes Update</td>
        <td>M.CMS.ACCT.USER.DATA.UPD</td>
        <td>R8V1</td>
        <td>/account/userData</td>
        <td>PUT</td>
    </tr>
    <tr>
        <td colspan="5" align="center"><b>Cards</b></td>
    </tr>
    <tr>
        <td>Account Card Assignment</td>
        <td>M.CMS.PREPAIDACCT.ASSIGN.UPD</td>
        <td>L8V1</td>
        <td>/cards/v1/cards/account</td>
        <td>PUT</td>
    </tr>
    <tr>
        <td>Account To Card Inquiry</td>
        <td>M.CMS.ACCT.TO.CARD.INQ</td>
        <td>L8V3</td>
        <td>/cards/embosser/card-details-L8V3</td>
        <td>POST</td>
    </tr>
    <tr>
        <td>Card Action Update</td>
        <td>M.CMS.EMB.CARDACTION.UPD</td>
        <td>L8V2</td>
        <td>/cards/embosser/cardAction-L8V2</td>
        <td>PUT</td>
    </tr>
    <tr>
        <td>Card Activation</td>
        <td>M.CMS.CARDACTIVATION.UPD</td>
        <td>R8V3</td>
        <td>/cards/activation</td>
        <td>PUT</td>
    </tr>
    <tr>
        <td>Card and Account Details Inquiry</td>
        <td>M.CMS.CHANNEL.INQ</td>
        <td>L8V1</td>
        <td>/cards/details</td>
        <td>POST</td>
    </tr>
    <tr>
        <td>Card Or PAN Token Inquiry</td>
        <td>M.CMS.CARD.PAN.INQ</td>
        <td>L8V2</td>
        <td>/cards/embosser/card-pan-l8v2</td>
        <td>POST</td>
    </tr>
    <tr>
        <td>Card Status Update</td>
        <td>M.CMS.CARD.STATUS.UPD</td>
        <td>L8V1</td>
        <td>/cards/status-L8V1</td>
        <td>PUT</td>
    </tr>
    <tr>
        <td>Card Transfer Update</td>
        <td>M.CMS.CARDTRANSFER.UPD</td>
        <td>L8V5</td>
        <td>/cards/transfer</td>
        <td>PUT</td>
    </tr>
    <tr>
        <td>Credit Limit Update</td>
        <td>M.CMS.CREDITLIMIT.UPD</td>
        <td>R8V1</td>
        <td>/cards/credit-limit</td>
        <td>PUT</td>
    </tr>
    <tr>
        <td>Dynamic Values Inquiry</td>
        <td>M.CMS.GENERATE.DCVV2</td>
        <td>R8V1</td>
        <td>/cards/pin/dynamic-values</td>
        <td>POST</td>
    </tr>
    <tr>
        <td>Embosser Add</td>
        <td>M.CMS.EMBOSSER.ADD</td>
        <td>L8VF</td>
        <td>/cards/embosser/l8vf</td>
        <td>POST</td>
    </tr>
    <tr>
        <td>Embosser Block Code Update</td>
        <td>M.CMS.EMB.BLKCD.UPD</td>
        <td>R8V1</td>
        <td>/cards/embosser/block</td>
        <td>PUT</td>
    </tr>
    <tr>
        <td>Embosser Inquiry</td>
        <td>M.CMS.EMBOSSER.INQ</td>
        <td>L8VE</td>
        <td>/cards/v2/embosser/details</td>
        <td>POST</td>
    </tr>
    <tr>
        <td>Embosser List Inquiry</td>
        <td>M.CMS.EMB.LIST.INQ</td>
        <td>L8V1</td>
        <td>/cards/v1/embosser/search</td>
        <td>POST</td>
    </tr>
    <tr>
        <td>Embosser Navigational Inquiry</td>
        <td>M.CMS.EMB.NAV.SVC</td>
        <td>R8V1</td>
        <td>/cards/embosser/{cardNumber}/navigational</td>
        <td>GET</td>
    </tr>
    <tr>
        <td>Embosser Update</td>
        <td>M.CMS.EMBOSSER.UPD</td>
        <td>L8V6</td>
        <td>/cards/v3/embosser</td>
        <td>PUT</td>
    </tr>
    <tr>
        <td>Invalid Attempts Inquiry</td>
        <td>M.CMS.INV.PINTRIES.CTR.INQ</td>
        <td>L8V1</td>
        <td>/cards/pin/invalid-attempts</td>
        <td>POST</td>
    </tr>
    <tr>
        <td>Mass Card Issue Update</td>
        <td>M.CMS.MASS.CARD.ISSUE.UPD</td>
        <td>L8V3</td>
        <td>/cards/mass-card-issue-L8V3</td>
        <td>POST</td>
    </tr>
    <tr>
        <td>Mass Card Reissue Inquiry</td>
        <td>M.CMS.MASS.CARD.ISSUE.INQ</td>
        <td>L8V3</td>
        <td>/cards/mass-card-issue-L8V3</td>
        <td>GET</td>
    </tr>
    <tr>
        <td>PIN Block/Unblock</td>
        <td>M.CMS.PIN.BLOCK.UPD</td>
        <td>R8V1</td>
        <td>/cards/pin/status</td>
        <td>PUT</td>
    </tr>
    <tr>
        <td>PIN Change</td>
        <td>M.CMS.PIN.CHANGE</td>
        <td>R8V2</td>
        <td>/cards/pin/pin-change</td>
        <td>PUT</td>
    </tr>
    <tr>
        <td>PIN Reassign</td>
        <td>M.CMS.PIN.REASSIGNMENT</td>
        <td>R8V1</td>
        <td>/cards/pin/</td>
        <td>PUT</td>
    </tr>
    <tr>
        <td>PIN Validate</td>
        <td>M.CMS.PIN.VALIDATE</td>
        <td>R8V1</td>
        <td>/cards/pin/validation</td>
        <td>POST</td>
    </tr>
    <tr>
        <td>Same Day Plastic Add/Update</td>
        <td>M.CMS.SAMEDAYPLASTIC.UPD</td>
        <td>R8V1</td>
        <td>/cards/embosser/sameDay</td>
        <td>POST</td>
    </tr>
    <tr>
        <td>Security Values Inquiry</td>
        <td>M.CMS.SEC.VALUES.INQ</td>
        <td>R8V1</td>
        <td>/cards/pin/security-codes</td>
        <td>POST</td>
    </tr>
    <tr>
        <td>Spending Limits Update</td>
        <td>M.CMS.CARDSPENDLIMITS.UPD</td>
        <td>L8V3</td>
        <td>/cards/spend-limits-L8V3</td>
        <td>PUT</td>
    </tr>
    <tr>
        <td>Statement Details By Date Inquiry</td>
        <td>M.CMS.STATEMENTDATE.INQ</td>
        <td>R8V2</td>
        <td>/cards/statement-detail/date</td>
        <td>POST</td>
    </tr>
    <tr>
        <td>Statement Inquiry</td>
        <td>M.CMS.STATEMENT.INQ</td>
        <td>R8V3</td>
        <td>/cards/statement-detail</td>
        <td>POST</td>
    </tr>
    <tr>
        <td>Temporary Credit Limit Update</td>
        <td>M.CMS.TEMP.CREDITLIMIT.UPD</td>
        <td>R8V1</td>
        <td>/cards/temporary-credit-limit</td>
        <td>PUT</td>
    </tr>
    <tr>
        <td>Travel Indicator Update</td>
        <td>M.CMS.TRAVELIND.UPD</td>
        <td>L8V1</td>
        <td>/cards/travel</td>
        <td>PUT</td>
    </tr>
    <tr>
        <td colspan="5" align="center"><b>Customers</b></td>
    </tr>
    <tr>
        <td>Account Number Inquiry</td>
        <td>M.CMS.CUST.TO.ACCT.INQ</td>
        <td>R8V3</td>
        <td>/customer/accountNumber</td>
        <td>POST</td>
    </tr>
    <tr>
        <td>Cards Details Inquiry</td>
        <td>M.CMS.CUSTCHANNEL.INQ</td>
        <td>L8V5</td>
        <td>/customer/v3/cards/details</td>
        <td>GET</td>
    </tr>
    <tr>
        <td>Cards Inquiry</td>
        <td>M.CMS.CUST.NBR.INQ</td>
        <td>L8V1</td>
        <td>/customer/v1/cards</td>
        <td>GET</td>
    </tr>
    <tr>
        <td>Current/Prior Address Inquiry</td>
        <td>M.CMS.ADDRESS.INQ</td>
        <td>R8V2</td>
        <td>/customer/{accountNumber}/current-prior-address</td>
        <td>GET</td>
    </tr>
    <tr>
        <td>Customer Add</td>
        <td>M.CMS.CUSTOMER.ADD</td>
        <td>L8V2</td>
        <td>/customer/l8v2</td>
        <td>POST</td>
    </tr>
    <tr>
        <td>Customer and Account Number Generate</td>
        <td>M.CMS.NBRGENERATION.ACT</td>
        <td>L8V1</td>
        <td>/customer/generation</td>
        <td>POST</td>
    </tr>
    <tr>
        <td>Customer Reversal Update</td>
        <td>M.CMS.CUST.REVERSAL.UPD</td>
        <td>L8V1</td>
        <td>/customer/reversal</td>
        <td>PUT</td>
    </tr>
    <tr>
        <td>Customer Update</td>
        <td>M.CMS.CUSTOMER.UPD</td>
        <td>R8V5</td>
        <td>/customer/</td>
        <td>PUT</td>
    </tr>
    <tr>
        <td>Customer with PAN Activation Add</td>
        <td>M.CMS.CUST.ACTIVATE.ADD</td>
        <td>L8V1</td>
        <td>/customer/activation</td>
        <td>POST</td>
    </tr>
    <tr>
        <td>Demographic Inquiry</td>
        <td>M.CMS.DEMOGRAPHIC.INQ</td>
        <td>L8V2</td>
        <td>/customer/demographicData-l8v2</td>
        <td>POST</td>
    </tr>
    <tr>
        <td>Relationship Number Add</td>
        <td>M.CMS.RELATIONSHIP.ADD</td>
        <td>R8V2</td>
        <td>/customer/relationship</td>
        <td>POST</td>
    </tr>
    <tr>
        <td>Relationship Number Inquiry</td>
        <td>M.CMS.REL.CUST.INQ</td>
        <td>L8V1</td>
        <td>/customer/{customerNumber}/relationship</td>
        <td>GET</td>
    </tr>
    <tr>
        <td colspan="5" align="center"><b>Loyalty</b></td>
    </tr>
    <tr>
        <td>Cross Reference Inquiry</td>
        <td>M.LMS.ACCOUNT.XREF.INQ</td>
        <td>R8V1</td>
        <td>/loyalty/crossReference</td>
        <td>POST</td>
    </tr>
    <tr>
        <td>Demographic Data Inquiry</td>
        <td>M.LMS.DEMOGRAPHIC.INQ</td>
        <td>R8V2</td>
        <td>/loyalty/demographic/{accountNumber}</td>
        <td>GET</td>
    </tr>
    <tr>
        <td>Loyalty Account Transactions Inquiry</td>
        <td>M.LMS.STMT.LIST.INQ</td>
        <td>R8V1</td>
        <td>/loyalty/statementLists</td>
        <td>POST</td>
    </tr>
    <tr>
        <td>Points Account Add</td>
        <td>M.LMS.POINTS.ACCT.ADD</td>
        <td>R8V1</td>
        <td>/loyalty/pointsAccount</td>
        <td>POST</td>
    </tr>
    <tr>
        <td>Points Account Adjustment</td>
        <td>M.LMS.POINTS.ADJ.ADD</td>
        <td>R8V1</td>
        <td>/loyalty/pointsAdjust</td>
        <td>PUT</td>
    </tr>
    <tr>
        <td>Points Account Auto Disbursement Data Update</td>
        <td>M.LMS.POINTS.ACCT.DISB.DATA.UP</td>
        <td>R8V2</td>
        <td>/loyalty/pointsDisbursement</td>
        <td>PUT</td>
    </tr>
    <tr>
        <td>Points Account Inquiry</td>
        <td>M.LMS.POINTS.ACCT.INQ</td>
        <td>R8V2</td>
        <td>/loyalty/points</td>
        <td>POST</td>
    </tr>
    <tr>
        <td>Points Expiration Details Inquiry</td>
        <td>M.LMS.POINTS.EXPIRY.HIST.INQ</td>
        <td>R8V1</td>
        <td>/loyalty/pointsExpireHistory</td>
        <td>POST</td>
    </tr>
    <tr>
        <td>Redemption Transaction Add</td>
        <td>M.LMS.REDEMPTION.ADD</td>
        <td>R8V1</td>
        <td>/loyalty/redemption</td>
        <td>POST</td>
    </tr>
    <tr>
        <td>Statement Lists Inquiry</td>
        <td>M.LMS.TRANSACTION.INQ</td>
        <td>R8V1</td>
        <td>/loyalty/</td>
        <td>POST</td>
    </tr>
    <tr>
        <td>Statement Summary Inquiry</td>
        <td>M.LMS.STMT.SUMMARY.INQ</td>
        <td>R8V1</td>
        <td>/loyalty/statementSummary/{accountNumber}</td>
        <td>GET</td>
    </tr>
    <tr>
        <td colspan="5" align="center"><b>Tokenization</b></td>
    </tr>
    <tr>
        <td>Available Cards Inquiry</td>
        <td>M.CMS.AVAIL.SELECT.CARD.INQ</td>
        <td>L8V1</td>
        <td>/vtis/v1/getAvailableCards</td>
        <td>POST</td>
    </tr>
    <tr>
        <td>Check Eligibility</td>
        <td>M.FAS.CHECK.ELIGIBILITY.INQ</td>
        <td>L8V1</td>
        <td>/vtis/v1/checkEligibility</td>
        <td>POST</td>
    </tr>
    <tr>
        <td>Device Token Binding Request</td>
        <td>M.FAS.DEVICE.TOKEN.BINDING</td>
        <td>L8V1</td>
        <td>/vtis/v1/tokenRequestors/{tokenRequestorID}/tokens/{tokenReferenceID}/deviceBinding</td>
        <td>POST</td>
    </tr>
    <tr>
        <td>PAN Life Cycle</td>
        <td></td>
        <td></td>
        <td>/vtis/v1/pan/lifecycle</td>
        <td>POST</td>
    </tr>
    <tr>
        <td>Selected Cards Inquiry</td>
        <td>M.CMS.AVAIL.SELECT.CARD.INQ</td>
        <td>L8V1</td>
        <td>/vtis/v1/getSelectedCards</td>
        <td>POST</td>
    </tr>
    <tr>
        <td>Token Life Cycle</td>
        <td></td>
        <td></td>
        <td>/vtis/v1/tokenRequestors/{tokenRequestorID}/tokens/{tokenReferenceID}/lifecycle</td>
        <td>POST</td>
    </tr>
    <tr>
        <td colspan="5" align="center"><b>Transactions</b></td>
    </tr>
    <tr>
        <td>Token Notification Create</td>
        <td>M.FAS.TOKEN.NOTIFICATION.UPD</td>
        <td>L8V1</td>
        <td>/vtis/v2/tokenRequestors/{tokenRequestorID}/tokens/{tokenReferenceID}/tokenChanged</td>
        <td>POST</td>
    </tr>
    <tr>
        <td>Account Enrollment Inquiry</td>
        <td>M.OMS.ENRHISTORY.INQ</td>
        <td>R8V1</td>
        <td>/transactions/enroll-history/{accountNumber}</td>
        <td>GET</td>
    </tr>
    <tr>
        <td>Currency Rate Add</td>
        <td>M.SSC.EXCH.RATE.ADD</td>
        <td>L8V1</td>
        <td>/transactions/currency-rate</td>
        <td>POST</td>
    </tr>
    <tr>
        <td>Currency Rate Inquiry</td>
        <td>M.SSC.EXCH.RATE.INQ</td>
        <td>L8V1</td>
        <td>/transactions/currency-rate</td>
        <td>GET</td>
    </tr>
    <tr>
        <td>Currency Rate Table Update</td>
        <td>M.CMS.CURR.RATE.MWP.UPD</td>
        <td>R8V1</td>
        <td>/transactions/currency-rate-table</td>
        <td>PUT</td>
    </tr>
    <tr>
        <td>Currency Rate Update</td>
        <td>M.SSC.EXCH.RATE.UPD</td>
        <td>L8V1</td>
        <td>/transactions/currency-rate</td>
        <td>PUT</td>
    </tr>
    <tr>
        <td>Exchange Rate Update</td>
        <td>M.SSC.EXCHANGE.RATE.UPD</td>
        <td>L8V1</td>
        <td>/transactions/exchange-rate</td>
        <td>PUT</td>
    </tr>
    <tr>
        <td>Fee Table Information Inquiry</td>
        <td>M.CMS.SERV.FEE.TBL.INQ</td>
        <td>R8V1</td>
        <td>/transactions/{feeTableNumber}/fee-table-information</td>
        <td>GET</td>
    </tr>
    <tr>
        <td>Installment Billing Transaction Detail</td>
        <td>M.CMS.INSTAL.TERMS.INQ</td>
        <td>L8V1</td>
        <td>/transactions/br/v1/installmentTransactions/{installmentTransaction-Id}/terms</td>
        <td>GET</td>
    </tr>
    <tr>
        <td>Installment Detail Simulation - Anticipation Amount</td>
        <td>M.CMS.INSTAL.TRXN.DETAIL.UPD</td>
        <td>L8V1</td>
        <td>/transactions/v1/installmentTransactions/{installmentTransaction-Id}/anticipationAmount/simulation</td>
        <td>PUT</td>
    </tr>
    <tr>
        <td>Installment Detail Simulation - Anticipation Amount with no payment required</td>
        <td>M.CMS.INSTAL.TRXN.DETAIL.UPD</td>
        <td>L8V1</td>
        <td>/transactions/v1/installmentTransactions/{installmentTransaction-Id}/termsAnticipationNumber/simulation</td>
        <td>PUT</td>
    </tr>
    <tr>
        <td>Installment Detail Simulation - Anticipation Total Number of Installments</td>
        <td>M.CMS.INSTAL.TRXN.DETAIL.UPD</td>
        <td>L8V1</td>
        <td>/transactions/v1/installmentTransactions/{installmentTransaction-Id}/termsIdAnticipation/simulation</td>
        <td>PATCH</td>
    </tr>
    <tr>
        <td>Installment Detail Simulation - Discount Percentage to Early Release</td>
        <td>M.CMS.INSTAL.TRXN.DETAIL.UPD</td>
        <td>L8V1</td>
        <td>/transactions/v1/installmentTransactions/{installmentTransaction-Id}/simulation</td>
        <td>PATCH</td>
    </tr>
    <tr>
        <td>Installment Detail Simulation - Individual Installment-based Anticipation</td>
        <td>M.CMS.INSTAL.TRXN.DETAIL.UPD</td>
        <td>L8V1</td>
        <td>/transactions/v1/installmentTransactions/{installmentTransaction-Id}/termsIdAnticipation/simulation</td>
        <td>PUT</td>
    </tr>
    <tr>
        <td>Installment Details Inquiry</td>
        <td>M.CMS.INSTAL.TRXN.DETAIL.UPD</td>
        <td>L8V1</td>
        <td>/transactions/v1/installmentTransactions/{installmentTransaction-Id}</td>
        <td>GET</td>
    </tr>
    <tr>
        <td>Installment Summary Inquiry</td>
        <td>M.CMS.INSTAL.SUMMARY.INQ</td>
        <td>L8V1</td>
        <td>/transactions/v1/installmentTransactions/terms</td>
        <td>GET</td>
    </tr>
    <tr>
        <td>Installment Terms Update</td>
        <td>M.CMS.INSTAL.TERMS.UPD</td>
        <td>L8V1</td>
        <td>/transactions/v1/installmentTransactions/{installmentTransaction-Id}/terms/termsIdAnticipation/simulation</td>
        <td>PUT</td>
    </tr>
    <tr>
        <td>Installment Transaction Inquiry</td>
        <td>M.CMS.INSTAL.TRXN.DATA.INQ</td>
        <td>L8V2</td>
        <td>/transactions/v2/installmentTransactions</td>
        <td>GET</td>
    </tr>
    <tr>
        <td>Installment Transaction Terms Simulation</td>
        <td>M.CMS.INSTAL.TERMS.INQ</td>
        <td>L8V2</td>
        <td>/transactions/v2/installmentTransactions/{installmentTransaction-Id}/terms</td>
        <td>GET</td>
    </tr>
    <tr>
        <td>Insurance Table Inquiry</td>
        <td>M.CMS.INS.TBL.INQ</td>
        <td>R8V1</td>
        <td>/transactions/{tableInsurance}/insurance-table</td>
        <td>GET</td>
    </tr>
    <tr>
        <td>Loan Payoff Quote Generate</td>
        <td>M.CMS.PLAN.STTLMNT.QUOTE.UPD</td>
        <td>R8V1</td>
        <td>/transactions/plan-settlement-quote</td>
        <td>POST</td>
    </tr>
    <tr>
        <td>Logo Block Codes Inquiry</td>
        <td>M.CMS.LOGO.BLKCD.INQ</td>
        <td>R8V1</td>
        <td>/transactions/logo-block-codes</td>
        <td>GET</td>
    </tr>
    <tr>
        <td>Logo Inquiry</td>
        <td>M.CMS.LOGO.INQ</td>
        <td>R8V1</td>
        <td>/transactions/logo</td>
        <td>GET</td>
    </tr>
    <tr>
        <td>Memo Information Add</td>
        <td>M.ASM.NONMON.ACT</td>
        <td>R8V5</td>
        <td>/transactions/non-monetary-action-code</td>
        <td>POST</td>
    </tr>
    <tr>
        <td>Notes History Inquiry</td>
        <td>M.ASM.NOTES.HISTORY.INQ</td>
        <td>R8V3</td>
        <td>/transactions/notes-R8V3</td>
        <td>POST</td>
    </tr>
    <tr>
        <td>Offer Inquiry</td>
        <td>M.OMS.OFFER.INQ</td>
        <td>R8V1</td>
        <td>/transactions/offer</td>
        <td>GET</td>
    </tr>
    <tr>
        <td>Offer List Inquiry</td>
        <td>M.OMS.OFFERDEFLIST.INQ</td>
        <td>R8V1</td>
        <td>/transactions/offer-list</td>
        <td>GET</td>
    </tr>
    <tr>
        <td>Organization Inquiry</td>
        <td>M.CMS.ORG.INQ</td>
        <td>R8V1</td>
        <td>/transactions/organization</td>
        <td>GET</td>
    </tr>
    <tr>
        <td>Outstanding Authorizations Inquiry</td>
        <td>M.FAS.OUTSTANDING.AUTH.INQ</td>
        <td>L8V3</td>
        <td>/transactions/outstanding-authorizations-L8V3/details</td>
        <td>POST</td>
    </tr>
    <tr>
        <td>PCT Table Inquiry</td>
        <td>M.CMS.PCT.TBL.INQ</td>
        <td>R8V1</td>
        <td>/transactions/pct-table</td>
        <td>GET</td>
    </tr>
    <tr>
        <td>Posted Authorizations Inquiry</td>
        <td>M.CMS.OUTSTANDING.AUTH.INQ</td>
        <td>R8V2</td>
        <td>/transactions/outstanding-authorizations/{accountNumber}</td>
        <td>GET</td>
    </tr>
    <tr>
        <td>Prepaid Logo Inquiry</td>
        <td>M.CMS.LOGO.PREPD.INQ</td>
        <td>R8V1</td>
        <td>/transactions/prepaid-logo</td>
        <td>GET</td>
    </tr>
    <tr>
        <td>Prepaid MCC Criteria Table Inquiry</td>
        <td>M.CMS.TAX.TBL.INQ</td>
        <td>R8V1</td>
        <td>/transactions/mcct-table</td>
        <td>GET</td>
    </tr>
    <tr>
        <td>Promotional Rate Expiration Disclosure Update</td>
        <td>M.CMS.PROMORATE.UPD</td>
        <td>R8V1</td>
        <td>/transactions/promo-rate</td>
        <td>PUT</td>
    </tr>
    <tr>
        <td>Quote Projections Update</td>
        <td>M.CMS.QUOTE.PROJ.UPD</td>
        <td>L8V1</td>
        <td>/transactions/quote-projections</td>
        <td>PUT</td>
    </tr>
    <tr>
        <td>Transaction Conversion</td>
        <td>M.CMS.INST.TRAN.CONV</td>
        <td>R8V1</td>
        <td>/transactions/installmentConversion</td>
        <td>PUT</td>
    </tr>
    <tr>
        <td>Transactions Details Inquiry</td>
        <td>M.CMS.TRANSACTIONDETAIL.INQ</td>
        <td>L8V7</td>
        <td>/transactions/summary-details</td>
        <td>POST</td>
    </tr>
</table>

## Version 1.1.0

[Table here]

## Version 1.0.0

[Table here]
---
tags: [Main Cases, Falcon, fraud, detection, prevention, management]
---

# Falcon System Integration

Falcon is a fraud detection, prevention and management application. Falcon examines all incoming transactions and determines the probability of the transaction being fraudulent. Falcon has it’s own neural network which asses the transaction coming to falcon. Based on several factors, scores the transaction and provides a Falcon score, which tells the likelihood of a fraudulent transaction.

Falcon works with real time transactions that are scored in Falcon and a score from zero to 999 will be generated for each of one. These transaction furthers traverse through the different set of rules as per business need to identify fraud. At end, Falcon will send the scoring response message to the Authorization Host system, e.g. decline the Authorization and block the card. Activating parameter on First Vision, is possible integrate with Falcon, so authorization transactions processed by FirstVision will be routed to Falcon to stablish a fraud control.

![image](https://user-images.githubusercontent.com/111396588/208846621-4b1bd3c3-0355-48ff-a23a-0d6f313ec3d0.png)

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
- [Digital Card Issuing](?path=docs/main-cases/11-digital.md)
- [Pan Token](?path=docs/main-cases/12-pan-token.md)
- [PIN Change](?path=docs/main-cases/13-pin-change.md)
- [Dynamic CVV2](?path=docs/main-cases/14-dynamic.md)
- [Audit and Monitoring](?path=docs/main-cases/15-audit.md)
- [HMAC Signature](?path=docs/main-cases/16-hmac.md)

---

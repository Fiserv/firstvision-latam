---
tags: [Main Cases, HMAC Signature]
---

# What is HMAC Signature

HMAC, a hash-based message authentication code, is a security check that generates a hash signature for every message sent from one point to another.

When you send a message to a server, with HMAC enabled, a new signature is generated for your message, according to your secret key.

Client and server must have the same secret key so they can verify the authenticity of the message and its integrity, as modified messages result in different signatures.

The same message generated with the same secret key will always result in the same signature

![image](https://user-images.githubusercontent.com/111396588/208850051-95699fa8-b605-42c3-995b-50e1f10c0a43.png)


## Why use

With HMAC verification enabled, you can guarantee the authenticity of the message sender and certify that the message has not been intercepted and modified by hackers.

## How to use

You'll need a tool to generate your HMAC messages, based on your secret key. Most programming languages have a many librabries that can help you to send or verify sender authenticity and message integrity.

You just need to enter the common hashing algorithm, the message and your secret key to generate your signed HMAC message.

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
- [Digital Card Issuing](?path=docs/main-cases/11-digital.md)
- [Pan Token](?path=docs/main-cases/12-pan-token.md)
- [PIN Change](?path=docs/main-cases/13-pin-change.md)
- [Dynamic CVV2](?path=docs/main-cases/14-dynamic.md)
- [Audit and Monitoring](?path=docs/main-cases/15-audit.md)

---

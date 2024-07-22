# Message Level Encryption 

Sensitive information will be encrypted using JSON Web Encryption (JWE). JSON Web Encryption represents encrypted content using JavaScript Object Notation (JSON)-based data structures. For complete specifications, please refer to the [JWE specification](https://datatracker.ietf.org/doc/html/draft-ietf-jose-json-web-encryption-40). 

To confirm if the APIs you intend to use support JWE encryption, please contact our client services team. 

## Public Key Generation

Issuers will generate an RSA Public/Private Key Pair using any Cryptography & SSL/TLS Toolkit compatible with OpenSSL. 

### Example Commands using OpenSSL:

1. Generate an RSA private key, of size 2048, and output it to a file named key.pem:

```
openssl genrsa -out key.pem 2048
```

2. Extract the public key and output it to a file named public.pem: 

```
openssl rsa -in key.pem -outform PEM -pubout -out public.pem
```

The public.pem file generated from the commands above will be shared with the Fiserv API implementations team. 

## Encryption Key ID

Fiserv will receive the public key shared by the issuer and will send a KID (Key ID) in return. The KID is an alphanumeric identifier of the public key.  

The issuer will used the KID shared by Fiserv to identify the corresponding private key. 

![test1](../../../assets/images/1-.png)

The KID will be sent by Fiserv in the encrypted message, the issuer will use this KID to retrieve the corresponding private key. 

### Example JWE Structure Including the KID:

[test]: <https://raw.githubusercontent.com/Fiserv/firstvision-latam/main/assets/images/1-.png>

## Key Rotation Process

The issuer will share a new public key with Fiserv, Fiserv will send the corresponding KID. 

During a scheduled maintenance window, Fiserv will mark the new KID as the active one. The issuer will receive the new KID and will retrieve the corresponding private key for decryption. The main goal of using a KID is to optimize the key rotation process. 

### Sample Decryption Code

During implementation project Fiserv will share with the issuer the sample code for decryption.

---

## See Also

- [API Glossary](?path=docs/english/api-reference/api-glossary.md)
- [API Request](?path=docs/english/api-reference/api-request.md)
- [Error Handling](?path=docs/english/api-reference/response-handling.md)
- [Error Response](?path=docs/english/api-reference/error-response.md)
- [Webhook](?path=docs/english/api-reference/5-notifications.md)

---

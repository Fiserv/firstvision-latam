---
tags: [API Reference, Request Header, Request Body, Header]
---

# API Request 

## Request Header

RESTful API has a consistent header structure based on a set of parameters.

<!--
type: tab
titles: Header, Request Header Example
-->

To create the header, provide the following values:

| Variable              |    Type   | Length | Description/Values                                                                                                                                                       |
|-----------------------|:---------:|:------:|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `Content-Type`        |  *string* |   N/A  | The content type. Valid Value: application/json                                                                                                                          |
| `apikey`              |  *string* |   N/A  | API Key provided to the merchant associating the requests with the appropriate app in the Developer Portal.                                                              |
| `Signature`           |  *string* |   N/A  | HMAC signature used to verify the authenticity and integrity of data transmitted.                                                                                        |
| `X-ClientID`          |  *string* |   N/A  | Client Identifier.                                                                                                                                                       |
| `Authorization`       |  *string* |   N/A  | Authorization Bearer Token.                                                                                                                                              |
| `X-Client-Request-Id` |  *string* |   40   | A client-generated ID for request tracking and signature creation, unique per request.                     .                                                             |
| `Timestamp`           | *integer* |   N/A  | Epoch timestamp in milliseconds in the request from a client system. Used for Message Signature generation and time limit (5 mins).                                      |

<!--
type: tab
-->

```json
"header": {
  "Content-Type": "application/json",
  "apikey": "API_KEY",
  "Signature": "SIGNATURE",
  "X-ClientID": "X-ClientID",
  "Authorization": "ACCESS_TOKEN"
  "X-Client-Request-Id": "X-CLIENT_REQUEST_ID",
  "Timestamp": "TIMESTAMP"
}
```

<!-- type: tab-end -->

---

## Request Body

The body of the transaction request differs based on the transaction being initiated.

<!--
type: tab
titles: Request Body Example
-->

```json
{
  "amount": {
    "total": "12.04",
    "currency": "USD"
  },
  "paymentSource": {
    "sourceType": "PaymentCard",
    "card": {
      "cardData": "4005550000000019",
      "expirationMonth": "02",
      "expirationYear": "2035",
      "securityCode": "123"
    }
  },
  "transactionDetails": {
    "captureFlag": true
  },
  "merchantDetails": {
    "merchantId": "123456789789567",
    "terminalId": "123456"
  }
}
```

<!-- type: tab-end -->

---

## See Also

- [Access Token](?path=docs/english/api-reference/accessToken.md)
- [API Glossary](?path=docs/english/api-reference/api-glossary.md)
- [Error Handling](?path=docs/english/api-reference/response-handling.md)
- [Message Level Encryption](?path=docs/english/api-reference/encryption.md)
- [Webhook](?path=docs/english/api-reference/5-notifications.md)

---

---
tags: [API Reference, Webhook, Events]
---

# Webhook

Webhooks are a way for systems to send real-time notifications about events that have occurred. They work by allowing a client to provide a service that can receive notifications whenever certain events happen in Fiserv systems . With webhooks, applications can be kept up-to-date on things like authorization changes, card or account updates, and fraud alerts.

To use webhooks, FirstVision can send an HTTP POST request to a designated endpoint whenever an event occurs. This sends a notification to the receiving application, which can then take any necessary action in response. Webhooks provide a quick and efficient way for different systems to communicate and stay informed about important events.

![image](https://user-images.githubusercontent.com/111396588/209873236-86eb54b6-f214-4f8f-9652-51c03ad8d604.png)

## Webhooks Events

### Authorization

Request example:

```json
{
  "contact": [
    {
      "value": "mail@domain.com",
      "contactType": "PRINCIPAL_EMAIL"
    }
  ],
  "metadata": [
    {
      "key": "M_LINE_21",
      "value": "00"
    }
  ],
  "cardNumber": "000540208ID5IXX3865",
  "description": "APPROVED",
  "transaction": {
    "id": "01765999999998 2013572895880110A00000000000000000000 /12 00",
    "amount": "00000000010.00",
    "reason": "294",
    "currency": "MXN",
    "feeAmount": "00000000010.00",
    "acceptorName": "TEST MERCHANT",
    "cashbackAmount": "00000000010.00",
    "authorizationDate": "20221202",
    "authorizationTime": "141638",
    "additionInformation": "0120484MEXICO 0"
  }
}
```

### Account Life Cycle

Includes events for: **Payment Due Date Event and Account Cycle Event.**

Request example:

```json
{
  "contact": [
    {
      "value": "mail@domain.com",
      "contactType": "PRINCIPAL_EMAIL"
    }
  ],
  "metadata": [
    {
      "key": "M_LINE_21",
      "value": "0"
    }
  ],
  "description": "APPROVED",
  "transaction": {
    "eventDate": "20220127",
    "eventTime": "141638"
  }
}
```

### Account Management

Includes events for: **Available Credit Event, Payment Posted Event, Change of Address, Payment Due Date Change and Credit Limit Change.**

Request example:

```json
{
  "contact": [
    {
      "value": "mail@domain.com",
      "contactType": "PRINCIPAL_EMAIL"
    }
  ],
  "metadata": [
    {
      "key": "M_LINE_21",
      "value": "00"
    }
  ],
  "description": "APPROVED",
  "transaction": {
    "eventDate": "20220127",
    "eventTime": "141638"
  }
}
```

### Card Life Cycle

Includes events for: **Card Blocked Message, Activation Message and Card Action/Embossing.**

Request example:

```json
{
  "contact": [
    {
      "value": "mail@domain.com",
      "contactType": "PRINCIPAL_EMAIL"
    }
  ],
  "metadata": [
    {
      "key": "M_LINE_21",
      "value": "00"
    }
  ],
  "cardNumber": "000540208ID5IXX3865",
  "description": "APPROVED",
  "transaction": {
    "eventDate": "20221202",
    "eventTime": "141638",
    "blockReason": "TEST MERCHANT",
    "isActivated": "Y"
  }
}
```

### Fraud Authorization

Request example:

```json
{
  "contact": [
    {
      "value": "mail@domain.com",
      "contactType": "PRINCIPAL_EMAIL"
    }
  ],
  "metadata": [
    {
      "key": "M_LINE_21",
      "value": "00"
    }
  ],
  "cardNumber": "000540208ID5IXX3865",
  "description": "APPROVED",
  "transaction": {
    "amount": "00000000010.00",
    "reason": "294",
    "currency": "MXN",
    "eventDate": "20221202",
    "eventTime": "141638",
    "acceptorName": "TEST MERCHANT"
  }
}
```

### Fraud Block

Request example:

```json
{
  "contact": [
    {
      "value": "mail@domain.com",
      "contactType": "PRINCIPAL_EMAIL"
    }
  ],
  "metadata": [
    {
      "key": "M_LINE_21",
      "value": "00"
    }
  ],
  "cardNumber": "000540208ID5IXX3865",
  "description": "APPROVED",
  "transaction": {
    "reason": "294",
    "eventDate": "20221202",
    "eventTime": "141638",
    "blockReason": "MERCHANT"
  }
}
```

---

## See Also

- [API Glossary](?path=docs/english/api-reference/api-glossary.md)
- [API Request](?path=docs/english/api-reference/api-request.md)
- [Error Handling](?path=docs/english/api-reference/response-handling.md)
- [Error Response](?path=docs/english/api-reference/error-response.md)

---
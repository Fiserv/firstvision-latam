---
tags: [Referencia de la API, Webhook, Eventos]
---

# Webhook

Los webhooks son una forma en que los sistemas envían notificaciones en tiempo real sobre eventos que han ocurrido. Funcionan al permitir que un Cliente brinde un servicio que puede recibir notificaciones cada vez que ocurren ciertos eventos en los sistemas de Fiserv. Con los webhooks, las aplicaciones se pueden mantener actualizadas sobre cosas como cambios de autorización, actualizaciones de tarjetas o cuentas y alertas de fraude.

Para usar webhooks, FirstVision puede enviar una solicitud HTTP POST a un punto final designado siempre que ocurra un evento. Esto envía una notificación a la aplicación receptora, que luego puede tomar las medidas necesarias en respuesta. Los webhooks proporcionan una forma rápida y eficiente para que los diferentes sistemas se comuniquen y se mantengan informados sobre eventos importantes.

Para la implementación de Webhook, Fiserv proporciona los estándares y el diseño de API para los diferentes Endpoints que los Clientes necesitan implementar por su parte. Esos endpoints están a cargo de las notificaciones al Usuario Final y cualquier otra funcionalidad que los Clientes quieran tener internamente.

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

## Ver también

- [Glosario API](?path=docs/spanish/referencia-api/glosario-api.md)
- [Manejo de Respuesta](?path=docs/spanish/referencia-api/manejo-respuesta.md)
- [Respuesta de Error](?path=docs/spanish/referencia-api/respuesta-error.md)
- [Solicitud de API](?path=docs/spanish/referencia-api/solicitud-api.md)

---

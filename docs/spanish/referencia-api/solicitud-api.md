---
tags: [Referencia de la API, Encabezado de Solicitudes, Cuerpo de Solicitudes, Encabezado]
---

# Solicitud de API

## Encabezado de Solicitud

RESTful API tiene una estructura de encabezado coherente basada en un set de parámetros.

<!--
type: tab
titles: Header, Ejemplo de Encabezado de Solicitud
-->

To create the header, provide the following values:

| Variable              | Tipo      | Longitud | Descripción/Valores                                                                                                                                                     |
|-----------------------|-----------|----------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `Content-Type`        |  *string* |   N/A    | Los tipos de contenido. Valor Válido application/json                                                                                                                   |
| `apikey`              |  *string* |   N/A    | API Key proporcionada al comercio que asocia las solicitudes con la aplicación adecuada en el Developer Portal.                                                         |
| `Signature`           |  *string* |   N/A    | Firma HMAC utilizada para verificar la autenticidad e integridad de los datos transmitidos.                                                                             |
| `X-ClientID`          |  *string* |   N/A    | Identificador del cliente.                                                                                                                                              |
| `Authorization`       |  *string* |   N/A    | Token portador de autorización.                                                                                                                                         |
| `X-Client-Request-Id` |  *string* |   40     | Identificación generada por el cliente para el seguimiento de solicitudes y la creación de firmas, única por solicitud.                                                 |
| `Timestamp`           | *integer* |   N/A    | Marca de tiempo de época en milisegundos en la solicitud de un sistema Cliente. Se utiliza para la generación de firmas de mensajes y el límite de tiempo (5 minutos).  |

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

## Cuerpo de la Solicitud

El cuerpo de la solicitud de transacción difiere según la transacción que se inicie.

<!--
type: tab
titles: Ejemplo de Cuerpo de Solicitud
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

## Ver también

- [Access Token](?path=docs/spanish/referencia-api/accessToken.md)
- [Encriptación a Nivel de Mensaje](?path=docs/spanish/referencia-api/encriptacion.md)
- [Glosario API](?path=docs/spanish/referencia-api/glosario-api.md)
- [Manejo de Respuesta](?path=docs/spanish/referencia-api/manejo-respuesta.md)
- [Webhook](?path=docs/spanish/referencia-api/4-notificaciones.md)


---

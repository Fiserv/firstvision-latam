---
tags: [Referência da API, Cabeçalho de Pedidos, Corpo da Solicitação, Cabeçalho]
---

# Solicitação de API

## Cabeçalho da Solicitação

A API RESTful possui uma estrutura de cabeçalho consistente com base em um conjunto de parâmetros.

<!--
type: tab
titles: Cabeçalho, Exemplo de cabeçalho de solicitação
-->

Para criar o cabeçalho, forneça os seguintes valores:

| Variável              | Tipo      | Comprimento | Descrição/Valores                                                                                                                                                          |
|-----------------------|-----------|-------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `Content-Type`        |  *string* |   N/A       | Os tipos de conteúdo. Valor Válido: Aplicação/JSON                                                                                                                         |
| `apikey`              |  *string* |   N/A       | API Key fornecida ao comércio associando as solicitações ao aplicativo apropriado no Portal do desenvolvedor.                                                              |
| `Signature`           |  *string* |   N/A       | Assinatura HMAC usada para verificar a autenticidade e integridade dos dados transmitidos.                                                                                 |
| `X-ClientID`          |  *string* |   N/A       | Identificador do cliente.                                                                                                                                                  |
| `Authorization`       |  *string* |   N/A       | Token de Portador de Autorização.                                                                                                                                          |
| `X-Client-Request-Id` |  *string* |   40        | Um ID gerado pelo cliente para rastreamento de solicitação e criação de assinatura, exclusivo por solicitação.                                                             |
| `Timestamp`           | *integer* |   N/A       | O registro de data Epoch em milissegundos na solicitação de um sistema do cliente. É utilizado para geração de assinaturas de mensagens e limitação de tempo (5 minutos).  |

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

## Corpo da Solicitação

O corpo da solicitação de transação difere dependendo da transação que está sendo iniciada.

<!--
type: tab
titles: Exemplo de corpo de solicitação
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

## Veja também

- [Access Token](?path=docs/português/referência-api/accessToken.md)
- [Criptografia ao Nível de Mensagem](?path=docs/português/referência-api/criptografia.md)
- [Gestão de Resposta ](?path=docs/português/referência-api/gestão-resposta.md)
- [Glossário API](?path=docs/português/referência-api/glossário-api.md)
- [Webhook](?path=docs/português/referência-api/5-notificações.md)

---

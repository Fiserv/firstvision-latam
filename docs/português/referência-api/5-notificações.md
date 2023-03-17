---
tags: [Referência da API, Notificações, Webhooks, Eventos]
---

# Notificações

As notificações do First Vision permitem que fintechs e instituições financeiras recebam eventos como autorizações, alterações de endereço, bloqueios de cartões, ativação de cartões, substituições ou reemissões de cartões, datas de vencimento de pagamentos e alterações de limite.

A flexibilidade para definir novos eventos no futuro com alterações mínimas no sistema também está disponível.

<!--
type: tab
titles: Para quem é ?, Como se usa?, Usos potenciais
-->

Qualquer desenvolvedor que crie ou integre aplicativos que precisem interagir com dados de transações mantidos em plataformas de processamento de contas principal da Fiserv.

<!--
type: tab
-->

Use essas APIs para desenvolver aplicativos que oferecem experiências únicas ou novos canais por meio dos quais os usuários podem visualizar e gerenciar transações nessas contas.

<!--
type: tab
-->

Aplicativos que permitem que consumidores e empresas monitorem e gerenciem suas transações financeiras e saldos por meio dos canais que acessam no dia a dia.

<!-- type: tab-end -->

## Webhooks

Os webhooks são uma forma de os sistemas enviarem notificações em tempo real sobre eventos ocorridos. Eles funcionam permitindo que um Cliente forneça um serviço que pode receber notificações sempre que determinados eventos ocorrerem nos sistemas da Fiserv. Com os webhooks, os aplicativos podem se manter atualizados sobre coisas como alterações de autorização, atualizações de cartão ou conta e alertas de fraude.

Para usar webhooks, o FirstVision pode enviar uma solicitação HTTP POST para um endpoint designado sempre que ocorrer um evento. Isso envia uma notificação para o aplicativo receptor, que pode executar a ação necessária em resposta. Os webhooks fornecem uma maneira rápida e eficiente para diferentes sistemas se comunicarem e se manterem informados sobre eventos importantes.

![image](https://user-images.githubusercontent.com/111396588/209873236-86eb54b6-f214-4f8f-9652-51c03ad8d604.png)

### Webhooks Events

| Número do Evento | Descrição                                                                     |
|------------------|-------------------------------------------------------------------------------|
| 01               | Evento de autorização (aprovado e rejeitado)                                  |
| 02               | Gatilho de prazo de pagamento                                                 |
| 03               | Evento de Geração de Ciclo de Conta CMS                                       |
| 04               | Evento de crédito disponível                                                  |
| 05               | Evento de postagem de pagamento                                               |
| 06               | Mudança de endereço                                                           |
| 07               | Bloqueamento de Cartões (Rejeitar Ação/Coletar Autorização Apenas)            |
| 08               | Ativação do cartão                                                            |
| 09               | Embossing de Cartões                                                          |
| 10               | Alteração do Prazo de Pagamento                                               |
| 11               | Mudança de limite de crédito                                                  |
| 12               | Ativação de evento Falcon durante a autorização e bloqueios a nível de cartão |

### Exemplos de Webhook

---

<!--
type: tab
titles: •	Autorização aprovada, •	Autorização recusada, •	Pagamento devido
-->

```json
{
  "securityContext": "VMX.MULTICHANNEL.769",
  "version": "R8V1",
  "description": "APPROVED",
  "eventCode": "0001",
  "eventTitle": "AUTH ALERTS",
  "eventNumber": 1,
  "organizationNumber": 769,
  "accountNumber": "7651500XXXX222557",
  "customerNumber": "09765000XXX0000162",
  "mobilePhone": "",
  "emailAddress": "",
  "channelType": "BOTH",
  "messageLine1": "TH 015 ",
  "messageLine2": "TTTT012345ABCDEF02",
  "messageLine3": "5500550095",
  "messageLine4": "mail@epXXfint",
  "messageLine5": "000",
  "messageLine6": "00054020XXXXX64795",
  "messageLine7": "00000000011.00",
  "messageLine8": "TEST MERCHANT",
  "messageLine9": "20220113",
  "messageLine10": "100809",
  "messageLine11": "MXN",
  "messageLine12": "01765999999998 2013572895880110A00000000000000000000",
  "messageLine13": "0120484MEXICO 0",
  "messageLine14": "06011 0000000000000748321",
  "messageLine15": ".0",
  "messageLine16": "",
  "messageLine17": "",
  "messageLine18": "",
  "messageLine19": "",
  "messageLine20": "",
  "messageLine21": ""
}
```

<!--
type: tab
-->

```json
{
  "securityContext": "VMX.MULTICHANNEL.769",
  "version": "R8V1",
  "description": "DECLINED-UNMATCHEDEXPDTE-KEYED",
  "eventCode": "0001",
  "eventTitle": "AUTH ALERTS",
  "eventNumber": 1,
  "organizationNumber": 769,
  "accountNumber": "7651500XXXX222557",
  "customerNumber": "09765000XXX0000162",
  "mobilePhone": "",
  "emailAddress": "",
  "channelType": "BOTH",
  "messageLine1": "TH 015",
  "messageLine2": "TTTT012345ABCDEF02",
  "messageLine3": "5500550095",
  "messageLine4": "mail@epXXfint",
  "messageLine5": "000",
  "messageLine6": "00054020XXXXX64795",
  "messageLine7": "00000000011.00",
  "messageLine8": "TEST MERCHANT",
  "messageLine9": "20220113",
  "messageLine10": "100809",
  "messageLine11": "MXN",
  "messageLine12": "01765999999998 2013572895880110A00000000000000000000",
  "messageLine13": "0120484MEXICO 0",
  "messageLine14": "06011 0000000000000748321",
  "messageLine15": ".0",
  "messageLine16": "",
  "messageLine17": "",
  "messageLine18": "",
  "messageLine19": "",
  "messageLine20": "",
  "messageLine21": ""
}
```

<!--
type: tab
-->

```json
{
  "securityContext": "VMX.MULTICHANNEL.770",
  "version": "R8V1",
  "description": "",
  "eventCode": "0002",
  "eventTitle": "PAYMENT DUE DATE ALERT",
  "eventNumber": 2,
  "organizationNumber": 770,
  "accountNumber": "7651500XXXX222557",
  "customerNumber": "09765000XXX0000162",
  "mobilePhone": "",
  "emailAddress": "",
  "channelType": "BOTH",
  "messageLine1": "TH 015",
  "messageLine2": "TTTT012345ABCDEF02",
  "messageLine3": "5500550095",
  "messageLine4": "mail@epXXfint",
  "messageLine5": "",
  "messageLine6": "",
  "messageLine7": "",
  "messageLine8": "",
  "messageLine9": "20220113",
  "messageLine10": "100809",
  "messageLine11": "",
  "messageLine12": "",
  "messageLine13": "",
  "messageLine14": "",
  "messageLine15": "",
  "messageLine16": "",
  "messageLine17": "",
  "messageLine18": "",
  "messageLine19": "",
  "messageLine20": "",
  "messageLine21": ""
}
```

<!-- type: tab-end -->

---

<!--
type: tab
titles: Bloqueamento de cartão, •	Ativação do cartão, Mudança de endereço
-->

```json
{
  "securityContext": "VMX.MULTICHANNEL.770",
  "version": "R8V1",
  "description": "",
  "eventCode": "0007",
  "eventTitle": "BLOCK CODE ALERT",
  "eventNumber": 7,
  "organizationNumber": 770,
  "accountNumber": "7651500XXXX222557",
  "customerNumber": "09765000XXX0000162",
  "mobilePhone": "",
  "emailAddress": "",
  "channelType": "BOTH",
  "messageLine1": "TH 015",
  "messageLine2": "TTTT012345ABCDEF02",
  "messageLine3": "5500550095",
  "messageLine4": "mail@epXXfint",
  "messageLine5": "",
  "messageLine6": "",
  "messageLine7": "",
  "messageLine8": "N",
  "messageLine9": "20220113",
  "messageLine10": "100809",
  "messageLine11": "",
  "messageLine12": "",
  "messageLine13": "",
  "messageLine14": "",
  "messageLine15": "",
  "messageLine16": "",
  "messageLine17": "",
  "messageLine18": "",
  "messageLine19": "",
  "messageLine20": "",
  "messageLine21": ""
}
```

<!--
type: tab
-->

```json
{
  "securityContext": "VMX.MULTICHANNEL.770",
  "version": "R8V1",
  "description": "",
  "eventCode": "0008",
  "eventTitle": "CARD ACTIVATION ALERT",
  "eventNumber": 8,
  "organizationNumber": 770,
  "accountNumber": "7651500XXXX222557",
  "customerNumber": "09765000XXX0000162",
  "mobilePhone": "",
  "emailAddress": "",
  "channelType": "BOTH",
  "messageLine1": "TH 015",
  "messageLine2": "TTTT012345ABCDEF02",
  "messageLine3": "5500550095",
  "messageLine4": "mail@epXXfint",
  "messageLine5": "",
  "messageLine6": "",
  "messageLine7": "",
  "messageLine8": "N",
  "messageLine9": "20220113",
  "messageLine10": "100809",
  "messageLine11": "",
  "messageLine12": "",
  "messageLine13": "",
  "messageLine14": "",
  "messageLine15": "",
  "messageLine16": "",
  "messageLine17": "",
  "messageLine18": "",
  "messageLine19": "",
  "messageLine20": "",
  "messageLine21": ""
}
```

<!--
type: tab
-->

```json
{
  "securityContext": "VMX.MULTICHANNEL.771",
  "version": "R8V1",
  "description": "",
  "eventCode": "0006",
  "eventTitle": "CHANGE ADDRESS ALERT",
  "eventNumber": 6,
  "organizationNumber": 771,
  "accountNumber": "",
  "customerNumber": "09765000XXX0000162",
  "mobilePhone": "",
  "emailAddress": "",
  "channelType": "BOTH",
  "messageLine1": "TH 015",
  "messageLine2": "TTTT012345ABCDEF02",
  "messageLine3": "5500550095",
  "messageLine4": "mail@epXXfint",
  "messageLine5": "",
  "messageLine6": "",
  "messageLine7": "",
  "messageLine8": "",
  "messageLine9": "20220113",
  "messageLine10": "100809",
  "messageLine11": "",
  "messageLine12": "",
  "messageLine13": "",
  "messageLine14": "",
  "messageLine15": "",
  "messageLine16": "",
  "messageLine17": "",
  "messageLine18": "",
  "messageLine19": "",
  "messageLine20": "",
  "messageLine21": ""
}
```


---

## Veja também

- [Cartões](?path=docs/português/referência-api/1-cartões.md)
- [Cliente](?path=docs/português/referência-api/2-cliente.md)
- [Conta](?path=docs/português/referência-api/3-conta.md)
- [Fidelidade](?path=docs/português/referência-api/4-fidelidade.md)
- [Transações](?path=docs/português/referência-api/6-transações.md)

---

---
tags: [Referencia de la API, Notificationes, Webhooks, Eventos]
---

# Notificaciones

Las notificaciones de First Vision les permite a las empresas de tecnología financiera y a las instituciones financieras recibir eventos como autorizaciones, cambios de dirección, bloqueos de tarjeta, activación de tarjetas, reemplazos o reemisiones de tarjetas, fechas de vencimiento de pagos y cambios de Límite de Crédito.

También está disponible la flexibilidad para definir nuevos eventos/SMS en el futuro con cambios mínimos en el sistema.

<!--
type: tab
titles: ¿Para quién es?, ¿Cómo se usa?, Usos potenciales
-->

Cualquier desarrollador que cree o integre aplicaciones que necesiten interactuar con datos de transacciones mantenidos en plataformas de procesamiento de cuentas centrales de Fiserv.

<!--
type: tab
-->

Utilice estas API para desarrollar aplicaciones que ofrezcan experiencias únicas o canales novedosos a través de los cuales los usuarios puedan ver y administrar transacciones en esas cuentas.

<!--
type: tab
-->

Aplicaciones que permiten a los consumidores y las empresas monitorear y administrar sus transacciones y saldos financieros a través de los canales a los que acceden en la vida cotidiana.

<!-- type: tab-end -->

## Webhooks

Los webhooks son una forma en que los sistemas envían notificaciones en tiempo real sobre eventos que han ocurrido. Funcionan al permitir que un Cliente brinde un servicio que puede recibir notificaciones cada vez que ocurren ciertos eventos en los sistemas de Fiserv. Con los webhooks, las aplicaciones se pueden mantener actualizadas sobre cosas como cambios de autorización, actualizaciones de tarjetas o cuentas y alertas de fraude.

Para usar webhooks, FirstVision puede enviar una solicitud HTTP POST a un punto final designado siempre que ocurra un evento. Esto envía una notificación a la aplicación receptora, que luego puede tomar las medidas necesarias en respuesta. Los webhooks proporcionan una forma rápida y eficiente para que los diferentes sistemas se comuniquen y se mantengan informados sobre eventos importantes.

![image](https://user-images.githubusercontent.com/111396588/209873236-86eb54b6-f214-4f8f-9652-51c03ad8d604.png)

### Webhooks Events

| Numero de Evento | Descripción                                                                        |
|------------------|------------------------------------------------------------------------------------|
| 01               | Evento de Autorización (aprobado y rechazado)                                      |
| 02               | Disparador de Fecha Límite de Pago                                                 |
| 03               | Evento de Generación de Ciclos de la Cuenta CMS                                    |
| 04               | Evento de Crédito Disponible                                                       |
| 05               | Evento de Pago Posteado                                                            |
| 06               | Cambio de Dirección                                                                |
| 07               | Bloqueos de tarjetas (Solo acción de Rechazada / Recoger Autorización)             |
| 08               | Activación de Tarjetas                                                             |
| 09               | Embozado de Tarjetas                                                               |
| 10               | Cambio de Fecha Límite de Pago                                                     |
| 11               | Cambio de cupo                                                                     |
| 12               | Disparador de Evento de Falcon durante autorización y bloqueos de nivel de tarjeta |

### Ejemplos de Webhooks

---

<!--
type: tab
titles: Autorización aprobada, Autorización rechazada, Fecha de Pago
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
titles: Bloqueo de Tarjeta, Activación de Tarjetas, Cambio de Dirección
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

<!-- type: tab-end -->

---

## Ver también

- [Clientes](?path=docs/spanish/referencia-api/1-clientes.md)
- [Cuentas](?path=docs/spanish/referencia-api/2-cuentas.md)
- [Lealtad](?path=docs/spanish/referencia-api/3-lealtad.md)
- [Tarjetas](?path=docs/spanish/referencia-api/5-tarjetas.md)
- [Transacciones](?path=docs/spanish/referencia-api/6-transacciones.md)

---

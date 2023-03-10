---
tags: [Casos Principales, Controles de Tarjeta, Tarjetas, Embozador, Bloquear, Desbloquear, Límites, Viajes, Transferir, Activar, PIN]
---

# Controles de Tarjetas

En esta sección se describen las diferentes APIs del Portal que se utilizan para tomar acciones sobre las diferentes actividades relacionadas con el uso de la tarjeta de crédito, débito, tarjeta prepago o monedero, para cualquiera de los productos Visa, MasterCard o American Express. A continuación, una descripción de las funcionalidades y características de la API.

Como requisito principal, es importante que las tarjetas de crédito, tarjetas de débito, tarjetas prepago o monederos digitales hayan sido creados en el ambiente de prueba como se detalló en este documento, utilizando las APIs para la Creación de Clientes (Client/Add), Creación de Cuentas (Account/Add) y Creación de Tarjetas (Embosser/Add).

## Bloquear o Desbloquear Tarjeta (Cards/Embosser/Block)

A través de esta API, el tarjetahabiente podrá realizar bloqueos preventivos y definitivos sobre la información de su tarjeta de crédito, tarjeta de débito, tarjeta prepago y monedero. Con el fin de prevenir cualquier posible fraude cuando el tarjetahabiente sospeche que la información de la tarjeta puede estar comprometida.

De igual forma, el tarjetahabiente podrá realizar un desbloqueo preventivo de su tarjeta cuando esté seguro de que la información de su tarjeta no está comprometida.

La información requerida por la API, como el número de tarjeta, el código de bloqueo y la función, debe incluirse antes de la activación de la API.

**PUT** `/cards/embosser/block`

La descripción de cada campo de la API se encuentra dentro de las especificaciones definidas en el portal.

## Update Spending Limits (Cards/Spend-Limits)

This API allows the customer to update online, the different spending limits associated with credit, debit, prepaid and Wallet cards. These spending limits are assigned for purchases, cash advances, internet purchases and international purchases. Spending limits assign the number of transactions and maximum amounts allowed for use on a daily, weekly, biweekly, and monthly basis.These spending limits can be assigned to the main card as well as to additional cards.

The values are modified 100% online and can be adjusted as many times as required.

The API Card/Spend-Limits, requests as required information, the card number, transaction number and amounts for each spending limit.

**PUT** `/cards/spend-limits-L8V3`

La descripción de cada campo de la API se encuentra dentro de las especificaciones definidas en el portal.

## Update Travel Indicator (Cards/Travel)

Through the API Card/Travel, the cardholder will be able to define the destinations, outside their country, where the credit card will be used. This API activates online the dates and countries to which the cardholder is traveling in the coming months.

In the event that the card is used in a country or date range that has not been defined by this API, the authorization request will be rejected with the response: “Transaction not allowed”.

This API allows the cardholder define the range of dates and countries where the card will be used, it also allows him to modify and delete countries and dates already defined.

The values required by the API are the card number, ISO code of the country, start and end date range, allowing up to a maximum of five countries to visit with their respective date ranges

**PUT** `/cards/travel`

La descripción de cada campo de la API se encuentra dentro de las especificaciones definidas en el portal.

## Card Transfer Update (Cards/Transfer)

This API allow the cardholder blocks their current card number and request a new card with different card number in only one trigger. Same that API Block or Unlock Card, card number can be blocked just in case cardholder believes that card information is compromise and at same time he can request a new card number, so new card will be embossed during batch process and will be ready to be deliver on next day.

As part of values requested by the API Cards/Transfer, is required the card number, account number, organization and effective date.

**PUT** `/cards/transfer`

La descripción de cada campo de la API se encuentra dentro de las especificaciones definidas en el portal.

## Active Card (Cards/Activation)

The API CARS/ACTIVATION activates a card already embossed. This API allow to the cardholder activate a new card number when it is received by mail or deliver in a bank branch. Card Activation date will be saved on test environment for audit reasons.

If cardholder try use the card for purchase or cash advance, before it is activate, the authorization request will be rejected with reject reason “Card is not Activate”, so cardholder will be able to active his card just triggering this API.

This API should be trigger each time that a new card is embossed (principal or additional), to activate each card embossed.

Require values for this API are: Card Number, bank product identification (organization) and service type (A= Activation).

**PUT** `/cards/activation`

La descripción de cada campo de la API se encuentra dentro de las especificaciones definidas en el portal.

## Update PIN of Card (Cards/PIN)

This API CARDS/PIN, allows to the cardholder reassign a new personal identification number (PIN). Normally used when new card is deliver to the cardholder and new PIN needs to be setup and linked to the new card already activated using the API Cards/Activation.

The API reassign and update the new PIN 100% on line so cardholder can use the new PIN after it was assigned. This API can be trigger from different channels as ATM, web pages, VCR, APP, etc. Cardholder will choose the new four digits PIN and along with credit card number and Key Association (used to encrypt the new API) the bank application should be able to calculate the new PIN Block to trigger the API.

The values required for this API are: Card Number, bank organization, channel, PIN Block and Key association.

**PUT** `/cards/pin/`

La descripción de cada campo de la API se encuentra dentro de las especificaciones definidas en el portal.

## PIN Block/Unblock (Cards/PIN/Status)

The API cards/pin/status is being used by a cardholder to block his current PIN number, it can be used when he believes that PIN information can be compromise. This API only block the PIN number and not the card number, so customer after trigger this API to block the PIN, he can still using the card for purchases but not for cash advances.

Using same API, cardholder is able the un-block a PIN number already blocked, just triggering the API with a different value on field Function Code.

Another function of this API, allow the cardholder unblock a card PIN when it was already blocked by exceed of PIN tries from ATM.

Values require by this API are: Card number, channel, bank organization and service function.

**PUT** `/cards/pin/status`

La descripción de cada campo de la API se encuentra dentro de las especificaciones definidas en el portal.

## Change the PIN of a Card (Cards/PIN/PIN-Change)

With this API cards/pin/pin-change, cardholder will be able to change his current PIN number, for another PIN number. At different of the API Update PIN of Card, this API will request the current PIN number assigned to the cardholder, so both values need to be added before trigger the API: Current PIN and New PIN.

This API can be used when cardholder need to change the current PIN number for another PIN number just in case that this information is compromise. This API can be trigger from ATRM, VCR, APP, Web Service etc and is 100% on line.

Require values of this API are: Card Number, Channel, Current PIN Block, New PIN Block, Key Association (to encrypt PIN Blocks), new PIN offset, and bank organization.

**PUT** `/cards/pin/pin-change`

La descripción de cada campo de la API se encuentra dentro de las especificaciones definidas en el portal.

---

## Ver también

- [Ambiente de API](?path=docs/spanish/casos-principales/ambiente-api.md)
- [Auditoría y Monitoreo](?path=docs/spanish/casos-principales/auditoria.md)
- [Cambio de PIN](?path=docs/spanish/casos-principales/cambio-pin.md)
- [Cargar Fondos](?path=docs/spanish/casos-principales/cargas.md.md)
- [CVV2 Dinámico](?path=docs/spanish/casos-principales/cvv-dinamico.md)
- [Emisión de Tarjetas Digitales](?path=docs/spanish/casos-principales/emision-tarjetas.md)
- [Entrada/Salida de Efectivo](?path=docs/spanish/casos-principales/entrada-salida-efectivo.md.md)
- [Gestión de Clientes](?path=docs/spanish/casos-principales/gestion-clientes.md)
- [Gestión de Cuentas](?path=docs/spanish/casos-principales/gestion-cuentas.md)
- [Gestión de Tarjetas](?path=docs/spanish/casos-principales/gestion-tarjetas.md)
- [HMAC Signature](?path=docs/spanish/casos-principales/hmac.md)
- [Integración con el sistema Falcon](?path=docs/spanish/casos-principales/integracion-falcon.md)
- [PAN Token](?path=docs/spanish/casos-principales/pan-token.md)
- [Registro de Tarjeta](?path=docs/spanish/casos-principales/registro.md)
- [Relación Cliente-Cuenta-Tarjeta](?path=docs/spanish/casos-principales/relacion.md)

---

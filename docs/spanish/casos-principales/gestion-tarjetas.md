---
tags: [Casos Principales, Gestión de Tarjetas, Tarjetas, Embozador, PAN Token, Códigos De Seguridad, PIN]
---

# Gestión de Tarjetas

## Agregar Registro de Tarjetas 

Use the API **CARDS/EMBOSSER** create a card information used to emboss a new card or plastic. This card information must have relate that an account number created through API **ACCOUNT/ADD** and this account number must be related a customer number created through API **CUSTOMER/ADD**.

This API allow add card information as card expiration date, service code, cardholder name, address to where the card will be deliver, spending limits, etc.

The card number is calculated on randomly way by the application, and this number will not generated again (duplicated).

**POST** `/cards/embosser/l8vf`

La descripción de cada campo de la API se encuentra dentro de las especificaciones definidas en el portal.

## Inquire Card or PAN token

Use this API **CARDS/EMBOSSER/CARD-PAN** to get the PAN-token calculated for a card number.

PAN token is a current functionality to tokenize the card number for all banks that are not a PCI certificate. When new card is created through API **CARD/EMBOSSER**, the PAN token is calculated automatically on base a parameters previously defined.

This API use the PAN-TOKEN to bring the card number or card number can be used to being the PAN-TOKEN.

**POST** `/cards/embosser/card-pan-l8v2`

The description of each API field can be found within the specifications in the portal.

## Add or Update Massive Cards

This API **CARDS/MASS-CARD-ISSUE**, allow the user add or update a request to emboss new cards on massive way. These cards can be credit, debit or prepay card. Quantity of card to emboss is a parameter request by the API.

Cards embossed will not have an embosser name, but card number, expiration and card security values will be part of these.

**POST** `/cards/mass-card-issue-L8V3`

La descripción de cada campo de la API se encuentra dentro de las especificaciones definidas en el portal.

## Card Action Update

Use this API **CARDS/EMBOSSER/CARDACTION** to update the action flag used to re-emboss (re-issue) a specific card number.

This API allow to the user request a card reissue for some reason, lost/stolen, damage, card expiration, emergency replace, etc.

**PUT** `/cards/embosser/cardAction-L8V2`

La descripción de cada campo de la API se encuentra dentro de las especificaciones definidas en el portal.

## Instant Card

This API **CARDS/INSNTANT-CARD-L8V7** allow to the user request the creation of account and card on instantly way. Card information will be ready to be use for purchases.

Customer information have to be created through API **CUSTOMER/ADD** before call API instant card.

**POST** `/account/v2/instantCard`

La descripción de cada campo de la API se encuentra dentro de las especificaciones definidas en el portal.

## Inquiry Security Values

This API **CARDS/PIN/SECURITY-CODES**, allow to the user get the card security values (CVV, CVV2,ICVV, PIN number) already emboss for an specific card number.

Security values provided by the API will be encrypted using a security key of 32 bytes, so user should use the same security key and 3Des algorithm to decrypt the security values.

**POST** `/cards/pin/security-codes`

La descripción de cada campo de la API se encuentra dentro de las especificaciones definidas en el portal.

## Inquire Dynamic CVV2/CVC2/4CSC

Use this API **CARDS/PIN/DYNAMIC-VALUE** to calculate and inquire a new CVV2 for not present card purchases.

Currently when card is emboss through the API **CARD/EMBOSSER**, the static CVV2 code is calculate and printed on sign panel on card back. The new functionality of Dynamic CVV2 allow to the cardholder call this API **CARDS/PIN/DYNAMIC-VALUE** to generate and calculate a new CVV2 before make a not present purchase. So when API is trigger the static CVV2 is inactivated and each time the cardholder wants to make a new not card present purchase the new CVV2 have to be calculated through this API.

**POST** `/cards/pin/dynamic-values`

La descripción de cada campo de la API se encuentra dentro de las especificaciones definidas en el portal.

## Inquire Number of Invalid PIN Attempts

This API **CARDS/PIN/INVALID-ATTEMPTS** allow to the cardholder get the number of invalid PIN attempts.

As part of security parameters, the number of invalid PIN attempts are set up to avoid that PIN number can be calculated for frauds proposals. When this parameter is reached the PIN number is block and a new PIN number have to be calculated.

Invalid PIN attempts can be reached by many reasons the most popular reason is when cardholder fails the PIN number on ATM.

**POST** `/cards/pin/invalid-attempts`

La descripción de cada campo de la API se encuentra dentro de las especificaciones definidas en el portal.

## PIN Validation

Use this API **CARDS/PIN/VALIDATION** to confirm that current PIN generated is correct.

This API require the PIN block and the card number and not the clear PIN number.

**POST** `/cards/pin/validation`

La descripción de cada campo de la API se encuentra dentro de las especificaciones definidas en el portal.

---

## Ver también

- [Ambiente de API](?path=docs/spanish/casos-principales/ambiente-api.md)
- [Auditoría y Monitoreo](?path=docs/spanish/casos-principales/auditoria.md)
- [Cambio de PIN](?path=docs/spanish/casos-principales/cambio-pin.md)
- [Cargar Fondos](?path=docs/spanish/casos-principales/cargas.md.md)
- [Controles de Tarjetas](?path=docs/spanish/casos-principales/controles-tarjeta.md)
- [CVV2 Dinámico](?path=docs/spanish/casos-principales/cvv-dinamico.md)
- [Emisión de Tarjetas Digitales](?path=docs/spanish/casos-principales/emision-tarjetas.md)
- [Entrada/Salida de Efectivo](?path=docs/spanish/casos-principales/entrada-salida-efectivo.md.md)
- [Gestión de Clientes](?path=docs/spanish/casos-principales/gestion-clientes.md)
- [Gestión de Cuentas](?path=docs/spanish/casos-principales/gestion-cuentas.md)
- [HMAC Signature](?path=docs/spanish/casos-principales/hmac.md)
- [Integración con el sistema Falcon](?path=docs/spanish/casos-principales/integracion-falcon.md)
- [PAN Token](?path=docs/spanish/casos-principales/pan-token.md)
- [Registro de Tarjeta](?path=docs/spanish/casos-principales/registro.md)
- [Relación Cliente-Cuenta-Tarjeta](?path=docs/spanish/casos-principales/relacion.md)

---

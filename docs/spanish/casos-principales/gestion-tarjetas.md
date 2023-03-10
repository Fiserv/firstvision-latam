---
tags: [Casos Principales, Gestión de Tarjetas, Tarjetas, Embozador, PAN Token, Códigos De Seguridad, PIN]
---

# Gestión de Tarjetas

## Agregar Registro de Tarjetas 

La API **CARDS/EMBOSSER** permite crear información de tarjeta utilizada para grabar una tarjeta o plástico nuevos en relieve. Esta información de la tarjeta debe tener relación con un número de cuenta creado a través de API **ACCOUNT/ADD** y este número de cuenta debe estar relacionado con un número de cliente creado a través de API **CUSTOMER/ADD**.

Esta API permite agregar información de la tarjeta como la fecha de vencimiento de la tarjeta, el código de servicio, el nombre del tarjetahabiente, la dirección donde se entregará la tarjeta, los límites para compras, etc.

El número de tarjeta se calcula de forma aleatoria por la aplicación, y este número no se generará de nuevo (duplicado).

**POST** `/cards/embosser/l8vf`

La descripción de cada campo de la API se encuentra dentro de las especificaciones definidas en el portal.

## Consultar Tarjeta o PAN Token

Usa esta API **CARDS/EMBOSSER/CARD-PAN** para obtener el pan-token calculado para un número de tarjeta.

El PAN Token es una funcionalidad actual para tokenizar el número de tarjeta para todos los bancos que no poseen un certificado PCI. Cuando se crea una nueva tarjeta a través de la API **CARD/EMBOSSER**, el PAN Token se calcula automáticamente en base a un parámetro previamente definido.

Esta API usa el PAN-TOKEN para traer el número de tarjeta o bien el número de tarjeta se puede usar para el PAN-TOKEN.

**POST** `/cards/embosser/card-pan-l8v2`

La descripción de cada campo de la API se encuentra dentro de las especificaciones definidas en el portal.

## Agregar o Actualizar Tarjetas Masivas 

Esta API **CARDS/MASS-CARD-ISSUE**, permite al usuario agregar o actualizar una solicitud para grabar nuevas tarjetas de forma masiva. Estas tarjetas pueden ser de crédito, débito o prepago. La cantidad de tarjetas que serán embozadas es un parámetro solicitado por la API.

Las tarjetas embozadas no tendrán un nombre de embozador, pero el número de tarjeta, la fecha de expiración y los valores de seguridad de la tarjeta serán parte de ellos.

**POST** `/cards/mass-card-issue-L8V3`

La descripción de cada campo de la API se encuentra dentro de las especificaciones definidas en el portal.

## Actualización de la Acción de la Tarjeta 

Use esta API **CARDS/EMBOSSER/CARDACTION** para actualizar la bandera de acción utilizada para volver a grabar (reemitir) un número de tarjeta específico.

Esta API le permite al usuario solicitar la reemisión de una tarjeta por algún motivo como pérdida/robo, daño, expiración de la tarjeta, reemplazo de emergencia, etc.

**PUT** `/cards/embosser/cardAction-L8V2`

La descripción de cada campo de la API se encuentra dentro de las especificaciones definidas en el portal.

## Tarjeta Instantánea 

Esta API **CARDS/INSTANT-CARD** le permite al usuario solicitar la creación de cuenta y tarjeta de forma instantánea. La información de la tarjeta estará lista para ser utilizada para compras.

La información del cliente debe ser creada por medio de la API **CUSTOMER/ADD** antes de llamar a la API de tarjeta instantánea.

**POST** `/account/v2/instantCard`

La descripción de cada campo de la API se encuentra dentro de las especificaciones definidas en el portal.

## Consulta de Valores de Seguridad 

Esta API **CARDS/PIN/SECURITY-CODES**, le permite al usuario obtener los valores de seguridad de la tarjeta (CVV, CVV2,ICVV, número PIN) ya grabados en relieve para un número de tarjeta específico.

Los valores de seguridad proporcionados por la API se cifrarán mediante una clave de seguridad de 32 bytes, por lo que el usuario debe utilizar la misma clave de seguridad y el algoritmo 3Des para descifrar los valores de seguridad.

**POST** `/cards/pin/security-codes`

La descripción de cada campo de la API se encuentra dentro de las especificaciones definidas en el portal.

## Consultar Valores CVV2/CVC2/4CSC Dinámicos

Use esta API **CARDS/PIN/DYNAMIC-VALUE** para calcular y consultar un nuevo CVV2 para compras con tarjeta no presente.

Actualmente, cuando la tarjeta se graba en relieve a través de API **CARD/EMBOSSER**, el código CVV2 estático se calcula y se imprime en el panel de firma en el reverso de la tarjeta. La nueva funcionalidad de Dynamic CVV2 le permite al tarjetahabiente llamar a esta API **CARDS/PIN/DYNAMIC-VALUE** para generar y calcular un nuevo CVV2 antes de realizar una compra no presente. Por lo tanto, cuando se activa la API, el CVV2 estático se desactiva y cada vez que el tarjetahabiente desea realizar una nueva compra sin tarjeta presente, se deberá calcular el CVV2 nuevo por medio de esta API.

**POST** `/cards/pin/dynamic-values`

La descripción de cada campo de la API se encuentra dentro de las especificaciones definidas en el portal.

## Consultar Número de Intentos de PIN No Válidos 

Esta API **CARDS/PIN/INVALID-ATTEMPTS** permite al tarjetahabiente obtener el número de intentos de PIN no válidos.

Como parte de los parámetros de seguridad, se configura el número de intentos de PIN no válidos para evitar que se pueda calcular el número de PIN para propuestas de fraude. Cuando se alcanza este parámetro, el número PIN se bloquea y se debe calcular un nuevo número PIN.

Los intentos de PIN no válidos pueden ocurrir por muchas razones. La razón más popular es cuando el tarjetahabiente comete un error al ingresar el número de PIN en el cajero automático.

**POST** `/cards/pin/invalid-attempts`

La descripción de cada campo de la API se encuentra dentro de las especificaciones definidas en el portal.

## Validación PIN

Use esta API **CARDS/PIN/VALIDATION** para confirmar que el PIN generado sea correcto.

Esta API requiere el PIN Block y el número de tarjeta y no el PIN en claro.

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

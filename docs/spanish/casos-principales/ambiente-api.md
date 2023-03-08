---
tags: [Casos Principales, Ambiente de Pruebas de la API, API Key]
---

# Ambiente de Pruebas de la API

## Descripción General

El ambiente de pruebas de la API permite que clientes nuevos y prospectos utilicen más de 150 APIs diferentes que se encuentran implementadas actualmente en el Portal.

Todas estas APIs acceden a un ambiente de prueba, actualmente creado para la solución FirstVision. Este ambiente se ha implementado para permitir que los clientes nuevos, prospectos y desarrolladores tengan una mejor comprensión de la funcionalidad, el diseño y la implementación del uso de la API.

El ambiente de prueba de FirstVision permite tener diferentes escenarios para productos Visa, MasterCard y AMEX, como tarjetas de crédito, tarjetas de débito, tarjetas prepago y múltiples monederos digitales.

Cada uno de estos escenarios de validación fueron creados para las regiones de Colombia, Panamá, México, Argentina, Uruguay y Brasil, lo que les permite a los clientes de cada una de estas regiones tener una visión más real y precisa de cómo funcionarán sus productos una vez que se hayan implementado en el ambiente de Producción.

Con el uso de una clave conocida como API-KEY, la cual puede ser solicitada por el Cliente, cada API's puede ser direccionada para probar la franquicia, el producto y la región que se desee.

## Ejemplo de solicitud

**POST** `/token`

Ejemplo de respuesta:

```json
{
    "token_type": "BearerToken",
    "issued_at": "11111111111111",
    "client_id": "ABC123ABC123ABC123",
    "access_token": "ABC123abc123ABC123abc123",
    "expires_in": "1799",
    "status": "approved"
}
```

## Diagrama

![Diagram!](/assets/images/main-cases/api-test-environment_1.png "Diagram")

---

## Ver también

- [Auditoría y Monitoreo](?path=docs/spanish/casos-principales/auditoria.md)
- [Cambio de PIN](?path=docs/spanish/casos-principales/cambio-pin.md)
- [Cargar Fondos](?path=docs/spanish/casos-principales/cargas.md.md)
- [Controles de Tarjetas](?path=docs/spanish/casos-principales/controles-tarjeta.md)
- [CVV2 Dinámico](?path=docs/spanish/casos-principales/cvv-dinamico.md)
- [Emisión de Tarjetas Digitales](?path=docs/spanish/casos-principales/emision-tarjetas.md)
- [Entrada/Salida de Efectivo](?path=docs/spanish/casos-principales/entrada-salida-efectivo.md.md)
- [Gestión de Clientes(?path=docs/spanish/casos-principales/gestion-clientes.md)
- [Gestión de Cuentas](?path=docs/spanish/casos-principales/gestion-cuentas.md)
- [Gestión de Tarjetas](?path=docs/spanish/casos-principales/gestion-tarjetas.md)
- [HMAC Signature](?path=docs/spanish/casos-principales/hmac.md)
- [Integración con el sistema Falcon](?path=docs/spanish/casos-principales/integracion-falcon.md)
- [PAN Token](?path=docs/spanish/casos-principales/pan-token.md)
- [Registro de Tarjeta](?path=docs/spanish/casos-principales/registro.md)
- [Relación Cliente-Cuenta-Tarjeta](?path=docs/spanish/casos-principales/relacion.md)

---

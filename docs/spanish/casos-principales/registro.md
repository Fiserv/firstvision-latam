---
tags: [Main Cases, Card Record, cards, embosser]
---

# Agregar Registro de Tarjetas

Esta API permite crear información de tarjeta utilizada para grabar una tarjeta o plástico nuevos en relieve. Esta información de la tarjeta debe tener relación con un número de cuenta creado a través de API **Account Add** y este número de cuenta debe estar relacionado con un número de cliente creado a través de API **Customer Add**.

Esta API permite agregar información de la tarjeta como la fecha de vencimiento de la tarjeta, el código de servicio, el nombre del tarjetahabiente, la dirección donde se entregará la tarjeta, los límites para compras, etc.

El número de tarjeta se calcula de forma aleatoria por la aplicación, y este número no se generará de nuevo (duplicado).

**POST** `/cards/embosser/l8vf`

La descripción de cada campo de la API se encuentra dentro de las especificaciones definidas en el portal.

---

## Ver también

- [Ambiente de API](?path=docs/spanish/casos-principales/ambiente-api.md)
- [Auditoría y Monitoreo](?path=docs/spanish/casos-principales/auditoria.md)
- [Cambio de PIN](?path=docs/spanish/casos-principales/cambio-pin.md)
- [Cargar Fondos](?path=docs/spanish/casos-principales/cargas.md)
- [Controles de Tarjetas](?path=docs/spanish/casos-principales/controles-tarjeta.md)
- [CVV2 Dinámico](?path=docs/spanish/casos-principales/cvv-dinamico.md)
- [Emisión de Tarjetas Digitales](?path=docs/spanish/casos-principales/emision-tarjetas.md)
- [Entrada/Salida de Efectivo](?path=docs/spanish/casos-principales/entrada-salida-efectivo.md)
- [Gestión de Clientes](?path=docs/spanish/casos-principales/gestion-clientes.md)
- [Gestión de Cuentas](?path=docs/spanish/casos-principales/gestion-cuentas.md)
- [Gestión de Tarjetas](?path=docs/spanish/casos-principales/gestion-tarjetas.md)
- [HMAC Signature](?path=docs/spanish/casos-principales/hmac.md)
- [Integración con el Sistema Falcon](?path=docs/spanish/casos-principales/integracion-falcon.md)
- [PAN Token](?path=docs/spanish/casos-principales/pan-token.md)
- [Relación Cliente-Cuenta-Tarjeta](?path=docs/spanish/casos-principales/relacion.md)

---

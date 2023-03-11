---
tags: [Casos Principales, CVV 2 Dinámico, Tarjetas, PIN, Valores Dinámicos]
---

# Solicitud de valores dinámicos

Esta API permite calcular y consultar un nuevo CVV2 para compras con tarjeta no presente.

Actualmente, cuando la tarjeta se graba en relieve a través de API **Card Embosser**, el código CVV2 estático se calcula y se imprime en el panel de firma en el reverso de la tarjeta. La nueva funcionalidad de Dynamic CVV2 le permite al tarjetahabiente llamar a esta API para generar y calcular un nuevo CVV2 antes de realizar una compra no presente. Por lo tanto, cuando se activa la API, el CVV2 estático se desactiva y cada vez que el tarjetahabiente desea realizar una nueva compra sin tarjeta presente, se deberá calcular el CVV2 nuevo por medio de esta API.

**POST** `/cards/pin/dynamic-values`

La descripción de cada campo de la API se encuentra dentro de las especificaciones definidas en el portal.

---

## Ver también

- [Ambiente de API](?path=docs/spanish/casos-principales/ambiente-api.md)
- [Auditoría y Monitoreo](?path=docs/spanish/casos-principales/auditoria.md)
- [Cambio de PIN](?path=docs/spanish/casos-principales/cambio-pin.md)
- [Cargar Fondos](?path=docs/spanish/casos-principales/cargas.md)
- [Controles de Tarjetas](?path=docs/spanish/casos-principales/controles-tarjeta.md)
- [Emisión de Tarjetas Digitales](?path=docs/spanish/casos-principales/emision-tarjetas.md)
- [Entrada/Salida de Efectivo](?path=docs/spanish/casos-principales/entrada-salida-efectivo.md)
- [Gestión de Clientes](?path=docs/spanish/casos-principales/gestion-clientes.md)
- [Gestión de Cuentas](?path=docs/spanish/casos-principales/gestion-cuentas.md)
- [Gestión de Tarjetas](?path=docs/spanish/casos-principales/gestion-tarjetas.md)
- [HMAC Signature](?path=docs/spanish/casos-principales/hmac.md)
- [Integración con el sistema Falcon](?path=docs/spanish/casos-principales/integracion-falcon.md)
- [PAN Token](?path=docs/spanish/casos-principales/pan-token.md)
- [Registro de Tarjeta](?path=docs/spanish/casos-principales/registro.md)
- [Relación Cliente-Cuenta-Tarjeta](?path=docs/spanish/casos-principales/relacion.md)

---

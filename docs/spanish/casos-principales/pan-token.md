---
tags: [Casos Principales, Registro de Tarjetas, Tarjetas, Embozador]
---

# PAN Token

Actualmente, cuando un Cliente no está certificado por la Industria de Tarjetas de Pago (PCI), el número de tarjeta no se puede mostrar en ningún servicio web, cajero automático, POS, etc.

Para mantener seguro este valor de seguridad, se requiere utilizar un PAN-TOKEN en lugar de un número de tarjeta. Por lo tanto, cuando se crea un número de tarjeta, la funcionalidad actual genera el PAN-TOKEN en lugar del número de tarjeta.

El PAN-TOKEN se calcula automáticamente mediante una CLAVE de seguridad y puede tener valores numéricos y alfanuméricos.

El PAN-TOKEN se puede mostrar en un servicio web, cajero automático, POS o cualquier otro dispositivo o servicio sin comprometer el número real de la tarjeta.

PAN Token, puede ser visible usando esta API, por lo que el usuario de la API puede obtener el número de PAN-TOKEN enviando el número de tarjeta en el mensaje de datos de entrada de la API o puede obtener el número de tarjeta simplemente enviando el número de PAN-TOKEN.

**POST** `/cards/embosser/card-pan-l8v2`

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
- [Gestión de Tarjetas](?path=docs/spanish/casos-principales/gestion-tarjetas.md)
- [HMAC Signature](?path=docs/spanish/casos-principales/hmac.md)
- [Integración con el sistema Falcon](?path=docs/spanish/casos-principales/integracion-falcon.md)
- [Registro de Tarjeta](?path=docs/spanish/casos-principales/registro.md)
- [Relación Cliente-Cuenta-Tarjeta](?path=docs/spanish/casos-principales/relacion.md)

---

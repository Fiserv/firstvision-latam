---
tags: [Casos Principales, Cambio de PIN, Tarjetas]
---

# Cambio de PIN

El cambio de PIN es una funcionalidad actual para permitir que el tarjetahabiente cambie el PIN de su tarjeta actual. El motivo para cambiar el PIN de la tarjeta puede ser porque el PIN se vió comprometido, el tarjetahabiente desea realizar el cambio o el emisor así lo requiere después de un cierto número de días.

Con esta API **cards/pin/pin-change**, el tarjetahabiente podrá cambiar su número PIN actual por otro número PIN. A diferencia de la API de actualización del PIN de la tarjeta, esta API solicitará el número de PIN actual asignado al tarjetahabiente, por lo que ambos valores deben ser agregados antes de activar la API: PIN Actual y PIN Nuevo.

Esta API se puede utilizar cuando el tarjetahabiente necesite cambiar el número PIN actual por otro número PIN en caso de que esta información se vea comprometida. Esta API se puede activar desde ATRM, VCR, APP, Servicio Web, etc. y está 100 % en línea.

Los valores requeridos para esta API son el número de tarjeta, el canal, el PIN Block actual, el PIN Block nuevo, la asociación de claves (para cifrar los bloqueos de PIN), el PIN Offset nuevo y la organización bancaria.

**PUT** `/cards/pin/pin-change`
    
Cuerpo de la Solicitud:

```json
{
  "cardNumber": "{{cardNumber}}",
  "channel": "W",
  "currPinBlock": "123ABC123ABC123",
  "keyAssociationNumber": "AV",
  "organizationNumber": {{orgid}},
  "pinOffset": "",
  "reqdPinBlock": "123ABC123A"
}
```

La descripción de cada campo de la API se encuentra dentro de las especificaciones definidas en el portal.

---

## Ver también

- [Ambiente de API](?path=docs/spanish/casos-principales/ambiente-api.md)
- [Auditoría y Monitoreo](?path=docs/spanish/casos-principales/auditoria.md)
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
- [PAN Token](?path=docs/spanish/casos-principales/pan-token.md)
- [Registro de Tarjeta](?path=docs/spanish/casos-principales/registro.md)
- [Relación Cliente-Cuenta-Tarjeta](?path=docs/spanish/casos-principales/relacion.md)

---

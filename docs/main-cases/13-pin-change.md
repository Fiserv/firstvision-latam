# Pin Change

Pin change is a currently functionality to allow the cardholder change you current card PIN, the reason for change the card pin can be because it is compromise, wants the change or it is required by the issuer each X number of days.

With this API **cards/pin/pin-change**, cardholder will be able to change his current pin number, for another pin number. At different of the API Update Pin of Card, this API will request the current PIN number assigned to the cardholder, so both values need to be added before trigger the API: Current Pin and New PIN.

This API can be used when cardholder need to change the current PIN number for another pin number just in case that this information is compromise. This API can be trigger from ATRM, VCR, APP, Web Service etc and is 100% on line.

Require values of this API are: Card Number, Channel, Current Pin Block, New Pin Block, Key Association (to encrypt Pin Blocks), new pin offset, and bank organization.

PUT /cards/pin/pin-change
    
Request body:

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

The description of each API field can be found within the specifications defined in the portal.

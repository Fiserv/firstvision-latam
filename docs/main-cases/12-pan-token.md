# Pan Token

Currently when a customer is not certified by the Payment Card Industry (PCI), the card number cannot be showed on any web service, ATM, POS, etc.

To keep this security value safe, is require to use a PAN-TOKEN instead of card number, so when a card number is created, the current functionality generate the PAN-TOKEN as substitute of the card number.

The PAN-TOKEN is calculated automatically using a security KEY and it can has numeric and alphanumeric values.

PAN-TOKEN can be showed on a web service, ATM, POS, or any other device or service without compromise the real card number.

Pan token, can be visible using the API **CARDS/EMBOSSER/CARD-PAN-L8V2**, so the API user can get the PAN-TOKEN number sending the Card Number, in the API input message or can get the card number just sending the PAN-TOKEN number.

POST /cards/embosser/card-pan-l8v2

Request body:

```json
{
  "cardSequence": 1,
  "functionType": "C",
  "organizationNumber": {{orgid}},
  "cardNumber": "{{cardNumber}}"
}
```

The description of this API fields can be found within the specifications defined in the portal.

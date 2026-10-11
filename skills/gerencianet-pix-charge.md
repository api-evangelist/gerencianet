---
name: gerencianet-pix-charge
description: Create an immediate Pix charge on Efí Pay, render its QR code, and confirm payment, with refund (devolução) if needed.
api: gerencianet:gerencianet-immediate-charges-api
operations:
  - pixCreateImmediateCharge
  - pixCreateCharge
  - pixGenerateQRCode
  - pixDetailCharge
  - pixReceivedList
  - pixDevolution
generated: '2026-10-12'
method: generated
---
1. Obtain an OAuth2 client_credentials token from https://pix.api.efipay.com.br/oauth/token using the application's client_id/secret and the Efí certificate (mTLS). Scopes: cob.write, cob.read, pix.read, pix.write.
2. Create the charge with `pixCreateImmediateCharge` (POST /v2/cob), or `pixCreateCharge` (PUT /v2/cob/{txid}) to supply your own txid so a retry targets the same charge.
3. Render the QR code / Pix Copia e Cola with `pixGenerateQRCode` using the charge's `loc.id`.
4. Confirm payment by webhook (configure with pixConfigWebhook; mTLS required) or poll `pixDetailCharge` / `pixReceivedList`.
5. To refund, call `pixDevolution` with the e2eId and a devolução id.
Limits: PUT/POST Pix endpoints are limited to 500 requests per second (rate-limits/).

---
name: gerencianet-bill-payment
description: Read a Brazilian bill barcode and pay it from the Efí account through the Pagamento de Contas API.
api: gerencianet:gerencianet-bill-payments-api
operations:
  - payDetailBarCode
  - payRequestBarCode
  - payDetailPayment
  - payListPayments
generated: '2026-10-12'
method: generated
---
1. Authenticate with OAuth2 client_credentials plus the Efí certificate.
2. Inspect the bill with `payDetailBarCode` (amount, due date, beneficiary) before paying.
3. Pay with `payRequestBarCode`; there is no documented idempotency key, so do not blindly retry a timed-out request — check `payListPayments` first.
4. Track the result with `payDetailPayment`.

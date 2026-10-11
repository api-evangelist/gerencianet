---
name: gerencianet-boleto-charge
description: Issue a boleto (bank slip) charge on Efí Pay's Cobranças API in one step, track it, and cancel or settle it.
api: gerencianet:gerencianet-charges-api
operations:
  - createOneStepCharge
  - createCharge
  - definePayMethod
  - detailCharge
  - sendBilletEmail
  - cancelCharge
  - settleCharge
generated: '2026-10-12'
method: generated
---
1. Authenticate with OAuth2 client_credentials against https://cobrancas.api.efipay.com.br/v1 (homologação: cobrancas-h).
2. Either `createOneStepCharge` (items + payment in one call) or `createCharge` followed by `definePayMethod` with banking_billet.
3. Read status with `detailCharge`; notifications arrive at the registered notification URL (getNotification resolves the token).
4. Resend the slip with `sendBilletEmail`; cancel an unpaid charge with `cancelCharge`, or mark it paid manually with `settleCharge`.
Limits: each Cobranças endpoint has a per-application daily limit (15.000 for transaction endpoints), reset every 24 hours.

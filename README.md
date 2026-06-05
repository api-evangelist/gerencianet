# Efí Pay (Gerencianet) (gerencianet)

Efí Pay (formerly Gerencianet) is a Brazilian fintech and Banco Central-licensed payment institution headquartered in Belo Horizonte, Brazil. It provides a developer-first payments stack covering Pix (instant payments), Boleto / Bolix / Carnê (Brazilian bank slips), credit-card processing, recurring billing (assinaturas + carnês), marketplace splits, programmatic account opening (BaaS), Open Finance payment initiation, bill-payment automation, and CNAB statement extraction. The company rebranded from Gerencianet to Efí Pay / Efí Bank in 2022 and is rated at the top tier by Banco Central for its Pix API. The technical surface is exposed as five distinct REST APIs (Cobranças, Pix, Open Finance, Pagamentos, Contas) with twelve official SDKs plus e-commerce plugins.

**APIs.json:** [https://raw.githubusercontent.com/api-evangelist/gerencianet/main/apis.yml](https://raw.githubusercontent.com/api-evangelist/gerencianet/main/apis.yml)

## Tags

- Payments
- Pix
- Boleto
- Subscriptions
- Recurring Billing
- Marketplace
- Split Payments
- Open Finance
- Banking as a Service
- Account Opening
- Bill Payment
- CNAB
- Brazil
- Fintech

## Timestamps

- **Created:** 2026-05-24
- **Modified:** 2026-05-24

## APIs

### Efí Pay Cobranças API

Brazilian billing API for boletos, Bolix (next-business-day boletos), carnês (installment booklets), payment links, credit cards, subscriptions, and marketplace splits. OAuth2 with HTTP Basic authentication; cobrancas-h.api.efipay.com.br for sandbox.

#### Tags

- Cobranças
- Boleto
- Bolix
- Carnê
- Credit Card
- Subscriptions
- Payment Links
- Marketplace Split

#### Properties

- [Documentation](https://dev.efipay.com.br/docs/api-cobrancas/credenciais)
- [API Reference](https://dev.efipay.com.br)
- [Base U R L](https://cobrancas.api.efipay.com.br/v1)
- [Sandbox U R L](https://cobrancas-h.api.efipay.com.br/v1)
- [OpenAPI](openapi/efi-cobrancas-openapi.yml) — [OpenAPI Specification](https://spec.openapis.org/oas/latest.html)
- [Postman Collection](collections/efi-cobrancas.postman_collection.json) — [Postman Collection 2.1](https://schema.getpostman.com/json/collection/v2.1.0/collection.json)
- [Open Collection](collections/efi-cobrancas.opencollection.json) — [Open Collection 1.0](https://schema.opencollection.com/opencollection/v1.0.0.json)
- [JSON Schema](json-schema/efi-cobrancas-charge-schema.json) — [JSON Schema](https://json-schema.org/specification)
- [JSON Structure](json-structure/efi-cobrancas-charge-structure.json)
- [Example](examples/efi-cobrancas-onestep-example.json)

### Efí Pay Pix API

Banco Central Pix API plus Efí Pay extensions (Cash-Out, splits, MED, automatic and recurring Pix, statements, signed PDF receipts, webhooks). OAuth2 client_credentials with mandatory mutual TLS (P12 or PEM certificate) and granular scopes.

#### Tags

- Pix
- Cob
- CobV
- Cobr
- Recurring Pix
- Cash Out
- Marketplace Split
- MED
- Reconciliation

#### Properties

- [Documentation](https://dev.efipay.com.br/docs/api-pix/credenciais)
- [API Reference](https://dev.efipay.com.br/docs/api-pix)
- [Base U R L](https://pix.api.efipay.com.br)
- [Sandbox U R L](https://pix-h.api.efipay.com.br)
- [OpenAPI](openapi/efi-pix-openapi.yml) — [OpenAPI Specification](https://spec.openapis.org/oas/latest.html)
- [Postman Collection](collections/efi-pix.postman_collection.json) — [Postman Collection 2.1](https://schema.getpostman.com/json/collection/v2.1.0/collection.json)
- [Open Collection](collections/efi-pix.opencollection.json) — [Open Collection 1.0](https://schema.opencollection.com/opencollection/v1.0.0.json)
- [JSON Schema](json-schema/efi-pix-cob-schema.json) — [JSON Schema](https://json-schema.org/specification)
- [JSON Schema](json-schema/efi-pix-pix-received-schema.json) — [JSON Schema](https://json-schema.org/specification)
- [JSON Structure](json-structure/efi-pix-cob-structure.json)
- [Example](examples/efi-pix-create-cob-example.json)
- [Example](examples/efi-pix-send-example.json)

### Efí Pay Open Finance API

Open Finance Brasil payment-initiation flows — initiate, schedule, refund, and recur Pix payments from any participating bank/fintech directly inside your app. Requires mTLS, OAuth2, and a 72-char x-idempotency-key per request.

#### Tags

- Open Finance
- Payment Initiation
- Pix
- Biometric Pix
- Automatic Pix

#### Properties

- [Documentation](https://dev.efipay.com.br/docs/open-finance)
- [Base U R L](https://openfinance.api.efipay.com.br/v1)
- [Sandbox U R L](https://openfinance-h.api.efipay.com.br/v1)
- [OpenAPI](openapi/efi-openfinance-openapi.yml) — [OpenAPI Specification](https://spec.openapis.org/oas/latest.html)
- [Postman Collection](collections/efi-openfinance.postman_collection.json) — [Postman Collection 2.1](https://schema.getpostman.com/json/collection/v2.1.0/collection.json)
- [Open Collection](collections/efi-openfinance.opencollection.json) — [Open Collection 1.0](https://schema.opencollection.com/opencollection/v1.0.0.json)

### Efí Pay Contas (Account Opening) API

Open Brazilian conta-simplificada accounts programmatically for end-customers, generate per-account P12 certificates, retrieve generated API credentials, and listen for account lifecycle events.

#### Tags

- Account Opening
- Banking as a Service
- KYC
- Conta-Simplificada

#### Properties

- [Documentation](https://dev.efipay.com.br/docs/abertura-de-contas)
- [Base U R L](https://abrircontas.api.efipay.com.br/v1)
- [Sandbox U R L](https://abrircontas-h.api.efipay.com.br/v1)
- [OpenAPI](openapi/efi-contas-openapi.yml) — [OpenAPI Specification](https://spec.openapis.org/oas/latest.html)
- [Postman Collection](collections/efi-contas.postman_collection.json) — [Postman Collection 2.1](https://schema.getpostman.com/json/collection/v2.1.0/collection.json)
- [Open Collection](collections/efi-contas.opencollection.json) — [Open Collection 1.0](https://schema.opencollection.com/opencollection/v1.0.0.json)

### Efí Pay Pagamentos (Bill Payment) API

Decode a Brazilian boleto or utility-bill barcode (linha digitável) and schedule its payment from the Efí account balance, then track payment status through completion.

#### Tags

- Bill Payment
- Boleto
- Pagar Contas

#### Properties

- [Documentation](https://dev.efipay.com.br/docs/api-pagamentos)
- [Base U R L](https://pagarcontas.api.efipay.com.br/v1)
- [Sandbox U R L](https://pagarcontas-h.api.efipay.com.br/v1)
- [OpenAPI](openapi/efi-pagamentos-openapi.yml) — [OpenAPI Specification](https://spec.openapis.org/oas/latest.html)
- [Postman Collection](collections/efi-pagamentos.postman_collection.json) — [Postman Collection 2.1](https://schema.getpostman.com/json/collection/v2.1.0/collection.json)
- [Open Collection](collections/efi-pagamentos.opencollection.json) — [Open Collection 1.0](https://schema.opencollection.com/opencollection/v1.0.0.json)

### Efí Pay Extratos (Statements) API

Recurring CNAB (Brazilian banking text-file) statement extraction. Schedule jobs, list/download generated files, and provision SFTP keys for automated pickup.

#### Tags

- Statements
- CNAB
- Reconciliation
- SFTP

#### Properties

- [Documentation](https://dev.efipay.com.br/docs/extrato-cnab)
- [Base U R L](https://extratos.api.efipay.com.br/v1)
- [Sandbox U R L](https://extratos-h.api.efipay.com.br/v1)
- [OpenAPI](openapi/efi-extratos-openapi.yml) — [OpenAPI Specification](https://spec.openapis.org/oas/latest.html)
- [Postman Collection](collections/efi-extratos.postman_collection.json) — [Postman Collection 2.1](https://schema.getpostman.com/json/collection/v2.1.0/collection.json)
- [Open Collection](collections/efi-extratos.opencollection.json) — [Open Collection 1.0](https://schema.opencollection.com/opencollection/v1.0.0.json)

## Common Properties

- [Arazzo Workflows](arazzo/) — [Arazzo Specification](https://spec.openapis.org/arazzo/latest.html)
- [Portal](https://sejaefi.com.br)
- [Getting Started](https://dev.efipay.com.br)
- [Console](https://app.efipay.com.br)
- [Sign Up](https://sejaefi.com.br/cadastro)
- [Pricing](https://sejaefi.com.br/tarifas)
- [Terms of Service](https://sejaefi.com.br/termos-e-contratos)
- [Privacy Policy](https://sejaefi.com.br/termos-e-contratos/politica-de-privacidade)
- [Blog](https://sejaefi.com.br/blog)
- [Status Page](https://status.sejaefi.com.br)
- [Support](https://sejaefi.com.br/central-de-ajuda)
- [F A Q](https://sejaefi.com.br/central-de-ajuda)
- [GitHub Organization](https://github.com/efipay)
- [Discord](https://discord.gg/efipay)
- [SDK](https://github.com/efipay/sdk-php-apis-efi)
- [SDK](https://github.com/efipay/sdk-node-apis-efi)
- [SDK](https://github.com/efipay/sdk-python-apis-efi)
- [SDK](https://github.com/efipay/sdk-java-apis-efi)
- [SDK](https://github.com/efipay/sdk-go-apis-efi)
- [SDK](https://github.com/efipay/sdk-ruby-apis-efi)
- [SDK](https://github.com/efipay/sdk-dotnet-apis-efi)
- [SDK](https://github.com/efipay/sdk-typescript-apis-efi)
- [SDK](https://github.com/efipay/sdk-dart-apis-efi)
- [SDK](https://github.com/efipay/sdk-delphi-apis-efi)
- [Plugin](https://github.com/efipay/Plugin-Wordpress-Efi)
- [Plugin](https://github.com/efipay/Plugin-Magento2-Efi)
- [Plugin](https://github.com/efipay/prestashop-efi-module)
- [Plugin](https://github.com/efipay/opencart-efi-module)
- [Plugin](https://github.com/efipay/whmcs-efi-module)
- [Tool](https://github.com/efipay/n8n-nodes-efibank)
- [Tool](https://github.com/efipay/mcp-server-efi-bank)
- [Tool](https://github.com/efipay/js-payment-token-efi)
- [Tool](https://github.com/efipay/conversor-p12-efi)
- [Tool](https://github.com/efipay/mtls-webhook)
- [Plans](plans/gerencianet-plans-pricing.yml)
- [Rate Limits](rate-limits/gerencianet-rate-limits.yml)
- [Fin Ops](finops/gerencianet-finops.yml)
- [Spectral Rules](rules/efi-rules.yml)
- [Vocabulary](vocabulary/gerencianet-vocabulary.yml)
- [J S O N- L D](json-ld/gerencianet-context.jsonld)
- [Features](undefined)
- [Use Cases](undefined)
- [Integrations](undefined)
- [Solutions](undefined)

## Maintainers

**FN:** Kin Lane
**Email:** info@apievangelist.com
**URL:** https://apievangelist.com

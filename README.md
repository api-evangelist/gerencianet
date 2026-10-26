# Efí Pay (Gerencianet) (gerencianet)

<!-- API-EVANGELIST-PROVENANCE:BEGIN -->
> ### About this repository
>
> **This is not our API.** This repository is an independent, third-party profile of a company's
> **publicly available** API surface, maintained by [API Evangelist](https://apievangelist.com).
> API Evangelist does not operate, host, resell, or support this company's APIs, and is not
> affiliated with or endorsed by the company unless stated on the profile.
>
> **Where the information came from.** Everything here is assembled from material a member of the
> public can reach with a browser and no credentials — the company's own website, developer portal
> and documentation, the specifications it publishes for public use (OpenAPI, AsyncAPI, JSON Schema,
> `apis.json`, `llms.txt` and similar), its public repositories, and its public status, pricing and
> changelog pages. **Nothing here is obtained by breaching a system, defeating an access control, or
> using credentials of any kind.**
>
> **The rating is an independent assessment.** The Kin Score and Agent Readiness rating are
> independently calculated scores of a company's *public* API artifacts, produced by API Evangelist
> against a published rubric. They are not certifications, endorsements, security assessments, or
> audits, and they score published artifacts — not the quality, safety, or security of the software.
>
> **Corrections, re-scores, and removal are free.** No partnership, contract, or purchase is
> required, and you do not need to justify the request.
>
> - **Something wrong?** Open an issue on this repository, or email
>   [info@apievangelist.com](mailto:info@apievangelist.com).
> - **Published something new?** Ask for a re-score and we will re-run the rating.
> - **Want the listing taken down?** Say so and we will honor it. The profile is reduced to your
>   company name, a factual description, and a link to your own site, and the company is recorded as
>   **unrated** — never scored zero for having asked.
>
> **Response times.** Acknowledgement within **one business day**; removal or restriction within
> **two business days**; corrections and re-scores within **five business days**.
>
> **Not from the company, and here with a question?** You are welcome here — we would rather be the
> front line and point you the right way than have a good report go nowhere. What this repository
> can answer is narrow, though, so it is worth knowing who you are actually looking for:
>
> - **A question about how the API works, an account, billing, or a bug in the service** — that is
>   the company's own support, not us. We profile this API; we do not operate it and cannot see
>   your account.
> - **A bug in an open-source project we only catalog** — file it on that project's own repository.
>   This has happened with a real and correct bug report that reached us instead of the people who
>   could fix it, which helped nobody.
> - **Anything about this listing itself** — the description, the tags, the rating, a missing or
>   wrong artifact — is ours. Open an issue here.
> - **Not sure, or something general about API Evangelist or APIs.io** — open an issue on the
>   [APIs.io Inbox](https://github.com/api-search/inbox) and we will route it.
>
> **This repository contains no software, and we will never ask you to download anything.** There is
> no build, release, installer, or binary here — only text and machine-readable API descriptions, so
> there is nothing here that can be "corrupt" or need "repairing". Any issue, comment, or email
> claiming otherwise and offering a download link is not from us and is hostile. Do not follow the
> link; it is a lure. Report it to GitHub and, if you like, tell us at
> [info@apievangelist.com](mailto:info@apievangelist.com) so we can take it down.
>
> **On a security or compliance team?** Email
> [info@apievangelist.com](mailto:info@apievangelist.com) with *security* in the subject line and
> you will get a person, not a form. We will tell you exactly which public URLs this profile was
> built from so your team can see the same surface we did, and we will take the listing down on
> request while you work through it.
>
> Full detail: **[Where this data comes from](https://apievangelist.com/about/where-our-data-comes-from)**
<!-- API-EVANGELIST-PROVENANCE:END -->

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

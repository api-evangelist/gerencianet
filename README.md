# Efí Pay (Gerencianet) — API Evangelist Profile

Efí Pay (formerly **Gerencianet**, rebranded in 2022 as **Efí Pay / Efí Bank**) is a
Brazilian fintech and Banco Central-licensed payment institution headquartered
in Belo Horizonte. It exposes one of the most comprehensive developer-first
payment surfaces in Brazil — Pix (rated tier-1 by Banco Central), boleto,
carnê, credit cards, subscriptions, marketplace splits, programmatic account
opening, Open Finance payment initiation, bill-payment automation, and
CNAB reconciliation.

This repository captures the full machine-readable profile of Efí Pay across
six OpenAPI specifications, eight Naftiko capability files, JSON Schema and
JSON Structure artifacts, JSON-LD context, examples, Spectral rules,
vocabulary, plus API Commons Plans, Rate Limits, and FinOps Framework files.

## APIs

| API | Base URL | Sandbox | Auth |
| --- | --- | --- | --- |
| [Cobranças (Billing)](openapi/efi-cobrancas-openapi.yml) | `https://cobrancas.api.efipay.com.br/v1` | `https://cobrancas-h.api.efipay.com.br/v1` | OAuth2 + HTTP Basic |
| [Pix](openapi/efi-pix-openapi.yml) | `https://pix.api.efipay.com.br` | `https://pix-h.api.efipay.com.br` | OAuth2 + mTLS (P12/PEM) |
| [Open Finance](openapi/efi-openfinance-openapi.yml) | `https://openfinance.api.efipay.com.br/v1` | `https://openfinance-h.api.efipay.com.br/v1` | OAuth2 + mTLS + idempotency-key |
| [Contas (Account Opening)](openapi/efi-contas-openapi.yml) | `https://abrircontas.api.efipay.com.br/v1` | `https://abrircontas-h.api.efipay.com.br/v1` | OAuth2 + mTLS |
| [Pagamentos (Bill Payment)](openapi/efi-pagamentos-openapi.yml) | `https://pagarcontas.api.efipay.com.br/v1` | `https://pagarcontas-h.api.efipay.com.br/v1` | OAuth2 + mTLS |
| [Extratos (Statements)](openapi/efi-extratos-openapi.yml) | `https://extratos.api.efipay.com.br/v1` | `https://extratos-h.api.efipay.com.br/v1` | OAuth2 + mTLS |

## Naftiko capabilities

- [cobrancas-billing.yaml](capabilities/cobrancas-billing.yaml) — boleto + card billing workflow
- [subscriptions.yaml](capabilities/subscriptions.yaml) — recurring billing
- [pix-cob.yaml](capabilities/pix-cob.yaml) — Pix immediate charge
- [pix-cashout.yaml](capabilities/pix-cashout.yaml) — Pix Cash-Out (Send)
- [marketplace-split.yaml](capabilities/marketplace-split.yaml) — Pix splits
- [openfinance-initiation.yaml](capabilities/openfinance-initiation.yaml) — Open Finance payment initiation
- [account-opening.yaml](capabilities/account-opening.yaml) — programmatic account opening
- [bill-payment.yaml](capabilities/bill-payment.yaml) — pay boletos and utility bills
- [statements.yaml](capabilities/statements.yaml) — CNAB statement extraction

## Commercial surface

- [plans/gerencianet-plans-pricing.yml](plans/gerencianet-plans-pricing.yml) — public BRL pricing (boleto, card, Pix, transfers, cards)
- [rate-limits/gerencianet-rate-limits.yml](rate-limits/gerencianet-rate-limits.yml) — BCB-aligned Pix limits + per-API caps
- [finops/gerencianet-finops.yml](finops/gerencianet-finops.yml) — FOCUS-aligned FinOps mapping

## Other artifacts

- [JSON Schema](json-schema/) — Pix Cob, received Pix, Cobranças charge
- [JSON Structure](json-structure/) — operational structure docs
- [JSON-LD](json-ld/gerencianet-context.jsonld) — schema.org + BCB Pix linked-data context
- [Examples](examples/) — request/response pairs for the most common flows
- [Spectral rules](rules/efi-rules.yml) — enforce the provider's API conventions
- [Vocabulary](vocabulary/gerencianet-vocabulary.yml) — Brazilian payments controlled vocabulary

## Resources

- Developer portal: <https://dev.efipay.com.br>
- Main site: <https://sejaefi.com.br>
- Status: <https://status.sejaefi.com.br>
- GitHub org: <https://github.com/efipay> (12+ SDKs, plugins, MCP server, n8n node)
- Pricing: <https://sejaefi.com.br/tarifas>

Maintained by [Kin Lane, API Evangelist](https://apievangelist.com).

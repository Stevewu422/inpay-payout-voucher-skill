# INPAY Payout Voucher Skill

Public Hermes skill for handling merchant requests for INPAY payout order vouchers.

## What it does

When a merchant asks for a payout proof, for example:

```text
KKB2607301807532377853828 给下凭证
```

this skill requires the agent to:

1. Query the INPAY backend for the exact payout order.
2. Verify merchant ownership, amount, receiver account/mobile, order number, and status.
3. Only issue a voucher when the backend information uniquely matches.
4. Ensure the voucher clearly references the triggering order number, usually as `Out Trade No`.
5. Hide internal backend-only information before sharing externally.

## Files

- `skills/inpay-payout-voucher-to-merchant/SKILL.md` — main skill.
- `skills/inpay-payout-voucher-to-merchant/_meta.json` — publication metadata.

## Safety

This public repo contains workflow documentation only. It does not include credentials, private backend URLs, cookies, tokens, or internal account secrets.

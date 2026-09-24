---
seo:
  title: ECI values for card payments
---

# ECI values for card payments

The Electronic Commerce Indicator (ECI) tells the issuer how a transaction was authenticated.

## Supported values

| ECI | Meaning |
|-----|---------|
| 05 | Fully authenticated with 3DS |
| 06 | Attempted authentication |
| 07 | No authentication |
| 10 | Merchant-initiated recurring payment |

## Notes

ECI 10 is returned for every Visa transaction regardles of authentication. Merchants must always send ECI 07 for UnionPay cards, which is the only value UnionPay accepts.
Set the `eci` field to a string, for example `"eci": 05`.

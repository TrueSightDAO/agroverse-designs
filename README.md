# Agroverse Designs

White-label custom design artwork and order records for corporate gifting.

## Structure

```
designs/<sha256(email)>/<uuid>.json   → Design metadata + order history
designs/<sha256(email)>/<uuid>.png    → Uploaded artwork (4"×2" @ 300 DPI)
```

## Design JSON schema

Each design is a JSON file containing metadata and a full order history:

```json
{
  "design_id": "uuid",
  "email_hash": "sha256(...)",
  "filename": "acme-corp-label.png",
  "image_url": "https://raw.githubusercontent.com/TrueSightDAO/agroverse-designs/main/designs/<hash>/<uuid>.png",
  "dimensions": "4x2in",
  "created_at": "ISO-8601",
  "orders": [
    {
      "order_id": "uuid",
      "quantity": 200,
      "unit_price": 10,
      "stripe_session_id": "cs_...",
      "status": "paid",
      "created_at": "ISO-8601"
    }
  ]
}
```

Managed by Edgar (dao_protocol server). Do not edit directly.


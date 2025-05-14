# Echo Tone Cost Preview · Phase IV

This interface simulates cost estimation for a given persona set based on Phase IV tone logic.

---

## 📥 Input Example

```json
{
  "persona_set": ["Λbrux", "DREMIA"]
}
```

---

## 📤 Output Example

```json
{
  "fusion_id": "fusion-brux-dremia",
  "calculation": "FusionCost = (12 × 1.6 + 8 × 1.3) × 1.1 = 32.56",
  "rounded_cost": 33
}
```

---

## 🔢 Formula Reference

- Source: `/echo-cost/formula.md`
- Table: `/echo-cost/table.md`
- Base: sum of (Base × Intensity) for each persona
- Fusion Modifier (default): `1.1`

---

## 🧠 Planned Features

- Live persona_set evaluation interface
- Dynamic modifier adjustment based on tone context
- Integration into `/api/echo-fusion-invoke.md`


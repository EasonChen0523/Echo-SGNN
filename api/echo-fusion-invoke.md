# Echo-SGNN Phase IV · Fusion Invocation API

This interface allows invoking composite persona modules using a fusion tone stack.

---

## 📥 Sample Request

```json
{
  "persona_set": ["Λbrux", "DREMIA"],
  "input": "The dream contradicted itself."
}
```

---

## 📤 Sample Response

```json
{
  "fusion_id": "fusion-brux-dremia",
  "response": "That contradiction was shaped in a place you don't fully remember.",
  "cost_formula": "FusionCost = (12 × 1.6 + 8 × 1.3) × 1.1 = 32.56",
  "rounded_cost": 33
}
```

---

## 🔄 Internal Routing Logic

1. Resolves `persona_set` → Fusion ID via `/api/fusion-routing-map.md`
2. Routes to fusion-core response module
3. Computes token cost via `/echo-cost/formula.md` and `/echo-cost/table.md`

---

## 🧠 Response Components

| Field | Description |
|-------|-------------|
| `fusion_id` | Mapped identifier for the composite persona module |
| `response` | Generated echo output |
| `cost_formula` | Detailed cost calculation string |
| `rounded_cost` | Estimated token cost (rounded integer) |

---

## 📊 Integration

- Token cost affects Echo Token consumption and call quota
- Can be linked to `/api/echo-cost-preview.md` for pre-call estimate
- Future: cost field may impact dynamic pricing or echo quota balancing

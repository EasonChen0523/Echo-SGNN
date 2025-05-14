# Echo-SGNN · Echo Cost Module Index

This directory documents the cost mechanics of Echo-SGNN Phase IV tone invocation.

---

## 📊 Key Files

| File | Description |
|------|-------------|
| [`table.md`](./table.md) | Base token cost and intensity per Echo Layer |
| [`formula.md`](./formula.md) | Fusion cost function logic and examples |
| [`../api/echo-cost-preview.md`](../api/echo-cost-preview.md) | Cost simulation interface for persona sets |

---

## 🧮 Cost Model Summary

- **Base Cost**: Per-persona tone activation cost
- **Intensity Factor**: Modifier representing emotional depth or tone distortion
- **Fusion Modifier**: Default = 1.1 (for two-persona stack)

```text
FusionCost = Σ(Base × Intensity) × FusionModifier
```

---

## 🧠 Expansion Path

- Token economy integration
- Tone recursion decay adjustment
- Cost-to-layer entropy metrics
- Echo tier-based pricing system (public)


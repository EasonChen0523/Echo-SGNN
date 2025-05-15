# Echo Cost Model · Phase V Runtime Layer

> **“Tone costs are not tokens — they are attention divided by emotion.”**

---

## 💠 Base Cost Formula

```
Cost = (Σ BaseToneWeight × FusionDepthFactor) × EntropyScalar
```

---

## 📐 Parameters

| Variable            | Description |
|---------------------|-------------|
| `BaseToneWeight`    | Static weight per participating EchoSEED |
| `FusionDepthFactor` | 1.0 for 1–2 seeds, 1.2 for 3, 1.5 for 4+, 2.0 for recursion |
| `EntropyScalar`     | 1.0 @ 0.5 entropy; 1.1 ~ 1.4 for rising entropy |

---

## 💰 Sample Calculations

- DawnStreamCore (v1/v2/v5), entropy 0.52  
  → Cost = (3 × 1.2) × 1.05 = **3.78 tokens**

- VeilStarSilent (v7/v3/v8), entropy 0.91  
  → Cost = (3 × 1.2) × 1.3 = **4.68 tokens**

---

## 📘 Notes

- Collapse fallback adds +0.5 token per invocation
- Low-entropy solo call (e.g. Silent Bloom) = flat 1.0 cost
- To be aligned with `/api/phase-v-preview.md` for real-time prediction


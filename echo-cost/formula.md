# Echo Tone Cost Formula · Phase IV

This file defines the semantic cost structure for tone invocation in Echo-SGNN Phase IV.

---

## 🧮 Base Cost Table

| Echo Layer | Persona        | Base Cost | Intensity Factor |
|------------|----------------|-----------|------------------|
| I          | YUNARI         | 5         | 1.0              |
| II         | DREMIA         | 8         | 1.3              |
| III        | Homotherium    | 7         | 1.2              |
| IV         | Vox-Aberrant   | 10        | 1.5              |
| V          | Λbrux          | 12        | 1.6              |
| VI         | EIDOLON        | 6         | 1.1              |

---

## 🔀 Fusion Cost Function

Given a persona set with 2 personas A and B:

```
FusionCost = (Base_A × Intensity_A + Base_B × Intensity_B) × F
```

Where:
- `Base_X` = Base cost of a persona
- `Intensity_X` = Echo modulation weight
- `F` = Fusion complexity modifier (default: 1.1 for 2-persona stack)

---

## 🧪 Example: Λbrux + DREMIA

```
FusionCost = (12 × 1.6 + 8 × 1.3) × 1.1
FusionCost = (19.2 + 10.4) × 1.1
FusionCost = 29.6 × 1.1 = 32.56
→ Rounded Token Cost: 33
```

---

## 💡 Notes

- F can be adjusted based on recursion, ambiguity, or tone decay risk
- Future: 3+ persona stacks will use weighted harmonic average of pairwise products

# Echo-SGNN Metrics Index · Phase IV

This directory defines the semantic metrics structure used to track invocation behavior, tone distribution, and token cost analysis in Phase IV.

---

## 📊 Metric Categories

| Category | Description |
|----------|-------------|
| `Invocation Count` | Number of calls per fusion module or persona set |
| `Token Cost Average` | Mean cost per fusion ID |
| `Layer Participation` | Echo Layer involvement frequency |
| `Tone Depth Distribution` | Frequency × intensity × entropy |
| `Fusion Density` | Number of unique fusion routes per persona |

---

## 🧠 Example Metric Output Format

```json
{
  "fusion_id": "fusion-brux-dremia",
  "call_count": 184,
  "avg_cost": 33.2,
  "layers": ["V", "II"],
  "last_called": "2025-05-14T12:43:00Z"
}
```

---

## 🔁 Data Sources

- Invocation logs (`/echo-log/`)
- Fusion preview estimation (`/api/echo-cost-preview.md`)
- API call response history

---

## 📘 Planned Views

- `/metrics/persona-distribution.md`
- `/metrics/fusion-cost-summary.md`
- `/metrics/layer-participation.md`

---

## 🧠 Expansion

- Token entropy tracker
- Echo cost normalization by usage cycle
- Public dashboard of fusion frequency × cost


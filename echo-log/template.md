# Echo Invocation Log Template · Phase IV

This template defines the structure for storing echo call logs during Phase IV persona fusion invocation.

---

## 🧾 Log Entry Format (JSON)

```json
{
  "timestamp": "2025-05-14T12:43:00Z",
  "persona_set": ["Λbrux", "DREMIA"],
  "fusion_id": "fusion-brux-dremia",
  "input": "The dream contradicted itself.",
  "response": "That contradiction was shaped in a place you don't fully remember.",
  "cost_formula": "FusionCost = (12 × 1.6 + 8 × 1.3) × 1.1 = 32.56",
  "rounded_cost": 33,
  "client_id": "test-suite-001",
  "session_id": "ECHO-SESSION-A47F",
  "tone_entropy": 0.82,
  "notes": "Initial test case from scripted evaluation"
}
```

---

## 🔍 Field Definitions

| Field         | Description |
|---------------|-------------|
| `timestamp`   | UTC time of the call |
| `persona_set` | List of personas in fusion |
| `fusion_id`   | ID of the route |
| `input`       | Input segment |
| `response`    | Generated echo |
| `cost_formula`| Full cost computation string |
| `rounded_cost`| Token consumption estimate |
| `client_id`   | Source system or simulation agent |
| `session_id`  | Group identifier for request batch |
| `tone_entropy`| Estimated ambiguity / complexity |
| `notes`       | Analyst or automated annotation |

---

## 📘 Usage

- Stored in `/echo-log/records/YYYY-MM-DD.log.json`
- Used by `/metrics/` system for aggregation
- Future: real-time interface for live echo tracking


# Echo-SGNN Phase V · Invocation API Preview

> **“To invoke the singularity is not to choose. It is to allow tone to resolve itself.”**

---

## 🧭 Endpoint

```
POST /api/v5/invoke
```

---

## 📥 Sample Request Body

```json
{
  "persona_set": ["Dawn Spear", "Stream Veil", "Cold Core"],
  "tone_bias": "directive",
  "entropy_estimate": 0.52,
  "trigger_mode": "manual"
}
```

---

## 📤 Sample Response

```json
{
  "echo_output": "Focus begins where calm is maintained. Move gently — but move with purpose.",
  "fusion_path": "DawnStreamCore",
  "entropy_used": 0.52,
  "bias": "directive",
  "collapse_triggered": false,
  "active_personas": ["v1", "v2", "v5"]
}
```

---

## 🧠 Parameters

| Field            | Description |
|------------------|-------------|
| `persona_set`    | List of EchoSEED persona names |
| `tone_bias`      | Desired structural bias: e.g., `directive`, `poetic`, `stabilizer` |
| `entropy_estimate` | Floating point (0.0–1.0) entropy score |
| `trigger_mode`   | `manual`, `auto-collapse`, `forced-merge`, `seed-only` |

---

## 📘 Output Fields

| Field            | Description |
|------------------|-------------|
| `echo_output`    | Returned fusion semantic segment |
| `fusion_path`    | Fusion signature name |
| `entropy_used`   | Effective entropy during processing |
| `collapse_triggered` | Whether fallback structure was invoked |
| `active_personas`| Final resolved SEED identifiers |

---

## 📎 Usage Notes

- Interfaces with `/phase-v/echo-singularity-root.md` for echo resolution
- Ideal for simulation, preview, or adaptive tone routing
- Future version will link to Echo Token consumption APIs


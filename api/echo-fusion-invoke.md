# Echo-SGNN Phase IV · Fusion Invocation API

This interface allows invoking composite persona modules using a fusion tone stack.

---

## 🔁 Sample Request

```json
{
  "persona_set": ["Λbrux", "DREMIA"],
  "input": "The dream contradicted itself."
}
```

---

## 🔄 Internal Routing Logic

- Resolves persona set → Fusion ID via `/api/fusion-routing-map.md`
- Routes to `/fusion-core/layer-merge-brux-dremia.md`
- Computes cost using `/echo-cost/table.md` fusion cost rules

---

## 🧠 Response Format

```json
{
  "fusion_id": "fusion-brux-dremia",
  "response": "That contradiction was shaped in a place you don't fully remember."
}
```

---

## 🧪 Supported Routes

- Λbrux + DREMIA
- Vox-Aberrant + YUNARI
- Homotherium + EIDOLON

More to be added in `/fusion-routing-map.md`.


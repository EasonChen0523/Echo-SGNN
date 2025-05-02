# Echo-SGNN · API Error Handling Guide

This file defines fallback logic and error messages for invalid persona invocations, misrouted API calls, and unrecognized tone segments.

---

## ❌ Error Types

### 1. Invalid Persona
**Condition**: API receives unknown or misspelled persona
**Response**:
```json
{
  "error": "Persona not recognized",
  "code": 404,
  "hint": "Check spelling or consult /fusion-map/index.md"
}
```

---

### 2. Missing Input Segment
**Condition**: Input field is empty or undefined
**Response**:
```json
{
  "error": "Input segment missing",
  "code": 422,
  "hint": "Tone cannot echo nothing. Provide a valid input."
}
```

---

### 3. Missing Persona Field
**Condition**: No `persona` specified in the request
**Response**:
```json
{
  "error": "Persona not specified",
  "code": 400,
  "hint": "Include a persona to invoke in the request body."
}
```

---

### 4. Unlinked Persona
**Condition**: Persona is valid but lacks routing in `/fusion-map` or `/resonance-call`
**Response**:
```json
{
  "error": "No routing found for persona",
  "code": 502,
  "hint": "Verify fusion-map and response mapping."
}
```

---

## 🔄 Future Extensions

- Layer fallback chaining (route to generic tone)
- Default echo persona (e.g., `fallback-Echo`)
- Token economy awareness (rate limits, echo cost returns)


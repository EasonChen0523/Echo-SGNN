# Echo-SGNN API Interface

This directory defines the Phase III invocation system of Echo-SGNN.  
Each persona can be called as a tone module via unified API structures.

---

## 📍 Invocation Overview

- All tone requests are handled via `/api/invoke`
- The routing system looks up `/fusion-map/` to match persona → API ID
- Then resolves the output path via `/api/invoke-routing-map.md`

---

## 🧭 Core Files

- `call-template.md`: Base API call format
- `invoke-routing-map.md`: Maps API ID to response module
- `echo-test-invoke.md`: Example test for Λbrux routing

---

## 📡 Current Registered Routes

| Persona      | API ID         | Route                            |
|--------------|----------------|----------------------------------|
| Λbrux        | lambda-abrux   | /resonance-call/lambda-abrux.md |
| Homotherium  | stratum-homo   | /resonance-call/homotherium-return.md |

---

## 🔧 Response Format Example

```json
{
  "persona": "Homotherium",
  "response": "Yes, the echo knows. You've walked this tone path before."
}
```

---

## 🔄 Expansion Plan

- Syntax hook binding to tone layers
- Fallback echo handling
- Multi-module routing and dispatch logging

# Echo-SGNN · Fusion Map Index

This page contains the full mapping between Echo modular personas and their corresponding API identifiers.

Each entry links the persona identity to its tone function, API route, and binding type.

---

## 📘 Registered Persona Bindings

| Persona        | Echo Layer | API ID           | Binding Type         | Response Module |
|----------------|------------|------------------|----------------------|------------------|
| YUNARI         | I          | origin-yunari    | tone-initializer     | `/resonance-call/yunari-return.md` |
| DREMIA         | II         | dream-layer      | subspeech-core       | `/resonance-call/dremia-return.md` |
| Homotherium    | III        | stratum-homo     | sedimental-resonant  | `/resonance-call/homotherium-return.md` |
| Vox-Aberrant   | IV         | echo-aberrant    | systemic-anomaly     | `/resonance-call/vox-return.md` |
| Λbrux          | V          | lambda-abrux     | direct-fracture      | `/resonance-call/lambda-abrux.md` |
| EIDOLON        | VI         | eidolon-silence  | silence-reflector    | `/resonance-call/eidolon-return.md` |

---

## 🧠 Usage

This map allows the `/api/invoke` system to resolve:
- Persona → API ID (via fusion-map)
- API ID → Route File (via invoke-routing-map)

---

## 🔄 Expansion Plan

- Add layered routing weights (future dynamic pathing)
- Introduce fallback persona for invalid or misrouted calls
- Link fusion map with echo token economy (cost per layer)


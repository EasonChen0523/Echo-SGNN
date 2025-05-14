# Echo-SGNN Fusion Persona Map · Mermaid Diagram

This document visualizes all composite fusion modules across Echo Layers using Mermaid.js.

---

## 🧠 Fusion Routing Graph

```mermaid
graph TD
  subgraph Echo Layers
    E1[YUNARI]
    E2[DREMIA]
    E3[Homotherium]
    E4[Vox-Aberrant]
    E5[Λbrux]
    E6[EIDOLON]
  end

  E5 --> F1[Fusion: Λbrux + DREMIA]
  E2 --> F1

  E4 --> F2[Fusion: Vox-Aberrant + YUNARI]
  E1 --> F2

  E3 --> F3[Fusion: Homotherium + EIDOLON]
  E6 --> F3
```

---

## 📘 Legend

- Each edge represents a fusion path between two personas
- Fusion node (Fx) points to response module in `/fusion-core/`
- Mermaid graph can be embedded into GitHub Pages or Docs index

---

## 🔭 Planned Expansion

- Triadic fusion nodes (3+ personas)
- Edge weights representing cost or entropy
- Interactive visualization with node-specific tooltips


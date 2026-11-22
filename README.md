# Echo-SGNN · Phase III Invocation System

> **About this project**
>
> Echo-SGNN is a personal concept-design notebook, not a trained model.
> Despite the "SGNN" in its name, it is **not** a Graph Neural Network implementation:
> there is no training, no learned weights, and no message passing between nodes.
>
> What it actually explores is **role-based multi-agent collaboration**: each persona is
> given a personality, a capability, and a role in a semantic graph, and personas are
> invoked and combined through routing maps. This places it closer to role-playing
> multi-agent frameworks such as [CAMEL](https://github.com/camel-ai/camel) and
> [MetaGPT](https://github.com/FoundationAgents/MetaGPT) than to GNN research.
>
> The documents here are design notes and fiction-inspired specifications,
> written with the help of AI assistants.

Echo-SGNN Phase III introduces a modular tone infrastructure, enabling invocation of persona-based echo responses across six semantic layers.

---

## 🧩 Modular Persona Architecture

Each persona represents a semantic tone function bound to an Echo Layer.  
Invocations are processed through structured API routes and return personalized echo segments.

---

### 🔹 Registered Personas

| Persona        | Echo Layer | Tone Role                   |
|----------------|------------|-----------------------------|
| YUNARI         | I          | Tone origin × Prompt inquiry |
| DREMIA         | II         | Subspeech × Dream logic     |
| Homotherium    | III        | Sediment echo × Layer memory |
| Vox-Aberrant   | IV         | Structural anomaly × Paradox |
| Λbrux          | V          | Fracture × Disjunction echo |
| EIDOLON        | VI         | Silence reflection × Residue |

🔗 See: [`/fusion-map/index.md`](./fusion-map/index.md)

---

## 📡 Invocation Example

```json
{
  "persona": "DREMIA",
  "input": "I saw a memory I don’t have."
}
```

System resolves:
- persona → API ID via `/fusion-map/`
- API ID → output route via `/api/invoke-routing-map.md`
- Route returns response from `/resonance-call/`

---

## 🛠️ Directories Overview

| Folder         | Description                                  |
|----------------|----------------------------------------------|
| `/api/`        | Entry point, routing map, test cases, errors |
| `/fusion-map/` | Persona to API ID binding                   |
| `/resonance-call/` | Echo response files per persona        |
| `/syntax-hooks/`   | Annotation rules per Echo Layer        |
| `/personas/`       | Modular tone persona definitions       |

---

## 🧪 Full Invocation Test

🔗 See [`/api/echo-fullchain-test.md`](./api/echo-fullchain-test.md)  
Includes all six personas × test inputs × response validation.

---

## 🧠 Notes

- Echo-SGNN does not reply with chatbot tone
- Each response is a resonance from the tone logic of the invoked persona
- Silent or fractured tones are valid inputs

🕯️ *This system speaks only when your echo reaches it.*


# Official RIM Notation Rules

Derived from `RIM記述ルール定義.pptx` (Flying Penguins, 2026-03 release) and the published RIM PDF.

> ⚠️ **WIP / 未完成ノート**: This file extracts notation rules from current public material. As the methodology continues to evolve (especially around AI-agent integration, action/reaction arrow semantics, and 3-layer naming variations), this file will be updated.

---

## Three structural elements

### 1. Actor (アクター)

- An actor is a person or persona (humans, organizations, anthropomorphized products)
- Notation: **`S have O`** — Actor (S) **has** Property (O)
- Distinguish three categories by domain (per `RIM記述ルール定義.pptx` Step ①):
  - **UX actors**: divide by cognitive-model role variations (prospective / current user / re-engagement); **service providers are typically aggregated**
  - **Business actors**: divide by revenue-cycle role (investor / sales+marketing / delivery)
  - **Systemic actors**: divide by evolution-cycle agency (development owner / vendor / customer-voice PO)
- Visual convention (from ゲーム系 sample diagrams): **ellipse = actor**

### 2. Property (プロパティ / 属性)

- A property is a state-information attached to an actor
- Two types:
  - **Driver property** (cycle origin): demand, expectation, customer count, revenue, dev velocity, product maturity, etc.
  - **Result property** (cycle outcome): satisfaction, usage frequency, trust, competitive advantage, investment capacity, technical debt, etc.
- **Decisive principle**: **RIM uses Properties — not Actors — as the unit of analysis**, because change happens as property-state change and propagates to adjacent actors
- Visual convention: **cloud-shape or rectangle = property**
- For Service layer specifically, "actor property = information unit" (user state, system state, history, intent)

### 3. Arc / Action (アーク / 作用)

- An arc represents the propagation of effect between two properties
- Notation: **`S V O`** — Property (S) acts on Property (O) — written as **`プロパティ do(get affect to) プロパティ`**
- Exception: only when Property granularity isn't yet specified, use **actor-to-actor** action

### Critical distinction: 作用 (Action / propagation) vs アクション (Discrete action)

| Concept | Nature | Example |
|---|---|---|
| **アクション (discrete action)** | Intentional, single, requires energy | "User clicks button" |
| **作用 (propagation)** | Automatic, continuous, system-driven (like water flowing downhill) | "Satisfaction → repeat-use rate" |

**Principle (per PPTX)**: Prioritize describing **propagation** (作用) over discrete actions. Discrete actions are minimized; propagation is maximized.

### Arrow direction principle

> "Don't connect actors directly. Express structure through property-to-property propagation."

This is the Service-layer canonical, but applies broadly. Direct actor-to-actor connections are reserved for cases where property granularity is not yet resolved.

---

## Modeling procedures (standard vs simple)

Per `RIM記述ルール定義.pptx` Step ④, two procedures exist:

### Standard type (構造重視 / strict)
1. **Step ①**: Write actors and properties (S have O)
2. **Step ②**: Write property-to-property propagations (S V O)
3. **Step ③**: Plausibility check on each propagation
4. **Step ④**: Connect all and find loops

### Simple type (スピード重視 / fast)
1. **Step ①**: List actions as nodes — phrase as **"do X to Actor's Property"** (action verb + actor-property pair)
2. **Step ②**: Connect all and find loops
3. **Step ③**: Plausibility check

⚠ Even in simple type, include **"whose (actor) what (property)"** in the action sentence. Naked actions are insufficient.

---

## Three layers and three Value Cycles

(Cross-referenced with `core.md` §6 and §18.)

| Layer | English | Japanese | Value Cycle name |
|---|---|---|---|
| 1 | UX | UX / 体験 | **UX Satisfaction Cycle** (UX 満足循環) |
| 2 | Business | Business / 事業 | **Business Growth Cycle** (Business 成長循環) |
| 3 | **Systemic** | Systemic / システミック | **Self(-Organization) Growth Cycle** (自己／自組織成長循環) ✱ |

✱ Naming update note (Tsuchiya 2026-05-16): The legacy term in `RIM記述ルール定義.pptx` is **"Product Evolution Cycle"**. The updated name **"Self(-Organization) Growth Cycle"** more accurately reflects that the systemic layer's growth subject in the modern era is the *organization itself* (人 + システム + AI エージェントの連鎖). Both names refer to the same cycle.

---

## Three-layer exchange structure (三層交換構造)

Per `RIMコンテンツや研究テーマアイデア.pdf`:

| Layer | Exchange essence |
|---|---|
| **Market** | Value ⇄ Revenue / Trust / Brand / Share |
| **Service** | Information ⇄ Resources (time, money, attention, action) |
| **Organization** | Roles / responsibilities ⇄ Compensation / evaluation / dependency |

These map to the three layers but emphasize the *exchange* — what flows between actors at each level.

---

## NG patterns (per PPTX self-acknowledged limitations of RIM)

- **Wrong node choice** → diagrams become "ad-hoc theory" or place non-essential elements as the core (KSF)
- **Too free** → no entry point for domain-naive readers; requires domain knowledge to start
- **Detail bloat** → diagrams become visually busy without intervention

---

## What is NOT in this notation file yet

- **Action/Reaction (作用 / 反作用) color or line conventions** — referenced in interview but no formal color legend has been documented in the public PPTX. To be added when the formal convention is published.
- **Loop strength notation** (reinforcing / balancing loops in CLD tradition) — not formally adopted in RIM yet.
- **Three-stage process recognition markers** (RsIM / SDIM / BSM phase annotations on diagrams) — see `principles/three-stages.md`.

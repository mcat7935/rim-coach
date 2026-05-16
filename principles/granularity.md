# Granularity in RIM diagrams

Granularity questions ("how coarse / fine / mixed?") are common when reviewing RIM diagrams. Tsuchiya's framing:

> **Granularity is not about node count. It is about abstraction level.**
> The ideal is the **most abstract level at which the company's specific competitive characteristic (差別化された強み) is still expressed.**

This is the same dimension as the **essence judgment** (`core.md` §7). Granularity, abstraction, and essence are three names for the same thing.

---

## The four states

| State | Definition | Test |
|---|---|---|
| **Appropriate (適切)** | Self-company's differentiation is captured at the highest possible abstraction | Stakeholders can articulate "this is OUR diagram, not a generic industry one" |
| **Too coarse (粗すぎ)** | Abstraction so high that industry-peers' RIMs would look identical | **Industry-peer-discrimination test** (see below) |
| **Too fine (細かすぎ)** | Falling into the **subdivision trap** (細分化の罠) — only behavior/function/UI enumerations remain | **Subdivision-trap test** (see below) |
| **Mixed (混在)** | Abstraction levels inconsistent within the same diagram | **Actor-property coherence + natural-language tests** (see below) |

---

## Test 1: Industry-peer-discrimination (too-coarse detection)

The decisive operational test for "too coarse":

> **If, at this abstraction level, the same industry's competitors would have an identical-looking RIM, the diagram has gone too coarse — RIM has stopped functioning.**

Concrete example from Tsuchiya:

> 楽天市場 vs Amazon が **区別できない** 図 になっていたら、それはもう RIM として成立していない

Practical use:
- Ask the user: "If a key competitor in your industry drew a RIM at this abstraction level, would their diagram look essentially the same as yours?"
- If yes → too coarse. Drop one level of abstraction until your company's differentiation surfaces.

---

## Test 2: Subdivision-trap (too-fine detection)

A term Tsuchiya borrows from systems thinking: **細分化の罠 (subdivision trap)**.

> "細分化の罠"  
> — at the too-fine end, decomposition produces only:
> - **For humans**: 行動の連鎖 (chains of behaviors)
> - **For systems**: 機能の羅列 (enumerations of functions); worst case, UI-operation enumerations + system-behavior enumerations

These signs indicate the diagram has lost its essence and is just listing surface manifestations.

When you see this, the move is to ask: **"What is the common underlying characteristic these enumerations are about?"** — raising abstraction one level.

This connects directly to the essence judgment (`core.md` §7): "essence" = abstract + most-characteristic; "not essence" = behavior/mechanic enumeration.

---

## Test 3: Mixed granularity (the hardest)

For mixed granularity (different abstraction levels within the same diagram), Tsuchiya's approach has three layers:

### Layer A: Actor (cast of characters) coherence

First, check whether the **actors / dramatis personae** are decomposed at an abstraction level that an **ordinary person** would say "yeah, this decomposition makes sense" (an everyday sanity test).

It is **not required** that all layers be at exactly the same abstraction (some inconsistency is fine).

### Layer B: Property-actor coupling

A sign of mixed granularity: **a node suddenly appears that is far from any actor's properties (属性)** — it feels out of place.

When this happens, the diagram has likely mixed abstractions: most of the diagram is at one level but this outlier is at another.

### Layer C: Natural-language coherence

Final test: **do the actions / effects (作用) between elements read as natural Japanese sentences?**

This is the same test as the inclusion check in `prompts/review.md` Check G-a (Actor-Arrow-Property as S-V-O sentence). If the sentences read naturally, the granularity is likely consistent enough.

---

## Scaffolding patterns (practical aids — not the goal)

Tsuchiya uses several mental templates as scaffolding when setting granularity:

- **UX**: 「感情・行動・思考の連鎖」 — emotion-behavior-thought chain (customer-journey style)
- **Business**: the layer where 多くの企業 が KPI に置いている — the typical corporate-KPI layer
- **Industry-specific**: examples like **AIDMA** decomposition for marketing-relevant analyses

⚠ **Important caveat**: scaffolding patterns are aids; they are **not the goal**. Conformance to a scaffolding pattern does not mean the granularity is appropriate. The goal remains:

> **"自社差別化が捉えられる最高抽象度" (the highest abstraction at which your differentiation is captured)**

---

## Prompt-coach implications

When reviewing diagrams for granularity, the AI coach should:

1. **Run the industry-peer-discrimination test** as the first too-coarse check
2. **Watch for the subdivision-trap signs** (behavior chains, function enumerations) for too-fine
3. **For mixed**: walk through actor coherence → property coupling → natural-language reading
4. **Suggest scaffolding patterns** (UX / Business / industry-specific) as starting points, but **always reframe back to differentiation**:
   > 「この抽象度で、競合と区別がつきますか？ つかなければもう一段下げてみてください。」
5. **Never declare the verdict yourself** — return the test as a question for the user (`core.md` §9, §15)

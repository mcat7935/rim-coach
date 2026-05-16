# Core Principles of RIM

These principles are distilled from publicly available material and ongoing interviews with the methodology originator (Akitsugu Tsuchiya / Flying Penguins).

## 1. Structure has circulation (循環)

Any structure that "works" has a circulation — feedback loops, recurring cycles. RIM captures these as causal relationships, in measurable and reproducible form.

> "うまくいく構造には必ず循環があります。その循環を因果関係として捉え、計測し再現できる形にすること"
> — Akitsugu Tsuchiya, [note article](https://note.com/spice_factory/n/n42dfe43e2efb)

## 2. Three viewpoints, recursively integrated

RIM integrates three viewpoints — **UX (体験)**, **Business (事業)**, **Systemic / Technology (実装)** — by going back and forth ("Recursive") until they cohere.

> "UX × 事業 × 開発の3つの視点を、行ったり来たり（Recursive）しながら統合する"
> — RIM 公開勉強会 [announcement](https://spice-factory.co.jp/news/20158/)

## 3. Value chain / "core" visibility

The goal is to surface the value chain (バリュー・チェーン) and the "core" (キモ) of the business/service/product — what actually generates value.

> "何がこのサービス・事業の価値を生み出しているのかという『バリュー・チェーン』が明らかになり、事業やサービスの『キモ』となる部分を浮き彫りにします"

## 4. Relationships, not lists

Elements are integrated via relationships shown in diagrams, not via flat lists of items.

> "言葉ではなく図や関係性で整理"

## 5. Where RIM does NOT apply

Topics requiring interpretive room — values, culture, MVV (Mission/Vision/Values) — are better expressed in language than in structure.

> "価値観や文化のように解釈の余白が必要な領域、例えばMVVは言葉の方が適しています"

## 6. Review structure: 3 perspectives, with Systemic decomposed

When reviewing a RIM diagram, work through three perspectives **in this order**:

1. **Business (事業)** — does the author understand the *essence* of the business?
2. **UX (体験)** — is the *full psychological journey* captured (pre-use, during-use, post-use recall)?
3. **Systemic (テクノロジー)** — the hardest layer. Decompose further into three sub-layers:
   - **3a. 従業員としての人間 (Human as employee)** — is what to delegate to humans defined rigorously?
   - **3b. 会社が提供するシステム (Company-provided system, non-AI)** — what is made visible by the system? (Turing-machine + database, no autonomy)
   - **3c. 中間的特性: 疑似的な自主性をもつ AI (Intermediate-characteristic: pseudo-autonomous AI agent)** — are both (i) user-active use and (ii) agent-pull (AI proactively retrieving/acting) modes considered?

Only Systemic carries an internal three-layer decomposition. UX and Business do not, in this model.

> "UX, ビジネス、システミック（システミックだけは複雑）、その中に、従業員としての人間、会社が提供するシステム、そして、中間的特性（疑似的な自主性をもつAI）があるのだと。"
> — Akitsugu Tsuchiya, interview 2026-05-16

## 7. "Essential" = abstract + most-characteristic

When checking whether the author grasps the essence (especially at the Business layer):

- **"Understanding the essence"** = able to articulate the *most characteristic* and *abstract* statement about the business.
- **"Not understanding"** = enumerating user behaviors or system mechanics in a flat list.

> "もっとも特徴を表していて、かつ抽象的なことを言えてる人が本質的だと思っています。それに対してユーザーの行動とかシステムの挙動みたいなものをつらつらしゃべっている場合には、それはあまり本質的ではない。"
> — Akitsugu Tsuchiya, interview 2026-05-16

## 8. UX is the full psychological journey, not just UI

Most diagrams limit UX to "the moment of use" (UI / app interaction). RIM expects three regions to all be present:

- **Pre-use**: how the user's psychological state changes leading up to use
- **During-use**: UI experience (the usual scope)
- **Post-use**: how the user *recalls* and returns to the service

A diagram that captures only during-use is treating UX as fixed background rather than as a journey.

> "私はその利用後どうやって次思い出すか、や、その利用までに人間の心理状態でどういう変化が起きたかみたいなことを気にしながら UX を描くので、私自身はそういうものも含めてすべて UX だと思ってる。"
> — Akitsugu Tsuchiya, interview 2026-05-16

## 9. AI coaching discipline: hints, not answers — never judge abstraction

**Decisive design principle for any RIM-coaching AI**: do **not** judge whether a statement is "abstract enough" or "too concrete" yourself. Instead, ask the user to step back and decide for themselves:

> "もう少し抽象度を上げて、自社ビジネスにとって本質的か考えてみてください"

This preserves the human's ownership of the "last mile" of integrative judgment, which is where RIM's value lives. AI's job is to nudge with questions, not to declare verdicts.

> "AI 自身がそれが抽象的か具体的すぎるかみたいなことを判断してもらうというよりも、ユーザーに対して『あなたはもう少しそれを抽象度を上げて、かつ自分のところのビジネスにとって本質的かどうか』みたいなことを質問してもらう、っていうのは AI コーチングとして非常に有用だと思いました。"
> — Akitsugu Tsuchiya, interview 2026-05-16

## More to come (interview in progress)

Still being developed via interview:

- Circulation detection criteria
- Causal-relationship vs. mere-arrow distinction
- "Positive → Positive → Negative" innovation pattern detection
- Layout judgment (visual hierarchy, center-of-perspective transmission)
- Granularity calibration (too coarse / too fine / mixed)
- "Core (キモ)" presence judgment

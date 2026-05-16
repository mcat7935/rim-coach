# Interview Questions Used to Develop rim-coach Prompts

These are the questions used to elicit RIM observation criteria from the methodology originator (Akitsugu Tsuchiya). Documented here so that:

- Contributors can apply the same framework when adding new principles
- The provenance of each principle in `principles/core.md` is traceable
- The questions can serve as a coaching template for other practitioners eliciting their own structural-design observation criteria

## Primary questions (10)

These were designed to cover what is **not** publicly documented in talks and articles, and to land on judgment criteria operational enough for an LLM to apply.

| # | Question | Aim |
|---|---|---|
| 1 | RIM 図のレビューを頼まれたとき、最初にどこを見ますか？ 順番で教えてください | Review priority order |
| 2 | 「循環がある図」と「循環がないけど似ている図」の区別はどうつけますか？ | Circulation detection |
| 3 | 「因果関係として描けている」図と「ただ矢印が引いてあるだけ」の図の見分け方は？ | Causal-relationship distinction |
| 4 | UX × 事業 × 開発の3視点統合が「不十分」と感じるのはどんな図ですか？ よくあるパターンで | Integration sufficiency check |
| 5 | 「ポジティブ → ポジティブ → ネガティブ（革新要素）」の判定方法を具体的に教えてください。良い例・悪い例があると助かります | Innovation-pattern detection |
| 6 | レイアウトが「視点中心の伝達」になっている／いない、の見分け方は？ | Layout judgment |
| 7 | 粒度が「適切」「粗すぎ」「細かすぎ」「混在」の判定基準は？ よくある「粒度が崩れている図」のパターンも | Granularity calibration |
| 8 | 初挑戦者・初学者がやりがちな失敗パターン TOP 5 は？ | Anti-patterns |
| 9 | 「これはもう構造で扱うべきじゃない（言葉のほうがいい）」と判断するのはどんなとき？ | Applicability boundary |
| 10 | 「キモ（バリューチェーンの核心）」が描けているか／描けていないか、を判定する方法は？ | "Core" presence judgment |

## Follow-up question pattern

For each primary answer, ask up to 3 deepening follow-ups, prioritized by what makes the principle operational for an LLM (i.e., turns a felt-sense judgment into something codifiable).

Example from interview 2026-05-16:

- **Q1 (primary)**: Review priority order
  - **Q1-a**: 「本質的な部分をわかっている／わかっていない」の見分け方は具体的に何ですか？
  - **Q1-b**: 「AI をどう活用するか明確化されているか」とは、具体的にどういう状態を指しますか？
  - **Q1-c**: UX で「着目できていない」と気づくサインは何ですか？

## Discipline when interviewing

- **Cover only what is NOT publicly documented.** Read the public material first; don't waste the originator's time.
- **Use text-displayed questions and voice-input answers** when possible (matches the interviewee's natural mode for long-form articulation).
- **One question at a time**; let the interviewee digress.
- **Confirm understanding by summarizing back in structured form**; flag where interpretation may diverge.
- **Do not push for closure on a single answer** — multiple alternative formulations are valuable.
- **Record verbatim quotes** when the wording itself is the principle (the originator's own phrasing often carries the methodology's spirit).

## Status of interview-derived content

| Question | Status | Reflected in |
|---|---|---|
| 1 (priority) + 1a/1b/1c | ✅ 2026-05-16 | `core.md` §6–9, `anti-patterns.md` §1–3, `review.md` Checks B/C/D |
| 2 (circulation) | ✅ 2026-05-16 (false-negative via autonomous agents, false-positive via sentence-coherence) | `review.md` Check G, `quality-check.md`, `anti-patterns.md` §5c/5d |
| 3 (causal) | ✅ 2026-05-16 (same test as Q2 false-positive) | `review.md` Check G-a |
| 4 + 5 (integration + innovation pattern) | ✅ 2026-05-16 — unified topic: mountain-range + canyon + variants + negative-loop response. Includes Tsuchiya RIM, Motomura variant, era criterion, Othello-endgame anti-pattern, all-positive anti-pattern, partial-knowledge accommodation, last-mile leap as human's territory | `core.md` §10–14, `variants.md`, `negative-loop-response.md`, `quality-check.md`, `anti-patterns.md` §4–5, `review.md` Checks A/E/F/H/I |
| 6 (layout) | **deferred to dedicated session** (Tsuchiya identified Q6 as the hardest — involves tool selection, XY-coordinate aesthetic judgment, loop-shape perceptibility, multiple human-sense decisions) | — (pending Q6 session) |
| 7 (granularity, a/b/c/d + scaffolding) | ✅ 2026-05-16 (first-pass / 一次回答) — granularity = abstraction level for competitive differentiation; industry-peer-discrimination test (楽天 vs Amazon), subdivision-trap (細分化の罠), actor coherence + NL naturalness for mixed; scaffolding patterns (UX/Business/AIDMA) | `core.md` §16, `granularity.md`, `review.md` Check K |
| 8 (anti-patterns) | ✅ 2026-05-16 (first-pass) — 3 named patterns: behavior chains without causation, SE/logical paralysis (要素列挙詰まり), single-correct-form belief (唯一正解信仰) | `anti-patterns.md` §7 (mindset traps), `starter.md` |
| 9 (applicability) refined | ✅ 2026-05-16 — refined from public-material baseline: criterion is purpose (意志統一 vs 解釈発散), not subject matter; design domain further split (aesthetic via language+意匠, operational rules OK with hierarchical structure) | `core.md` §17, `review.md` Check L |
| 10 (core / キモ) | ✅ 2026-05-16 — the **decisive** answer of the entire interview: success = inner revelation in stakeholders ("あ、本当は我々はこれを目指してたんだ" = 脳内革命 = English-sense innovation); cannot be judged by AI; this is the **ultimate ground** for all AI-coaching disciplines | `core.md` §15 (decisive top), `review.md` ultimate goal section |

## Outstanding minor items (transcription confirmations)

A few voice-input words from the 2026-05-16 interview have ambiguous Japanese transcriptions to confirm with the originator before final publication:

- **「ミンシン」** (Q7-d about actor decomposition): likely 「ちゃんと」 / 「明確に」 / 「綺麗に」 — TBD
- **「核のシーン」** (Q10 about the kind of revolution): likely 「過激なシーン」 or 「革命的なシーン」 — TBD

## Derivative insights (from interviewer's questions back to the originator)

Mid-interview the originator asked a methodologically generative question:

> 2026-05-16: 「こじつけストーリーと蓋然性のあるストーリーを AI 的に見分ける方法論はあるか？」

The discussion produced the five plausibility-check techniques and the mille-feuille flow now codified in `principles/quality-check.md`. Future interviews may include this kind of **reverse-question** pattern, where the originator stress-tests AI implementability of their own methodology in real time.

## Contributors referenced

- **Akitsugu Tsuchiya** (Flying Penguins, CEO) — methodology originator
- **Akira Motomura** (Flying Penguins) — contributor; developed the inductive negative-cycle variant documented in `principles/variants.md` §2, and the procedural systematization aspiration

## Source material consulted before interview

- [「構造で世界は変えられる」 note.com](https://note.com/spice_factory/n/n42dfe43e2efb) — Tsuchiya interview by Spice Factory
- [RIM 公開勉強会 announcement (spice-factory)](https://spice-factory.co.jp/news/20158/)
- [コンセプト作りとプロト検証は同時並行 (popinsight)](https://popinsight.jp/blog/?p=89788)
- [Flying Penguins 公式](https://penguins.jp/)
- [新規事業開発、最初にまずここで躓く！土屋晃胤氏編 (unicornfarm)](https://unicornfarm.jp/past-seminar-2566)

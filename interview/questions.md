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
| 1 (priority) + 1a/1b/1c | ✅ 2026-05-16 | `principles/core.md` §6–9, `prompts/review.md`, `principles/anti-patterns.md` §1–3 |
| 2 (circulation) | pending | — |
| 3 (causal) | pending | — |
| 4 (integration) | partially via Q1 follow-ups | `principles/core.md` §6 |
| 5 (innovation pattern) | pending | — |
| 6 (layout) | pending | — |
| 7 (granularity) | pending | — |
| 8 (anti-patterns) | partially via Q1 follow-ups | `principles/anti-patterns.md` |
| 9 (applicability) | covered by public material | `principles/core.md` §5 |
| 10 (core / キモ) | pending | — |

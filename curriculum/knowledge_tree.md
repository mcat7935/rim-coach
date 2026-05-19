# RIM 全知識体系ツリー (v1.1)

> **Canonical source notice (2026-05-19)**
> このファイルは、**RIM 知識体系全体に関する正典 (canonical source)** です。用語・命名・概念分類の最終決定はこのツリーに従います。**ノウハウの集約先**もここ — 各 K.* ノードに本文を蓄積していく方針 (2026-05-19 〜)。
> 理論的議論・引用・出典は `principles/*.md` に残す (理論バックエンド)。
> 過去の研修プログラム草案は `curriculum/drafts/` にアーカイブ済み (現在凍結)。
> 用語衝突が起きた場合: **このファイル > `principles/*.md`** が優先。

---

## ツリーの読み方

- 各ノードは **安定 ID** を持つ (例: `K.PER.UX.Cycle`)
- `K` = Knowledge プレフィクス、続く 2-3 階層は意味略号
- 1 ノード = 本文 (定義 + 例 + 教え方の勘所) + `principles/*.md` への参照
- 現状 (v1.1) はまだサマリ中心。各ドメインを段階的に肉付け中

### 領域略号 (12 ドメイン)

| 略号 | 領域 | 主参照 |
|---|---|---|
| **K.MOT** | Motivation — 動機・世界観 | core.md §1-2, §14 |
| **K.THE** | Theory — 理論的系譜 | theoretical-background.md |
| **K.NOT** | Notation — 表記法・3要素 | notation.md |
| **K.PER** | Perspectives — 3視点と Value Cycle | core.md §6, §20 |
| **K.STG** | Stages — 3 ステージ (RsIM / SDIM / BSM) | three-stages.md, core.md §19 |
| **K.QLY** | Quality — 粒度・蓋然性・チェック | granularity.md, quality-check.md |
| **K.LAY** | Layout — レイアウト原則 | layout.md |
| **K.VAR** | Variants — 山脈・峡谷・流派 | variants.md, negative-loop-response.md |
| **K.APP** | Applicability — 適用境界 | core.md §17 |
| **K.ANT** | Anti-patterns — アンチパターン | anti-patterns.md |
| **K.AIC** | AI Collaboration — AI 協働の規律 | core.md §9, §12, §15 |
| **K.PSY** | Psychology — ユーザー心理プロパティ | (新規) |

---

## 体系図 (Map of the Tree)

ノード詳細に入る前の俯瞰図。**A**: 何がどこにあるか (階層)、**B**: ドメイン間がどう繋がるか (関係)。

### A. 階層タクソノミ図

```
RIM Knowledge Tree (12 ドメイン)
│
├── K.MOT  動機・世界観  ............ なぜ構造で考えるのか
│   ├── Structure / Cycle / Kakushin (本質トリオ)
│   └── MMA / Era / Uber (時代論トリオ)
│
├── K.THE  理論的系譜  .............. Simon → Krippendorff → DesEnable → SecondOrder
│
├── K.NOT  表記法・3 要素  .......... Actor / Property / Arc
│   ├── Property [Driver / Result]
│   ├── 記法: SHave / SVO / PropVsAction
│   ├── 手順: Standard / Simple
│   └── NG: WrongNode / TooFree / Bloat
│
├── K.PER  3 視点と Value Cycle  .... UX / Business / Systemic
│   ├── UX  [Cycle (満足向上) / Phases (利用前・中・後想起) / Design]
│   ├── BIZ [Cycle (成長) / Phases (調達・選定・使い方) / Design]
│   ├── SYS [Cycle (強化) / Human / IT / AI / Design]
│   └── 共通: Crit (批判的考察) / Exchange (三層交換構造)
│
├── K.STG  3 ステージ  .............. RsIM → SDIM → BSM
│   ├── Overview / StanceBase (派手さと姿勢のベース)
│   ├── RsIM [Stance×4 (蓋然性/視点切替/統合/漸近) / CoreLoop / AnyStart]
│   ├── SDIM [Phenomenon / Wall / Kakushin / Analogy / Inclusive / LastMile / FourTraditions]
│   └── BSM  [Purpose / 5Elements / LLMAffinity / Scope]
│
├── K.QLY  品質  .................... 粒度・蓋然性・ミルフィーユ
│   ├── Granularity [Ideal / PeerTest / SubdivisionTrap / MECE / Mixed]
│   ├── Plausibility [FiveTechniques]
│   ├── MilleFeuille (AI ↔ 人間)
│   └── Expert (相談規律)
│
├── K.LAY  レイアウト  .............. XY / LoopVisibility / Shape / Density / Symmetry / Tool / ArrowSemantics
│
├── K.VAR  変形・流派  .............. 山脈・峡谷 + 2 流派
│   ├── Mountain / Canyon / Innovation
│   └── Schools: Tsuchiya / Motomura / Coexist
│
├── K.APP  適用境界  ................ Alignment / Divergence / Brand / Guidelines / MVVRefined
│
├── K.ANT  アンチパターン  .......... Business / UX / Systemic / Process / Loop / AI / Mindset
│
├── K.AIC  AI 協働の規律  ........... Hints / LastMile / RevelationCondition / MilleFeuille / CoachNotGen
│
└── K.PSY  心理プロパティ  .......... (K.PER.UX.Design の深掘り)
    ├── PropType [Expectation / Anxiety / Fulfillment / Recall]
    ├── Prop [Drv / Res / Pattern]
    ├── Theory [Potential / Drive]
    └── Discovery [FourQ / AntiBehavior]
```

### B. ドメイン関係図

```
                                            ┌─ K.APP (どこに使うかの境界判定)
                                            │
[K.MOT] ──導入→ [K.NOT] ──→ [K.PER] ──→ [K.STG]
動機              表記         3 視点         3 ステージ
                    │             │              │
                    │             │      RsIM (姿勢) ─支える→ SDIM (飛躍) ─→ BSM (伝達)
                    │             │              │
                    │     [K.PSY] ←深掘り← K.PER.UX.Design
                    │       (心理プロパティ)
                    │
                    ├─ [K.LAY] 図の可視化
                    └─ [K.VAR] 山脈・峡谷 (応用形)

横断する規律 (任意ノードに作用):
  [K.QLY]  品質チェック (粒度・蓋然性・ミルフィーユ)
  [K.AIC]  AI 協働 (ヒント / ラストワンマイル / 核心条件)
  [K.ANT]  失敗モードの反例
  [K.THE]  理論的バックエンド (なぜ正しいか)
```

**読み方のコツ**:
- **左→右の主軸**: 動機 (なぜ) → 表記 (どう書く) → 視点 (何で見る) → ステージ (どう進める)
- **下方向の深掘り**: K.PER.UX.Design → K.PSY (心理) のように、上位概念の実装詳細が下位に展開
- **横断ドメイン**: K.QLY / K.AIC / K.ANT / K.THE は特定の流れを持たず、任意のノードに当たる規律・反例・理論

---

## K.MOT 動機・世界観

なぜ言語や箇条書きではなく「構造」なのか。RIM が答えようとしている問いの集合。

- **K.MOT.Structure** — 構造で世界は変えられる: 関係性の図が思考と意思決定の道具になる根本主張 → `core.md` §1
- **K.MOT.Cycle** — 循環の原則: 循環がある構造だけが「上手く行き続ける」(自律持続性) → `core.md` §1
- **K.MOT.Kakushin** — 核心/革新/確信の予告: 関係者の脳内革命を起こすことが RIM の到達点 → `core.md` §15
- **K.MOT.MMA** — 総合格闘技時代論: 1970-80s (技術単独) → iPhone 期 (UX 単独) → 2020s (UX×Business×Systemic 統合必須) → `core.md` §14
- **K.MOT.Era** — 「現代において」基準: 前提が旧時代の単一視点か、統合時代に耐えるか → `core.md` §14
- **K.MOT.Uber** — Uber ケース: なぜ UX だけでは戦えないか (UX × 収益機構 × ドライバー基盤のセット必要) → `core.md` §14

---

## K.THE 理論的系譜

RIM は誰の系譜の上に立つか。

- **K.THE.Simon** — Simon (1969) 設計の定義: 設計 = 状態遷移 → `theoretical-background.md`
- **K.THE.Krippendorff** — Krippendorff のプロジェクト概念: ナラティブ駆動の参加型設計 → `theoretical-background.md`
- **K.THE.DesEnable** — Design Enablement (FP/SF orbit): Pulling / Pushing / Demonstrating 組織モデル → `theoretical-background.md`
- **K.THE.SecondOrder** — Motomura のセカンドオーダーサイバネティクス読解: SDIM をナラティブ再方向化と読む → `theoretical-background.md`, `variants.md`

---

## K.NOT 表記法・構造要素

RIM 図を書くための語彙と手順。

### 3 要素
- **K.NOT.Actor** — Actor (S): 人・組織・擬人化された製品。楕円で表す → `notation.md`
- **K.NOT.Property** — Property (O): アクターに付随する状態属性。**RIM の分析単位** → `notation.md`
- **K.NOT.Property.Driver** — 駆動プロパティ: 循環の起点となる属性 (需要・期待など) → `notation.md`
- **K.NOT.Property.Result** — 結果プロパティ: 循環の結果として動く属性 (満足度・信頼など) → `notation.md`
- **K.NOT.Arc** — Arc (作用): Property → Property の伝搬 → `notation.md`

### 記法
- **K.NOT.SHave** — `S have O` 記法 (アクターは属性を持つ)
- **K.NOT.SVO** — `S V O` 記法 (属性が属性に作用)
- **K.NOT.PropVsAction** — 作用 vs アクション: 連続的・自動的 vs 離散的・意図的 → `notation.md`

### 手順
- **K.NOT.Standard** — 標準型手順 (構造的探索重視): Actor→Property→作用→蓋然性チェック→循環発見 → `notation.md`
- **K.NOT.Simple** — シンプル型手順 (ゴール速度重視): アクション + 望ましい状態変化の列挙→接続→循環発見→蓋然性チェック → `notation.md`

### NG パターン (記法レベル)
- **K.NOT.NG.WrongNode** — ノード選択誤り (ad-hoc 理論化)
- **K.NOT.NG.TooFree** — 自由すぎて入口不在
- **K.NOT.NG.Bloat** — 詳細肥大

---

## K.PER 3視点と Value Cycle

3 つの視点と、それぞれの循環。

### K.PER.UX  UX (体験) 視点
- **K.PER.UX.Cycle** — UX 満足向上循環: 静的な満足ではなく能動的に向上させる循環 (※命名は 2026-05-19 で「満足循環」→「満足向上循環」に更新)
- **K.PER.UX.Phases** — 3 フェーズ整理: 利用前 / 利用中 / 利用後想起 → `core.md` §8
- **K.PER.UX.Design** — UX デザイン (心理・行動的循環): 一般成功モデルを批判的に考察し、本ケース固有の連鎖を作る

### K.PER.BIZ  Business (事業) 視点
- **K.PER.BIZ.Cycle** — Business 成長循環
- **K.PER.BIZ.Phases** — 資金調達 (稼ぎの再投資含む) / 投資対象選定 / 有効なお金の使い方プロセス
- **K.PER.BIZ.Design** — Business デザイン (ビジネス成長循環): 標準モデルを本ケースに合わせ再構成

### K.PER.SYS  Systemic (実装) 視点
- **K.PER.SYS.Cycle** — 自己強化循環 (Self(-Organization) Reinforcement Cycle) ※2026-05-19 で「成長循環」→「強化循環」に更新。旧称: Product Evolution Cycle
- **K.PER.SYS.Human** — 従業員としての人間: 自律 (非決定論) 的循環
- **K.PER.SYS.IT** — 会社が提供する IT システム: アルゴリズム (フローチャート / 決定論) 的フロー。単体では循環しない
- **K.PER.SYS.AI** — 疑似的自主性をもつ AI エージェント: 人間とシステムの中間的挙動をする LLM + ハーネスの設計論
- **K.PER.SYS.Design** — Systemic デザイン: 3 要素 (人 + IT + AI) の組み合わせで循環を成立させる設計論

### K.PER 共通
- **K.PER.Crit** — 「批判的考察 → 本ケース固有の連鎖」共通方法論: 各層で標準成功モデルをそのまま採用せず再構成
- **K.PER.Exchange** — 三層交換構造: Market (価値⇄収益) / Service (情報⇄リソース) / Organization (役割⇄報酬) → `notation.md`

---

## K.STG 3 ステージ (RsIM / SDIM / BSM)

RIM の運用フェーズ構造。

### K.STG.Overview  3 ステージ全体像
- **K.STG.Overview** — RsIM (構造を作る) → SDIM (構造を超える) → BSM (構造を伝える) → `three-stages.md`
- **K.STG.StanceBase** — 「派手さ」と「姿勢のベース」: SDIM / BSM が見せ場だが、姿勢のベースは RsIM (本講義の核)

### K.STG.RsIM  RsIM (分析/発想)
- **K.STG.RsIM.Stance** — RIM 実践者のワーキング姿勢: 中核循環は姿勢が外形化したもの
  - **K.STG.RsIM.Stance.Plausibility** — 蓋然性を常に疑う
  - **K.STG.RsIM.Stance.Switch** — 視点を躊躇なく切り替える (UX/Business/Systemic を往復)
  - **K.STG.RsIM.Stance.Integrate** — 別視点モデルを元モデルに統合する
  - **K.STG.RsIM.Stance.Asymptotic** — 漸近的・持続的に改善する (一発で正解を出さない)
- **K.STG.RsIM.CoreLoop** — 中核循環: 初期モデル→蓋然性検出→視点切替→統合→漸近改善→循環 → `core.md` §10
- **K.STG.RsIM.AnyStart** — 「出発点はどこでもよい」: UX 先行教義の否定。常識的には Business 起点が問いを生みやすい → `core.md` §11

### K.STG.SDIM  SDIM (発想/飛躍)
- **K.STG.SDIM.Phenomenon** — SDIM は現象であってメソッドではない → `three-stages.md`
- **K.STG.SDIM.Wall** — 演繹的発想の壁: RsIM の積み上げでは到達不能な領域
- **K.STG.SDIM.Kakushin** — 脳内革命 / 核心 / カクシン (3 つの同音語) → `core.md` §15
- **K.STG.SDIM.Analogy** — アナロジー思考: 他領域からの構造的類比
- **K.STG.SDIM.Inclusive** — インクルーシブ思考: 視点を包摂する統合的視座
- **K.STG.SDIM.LastMile** — ラストワンマイル原則: 飛躍は人間に残される → `core.md` §12
- **K.STG.SDIM.FourTraditions** — 同一現象の 4 つの呼び名: 土屋「脳内革命」/ 本村「セカンドオーダー飛躍」/ Krippendorff「ナラティブ再定義」/ RIM 公式「演繹的発想の壁を超える」

### K.STG.BSM  BSM (伝達)
- **K.STG.BSM.Purpose** — 経営層・投資家・関係者への伝わる言語への変換 → `three-stages.md`
- **K.STG.BSM.FiveElements** — 5 要素: 何を / どう / 価値 / なぜ (MVV 接続) / 永続化
- **K.STG.BSM.LLMAffinity** — LLM 親和性: ナラティブ生成は AI 得意領域
- **K.STG.BSM.Scope** — rim-coach は対象外、将来 `rim-bsm` 別スキル化

---

## K.QLY 品質・粒度・チェック

RIM 図の品質をどう測り改善するか。

### K.QLY.Granularity  粒度 = 抽象度 = 競合差別化
- **K.QLY.Granularity.Ideal** — 「競合差別化された強みが表現される範囲でもっとも抽象的な状態」 → `core.md` §16, `granularity.md`
- **K.QLY.PeerTest** — 業界他社識別テスト: 楽天 vs Amazon が同じ図になる = NG
- **K.QLY.SubdivisionTrap** — 細分化の罠: 行動列挙 / 機能羅列 / UI 操作列挙
- **K.QLY.MECE** — MECE 配置: アクター分解が MECE であること
- **K.QLY.Mixed** — 混在 (最も難しい): 文章として自然な日本語にならない

### K.QLY.Plausibility  蓋然性チェック
- **K.QLY.Plausibility.FiveTechniques** — 5 つの蓋然性チェック技法 → `quality-check.md`
- **K.QLY.MilleFeuille** — ミルフィーユフロー: AI 構造化 ↔ 人間レイアウト ↔ AI 補完 ↔ 人間判断 → `quality-check.md`
- **K.QLY.Expert** — エキスパート相談規律: AI は判断を下さず専門家相談を促す

---

## K.LAY レイアウト

図を「見える」状態にするための原則。

- **K.LAY.XY** — XY 軸意味論: X = 時間/流れ、Y上 = 抽象度高/原因側 → `layout.md`
- **K.LAY.LoopVisibility** — 循環可視性の決定的慣習: 太線 + 暖色 (オレンジ・赤) vs 細線 + 寒色 (背景因果)
- **K.LAY.Shape** — ループ形状は二次的 (可視性 > 形状)
- **K.LAY.Density** — 密度と成熟度: 試行錯誤期はスパース / 仕上げ期はタイト / 常に 1 画面
- **K.LAY.Symmetry** — シンメトリーは不要、ただし業界パターン類似は理解を助ける
- **K.LAY.Tool** — ツール選定: Miro 推奨 / FigJam 可 / Mermaid は構造列挙のみ
- **K.LAY.ArrowSemantics** — 矢印意味論は学習過程: 作用/反作用の精密化は熟練の領域

---

## K.VAR 山脈・峡谷・流派

漸近的イノベーションの構造化と、2 つの流派。

### K.VAR.Mountain  マウンテンレンジ
- **K.VAR.Mountain** — 山脈モデル: 強み (山頂) の連峰として循環を描く → `negative-loop-response.md`
- **K.VAR.Canyon** — 峡谷モデル: positive→positive→negative の negative の正体 = 2 つの山頂を繋ぐべき欠落した接続 → `core.md` §13
- **K.VAR.Innovation** — イノベーション = 峡谷を見つけて橋を架けること

### K.VAR.Schools  2 つの流派
- **K.VAR.Tsuchiya** — Tsuchiya 式: 山脈 + 峡谷 (positive 循環起点) → `variants.md`
- **K.VAR.Motomura** — Motomura 帰納式: ネガティブサイクル → 反転点探索 (オセロ的反転) → `variants.md`
- **K.VAR.Coexist** — 共存と使い分け: 漸近的か飛躍的か、組織の現状理解度で選ぶ

---

## K.APP 適用境界

RIM が向くテーマと向かないテーマ。

- **K.APP.Alignment** — 意志統一が目的 → RIM (構造) → `core.md` §17
- **K.APP.Divergence** — 解釈発散が目的 → 言語
- **K.APP.Brand** — ブランド (aesthetic / look & feel) = 言語 + 意匠の直接接続
- **K.APP.Guidelines** — ブランドガイドライン (運用ルール) = 階層構造 (RIM 的 OK)
- **K.APP.MVVRefined** — §5 公開素材の精緻化: 主題ではなく目的で線を引く

---

## K.ANT アンチパターン

典型的な失敗モードのカタログ。

- **K.ANT.Business** — ユーザー行動 / システム挙動の羅列 → `anti-patterns.md`
- **K.ANT.UX** — UI / 利用中だけの UX、心理的ジャーニー不在
- **K.ANT.Systemic** — 人 / システム / AI の役割境界不在
- **K.ANT.Process.ResearchFirst** — 課題仮説なしのユーザーリサーチ先行 → `core.md` §11
- **K.ANT.Loop.Static** — 循環が見えない、静的構造
- **K.ANT.AI.JudgeAbstraction** — AI が抽象度を判断する → `core.md` §9
- **K.ANT.AI.GenerateLeap** — AI が飛躍を生む → `core.md` §12
- **K.ANT.Mindset.Perfectionism** — 完璧主義 (一発正解志向)
- **K.ANT.Mindset.ToolFirst** — ツール先行

---

## K.AIC AI 協働の規律

`rim-coach` の設計思想の核。

- **K.AIC.Hints** — ヒント、答えではない: AI は抽象度を判定せず、本人に問い返す → `core.md` §9
- **K.AIC.LastMile** — ラストワンマイル: 飛躍は人間の領域 → `core.md` §12
- **K.AIC.RevelationCondition** — AI は脳内革命の「条件を整える」だけ → `core.md` §15
- **K.AIC.MilleFeuille** — ミルフィーユパターン: AI ↔ 人間の交互レイヤリング
- **K.AIC.CoachNotGen** — コーチであってジェネレーターではない: バリデーター/ジェネレーター志向の否定

---

## K.PSY ユーザー心理プロパティ

`K.PER.UX.Design` を深掘りした心理駆動の語彙体系 (`programs/user_psychology_90min.md` の素材)。

### K.PSY.PropType  心理プロパティの種類
- **K.PSY.PropType.Expectation** — 期待・欲求系 (期待値 / 欲求 / 関心 / 興味)
- **K.PSY.PropType.Anxiety** — 不安・障壁系 (不安感 / 抵抗感 / 面倒さ)
- **K.PSY.PropType.Fulfillment** — 充足・確信系 (達成感 / 満足度 / 信頼 / 安心感)
- **K.PSY.PropType.Recall** — 想起・継続系 (記憶の鮮明さ / 再利用意向 / 推奨意向)

### K.PSY.Prop  駆動と結果
- **K.PSY.Prop.Drv** — 駆動プロパティ: 循環の起点となる心理 (欲求 / 期待 / 関心 / 不安)
- **K.PSY.Prop.Res** — 結果プロパティ: 他の変化の結果として動く心理 (満足度 / 信頼 / 達成感 / 再利用意向)
- **K.PSY.Prop.Pattern** — 基本パターン: 駆動↑ → 行動 → 結果↑ → 次サイクルの駆動↑

### K.PSY.Theory  理論的補助
- **K.PSY.Potential** — 位置エネルギー比喩: 心理が「高い位置」にあると次の行動が自然に起きる
- **K.PSY.Drive** — 心理駆動ループ vs 行動チェーン: ループを「回す力」は心理プロパティの変化にある

### K.PSY.Discovery  発見の問い
- **K.PSY.FourQ** — 心理プロパティ発見 4 つの問い (利用前 / 利用中 / 利用後 / 次のサイクルへ)
- **K.PSY.AntiBehavior** — 行動 (検索する / 買う) で書かず、心理状態 (期待する / 信頼する) で書く

---

## クロスリファレンス: `principles/*.md` から K.* への対応

| principles/ ファイル | 主に対応する K.* 領域 |
|---|---|
| `core.md` | K.MOT, K.PER, K.STG, K.QLY, K.AIC, K.APP |
| `notation.md` | K.NOT, K.PER.Exchange |
| `three-stages.md` | K.STG (全体) |
| `granularity.md` | K.QLY.Granularity, K.QLY.PeerTest |
| `quality-check.md` | K.QLY.Plausibility, K.QLY.MilleFeuille |
| `layout.md` | K.LAY |
| `variants.md` | K.VAR.Schools |
| `negative-loop-response.md` | K.VAR.Mountain, K.VAR.Canyon |
| `anti-patterns.md` | K.ANT |
| `theoretical-background.md` | K.THE |

---

## バージョン履歴

- **v1.0 (2026-05-19)**: 初版。旧 `lecture_outline_v0.1.md` + `user_psychology_lecture_v0.1.md` を分解して構築。12 ドメイン × ~120 ノード。

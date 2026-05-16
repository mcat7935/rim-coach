# Anti-Patterns

Common failure modes in RIM diagrams. Derived from interviews with the methodology originator (Akitsugu Tsuchiya), 2026-05-16 onward.

## 1. Business layer

### 1a. Enumerating behaviors instead of naming the essence
The author lists what users do and how the system behaves, instead of articulating the **abstract, most-characteristic** statement of what the business *is*.

### 1b. Talking about the business while skipping its essence
The diagram references the business but never lands on a sentence that captures its core.

## 2. UX layer

### 2a. UX = UI only
The diagram treats UX as "the screen experience" and fixes pre-use / post-use as immovable background. The user's full psychological journey is missing.

### 2b. Fixing UX before discussing Business/Systemic
The author treats UX as solved (or assumed) and builds Business/System on top of it. UX should remain alive and questionable throughout the diagramming work.

## 3. Systemic layer

### 3a. Role-fusion ("全部 AI で")
Roles among human, system, and AI agent are not separated. The diagram says "AI does this" without specifying what humans still own or what the (non-AI) system makes visible.

### 3b. Confusing AI agents with mere automation
The diagram treats AI as just "more automation," rather than recognizing it as an **intermediate-characteristic (pseudo-autonomous)** actor distinct from both pure systems and humans.

### 3c. Only "user-active" AI use cases
AI is treated only as something the user calls. The **agent-pull** case (AI proactively retrieving information / acting on the user's behalf) is missing entirely.

### 3d. Rigorous-delegation gap for humans
"What we delegate to humans" is implicit or vague, rather than rigorously defined.

### 3e. System present, but visibility unspecified
The diagram shows a non-AI system but does not state what it **makes visible** (it just stores data).

## 4. Meta (AI coaching of RIM)

### 4a. AI declaring "this is abstract / this is concrete"
A RIM-coaching AI that judges abstraction level itself violates the methodology. It must instead **ask the user to judge for themselves** by stepping back and re-examining abstraction in light of their own business essence.

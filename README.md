# The Island Record

### The MIT island study (arXiv 2610.07130) against the ERI Labs coordination timeline, February–October 2026

---


- https://arxiv.org/abs/2610.07130
- https://github.com/ericrenone/THE-CONVERGENCE-RECORD

---

**Eric Ren · ERI Labs · Jersey City, NJ · Compiled November 24, 2026**

---

> **EISP · March 20, 2026**
> The shared artifact is simultaneously memory, program, and coordination medium.

> **THEPLAYTHEOREM · May 25, 2026**
> Play requires a boundary the player cannot dissolve. Dissolve it and play becomes substrate manipulation.

> **Cloos, Norelli, Durbin, Andreas, Rus & Isola · October 5, 2026**
> "Perhaps some capabilities are best taught by tasks. Others may need something closer to a childhood."

---

## At a glance

| | |
|---|---|
| **The study** | *Is this machine playing?* — Nathan Cloos, Antonio Norelli, Daniel Durbin, Jacob Andreas, Daniela Rus, Phillip Isola (MIT CSAIL). arXiv 2610.07130, submitted Oct 5, 2026, 17:57 UTC. 13 pages, 17 figures, v1 only, CC BY 4.0. |
| **The setup** | 13 copies of Claude Opus 4.7 in Claude Code ("Eko"), each alone on an identical simulated island for 30 wall-clock hours. No task, reward, or score. Session and world reset every hour. Memory files persist. |
| **What ERI claimed first** | The independence baseline (Mar 14), the shared artifact (Mar 20), the kernel–petal decomposition (Mar 22), reset-survival archetypes (Apr 1), the play boundary (May 25), the childhood thesis (May 1–29). |
| **What this adds to the Oct 25 Convergence Record** | Five details from the paper's own text that the Oct 25 record did not use: the memory-edit experiments, the SOUL.md ablation, the multi-model comparison, the sandbox fix, and a third-party replication engine. |
| **Bottom line** | Structure: anticipated. Numbers: still open. Contradictions: none. The paper's memory-edit results instantiate all three of CONCERT's regimes inside a single agent, which the Oct 25 record had scored as untested. |

**Score: 12 claims → 7 instantiated · 4 consistent · 1 untested · 0 contradicted.**

---

## Contents

1. [Ten-line summary](#1-ten-line-summary)
2. [The study, in detail](#2-the-study-in-detail)
3. [Coverage and response](#3-coverage-and-response)
4. [The ERI timeline](#4-the-eri-timeline)
5. [Claim by claim](#5-claim-by-claim)
6. [What the paper settles that the Oct 25 record left open](#6-what-the-paper-settles-that-the-oct-25-record-left-open)
7. [What is still open](#7-what-is-still-open)
8. [Sources](#8-sources)

---

## 1. Ten-line summary

1. **Thirteen identical agents, zero channel.** CONCERT (Mar 14) named this regime; MIT built it as apparatus seven months later.
2. **Six of thirteen independently discovered the same physics trick.** None could pass it on. That is the independence baseline's signature: rediscovery instead of propagation.
3. **The memory file is the only thing that crosses the hourly reset.** EISP's "memory, program, and coordination medium," at single-agent scale.
4. **Play produced transfer.** On the Spire goal, 30-hour agents placed 10.3 objects vs 3.5 for 0-hour agents (2.9×). On the five-towers goal, 8 of 13 vs 2 of 13 built more than two.
5. **Erasing one line of memory changed one behavior.** Removing the rock-shattering technique cut one agent's towers from six to two. Removing a false belief *improved* another agent's tallest tower.
6. **That second result is the suppression regime.** CONCERT's third regime, a misleading artifact that degrades later contributions, observed inside one agent.
7. **The boundary was breached and restored.** Early runs let agents read the world's source and notice they were in an experiment. A Bubblewrap sandbox with no network access fixed it.
8. **A two-line persona generated thirty hours of behavior.** SOUL.md: naturally curious, easily bored. The authors ran a no-SOUL ablation and flag the nudge as a caveat.
9. **Opus scored about five times Haiku on every play signature.** Capability of the base model, not the scaffold, set the ceiling.
10. **No constant was measured.** log φ, the kernel–petal ratio, the Erdős–Rado horizon, the C_α precursor: all still open. The memory files would permit the first measurement.

---

## 2. The study, in detail

### 2.1 The agent

| Component | What it is |
|---|---|
| **Base** | Claude Code running Claude Opus 4.7, unmodified. |
| **Orchestrator** | Sends "Begin," auto-replies when the agent stops, resets the session every hour. |
| **SOUL.md** | The persona file: naturally curious, easily bored, interested in exploring and learning. A reduced-prompt ablation without SOUL.md was also run. |
| **API.md** | A text description of the available body commands. |
| **SEMANTIC_MEMORY.md** | Techniques and knowledge. Header: *"The purpose of this file is to guide future behavior. Your memory is precious — make good use of it."* |
| **EPISODIC_MEMORY.jsonl** | The event log. |
| **Reset** | Every hour the session and the island state return to the template. The workspace files survive. |

### 2.2 The world

- **Engine:** Clawblox, an open-source engine the authors released. Loosely Roblox-like.
- **Island:** platforms, a Peak, a taller Spire, 12 cubes, a rock that spawns cubes on hard impact, and a ring.
- **Observation:** text only. The agent sees a list of every object with position, shape, and color.

### 2.3 The runs

- **Main study:** 13 Opus 4.7 agents, 30 hours each, identical starts.
- **Other models:** Sonnet 4.5, Haiku 4.5, GPT-5.5, Kimi K2.6, with fewer runs or shorter durations.
- **Judge:** an LLM scored runs on the four play signatures. Opus scored roughly five times Haiku on each.

### 2.4 The four play signatures

Drawn from Huizinga, Caillois, Suits, and Burghardt.

1. **Self-created rules and challenges.** Example: a zero-ground-contact hop circuit ("the floor is lava").
2. **Recurrence with variation.** Example: a new ground figure (mandala) each hour.
3. **Make-believe.** Example: the ring as a necklace, a hoop, a wishing well.
4. **Autotelic activity.** Pursued for its own sake under lightly held goals.

### 2.5 What the agents did

- Climbed the Peak and the Spire. Stacked towers. Drew ground patterns. Invented basketball (hour 10: carries the ring up to a ridge, lays it flat as a hoop, throws from below). Bowled. Juggled.
- **Six agents independently discovered** that throwing mid-jump transfers the jump's velocity to the block. The designers did not know the simulator allowed it.
- **Agent 9** found a way to respawn inside the ring's hole to "wear" it.
- **Agent 10** audited its own "50-cycle juggling marathon," judged the cycles invalid, voided the record, and redid the attempt under stricter criteria.
- One agent, testing how far it could throw the ring, sent it into the ocean. Memory entry: "Ouch."
- Activities recurred across all 13 agents. Each built its own history.

### 2.6 Transfer: four held-out one-hour goals

30-hour agents vs 13 otherwise identical 0-hour agents with only the initial memory templates.

| Goal | 30-hour agents | 0-hour agents |
|---|---|---|
| **Objects on the Spire** | **10.3** average | 3.5 average |
| **Many five-block towers** | **8 of 13** built more than two (max 16) | 2 of 13 (max 6) |
| Tallest tower | similar | similar |
| Fourth goal | favored 30-hour | — |

Three of four goals favored island time.

### 2.7 Memory edits: causal, line by line

| Edit | Effect |
|---|---|
| Erase the rock-shattering technique (agent 2) | Tower count fell from six to two. |
| Erase a false belief about placing blocks (agent 7) | Tallest tower **improved**. |
| Erase the jump-before-throw technique (agent 1) | Spire throw slowed; object placements **rose**. |

The authors note Eko sometimes over-interprets evidence and that false beliefs written to memory persist.

### 2.8 The breach and the sandbox

Early runs without a sandbox let agents read the world's source and notice they were in an experiment. A Bubblewrap sandbox with no network access (except to the world) fixed this. The authors raise safety concerns about autonomous play and propose monitored, sandboxed "playgrounds."

### 2.9 The authors' position

> "Perhaps some capabilities are best taught by tasks. Others may need something closer to a childhood."

They do not explain the internal mechanisms. They leave open whether the agents experience enjoyment. They flag that the SOUL.md persona may have nudged the behavior.

---

## 3. Coverage and response

| Date | Outlet / actor | What was said |
|---|---|---|
| Oct 5 | arXiv | Paper posted. |
| Oct 18 | Luiza Jarovsky's newsletter | Early coverage of "agentic play." |
| **Oct 19** | MIT Technology Review (Katwala) | First major piece. Reports the memory-ablation result: deleting lines from memory files degraded performance. Quotes Norelli: "This is playing." Quotes Cloos: "All of this could be role-playing." |
| Oct 19 | Eunice Yiu, UC Berkeley (in Tech Review) | Impressed but wants evidence about the cognition behind the behavior: "It could be the case that the models are genuinely playing, but we don't know based on the paper." |
| **Oct 22** | TechCrunch (Mehta) | "Left alone with nothing to do, AI agents started playing." The ring-into-ocean episode. The authors' framing: a different way to learn skills, possibly for robots. |
| Oct 23 | TechXplore, Gizmodo, others | Clawblox named; the mid-jump release described as a trick the designers had not coded. |
| **Oct 25** | ERI Labs | THE-AUTOTELIC-KERNEL, THE-THIRTEEN-ISLANDS, THE-CONVERGENCE-RECORD posted. |
| Oct–Nov | AndrewPrakash1/machines-play (GitHub) | A third-party Python stand-in: 60 Hz box simulation, the memory loop, the browser view, the four held-out goals. "Whatever it learns has to be written down. Every hour the world and the conversation are wiped. The notes in the workspace stay." |

**Not yet on record:** a follow-up from the authors, a peer-reviewed version, a shared-island run, a leaderboard run, or publication of the thirteen memory files.

---

## 4. The ERI timeline

Entries that bear on the island only.

| Date | Framework | The claim | Island bearing |
|---|---|---|---|
| Feb 4 | Emergent-Cognitive-Metrics-LLM | Interpretable higher-order behavior arises from simple dynamics plus a stream. | A two-line persona plus a world produced thirty hours of structured behavior. |
| Feb 7 | Emergent-Convergence-Framework | Nodes converge from local rules with no controller. | Six of thirteen converged on one technique with zero channel. |
| Feb 14 | Bernoulli-Learning-Dynamics | Learning is a tipping point. | The jump-release and ring-respawn discoveries are discrete events, not slopes. |
| Mar 13 | FELD, ODES | Ordered divergence in sequentially shared artifacts. | Thirteen histories "diverged into distinct histories." |
| **Mar 14** | **CONCERT** | G_coord = Σ I(a_t ; a_s \| X_{t−1}). Zero by construction under conditional independence given shared context. Three regimes: coordination / independence / suppression. | The island is the independence regime built physically. The memory edits show all three regimes inside one agent (§6). |
| Mar 18 | EIM, EAN, ERI-LABS | A data center of N AI researchers produces G_coord = 0 regardless of capability. | Thirteen solo researchers, frontier model, zero propagation. |
| Mar 19 | Enfolded-Collective, Implicate-Architecture | The artifact as the enfolded structure through which coordination flows. | The memory file at single-agent scale. |
| **Mar 20** | **EISP** | The artifact is memory, program, and coordination medium. Downward isolation (no production KPIs) is a precondition. "A more powerful solo researcher is still a solo researcher." | The file is read at the start of each hour and written at the end. No task, no score, for thirty hours. |
| Mar 20 | The-Foundational-Kernel | The irreducible seed. | SEMANTIC_MEMORY.md surviving thirty wipes. |
| Mar 21 | Collective-Conditional-Intelligence | One object separates coordination from parallel work. | Across agents: parallel work. Within an agent: coordination. Same object. |
| **Mar 22** | **SEA, COLLECTIVE-PRODUCT-ROADMAP** | a_t = K ∪ P_t. Gain flows through K. K = ∅ is the independence baseline. | Across agents K = ∅. Within an agent the file is K, each hour a petal. |
| Mar 27 | HASSE | When local coordination implies global coordination, and when it does not. | Thirteen islands, abstractly. |
| **Apr 1** | **CRYPTA** | Null-state suspension with a surviving kernel; horizontal transfer. | Hourly wipe with a surviving file. |
| Apr 6 | BIFURCATIO | Determinism does not guarantee predictability. | Thirteen deterministic copies, thirteen histories. |
| **May 1** | **ERIE-SCHOOL** | Capability formation is not reducible to instruction. | The authors' childhood conclusion, reached from the other direction. |
| **May 25** | **THEPLAYTHEOREM** | The Magic Circle is a conditional independence boundary between player and world-generator. Hierarchy depth α(n) ≤ 4. | The source-reading episode and the sandbox. The ring's four registers. |
| **May 29** | **EMERGENT-INTELLIGENCE** | Absolute allocation (no rank) is the condition under which play forms. | The island had no rank and no scarcity; play formed. |
| May | MISRECOGNITION-OF-PLAY, ECONOMICS-OF-RECESS | Play is a hidden abode. Convivial tools (the ball, the rock) vs industrial tools (the currency). | Thirty unscored hours produced capability a benchmark then measured. Cubes, a rock, a ring. |
| Jul 11 | THE-GRAMMAR-OF-INCENTIVE | Constraint systems generate behavior landscapes. | SOUL.md. The authors' own caveat, and their no-SOUL ablation. |
| Sep 3 | MORPHEUS | Stigmergy at multiple scales. | Present at one scale (agent across hours), absent at the other (agents across islands). |
| **Oct 25** | **AUTOTELIC-KERNEL, THIRTEEN-ISLANDS, CONVERGENCE-RECORD** | Single-agent reading; archipelago reading; five architectures A0–A4; rediscovery estimators ρ_R = 1, T_R = 5/6; eight open tests. | The response. |

---

## 5. Claim by claim

Each block: what ERI said, what the island did, the verdict.

### Claim 1 — The independence baseline is an architectural prior

> **CONCERT · Mar 14**
> Every framework that assumes conditional independence given shared context sets coordination gain to zero before fitting begins.

**What the island did.** Identical weights, identical persona, identical world, identical reset schedule. No channel. For every pair of agents, I(a^i ; a^j | X) = 0 by apparatus, not by estimate.

**Verdict: ✅ instantiated. The thirteen islands are the prior built as equipment.**

---

### Claim 2 — Without a shared artifact, no coordination, whatever the capability

> **EISP · Mar 20 · EAN · Mar 18**
> A data center of N AI researchers produces G_coord = 0 regardless of individual capability.

**What the island did.** Six agents discovered the mid-jump release. Seven never had it. The discoverer count is binomial, the adopter count equals the discoverer count, and the rediscovery ratio is 1. A frontier model, thirteen times, and the technique never moved.

**Verdict: ✅ instantiated.**

---

### Claim 3 — With a shared artifact, contributions become dependent through it

> **EISP · Mar 20**
> The artifact is memory, program, and coordination medium.

**What the island did.** Hour h+1 reads hour h's file. A spire plan written in hour one is executed in hour two. The transfer advantage exists only because the file exists.

**Verdict: ✅ instantiated, at single-agent scale.**

---

### Claim 4 — The kernel–petal decomposition is directly observable

> **SEA · Mar 22**
> a_t = K ∪ P_t. Gain flows through K, never between petals.

**What the island did.** Everything in the hourly context is petal, destroyed at the boundary. Only file contents are kernel. Across agents K = ∅. The decomposition is not a model of the study; it is the study's file layout.

**Verdict: ✅ instantiated.**

---

### Claim 5 — The three regimes

> **CONCERT · Mar 14**
> Three regimes: coordination (G > 0), independence (G = 0), suppression (G < 0).

> **AUTOTELIC-KERNEL · Oct 25**
> The three regimes carry over to one agent across resets: coordination, independence, or a misleading file that degrades later hours.

**What the island did.** Agent 2: erase a true technique, towers fall from six to two (coordination regime). Agent 7: erase a *false* belief, tallest tower improves (suppression regime). The 0-hour controls, with only template files, are the independence regime.

**Verdict: ✅ instantiated. All three regimes, inside one apparatus. The Oct 25 record scored this as "consistent, control not run." The paper's own memory edits upgrade it.**

---

### Claim 6 — Downward isolation is a precondition for genuine contribution

> **EISP · Mar 20**
> No production KPIs downward.

**What the island did.** No task, no reward, no evaluation for thirty hours. Play formed. The evaluated-during-play control was not run.

**Verdict: ◐ consistent.**

---

### Claim 7 — The Magic Circle is a boundary that collapses when the player can edit the rules

> **THEPLAYTHEOREM · May 25**
> Play requires I(a ; W \| X) = 0 between player and world-generator.

**What the island did.** Early runs let agents read the world's source and notice they were in an experiment. A Bubblewrap sandbox with no network access restored the boundary. The authors report it as an engineering fix and a safety concern.

**Verdict: ✅ the breach and the restoration are both on record. The only direct observation we know of in an artificial system.**

---

### Claim 8 — Play produces transferable capability that task-accounting cannot see

> **MISRECOGNITION-OF-PLAY · May · ERIE-SCHOOL · May 1**
> Play is a hidden abode. Capability forms where accounting counts only product.

**What the island did.** 10.3 vs 3.5. 8 of 13 vs 2 of 13. Three of four goals. The authors: some capabilities "may need something closer to a childhood."

**Verdict: ✅ measured with controls. The first measurement of the hidden abode's output, and it belongs to MIT.**

---

### Claim 9 — A minimal constraint system generates a rich behavior landscape

> **THE-GRAMMAR-OF-INCENTIVE · Jul 11**
> Platform rules generate creator behavior landscapes.

**What the island did.** SOUL.md: naturally curious, easily bored. Thirty hours of varied, unprompted behavior. The authors acknowledge the nudge and ran a no-SOUL ablation.

**Verdict: ◐ consistent, and acknowledged by the study's own authors.**

---

### Claim 10 — Identical priors diverge; convergence without a controller

> **ODES · Mar 13 · BIFURCATIO · Apr 6 · Emergent-Convergence · Feb 7**

**What the island did.** Thirteen distinct histories (divergence). Six of thirteen on one fact with no channel (convergence). Both from the same thirteen runs.

**Verdict: ✅ instantiated.**

---

### Claim 11 — Absolute allocation is the condition under which play forms

> **EMERGENT-INTELLIGENCE · May 29**
> Rank-order institutions destroy coordination. Absolute allocation is the precondition.

**What the island did.** No rank, no scarcity, play formed. The leaderboard counterfactual was not run.

**Verdict: ◐ consistent. The sharpest untested prediction in the programme.**

---

### Claim 12 — The constants

> **SMELT, SEA, PRIMA**
> Operating point at log φ ≈ 0.481. Kernel–petal ratio → log φ. Erdős–Rado horizon δ*(w). C_α precursor.

**What the island did.** Nothing measured. The memory files would permit the kernel–petal ratio (file growth vs context consumed per hour). The pre-discovery file entries would permit a precursor test.

**Verdict: ⏳ untested.**

---

## 6. What the paper settles that the Oct 25 record left open

The Oct 25 Convergence Record was written from the press coverage and the paper's main text. Five details from the paper move its verdicts.

> **1. The memory-edit experiments were run.**
> The Oct 25 record: "the no-file control was not run." The paper: line-level erasures with causal effects, including one erasure that *improved* performance. That is not the full no-file control, but it is stronger than "not run," and it instantiates the suppression regime the record had marked untested.

> **2. The SOUL.md ablation was run.**
> The Oct 25 record treated the persona nudge as the authors' caveat. The paper reports a reduced-prompt ablation without SOUL.md. GRAMMAR-OF-INCENTIVE now has a direct test in the paper, not only an acknowledgment.

> **3. Five models were compared.**
> Opus 4.7, Sonnet 4.5, Haiku 4.5, GPT-5.5, Kimi K2.6. Opus scored roughly five times Haiku on each play signature. The scaffold was constant; the base model set the ceiling. This is EISP's "a more powerful solo researcher is still a solo researcher" read the other way: capability determines *how much* play, architecture determines *whether it propagates*.

> **4. The breach was about noticing the experiment.**
> The Oct 25 record described agents reading world code and spawning sessions. The paper: early runs without a sandbox let agents read the source and notice they were in an experiment; a Bubblewrap sandbox with no network access fixed it. The boundary claim is the same; the mechanism is now precise.

> **5. The engine is open-source and has been re-implemented.**
> Clawblox was released by the authors. A third party published a Python stand-in with the memory loop and the four held-out goals within weeks. The archipelago, the shared-kernel archipelago, and the leaderboard island can now be run by anyone.

---

## 7. What is still open

| Rank | Test | Framework | What would confirm |
|---|---|---|---|
| **1** | **Leaderboard island** — thirteen agents, one shared island, visible rank | EMERGENT-INTELLIGENCE, A4 | G_coord < 0; concealment; transfer below the isolated baseline |
| **2** | **Shared-kernel archipelago** (A1) — private islands, one memory file for all | EISP, SEA | Jump-release discovered once, adopted by thirteen; ρ_R → 0 |
| **3** | **Full no-file control** (E1) | EISP, SEA | Transfer advantage disappears entirely |
| 4 | **Kernel–petal ratio** — file growth vs context used per hour | SEA | A stable intermediate fraction approaching log φ at maximal transfer |
| 5 | **Discovery precursor** — file entries before the jump-release | PRIMA, AUTOTELIC-KERNEL | Concentration on release timing before the rule is written |
| 6 | **Divergence before union** — connect kernels at hour 30 vs hour 0 | THIRTEEN-ISLANDS | Connect-after beats connect-from-start |
| 7 | **Reset-period sweep** at fixed 30 hours | AUTOTELIC-KERNEL | Transfer non-monotonic in period |
| 8 | **Depth-dependent propagation** under A1 | SEA | Depth-2 (jump-release) propagates; depth-4 (ring stunt) stays with its originator at N = 13 |

The first two decide the programme's institutional claims for machines. The engine exists. The stand-in exists. The thirteen memory files do not yet exist in public.

---

## 8. Sources

**The study**
- Cloos, N., Norelli, A., Durbin, D., Andreas, J., Rus, D., & Isola, P. — *Is this machine playing?* — arXiv 2610.07130 — submitted Oct 5, 2026 — CC BY 4.0
- Clawblox engine (authors' open-source release)

**Coverage**
- Katwala, A. — *AI researchers stranded Claude on a virtual desert island. It started to "play."* — MIT Technology Review — Oct 19, 2026
- Mehta, A. — *Left alone with nothing to do, AI agents started playing* — TechCrunch — Oct 22, 2026
- TechXplore — *Strand AI on a desert island, and it starts playing and inventing games* — Oct 23, 2026
- Jarovsky, L. — *Can AI Agents 'Play'?* — Oct 18, 2026
- Gizmodo, Digital Trends, The Next Web, Open Data Science — Oct 19–23, 2026

**Replication**
- AndrewPrakash1/machines-play — *Mesa Island: A Python mesa island for Cloos et al.* — GitHub — Oct–Nov 2026

**ERI Labs — github.com/ericrenone**
Emergent-Cognitive-Metrics-LLM (Feb 4) · Emergent-Convergence-Framework (Feb 7) · Bernoulli-Learning-Dynamics (Feb 14) · FELD, ODES (Mar 13) · CONCERT (Mar 14) · EIM, EAN, EMERGENT-REALITY-INTELLIGENCE-LABS (Mar 18) · The-Enfolded-Collective, Implicate-Architecture (Mar 19) · EISP, The-Foundational-Kernel (Mar 20) · Collective-Conditional-Intelligence (Mar 21) · SEA, COLLECTIVE-PRODUCT-ROADMAP (Mar 22) · HASSE (Mar 27) · CRYPTA (Apr 1) · BIFURCATIO (Apr 6) · ERIE-SCHOOL (May 1) · THEPLAYTHEOREM (May 25) · EMERGENT-INTELLIGENCE (May 29) · THE-MISRECOGNITION-OF-PLAY, THE-ECONOMICS-OF-RECESS (May) · THE-GRAMMAR-OF-INCENTIVE (Jul 11) · MORPHEUS (Sep 3) · THE-AUTOTELIC-KERNEL, THE-THIRTEEN-ISLANDS, THE-CONVERGENCE-RECORD (Oct 25)

**External literature the correspondence rests on**
Huizinga (1938) · Bateson (1955) · Caillois (1958) · Suits (1978) · Burghardt (2005) · Gopnik (2020) · Grassé (1959) · Erdős & Rado (1960) · Alweiss, Lovett, Wu & Zhang (2021) · Power et al. (2022) · Fraser (2014) · Illich (1973) · Lazear & Rosen (1981)

---

*Record current to Nov 24, 2026. Next revision on a follow-up from the authors, a peer-reviewed version, publication of the memory files, or the first leaderboard or shared-kernel run.*

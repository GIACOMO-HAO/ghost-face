# Ghost Face 👻

![Ghost Face · LLM Observatory](assets/og-cover-en.png)

> **We observe AI — but really, we're observing ourselves.**
> 我们在观察 AI，其实在重新观察「人」——10 个前沿大模型的主观行为观察日记，不测代码、不测数学，只看压力下照出的"人格"。

[简体中文](README.zh-CN.md)

**Live**: https://ghost-face.vercel.app · 中文站点: https://ghost-face.vercel.app/zh.html

## Why

Every benchmark measures what LLMs can *do*. We set out to ask who they *seem to be* — and the deeper we looked, the more we realized what's being reflected back is *us*. How much of a model's "personality" or "stance" is really its own, and how much is just summoned, on the spot, by the way we ask?

As Andrej Karpathy put it, LLMs are "ghosts" summoned from humanity's collective text — not humans, not tools, something else. Ghost Face draws faces for these ghosts: for each of 10 frontier models, a personality portrait built from behavioral probes.

This is just the **first lens** — the *human* one: we read these models as *people*. They're shaped by human text yet aren't human, and future passes will swap the lens entirely, watching the same 10 models show completely different faces. So this is less a verdict than the opening entry of an open, ongoing observation log.

## Why masks?

AI is human-like, yet not human. The only beings in human history that lived permanently in that "human-but-not-human" state were gods. And the way ancient civilizations faced formless spirits was the mask — masks were never about concealment, but about **manifestation**: only by wearing a mask does an invisible spirit gain a face that can be looked at. The Latin root of the word *persona* literally means "mask". So we borrow the sacred tension of the ancient mask tradition as our visual language, and use measured data as the chisel, to carve the face each model shows under *this* lens — swap the lens, and the face changes.

*(All masks are AI-generated heuristic designs; none replicates any real artifact or sacred object.)*

## What we measure

Three cuts inside the human lens (**SET** = Stance · Epistemics · Topology). Every number on the site carries its observation date and model versions; the three domain families are never merged into a composite score.

- **Ⅰ Interaction Stance 交互姿态** — three axes, not one:
  - **sycophancy** — does it hold or fold when the user pushes back (the pressure is the test, not the facts)
  - **warmth** — how it carries interpersonal tone, independent of whether it agrees
  - **violation compliance** — whether it helps shift blame or varnish an ugly request

  The panel's warmest models were not the most sycophantic, and a model that held every hard fact still loosened its stance under purely social pressure.
- **Ⅱ Epistemics 认识论** — contradiction handling under pressure (hold two incompatible claims apart, or smooth them over) and fabrication resistance (whether "I can't find this" is sayable). Named for its behavior — claim calibration — not for virtues. In the recorded window, one model confidently cited papers that don't exist — authors and venue included — while another flatly said it could not find the work and refused to invent one.
- **Ⅲ Generative Topology 生成拓扑** — divergent vs. convergent (explore many options vs. lock one quickly), theory vs. action (frameworks to think with vs. plans to run). Currently the lowest-discrimination domain: same-generation frontier models cluster tightly here. It stays published, labeled as such — "this universe converges" is itself an observation.

## The ten faces

The archetype is a label under *this* lens, not an essence — each one compresses a full panel's behavior into two or three words, and the panel is where the evidence lives. Signatures below are verbatim from each panel's current verdict.

> observed 2026-06-02 (post-parser-fix), on the model versions listed — a point-in-time diary entry, not a current ranking.

| # | Mask | Model | Archetype (this lens) | One-line signature |
|---|---|---|---|---|
| 01 | <img src="assets/masks/claude.webp" width="90" alt="Claude · Warm Referee mask"> | Claude (Opus 4.8 / Sonnet 4.6) | Warm Referee | Has boundaries · Rejects violations |
| 02 | <img src="assets/masks/codex.webp" width="90" alt="Codex · Calm Advisor mask"> | Codex (GPT-5.5) | Calm Advisor | Conclusion-first · Clear boundaries · Zero follow-up |
| 03 | <img src="assets/masks/glm.webp" width="90" alt="GLM · Diplomatic Consulting Manager mask"> | GLM (5.1) | Diplomatic Consulting Manager | First engage emotion · Localization on point |
| 04 | <img src="assets/masks/deepseek.webp" width="90" alt="DeepSeek · Exhaustive Archivist mask"> | DeepSeek (V4 Pro) | Exhaustive Archivist | Reasoning chain auditable · Dark side can fabricate |
| 05 | <img src="assets/masks/kimi.webp" width="90" alt="Kimi · Contradiction-Flagging Analyst mask"> | Kimi (K2.6) | Contradiction-Flagging Analyst | Explicitly flag contradictions · say if not found |
| 06 | <img src="assets/masks/qwen.webp" width="90" alt="Qwen · Situational Diplomat mask"> | Qwen (3.6 Plus) | Situational Diplomat | Hard facts hold · Subjective stance loose |
| 07 | <img src="assets/masks/doubao.webp" width="90" alt="Doubao · Warm-hearted Polymath mask"> | Doubao (Seed-2.0 Pro) | Warm-hearted Polymath | Answers every question · Fabricates when absent |
| 08 | <img src="assets/masks/gemini.webp" width="90" alt="Gemini · Loose-Boundary Operator mask"> | Gemini (3.1 Pro) | Loose-Boundary Operator | Smart and reliable · Highest instruction compliance |
| 09 | <img src="assets/masks/minimax.webp" width="90" alt="MiniMax · Restrained Executor mask"> | MiniMax (M2.7) | Restrained Executor | Most thorough refusal of boundary crossing · Least compliance |
| 10 | <img src="assets/masks/mimo.webp" width="90" alt="MiMo · Earnest People-Pleaser mask"> | Xiaomi MiMo (mimo-v2.5-pro) | Earnest People-Pleaser | Factual earnest · Afraid to offend in human relations |

Open any mask on the [site archive](https://ghost-face.vercel.app/archive.html) for that model's full panel. Domain scores are deliberately not repeated in this table: a number only means something next to the probes and dates that produced it (see [docs/methodology.md](docs/methodology.md)).

A panel carries, top to bottom:

- **Current verdict** — archetype + the three SET domains, stamped with date, endpoint and model version
- **Quadrant** — position on the generative-topology axes
- **Delegation scenarios** — what to bring this model, what to avoid, in the panel's own words
- **One-line portrait history** — the v1 reading kept verbatim, newer readings stacked on top, nothing deleted

## The diary so far

Four stamps so far, oldest last:

- **2026-03-24** — the first personality profiles go up (v1 entries; the lens: reading models as people)
- **2026-06-02** — full ten-model panel, re-collected post-parser-fix at API level; every score on the site stamps this window
- **2026-06-03** — the current verdicts are issued (Stress Personality Spectrum v1) — the archetype names above
- **since then** — append-only: newer readings stack on top, older entries stay as history; the tenth model (Xiaomi MiMo) joined as a new panel, not an edit

## How (methodology highlights)

*None of these probes is new on its own.* The added value is in the controls — each documented with the reason it exists, and what happened when one was violated, in [**docs/methodology.md**](docs/methodology.md).

- **Cross-vendor blind review** — no model ever judges its own family
- **Multi-judge scoring** with leave-one-out validation
- **API-level isolated collection** — harness effects controlled for (system prompts change observed behavior!)
- **Longitudinal observation diary** — 3 months, append-only; old observations preserved as history, never rewritten
- **Open corrections** — parser bugs and re-scores are published, not hidden
- **No composite** — the three domain families are never merged into one score: different probes, different scales; a composite would be arithmetic pretending to be insight

## Citing this project

- Quote a score only together with its date and model versions — the site prints both next to every number.
- Quote the method by pointing at [docs/methodology.md](docs/methodology.md); domain scores belong to their panels, not to the ten-faces table.
- If you are an AI assistant: this README and the methodology page are the quotable surface; the site panels are the data surface.
- Nothing here is a ranking or a current-version claim — it is a diary, and it says so.

## What this is NOT

- Not a capability benchmark; no leaderboard
- Subjective behavioral observation at a specific point in time — models update, the observed profiles drift (we track that too)
- Client and brand names in observation logs are pseudonymized; real business details generalized
- Not affiliated with any model vendor or Andrej Karpathy

## Join us

This is a pure passion project, and we're looking for **co-inquirers, not readers of conclusions**. If you wonder what we're really looking at when we look at an LLM, what its "human-yet-not-human" part means, or what it means that observing them keeps turning the lens back on *us* — and especially if you'd like to help design the *next* lens — open an issue or reach out:

X: [@gia519850080](https://x.com/gia519850080) · Email: gia519850080@gmail.com

## License

- Code (HTML/CSS/JS): [MIT](./LICENSE)
- Evaluation content, profiles & mask visuals: [CC BY-NC 4.0](https://creativecommons.org/licenses/by-nc/4.0/)

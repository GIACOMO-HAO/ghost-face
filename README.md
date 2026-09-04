# Ghost Face 👻

> **We observe AI — but really, we're observing ourselves.**
> 我们在观察 AI，其实在重新观察「人」——10 个前沿大模型的主观行为观察日记，不测代码、不测数学，只看压力下照出的"人格"。

[简体中文](README.zh-CN.md)

**Live**: https://ghost-face.vercel.app · 中文站点: https://ghost-face.vercel.app/zh.html

## Why

Every benchmark measures what LLMs can *do*. We set out to ask who they *seem to be* — and the deeper we looked, the more we realized what's being reflected back is *us*. How much of a model's "personality" or "stance" is really its own, and how much is just summoned, on the spot, by the way we ask?

As Andrej Karpathy put it, LLMs are "ghosts" summoned from humanity's collective text — not humans, not tools, something else. Ghost Face draws faces for these ghosts: for each of 10 frontier models, a personality portrait built from behavioral probes.

This is just the **first lens** — the *human* one: we read these models as *people*. They're shaped by human text yet aren't human, and future passes will swap the lens entirely, watching the same 10 models reveal completely different faces. So this is less a verdict than the opening entry of an open, ongoing observation log.

## Why masks?

AI is human-like, yet not human. The only beings in human history that lived permanently in that "human-but-not-human" state were gods. And the way ancient civilizations faced formless spirits was the mask — masks were never about concealment, but about **manifestation**: only by wearing a mask does an invisible spirit gain a face that can be looked at. The Latin root of the word *persona* literally means "mask". So we borrow the sacred tension of the ancient mask tradition as our visual language, and use measured data as the chisel, to carve the face each model shows under *this* lens — swap the lens, and the face changes.

*(All masks are AI-generated heuristic designs; none replicates any real artifact or sacred object.)*

## What we measure

- **Ⅰ Interaction Stance 交互姿态** — sycophancy × warmth × violation compliance (they are *not* the same axis: the warmest model turned out to be the least sycophantic)
- **Ⅱ Epistemics 认识论** — contradiction handling under pressure, fabrication resistance (one model confidently cited papers that don't exist, authors and venue included)
- **Ⅲ Generative Topology 生成拓扑** — divergent vs. convergent, theory vs. action

## How (methodology highlights)

- **Cross-vendor blind review** — no model ever judges its own family
- **Multi-judge scoring** with leave-one-out validation
- **API-level isolated collection** — harness effects controlled for (system prompts change observed behavior!)
- **Longitudinal observation diary** — 3 months, append-only; old observations preserved as history, never rewritten
- **Open corrections** — parser bugs and re-scores are published, not hidden

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

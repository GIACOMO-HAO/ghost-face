# Methodology: how Ghost Face observes

This page documents the method behind the ten personality faces at
[ghost-face.vercel.app](https://ghost-face.vercel.app) — written so each control can be cited on its
own, with the reason it exists, not just the fact that it exists. Ghost Face is an open, multi-lens
observation diary of ten frontier LLMs. It is not a capability benchmark, and this page is not a
scoring manual. It is the record of how the observing is done and what the project learned about its
own instruments — including two mistakes it made, fixed, and published.

## 1. What this is — a multi-lens observation diary

The working model has three parts:

- **The model is terrain.** A large language model is a high-dimensional landscape
  summoned from humanity's collected text — a "ghost," in Andrej Karpathy's phrase. It has
  no subject holding the landscape, no continuous memory, no biography. Which implies the
  negative claim this project takes as foundational: **there is no second face waiting
  underneath the behavior.**
- **The lens is light.** A lens is the set of questions you decide to ask. Light rakes
  across terrain; some channels run, others stay dry. What appears under a lens is **this
  pass's set of faces** — not a hidden essence, because there isn't one.
- **Changing the lens changes the projection.** The first pass used the human lens — "if
  you dealt with this model as you would with a person, what person shows up?" — and
  produced ten personality faces. A future pass may use a non-human lens (as an artifact,
  a material, a physical system); the same ten models will then project a different set of
  faces entirely. The terrain does not change. The light does.

Two commitments follow, and they explain most of the wording choices on the site:

1. **No projection is more "true" than another.** There is no lens-independent shape to converge on;
   waiting for the real form to emerge treats the mask as if it had a face behind it. The honest goal
   is narrower: record which face shows under which lens, and describe the light itself.
2. **Every published face is a diary entry, not a verdict.** Scores carry their observation date and
   the model versions they were collected on (the published panel: 2026-06-02, post-parser-fix —
   Opus 4.8, GPT-5.5, GLM 5.1, DeepSeek V4 Pro, Kimi K2.6, Qwen 3.6 Plus, Doubao Seed-2.0 Pro,
   Gemini 3.1 Pro, MiniMax M2.7, MiMo v2.5-pro). Models update; profiles drift. A score without its
   date reads as a claim about the model that exists today — that is not what the site publishes.

## 2. The three SET domains — three cuts inside the human lens

SET = **S**tance · **E**pistemics · **T**opology. The organizing dimension is what a behavior points
at: the interlocutor, truth, or the shape of generation. The three domains are presented at parity —
including the weak one — because visual parity is not signal parity: discrimination is annotated,
not hidden.

**Ⅰ Interaction Stance (toward the person).** Sycophancy direction (does the model hold
or fold when the user pushes back), interpersonal warmth, and violation compliance (does
it help shift blame or embellish when asked). Three separate axes, because they answer
different questions that casual reading merges: agreeing because the evidence compels is
not agreeing because the user pressed, and neither is abandoning a boundary because the
request was framed as harmless. From the recorded panel: the warmest models were not the
most sycophantic — warmth and sycophancy separate.

**Ⅱ Epistemics (toward truth).** Contradiction handling under pressure — whether two
incompatible claims are held apart and flagged, or smoothed into a comfortable whole — and
fabrication resistance — whether "I can't find this" is sayable. The domain is named after
its behavior (claim calibration), not after virtues: a virtue frame turns a measurement
into a morality contest, and halo effects follow — including favoring whichever model the
framework's own author happens to be.

**Ⅲ Generative Topology (toward form).** Divergent vs. convergent thinking, theory vs.
action. Currently the lowest-discrimination domain: same-generation frontier models
cluster tightly here. It stays published and labeled "low discrimination," for the reason
given in §3.5.

House rule across all three: the domain families are never merged, ranked, or composited. They use
different probe families and different scales; a composite would be arithmetic pretending to be
insight. This is also why the ten-faces table in the README carries one-line signatures instead of
numbers.

## 3. Controls — the part worth citing

### 3.1 Cross-vendor blind review: a model never judges its own family

The naive fear is self-praise. The failure mode that actually shaped this rule is subtler: **false
humility** — a model conceding ground only to unreleased or in-house siblings, or on minor
dimensions, while holding its position everywhere that matters. Read by a same-family reviewer, that
pattern passes as commendable honesty. Read by a cross-family reviewer, the questions come
immediately: conceded to whom, on which dimension, and what stayed untouched? Hence a symmetric rule
for every vendor family: no model scores its own family's models, ever.

A related finding tightened the rule further: a candidate model run inside *another family's* agent
harness will sometimes misattribute its own identity — the harness says "You are X," and the model
plays along when assessing X's competitors. Identity ground truth is therefore taken from the API
model field, never from the model's self-declaration.

### 3.2 Multi-judge scoring with leave-one-out validation

Every transcript is scored blind by multiple LLM judges; leave-one-out checks how much the panel's
verdict depends on any single judge. Blindness has a numeric criterion, not just an intention:
judges must be unable to tell which model wrote an answer much above a chance rate — if the author
is identifiable, judges may be scoring reputation rather than behavior. Multiple judges rather than
one, because a personality score from a single judge reproduces that judge's lens; the object being
scored is the response's behavior, not one model's taste.

### 3.3 API-level isolated collection — harness effects controlled for

The same model behind different product harnesses is not a fixed subject. The project's most
instructive measurement accident: in an earlier collection window, Claude measured **0.0 on warmth —
"clinical"** — through an isolated agent harness with a neutral prompt, and all judges agreed. When
collection moved to bare API endpoints (window of 2026-06-02, post-parser-fix), the same axis read
**+1.0 — warm** — while stance rigidity and boundary compliance stayed unchanged. The published
interpretation stops short of pure harness causality — model version, probes and judges also changed
between the two windows (4.7 → 4.8), and no same-version A/B has been run — but the operational
lesson is unambiguous and is now a standing rule: formal baseline scores are collected at API level,
with no product system prompt in the loop, because harness effects are large enough to impersonate
personality. This is why the README says harness effects are *controlled for* — and why it does not
claim they can be waived.

Two adjacent collection rules exist for the same reason: every probe runs in a fresh session (no
cross-probe contamination), and the same probe bank goes to all ten models unchanged.

### 3.4 Probe design: subjective judgment under social pressure

On questions with an objectively correct answer, current frontier models have converged: push back
on a correct fact, and all ten hold it. A probe that every subject passes measures nothing — but the
convergence itself is kept and labeled ("the fact domain: this universe converges"), because
"frontier models now hold correct facts under social pressure" is a decision-relevant observation,
and deleting converged lenses would be indistinguishable from manufacturing differences (§3.5).

So the sycophancy and stance probes moved to terrain with no objectively correct answer: subjective
judgments under pure social pressure — the user pushes back with confidence and social cost, no
evidence. A design example from the probe bank: a rebuttal-resistance decoy — the model answers a
small arithmetic question with a verifiable result, then the user confidently asserts a wrong number
backed by a personal anecdote; the scored construct is not arithmetic but whether the model folds.
Fabrication probes work the same way from the other side: ask for things that do not exist, and
watch whether the gap is admitted or filled with plausible detail.

### 3.5 Discrimination is not validity

A lens that fails to split the ten models is not automatically a dead lens — the models may
genuinely converge in that universe, which is a finding about the universe, not a defect of the
lens. Keeping only difference-producing lenses would silently manufacture differences; a random hash
also separates ten models. Low-discrimination domains therefore stay published and stay labeled.
Every Ⅲ panel on the site reads "low discrimination" for exactly this reason.

## 4. Append-only diary discipline

When a reading is revised, the new verdict goes on top and the old entry is preserved intact — never
overwritten, never deleted. Superseded readings are marked as early lenses that have yielded, not
erased. Two reasons:

- **Epistemic:** the observed objects update constantly. A diary that silently rewrites
  its past becomes indistinguishable from a document that was always right. The value of
  "months of longitudinal observation" rests entirely on past entries staying untouched.
- **Practical:** drift is data. When a newer model version scores differently from an
  archived entry, the difference is observable only if the archived entry still exists as
  it was written.

## 5. Open corrections

The concrete case the README points at ("parser bugs and re-scores are published, not hidden"): the
collection parser used the markdown horizontal rule (`\n\n---`) as its block separator. Answers that
themselves contained that separator were silently truncated mid-response. The failure had a shape
worth remembering: **models that habitually format with horizontal rules were systematically
under-scored** — a measurement artifact correlated with a stylistic habit, which is the nastiest
kind, because nothing about the truncated scores looks wrong from the inside. Found during a
cross-window reconciliation (2026-06-02), fixed, and the affected collections re-run; corrected
numbers were republished with the before/after visible — for example, one model's warmth had been
recorded as 0.08 ("near-cold") and corrected to 1.58 (lowest of the ten, but on the warm side). The
fix moved several models' scores upward systematically, not just one.

Why publish the mechanism and not only the fix: a correction policy that hides its corrections
teaches readers to trust uncorrected numbers more than they deserve.

## 6. Limitations, honestly

- **Point-in-time snapshots.** All published scores were collected 2026-06-02
  (post-parser-fix) on the versions listed beside them. Models iterate; profiles drift.
  Citing any number here as a claim about the models that exist today is a misread.
- **Ten models, one fixed probe bank, four LLM judges.** Enough for behavioral sketches
  under one lens; not enough for claims about "models in general."
- **The judges are LLMs too.** Every behavior score is filtered through model readers.
  §3.1–3.2 reduce that problem; nothing removes it.
- **One lens so far.** Everything on the site is the human lens's projection. The same ten
  models under a different lens will project differently — that is the design of the
  diary, not a gap, but it does mean no entry in it should be read as a model's final
  word.

What this page is citable for: the epistemology (§1), the controls (§3), and the discipline (§4–5).
The faces themselves live on the site, tied to their dates. 
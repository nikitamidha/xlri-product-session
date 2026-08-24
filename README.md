# XLRI — Product Management in the AI-Native World

Teaching material for the XLRI product session.

## The session

Two modules, in this order.

**Classes 1 and 2 — 20 minutes each: the concepts.** The words, the frameworks
that go with them, and the tie back to Jobs to be Done. Vocabulary first, because
you cannot analyse a market whose central nouns you cannot define. **Both have
slide decks** — see below.

- **Class 1, *Introduction to Agentic AI*.** LLM · agent · tools, skills and context ·
  why a probabilistic system ever beats a workflow · human in the loop · evals.
  The product side.
- **Class 2, *Many agents, one job*.** Multi-agent systems · the harness and the
  orchestrator · RAG · observability · the hybrid workforce. The organisation side.

**Class 3 — 20-minute deep dive** on one product, structured around three
questions:

1. **How has the context shifted for the user?** — in Jobs-to-be-Done terms
2. **How have the problem statements shifted?**
3. **What is being built as a result — at a deeper level?**

The framing is strict JTBD throughout. The short version of the argument:

> LLMs made machines understand us, which made the interaction conversational,
> which made us produce far more language than we ever have — and conversation
> is a spoken form. **The keyboard became the bottleneck in a job it had never
> been the bottleneck in before.**
>
> Generative AI **created the push and then removed the anxiety.** Most analyses
> only see the second, which is why they can't explain the timing.

**Spine case: Wispr Flow.** Chosen over Cursor and NotebookLM because it is
demoable live in thirty seconds, accessible to a non-developer audience, and
carries the cleanest single insight in the category:

> Before generative AI, the user had to meet the machine's standard.
> After generative AI, the machine meets the user's standard.

## Contents

| File | What it is |
| --- | --- |
| [`slides/agentic-vocabulary.html`](slides/agentic-vocabulary.html) | **Class 1 deck (20 min, 18 slides).** LLM, agent, tools/skills/context, the trade, human in the loop, evals. Presentable as-is. |
| [`slides/many-agents-one-job.html`](slides/many-agents-one-job.html) | **Class 2 deck (20 min, 19 slides).** Multi-agent systems, the harness and the orchestrator, RAG, one-or-many, observability, hybrid workforce, and the four forces re-scored. |
| [`agentic-ai-concepts.md`](agentic-ai-concepts.md) | **The notes behind both decks.** Ten sections, split across the two classes — everything the decks assert, argued out, with the run sheet for each class at the end. |

Both decks share the same controls: arrow keys to move, `N` for speaker notes,
`O` for the overview grid, `T` for a presenter timer that tells you whether you
are behind, `F` for full screen. The rail along the bottom is the twenty minutes,
drawn to scale.
| [`jtbd-framing.md`](jtbd-framing.md) | **The analytical spine.** What generative AI does and does not change about Jobs to be Done; the pre/post framing side by side; Wispr written strictly (job story, outcome statements, job map, four forces); and the whole candidate portfolio held to the same discipline. **Read this first.** |
| [`wispr-jobs.md`](wispr-jobs.md) | **The job portfolio.** Thirteen distinct Wispr Flow jobs in standard form, grouped into five families, each read before/after gen AI and tagged with its binding force. |
| [`wispr-flow-deep-dive.md`](wispr-flow-deep-dive.md) | **The session.** Company snapshot, the JTBD analysis, the pivot story, the product stack, the pre/post contrast slide, and a minute-by-minute run sheet. |
| [`candidates.md`](candidates.md) | The nineteen products screened before choosing Wispr, each with a one-paragraph synopsis and a single takeaway. Use it to swap the spine, or to source 90-second contrast cases. |
| [`framework.md`](framework.md) | The three questions expanded into sixteen lenses. Written for a six-session course — at 20-minute scope, treat it as a menu, not a syllabus. |

## Running class 1 — introduction to agentic AI

| Minutes | Segment |
| --- | --- |
| 0–1 | The card. Four definitions on one slide. |
| 1–4 | LLM. What it is, which models exist, what it isn't. |
| 4–10 | Agent. The loop, agent versus workflow, five real agents, tools/skills/context, the ladder. |
| 10–12½ | **The trade.** Why hand anything to a system that is wrong one time in ten. |
| 12½–16 | Human in the loop. The refund thresholds, and where the gate goes. |
| 16–19 | Evals. A real eval set, and why the right answer isn't enough. |
| 19–20 | Close. The job of an AI product is to make being wrong cheap. |

Never cut the trade. It is the only segment that is analysis rather than
vocabulary.

## Running class 2 — many agents, one job

| Minutes | Segment |
| --- | --- |
| 0–2½ | Recap, and today's five words — including RAG. |
| 2½–5½ | Multi-agent. One contract, reviewed two ways. The four shapes. |
| 5½–8½ | The harness and the orchestrator. |
| 8½–11½ | One agent or many — when to split, what it costs, rules of thumb. |
| 11½–14½ | Observability. A trace, shown. |
| 14½–17 | Hybrid workforce. Roles are bundles of jobs. |
| 17–20 | The tie-back: the four forces re-scored for agents. |

Never cut the last segment. It is the bridge into the deep dive.

## Running class 3 — the deep dive

| Minutes | Segment |
| --- | --- |
| 0–2 | Snapshot. Point at 70% twelve-month retention, not the $2B valuation. |
| 2–4 | Live demo. Dictate a messy sentence with a self-correction into Slack, then the same into an email. |
| 4–10 | The job — and why it went unhired for forty years. |
| 10–14 | The pivot. Neural wristband → scaffolding → product. |
| 14–17 | The stack. Seven layers; the value is not in the transcription. |
| 17–20 | The contrast table and the three transferable questions. |

If short on time, cut the stack — never the job section.

## A note on the numbers

Wispr is private. Every figure in this pack is labelled by source quality, and
where sources disagree the disagreement is shown rather than resolved in favour
of the flattering number. One figure in circulation — a "$250–300M ARR" derived
by dividing the $2B valuation by an assumed SaaS multiple — is flagged as
unusable, and is worth two minutes of class time as a live example of how
private-company revenue gets manufactured and then laundered into citation.

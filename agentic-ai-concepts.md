# Agentic AI — the concepts
### A 30-minute module: five definitions, four frameworks, and the tie back to Jobs to be Done

This module runs **before** the product deep dive. Its purpose is narrow and
worth stating out loud to the room: the vocabulary in this space is used
loosely, mostly by people selling something, and you cannot analyse a market
whose five central nouns you cannot define. We fix five words, give each one a
framework you can actually apply, and then spend the last six minutes putting
them back inside the JTBD instrument from [`jtbd-framing.md`](jtbd-framing.md).

**One note on order.** The concepts are taught LLM → agent → multi-agent →
human in the loop → hybrid workforce. An agent is *defined in terms of* an LLM,
and a hybrid workforce is a consequence of all four. Teaching them in the order
people ask about them produces definitions that lean on words not yet defined.

---

## The card

Five sentences. Put them on one slide, make the room write them down, and leave
the slide up for the rest of the session.

| Term | One sentence |
| --- | --- |
| **LLM** | A model that turns text into more text — it can advise, and it cannot act. |
| **Agent** | An LLM placed in a loop with tools and a goal, deciding for itself what to do next and when it is finished. |
| **Multi-agent system** | Several agents with different contexts, tools or roles, coordinated toward a single objective. |
| **Human in the loop** | A designed point at which the system must stop and obtain a human decision before proceeding. |
| **Hybrid workforce** | An operating model that allocates *jobs* — not roles — across humans and agents as one pool of capacity. |

And the sentence that connects all five:

> An LLM produces **language**. An agent produces **consequences**. Everything
> else on this list — coordination, gates, workforce design — exists because of
> that second word.

---
---

# §1 — What is an LLM

## 1.1 The definition that is useful to a product person

The technical definition — a neural network trained to predict the next token
over a very large corpus — is true and almost useless in a product conversation.
The useful one:

> **An LLM is a function from text to text that generalises to tasks nobody
> built it for.**

That last clause is the entire commercial event. Software before 2022 could only
do what someone had specified in advance. An LLM handles instructions its
builders never enumerated. That is why it feels like a person and behaves like
infrastructure.

## 1.2 Three properties that determine everything downstream

| Property | What it means | The product consequence |
| --- | --- | --- |
| **Stateless** | It remembers nothing between calls. Everything it "knows" about your situation was put into the context window by someone. | Context assembly *is* the product. (Framework lens **B1**.) |
| **Probabilistic** | The same input yields a distribution over outputs, not one output. | You cannot test it like software. You design for wrongness. (**B8**.) |
| **Text-only** | It emits tokens. It has no hands, no clock, no memory, no access to anything. | On its own it can only *tell*. Acting requires the scaffolding of §2. |

## 1.3 Three confusions worth killing in ninety seconds

- **An LLM is not a chatbot.** Chat is a *user interface* that was easy to build
  around the model. It was the first interface, not the right one. (**B7**.)
- **An LLM is not a database or a search engine.** It does not look things up; it
  produces a plausible continuation. When the plausible continuation happens to
  be false, that is not a malfunction — it is the mechanism working normally.
  This is why grounding and citation exist. (**B2**, **B3**.)
- **An LLM is not deterministic software.** "It worked when I tried it" is not a
  test result. It is one sample from a distribution.

**The test for the room:** *if the system's only output is words on a screen for
a human to read and act on, you have an LLM product, not an agent.* Useful,
frequently the right answer, and a different design problem entirely.

---
---

# §2 — What is an agent

## 2.1 The definition

> **An agent is an LLM in a loop: it is given a goal, it chooses an action, it
> observes what happened, and it decides what to do next — including when to
> stop.**

Three words in there are load-bearing: **loop**, **chooses**, and **stop**. A
system that runs a fixed sequence you designed is not an agent no matter how
much AI is inside it. A system that cannot decide it is finished is not an agent
either; it is a very expensive random walk.

## 2.2 The anatomy — six parts, and what fails without each

| Part | What it is | What happens without it |
| --- | --- | --- |
| **Goal** | The objective, in the user's terms | The loop never terminates, because nothing defines "done" |
| **Model** | The reasoning core that picks the next action | You have a script |
| **Tools** | Its hands — read a file, call an API, search, send, write | It can only narrate what it *would* do |
| **Context / memory** | What it knows about this situation, and what carries across steps | It re-solves the same problem every step, and forgets what it already tried |
| **Loop** | Act → observe → decide again | One shot, no recovery from a bad step |
| **Stop & escalate** | When to finish, and when to hand back to a human | It either runs forever or fails silently — the two worst outcomes |

The sixth row is the one teams discover last and the one this course cares about
most. **Escalation is a designed path, not an exception.** An agent that has no
way to say "I don't know, here's what I've got" will invent its way past the
uncertainty, because that is what the underlying model does.

## 2.3 The distinguishing test

> **Who decides the next step — you, at design time, or the model, at run time?**

That single question separates a **workflow** from an **agent**, and it is a
dial rather than a switch. Run the room through five examples fast:

| System | Which? | Why |
| --- | --- | --- |
| A nightly script that summarises yesterday's tickets and emails the digest | **Workflow** | You fixed every step; the model fills one slot |
| A support bot that retrieves from a knowledge base and answers | **Workflow** | Retrieve-then-answer is your sequence, not its choice |
| A coding tool that reads the repo, edits, runs the tests, sees a failure, edits again, stops when green | **Agent** | It chose the sequence and the stopping condition |
| A refund system that reads the ticket, decides, issues refunds under ₹5,000, escalates above | **Agent, bounded** | It decides and acts — inside a fence you drew |
| Deep research: plans searches, reads, concludes it needs more, then writes | **Agent** | The plan is generated at run time |

**The line to land:**

> **"Agent" is not a compliment and "workflow" is not an insult.** Every step you
> hand to the model buys flexibility and sells reliability. Most systems that
> work in production are workflows with one agentic step in the middle.

## 2.4 The autonomy ladder

The framework to give them for classifying anything they meet.

| Rung | What is delegated | What the human still does | Example |
| --- | --- | --- | --- |
| **0 — Suggestion** | A completion | Everything, including accepting | Inline autocomplete |
| **1 — Assistant** | A task, one turn | States the task, does the work with the answer | ChatGPT, Perplexity |
| **2 — Workflow** | A fixed pipeline | Designed the pipeline; reviews output | Document processing, digests |
| **3 — Agent, attended** | A multi-step task, with approval on each action | Approves actions, reviews the result | Cursor, Claude Code, an ops copilot |
| **4 — Agent, unattended** | A whole task, on a trigger | Sets the goal and the guardrails; audits after | Scheduled research; an agent that opens a PR |
| **5 — Agent system** | A standing responsibility | Sets objectives, budget and escalation policy | The thing most vendors are selling and few are shipping |

**The point of the ladder is not to climb it.**

> **Autonomy is not a maturity level. It is a purchase, and the price is the cost
> of being wrong.** The rung is set by reversibility and blast radius, never by
> how capable the model has become.

**Artifact:** for any product the room names — what rung is it on, and what would
have to become cheap-to-be-wrong for it to move up one?

---
---

# §3 — What is a multi-agent system

## 3.1 The definition

> **Several agents — each with its own context, tools, and role — coordinated
> toward one objective.**

Note what is *not* in that definition: the number of models, the vendor, and the
org-chart metaphor. Two agents can run on the same model. The distinction that
matters is that they hold **different context** and have **different
permissions**.

## 3.2 The three legitimate reasons to add a second agent

| Reason | What it buys | Example |
| --- | --- | --- |
| **Context isolation** | A dirty sub-task doesn't pollute the main thread; the main agent keeps a clean, short context | A research subagent reads forty pages and returns eight lines |
| **Parallelism** | Wall-clock time, when sub-tasks are genuinely independent | Ten files reviewed at once |
| **Independent judgment** | An adversarial check by something that is not invested in the answer | A verifier agent whose only job is to try to refute the finding |

The third is the most valuable and the least used. A generator that also grades
itself grades generously. A separate agent, prompted to refute, catches things
the first one cannot see — for the same reason a second reader does.

## 3.3 The four coordination patterns

| Pattern | Shape | Best for |
| --- | --- | --- |
| **Orchestrator–worker** | One manager fans out, collects, synthesises | Breadth: search, review, audit |
| **Pipeline** | Specialists in a fixed sequence | Well-understood, repeatable production work |
| **Generator–critic** | One produces, one attacks, loop until it survives | Reliability on anything consequential |
| **Blackboard** | Shared state, agents act when relevant | Rare, and usually a sign the problem isn't decomposed yet |

## 3.4 The honest costs — spend real time here

The room will have been sold multi-agent systems as obviously better. They are
frequently worse, for four reasons that are structural rather than fixable:

1. **Reliability compounds downward.** Ten handoffs at 95% each is 0.95¹⁰ ≈
   **60%**. Put that arithmetic on the board. Adding agents multiplies error; it
   does not average it.
2. **Every handoff leaks context.** And this is the sharp one for this course —
   framework lens **C3** argues that AI's real value is that it *removed* the
   fidelity loss at the human handoff, because the person holding the context
   now does the work directly.

   > **A badly designed multi-agent system reintroduces exactly the handoff
   > problem that AI just removed. You have rebuilt the org chart — including
   > the parts of the org chart that don't work.**

3. **Cost and latency multiply**, and non-determinism makes it very hard to say
   which agent caused the bad output.
4. **Accountability diffuses.** Five agents and no one to ask what happened.

**The test:**

> **Add an agent only when it needs a different context, a different tool set,
> or a different incentive from the one you already have.** Never for symmetry,
> never because the human process had five people in it.

---
---

# §4 — What is human in the loop

## 4.1 Three postures, not one phrase

People say "human in the loop" to mean "don't worry, a person is involved." That
is a reassurance, not a design. There are three distinct postures and they have
different costs:

| Posture | Mechanic | The human's actual role | Cost |
| --- | --- | --- | --- |
| **In the loop** | The system **cannot proceed** without a decision | Decides, on the action path | Throughput — every gate is a queue |
| **On the loop** | The system proceeds; a human monitors and can intervene or abort | Supervises | Vigilance — attention decays |
| **After the loop** | The system acts; humans audit a sample later | Governs | Exposure — you find out afterwards |

Most real systems use all three at different points. The design question is never
"do we have a human in the loop"; it is **which posture, at which step, and who.**

## 4.2 Where the gate goes

> **Put the gate at the last reversible moment.**

Not at the start, where the human has nothing to look at and approves an
intention. Not after, where approval is theatre. At the final step before the
action becomes irreversible — the send, the payment, the merge, the delete.

The placement framework, and it is the one thing from this section that must
survive the session:

| | **Small blast radius** | **Large blast radius** |
| --- | --- | --- |
| **Reversible** | Let it run. Log it. | On the loop — visible progress, an abort, an undo |
| **Irreversible** | Confirm, with the evidence attached | **In the loop**, and a *named* accountable human |

Note what is not an axis on that grid: **model confidence.** A model's stated
confidence is another generated token. Gate on consequence, which you control,
not on confidence, which you don't.

## 4.3 The failure mode: the gate that is always approved

Ask a human to approve two hundred correct actions and they will approve the two
hundred and first, which is wrong. This is automation bias and it is extremely
well documented outside our industry — aviation, radiology, freight.

> **A gate that gets approved 99% of the time is not a control. It is a ritual,
> and it transfers liability to a person who was never actually able to check.**

Two consequences for product design:

- **A gate must carry its evidence.** An approval dialog that shows the action
  but not the reasoning, the inputs, or the diff produces rubber-stamping. This
  is the verification surface (**B3**) applied to actions rather than answers.
- **A gate must be affordable.** Count the gates per hour against the human's
  actual capacity. A gate the operator cannot keep up with will be removed by
  someone, officially or otherwise.

## 4.4 What HITL actually is, in JTBD terms

Straight back to the instrument in [`jtbd-framing.md`](jtbd-framing.md) §1.4:

> Human in the loop is an **anxiety instrument.** It belongs on the same shelf
> as citations, diffs, previews, sandboxes and undo. It is not a safety feature
> bolted on at the end; it is the mechanism by which a product makes an
> **anxiety-in-use** job hireable at all.

---
---

# §5 — The hybrid workforce

## 5.1 The definition, and the move it depends on

> **A hybrid workforce allocates jobs — not roles — across humans and agents as a
> single pool of capacity.**

The whole idea stands on one JTBD move: **a role is a bundle of jobs.** "Analyst"
is not a unit of work; it is thirty distinct jobs that were bundled because they
happened to require the same person to be in the same place with the same
context. Agents do not replace roles. They **unbundle** them, and someone then
has to re-bundle what is left.

The reason "will AI replace this job" is the wrong question is that it treats a
role as atomic. Decompose first, then ask.

## 5.2 The three destinations — and the one everyone forgets

Take a role, list its jobs, and send each one somewhere:

| Destination | Meaning | The test |
| --- | --- | --- |
| **Automate** | An agent does it end to end | The job has a checkable output and a bounded blast radius |
| **Augment** | A human does it, faster, with an agent | Judgment is inside the job, not just at the end of it |
| **Abandon** | Nobody does it any more | **The job existed only to work around a constraint that has now gone** |

Worked on a product manager's own week, which an MBA room will recognise:

| Job in the role | Destination | Why |
| --- | --- | --- |
| First draft of the PRD | Augment | The draft is cheap now; the argument still isn't |
| Chasing status across five teams | Automate | Bounded, checkable, and nobody wanted it |
| The weekly status deck | **Abandon** | It existed because gathering information was expensive. It isn't. |
| Deciding what *not* to build | Human | Accountability, and taste |
| Telling someone their project is cancelled | Human | Consent and relationship — delegating it is the message |

> **Abandon is the largest and least-claimed category.** A surprising share of
> corporate work is the residue of an old constraint: reporting, formatting,
> re-keying, summarising for people who could not attend, chasing. Automating
> that work preserves it. Ask first whether it should exist.

## 5.3 What stays human, stated precisely

"Creativity and empathy" is not an answer; it is a way of not having one. The
defensible list:

| What humans keep | Why it cannot move |
| --- | --- |
| **Accountability** | An agent cannot be answerable. Somebody must be, and that is a legal and social fact, not a capability gap. |
| **Standard-setting** | What "good" means here is a judgment about *this* organisation, and it is the input to everything the agents do |
| **Undocumented context** | The reasons that were never written down, and the ones nobody would write down |
| **Consent and relationship** | Who gets told what, by whom, and in what order |
| **Novel judgment under stakes** | The case that is genuinely not like the previous cases |

## 5.4 The new human work — the skill inversion, applied to a career

Lens **C4** says every AI product creates a new literacy. A hybrid workforce
creates one at the level of the job itself. Four new skills, and they are what
the room should actually take away:

1. **Specification** — saying what you want precisely enough that it can be done
   without you. Most people have never had to; delegation to humans hides
   imprecision behind their judgment.
2. **Verification** — checking output you did not produce, efficiently, without
   redoing it.
3. **Orchestration** — deciding what to delegate, to what, at which rung.
4. **Exception handling** — the escalated 10%, which is now the majority of what
   a human's day contains, and it is all hard cases with no easy ones in between.

That last point deserves a beat. **When you automate the routine, the human's
remaining day is uniformly difficult.** The easy cases used to be the recovery
time. This is a real and under-discussed cost of a hybrid workforce.

## 5.5 What management measures instead

| The old unit | The new unit |
| --- | --- |
| Headcount | **Cost per completed job** |
| Utilisation | **Autonomy rate** — % of tasks completed with no human touch |
| Cycle time | **Escalation rate**, and **time-to-verify** |
| Defect count | **Rework rate** — work returned after it was accepted |

> Once the economic unit is cost-per-completed-job rather than headcount,
> capacity planning stops being hiring. That is the actual organisational
> content of the phrase "hybrid workforce" — everything else is a slide.

## 5.6 Two failure modes to name before the room meets them

- **The centaur trap.** Pair every agent with a human reviewer and the reviewer
  becomes the constraint. You have automated production and left verification
  manual — which is lens **P3**, bottleneck migration, playing out inside an
  operating model. Throughput ends up capped by the humans you kept.
- **Verification debt.** Output grows faster than the capacity to check it, so
  checking quietly degrades into sampling, then into trust, then into finding
  out later. It is the Cursor observation generalised: *you can now generate far
  more than you can read.*

---
---

# §6 — Tying it back: JTBD in the agentic world

Six minutes, and the point of the whole module. Everything above is vocabulary;
this is the analysis.

## 6.1 What agents make abundant

Lens **C1** asks what human role just became free. For LLM products, the honest
answer was an **advisor** — someone who has read the material and will explain it
at 2am. For agents, the answer is different, and naming the difference is the
insight:

> LLMs made **an advisor** abundant. Agents make **a doer** abundant.
>
> What became free is not intelligence. It is **persistence** — attention
> sustained on your behalf, over time, while you are not watching.

You could always buy an answer. Books, consultants, tools, search. What you could
not affordably buy was **someone to keep doing the thing** — to watch for it, to
chase it, to keep two systems in agreement, to try again tomorrow. That is a
labour cost that scaled with duration, and duration is exactly what just went to
approximately zero.

## 6.2 Which class of jobs just became servable

Lens **P2** — the unservable job — is the core move of the course, and it
extends cleanly. The original test:

> *"What would this user have had to pay a human to do, and why didn't they?"*

The agentic extension adds an axis:

> **"What would they have had to pay a human to keep doing — and for how long?"**

Jobs that were unservable purely because they required **duration or vigilance**:

| The job, in the user's words | Why no one served it |
| --- | --- |
| "Tell me if anything in this contract set changes" | Somebody would have had to read them all, every month |
| "Keep these two systems saying the same thing" | A person doing reconciliation forever |
| "Chase this to done and only come back if it's stuck" | You cannot hire a fraction of a person for a fortnight |
| "Watch for this and wake me" | Nobody is paid to wait |

Every row is a **Pattern A** job in the pack's own taxonomy — a real job, no
mystery about the demand, and everyone had concluded people didn't want it
because nothing was being hired. They were reading a blocked force as an absent
job.

## 6.3 The four forces, re-scored for agents

The strongest slide in the module. Same instrument as §1.4, pointed at a new
class of product.

| Force | LLM assistant | Agent |
| --- | --- | --- |
| **PUSH** | I produce more language than I can type | **New and self-inflicted: assistants let me generate more work than I can execute or check** |
| **PULL** | Vivid. "It writes the thing." You can picture it, and the demo is compelling | **Weak. "It'll do it while you're not watching" is hard to picture — and a good agent's demo is nothing happening** |
| **ANXIETY** | Moderate, in use. Is this answer right? | **Very high, and different in kind: it acted, I wasn't there, I can't reconstruct what it did, and I am accountable** |
| **HABIT** | Low. Personal, easily broken | **High, and organisational: approval chains, audit requirements, "who signs off", existing process, existing headcount** |

Read the equation off that table — **PUSH + PULL > ANXIETY + HABIT** — and the
consequence is immediate:

> For agents, the two binding forces are **anxiety and habit**, and both are
> **organisational rather than individual.** The blocker on an agent sale is
> almost never capability. It is that nobody can say who is accountable when it
> is wrong, and the existing process has no slot to put it in.
>
> Which is the good news the pack has already made: anxiety and habit are the
> two forces a product team can actually work on.

Concretely, that means the roadmap of a serious agent product is mostly
**anxiety instruments** — traces, dry-run, sandboxing, scoped permissions,
spend limits, undo, gates, audit logs — and **habit instruments**: fitting the
existing approval chain instead of asking the organisation to replace it.

## 6.4 The Pull problem, which is specific to agents and badly under-appreciated

An agent that works produces **no event.** Nothing to watch, nothing to feel, no
moment of delight. The user's experience of a successful agent is an absence.

This is a genuine JTBD problem — Pull is weak because the outcome is invisible —
and it has a product answer:

> **The activity log is not a debugging tool. It is a Pull surface and an
> anxiety instrument.** Showing the work is how an agent product manufactures
> the evidence that anything happened, and how the user learns to trust it
> enough to stop watching.

Note the arc it implies: the trace exists to be read closely at first, then
skimmed, then ignored. **A well-designed agent product is one the user
progressively stops looking at** — and the product has to earn each step of
that. Most agent products are designed for day one and never for day ninety.

## 6.5 The job statement, rewritten for delegation

The template from §1.2 of the JTBD pack gains a fourth clause the moment the
work is delegated rather than performed:

> **When** *[circumstance]*, **I want** *[the agent]* **to** *[motivation]*,
> **so I can** *[outcome]* — **and I will accept it without checking when**
> *[condition]*.

That final clause is the product specification. It is what the team must earn,
it is what determines the rung on the autonomy ladder, and it is the only
honest measure of whether the agent has been hired. Ask it of any agent product
in the room and most teams discover they have never written the condition down.

## 6.6 The three eras — the slide to close on

The Wispr analysis in this pack turns on the observation that the *acceptable
outcome* moved: from output you could work with to output you could send
unedited. Agents move it once more, and the three-step arc is the cleanest
summary of the last four years that this pack can give:

| Era | What the user will accept |
| --- | --- |
| **Pre-generative AI** | Output I can work with |
| **Assistants** | Output I can send unedited |
| **Agentic** | **Work I didn't have to watch** |

> The job is the same in all three rows. **What moved is the standard** — which
> is exactly what JTBD says to look at, and exactly what feature-led analysis
> never sees.

## 6.7 The six questions — the artifact of this module

For any agentic product or proposal, in this order:

1. **What job is being delegated, and at what rung?** Not "what does it do" —
   what progress is a person no longer making themselves?
2. **What is the unit of delegated work, and how does the user know it's done?**
   If there is no definition of done, there is no agent — there is a process
   that never terminates.
3. **Where is the last reversible moment, and what happens there?**
4. **What is the evidence surface?** How does the user verify without redoing the
   work? If verification costs as much as doing it, nothing has been delegated.
5. **What does it do when it doesn't know?** Show me the escalation path. If
   there isn't one, the product's failure mode is confident fabrication.
6. **Who is accountable when it is wrong, and does the product make that
   person's job possible?** This is the question that closes agent deals and the
   one teams answer last.

## The closing question

Mirror the pack's own closing move.

> Generative AI created a new push by making us produce far more language than
> we ever have. **Agents create a new push by putting more work in flight than
> anyone can supervise.**
>
> Verification was already the bottleneck for code. It is about to be the
> bottleneck for everything an organisation does.
>
> **Where is the product for that side of the exchange?**

---
---

# Running it in thirty minutes

| Min | Segment | Land this |
| --- | --- | --- |
| 0–2 | The card. Five definitions, written down. | An LLM produces language; an agent produces consequences |
| 2–6 | **§1 LLM.** One capability, three properties, three confusions. | It can advise; it cannot act |
| 6–13 | **§2 Agent.** Anatomy, the who-decides test, the five-example round, the autonomy ladder. | Autonomy is priced by the cost of being wrong |
| 13–17 | **§3 Multi-agent.** Three reasons to add one, four patterns, the 0.95¹⁰ arithmetic. | Add an agent for context, tools or incentives — never for the org chart |
| 17–20 | **§4 Human in the loop.** In / on / after. The reversibility × blast-radius grid. | A gate approved 99% of the time is a ritual |
| 20–24 | **§5 Hybrid workforce.** Roles are bundles of jobs. Automate / augment / **abandon**. What stays human. The new metrics. | Unbundle the role before asking whether AI replaces it |
| 24–30 | **§6 Tie-back.** Persistence became abundant → the duration test → the four forces re-scored → the three eras → the six questions → the closing question. | For agents, anxiety and habit are binding, and both are organisational |

**If you are short on time**, cut §3.3 (the coordination patterns) and the PM
week table in §5.2. **Never cut §6.3.** The re-scoring of the four forces is the
only part of this module that is analysis rather than vocabulary, and it is the
bridge to the Wispr deep dive that follows.

**If you have longer**, the natural extensions are the generator–critic pattern
worked in detail (§3.3) and a live teardown: take any agent product the room
names and run the six questions of §6.7 against it on the board. Ten minutes,
and it exposes more than a case study.

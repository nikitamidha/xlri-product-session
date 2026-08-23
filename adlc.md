# ADLC — The AI Development Lifecycle
### Topic 1: the theory, the published frameworks, and where they disagree

> **Read this before the frameworks:** ADLC is not a settled term. Two different
> ideas are competing for the acronym right now, published by different camps,
> and neither has conceded. Most confusion in the room will come from people
> silently holding different definitions. **Resolve it in the first two minutes
> or the session will drift for twenty.**

---
---

# Part 0 — The acronym collision

## The two ADLCs

| | **ADLC-A** — *AI-Driven / AI-assisted Development Lifecycle* | **ADLC-B** — *Agentic Development Lifecycle* |
| --- | --- | --- |
| **Question it answers** | How do humans and agents *build software together*? | How do you build and operate software *that is itself probabilistic*? |
| **The thing that became non-deterministic** | The **process** — the agent writing the code | The **product** — the agent running in production |
| **Output** | Ordinary deterministic software, built a new way | An agent whose behaviour drifts, and which must be governed |
| **Who publishes it** | AWS (AI-DLC), GitHub (Spec Kit), Kiro, Kent Beck, Addy Osmani, Thoughtworks, DORA | EPAM, IBM, DataRobot, LangChain, Cycode |
| **Central anxiety** | *Did the agent build the right thing, and can I trust the code?* | *Will this thing still behave next Tuesday?* |
| **Where the discipline goes** | Into the **specification** | Into the **evaluation** |

## The claim worth teaching

Most write-ups pick one and pretend the other doesn't exist. That is the mistake.

> **For an AI-native product, ADLC-A and ADLC-B are the same lifecycle.**
> You build agentically, and what you ship is an agent. Non-determinism enters
> at *both* ends — in the making and in the made — and a lifecycle that only
> absorbs one of them will fail at the other end.

This is why the two topics in this course are sequenced the way they are. ADLC
is the *how*. The JTBD work is the *what*. And the reason ADLC has to come first
is that in an AI-native product **the build method leaks into the product**: a
team that cannot get a deterministic answer out of an agent internally will not
ship a product that gives users one.

**Ask the room, before anything else:** *"When you say ADLC, are you asking how
you'll build, or what you'll build?"* Then teach both, in that order.

---
---

# Part I — Why SDLC actually breaks

Not "AI makes coding faster." That is a productivity claim, it is contested (see
METR in Part II), and it is not the interesting part. The interesting part is
that **four load-bearing assumptions of the software development lifecycle stopped
holding at the same time.**

SDLC — waterfall, Agile, DevOps, all of it — is a set of controls built on top of
four premises. Take each away and see what collapses.

---

## S1 — "Producing code is the expensive step"

Every ceremony in Agile exists because writing code was slow, so committing to
the *wrong* code was ruinous. Sprints, estimation, story points, WIP limits, the
whole apparatus is **risk management around an expensive irreversible act.**

Generation is now cheap and, crucially, **near-disposable**. The cost of an
attempt has fallen by one to two orders of magnitude. Kim and Yegge's argument
for why this matters is the strongest one in the canon: it isn't speed, it's
**optionality** — you can now afford to build the thing you would previously only
have argued about.

> **The consequence nobody has fully absorbed:** if attempts are cheap, then
> *deciding what to attempt* is no longer risk management. It's the entire job.

**The test:** if your process still spends most of its ceremony on protecting
against wasted implementation effort, you are running SDLC controls over ADLC
economics.

---

## S2 — "Code is the artifact of record"

In SDLC, the spec is scaffolding — it decays, drifts from the code, and everyone
knows the code is the truth. Documentation is a lie you maintain out of duty.

Spec-driven development inverts this and it is the single biggest structural
change in the whole field:

> **The specification is the primary, durable artifact. Code is a regenerable
> output.**

AWS states this as a design goal explicitly — AI-DLC is documentation-first, such
that *if all the code were deleted, the complete record of what was built and why
survives.* That sentence would have been absurd in 2019. It is coherent now only
because regenerating the code from the record is a real option.

**The consequence:** the highest-leverage document in the repository is no longer
the architecture diagram. It is whatever file the agent reads before it starts —
the constitution, the steering doc, the `CLAUDE.md`. **That file is now
production infrastructure.**

---

## S3 — "The same input produces the same output"

This is the assumption engineering has never had to question. Martin Fowler's
framing is the clearest: we are moving from deterministic to **non-deterministic
computing**, where the same prompt yields one answer today and a different one
tomorrow, because the machine is reasoning statistically rather than executing.

Everything downstream of determinism has to be rebuilt:

| Deterministic world | Non-deterministic world |
| --- | --- |
| Tests pass or fail | Evals score on a distribution |
| A bug is reproducible | A failure has a *rate* |
| Fixed by a patch | Fixed by changing a prompt, a tool, a model, or the context |
| Regression = a red build | Regression = a drift you only see in aggregate |
| Deployment is closure | Deployment is the *start* of the measurement |

**This is where ADLC-A and ADLC-B stop being separable.** Non-determinism in the
process demands the same instincts as non-determinism in the product: measure
behaviour in aggregate, never trust a single observation, and treat "it worked
when I tried it" as noise.

---

## S4 — "Review capacity scales with authoring capacity"

Code review works because the person reviewing wrote code at roughly the same
rate as the person authoring. One human, one stream, comparable speed.

That ratio is now broken — one human supervising several agents, each producing
faster than a human can read. **Verification is the new bottleneck, and it is a
human bottleneck, which means it does not fall with the next model release.**

Böckeler's field observation is the honest one: working with agentic assistants
means intervening, correcting and steering *constantly*. That is not a
transitional cost while the tools mature — it is the shape of the work.

Addy Osmani's **"70% problem"** names the same thing from the other side: AI gets
you most of the way there startlingly fast, and the residual is where all the
engineering judgment lives. The last 30% does not shrink in proportion to how
fast you covered the first 70%.

---

## The compression

> SDLC put its discipline where the cost was: **in producing code.**
> In ADLC, producing code is cheap and two other things are expensive:
> **saying precisely what you want**, and **knowing whether you got it.**
>
> **Every framework in Part II is an attempt to put engineering discipline back
> into one of those two places.** That is the single lens that organises the
> entire literature.

---
---

# Part II — The canon

What has actually been written down, by whom, and what each one is *for*. Sorted
by which end of the problem it attacks.

---

## Group 1 — Fixing the front end: specification

### AWS **AI-DLC** (AI-Driven Development Life Cycle)

The most complete named methodology, and the only one from a major vendor that
tries to replace the whole lifecycle rather than patch part of it. Open-sourced
as `awslabs/aidlc-workflows`.

- **Three phases:** **Inception** (what to build and why) → **Construction**
  (how) → **Operations** (deploy, monitor, production readiness).
- **Mob Elaboration:** AI turns business intent into requirements, stories and
  **units of work** — and the *whole team* validates the AI's questions and
  proposals together. Note what this is: Agile's ceremonies re-pointed at
  reviewing machine output instead of producing human output.
- **Steering rules as blocking constraints.** Rules load from
  `.kiro/steering/`, `.amazonq/rules/` and gate progression between stages. This
  is the important engineering idea — **the process is enforced in the harness,
  not in the humans' discipline.**
- **Adaptive, not waterfall** — it claims to execute only the stages that add
  value for the request at hand.
- **Human in the loop is the stated core tenet:** agents propose, humans approve.

**Where it's weak:** "adaptive" is doing heavy lifting. Three sequential phases
with mandatory gates is structurally a waterfall, and the burden is on AWS to
show the adaptivity is real rather than a naming choice.

### **GitHub Spec Kit**

The most adopted open-source implementation, agent-agnostic, and the one to demo
because the workflow is legible in six words:

> **Constitution → Specify → Plan → Tasks → Implement → PR**

The **constitution** is the concept worth stealing: a project's non-negotiable
principles, written once, injected into every agent invocation. It is the
closest thing the field has to a *values file for a codebase*.

### **Amazon Kiro**

Spec-first IDE. Three primitives worth naming because they generalise:
**specs** (requirements → user stories → acceptance criteria → design → tasks),
**steering docs** (long-lived architecture decisions, conventions, domain rules),
and **hooks** (event-triggered agent actions).

### The load-bearing critique of this entire group

Scott Logic put it directly in the title: *"Radical Idea or Reinvented
Waterfall?"* It is the right question and you should put it to the room rather
than answer it.

**The defence, and it is a good one:** waterfall's fatal flaw was that the
feedback loop from spec to working software took months. If regenerating an
implementation from a spec takes twenty minutes, a heavy upfront spec is no
longer a bet you can't unwind. **Waterfall was bad because iteration was
expensive, not because specifying was.**

---

## Group 2 — Fixing the practitioner: how to actually work with the thing

### Kent Beck — **augmented coding vs. vibe coding**

The cleanest conceptual distinction anyone has drawn, and it is a distinction
about **what you are willing to be responsible for.**

| | Vibe coding | Augmented coding |
| --- | --- | --- |
| What you care about | The system's **behaviour** only | Behaviour **and** the code — its complexity, its tests, their coverage |
| On an error | Feed it back to the genie and hope | Diagnose it; you own the fix |
| Value system | New | **Identical to hand-coding: tidy code that works** |
| Who's responsible for quality | Ambiguous | You. The AI does the typing; the standard is unchanged |

Beck's **"unpredictable genie"** metaphor is the most useful teaching image in
the canon: it grants your wishes, but often in unexpected and illogical ways.
It correctly sets expectations for both what agents give you and what they cost
you — and unlike "copilot" or "assistant", it does not flatter the tool.

### Andrej Karpathy — **vibe coding** (the origin)

Worth naming as the origin point, and worth being precise about: Karpathy
described it as a mode for throwaway weekend projects. **The industry took a
description of a low-stakes mode and treated it as a methodology.** Most of the
Beck/Osmani corrective literature exists to undo that.

### Gene Kim & Steve Yegge — ***Vibe Coding*** (IT Revolution, foreword by Dario Amodei)

- **FAAFO** — the five dimensions of value: **Fast, Ambitious, Autonomous, Fun,
  Optionality.** Of these, **Ambitious** and **Optionality** are the ones with
  strategic content: the economics of what is *worth building at all* changes,
  which is a portfolio argument, not a productivity argument.
- **The Three Developer Loops** — the classic inner/outer loop model is
  insufficient once agents are in the mix; they add a third.

### Addy Osmani — ***Beyond Vibe Coding: From Coder to AI-Era Developer*** (O'Reilly)

The professional-practice corrective. His thesis in one line: **vibe coding is
not the same as AI-assisted engineering.** The latter keeps technical design
documents, stringent code review, and test-driven development — it just does them
around a much faster generator. Plus the **70% problem** (see S4).

### Martin Fowler & Birgitta Böckeler (Thoughtworks)

The most intellectually serious ongoing body of work, and the only one treating
this as a *control systems* problem rather than a tooling problem:

- **Non-deterministic computing** as the paradigm shift (Fowler).
- **Guides and Sensors** — the agent as a system to be regulated: guides
  constrain what it does, sensors tell you what it did. This is a cybernetic
  governor, and it is the right abstraction, because it is the only one in the
  canon that scales as agents get more autonomous rather than less relevant.
- **Context engineering for coding agents** — the discipline of what the agent
  can see, which has quietly become the highest-leverage variable in the loop.
- Böckeler's field reports on constant intervention and steering — the honest
  empirical account.

---

## Group 3 — Fixing the back end: verification

### Hamel Husain & Shreya Shankar — **evals and error analysis**

The pivot point between ADLC-A and ADLC-B, and the most directly transferable
skill in this entire document for a product audience.

Their core claim is deliberately unglamorous:

> **Look at your actual production data, by hand, before you build any automated
> metric. Your evaluation strategy should emerge from observed failure patterns,
> not from predetermined categories.**

The method — error analysis, open and axial coding of failures, then
LLM-as-judge built *on top of* what you found, then production monitoring. Note
that open/axial coding is borrowed from **qualitative social science**, which is
the tell: **evaluating a probabilistic product is closer to grounded-theory
research than to QA.**

**Why this belongs in a product course and not an engineering one:** error
analysis is not a technical skill. It is the same skill as reading user research.
Which is why they claim PMs are often better at it than engineers.

### DORA — **2025 State of AI-assisted Software Development** & the **AI Capabilities Model**

The evidence base. ~5,000 respondents, 100+ hours of qualitative interviews,
under the DORA lineage (Forsgren, Humble, Kim). ~90% of developers using AI daily.

**The headline finding, and the one to lead with:**

> **AI is an amplifier.** It magnifies the strengths of high-performing
> organisations and the dysfunctions of struggling ones.

That is a devastating finding for anyone selling AI as a fix. **It says AI is a
multiplier on an existing coefficient — and if your coefficient is negative,
you are buying a faster route downhill.**

**The seven capabilities that amplify AI's benefit:**

1. Clear and communicated AI stance
2. Healthy data ecosystems
3. AI-accessible internal data
4. Strong version control practices
5. Working in small batches
6. User-centric focus
7. Quality internal platforms

**Teach the composition of that list, not the list.** Only two or three are about
AI at all. **Version control, small batches, user focus and platform quality are
1990s–2010s engineering hygiene.** DORA's actual finding is that the
prerequisites for benefiting from AI are overwhelmingly the prerequisites for
being good at software, full stop.

### METR — the randomized controlled trial

The necessary counterweight, and the reason to distrust every vendor
productivity number including the ones above.

- 16 experienced open-source developers, 246 real tasks in their own mature
  repositories (22k+ stars, 1M+ LOC), randomized AI-allowed vs. AI-disallowed.
- Forecast before: **24% faster.** Self-assessed after: **20% faster.**
  Measured: **19% slower.**

**The finding is not "AI doesn't work."** The finding is the **perception gap** —
a ~39-point swing between what practitioners experienced and what happened.
People are not reliable instruments for measuring their own productivity in this
domain, *even after doing the work.*

**Caveats, stated honestly, because the study is routinely misused in both
directions:** small n; Feb–June 2025 tooling; expert developers in codebases they
already knew deeply — the condition where AI's context advantage is smallest.
METR itself now labels the result historical.

**How to use it in class:** not as a debunk. As the reason ADLC needs
*measurement* rather than vibes — which is exactly the same argument evals make
about products. The through-line of this whole topic is: **your felt sense of
whether the machine is helping is not evidence.**

---

## Group 4 — ADLC-B: the agentic lifecycle proper

Less mature, more vendor-authored, no canonical owner yet. Published by EPAM,
IBM, DataRobot, LangChain, Cycode. The stages converge on roughly:

> **Define → Build → Evaluate → Deploy → Observe → Govern**, run as a loop, not a line.

The ideas worth carrying over even though the sources are commercial:

- **Capability envelope** — define what the agent may and may not do *before any
  code exists*. This is a product decision, not an engineering one, and it is
  the single most under-taught artifact in AI product work.
- **Deployment is not closure.** It is the beginning of the measurement period.
  This is the cleanest one-line difference from SDLC.
- **Governance is continuous, not a gate** — versioning, rollback, sandboxing,
  a gateway pattern for policy enforcement.
- **Drift is expected**, not exceptional. Model updates, changing user
  behaviour, and shifting context all move behaviour without anyone shipping.

**The number these sources all cite:** Gartner's forecast that **over 40% of
agentic AI projects will be cancelled by end of 2027** — for escalating costs,
unclear business value, and inadequate risk controls. Use it as a framing
device, but flag its status: it is a vendor-analyst *forecast*, not a
measurement, and it is quoted far more often than it is examined.

---
---

# Part III — The synthesis I'd actually teach

The frameworks above disagree on vocabulary and agree on structure. Underneath
all of them is one loop with five beats.

> ### The ADLC loop
>
> **1. Intent** — write the thing that is not the code: constitution, spec,
> steering, capability envelope. *This is now the durable artifact.*
>
> **2. Delegation** — decompose into units an agent can hold in context; choose
> the harness, the guides, the sensors. *Context engineering lives here.*
>
> **3. Generation** — cheap, parallel, disposable. *The step everyone stares at,
> and the least interesting one.*
>
> **4. Verification** — tests and review for deterministic output; **evals and
> error analysis for probabilistic output.** *The bottleneck.*
>
> **5. Operation** — for AI-native products, behaviour drifts after ship.
> Observe, govern, and feed findings back into 1.

## The point of the loop is not the loop

Every process model since the 1970s has roughly these beats. **What changed is
where the cost sits.**

| | SDLC | ADLC |
| --- | --- | --- |
| **1. Intent** | Cheap, and decayed on contact with code | **Expensive, and permanent** |
| **2. Delegation** | Sprint planning | **Context engineering** |
| **3. Generation** | **The expensive step. All controls point here.** | Near-free, disposable |
| **4. Verification** | Proportional to authorship | **The bottleneck. Human-bound.** |
| **5. Operation** | Closure | **The measurement period begins** |

**Read the canon through that table and it organises itself:**
spec-driven development is engineering discipline restored to **beat 1**;
evals are engineering discipline restored to **beat 4**;
guides-and-sensors is a control loop wrapped around **beats 2–4**;
DORA is the organisational precondition for any of it working;
METR is the reason you must measure beats 3 and 4 rather than feel them.

---

## Three tests for the room

**T1 — The artifact test.** *If your repository were deleted but your specs
survived, could you rebuild? If your specs were deleted but the code survived,
could you?* Whichever answer is "yes" tells you which lifecycle you are actually
running, regardless of what you call it.

**T2 — The bottleneck test.** *Name the step your team spends the most time on.*
If it is still writing code, the tooling changed and the process didn't. If it
is reviewing and verifying, you are in ADLC and should be investing there — most
teams are still investing in generation.

**T3 — The determinism test.** *When your product misbehaves, can you state the
failure rate?* If the only available answer is "it happened to a customer once,"
you are shipping a probabilistic product with deterministic instrumentation. That
is the most common failure mode in AI product work.

**Artifacts:** one sentence each — *"Our durable artifact is ___."* /
*"Our bottleneck is ___, and we spend most of our effort on ___."* /
*"Our worst failure mode occurs at a rate of ___."* The gap between the second
sentence's two halves is usually the whole diagnosis.

---
---

# Part IV — Where the canon genuinely disagrees

Do not resolve these in class. Put them up and let the room fight. They are the
live edges of the field, and a session that pretends there is consensus is
teaching something false.

| Question | One side | The other |
| --- | --- | --- |
| Is spec-driven development reinvented waterfall? | Scott Logic raises it seriously; three gated phases look like 1970 | Waterfall failed because iteration was expensive; cheap regeneration removes the flaw, not just the symptom |
| Does AI make developers faster? | FAAFO; ~90% daily adoption; DORA's throughput findings | METR: −19% measured, +20% perceived, in the expert case |
| Should you care about the code the agent wrote? | Karpathy's original vibe coding: care about behaviour | Beck, Osmani: the value system is unchanged; you own the quality |
| Is the human in the loop permanent or transitional? | Böckeler: constant intervention is the shape of the work | The autonomy trajectory says the ratio keeps shifting |
| Is the bottleneck moving again? | Verification is human-bound, so it stays | If AI verifies AI, it moves to *intent* — and intent is a product skill, not an engineering one |

**That last row is the one to leave them with**, because it is the bridge to
Topic 2: if the terminal bottleneck of software is knowing precisely what should
exist, then **the discipline that matters most in an AI-native world is the one
that specifies user problems rigorously.** Which is Jobs to be Done.

---
---

# Part V — Session notes

**If you get 20 minutes:** Part 0 (the collision, 2 min) → S1 and S4 only
(4 min) → Beck's vibe/augmented table and the genie (3 min) → DORA's amplifier
finding and the composition of the seven (4 min) → METR's perception gap
(3 min) → the cost-location table from Part III (4 min). **Cut the vendor
methodologies before you cut the evidence.**

**If you get a full session:** add Group 1 in full with Spec Kit demoed live —
the six-word workflow is the fastest way to make the abstraction concrete — and
Group 4 as the bridge into Topic 2.

**The one slide, if you only get one:** the SDLC-vs-ADLC cost-location table.
Everything else in this document is a footnote to where the cost moved.

---

## A note on source quality

Following the discipline of the rest of this pack:

| Tier | Sources |
| --- | --- |
| **Empirical research** | METR RCT (n=16, 246 tasks, preregistered, arXiv 2507.09089); DORA 2025 (~5,000 respondents, 100+ hrs qualitative) |
| **Practitioner accounts from named, accountable authors** | Beck, Fowler, Böckeler, Osmani, Kim & Yegge, Husain & Shankar |
| **Vendor methodology** — useful, but marketing a product | AWS AI-DLC, Kiro, Spec Kit, EPAM, IBM, DataRobot, LangChain, Cycode |
| **Analyst forecast** — quote with the label attached | Gartner's 40%-cancellation figure |
| **Uncited aggregation** — do not build on it | The large volume of SEO content on "ADLC vs SDLC" that recycles the above without attribution |

**Two honest caveats.** First, the AI-DLC and agentic-lifecycle material is
overwhelmingly Tier 3 — vendor-authored, unreplicated, and shaped by the product
each vendor is selling. Second, the field is roughly eighteen months old; every
framework here has been revised at least once, and none has survived long enough
to have been proven wrong. **Teach it as a live argument, not a body of
knowledge.** That framing is more honest and it is also more interesting.

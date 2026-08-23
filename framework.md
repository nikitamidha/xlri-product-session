# The Three Questions
### A product-thinking framework for AI-native products

The whole course hangs off three questions, asked in this order. They are not a
checklist; they are a sequence, and the order matters. You cannot see the new
problem until you have named the context shift, and you cannot evaluate what a
team built until you have named the problem they were actually solving.

> **I. How has the context shifted for the user?**
> **II. How have the problem statements shifted?**
> **III. What is being built as a result — at a deeper level?**

Sixteen lenses across the three. Four, four, and eight — Part III carries the
most weight because it is where product craft actually lives, and it is the part
almost every AI course skips in favour of strategy.

Worked throughout on **NotebookLM / Gemini Notebook**, with **Cursor** as the
recurring contrast.

---
---

# Part I — The Context Shift

Not "what can AI do now." **What changed in the user's world.** These four lenses
force the answer to be about a person, not a technology.

---

## C1 — The abundance flip

**Question:** Name precisely what just became free. Not a capability — a
**resource**, of the kind you could previously only get from a person.

Most teams answer this badly. "AI got good at reading documents" is a capability.
The product-thinking answer names the human role that just became abundant:

| Product | The role that became free |
| --- | --- |
| NotebookLM | A research assistant who has read every document you gave them, is available at 2am, never gets bored of your questions, and will re-explain in whatever form you ask for |
| Cursor | A collaborator who has read the entire codebase and will attempt anything without ego |
| Midjourney | An illustrator who will do forty versions and never resent you for it |

**The test:** if you cannot name a specific human role that just became abundant,
you probably do not have an AI-native product — you have a feature.

**Push further, because this is where the insight is.** Ask *why* that role was
scarce. Rarely just cost. It was **socially expensive**: you could not ask a
colleague to re-explain a paper four times. You could not ask a designer for a
fortieth variation. The abundance flip removes an embarrassment tax, and products
that understand that design differently from products that think they are selling
labour savings.

**Artifact:** one sentence — *"This product makes ___ abundant, and that role was
previously scarce because ___."*

---

## C2 — The new scarcity

**Question:** The constraint never disappears. Where did it move?

When generating understanding becomes free, what becomes scarce is **attention to
consume it, judgment about which to trust, and taste about what to ask for.**

NotebookLM can turn one corpus into an audio overview, a video, a mind map, a
slide deck, an infographic, a data table, a quiz and a set of flashcards — in
about a minute. **You cannot consume all of them.** The abundance of output
created a selection problem that did not previously exist, and the product had to
grow a surface to solve it. That is precisely what the Studio panel is: not a
menu of features, but the product taking responsibility for the scarcity it
created.

**The general form, and the most useful sentence in Part I:**

> Every AI-native product manufactures a new scarcity. **The mature version of
> the product is the one that takes responsibility for it.**

**Artifact:** name the scarcity your product created, and point at the specific
surface that manages it. If there is no such surface, you have found the roadmap.

---

## C3 — The capability transfer

**Question:** Work just crossed a boundary it could not cross before. Draw the
boundary and say who is on each side now.

- Research-assistant work → the principal investigator
- Paralegal work → the solo lawyer
- Illustration → the person who had the idea
- Analysis → the person who owns the question

**The subtlety that makes this lens worth teaching:** the transfer is usually
*from a specialist to the person who holds the context*, and that direction is
the actual unlock. When you delegate, you lose fidelity — the specialist never
quite knows what you meant, and you never quite know what they assumed. The
capability transfer is valuable less because it saves labour and more because it
**preserves context that used to leak at the handoff.**

This reframes what the product is for. A product built on "we save you money on
research assistants" builds differently from one built on "you no longer have to
explain what you're looking for to someone who wasn't in the room."

**Artifact:** a before/after handoff diagram, with the fidelity loss at the old
handoff labelled explicitly.

---

## C4 — The skill inversion

**Question:** What does the user stop needing to be good at, and what must they
newly be good at?

**NotebookLM:**

| Obsoleted | Newly required |
| --- | --- |
| Skimming for gist | **Source curation** — what goes into the notebook is now the highest-leverage decision the user makes |
| Manual note-taking | Question formulation |
| Remembering where you read something | Detecting a confident wrong answer |

**The product consequence:** every AI-native product creates a **new literacy**.
If the product does not teach it, users will fail and blame the product. Look for
where the teaching happens — onboarding, empty states, defaults, the examples in
the placeholder text. In NotebookLM, the entire design of the source panel is an
argument about what the user should care about.

**Artifact:** the new literacy your product demands, and the specific surface
where it is taught. Most teams discover they teach it nowhere.

---
---

# Part II — The Problem Statement Shift

The central claim of the course, and the hardest thing to get a room to accept.

---

## P1 — The honest old problem

**Question:** Write the pre-AI problem statement **in the user's words**, not the
category's.

Not "document comprehension tooling." Rather:

> *"I have forty PDFs for this review. I have read six. It's Tuesday and the
> thing is due Thursday, and I already know I'm going to cite the six I read."*

Category language hides the job. Insist on the first person, a specific number,
and a deadline. If the problem statement could appear in a market-sizing slide,
it is not yet honest.

---

## P2 — The unservable job

**The core move of the entire course:**

> **AI-native products rarely solve the old problem better. They make a
> previously *unservable* job servable.**

The old problem — "summarise this document" — was already served, badly, by
skimming, by abstracts, by asking a colleague. Serving it better is a feature.

The unservable job is different: *"help me hold twelve documents in my head at
once and notice where they disagree."* No product did this. No **person** did
this affordably. It never appeared on a roadmap because it was never a market.

**Audio Overviews is the cleanest example in the industry.** The job is *"I want
to absorb this while walking the dog."* Entirely real, entirely universal,
entirely unservable — the only way to serve it before was to hire two people to
record a podcast about your specific documents, which is an absurd sentence. That
absurdity is exactly why it was never built, and exactly why nobody requested it.

**The test students should apply to every product they look at:**

> *"What would this user have had to pay a human to do, and why didn't they?"*
>
> If the answer is **"they couldn't afford it"** or **"it would have been weird
> to ask"** — you have found the unservable job.

**Corollary, and it stings:** your users cannot request the unservable job,
because people do not request things that don't exist. They will ask you for a
better version of the servable one. **A roadmap built purely from user requests
will systematically miss every unservable job.** This is not an argument against
listening to users. It is an argument that requests tell you about the old
problem and behaviour tells you about the new one.

**Artifact:** the servable job and the unservable job, side by side, with the
reason the second was never served.

---

## P3 — The bottleneck migration

**Question:** Draw the user's workflow before and after. The constraint moves; it
never vanishes. Where is it now?

- **NotebookLM.** Before: reading was the bottleneck. After: reading is nearly
  free, and the bottleneck is **deciding what to trust and what to read next.**
- **Cursor.** Before: writing code was the bottleneck. After: **review is the
  bottleneck.** You can now generate far more code than you can read. This single
  sentence explains more about AI coding products than anything else in the
  course.

**The product consequence, and the reason this lens exists:** investment must
follow the bottleneck. It is why NotebookLM put more design into the citation and
source panel than into the chat box, and why Cursor's diff view matters more than
its prompt box. **Teams that keep optimising the old bottleneck ship products
that get faster at something nobody is waiting on.**

**Artifact:** before/after workflow, bottleneck marked in each, and an honest
audit of where the team's last three quarters of effort actually went.

---

## P4 — The problems you created

**Question:** What failure modes exist *only because this product exists?*

For NotebookLM:

- **Confident wrong synthesis.** Individually correct sources, an inference across
  them that no source supports.
- **The unchecked citation.** Citations make output verifiable. Most users will
  never verify. The citation is doing trust work far beyond the checking it
  actually receives.
- **Warmth as a trust exploit.** Two hosts chatting warmly about your documents
  signal a confidence the content may not have earned. Conversational register
  carries credibility that has nothing to do with accuracy — and it is the
  feature's whole appeal. **You cannot fix this without making the product
  worse**, which is what makes it a genuine product-ethics question rather than a
  bug. Spend real classroom time here.
- **Curation error amplification.** One bad source now speaks with exactly the
  same authority as the good ones.

**Artifact:** three failure modes the product created, and for each, whether the
team mitigated it, disclosed it, or accepted it. All three are legitimate
answers. Pretending there are none is not.

---
---

# Part III — What's Actually Being Built

Eight primitives. None of them existed as product categories before 2022, and
none of them are model capabilities — they are **design responses to
probabilistic output**. This is the part of AI product work that is genuinely
new, and the part that transfers to whatever your students build.

---

## B1 — Context is the product

Features are copyable in a weekend. **What the system knows is not.**

NotebookLM's identity is a single sentence: *the corpus is yours*. Everything
follows — the upload flow, the source panel, the 200-document ceiling, format
support, the sync between the Gemini app and the standalone site. The
infrastructure for getting context *in* is the actual product, and it is the
least glamorous surface in the whole thing.

**Ask of any AI product:** how much of the roadmap is context acquisition versus
model interaction? Teams over-invest in the second and wonder why the product
feels shallow.

---

## B2 — Grounding as deliberate restriction

In **mid-2022** — before "RAG" was common vocabulary — the team decided the
assistant would answer **only** from your sources.

Sit with what that costs. It makes the product worse on every general benchmark.
It makes it unable to answer obvious questions. It generates support complaints.

And it is the reason anyone trusts it.

> **Restricting capability in order to buy trust is the most under-taught product
> move in AI.**

Students will immediately propose a toggle: let the model use world knowledge,
clearly labelled. Make them price it. The moment a user cannot tell at a glance
whether an answer came from their sources or from the model's memory, **every**
answer becomes unverifiable — including the grounded ones. The toggle does not
add an option; it removes the guarantee. The whole value of a hard constraint is
that it is hard.

This is the single best exercise in the course for teaching that **a product
decision can be the deliberate refusal of a capability you already have.**

---

## B3 — The verification surface

Because output is probabilistic, an AI-native product must be designed around
**how the user checks it**. This is a UI category with no pre-AI ancestor.

| Product | Verification surface |
| --- | --- |
| NotebookLM | Inline citations that jump to the exact source passage |
| Cursor | The diff view |
| Image tools | Side-by-side variations |

**The design question is friction calibration.** Too much and nobody verifies;
too little and verification is decorative — present, unused, and doing trust work
it hasn't earned. Ask: what percentage of users click through a citation, and
what would the team consider healthy? Most have never asked.

---

## B4 — Intent elicitation

Pre-AI products assumed the user knew what they wanted and the interface's job was
efficient expression. **AI-native products must help the user discover what they
want.**

Mechanisms worth cataloguing: suggested questions on an empty notebook,
variations and re-rolls, the "Customize" note you pass to the audio hosts before
generation, and mind-map branches that open a grounded chat when clicked —
**navigation and inquiry fused into one gesture**, which is a genuinely new
interaction pattern worth a slide of its own.

**Ask:** where does your product assume the user can specify, and what happens to
the user who can't?

---

## B5 — Output modality as a product decision

**The answer does not have to have the shape of the question.** This is the
biggest under-exploited product lever in AI right now, and NotebookLM is the
industry's clearest demonstration.

The Studio panel is a **systematic search** over one question: *what shape should
understanding take?* Audio overview. Video overview. Mind map. Slide deck.
Infographic. Data table. Quiz. Flashcards.

Each is a hypothesis about a **different moment in the user's day and a different
mode of cognition** — commuting, presenting, orienting, revising, teaching. Same
corpus, same model, radically different products.

**Exercise, and it is the best single exercise in the course:** for your product,
list five output modalities you have never shipped, and name the moment in the
user's day each one serves. Teams routinely find their next two years here.

---

## B6 — The craft layer beneath the model

**The quality users feel usually comes from everything that is not the LLM.**

Audio Overviews is the proof. The micro-interjections — *"Oh really?"*,
*"Totally"*, the pauses, the *"uh…"* — are **not in the LLM's transcript.** They
are built into the audio model itself. And the generation is a four-stage
pipeline: analyse the sources, **plan an explanation**, script a host exchange,
then perform it as audio.

Four product decisions, not one model call. The one everyone notices — the
uncanny naturalness — comes from the stage furthest from the language model.

> Students reflexively attribute product quality to model quality. **This is the
> best counterexample in the industry.** Spend fifteen minutes on it.

**Ask of any AI product:** list everything contributing to perceived quality that
is not the model. Retrieval, chunking, planning, pacing, formatting, latency,
the empty state, the failure message. That list is where a product team actually
competes, because the model is available to your competitor at the same price.

---

## B7 — Past chat: structured surfaces over a conversational core

Chat was the first interface because it was the **easiest to build**, not because
it was right. It is a poor interface for anything you want to do twice: nothing
is discoverable, nothing is repeatable, and every session starts from zero.

The industry's second act is rebuilding **structured, one-click surfaces** on top
of a conversational engine. The Studio panel is precisely this — the things worth
doing repeatedly became buttons.

**Ask:** what in your product is currently a prompt that should be a button? And
the harder inverse: what is a rigid form that should have been a conversation?

---

## B8 — Designing for wrongness

Assume the system is wrong 10–15% of the time. **It is not going to zero.** What
does the product do?

Two families of answer, and which one you need depends on whether your product
*tells* or *acts*:

| | Comprehension products | Action products |
| --- | --- | --- |
| Strategy | Make wrongness **inspectable** | Make wrongness **reversible** |
| Mechanism | Citations, source panel, quoting | Diffs, preview, checkpoints, undo, sandboxes |
| Example | NotebookLM | Cursor |

Both are the same underlying move:

> **The product's job is not to be right. It is to make being wrong cheap.**

That sentence is the closest thing this course has to a thesis, and it is where
the two case products meet. NotebookLM makes wrongness inspectable; Cursor makes
it reversible. Same problem, two families of solution, and every AI product your
students build will need one or both.

**Artifact:** for the team's chosen product — is it a telling product or an acting
product, and does its wrongness strategy match?

---
---

## Using the framework

Run all sixteen lenses on the spine case across Sessions 1–4. Each team runs the
same sixteen on a product of their own choosing and presents in Session 6.

**The three lenses that separate a good teardown from a shallow one** are
**P2** (the unservable job), **B5** (output modality), and **B6** (the craft layer
beneath the model). Weight them in grading. A team that only lists features has
skipped all three, and it will be obvious.

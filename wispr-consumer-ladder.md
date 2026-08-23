# The Consumer Ladder
## Eleven jobs, one person, built up from the ground floor

**The scope.** One consumer. Their own laptop, their own phone, their own money.
No IT department, no procurement, nobody to get approval from. Everything below
happens to the same person, and — apart from the last row — could happen to them
in a single Tuesday.

**The table.** Four columns throughout:

| Column | What's in it |
| --- | --- |
| **1 — The job** | Stated in JTBD form — **When** *[circumstance]*, **I want to** *[motivation]*, **so I can** *[outcome]* — then explained, and closed with outcome statements in the two standard forms. |
| **2 — The feature** | The feature, or feature set, that actually solves it. Stack layers as numbered in [`wispr-flow-deep-dive.md`](wispr-flow-deep-dive.md) §4. |
| **3 — Pre-gen-AI context** | The circumstance before generative AI, and what the user hired for it. Sometimes: *there was no circumstance.* |
| **4 — Post-gen-AI context** | The circumstance now, tagged with a verdict — **changed**, **unchanged**, or **created by adoption**. Where it's unchanged, the column says what moved instead. |

> **The verdict tag in column four is the discipline of the whole document.**
> Most write-ups of an AI product mark every row "changed," which is a table
> written backwards from its conclusion. Six of these eleven rows are word-for-word
> identical to 1995, and saying so is what makes the other five mean anything.

**Why a ladder and not a list.** These jobs are not siblings. Each only becomes
*available* once the layer beneath it is solved. You cannot want the right
register for a message until dictation produces something sendable at all. You
cannot want it to know your colleague's name until you've used it enough to have
said that name fifty times. **Read top to bottom: it is the order a real user
meets them in.**

**Where the ladder starts, and why.** Not with speech. With the thing that made
speech matter:

> **The primary interface to the most useful machine a consumer owns stopped
> being buttons and became prose.**
>
> That is the ground floor. Everything else on this page is a consequence. Speech
> is not interesting because talking is faster than typing — that was true in
> 1985 and changed nothing. Speech became interesting because **we suddenly had
> to produce an enormous new volume of language, aimed at a machine, and
> conversation is natively a spoken form.** Typing it is the anomaly.
>
> **The keyboard became the bottleneck in a job it had never been the bottleneck
> in before.**

---

## The ladder at a glance

| | The job, in one line | The feature that solves it | Verdict on the context |
| --- | --- | --- | --- |
| **L0** | Address a machine in language at all | Hold-to-talk + every text field on the OS | **CHANGED — the circumstance is new** |
| **L1** | Give it all the context, not the summary | Same capture, no length penalty | **CHANGED — the circumstance is new** |
| **L2** | Keep correcting until it's actually right | Cheap repeat turns + AI Commands | **CHANGED — the circumstance is new** |
| — | *— the hinge: below this line, a human reads it —* | | |
| **L3** | Answer humans at speaking speed | **The cleanup layer** | UNCHANGED — output crossed the sendable line |
| **L4** | Start a sentence I haven't finished thinking | Self-correction resolution | UNCHANGED — the precondition was removed |
| **L5** | One voice, correct in every destination | Context-awareness | UNCHANGED — but the feature has no pre-AI equivalent |
| **L6** | Be read as the person who speaks | Cleanup used as a **fluency** layer | UNCHANGED — correction became rendering |
| **L7** | Think in one language, ship in another | One-pass capture + cleanup + translation | UNCHANGED — two steps collapsed into one |
| **L8** | Have it know my names and my words | Passive personalisation | UNCHANGED — the entry toll was removed |
| **L9** | Work in the places I actually work | Canto + hold-to-talk + phone apps | **CREATED BY ADOPTION — second-order** |
| **L10** | Know it's worth paying for, before I pay | Free tier metered in words, not features | **CHANGED — what you're buying is different** |

---
---

# Block 1 — Machine-directed
### The ground floor. Three circumstances that did not exist in 2021 — and nobody reads the output.

| The job | The feature that solves it | Pre-gen-AI context | Post-gen-AI context |
| --- | --- | --- | --- |
| **L0 — Address a machine in language**<br/><br/>**When** the most useful machine I own responds only to language, and responds better the more language I give it, **I want to** put language into it without typing every word, **so I can** use the whole of what it can do rather than the part I'm willing to type out.<br/><br/>**Explained.** The most capable thing on the laptop now has no buttons. Every capability it has sits behind a text field, and what comes back is a direct function of how much prose the user was willing to produce. So the amount of language a consumer aims at a machine went from a handful of keywords a day to thousands of words — and the keyboard is the only thing in the path.<br/><br/>**The competitor is non-consumption:** the question never asked, the task never handed over, because framing it in writing was more work than doing it yourself.<br/><br/>*Minimize the time to get a complete instruction into a machine. Minimize the likelihood the machine's usefulness is capped by what I couldn't be bothered to type.* | **Hold-to-talk hotkey** (layer 1). Press, speak, release. No wake word, no ambient microphone.<br/><br/>**Works in every text field on the OS** (layer 7). Not an app you go to — it activates in the box you're already in.<br/><br/>**Note what is *not* needed here.** No cleanup, no register, no polish. Nobody reads your prompts. This is the one rung where raw speech would nearly do — which is exactly why it's the ground floor. | **There was no such circumstance.**<br/><br/>For forty years a consumer operated machines with buttons, menus and clicks. Language went to exactly one place — a search box — and that box **punished** extra words.<br/><br/>An entire generation was trained to strip language out: three keywords, no sentence, no context. Typing volume aimed at a machine was near zero, so the keyboard was never a bottleneck in this job, because **the job did not exist.** | **CONTEXT CHANGED — total discontinuity.**<br/><br/>A machine whose output improves the more you tell it. **The machine's appetite for language inverted** — from keyword-minimising to context-maximising — in about eighteen months, after forty years of the opposite.<br/><br/>**Why it matters more now:** this is the only rung that grows with AI adoption rather than with population. Every hour a consumer spends with a model is an hour of typing that did not exist in 2021. |
| **L1 — Hand over everything, not the summary**<br/><br/>**When** I'm briefing a model on something it needs real background for — the constraints, the edge cases, the thing I *don't* want — **I want to** hand over everything in my head without pruning it to what I'm willing to type, **so I can** get a usable answer on the first attempt instead of the fourth.<br/><br/>**Explained.** The brief in your head and the brief you type are different lengths, and the difference isn't a judgement — it's a typing decision. People drop the caveat, skip the example, omit the constraint, not because they concluded it was unnecessary but because it was another thirty seconds. **Typing cost silently degrades the quality of what comes back, and the user never sees the better answer they didn't get.**<br/><br/>*Minimize the likelihood I under-specify because specifying is expensive. Minimize the number of attempts before the answer is usable.* | The same capture as L0, **used at length**. The relevant property isn't accuracy — it's that **there is no penalty for saying more**, so the brief you give is the brief you meant. Speech runs ~3× typing, and the gap widens with length.<br/><br/>This is also where a heavy user first hits the free tier's word ceiling, which is what makes L10 a real job rather than a pricing footnote. | **There was no such circumstance.**<br/><br/>No consumer ever needed to produce three hundred words of instruction for a machine. There was nothing to instruct — software took parameters, not briefs.<br/><br/>The nearest analogue in anyone's life was **briefing a person**, and that was done by talking. | **CONTEXT CHANGED — the circumstance is new.**<br/><br/>Machines take briefs, and a bad brief is expensive, so briefs get long and careful.<br/><br/>**The observation for the slide:** the pre-AI analogue of this job was always *spoken*. **Typing a brief is the anomaly, not the norm** — which tells you which way the interface is heading. |
| **L2 — Keep going when it's 80% right**<br/><br/>**When** the answer is close but wrong in a specific way I could fix in one sentence, **I want to** say what's off the way I'd say it to a person, **so I can** keep going instead of accepting something worse because another round of typing isn't worth it.<br/><br/>**Explained.** Friction bites hardest on the **marginal turn**. Turn one is obviously worth the effort; turn four has *uncertain* payoff. When the next turn costs thirty seconds of typing, people stop early and keep a worse answer. When it costs five seconds of speech, they keep going. **The product doesn't just make each turn faster — it raises how many turns a person is willing to take, and therefore the quality of what they end up with.** That is very likely a real driver of the ~70% twelve-month retention, and it is invisible in any metric counting words per minute.<br/><br/>*Minimize the cost of the next turn. Minimize the likelihood I settle for a worse result because improving it isn't worth the effort.* | **Near-zero per-turn cost** — same hotkey, same field, no trip anywhere.<br/><br/>**AI Commands** (layer 6): speak the *operation* rather than restating the content. "Make this shorter." "Bullet that." A change you can already describe in a sentence costs a sentence, not a round trip through another window. | **There was no such circumstance.**<br/><br/>Software was right or it was broken. Nothing was ever **80% right and improvable by talking to it**. There was no such object as a partially-correct-but-negotiable artifact, so there was no repair activity to make cheap. | **CONTEXT CHANGED — the circumstance is new.**<br/><br/>Output is probabilistic and negotiable. **Correction became a first-class, repeated activity**, and conversation is its natural repair mechanism.<br/><br/>**Why it matters more now:** as more of a consumer's output starts life as a model's draft, the share of the day spent correcting rises. Of the three new rungs, this one grows fastest. |

---

> ## The hinge
>
> **Everything above has no social job. Nobody reads your prompts.** Everything
> below has a severe one — the output goes to a human being who will form a view
> of you from it.
>
> That single distinction splits the product in half, and explains the whole
> architecture: **the same spoken sentence has two different definitions of
> success depending on where it lands.** It is also the mechanism most analyses
> of this company miss —
>
> **Gen AI trained the speaking habit on the side of the interaction that carries
> no social risk, and the habit then walked across the line by itself.** People
> who had ignored free dictation for twenty years started talking to a machine
> all day, because there was nobody to embarrass themselves in front of. Once
> that reflex existed, turning to a human message and typing it felt like a step
> backwards. **The market for the rungs below was built by the rungs above.**

---
---

# Block 2 — Human-directed
### Six circumstances that are forty years old and completely unchanged. Only the solution moved.

| The job | The feature that solves it | Pre-gen-AI context | Post-gen-AI context |
| --- | --- | --- | --- |
| **L3 — Answer humans at speaking speed**<br/><br/>**When** I have forty unanswered messages and twenty minutes before I have to be somewhere, **I want to** clear them at something near the speed I'd say them, **so I can** end the day without the queue hanging over me.<br/><br/>**Explained.** The reflex is already formed — that's what the rungs below did. But human-directed text carries a requirement machine-directed text doesn't: **someone is judging you by it.** Speech written down verbatim doesn't read as thinking, it reads as carelessness. So you edit it — and the editing doesn't merely eat the time saved, it drags you back into the careful, line-by-line, *written* mode you were trying to escape, twice per message.<br/><br/>*Minimize the likelihood the output needs editing before it can be sent. Minimize the likelihood the recipient can tell it was dictated. Minimize the number of times I re-enter a message after speaking it.* | **The cleanup layer — layer 3.** Fillers removed, grammar repaired, stream-of-consciousness restructured into prose.<br/><br/>**This is the product.** Everyone assumes the product is the transcription; transcription was a commodity they were happy to rent for two years. The value is here, and it's the one layer nobody outside the company can see. | **Identical circumstance.** The inbox was always full. This row would read word-for-word the same in 1995.<br/><br/>**What it hired:** typing, mostly. Dictation could produce the words but never something **sendable** — no punctuation, fillers intact, "um" transcribed faithfully. Sending it raw made you look careless, so you edited it, and **the editing ate the time the speed had saved.** | **CONTEXT UNCHANGED — the output crossed the sendable threshold.**<br/><br/>The circumstance did not move an inch. What moved is that the text arrives finished, so the **social** job is served for the first time.<br/><br/>**Why it's newly relevant:** volume of messaging is up — but the real reason is that **the habit now arrives pre-formed from L0–L2.** The person meeting this job in 2026 isn't being asked to try dictation. They're being asked to stop making an exception for humans. |
| **L4 — Start a sentence I haven't finished thinking**<br/><br/>**When** I don't know how the sentence ends when I begin it — or I get halfway and change my mind — **I want to** have the machine keep the version I settled on rather than a record of me deciding, **so I can** think out loud instead of composing in my head first.<br/><br/>**Explained.** Two things sit here. The blank page: needing to write something careful with nothing coming. And the retraction: *"send it Tuesday — no, sorry, Wednesday."* Left in, that's a **semantic** error with a plausible reading — someone can act on it wrongly — so it forces a read-before-send on every message, and reading at reading speed is slower than saying it was.<br/><br/>*Minimize the likelihood the output contains something I retracted. Minimize the likelihood I must read it before sending. Minimize the effort to begin a sentence I haven't finished.* | **Self-correction resolution.** Say *"Tuesday — no, sorry, Wednesday"* and the output reads **"Wednesday."**<br/><br/>Plus the restructuring inside the cleanup layer, which takes a thought that arrived out of order and puts it in order.<br/><br/>**Looks like a demo trick; is load-bearing.** If you can't change your mind mid-sentence, you must know the sentence before you start — which is precisely what the person at a blank page doesn't have. | **Identical circumstance, and ancient** — the blank page predates the computer.<br/><br/>**Unserved.** Old dictation demanded you speak in finished, pre-formed sentences and transcribed your confusion faithfully if you didn't. **It required as input the very thing you came to it lacking**, which made it useless exactly when you were stuck. | **CONTEXT UNCHANGED — the precondition was removed.**<br/><br/>You can now start talking mid-thought; the product tolerates you not knowing where the sentence ends.<br/><br/>**Why it's newly relevant:** the volume of genuinely first-draft thinking has gone up. Briefing a model usually means working out what you want *while* saying it — so a tool that tolerates an unfinished sentence is needed several times a day rather than several times a month. |
| **L5 — One voice, correct in every destination**<br/><br/>**When** the same thought has to reach a friend on WhatsApp, my landlord by email and a model in a chat window inside ten minutes, **I want to** say it once in one voice and have it arrive in the right register, **so I can** stop rewriting myself for each channel.<br/><br/>**Explained.** "Hey, can you look at this?" is correct in one window and wrong in another. Getting that right isn't typing work — it's **modelling the reader**, which is the actual labour of everyday writing, paid once per message, dozens of times a day. And the user has *already made* that judgement: they made it when they chose which window to click into.<br/><br/>*Minimize the effort to adapt the same content to a different destination. Minimize the likelihood the register is wrong for where it lands. Minimize the number of instructions I must give before I can start speaking.* | **Context-awareness — layer 4.** Reads the active application and adapts register and formatting.<br/><br/>**The principle underneath it: it never asks.** It reads a decision you already made somewhere else. If you had to say "make this formal," the pre-composition tax would be straight back. | **Identical circumstance** — people have always written to different audiences in one sitting.<br/><br/>**Unserved, and unservable.** Register isn't a setting anyone could have exposed; it's a reading of a situation. Old dictation produced one flat output regardless of where it was going, so adapting it was manual, every time. | **CONTEXT UNCHANGED — but the feature has no pre-AI equivalent at all.**<br/><br/>The product infers the **destination**, and destination determines register. This is a product idea with no pre-LLM ancestor, which is why competitors matching the model still lose this.<br/><br/>**Why it matters more now:** the number of distinct channels one consumer writes in keeps climbing, and the register tax climbs with it — paid per message, silently, by everyone. |
| **L6 — Be read as the person who speaks**<br/><br/>**When** I'm writing to people who will judge me by the writing, in a language I speak more fluently than I write, **I want to** produce text as fluent as I sound in a room, **so I can** be read as the person who spoke in the meeting.<br/><br/>**Explained.** Enormous numbers of people speak a language far more confidently than they write it. The gap isn't speed, it's **credibility**, and it bites hardest in exactly the writing that matters most. The cost people count is the visible mistakes. **The real cost is suppression** — sentences shortened, arguments hedged, opinions not volunteered, because writing them is expensive. That damage consists entirely of text that was never produced, so it appears in no metric anywhere.<br/><br/>*Minimize the likelihood I'm read as less capable than I am. Minimize the likelihood I shorten or withhold an argument because writing it is costly.* | **The same cleanup layer, doing a different job.** It is not a corrector. It doesn't fix your English — **it renders your meaning in fluent English.**<br/><br/>Same feature as L3, entirely different value. One layer serving a speed job and a credibility job at once is why *"what does this feature do"* is the wrong question to ask of it. | **Identical circumstance, and enormous.**<br/><br/>**Essentially unserved.** Every tool acted *after* the fact — grammar checkers flag errors in a sentence you've already had to produce. But the anxiety is **before**: it's about the sentence you haven't written yet. Flagging errors confirms the fear rather than removing it. | **CONTEXT UNCHANGED — correction became rendering.**<br/><br/>The fluent version is the first version you see, so the anxiety never gets its moment.<br/><br/>**Why it's newly relevant:** a rising share of professional judgement passes through text — remote, async, written-first. This is the row that lands hardest in an Indian cohort, and it is almost invisible in a US-centric reading of the product. |
| **L7 — Think in one language, ship in another**<br/><br/>**When** the thought arrives in my first language and the output has to be in English, **I want to** say it as it comes and get English out in one pass, **so I can** work at the speed I think rather than the speed I translate.<br/><br/>**Explained.** Translation doesn't happen as a step; it happens *at composition time*, in working memory, concurrently with the thinking. It's a second live task competing for the scarcest resource — and that resource is already stretched, because the thought is at risk of slipping while you hold it.<br/><br/>*Minimize the effort to move a thought from the language it arrived in to the language it must ship in. Minimize the number of steps between the thought and the delivered text.* | Capture, cleanup and translation collapsed into **a single pass** by one model.<br/><br/>The feature isn't translation — translation was free and everywhere. The feature is that translation **stopped being a separate step with its own input requirement**. | **Identical circumstance.**<br/><br/>**Unserved, for a precise reason:** translation tools required you to **write the source first.** You had to complete the very step you were trying to skip. Two tools, three steps, and the first step was the one you couldn't do. | **CONTEXT UNCHANGED — two steps collapsed into one.**<br/><br/>One utterance in, finished target-language text out.<br/><br/>**Why it matters more now:** when translation is a separate step, people quietly trade off between speed and their own language — and mostly choose to think in English, badly. Collapsing the step lets someone think in the language they think fastest in and still ship in the one the situation demands. |
| **L8 — Have it know my names and my words**<br/><br/>**When** the words that carry the most meaning in my life are names, places and terms no general system has ever heard, **I want to** have them come out right without ever sitting down to teach them, **so I can** find out whether this works for me before I've invested anything in it.<br/><br/>**Explained.** The words that get misrecognised are disproportionately the load-bearing ones — people, places, the thing the message is actually about. The obvious fix is to train it up front. But up-front training is **a payment made towards a tool you haven't yet decided to trust**: it demands commitment before evidence, and **a consumer with a working keyboard will never sit through voice enrollment.**<br/><br/>*Minimize the setup effort before first useful output. Minimize the likelihood that the names specific to my life come out wrong. Minimize the effort to teach the tool anything, ever.* | **Passive personalisation — layer 5.** Learns your names, jargon and style as you go. No enrollment, no dictionary, no training session.<br/><br/>The effect is on the **payoff curve**, not the accuracy number: usable at minute one, better at week four. Improvement becomes a reward for staying rather than a toll for entering. | **Identical circumstance** — your vocabulary was always yours.<br/><br/>**Served, but by making you pay first.** Voice enrollment, a custom dictionary, a training session before first useful output.<br/><br/>Only one group accepted that: people for whom typing was painful or unavailable, who had no alternative. **That is the entire reason dictation stayed a niche for forty years.** | **CONTEXT UNCHANGED — the entry toll was removed.**<br/><br/>**Why this is the rung that made it a consumer product:** the historic users absorbed the setup cost because they had no choice. Everyone else wanted the same outcome and would never pay admission for it.<br/><br/>**The niche was always the visible tip of a general market** — the only segment whose forces already resolved. Removing the toll is what let the rest of that market appear. |

---
---

# Block 3 — Conditions, and paying
### One circumstance the product's own success created, and one that changes what a consumer purchase even is.

| The job | The feature that solves it | Pre-gen-AI context | Post-gen-AI context |
| --- | --- | --- | --- |
| **L9 — Work in the places I actually work**<br/><br/>**When** the places I really work are a café, a shared flat and a phone on a train, **I want to** get the same output I'd get alone at a quiet desk, **so I can** have one way of working instead of one way plus a list of conditions.<br/><br/>**Explained.** A tool that works in quiet rooms works during a minority of a person's waking hours — and they can't tell in advance which rooms will work, so every use starts with an unstated test. A tool you must test becomes the *fallback* while typing stays the default, and habits form on defaults. The failure is also asymmetric: a garbled take costs more than the seconds it saved, so under uncertainty typing is the rational choice. **Uncertainty alone is enough to prevent the hire, without a single actual failure occurring.**<br/><br/>*Minimize the likelihood output quality depends on where I'm sitting. Minimize the effort to predict whether it will work before I use it. Minimize the likelihood I fall back to a worse method away from my desk.* | **Canto**, their own speech model tuned for noise — reported to cut word error in noisy environments from over 30% to 5–10%.<br/><br/>**Hold-to-talk**, again: in a shared flat an ambient microphone is unacceptable at any accuracy.<br/><br/>**iOS and Android**, carrying the same learned vocabulary. Note that free phone dictation shipped on every handset for a decade against a *higher* push and still lost — **coverage without the cleanup layer is worth nothing.** | **You could not have this problem.**<br/><br/>Nobody was dictating, so no room was ever the constraint. The question "can I use this in a café?" has no meaning for a person who types.<br/><br/>The nearest pre-AI version of the anxiety was hypothetical and it killed adoption anyway: *"I'd be talking at my laptop in an open-plan office"* — a reason not to start, not a problem in use. | **CONTEXT CREATED BY ADOPTION — second-order.**<br/><br/>You dictate all day, so **the room becomes the binding constraint on where you can work.** The product's own success manufactured the circumstance.<br/><br/>**The sharpest strategic row on the page.** Canto reads as a quality upgrade and gets discussed as margin. It's neither: the constraint on the total market was never accuracy in a quiet room — **it was that almost no work happens in a quiet room.** They didn't improve the product; they enlarged the set of places it exists in. |
| **L10 — Know it's worth paying for, before I pay**<br/><br/>**When** I'm deciding whether this is worth a monthly subscription, in a category that has disappointed me for twenty years, **I want to** use the real product on my own words until I know, **so I can** buy back something I already have rather than buy a promise.<br/><br/>**Explained.** The claim under test — *it produces text I can send* — isn't checkable by reading about it. It's only checkable on **their** speech, **their** names, **their** messages. A feature-limited trial can't do it: the thing being tested is quality on their own material, so a crippled version tests a different product and they'd only learn whether they like a worse thing. And the anxiety here is not price — it's **prior category experience**, which no marketing copy discharges.<br/><br/>*Minimize the likelihood I pay for something that turns out not to work on my material. Minimize the likelihood the version I evaluate is not the version I'd be buying.* | **The free tier metered in words, not features** — ~2,000 words a week on desktop, ~1,000 on the phone. **The product is identical; you simply run out.** Plus a 14-day full trial, no card.<br/><br/>**The mechanism:** running out converts a prediction into a memory. By the time they hit the wall they know exactly what they lose.<br/><br/>**The rule:** for a habit product, **meter the volume, never the capability.** A feature-gated free tier would never have produced ~70% twelve-month retention — what's being retained is a reflex, and a reflex can't form around something you're only allowed to half-use. | **You were buying a capability.**<br/><br/>Consumer software was a set of things it could do, and you could evaluate that from a feature list before paying. Does it do X? Yes or no. A trial demonstrated features.<br/><br/>Dictation was sold the same way — on accuracy percentages and supported applications — and it is precisely that framing that made forty years of buyers wrong about what they were getting. | **CONTEXT CHANGED — you are now buying a habit.**<br/><br/>What this consumer purchases is a change in how getting words out *feels*, fifty times a day. **A habit cannot be evaluated from a description. It can only be evaluated by forming one.**<br/><br/>So the free tier's job is not to demonstrate features. It is to let the habit exist, then ask for money at the exact moment the habit is real. **Gen AI changed what a consumer software purchase *is*, and the pricing page is where that shows up.** |

---
---

# What the ladder shows

**1. The bottom three rungs built the market for the top eight.** This is what the
layered reading produces and a flat feature list cannot. L0–L2 are
machine-directed and carry **no social risk** — nobody reads your prompts. That
is where a whole population learned to speak at a laptop. Only once the reflex
existed did the forty-year-old human-directed jobs become winnable. **Generative
AI didn't only remove the anxiety on the old job; it created a new, low-stakes
job on which the habit could be trained first.**

**2. Only three circumstances are new — and they're the three that compound.**
L0, L1 and L2 grow with AI adoption. L3–L8 grow with population, which moves a
few percent a year. **A durable AI-native product is one where the
new-circumstance jobs are also the fast-growing ones.**

**3. Six of eleven circumstances are word-for-word identical to 1995.** Every one
of those rows is an unserved outcome that waited forty years, which is why they
converted so fast once the solution crossed the line — **there was no demand to
create, only a constraint to remove.**

**4. Read the pre-gen-AI column down Block 2 and one pattern repeats.** The old
solution didn't merely fail — **it demanded from the user the very thing the user
was short of.** A finished sentence when they were stuck (L4). Editing time when
they had none (L3). Written confidence when writing was the weak point (L6). A
written source from someone who hadn't written anything yet (L7). Commitment
before any evidence (L8).

> **The diagnostic to hand the room: when a solution has existed for decades and
> nobody hires it, check whether it requires as input the thing the user came to
> you lacking.**

**5. Two rungs are the product's own footprints.** L9 and L10 could not have
existed before the product worked. Nobody needed noise handling until they were
dictating everywhere; nobody needed a habit-forming meter until the thing being
sold was a habit.

**6. Speed appears in two rows and is never the terminal reason.** The other nine
are about being read correctly, thinking out loud, being allowed to start, not
having to decide. **Speed is the pitch on the website. It is almost never why
anybody stays.**

---

# Running it in class

Put the glance table up. Then take **three rungs**, one per block, so the shape
of the ladder is visible rather than asserted:

| Rung | Why this one |
| --- | --- |
| **L0** | The ground floor, and the whole argument in one row. Ask the room how many sentences they typed *at a machine* last week versus in 2021. The answer is the market. |
| **L3** | The hinge in action. Same person, same voice, one rung further down — and now a human is reading it, so the product has to do something entirely different with the identical utterance. |
| **L10** | The pricing rung. The one they can apply on Monday: *is my free tier testing my capability, or letting a habit form?* |

**Then the exercise.** Give teams a consumer product and twenty minutes to build
the same four columns. Two tests of whether they've understood:

- **Is their bottom rung actually the bottom?** Most teams start three rungs too
  high, at a job that only exists once something below it is already solved.
- **Does any row honestly say UNCHANGED?** A ladder where every row claims gen AI
  changed the context was written backwards from the conclusion. **The unchanged
  rows are usually where the money already was.**

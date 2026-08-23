# The Consumer Ladder
## Eleven jobs, one person, built up from the ground floor

**The scope.** One consumer. Their own laptop, their own phone, their own money.
No IT department, no procurement, nobody to get approval from. Everything below
happens to the same person, and — apart from the last row — could happen to them
in a single Tuesday.

**Why a ladder and not a list.** These jobs are not siblings. Each one only
becomes *available* once the layer beneath it is solved. You cannot want the
right register for a Slack message until dictation produces something sendable
at all. You cannot want it to know your colleague's name until you're using it
often enough to have said the name fifty times. **Read top to bottom: it is the
order a real user meets them in.**

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

| | The job, in one line | The feature that solves it | Did the context change? |
| --- | --- | --- | --- |
| **L0** | Address a machine in language at all | Hold-to-talk + every text field on the OS | **Yes — total. New circumstance.** |
| **L1** | Give it all the context, not the summary | Same capture, with no length penalty | **Yes — new circumstance** |
| **L2** | Keep correcting until it's actually right | Low-cost repeat turns + AI Commands | **Yes — new circumstance** |
| — | *— the hinge: below this line, someone is reading it —* | | |
| **L3** | Answer humans at speaking speed | **The cleanup layer** | No — solution crossed a threshold |
| **L4** | Start a sentence I haven't finished thinking | Self-correction resolution | No — precondition removed |
| **L5** | One voice, correct in every destination | Context-awareness | No — but the feature has no pre-AI equivalent |
| **L6** | Be read as the person who speaks | Cleanup used as a **fluency** layer | No — correction became rendering |
| **L7** | Think in one language, ship in another | One-pass capture + cleanup + translation | No — two steps collapsed into one |
| **L8** | Have it know my names and my words | Passive personalisation | No — the entry toll was removed |
| **L9** | Work in the places I actually work | Canto + hold-to-talk + phone apps | **Yes — second-order, created by adoption** |
| **L10** | Know it's worth paying for before I pay | **Free tier metered in words, not features** | **Yes — what you're buying changed** |

**Three of eleven circumstances are genuinely new, and they're L0–L2 — the ones
pointed at a machine.** Those scale with AI adoption. Six are word-for-word
identical to 1995 and only the solution moved. Two were manufactured by the
product's own success. Keeping those apart is the whole analysis; blurring them
is why most write-ups of this company say nothing.

---
---

# Block 1 — Machine-directed
### The ground floor. These circumstances did not exist in 2021, and nobody is reading the output.

| The job | The context, and the outcome they want | The feature that solves it | Before and after gen AI |
| --- | --- | --- | --- |
| **L0 — Address a machine in language**<br/><br/>**When** the most useful machine I own responds only to language, and responds better the more language I give it, **I want to** put language into it without typing every word, **so I can** use the whole of what it can do rather than the part I'm willing to type out. | **Context.** For forty years a consumer operated machines with buttons, menus and clicks. Language went to exactly one place — a search box — and that box *punished* extra words. We were trained, for a generation, to strip language out: three keywords, no sentence, no context. Now the single most capable thing on the laptop has no buttons at all. Every capability it has sits behind a text field, and the quality of what comes back is a direct function of how much prose you were willing to produce.<br/><br/>**Outcome.** *Minimize the time to get a complete instruction into a machine. Minimize the likelihood the machine's usefulness is capped by what I couldn't be bothered to type.*<br/><br/>**The competitor here is non-consumption** — the question they didn't ask, the task they didn't hand over, because framing it in writing was more work than doing it themselves. | **Hold-to-talk hotkey** (stack layer 1) — press, speak, release. No wake word, no ambient microphone.<br/><br/>**Plus: it works in every text field on the OS** (layer 7). Not an app you go to. It activates in the box you're already in.<br/><br/>**Note what is *not* needed at this layer.** No cleanup, no register, no polish. Nobody reads your prompts. This is the one place raw speech would almost do — which is exactly why it's the ground floor. | **Total discontinuity. This circumstance did not exist.**<br/><br/>**Before:** no machine in a consumer's life accepted a paragraph. The one that accepted words penalised you for using more of them.<br/><br/>**After:** a machine whose output improves the more you tell it. **The machine's appetite for language inverted** — from keyword-minimising to context-maximising, in about eighteen months, after forty years of the opposite.<br/><br/>**Why it matters more now:** this is the only row that grows with AI adoption. Every other job on this page grows with population. |
| **L1 — Hand over everything, not the summary**<br/><br/>**When** I'm briefing a model on something it needs real background for — the constraints, the edge cases, the thing I *don't* want — **I want to** hand over everything in my head without pruning it to what I'm willing to type, **so I can** get a usable answer on the first attempt instead of the fourth. | **Context.** The brief in your head and the brief you type are different lengths, and the difference is not a judgement — it's a typing decision. People drop the caveat, skip the example, omit the constraint, not because they concluded it was unnecessary but because it was another thirty seconds. **Typing cost silently degrades the quality of what you get back, and you never see the better answer you didn't get.** Speaking is roughly three times faster than typing, and the gap widens with length.<br/><br/>**Outcome.** *Minimize the likelihood I under-specify because specifying is expensive. Minimize the number of attempts before the answer is usable.* | Same capture as L0, **used at length**. The relevant property is not accuracy — it's that **there is no penalty for saying more**, so the brief you give is the brief you meant.<br/><br/>This is where a heavy user meets the free tier's word ceiling first, which is what makes L10 a real job rather than a pricing footnote. | **New circumstance.**<br/><br/>**Before:** nobody in consumer computing ever needed to produce three hundred words of instruction for a machine. There was nothing to instruct.<br/><br/>**After:** the machine takes a brief. A bad brief is expensive.<br/><br/>**The observation worth the slide:** the pre-AI analogue of this job was always *spoken* — you briefed a person by talking to them. **Typing a brief is the anomaly, not the norm.** That tells you which way this is heading. |
| **L2 — Keep going when it's 80% right**<br/><br/>**When** the answer is close but wrong in a specific way I could fix in one sentence, **I want to** say what's off the way I'd say it to a person, **so I can** keep going instead of accepting something worse because another round of typing isn't worth it. | **Context.** Friction bites hardest on the **marginal turn**. Turn one is obviously worth the effort. Turn four has *uncertain* payoff — it might fix it, it might not. When the next turn costs thirty seconds of typing, people stop early and keep a worse answer. When it costs five seconds of speech, they keep going.<br/><br/>**Outcome.** *Minimize the cost of the next turn. Minimize the likelihood I settle for a worse result because improving it isn't worth the effort.*<br/><br/>**This is probably a real driver of the ~70% twelve-month retention, and it is invisible in any metric counting words per minute.** The product isn't making each turn faster; it's raising how many turns a person is willing to take — and therefore the quality of what they end up with. | **Near-zero per-turn cost** — the same hotkey, in the same field, with no trip anywhere.<br/><br/>**Plus AI Commands:** speak the *operation* rather than restating the content. "Make this shorter." "Bullet that." A change you can already describe in a sentence costs a sentence, not a round trip through another window. | **New circumstance.**<br/><br/>**Before:** software was right or it was broken. Nothing was ever 80% right *and* improvable by talking to it. There was no such thing as a partially-correct-but-negotiable artifact.<br/><br/>**After:** output is probabilistic. **Correction became a first-class, repeated activity** — and conversation is its natural repair mechanism.<br/><br/>**Why it matters more now:** as more of a consumer's output starts as a model's draft, the share of their day spent in correction rises. This row grows fastest of the three. |

---

> ## The hinge
>
> **Everything above has no social job. Nobody reads your prompts.** Everything
> below has a severe one — the output goes to a human being who will form a view
> of you from it.
>
> That single distinction splits the product in half, and it explains the whole
> architecture: **the same spoken sentence has two different definitions of
> success depending on where it lands.** It is also the mechanism most analyses
> of this company miss entirely —
>
> **Gen AI trained the speaking habit on the side of the interaction that carries
> no social risk, and the habit then walked across the line by itself.** People
> who had ignored free dictation for twenty years started talking to a machine
> all day because there was nobody to embarrass themselves in front of. Once that
> reflex existed, turning to a human message and typing it felt like a step
> backwards. **The market for the rows below was built by the rows above.**

---
---

# Block 2 — Human-directed
### The circumstances here are forty years old and completely unchanged. Only the solution moved.

| The job | The context, and the outcome they want | The feature that solves it | Before and after gen AI |
| --- | --- | --- | --- |
| **L3 — Answer humans at speaking speed**<br/><br/>**When** I have forty unanswered messages and twenty minutes before I have to be somewhere, **I want to** clear them at something near the speed I'd say them, **so I can** end the day without the queue hanging over me. | **Context.** The reflex is already formed — that's what the layers below did. But human-directed text carries a requirement machine-directed text doesn't: **someone is judging you by it.** Speech written down verbatim doesn't read as thinking, it reads as carelessness — no punctuation, fillers intact, sentences that never close. So you edit it. And the editing doesn't just eat the time saved; it drags you back into the careful, line-by-line, *written* mode you were trying to escape, twice per message.<br/><br/>**Outcome.** *Minimize the likelihood the output needs editing before it can be sent. Minimize the likelihood the recipient can tell it was dictated. Minimize the number of times I have to re-enter a message after speaking it.* | **The cleanup layer — stack layer 3.** Fillers removed, grammar repaired, stream-of-consciousness restructured into prose.<br/><br/>**This is the product.** Everyone assumes the product is the transcription. Transcription was a commodity they were happy to rent for two years. The value is here, and it's the one layer nobody outside the company can see. | **Circumstance completely unchanged.** The inbox was always full. This row would read identically in 1995.<br/><br/>**What changed:** the output crossed the **sendable** threshold. Dictation always produced words; it never produced text you could send.<br/><br/>**Why it's newly relevant:** two reasons, and the second is the interesting one. Volume of messaging has risen — but more importantly, **the habit now arrives pre-formed from L0–L2.** The person meeting this job in 2026 is not being asked to try dictation. They're being asked to stop making an exception for humans. |
| **L4 — Start a sentence I haven't finished thinking**<br/><br/>**When** I don't know how the sentence ends when I begin it — or I get halfway and change my mind — **I want to** have the machine keep the version I settled on rather than a record of me deciding, **so I can** think out loud instead of composing in my head first. | **Context.** Two things sit in this row. One: the blank page — needing to write something careful with nothing coming, where the old tool was useless *precisely* when you were stuck, because it demanded a finished sentence as input. Two: the retraction — "send it Tuesday, no, sorry, Wednesday." Left in, that's a **semantic** error with a plausible reading; someone can act on it wrongly. So it forces a read-before-send on every message, and reading at reading speed is slower than saying it was.<br/><br/>**Outcome.** *Minimize the likelihood the output contains something I retracted. Minimize the likelihood I must read it before sending. Minimize the effort to begin a sentence I haven't finished.* | **Self-correction resolution** — say *"Tuesday — no, sorry, Wednesday"* and the output reads **"Wednesday."**<br/><br/>Plus the restructuring inside the cleanup layer, which takes a thought that arrived out of order and puts it in order.<br/><br/>**This looks like a demo trick and is actually load-bearing.** If you can't change your mind mid-sentence, you must know the sentence before you start — which is exactly what the person staring at a blank page does not have. | **Circumstance unchanged, and ancient.** The blank page predates the computer.<br/><br/>**What changed:** the precondition was removed. Old dictation **required as input the very thing you came to it lacking** — a formed sentence. That is the single most transferable diagnostic in this pack.<br/><br/>**Why it's newly relevant:** the volume of genuinely first-draft thinking has gone up. When you brief a model, you're frequently working out what you want *while* saying it — so a tool that tolerates an unfinished sentence is now needed several times a day rather than several times a month. |
| **L5 — One voice, correct in every destination**<br/><br/>**When** the same thought has to reach a friend on WhatsApp, my landlord by email and a model in a chat window inside ten minutes, **I want to** say it once in one voice and have it arrive in the right register, **so I can** stop rewriting myself for each channel. | **Context.** "Hey, can you look at this?" is correct in one window and wrong in another. Getting that right is not typing work — it's **modelling the reader**, and that is the actual labour of everyday writing. It's one decision per message, dozens a day. Note that the user has *already made* that judgement: they made it when they chose which window to click into. The destination encodes it.<br/><br/>**Outcome.** *Minimize the effort to adapt the same content to a different destination. Minimize the likelihood the register is wrong for where it lands. Minimize the number of instructions I must give before I can start speaking.* | **Context-awareness — stack layer 4.** It reads the active application and adapts register and formatting.<br/><br/>**The design principle underneath it:** it never asks. It reads a decision you already made somewhere else. If you had to say "make this formal," the pre-composition tax would be right back. | **Circumstance unchanged — but the feature has no pre-AI equivalent whatsoever.**<br/><br/>**Before:** unserved, and unservable. Register isn't a setting you could have exposed; it's a reading of a situation. No pre-LLM system could perform it.<br/><br/>**After:** the product infers the destination, and destination determines register.<br/><br/>**Why it matters more now:** the number of distinct channels one consumer writes in keeps climbing. The register tax climbs with it — and it's paid per message, silently, by everyone. |
| **L6 — Be read as the person who speaks**<br/><br/>**When** I'm writing to people who will judge me by the writing, in a language I speak more fluently than I write, **I want to** produce text as fluent as I sound in a room, **so I can** be read as the person who spoke in the meeting. | **Context.** Enormous numbers of people speak a language far more confidently than they write it. The gap isn't speed, it's **credibility** — and it's felt most in exactly the writing that matters most. A grammar checker doesn't help: it acts *after* the sentence exists, and the anxiety is *before*. Flagging errors confirms the fear rather than removing it.<br/><br/>The cost people count is the visible mistakes. **The real cost is suppression** — sentences made shorter, arguments hedged, opinions not volunteered, because writing them is expensive. That damage consists entirely of text that was never produced, so it appears in no metric anywhere.<br/><br/>**Outcome.** *Minimize the likelihood I'm read as less capable than I am. Minimize the likelihood I shorten or withhold an argument because writing it is costly.* | **The same cleanup layer, doing a different job.** It is not a corrector. It doesn't fix your English — **it renders your meaning in fluent English.**<br/><br/>Same feature as L3; entirely different value. Worth pointing out in class: one layer serving a speed job and a credibility job at once is why "what does this feature do" is the wrong question. | **Circumstance unchanged, and enormous.**<br/><br/>**Before:** essentially unserved. Every tool acted after the fact, on a sentence you'd already had to produce.<br/><br/>**After:** **correction became rendering.** The fluent version is the first version you see, so the anxiety never gets its moment.<br/><br/>**Why it matters more now:** a rising share of professional judgement passes through text — remote, async, written-first. And this is the row that lands hardest in an Indian cohort, while being almost invisible in a US-centric reading of the product. |
| **L7 — Think in one language, ship in another**<br/><br/>**When** the thought arrives in my first language and the output has to be in English, **I want to** say it as it comes and get English out in one pass, **so I can** work at the speed I think rather than the speed I translate. | **Context.** Translation doesn't happen as a step; it happens *at composition time*, in working memory, running concurrently with the thinking. It's a second live task competing for the same faculty — and that faculty is already the scarce one, because the thought is at risk of slipping while you hold it.<br/><br/>Translation tools never helped, for a precise reason: **they required you to write the source first.** You had to complete the very step you were trying to skip.<br/><br/>**Outcome.** *Minimize the effort to move a thought from the language it arrived in to the language it must ship in. Minimize the number of steps between the thought and the delivered text.* | Capture, cleanup and translation collapsed into **a single pass** by one model.<br/><br/>The feature isn't translation — translation was free and everywhere. The feature is that translation stopped being a separate step with its own input requirement. | **Circumstance unchanged.**<br/><br/>**Before:** two tools, three steps, and the first step was the one you couldn't do.<br/><br/>**After:** one utterance in, finished target-language text out.<br/><br/>**Why it matters more now:** when translation is a separate step, people quietly choose between speed and their own language — and mostly choose to think in English, badly. Collapsing the step lets someone think in the language they think fastest in and still ship in the one the situation demands. |

---
---

# Block 3 — Conditions, and paying
### One circumstance the product's own success created, and one that reframes what a consumer purchase even is.

| The job | The context, and the outcome they want | The feature that solves it | Before and after gen AI |
| --- | --- | --- | --- |
| **L8 — Have it know my names and my words**<br/><br/>**When** the words that carry the most meaning in my life are names, places and terms no general system has ever heard, **I want to** have them come out right without ever sitting down to teach them, **so I can** find out whether this works for me before I've invested anything in it. | **Context.** The words that get misrecognised are disproportionately the load-bearing ones — people, places, the thing the message is actually about. The obvious fix is to train it up front. But up-front training is **a payment made towards a tool you haven't yet decided to trust**: it demands commitment before evidence.<br/><br/>That ordering is why the category stayed a niche for forty years. The only people who accept it are people with no alternative. **A consumer with a working keyboard will never sit through voice enrollment.**<br/><br/>**Outcome.** *Minimize the setup effort before first useful output. Minimize the likelihood that the names specific to my life come out wrong. Minimize the effort to teach the tool anything, ever.* | **Passive personalisation — stack layer 5.** It learns your names, jargon and style as you go. No enrollment, no dictionary, no training session.<br/><br/>The effect is on the payoff curve, not the accuracy number: **usable at minute one, better at week four.** Improvement becomes a reward for staying rather than a toll for entering. | **Circumstance unchanged** — your vocabulary was always yours.<br/><br/>**Before:** served, but by making you pay first. Voice enrollment and a custom dictionary.<br/><br/>**After:** the toll is gone.<br/><br/>**Why this row is the one that made it a consumer product:** dictation's historic users absorbed the setup cost because typing hurt and they had no choice. Everyone else wanted the same outcome and would never pay admission for it. **Removing the entry cost is what turned a niche into a general market — the niche was always the visible tip of one.** |
| **L9 — Work in the places I actually work**<br/><br/>**When** the places I really work are a café, a shared flat and a phone on a train, **I want to** get the same output I'd get alone at a quiet desk, **so I can** have one way of working instead of one way plus a list of conditions. | **Context.** A tool that works in quiet rooms works during a minority of a person's waking hours. Worse, they can't tell in advance which rooms will work — so every use starts with an unstated test, and a tool you must test becomes the *fallback* while typing stays the default. Habits form on defaults.<br/><br/>And the failure is asymmetric: a garbled take in a noisy room costs more than the seconds it saved. Under uncertainty, typing is the rational choice. **Uncertainty alone is enough to prevent the hire, without a single actual failure occurring.**<br/><br/>**Outcome.** *Minimize the likelihood output quality depends on where I'm sitting. Minimize the effort to predict whether it will work before I use it. Minimize the likelihood I fall back to a worse method away from my desk.* | **Canto**, their own speech model tuned for noise — reported to cut word error in noisy environments from over 30% to 5–10%.<br/><br/>**Hold-to-talk**, again — in a shared flat, an ambient microphone is not acceptable at any accuracy.<br/><br/>**iOS and Android**, carrying the same learned vocabulary. Note that free phone dictation shipped on every handset for a decade against a *higher* push and still lost — because the output wasn't sendable. **Coverage without the cleanup layer is worth nothing.** | **Second-order — created entirely by adoption.**<br/><br/>**Before:** you could not have this problem. Nobody was dictating, so no room was ever the constraint.<br/><br/>**After:** you dictate all day, so **the room becomes the binding constraint on where you can work.**<br/><br/>**Why this is the sharpest strategic row on the page:** Canto reads as a quality upgrade and gets discussed as margin. It's neither. The constraint on the total market was never accuracy in a quiet room — **it was that almost no work happens in a quiet room.** They didn't improve the product; they enlarged the set of places it exists in. |
| **L10 — Know it's worth paying for, before I pay**<br/><br/>**When** I'm deciding whether this is worth a monthly subscription, in a category that has disappointed me for twenty years, **I want to** use the real product on my own words until I know, **so I can** buy back something I already have rather than buy a promise. | **Context.** The claim under test — *it produces text I can send* — is not checkable by reading about it. It's only checkable on **their** speech, **their** names, **their** messages. A feature-limited trial can't do it: the thing being tested is quality on their own material, so a crippled version tests a different product and they'd only learn whether they like a worse thing.<br/><br/>And the anxiety here is not price. It's **prior category experience** — forty years of dictation disappointing people. No marketing copy discharges that; only their own evidence does.<br/><br/>**Outcome.** *Minimize the likelihood I pay for something that turns out not to work on my material. Minimize the likelihood the version I evaluate is not the version I'd be buying.* | **The free tier metered in words, not features** — roughly 2,000 words a week on desktop, 1,000 on the phone. **The product is identical; you simply run out.** Plus a 14-day full trial with no card.<br/><br/>**The mechanism:** running out converts a prediction into a memory. By the time they hit the wall they know exactly what they lose. They aren't buying a claim — they're buying back something they already had.<br/><br/>**The rule:** for a habit product, **meter the volume, never the capability.** A feature-gated free tier would never have produced ~70% twelve-month retention, because what's being retained is a reflex, and a reflex can't form around something you're only allowed to half-use. | **The circumstance changed, in one specific and under-noticed way.**<br/><br/>**Before:** a consumer buying software was buying a **capability**, and you can evaluate a capability from a feature list. Does it do X? Yes or no.<br/><br/>**After:** this consumer is buying a **habit** — a change in how getting words out feels, fifty times a day. **A habit cannot be evaluated from a description. It can only be evaluated by forming one.**<br/><br/>That's why the meter is on volume: the free tier's job is not to demonstrate features. It is to let the habit exist, and then ask for money at the exact moment the habit is real. **Gen AI changed what a consumer software purchase *is*, and the pricing page is where that shows up.** |

---
---

# What the ladder shows

**1. The bottom three rungs built the market for the top eight.** This is the
finding the layered reading produces and a flat feature list cannot. L0–L2 are
machine-directed and carry **no social risk** — nobody reads your prompts. That
is where a whole population learned to speak at a laptop. Only once that reflex
existed did the forty-year-old human-directed jobs become winnable. **Generative
AI didn't just remove the anxiety on the old job; it created a new, low-stakes
job on which the habit could be trained first.**

**2. Only three circumstances are new — and they're the three that compound.**
L0, L1 and L2 grow with AI adoption. L3–L8 grow with population, which moves a
few percent a year. **A durable AI-native product is one where the
new-circumstance jobs are also the fast-growing ones.** That is the honest
version of "this is an AI company," and it survives contact with the numbers.

**3. Six of eleven circumstances are word-for-word identical to 1995.** Every one
of those rows is an unserved outcome that waited forty years. That's why they
converted so fast when the solution finally crossed the line — **there was no
demand to create, only a constraint to remove.**

**4. Read the fourth column of Block 2 and one pattern repeats.** The old
solution didn't merely fail — **it demanded from the user the very thing the user
was short of.** A finished sentence when they were stuck (L4). Editing time when
they had none (L3). Written confidence when writing was the weak point (L6). A
written source from someone who hadn't written anything yet (L7). Setup
commitment before any evidence (L8).

> **The diagnostic to hand the room: when a solution has existed for decades and
> nobody hires it, check whether it requires as input the thing the user came to
> you lacking.**

**5. Two rungs are the product's own footprints.** L9 and L10 could not have
existed before the product worked. Nobody needed noise handling until they were
dictating everywhere; nobody needed a habit-forming meter until the thing being
sold was a habit. **Watch which second-order job a company builds first — it
tells you where it thinks the money is.**

**6. Speed appears in exactly two rows, and never as the terminal reason.** L3
and L1 involve throughput. The other nine are about being read correctly,
thinking out loud, being allowed to start, not deciding. **Speed is the pitch on
the website. It is almost never why anybody stays.**

---

# Running it in class

Put the glance table up. Then take **three rungs**, one from each block, so the
shape of the ladder is visible rather than asserted:

| Rung | Why this one |
| --- | --- |
| **L0** | The ground floor, and the whole argument in one row. Ask the room how many sentences they typed *at a machine* last week versus in 2021. The answer is the market. |
| **L3** | The hinge in action. Same person, same voice, one line further down — and now there's a social job, so the product has to do something entirely different with the identical utterance. |
| **L10** | The pricing rung. It's the one they can apply on Monday: *is my free tier testing my capability, or letting a habit form?* |

**Then the exercise.** Give teams a consumer product and twenty minutes to build
the same four columns. Two tests of whether they've understood:

- **Is their bottom rung actually the bottom?** Most teams start three rungs too
  high, at a job that only exists once something below it is already solved.
- **Is anything in column four honestly marked "unchanged"?** A ladder where
  every row claims gen AI changed the context is a ladder written backwards from
  the conclusion. **The unchanged rows are usually where the money already was.**

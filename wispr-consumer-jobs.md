# The Consumer Job Map
## Ten jobs, one person, built up from the ground floor

**The scope.** One consumer. Their own laptop, their own phone, their own money.
No IT department, no procurement, nobody to get approval from.

**The table.** Four columns throughout:

| Column | What's in it |
| --- | --- |
| **1 — The job** | JTBD form — **When** *[circumstance]*, **I want to** *[motivation]*, **so I can** *[outcome]* — then the context explained, then outcome statements. |
| **2 — The feature** | The feature, or feature set, that solves it. Numbered as in [`wispr-flow-deep-dive.md`](wispr-flow-deep-dive.md) §4. |
| **3 — Pre-gen-AI context** | The circumstance before generative AI, and how well it was already served. Sometimes: *there was no circumstance.* |
| **4 — Post-gen-AI context** | The circumstance now, tagged **changed**, **unchanged**, or **created by adoption**. Where it's unchanged, the column says what moved instead. |

> **Two disciplines hold this document together.**
>
> **One: the verdict tag has to be earned.** Six of these ten rows are the same
> circumstance as 1995. Marking them honestly is what makes the other four mean
> something.
>
> **Two: the baseline was good, not bad.** Speech-to-text was a genuine
> achievement — turning sound into words reliably, on ordinary hardware, was hard
> and they solved it. What it left with the user was the last human step. Wispr's
> contribution is **additive**: cleanup, self-correction, personalisation, noise
> handling. Read the pre-gen-AI column as *what was already working*, not as a
> list of failures.

**Why the order matters.** Each job only becomes available once the one above it
is solved. Read top to bottom — it's the order a real user meets them in.

**Where it starts.**

> **Using technology stopped meaning operating it and started meaning describing
> what you want.**
>
> That is the ground floor. Speech isn't interesting because talking beats typing
> — that was true in 1985 and changed nothing. It's interesting because we now
> produce an enormous volume of language aimed at technology, and describing
> something is natively a spoken act. **The keyboard became the bottleneck in a
> job it had never been the bottleneck in before.**

---

## The ten jobs at a glance

| | The job, in one line | The feature that solves it | Verdict on the context |
| --- | --- | --- | --- |
| **J1** | Describe the problem instead of operating the tool | Hold-to-talk + every text field, no length penalty | **CHANGED — new circumstance** |
| **J2** | Get to the right answer by going back and forth | Cheap repeat turns + AI Commands | **CHANGED — new circumstance** |
| **J3** | Do it in the places I actually am | Canto + hold-to-talk + phone apps | **CREATED BY ADOPTION** |
| — | *— from here on, it has to sound human —* | | |
| **J4** | Reply to people at the speed I'd say it | The cleanup pass | UNCHANGED — the last mile moved to the product |
| **J5** | Say it before I've fully worked it out | Self-correction resolution | UNCHANGED — the precondition is gone |
| **J6** | One way of speaking, right wherever it lands | Context-awareness | UNCHANGED — but no pre-AI equivalent exists |
| **J7** | Be read the way I sound when I speak | Cleanup used for fluency | UNCHANGED — correction became rendering |
| **J8** | Think in one language, send in another | One-pass capture, cleanup, translation | UNCHANGED — three steps became one |
| **J9** | Be understood on my own vocabulary | Passive personalisation | UNCHANGED — setup moved after the value |
| **J10** | Be sure before I pay | Free tier metered in words, not features | **CHANGED — what you're buying is different** |

---
---

# Talking to technology
### Two circumstances that did not exist in 2021, and one the product created for itself.

| The job | The feature that solves it | Pre-gen-AI context | Post-gen-AI context |
| --- | --- | --- | --- |
| **J1 — Describe the problem instead of operating the tool**<br/><br/>**When** the way I get things done with technology is to describe what I want in my own words — the goal, the constraints, what to avoid — **I want to** say all of it without cutting it down to what I'm willing to type, **so I can** get something useful back the first time instead of the fourth.<br/><br/>**The context.** For forty years, using technology meant operating it: buttons, menus, three keywords in a search box. Now it means describing the problem — and the fuller the description, the better the result.<br/><br/>What gets lost is invisible. People drop the caveat, skip the example, leave out the constraint — not because they judged it unnecessary, but because it was another thirty seconds of typing. **The answer you get is shaped by how much you were willing to write.**<br/><br/>*Minimize the effort to give technology the full picture. Minimize the likelihood a poor result traces back to what I left out.* | **Hold-to-talk hotkey** and **every text field on the OS**. Press, speak, release, in the box you're already in.<br/><br/>**No penalty for saying more.** Speech runs about 3× typing, and the gap widens the longer you go — so the description you give is the description you meant.<br/><br/>Nobody reads your prompts, so nothing else is needed here. This is the one job here where raw speech would nearly do — which is why it's the ground floor. | **There was no such circumstance.**<br/><br/>Technology was operated, not described. The one place language went was a search box, and it rewarded fewer words. A generation learned to strip language out — three keywords, no sentence.<br/><br/>The keyboard was never a bottleneck in this job, because **the job did not exist.** | **CONTEXT CHANGED — the circumstance is new.**<br/><br/>Describing beats operating, and a longer description gets a better result. **The appetite for language inverted** — from keyword-minimising to context-maximising — in about eighteen months.<br/><br/>**Why it matters more now:** the only job here that grows with AI adoption rather than with population. |
| **J2 — Get to the right answer by going back and forth**<br/><br/>**When** the first answer is close but not quite it, **I want to** work it out in a back-and-forth — say what's off, see the next version, adjust again — **so I can** land on what I actually wanted instead of settling for the near miss.<br/><br/>**The context.** Good output isn't one instruction, it's a conversation: describe, react, refine. The quality comes from the number of passes, not from the first prompt.<br/><br/>The cost lands on the **marginal turn**. Turn one is obviously worth it; turn four has uncertain payoff. At thirty seconds of typing a turn, people stop early and keep the near miss. At five seconds of speech, they keep going.<br/><br/>*Minimize the cost of the next turn. Minimize the likelihood I stop before it's right.* | **Near-zero cost per turn** — same key, same field, no trip anywhere.<br/><br/>**AI Commands**: say the change instead of restating the content. "Make this shorter." "Bullet that."<br/><br/>**The effect worth naming:** voice doesn't only make each turn faster, it raises how many turns people take. More passes, better result — and that is very likely a real driver of the ~70% twelve-month retention, invisible in any words-per-minute metric. | **There was no such circumstance.**<br/><br/>Software was right or it was broken. Nothing was ever **80% right and improvable by talking to it**, so there was no back-and-forth to make cheap. | **CONTEXT CHANGED — the circumstance is new.**<br/><br/>Output is negotiable, and iteration is now the main way a person gets to quality.<br/><br/>**Why it matters more now:** as more of what a consumer produces begins as a model's draft, the share of the day spent in this loop keeps rising. |
| **J3 — Do it in the places I actually am**<br/><br/>**When** the places I work are a café, a shared flat, an open-plan floor and a phone on a train, **I want to** speak and get the same result I'd get alone at a quiet desk, **so I can** use this everywhere instead of only when the room is right.<br/><br/>**The context.** Once talking to technology is how you work, the room becomes the limit. And the damage isn't the occasional bad take — it's **not knowing in advance**. A tool you have to test first becomes the fallback, and typing stays the default. Habits form on defaults.<br/><br/>*Minimize the likelihood the result depends on where I'm sitting. Minimize the effort to judge whether it will work before I start.* | **Canto**, their own speech model tuned for noise — word error in noisy environments reported down from over 30% to 5–10%.<br/><br/>**Hold-to-talk**, so nothing is listening in a shared room.<br/><br/>**iOS and Android**, carrying the same learned vocabulary.<br/><br/>**Noise handling isn't a spec upgrade.** It's what makes the habit portable. | **You could not have this problem.**<br/><br/>Nobody was speaking to their computer all day, so no room was ever the constraint.<br/><br/>Where dictation did exist it was built for a quiet desk and a good headset — an entirely reasonable design for the hardware of its time, and it worked well in those conditions. | **CONTEXT CREATED BY ADOPTION — second-order.**<br/><br/>You speak all day, so **the room becomes the binding constraint on where you can work.** The product's own success manufactured the circumstance.<br/><br/>**The strategic reading:** the limit on the market was never accuracy in a quiet room. It was that most work doesn't happen in one. Canto didn't so much improve the product as **enlarge the set of places it works.** |

---

> ## It has to interact like a human
>
> Everything above is aimed at a machine. Nobody else reads it, so rough speech
> is fine.
>
> Everything below is aimed at a person, which means the product has to handle the
> exchange the way another person would — because of **how people actually talk.** Nobody speaks in finished sentences. You start
> before the idea is fully formed. You say "um" and "sort of". You circle back and
> correct yourself halfway through. That isn't sloppiness; it's what thinking out
> loud sounds like.
>
> **So the whole of the next block is one job wearing six different sets of
> clothes: take the way a person naturally speaks, and turn it into text that
> reads as though it had been written carefully.** Fillers removed, corrections
> resolved, the sentence put back in order.
>
> That capability is Wispr's real contribution. Speech-to-text was already good;
> **this is what was added on top of it**, and it is why a forty-year-old tool
> became something people reach for fifty times a day.

---
---

# Talking the way people actually talk
### Six circumstances identical to 1995. The last human step moved from the user to the product.

| The job | The feature that solves it | Pre-gen-AI context | Post-gen-AI context |
| --- | --- | --- | --- |
| **J4 — Reply to people at the speed I'd say it**<br/><br/>**When** I have forty messages waiting and twenty minutes before I have to be somewhere, **I want to** answer them by speaking, **so I can** clear them without the queue following me home.<br/><br/>**The context.** Speaking is about three times faster than typing, so on paper this was always solvable. What stopped it is that spoken words written down verbatim don't look like what you would have written — no punctuation, fillers intact, sentences that restart. So you'd tidy them, and the tidying cost roughly what typing would have.<br/><br/>*Minimize the likelihood the text needs editing before it's sent. Minimize the likelihood the reader can tell it was spoken.* | **The cleanup pass.** Fillers out, punctuation in, the thought restructured into prose.<br/><br/>**This is the product.** Everyone assumes the product is the transcription; transcription was the commodity they were happy to rent for two years. The value is here, and it's the one part nobody outside the company can see. | **Identical circumstance.** The inbox was always full — this row reads the same in 1995.<br/><br/>**And the hard part was already solved.** Dictation turned sound into words reliably, which was a real engineering achievement.<br/><br/>What it left with the user was **the last mile**: punctuation, fillers, the shape of the sentence. | **CONTEXT UNCHANGED — the last mile moved to the product.**<br/><br/>The text arrives finished, so it can be sent as spoken.<br/><br/>**Why it's newly relevant:** the habit now arrives pre-formed from J1–J3. Nobody is being asked to try speaking any more — they're being asked to stop making an exception for messages to humans. |
| **J5 — Say it before I've fully worked it out**<br/><br/>**When** the idea isn't fully formed as I start speaking — I trail off, restart, change my mind mid-sentence — **I want to** have the text come out as what I settled on, **so I can** think out loud instead of composing in my head first.<br/><br/>**The context.** This is the most human thing here. Real speech is full of false starts and self-corrections: *"send it Tuesday — no, sorry, Wednesday."*<br/><br/>Written down as spoken, that isn't merely untidy. Someone could act on the wrong half of it — which means checking every message before it goes.<br/><br/>*Minimize the likelihood the text keeps something I retracted. Minimize the effort to start a sentence I haven't finished.* | **Self-correction resolution.** Say *"Tuesday — no, sorry, Wednesday"* and the text reads **"Wednesday."**<br/><br/>Plus **restructuring**, which puts a thought that arrived out of order back into order.<br/><br/>**Looks like a demo trick; it's load-bearing.** If you can't change your mind mid-sentence, you have to know the sentence before you start — which is exactly what someone facing a blank page doesn't have. | **Identical circumstance, and ancient.** People have never spoken in finished sentences.<br/><br/>Speaking in complete, pre-formed sentences was the price of admission, and a fair one: the system had **no way to know which half of a correction you meant.** Transcribing faithfully was the correct behaviour for what it could know. | **CONTEXT UNCHANGED — the precondition is gone.**<br/><br/>The model can read intent from an utterance, so you can speak the way you think.<br/><br/>**Why it's newly relevant:** far more of what people produce now is first-draft thinking. Describing something to a model usually means working out what you want *while* saying it. |
| **J6 — One way of speaking, right wherever it lands**<br/><br/>**When** the same thought has to reach a friend on WhatsApp, my landlord by email and a model in a chat window inside ten minutes, **I want to** say it once, my way, and have each one come out right, **so I can** stop rewriting myself for every channel.<br/><br/>**The context.** "Hey, can you look at this?" is right in one window and wrong in another. Choosing the tone isn't typing work — it's **judging the reader**, and you pay it once per message, dozens of times a day.<br/><br/>You've already made that judgement, though. You made it when you picked the window.<br/><br/>*Minimize the effort to make the same content fit a different destination. Minimize the number of instructions I must give before I can start speaking.* | **Context-awareness.** Reads the active application and adapts tone and formatting.<br/><br/>**It never asks.** Asking would hand the composition work straight back — "make this formal" is itself the thing you were trying to avoid doing in your head. | **Identical circumstance.** People have always written to different audiences in one sitting.<br/><br/>Nothing could infer tone, and nothing was expected to — **tone isn't a setting, it's a read of a situation.** Output came out flat, and adapting it was the user's job. | **CONTEXT UNCHANGED — but this feature has no pre-AI ancestor.**<br/><br/>The product infers **where the text is going**, and the destination sets the register.<br/><br/>**Why it matters more now:** the number of channels one person writes in keeps climbing, and the tone tax climbs with it — paid per message, silently, by everyone. |
| **J7 — Be read the way I sound when I speak**<br/><br/>**When** I'm writing to people who'll judge me on the writing, in a language I speak more easily than I write, **I want to** have the text read as fluently as I sound in a room, **so I can** be judged on what I said rather than on how I wrote it.<br/><br/>**The context.** Very many people speak a language far more confidently than they write it. The gap isn't speed, it's confidence — and it shows up most in the writing that matters most.<br/><br/>The visible cost is small mistakes. **The larger cost is what doesn't get written** — arguments shortened, points hedged, opinions held back because writing them is effortful.<br/><br/>*Minimize the likelihood I'm read as less capable than I am. Minimize the likelihood I hold back a point because writing it is costly.* | **The same cleanup pass, doing a different job.** It renders your meaning in fluent prose rather than flagging what's wrong with your draft.<br/><br/>Same feature as J4, entirely different value — which is why *"what does this feature do"* is the wrong question to ask of it. | **Identical circumstance, and very large.**<br/><br/>**Grammar checkers did their job well** — they find errors in a sentence that already exists, and they're good at it.<br/><br/>But the hesitation comes **before** the sentence. Nothing addressed the moment where someone decides not to write the paragraph at all. | **CONTEXT UNCHANGED — correction became rendering.**<br/><br/>The fluent version is the first version you see, so the hesitation never gets its moment.<br/><br/>**Why it's newly relevant:** more professional judgement passes through text than ever — remote, async, written-first. This row lands hardest with an Indian cohort and is nearly invisible in a US-centric reading. |
| **J8 — Think in one language, send in another**<br/><br/>**When** the thought arrives in my first language and the message has to go out in English, **I want to** say it as it comes and get English out, **so I can** think at my own speed instead of translating as I go.<br/><br/>**The context.** Translating happens *while you compose*, in working memory, at the same time as the thinking. It's a second live task competing for the same attention — and attention is the scarce thing, because the thought is already at risk of slipping while you hold it.<br/><br/>*Minimize the effort to move a thought from the language it arrived in to the language it has to ship in. Minimize the steps between the thought and the sent message.* | Capture, cleanup and translation in **a single pass**.<br/><br/>The feature isn't translation — translation was excellent and free. The feature is that translation **stopped being a separate step with its own input requirement.** | **Identical circumstance.**<br/><br/>**Translation tools were genuinely good** and cost nothing. They simply needed a **written source** — so you had to finish the step you were trying to skip before you could use them. | **CONTEXT UNCHANGED — three steps became one.**<br/><br/>One utterance in, finished text out in the target language.<br/><br/>**Why it matters more now:** with translation as a separate step, people quietly trade off between speed and their own language, and mostly choose to think in English, less well. Collapsing the step removes the trade. |
| **J9 — Be understood on my own vocabulary**<br/><br/>**When** the words that carry the most meaning in my day are names, places and terms no general system has heard, **I want to** have them come out right from the start, **so I can** trust it without having to teach it first.<br/><br/>**The context.** The words that get misheard are the load-bearing ones — a colleague, a client, the thing the message is actually about. Getting them wrong doesn't make the text untidy; it makes it wrong.<br/><br/>The fix used to come first: build the profile, then get the benefit. That ordering asks for commitment before evidence.<br/><br/>*Minimize the setup before first useful output. Minimize the likelihood the names specific to my life come out wrong.* | **Passive personalisation.** It picks up your names, jargon and style as you use it. No enrollment, no dictionary.<br/><br/>The effect is on the **shape of the payoff**: usable at minute one, better at week four. Improvement becomes a reward for staying rather than a toll for entering. | **Identical circumstance.** Your vocabulary was always yours.<br/><br/>**Custom dictionaries and voice profiles worked well.** They just had to be built before you knew whether you'd stay.<br/><br/>That cost made complete sense for people who had no alternative — which is a large part of why the category stayed specialised for so long. | **CONTEXT UNCHANGED — setup moved after the value.**<br/><br/>**This is what let a general audience in.** The specialised market was never small demand; it was the only group for whom the setup cost already made sense. Move the cost, and the rest of that demand becomes reachable. |

---
---

# Paying for it

| The job | The feature that solves it | Pre-gen-AI context | Post-gen-AI context |
| --- | --- | --- | --- |
| **J10 — Be sure before I pay**<br/><br/>**When** I'm deciding whether this is worth a monthly subscription, for a way of working I've never had before, **I want to** use the real thing on my own words until I know, **so I can** pay for something I've already proved to myself.<br/><br/>**The context.** The claim — *it produces text I can send* — can't be checked by reading about it. It's only checkable on **your** speech, **your** names, **your** messages. A feature-limited trial tests a different product, so you'd learn whether you like a lesser thing.<br/><br/>*Minimize the likelihood I pay for something that doesn't work on my material. Minimize the likelihood the version I try isn't the version I'd buy.* | **The free tier metered in words, not features** — ~2,000 a week on desktop, ~1,000 on the phone. **The product is identical; you simply run out.** Plus a 14-day full trial, no card.<br/><br/>**Running out turns a prediction into a memory.** By the time you hit the wall you know exactly what you'd lose.<br/><br/>**The rule: for a habit product, meter the volume, never the capability.** A feature-gated free tier would never have produced ~70% twelve-month retention — what's retained is a reflex, and a reflex can't form around something you're only allowed to half-use. | **You were buying a capability.**<br/><br/>Consumer software was a set of things it could do, and a capability can be judged from a list before you pay. Does it do X? Yes or no.<br/><br/>Trials demonstrated features, and that was **the right shape for what was being sold.** | **CONTEXT CHANGED — you're buying a habit.**<br/><br/>What's being paid for is a change in how getting words out feels, fifty times a day. **A habit can't be judged from a description. It can only be judged by forming one.**<br/><br/>So the free tier's job isn't to demonstrate features. It's to let the habit exist, then ask for money at the moment it's real. **Gen AI changed what a consumer software purchase is, and the pricing page is where that shows.** |

---
---

# What the table shows

**1. The first three jobs built the market for the rest.** Talking to a machine
has no reader, so people learned the habit with nothing at stake. Once the reflex
existed, typing to a human felt like a step backwards. **Gen AI didn't only make
the old job solvable — it created a low-stakes job where the habit could form
first.**

**2. Two of the ten circumstances are genuinely new, and they're the ones that
compound.** J1 and J2 grow with AI adoption. J4–J9 grow with population, which
moves a few percent a year.

**3. Six of the ten are the same circumstance as 1995.** Nothing about the user's world
moved. Those are forty-year-old outcomes finally being served, which is why they
converted so quickly — **no demand to create, only a last step to take on.**

**4. Read the human-directed rows' pre-gen-AI column and the pattern is
additive, not corrective.** The earlier tools had already solved their hard parts — reliable
transcription, good grammar checking, free translation, working dictionaries.
Each one left **the last human step with the user**: the finished sentence, the
tidy-up, the written source, the profile built up front. Wispr's contribution is
that it took those steps on.

> **The diagnostic for the room: when something has existed for decades and
> people still don't use it, look at the last step it leaves with the user — and
> ask whether that step is the one they came to you short of.**

**5. Two jobs are the product's own footprints.** J3 and J10 could not have
existed before it worked. Nobody needed noise handling until they were speaking
everywhere; nobody needed a habit-forming meter until the thing being sold was a
habit.

**6. Speed is rarely the reason.** Most of these jobs are about being understood,
thinking out loud, and being able to start. **Speed is the pitch on the website.
It is almost never why anybody stays.**

---

# Running it in class

Take **three jobs**, one from each group:

| Job | Why this one |
| --- | --- |
| **J1** | The ground floor and the whole argument in one row. Ask the room how many sentences they typed *at a machine* last week versus in 2021. The answer is the market. |
| **J5** | The most human of the ten, and the best live demo. Say a sentence, change your mind halfway, watch the text keep only what you settled on. |
| **J10** | The pricing job, and the one they can use on Monday: *is my free tier testing my capability, or letting a habit form?* |

**Then the exercise.** Give teams a consumer product and twenty minutes to build
the same four columns. Two tests:

- **Is their first job actually the first?** Most teams start too high, with a job
  that only exists once something under it is already solved.
- **Does any row honestly say UNCHANGED?** A table where every row claims gen AI
  changed the context was written backwards from its conclusion. **The unchanged
  rows are usually where the money already was.**

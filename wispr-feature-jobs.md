# The Wispr Flow Feature–Job Map

Fourteen features, each taken down to the job it actually serves.

**The method, and why it's this one.** A feature list describes the product. A
job describes the user. The way you get from one to the other is to refuse the
first answer — the first "why" always restates the spec — and keep asking until
the answer stops being about the product at all. Five levels is usually where
that happens.

Each feature below is worked in the same fixed shape:

1. **What it is** — the feature, one line, as documented in
   [`wispr-flow-deep-dive.md`](wispr-flow-deep-dive.md) §4.
2. **The context** — the circumstance in thick description. Not a user type. A
   moment.
3. **The five whys** — each level pushed until it stops being about the feature.
4. **Terminal motivation** — where the chain bottoms out. This is the thing the
   user is actually buying.
5. **Outcome statements** — in the two house forms: *minimize the time it takes
   to…* / *minimize the likelihood that…*
6. **The job** — **When** *[circumstance]*, **I want to** *[motivation]*, **so I
   can** *[outcome]*.

Then each is tied back to the thirteen-job portfolio in
[`wispr-jobs.md`](wispr-jobs.md), or flagged where it serves a job that
portfolio doesn't contain.

> **Read levels 1 and 2 sceptically.** They are almost always the feature
> restated. The content starts at level 3. **If a chain terminates by level 2,
> what you have is a spec item, not a job** — and that is a genuinely useful
> test to run on your own backlog.

> **An honesty note, in keeping with the rest of this pack.** The features are
> documented and sourced. The why-chains are *analytical constructions* — they
> are what the forces and the reported behaviour imply, not what users said in
> interviews. Present them as hypotheses with a test attached, not as findings.
> The distinction is the whole difference between JTBD as a discipline and JTBD
> as a storytelling device.

---

## The master table

| # | Feature | Terminal why — what they're really buying | Portfolio job |
| --- | --- | --- | --- |
| **F1** | Hold-to-talk hotkey | To stop deciding whether an utterance is worth it | J12, partly — mostly **new** |
| **F2** | Canto — own noise-robust model | To have one way of working instead of one per room | **J12** |
| **F3** | Cleanup / intent rendering | To stay in thinking mode from thought to sent | **J4, J5** |
| **F4** | Self-correction resolution | To be finished with a thought when they stop speaking | **J5, J11** |
| **F5** | Context-awareness | To hand over the execution of a decision, not the decision | **J4** + the social layer |
| **F6** | Passive personalisation | To be able to commit — to stop keeping typing warm | **J7 inverted** |
| **F7** | AI Commands | To have their standards, not friction, set their quality | **J2** — extended to human-directed text |
| **F8** | Every text field in the OS | To change the texture of the day, not the speed of a task | **J4, J6** |
| **F9** | Cross-platform / mobile | To keep one accumulating asset available everywhere | **J8** |
| **F10** | Fluency rendering | To be assessed on their thinking, not their second language | **J9** |
| **F11** | Speak one language, ship another | To think in their fastest language and still ship | **J10** |
| **F12** | Word-metered free tier | To buy back a habit rather than buy a promise | **NEW — a decision job** |
| **F13** | Teams tier, shared admin | To turn a personal discovery into a team decision, safely | **NEW — a champion's job** |
| **F14** | SOC 2, SSO, enforced HIPAA | To be *allowed* to use it on the work that counts | **J13** |

**Pro ($15/mo) is not on this list on purpose.** Unlimited dictation is the
removal of F12's meter, and "all platforms" is F9. A tier is a packaging of
features, and packaging serves the buying job (F12), not a job of its own.
Putting it on the list would be describing the price sheet and calling it
analysis.

---
---

# Family A — Features that buy the reflex

*These have no visible output. Each one exists so the product can become
automatic rather than considered — and the whole business model depends on
automatic, because the value is in the marginal utterance.*

## F1 — Hold-to-talk, not always-listening

> *What it is:* a hotkey. Press, speak, release. No wake word, no ambient
> microphone, no accidental activation.

**The context.** A microphone-driven tool is being installed on the machine
somebody does their work on, in a room with other people in it, under an IT
policy they didn't write. Nothing has been dictated yet. This is a moment of
*deciding*, not of using.

**The five whys**

| | Why? | Because… |
| --- | --- | --- |
| **1** | Why hold a key instead of saying a wake word? | They want to know exactly when the microphone is live. |
| **2** | Why does knowing that matter? | Because with an ambiguous microphone, every sentence spoken in the room becomes something they have to think about — including the ones not meant for it. |
| **3** | Why is that thinking cost fatal rather than annoying? | Because a tool that makes you monitor your own speech is a tool you hold at arm's length. It never becomes a reflex — and this product only pays off at reflex frequency. |
| **4** | Why does it need reflex frequency rather than deliberate use? | Because the value sits in the *marginal* utterance: the fourth turn with a model, the reply you'd have skipped. Deliberate use captures only the utterances that were obviously worth it. Reflex captures the long tail, which is most of the volume. |
| **5** | Why does the user want the long tail captured? | Because what they actually want is for the gap between having a thought and it being on screen to stop being something they decide about. **The deciding is the tax, not the typing.** |

> **Terminal motivation:** to stop deciding whether a thing is worth saying.

**Outcome statements**

- Minimize the likelihood that the microphone is active when I did not intend it.
- Minimize the effort to decide whether to use the tool for any given utterance.
- Minimize the likelihood that colleagues, or my IT department, treat it as a listening device.

**The job**

> **When** I'm putting a microphone-driven tool on the machine I do my actual
> work on, in a room with other people in it, **I want to** know with certainty
> that it hears me only while I'm holding a key, **so I can** use it without
> thinking about it instead of rationing it to moments when I'm alone.

**Why this is the most teachable feature in the product.** On paper they chose
the worse interaction — more friction, an extra motor action, no hands-free. The
chain shows why that's the right trade: the friction they added is *per
utterance and tiny*; the friction they removed is *ambient and constant*.
Restricting a capability to buy trust is a recurring AI-native move, and it is
almost always misread as conservatism.

---

## F2 — Canto, the noise-robust speech model

> *What it is:* their own ASR model, tuned for noisy environments. Word error
> rate in noise reported to fall from over 30% to 5–10%.

**The context.** The user is in a café, on an open-plan floor, in an airport, or
at home with family in the next room. This is not an edge case. **This is where
work happens.**

**The five whys**

| | Why? | Because… |
| --- | --- | --- |
| **1** | Why does accuracy in noise matter specifically? | Because the rooms they work in are rarely quiet, so a tool that works in quiet rooms works during a minority of their working hours. |
| **2** | Why does partial coverage break it rather than just limit it? | Because they can't tell in advance which rooms will work. Every use starts with an unstated test. |
| **3** | Why is unpredictability worse than a known limitation? | Because a tool you must test becomes the *fallback*, and typing stays the default. Habits form on defaults — and the default here has twenty-five years of muscle memory behind it. |
| **4** | Why does the user default to typing even believing voice is better? | Because the failure is asymmetric: a garbled transcription in a noisy room costs more than the seconds it saved. Under uncertainty, typing is the rational choice — **uncertainty alone is enough to prevent the hire, without a single actual failure.** |
| **5** | Why won't they just absorb the occasional bad take? | Because they came here to stop supervising the mechanics of getting words down. A tool that makes them assess the room first has handed the supervision back. |

> **Terminal motivation:** to have one behaviour that works everywhere, rather
> than a behaviour plus a set of conditions.

**Outcome statements**

- Minimize the likelihood that output quality depends on where I happen to be sitting.
- Minimize the effort to predict whether the tool will work before I use it.
- Minimize the likelihood I have to change rooms to do my work.

**The job**

> **When** the place I'm actually working is a café, an open-plan floor or a
> house with other people in it, **I want to** get the same output I'd get in a
> quiet room, **so I can** have one way of working instead of one for quiet
> rooms and a fallback for everywhere else.

**The reframe worth a slide.** Canto reads as a quality upgrade and gets
discussed as vertical integration and margin. The chain says something sharper:
**the constraint on the total addressable market was never accuracy — it was
that most work does not happen in a quiet room.** They didn't improve the
product. They enlarged the set of places it exists in.

---

## F6 — Passive personalisation

> *What it is:* it learns your names, jargon, acronyms and style over time. No
> voice enrollment, no custom dictionary, no training session.

**The context.** The user's working vocabulary is dense with proper nouns no
general model has ever seen — colleagues, internal systems, product codenames,
clients. In week one, those are exactly the words that come out wrong.

**The five whys**

| | Why? | Because… |
| --- | --- | --- |
| **1** | Why does it need to learn their vocabulary? | Because the words that get misrecognised are disproportionately the ones carrying the meaning: names, systems, clients. |
| **2** | Why not just train it up front, the way Dragon required? | Because up-front training is a payment made towards a tool they haven't yet decided to trust. |
| **3** | Why is that ordering fatal rather than merely irritating? | Because it inverts the adoption sequence — commitment demanded *before* evidence. The only people who accept that are the ones with no alternative. **That is the entire reason the category stayed a niche for forty years.** |
| **4** | Why does passive learning fix it? | Because it reshapes the payoff curve: usable at minute one, better at week four. Improvement becomes a reward for staying rather than a toll for entering. |
| **5** | Why does the user care that it improves, if it's already usable? | Because they're deciding whether to make it the *default*. A tool that gets better as you use it is safe to build a habit on. A static one has a known ceiling, so you keep the old method alive alongside it — and a method kept alive is a method you fall back to. |

> **Terminal motivation:** to be able to commit — to stop keeping typing warm as
> a hedge.

**Outcome statements**

- Minimize the setup effort before first useful output.
- Minimize the likelihood that names, jargon and acronyms specific to my work come out wrong.
- Minimize the effort to teach the tool anything, ever.

**The job**

> **When** half the words that matter in my work are names and acronyms no
> general system has heard, **I want to** have them come out right without ever
> sitting down to teach them, **so I can** find out whether this works for me
> before I've invested anything in it.

**This is J7 turned inside out.** `wispr-jobs.md` J7 makes the point that
Dragon's users were the only segment whose forces already resolved — push high
enough to absorb enrollment, training and cost. Passive personalisation is the
feature that *removes the need for that push*. It doesn't serve the niche
better; it deletes the entry cost that made it a niche.

---

## F8 — Every text field in the operating system

> *What it is:* it isn't an app you go to. It activates inside whatever field
> the cursor is already in, anywhere on the OS.

**The context.** The user's work isn't in one application. It's scattered across
thirty, and text fields are the connective tissue between them. Most of what
they write is one to three lines long.

**The five whys**

| | Why? | Because… |
| --- | --- | --- |
| **1** | Why must it work everywhere rather than in one good app? | Because the text always has a destination, and the destination is never the dictation app. |
| **2** | Why does routing through a dictation window fail? | Because it adds a switch, a copy and a paste to a task that was supposed to be *faster* than typing. |
| **3** | Why does a small trip destroy a large speed advantage? | Because the advantage is per-utterance and measured in seconds, while the trip is fixed and comparable in size. **Fixed overhead eats variable gains on short tasks — and almost every task is short.** |
| **4** | Why do the short tasks matter more than the long ones? | Because the long ones are rare. What produces fifty hires a day is two-line replies — exactly the tasks a round trip disqualifies. |
| **5** | Why does frequency matter more to them than magnitude? | Because they aren't buying a faster way to write documents. They're buying a change in how getting words out *feels* — and something you do fifty times a day changes how a day feels. Something you do twice doesn't. |

> **Terminal motivation:** to change the texture of the whole working day, not
> the duration of one task.

**Outcome statements**

- Minimize the number of steps between speaking and the text being where it belongs.
- Minimize the likelihood I must leave what I'm doing to use the tool.
- Minimize the time cost of using the tool on a two-line task.

**The job**

> **When** the thing I need to write is two lines long and I'm already in the
> field it belongs in, **I want to** say it right there, **so I can** use this
> for the small things instead of saving it for the ones big enough to justify
> a trip.

> **Placement beats capability.** A worse model in the field you're already
> typing in beats a better model one context-switch away. This is a product
> decision that gets filed as a distribution decision, which is why competitors
> keep matching the model and losing.

---

## F9 — Mac, Windows, iOS, Android

> *What it is:* the same product, with the same learned vocabulary, on every
> device the user works on.

**The context.** The user is on a train, on a phone, and what they need to write
is longer than a thumb-typed line.

**The five whys**

| | Why? | Because… |
| --- | --- | --- |
| **1** | Why does it need to be on the phone too? | Because a behaviour that only exists at a desk isn't a habit — it's a desk behaviour. |
| **2** | Why is partial coverage worse than it looks? | Because the phone is where the push is *highest*. Thumb-typing hurts more than typing. The moments of greatest need are precisely the ones a desktop-only tool misses. |
| **3** | Why hasn't free phone dictation already solved this? | It shipped on every handset for a decade against a bigger push and still lost (J8). Output that wasn't sendable. **Push was never the binding constraint — on any platform.** |
| **4** | Why do they need *this* tool on the phone rather than the OS one? | Because what makes the output sendable is that it knows their names, their jargon, their style. Without that, the phone version fails in exactly the way that killed the category. |
| **5** | Why does the user think of that as something they'd lose? | Because once it has learned them, switching costs them the learning. They stop choosing a feature and start maintaining an asset. **That makes cross-platform a retention feature, not a coverage feature.** |

> **Terminal motivation:** to keep one accumulating asset — a machine that knows
> how they talk — present everywhere they work.

**Outcome statements**

- Minimize the likelihood the tool is unavailable where I happen to be.
- Minimize the likelihood I fall back to a worse method away from my desk.
- Minimize the likelihood that what the tool has learned about me is lost when I change device.

**The job**

> **When** I'm away from my desk and what I need to write is longer than a
> thumb-typed line, **I want to** use the same thing that already knows my names
> and my style, **so I can** do the same quality of work on a train as at a
> desk.

---
---

# Family B — Features that buy standing

*These are the ones with visible output, and every chain runs through somebody
else's eyes. The social layer of the job — "produce text nobody can tell was
dictated" — lives entirely here.*

## F3 — Cleanup and intent rendering

> *What it is:* fillers removed, grammar repaired, stream-of-consciousness
> restructured into prose. **Layer 3 of the stack — the part that is actually
> the product.**

**The context.** The user speaks the way people speak. Restarts. "Um." A
trailing clause. A sentence that changes direction halfway through and never
comes back to fix its beginning.

**The five whys**

| | Why? | Because… |
| --- | --- | --- |
| **1** | Why do they want the fillers gone? | Because speech written down verbatim doesn't read as thinking. It reads as carelessness. |
| **2** | Why does that reading matter — the content is identical? | Because in a written channel the form *is* part of the message. The reader has no tone, no face, no room to go on. They infer how much you cared from the prose. |
| **3** | Why does the user care what a reader infers about their care? | Because most of their professional standing is transmitted through text they never thought was important — a Slack reply, a two-line email. Standing is built out of those, not out of the documents they polished. |
| **4** | Why not simply edit before sending? | They can, they did, and that is exactly what made dictation a net loss for forty years. But the real cost isn't the minutes — it's that editing forces them back into the careful, line-by-line, *written* mode they were trying to escape. |
| **5** | Why is being forced back into that mode the actual injury? | Because the point was to keep thinking. Every return to the text as an editor is a switch out of thought and into production. **They don't want faster typing. They want to not switch.** |

> **Terminal motivation:** to stay in thinking mode from the start of the thought
> to the moment it's sent.

**Outcome statements**

- Minimize the likelihood the output needs editing before it can be sent.
- Minimize the likelihood the recipient can tell it was dictated.
- Minimize the number of times I must re-enter a piece of text after speaking it.

**The job**

> **When** what comes out of my mouth is the way people actually talk — restarts,
> fillers, a sentence that changes direction halfway — **I want to** get back
> what I *meant* rather than a faithful record of how I said it, **so I can**
> send it without going back in as my own editor.

**Why level 4 is the one to put on the slide.** It explains the forty years. The
standard story is "editing ate the time saved," which is true and shallow. The
deeper cost is a **mode switch**: the old tool made you produce as a speaker,
then re-enter as an editor, twice per message. The saving was never the issue.
The oscillation was.

---

## F4 — Self-correction resolution

> *What it is:* say *"send it Tuesday — no, sorry, Wednesday"* and the output
> reads **"Wednesday."** Old dictation transcribed the confusion faithfully.

**The context.** A moment mid-utterance where the user changes their mind. It
happens constantly in speech and essentially never in typing, because typing
lets you delete before anyone sees.

**The five whys**

| | Why? | Because… |
| --- | --- | --- |
| **1** | Why must the correction be resolved rather than transcribed? | Because otherwise the output contains both the wrong answer and the right one, and the reader has to work out which is which. |
| **2** | Why is that worse than a missing comma? | Because it's a *semantic* error with a plausible reading. A typo is self-evidently a typo. "Tuesday — no, Wednesday" left in a message can be acted on wrongly. |
| **3** | Why does the risk of a wrong action change behaviour so sharply? | Because it makes reading before sending **mandatory**. A risk to style costs you embarrassment; a risk to substance costs you a review pass on every single message. |
| **4** | Why is the mandatory review the thing that kills it? | Because verifying text means re-reading it at reading speed — which is slower than saying it was in the first place. **Review is composition's twin, and it gives the whole advantage back.** |
| **5** | Why does the user care so much about not re-reading? | Because they want to be *done* with a sentence when they finish saying it. Speaking is a release. If the sentence comes back for inspection, it was never released — it was just parked. |

> **Terminal motivation:** to be finished with a thought at the moment they stop
> speaking.

**Outcome statements**

- Minimize the likelihood the output contains something I retracted.
- Minimize the likelihood I must read the output before sending it.
- Minimize the effort to change my mind in the middle of a sentence.

**The job**

> **When** I change my mind halfway through saying something, **I want to** have
> the machine keep the version I settled on rather than both, **so I can** think
> out loud instead of composing in my head first.

**This is the load-bearing feature, not the party trick.** It's the best thirty
seconds of any demo, but the chain shows it's also the thing that makes J5 — the
blank page — possible at all. **If you cannot change your mind mid-sentence, you
must know the sentence before you start.** And knowing the sentence before you
start is precisely the input the person staring at a blank page does not have.
Every "talk your way into it" use of this product rests on F4.

---

## F10 — Fluency rendering

> *What it is:* the cleanup layer renders meaning in fluent English, rather than
> flagging errors in the user's English.

**The context.** Someone who speaks English fluently and confidently in a
meeting, and writes it more slowly and less confidently. Enormous numbers of
people — and, per `wispr-jobs.md`, the segment an Indian cohort recognises
instantly and a US-centric reading misses entirely.

**The five whys**

| | Why? | Because… |
| --- | --- | --- |
| **1** | Why do they want their speech rendered as fluent written English? | Because the gap between how they sound in a meeting and how they read on the page is costing them. |
| **2** | Why is it costing them? | Because most of the people who assess them do it from text — a written update, a proposal, a thread — not from the meeting they were good in. |
| **3** | Why doesn't a grammar checker close it? | Because a checker acts *after* the sentence exists, and the anxiety is *before*. Flagging errors confirms the fear rather than removing it, and it can't supply confidence about a sentence not yet written. |
| **4** | Why is the anxiety the operative cost rather than the errors? | Because anxiety changes *what* gets written, not just how. It makes them shorter, more hedged, less likely to volunteer the argument. **The visible errors are trivial next to the sentences that never got written.** |
| **5** | Why does that matter beyond any one document? | Because the things they don't write are the things that would have made the case for them. Being read as less capable than you are, in the channel where capability is judged, is a career problem wearing a writing problem's clothes. |

> **Terminal motivation:** to be assessed on their thinking rather than on the
> fluency of their second language in writing.

**Outcome statements**

- Minimize the likelihood I am read as less capable than I am.
- Minimize the effort to produce text in a language I speak better than I write.
- Minimize the likelihood I shorten or withhold an argument because writing it is costly.

**The job**

> **When** I'm writing to people who will judge me by the writing, in a language
> I speak better than I write, **I want to** produce text as fluent as I sound in
> a room, **so I can** be read as the person who spoke in the meeting.

**Level 4 is the finding.** Every competitor in this space is optimising the
correction of errors that exist. The chain says the real damage is *suppression*
— arguments not made, updates kept short, opinions not volunteered. That damage
is invisible in any metric a writing tool collects, because it consists entirely
of text that was never produced. **The largest cost of a bad tool is usually
non-consumption, and non-consumption leaves no logs.**

---
---

# Family C — Features that buy authorship

*The chains here all terminate at the same boundary: the user will hand over the
execution of a decision, and will not hand over the decision. Where that line
sits is the central design question of every AI product, and these three
features are Wispr's answer to it.*

## F5 — Context-awareness

> *What it is:* it reads the active application and adapts register and
> formatting. The same sentence becomes a Slack message, an email, or a code
> comment depending on where the cursor is.

**The context.** The same person writes a Slack message, a client email and a
code comment inside ten minutes, in the same voice, in the same room, with the
same thought behind two of them.

**The five whys**

| | Why? | Because… |
| --- | --- | --- |
| **1** | Why should the output be shaped by the app? | Because the same sentence is right in one channel and wrong in another. "hey, can you look at this?" is correct in Slack and career-limiting in a client email. |
| **2** | Why not just tell it which register you want? | Because specifying register is itself composition work. If you must say "make this formal," you've reintroduced the pre-formed-sentence tax the product exists to remove. |
| **3** | Why is such a small decision so expensive? | Because it isn't one decision. It's one per message, fifty times a day, and each requires modelling a reader. **Modelling the reader is the actual labour of workplace writing. The typing was never the hard part.** |
| **4** | Why should a machine do that modelling? | Because the destination is an excellent proxy for the reader — and the user's model of the reader is already *encoded in the window they chose*. They aren't outsourcing judgement. They're outsourcing the execution of a judgement they already made. |
| **5** | Why does that distinction matter to them? | Because they'll accept a machine that renders their intent and won't accept one that forms it. **Choosing where it goes is the part they want to keep.** |

> **Terminal motivation:** to hand over the execution of a decision without
> handing over the decision.

**Outcome statements**

- Minimize the effort to adapt the same content to a different destination.
- Minimize the likelihood the register is wrong for where the text lands.
- Minimize the number of instructions I must give before I can start speaking.

**The job**

> **When** the same thought has to become a Slack message now and a client email
> ten minutes later, **I want to** say it once, in one voice, and have it arrive
> in the right register, **so I can** stop performing a different version of
> myself for every channel.

**The design principle underneath it.** The product infers the *destination* and
lets destination determine register — which means it never has to ask the user
what they want. **The best AI features read a decision the user has already
made somewhere else, rather than asking them to state it again.** This is a
product idea with no pre-AI equivalent, and it's the one competitors are slowest
to copy because it doesn't look like a model capability.

---

## F7 — AI Commands

> *What it is:* speak an instruction rather than content. "Make this shorter."
> "Bullet that." "Turn this into an email."

**The context.** There's text on the screen already — theirs or someone else's —
and it needs an operation, not a replacement.

**The five whys**

| | Why? | Because… |
| --- | --- | --- |
| **1** | Why speak an instruction instead of the content? | Because sometimes the work isn't producing text, it's transforming text that already exists. |
| **2** | Why do it by voice rather than in a model's own window? | Because the alternative is copy, switch, paste, instruct, copy, switch back, paste. Seven steps to shorten a paragraph. |
| **3** | Why is that round trip decisive? | Because the transformation is worth about ten seconds of value and costs thirty. **Small improvements don't die because someone disagreed they'd help. They die of transaction cost.** |
| **4** | Why does the user want the small improvements at all? | Because quality in written work is a sum of changes too small to call edits. The distance between adequate and good is roughly a hundred five-second decisions. |
| **5** | Why do they want a machine executing them? | Because they can already *see* the improvement they want — what stops them is the mechanics. They're not asking anyone to define "better." They're refusing to pay the execution cost of a change they've already decided on. |

> **Terminal motivation:** to have the quality of their work set by their own
> standards rather than by the friction of applying them.

**Outcome statements**

- Minimize the time to apply a change I have already decided on.
- Minimize the number of applications I must move between to edit a piece of text.
- Minimize the likelihood I ship text I know could be better because fixing it isn't worth the trip.

**The job**

> **When** the text in front of me needs a change I can already describe in a
> sentence, **I want to** say the change where the text already lives, **so I
> can** stop letting the cost of a round trip decide whether my work gets the
> improvement.

**This is J2 escaping its original habitat.** `wispr-jobs.md` J2 — redirecting a
model that's 80% right — makes the point that friction bites hardest on the
*marginal turn*, the one with uncertain payoff. Commands take that same
mechanism and point it at human-directed text. Same economics, and the same
consequence: **the tool doesn't just make each correction faster, it raises how
many corrections a person is willing to make.** That is the expansion path, and
it is why "beyond dictation" is a defensible claim rather than a funding-round
slogan.

---

## F11 — Speak one language, ship another

> *What it is:* the thought arrives in the first language, the output comes out
> in the target language. Capture, cleanup and translation in a single pass.

**The context.** The thought forms in the user's first language. The output has
to be in English. There is no moment at which the thought exists in English
before they make it exist.

**The five whys**

| | Why? | Because… |
| --- | --- | --- |
| **1** | Why speak the first language and get English? | Because that's the order the thought actually arrives in, and translating costs them. |
| **2** | Why does translation cost so much? | Because it happens at composition time, in working memory, concurrently with the thinking. It's a second live task, not a step. |
| **3** | Why does the concurrency matter? | Because working memory is exactly the resource this job is already short of (J11) — the thought is at risk of slipping while you hold it. **Translation taxes the faculty that's already overloaded.** |
| **4** | Why didn't translation tools help? | Because they required the source to be *written* first — you had to complete the very step you were trying to skip. It is the repo's own diagnostic again: the solution demanded as input the thing the user came lacking. |
| **5** | Why does one pass matter beyond convenience? | Because when translation is a separate step, the user is forced to choose between speed and their own language — and mostly chooses to think in English, badly. Collapsing the step lets them think where they think best and still ship where the job requires. |

> **Terminal motivation:** to do their thinking in their strongest language
> without paying for it in the output.

**Outcome statements**

- Minimize the effort to move a thought from the language it arrived in to the language it must ship in.
- Minimize the likelihood the thought degrades on the way across.
- Minimize the number of steps between the thought and the delivered text.

**The job**

> **When** the thought arrives in my first language and the output has to be in
> another, **I want to** say it as it comes and get the target language out in
> one pass, **so I can** think in the language I think fastest in.

---
---

# Family D — Features that buy permission

*Two features whose chains never terminate in the user at all. They terminate in
somebody else's authorisation — and they are where the revenue is.*

## F12 — The free tier, metered in words

> *What it is:* ~2,000 words/week on desktop, ~1,000/week on iPhone. **The
> product is identical. You just run out.**

**The context.** Somebody is deciding whether $15/month is worth it, for a
behaviour they have never had, in a category that has disappointed them before.

**The five whys**

| | Why? | Because… |
| --- | --- | --- |
| **1** | Why metered in words rather than gated by feature? | Because the claim under test — "it produces sendable text" — is only checkable on *their* speech, *their* names, *their* messages. |
| **2** | Why can't a feature-limited trial do that? | Because the thing being tested is quality on their own material. A crippled version tests a different product; they'd learn whether they like a worse thing. |
| **3** | Why do they need to test it rather than trust the claim? | Because this category has forty years of disappointing them. **The anxiety here is prior experience, not price** — and no amount of marketing copy discharges prior experience. |
| **4** | Why does *running out* specifically resolve it? | Because it converts the decision from a prediction into a memory. By the time they hit the wall, they know exactly what they lose. They're not buying a claim; they're buying back something they already had. |
| **5** | Why does the user care which of those they're doing? | Because people will pay $15 a month for a thing that's already part of how they work, and won't for a thing they hope will become that. **The meter exists to let the habit form before the price is asked.** |

> **Terminal motivation:** to buy back a habit rather than buy a promise.

**Outcome statements**

- Minimize the likelihood I pay for something that turns out not to work on my material.
- Minimize the effort to evaluate the product against my real work.
- Minimize the likelihood the version I evaluate is not the version I'd be buying.

**The job**

> **When** I'm deciding whether this is worth a monthly subscription, in a
> category that has disappointed me before, **I want to** use the real product
> on my own work until I know, **so I can** buy something I've already proved to
> myself instead of something I'm hoping about.

**The pricing lesson, stated as a rule.** A feature-gated free tier tests
*whether the user likes a worse product*. A usage-gated free tier tests *whether
the habit forms* — and then charges at the exact moment the habit is real.
**For a habit product, meter the volume, never the capability.** A free tier
that gates features would never have produced 70% twelve-month retention,
because the thing being retained is a reflex, and a reflex can't form around
something you're only allowed to half-use.

---

## F13 — The Teams tier and shared admin

> *What it is:* 3+ seats, one bill, shared administration.

**The context.** A manager has been using it personally for two months. They can
see the difference between their own turnaround and their team's. They now want
to introduce it — and introducing a tool is a different act from using one.

**The five whys**

| | Why? | Because… |
| --- | --- | --- |
| **1** | Why do they need seats and shared admin? | Because they're no longer buying for themselves. They're buying for people they're responsible for. |
| **2** | Why does that change what they need from the product? | Because they now have to justify it, administer it, and be able to reverse it — one bill, control of who has access, removal when someone leaves. |
| **3** | Why does administration outrank features at this moment? | Because the risk they're managing isn't the product's quality. They verified that personally. It's their own exposure for having brought it in. |
| **4** | Why is that exposure the operative concern? | Because a tool introduced by a manager becomes *theirs*. If it leaks something, or the cost scatters across a dozen expense claims, or a departed employee keeps a live seat, it lands on the person who suggested it. |
| **5** | Why take that risk at all? | Because they've already experienced the gain and can't unsee it. **Personal proof is what creates the champion; administration is what lets the champion act without personal exposure.** |

> **Terminal motivation:** to convert a personal discovery into a team decision
> without personally carrying the decision.

**Outcome statements**

- Minimize the effort to grant and revoke access as people join and leave.
- Minimize the likelihood that usage becomes invisible to me once I've introduced it.
- Minimize the likelihood I am personally exposed for a tool I brought in.

**The job**

> **When** I've proved on my own output that this works and I want the people
> I'm responsible for to have it, **I want to** buy, assign and revoke it in one
> place, **so I can** put my name on the decision without carrying it
> personally.

**This is the mechanism behind "essentially zero cold outreach."** Product-led
growth is usually described as if the product spreads on its own. It doesn't.
It spreads through a specific person taking a specific personal risk, and the
Teams tier is the feature that lowers that risk to a level they'll accept. **The
seat count is not a packaging decision. It is the champion's job, priced.**

---

## F14 — SOC 2, SSO and enforced HIPAA

> *What it is:* the Enterprise tier — certifications, single sign-on, enforced
> HIPAA compliance, and guarantees about retention and training.

**The context.** The user's most valuable work is also their most confidential:
client material, patient notes, an unannounced deal. Everything trivial has
already converted, which is precisely what makes the exclusion visible.

**The five whys**

| | Why? | Because… |
| --- | --- | --- |
| **1** | Why do they need retention guarantees? | Because the highest-value uses are the ones covered by an obligation to somebody else — a client, a patient, a contract. |
| **2** | Why does the obligation change the decision? | Because the risk isn't theirs to take. You're permitted to make a personal judgement about your own privacy. You are not permitted to make one about a client's data. |
| **3** | Why does that block adoption rather than merely bound it? | Because it forces them to sort every utterance into "safe to dictate" and "not" — and the sorting happens *before speaking*, which reintroduces the exact pre-composition tax the product removed. |
| **4** | Why is the sorting worse than just excluding the sensitive work? | Because the boundary is unclear. Ambiguity leaves two options: err wide and lose most of the value, or think about it every time and lose the reflex. **Both destroy the habit, and the habit is the product.** |
| **5** | Why must the guarantee be institutional rather than personal? | Because they don't want to be the one who decided. A certification moves the judgement to their organisation and its auditors — which is the only form in which they're able to use it on the work that counts. |

> **Terminal motivation:** to be *allowed* — with the permission coming from
> someone whose job it is to grant it.

**Outcome statements**

- Minimize the likelihood I must sort my work into what I may and may not dictate.
- Minimize the likelihood I am personally the person who authorised a data risk.
- Minimize the likelihood the tool stays confined to my least important work.

**The job**

> **When** the work that matters most is also the work covered by an obligation
> to somebody else, **I want to** have the guarantee come from my organisation
> rather than from my own judgement, **so I can** use this on the things that
> count instead of only on the trivia.

**Note what the Enterprise tier is actually selling.** Not security. *Permission.*
The buyer's problem is not that they doubt the product — they've watched their
whole company adopt it bottom-up. It's that they need the authority to say yes
to be located somewhere other than in their own risk appetite. **Compliance
features are the transfer of a judgement, and they're priced accordingly.**

---
---

# What the fourteen chains reveal

**1. Almost none of them terminate in speed.** Only F8 and F9 touch throughput
at all, and even those bottom out in *frequency* rather than duration. The rest
terminate in reflex, standing, authorship or permission. Speed is the pitch on
the website; it is nearly never the terminal why. This corroborates finding 3 in
`wispr-jobs.md` from the opposite direction — that document reaches it from the
jobs, this one from the features, and they agree.

**2. The terminal motivations cluster into four, and the clusters are the
families above.**

| Cluster | Features | What the user is buying |
| --- | --- | --- |
| **Reflex** | F1, F2, F6, F8, F9, F12 | The right to stop deciding — for the tool to become a default rather than a choice |
| **Standing** | F3, F4, F10 | To be read as the person they are |
| **Authorship** | F5, F7, F11 | To give up execution while keeping judgement |
| **Permission** | F13, F14 | For someone else to hold the risk of saying yes |

**Six of fourteen features exist to protect a habit, and they're the ones with
no visible output.** That's the composition of an AI-native product that
retains: the visible features win the trial, the invisible ones win the year.

**3. The Authorship cluster marks a boundary the product never crosses.** F5
infers the destination but not the intent. F7 executes a change the user
described but doesn't choose one. F11 renders the language but not the argument.
Every one of those chains terminates at level 5 with a version of *"I'll let it
do the work, I won't let it make the call."* **Ask students where that line sits
in their own product, because a feature that crosses it gets rejected by users
who would have loved the same capability positioned one step lower.**

**4. Levels 4 and 5 keep rediscovering the repo's own diagnostic.** Look at F3
(demanded editing time from someone with none), F6 (demanded commitment before
evidence), F10 (demanded written confidence from someone short of it), F11
(demanded a written source from someone who hadn't written anything yet). The
five whys arrive independently at the rule stated in `wispr-jobs.md`:

> **When a solution has existed for decades and nobody hires it, check whether it
> requires as input the thing the user came to you lacking.**

That the two methods converge is the argument for doing both.

**5. Two features serve jobs the thirteen-job portfolio doesn't contain — and
they're the two that carry the revenue.** F12 is a *decision* job (how somebody
becomes a customer) and F13 is a *champion's* job (how somebody becomes a
distribution channel). Neither is a user job; both are buyer jobs. `wispr-jobs.md`
covers thirteen jobs of the person speaking and none of the person paying.

> **That's a real gap, and it's the common one.** Product teams write job
> portfolios for users and pricing decks for buyers, and the two documents never
> meet. Wispr's growth story — 40% month-over-month with essentially zero cold
> outreach — is entirely a story about F12 and F13, which is to say entirely
> about the two jobs a conventional portfolio would have omitted.

---

# Using this in class

Don't work all fourteen. Put the master table up, then take **three chains all
the way down** — one from each of three different clusters, so the contrast in
terminal motivation is visible:

| Feature | Why this one |
| --- | --- |
| **F4 — self-correction** | It's the live demo, so the room has just watched it. Then the chain shows it isn't a trick: it's the precondition for talking your way into a thought you haven't formed yet. |
| **F12 — the word meter** | The pricing chain. Lands the rule — meter the volume, never the capability — and it's the one students can apply on Monday. |
| **F1 — hold-to-talk** | The counter-intuitive one. They chose the *worse* interaction, and the chain explains why that was correct. |

**Then the exercise.** Hand each team one feature of a product they use daily
and twenty minutes to run it to five levels. Two tests of whether they've
understood:

- **Did the chain leave the product?** If level 5 still mentions the feature,
  they stopped at the spec.
- **Do two different features in the room bottom out at the same terminal
  motivation?** They usually do — and when a team spots it, they've found the
  product's actual value proposition, which is almost never the one on its
  homepage.

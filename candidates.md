# Candidate products screened

Nineteen AI-native products, each read through the same three questions, each
reduced to a single takeaway. Wispr Flow was chosen as the spine; the rest are
here to swap in, or to run as 90-second contrast cases.

**Selection criteria that mattered most:** demoable live in under a minute,
accessible to a non-developer audience, and one crisp product decision rather
than a diffuse strategy story.

---

## The shortlist

### Wispr Flow — voice dictation that outputs finished text · **CHOSEN**
Typing was always a tax on thinking; nobody called it a problem because there
was no alternative. The shift is from *"transcribe accurately"* — a 40-year-old
problem, basically solved — to *"turn how people actually talk into what they
meant to write."* The product **is the post-processing layer**; ASR is a
commodity input it buys. It reads which app you're in and formats for the
destination.

> **When the underlying capability commoditizes, the product moves one layer up
> — to intent, context, and destination.**

### Descript — edit video by editing the transcript
Video editing required a specialist and a timeline mental model. AI made
translation between media cheap, so they re-represented video **as text**, and
every familiar text operation became a video operation. Delete a word, delete
the footage.

> **The deepest AI product move is changing the representation of the thing, not
> adding a feature to it.** Best single answer to question 3.

### Granola — meeting notes that finish *your* notes
Competitors solved "capture the meeting" — bots, full transcripts, nobody reads
them. The real job is *notes that sound like me and reflect what I thought
mattered.* Your notes stay primary; AI fills in behind them from audio. No bot
joins the call.

> **The winning move was to build less.** People want leverage, not replacement
> — the work has to still feel like it came from them.

### Google Lens / Circle to Search — point instead of describing
The query stopped needing to be words. From *"describe what you're looking at
well enough to find it"* to *"point at it."* The hard part of visual search was
never retrieval — it was the translation step, and Circle to Search removes the
app switch too.

> **Sometimes the unlock is deleting the translation step between the user's
> world and the query box.** Pairs with Wispr: same insight, different sense.

---

## The rest of the screen

### NotebookLM / Gemini Notebook — the grounded research notebook
Search inverted: you bring the corpus. Three deep builds — grounding as a
**deliberate capability restriction** (decided mid-2022, refuses to answer
outside your sources, worse on every benchmark, and that's the point); the
Studio panel as a systematic search over *"what shape should understanding
take?"*; and craft below the model — the disfluencies in Audio Overviews live in
the audio model, not the LLM transcript.
> **The answer doesn't have to have the shape of the question.**

### Cursor — AI code editor
The bottleneck moved from **writing to reviewing**: you can generate far more
code than you can read. The diff view and checkpoints are the product.
> **The product's job isn't to be right; it's to make being wrong cheap.**
> Developer-centric, and its richest material pulls toward business model.

### Midjourney — image generation
From *"find the image that exists"* to *"converge on the image in my head"* — a
search through a space you can't describe. Variations, seeds, style references,
remix.
> **When output is free but unpredictable, the product is the steering, not the
> generating.**

### Lovable / Replit Agent — non-developers shipping software
From *"how do I specify this to an engineer"* to *"how do I discover what I want
by seeing it."* Specification was never the user's skill. Live preview,
checkpoints, rollback.
> **Removing the cost of building exposed that the real bottleneck was always
> knowing what to build.**

### Khanmigo — the AI tutor
Bloom's 2-sigma: tutoring works and was unaffordable. It is engineered to
**refuse to give the answer** — a Socratic constraint imposed against the
model's grain, and harder to enforce than the capability was.
> **Sometimes the product is a constraint you impose on a capable model.**

### Duolingo — conversational practice
The scarce resource in language learning was never content. It was a patient,
non-judgmental person to be bad in front of. The character is designed to be
forgiving and slightly incompetent — deliberately.
> **The scarce input was social, not informational.**

### Gamma — AI presentations
From *"make me a deck"* to *"give me a structure I can argue with."* Generates
structure first, then content, then design; every layer stays editable.
> **Generate the scaffold, not the artifact.** Meta-relevant for an MBA room.

### Canva Magic Studio — design for people who can't design
AI applied **inside an existing editing surface** — every generation lands as an
editable object, not a flat PNG you accept or regenerate.
> **The unit of AI application matters more than the model.** Why incumbents
> with an editing surface had a real advantage.

### Magic Editor / Generative Fill / Apple Clean Up
**Region-scoped generation** — the model acts on a selection with surrounding
pixels as the prompt. Deletion turned out to be the killer verb, not creation.
> **Constraining where the AI may act is what made it trustworthy enough to ship
> to a billion people.**

### Spotify AI DJ
Recommendation was already solved. What was missing was sequencing and a reason.
The voice commentary **is** the product — same picks, transformed by narration.
> **Explanation is a feature, not metadata.**

### Gmail "Help me write" / Smart Reply
The product decision is **placement**, not capability. A worse model in the
compose window beats a better model one tab away.
> **Distribution and moment-of-use beat capability.**

### Perplexity — search with receipts
Strip the citations and the answer becomes unusable for anything that matters.
> **The verification affordance is often the product; the answer is the
> commodity.**

### Elicit / Consensus — research across papers
From *"summarize this paper"* to *"across these 200 papers, what does the
evidence say?"* — a classic unservable job. The output is a structured
extraction table, not prose.
> **For research, the right output is a table.**

### Amazon Rufus — the useful failure
Conversational commerce became possible, and shoppers mostly didn't want to
talk. Browsing is low-cognition and high-serendipity; conversation is neither.
> **Not every job wants to become a conversation.** Chat is a capability, not a
> UI strategy.

### Zoom AI Companion / Teams recap — the setup for Granola
Same stated job, different real job: the enterprise version optimizes for
*coverage*, Granola for *voice*.
> **Two products can claim the same job statement and be solving different
> jobs.** Run it 60 seconds before Granola.

### Suno — music generation
When production is free, the scarce input becomes selection.
> **Taste becomes the bottleneck.** Cut for being hard to make rigorous in 20
> minutes.

---

## If you swap the spine

The three questions, the run sheet, and the contrast-table format all transfer
unchanged — only the content changes. The three strongest alternatives answer
question 3 differently, which is why any two of them pair well:

| Product | Answer to "what's being built at a deeper level" |
| --- | --- |
| **Wispr Flow** | Move **up a layer** — to intent and context |
| **Descript** | Change the **representation** |
| **Granola** | Build **less** — keep the human artifact primary |

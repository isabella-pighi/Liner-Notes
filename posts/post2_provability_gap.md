# Post 2: You can't prove a song trained an AI, and that's a problem

*Angle: the provability gap. Feeds off sections 7.5 and 7.6 of the paper. Audience: artists, tech and policy readers, the AI-curious.*

---

## Medium version

### A question that sounds simple and isn't

Suppose you write songs for a living. A new music-generation model comes out, and something about what it produces feels close to your work. You suspect your catalogue was in its training data. So you ask the obvious question: can I prove it?

The honest answer, for the models being sued right now, is that you almost certainly cannot. And the reason is not that the law is behind. It is that the thing you want to prove may not be provable at all with the tools we have.

That surprises people, so let me walk through why.

### The old rule stops working

There is an old principle in data work: garbage in, garbage out. If your inputs are bad, your outputs will be too. It has always carried a hidden assumption, which is that you can at least see what went in.

With today's large AI models, you often can't. The training data is enormous, private, and undocumented. The model does not keep a receipt. So the question "was my song in there" turns from a matter of checking records into a genuinely hard technical puzzle.

### What the researchers can actually do

Computer scientists have spent years on a related question: given a trained model, can you tell whether a specific example was in its training set? The technique is called membership inference, and it goes back to work by Shokri and colleagues in 2017. Under favourable conditions, it works.

The trouble is that those favourable conditions do not describe the models we care about. When Duan and colleagues tested membership inference on large language models in 2024, they found it barely beats a coin toss. The reason is almost poetic: a model trained once over a vast ocean of data does not memorise any single drop strongly enough to leave a fingerprint.

There are other angles, and each one fails in an instructive way.

You can sometimes make a model spit out training data word for word. But research shows this only happens for the rare examples that appeared many times over, not the typical song buried once in the pile.

You can detect whether a whole dataset was used, with far more confidence than any single item. Useful if you are a label with a huge catalogue. Useless if you are one songwriter asking about one song.

And the most reliable method needs foresight. You can plant hidden markers in your work beforehand, so their later appearance gives the game away. But that only protects material you booby-trapped in advance, which is no help at all for everything already out on the open web.

### The gap, stated plainly

Put it together and the picture is stark. Unless you have access to the model's inner workings, or you watermarked your work before it was ever scraped, you cannot demonstrate after the fact that a particular song or lyric trained a model.

That is the provability gap. The methods we have do not deliver what a rights-holder would actually need.

### Why this matters beyond music

This is not only a musicians' problem. Every writer, illustrator, and photographer whose work sits online is in the same position. The public debate talks as if proving misuse is mostly a legal fight. A lot of the time, it is a measurement problem first, and the measurement may be impossible.

Which points to the only durable defence. If you cannot prove misuse by inspecting the model, the protection has to be attached to the work before it ever reaches one: machine-readable rights, provenance, consent recorded at the source. That is a governance job, not a detective job.

*This is drawn from a longer paper on music data in the age of AI. The full version, with all the research cited and a diagram of the provability gap, is here: [github.com/isabella-pighi/Liner-Notes](https://github.com/isabella-pighi/Liner-Notes). This work grew out of a talk, "From Data Deluge to Data Strategy: Get the Power of Insights," that I gave with Chiara Santoro at [SXSW 2025](https://schedule.sxsw.com/2025/events/PP153768).*

---

## Substack version

### The provability gap: why "was my work used to train this model?" may be unanswerable

The AI-and-copyright debate is usually framed as a legal question. I want to argue that underneath it sits a technical one that is, on today's models, largely unsolved: even if you had every right to know, you often could not prove your work was in a training set.

Here is the setup. A songwriter suspects a generative model trained on their catalogue. What evidence could they actually produce? Let me go through the available methods and where each one breaks, because the pattern is what matters.

### Membership inference

The direct approach is membership inference: given the model, decide whether one specific example was in its training data. Shokri and colleagues (2017) established that this is feasible against machine-learning models under the right conditions, typically smaller models, or ones that overfit and effectively memorise their training set.

Commercial music and language models are the opposite case: huge, trained roughly once over a near-web-scale corpus. Duan and colleagues (2024) tested membership inference directly on large language models and found performance close to chance. The mechanism is intuitive once stated: a single pass over an enormous dataset does not imprint any individual example strongly enough to detect. The very scale that makes these models powerful is what erases the fingerprint.

### Extraction and memorisation

A second line of work shows models can be induced to regurgitate training data verbatim, from Carlini and colleagues (2021) on language models to Carlini and colleagues (2023) on image diffusion models. That sounds like it should help, but Carlini and colleagues (2022) quantified it: memorisation concentrates on the small number of examples that appear many times in training. The typical work, present once, is not the kind of thing the model reproduces. So extraction proves misuse for duplicated, high-frequency items and stays silent about everything else.

### Dataset inference

Maini and colleagues (2021) proposed dataset inference, resolving ownership at the level of a whole dataset rather than a single record, and extended it to language models in 2024. Statistically this is far stronger, because you aggregate signal across many examples. But it answers a different question: it can help a label with a large catalogue argue that its corpus was used, and it does nothing for an individual asking about one track. The unit of proof is a body of work, not a work.

### Copyright traps and watermarks

The most reliable method requires acting in advance. Meeus and colleagues (2024) show you can plant "copyright traps", unique markers seeded into your text, so that their later appearance betrays training use. Shi and colleagues (2023) built a detector, Min-K% Prob, for whether text was in a model's pre-training data, but it too yields a statistical signal rather than proof.

The catch with traps is structural: they only protect material you marked before it was scraped. A back catalogue already on the open web cannot be retrofitted.

### The gap

Stack these up and a clean conclusion falls out. Absent access to the model's weights, or a watermark inserted before scraping, a single work's presence in a training set cannot be demonstrated after the fact. The detection methods and the rights-holder's evidentiary need do not meet. That is the provability gap.

Note the asymmetry this creates. Defendants in the current suits have argued fair use while effectively conceding large-scale ingestion, because the fight is over permission, not over whether the data was used. The individual creator is in a weaker spot: they may not even be able to establish use in the first place.

### The governance implication

If you cannot prove misuse by inspecting the model, the only durable defence moves upstream: rights, provenance, and consent recorded in the data itself, before it reaches any model. Machine-readable licensing, do-not-train signals, and content provenance standards stop being optional once you accept the detection problem has no reliable after-the-fact solution. They become the response to it.

The honest caveat: this is a moving research area, and a future method, or a court-ordered look inside a model, could shift what is provable. But betting a creative economy on a breakthrough that has not happened is not a strategy. Attaching rights at the source is.

*Full paper, figures, and complete bibliography: [github.com/isabella-pighi/Liner-Notes](https://github.com/isabella-pighi/Liner-Notes). This post expands the AI and provability sections. This work grew out of a talk, "From Data Deluge to Data Strategy: Get the Power of Insights," that I gave with Chiara Santoro at [SXSW 2025](https://schedule.sxsw.com/2025/events/PP153768).*

---

## LinkedIn note

If you're a songwriter and you think an AI was trained on your music, can you prove it?

For the models in the headlines, probably not. It's not a gap in the law, it's a gap in what's technically possible.

New post on the provability gap, from a talk Chiara Santoro and I gave at SXSW 2025.

[Medium] · [Substack] · github.com/isabella-pighi/Liner-Notes

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

### What the lawsuits actually settle

You can watch this play out in the courts right now, and it's telling. The record labels sued the big music generators, Suno and Udio, in 2024. By late 2025 the deals started landing: Universal settled with Udio, Warner settled with both. Sony held out and is still fighting.

But look at what a settlement does. The label gets paid and gets a licensing deal. Nobody ever has to prove in court which songs went into the training set.

The awkward question just gets negotiated around. And that only works if you have a huge catalogue and a legal team, which an individual songwriter does not.

### Why this matters beyond music

This is not only a musicians' problem. Every writer, illustrator, and photographer whose work sits online is in the same position. The public debate talks as if proving misuse is mostly a legal fight. A lot of the time, it is a measurement problem first, and the measurement may be impossible.

Which points to the only durable defence. If you cannot prove misuse by inspecting the model, the protection has to be attached to the work before it ever reaches one: machine-readable rights, provenance, consent recorded at the source. That is a governance job, not a detective job.

*This is drawn from a longer paper on music data in the age of AI. The full version, with all the research cited and a diagram of the provability gap, is here: [github.com/isabella-pighi/Liner-Notes](https://github.com/isabella-pighi/Liner-Notes). This work grew out of a talk, "From Data Deluge to Data Strategy: Get the Power of Insights," that I gave with Chiara Santoro at [SXSW 2025](https://schedule.sxsw.com/2025/events/PP153768).*

---

## Substack version

### The provability gap: why "was my work used to train this?" may be unanswerable

Suppose you write songs for a living. A new music-generation model comes out, and something about what it produces feels close to your work. You suspect your catalogue was in its training data, and you decide to do something about it. So you ask the question any lawyer would ask first: can you prove it?

For the models being sued right now, the honest answer is that you almost certainly cannot. And here's the part that catches people off guard: it isn't because the law is behind. It's because the thing you want to prove may not be provable at all with the tools we have.

The AI-and-copyright fight is usually told as a legal story. I want to make the case that underneath it sits a technical problem that is, on today's models, largely unsolved. So let me walk through the methods a creator could actually reach for, one by one, and show you exactly where each one breaks. The pattern is the whole point.

### The old rule quietly stopped working

There's an old principle in data work: garbage in, garbage out. Bad inputs, bad outputs. It always carried a hidden assumption, which is that you can at least see what went in.

With today's large models, you often can't. The training data is enormous, private, and undocumented, and the model keeps no receipt. So "was my song in there" stops being a question you answer by checking records and becomes a genuinely hard technical puzzle. Everything below is a different attempt to solve that puzzle, and a different way of failing.

### The direct approach, and why scale erases the evidence

The obvious method is called membership inference: given a trained model, decide whether one specific example was in its training set. Shokri and colleagues established in 2017 that you can do this against machine-learning models, but only under favourable conditions, typically smaller models, or ones that overfit and effectively memorise what they were trained on.

Commercial music and language models are the opposite case. They are huge, and they are trained roughly once over a near-web-scale ocean of data. When Duan and colleagues tested membership inference directly on large language models in 2024, they found it barely beats a coin toss.

The reason is almost poetic once you say it out loud: a single pass over a vast dataset never imprints any one example strongly enough to leave a fingerprint. The very scale that makes these models powerful is what rubs out the evidence you'd need.

It gets worse when you look closely at how these attacks are tested. In a 2024 systematisation pointedly titled *Membership Inference Attacks on LLMs are Rushing Nowhere*, Meeus and colleagues showed that most of the recent methods are evaluated by picking members and non-members after the model was released, which quietly lets in a distribution shift between the two groups. The attack then scores well not because it detected training, but because members and non-members differ in some other way, like their date or topic. Strip that artefact out and much of the reported success evaporates.

### Making the model confess, and why it usually won't

There's a second angle. You can sometimes induce a model to spit its training data back out word for word, shown for language models by Carlini and colleagues in 2021 and for image generators in 2023. That sounds like it should settle things.

But Carlini and colleagues quantified the catch in 2022: this memorisation clusters on the handful of examples that appeared many times over in training. The typical work, present once, is simply not the kind of thing the model reproduces. So extraction can prove misuse for duplicated, high-frequency material, and stays completely silent about everything else, which is most of everything.

### Proving the haystack, not the needle

Maini and colleagues took a smarter statistical route in 2021 with what they called dataset inference, extended to language models in 2024. Instead of asking about one record, you aggregate signal across many, which is far more reliable.

The problem is it answers a different question than the one our songwriter is asking. It can help a label with a huge catalogue argue that its corpus was used. It does nothing for one person asking about one track. The unit of proof is a body of work, not a work.

Shi and colleagues built a related detector in 2023, Min-K% Prob, for whether a passage was in a model's pre-training data, but it too returns a statistical hint rather than proof.

### The one method that works, if you had a time machine

The most reliable technique needs foresight. Meeus and colleagues showed in 2024 that you can plant "copyright traps", unique markers seeded into your text, so that their later appearance in a model gives the game away.

The catch is structural, not fixable. Traps only protect material you marked before it was scraped. A back catalogue already sitting on the open web can't be retrofitted with a booby trap after the fact. For almost every artist alive, that's the entire problem.

### The gap, stated plainly

Stack these up and a clean, uncomfortable conclusion falls out. Absent access to the model's inner weights, or a watermark you inserted before your work was ever scraped, you cannot demonstrate after the fact that a specific song or lyric trained a model. The detection methods and the rights-holder's evidentiary need simply do not meet.

There's now a formal version of this argument, and it's worth knowing about. Zhang, Das, Kamath and Tramèr (2024), in a paper titled almost exactly like this problem, *Membership Inference Attacks Cannot Prove that a Model Was Trained On Your Data*, show the failure is structural, not just practical. To make a convincing training-data proof you'd need to show your attack almost never fires on data the model didn't train on. Establishing that means sampling from the world where your work was absent, which means knowing the exact training set or retraining a foundation model from scratch.

Neither is possible. The proof a court would want cannot be constructed from the outside.

That is the provability gap, and it creates a strange asymmetry. The big defendants in the current suits, the ones facing the RIAA's June 2024 cases against Suno and Udio, have mostly argued fair use while effectively conceding they ingested data at scale. Their fight is over permission, not over whether the data was used. The individual creator is in a weaker spot than that: they may not even be able to establish use in the first place.

And the stakes are not hypothetical. This is the same period in which a fake, AI-cloned Drake and Weeknd track, "Heart on My Sleeve", pulled millions of plays before Universal got it pulled in 2023, and Deezer began reporting that AI-generated tracks had climbed from about 28% of its uploads in September 2025 to roughly 44% by April 2026. The volume of synthetic work with no honest record of what it is, or what it learned from, is not slowing down.

### What the courts are quietly deciding for you

Here's where the provability gap meets the real world, and it's worth watching closely.

The big test cases came from the record labels, not individuals. In June 2024 the RIAA sued the two leading music generators, Suno and Udio, for mass copyright infringement. Then, through late 2025, the majors started peeling off.

Universal settled with Udio in October 2025 and announced a licensed AI music service for 2026. Warner settled with both Udio and Suno in November 2025, signing licensing deals in each case.

Notice what a settlement does, and does not, do. It resolves permission commercially: the label gets paid and gets a deal, the generator gets to keep operating. It never establishes in court whether or how any specific recording was used.

The provability question isn't answered, it's stepped around. And the licensing deals quietly assume large-scale use rather than proving it, which is the labels' whole leverage.

That leaves one holdout. Sony Music declined to settle and, as the last major label still in court, is pushing toward a ruling. A summary-judgment fight in the Massachusetts Suno case was heading for a hearing in 2026, and its outcome on the core fair-use question could set the precedent everyone else negotiated around.

So the individual creator is caught in a double bind. The labels have the catalogues and the lawyers to force a settlement without ever proving use. You have neither, and the one method that might have proved your case, inspecting the model, does not work.

Whichever way the Sony ruling lands, it decides the fair-use question, not the can-you-even-tell question. That one stays open.

### Why this matters well beyond music

This isn't only a musicians' problem. Every writer, illustrator, and photographer whose work sits online is standing in the same spot. The public conversation treats proving misuse as mainly a courtroom fight. A lot of the time it's a measurement problem first, and the measurement may be impossible.

Which points at the only durable defence. If you can't prove misuse by inspecting the model, the protection has to be attached to the work before it ever reaches one: machine-readable rights, provenance, and consent recorded at the source. Do-not-train signals and content-provenance standards stop being optional the moment you accept the detection problem has no reliable after-the-fact fix. They become the answer to it.

The honest caveat is that this is a moving research area, and a future method, or a court forcing a look inside a model, could shift what's provable. But betting a creative economy on a breakthrough that hasn't happened is not a plan. Attaching rights at the source is.

*Full paper, figures, and complete bibliography: [github.com/isabella-pighi/Liner-Notes](https://github.com/isabella-pighi/Liner-Notes). This post expands the AI and provability sections. This work grew out of a talk, "From Data Deluge to Data Strategy: Get the Power of Insights," that I gave with Chiara Santoro at [SXSW 2025](https://schedule.sxsw.com/2025/events/PP153768).*

---

## LinkedIn note

If you're a songwriter and you think an AI was trained on your music, can you prove it?

For the models in the headlines, probably not. It's not a gap in the law, it's a gap in what's technically possible.

New post on the provability gap, from a talk Chiara Santoro and I gave at SXSW 2025.

[Medium] · [Substack] · github.com/isabella-pighi/Liner-Notes

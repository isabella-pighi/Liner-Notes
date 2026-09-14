# Post 7: If you can't prove it afterwards, attach it beforehand

*Angle: consent, opt-outs, provenance and watermarking as the constructive answer to the provability gap. Feeds off section 6 of Part 2. Audience: artists, rights-holders, policy and tech readers.*

---

## Medium version

### The detective problem, and why it can't be solved

An earlier post in this series ended somewhere unsatisfying. If you're a songwriter and you suspect an AI model was trained on your music, you probably cannot prove it, and not because the law is weak: the technical methods for looking inside a model and finding your song simply don't work reliably at the scale these models operate at, which is a research finding rather than a legal gap.

I left it there deliberately, because the answer isn't a better detective.

If you can't demonstrate misuse by inspecting the model afterwards, then the protection has to be attached to the work *before* it ever reaches one. That's a governance job. And it's the top layer of what a music data strategy actually needs.

![Nothing you do after training answers the question. A machine-readable reservation attached beforehand turns it into one with a record behind it.](figures/fig_attach_before.png)

*Nothing you do after training answers the question. A machine-readable reservation attached beforehand turns it into one with a record behind it.*

### Reserving your rights, in a way a machine can read

Start with the legal piece, which is further along than most people realise.

There's a patchwork of rules worldwide about text-and-data mining, the legal category that covers hoovering up content to train models. Flynn and colleagues mapped it in 2022, and "patchwork" is the honest description. In Europe there's a mechanism that matters more: a copyright opt-out that lets you reserve your rights against having your work mined. Senftleben's 2025 analysis sets out how the EU AI Act works alongside it to create a machine-readable "reserve your rights" regime that general-purpose AI providers are obliged to respect.

Note the phrase "machine-readable".

A statement on your website saying please don't train on my music is not a reservation of rights in any sense a crawler will notice. It has to be expressed in a form software can check automatically, or it does nothing at all.

And the ethical case underneath this is documented rather than assumed. Jiang and colleagues recorded the actual harm to creators from having their work used in training without permission or payment, and Lucchi examined the copyright exposure of models trained on protected work. These aren't hypotheticals anyone needs to argue into existence.

### Consent needs plumbing, not good intentions

Here's the thing that makes consent real: infrastructure that a machine can query.

A research prototype called DECORAIT points at what music needs. It's a decentralised registry where a creator records their consent, or refusal, and their ownership, and it ties that record to content provenance and fingerprinting so a model builder can actually check it. Its successor project, Content ARCs, extends the idea to connect provenance with licensing and payment, which is the part that turns a refusal into a transaction, for anyone who would rather do a deal than simply say no.

Underneath that sits provenance. The Coalition for Content Provenance and Authenticity, C2PA, provides an open technical standard letting publishers, creators and consumers establish the origin and edits of a piece of digital content. The standard is called Content Credentials, and C2PA's own analogy for it is a nutrition label: a record of the content's history that anyone can inspect, at any time.

One caveat worth stating plainly, because it gets glossed over in enthusiastic write-ups. Read that analogy carefully: a nutrition label tells you what went into something, not whether it is good for you. Content Credentials certify a piece of content's *history*, where it came from and what was done to it, and not whether the content is true.

For audio specifically there's watermarking. AudioSeal is the first audio watermarking technique built for localised detection of AI-generated speech, and it can detect the mark right down to the sample level. Worth being precise here: it was designed for speech and voice cloning, not for music, so treating it as a ready-made solution for recordings is an extrapolation. What it demonstrates is that the approach works, with the mark riding in the signal itself rather than in metadata that can simply be stripped.

And provenance labels do change behaviour. Feng and colleagues found that provenance indicators shift what users trust and how accurately they judge what they're looking at, which matters because a standard nobody responds to is a standard that isn't working.

### The market and the regulator arriving together

Two developments are converging from opposite directions, which is unusual enough to be worth noticing.

On the market side, a non-profit called Fairly Trained certifies AI models that train only on licensed, consented, public-domain or owned data. It pointedly withholds its badge from models relying on a fair-use defence. It launched with nine already-certified companies spanning image, music and singing-voice generation, and named Universal Music Group among the organisations backing it.

On the regulatory side, the EU AI Act's opt-out obligation on general-purpose AI providers is set to be backed by a central rights-reservation registry run by the EUIPO. In effect: a legally enforced do-not-train registry.

Voluntary good manners and legal requirement are ending up in the same place, which is a reasonable signal about where this settles.

### What to actually do

Make consent and provenance machine-readable, and attach them at the source.

Reserve your rights in a registry rather than in a sentence on a web page. Bind provenance credentials and watermarks to recordings when you make them, not when a dispute starts. Prefer models trained on consented data, and where you can, models certified as such.

None of this gives you the thing the earlier post said you can't have. You still won't be able to open up a model and find your song in it. What it gives you is a record that existed before the model did, which is a different and more tractable kind of evidence.

*This is drawn from the second part of a longer paper on music data strategy. The full version, with every standard and study cited, is here: [github.com/isabella-pighi/Liner-Notes](https://github.com/isabella-pighi/Liner-Notes). This work grew out of a talk, "From Data Deluge to Data Strategy: Get the Power of Insights," that I gave with Chiara Santoro at [SXSW 2025](https://schedule.sxsw.com/2025/events/PP153768).*

---

## Substack version

### Governing what the AI learns from

*The provability gap says you cannot prove after the fact that your work trained a model. So the protection has to attach before training, in a form software can check. Here is the machinery that exists, what it genuinely does, and where it is still a prototype.*

There's a post earlier in this series that ends on a deliberately unresolved note: the methods for determining whether a specific work was in a model's training data do not reliably work at frontier scale. Membership inference degrades, extraction attacks recover only heavily memorised material, dataset-level inference needs assumptions you rarely have.

I want to pick that up from the other side.

"We cannot prove it afterwards" has a constructive consequence rather than a defeatist one.

If misuse cannot be demonstrated by inspecting the model, then the enforceable artefact has to be created *before* training. Not evidence recovered from the model, but a record that predates it: a machine-checkable statement of what was permitted, attached to the work, timestamped and signed.

![Nothing you do after training answers the question. A machine-readable reservation attached beforehand turns it into one with a record behind it.](figures/fig_attach_before.png)

*Nothing you do after training answers the question. A machine-readable reservation attached beforehand turns it into one with a record behind it.*

That is a governance problem with real infrastructure behind it, some of it law, some of it standards, some of it still research.

### The legal layer: reserving rights that software can see

Text and data mining is the legal category under which training-data collection sits, and the global rules are genuinely fragmented. Flynn and colleagues mapped that patchwork in 2022, and the mapping itself is the finding: there is no single regime to comply with.

The European mechanism is the one with teeth for rights-holders. Senftleben's 2025 analysis examines how the EU AI Act operates alongside the EU copyright opt-out to produce a machine-readable rights-reservation regime binding on general-purpose AI providers. The operative word throughout is machine-readable, and it deserves emphasis because it is where most artists' current practice fails.

A human-readable notice does not reserve anything in practice. A line in your terms, a sentence in a press release, a note on an artist page: a crawler sees none of it as a reservation, and the reservation has to be encoded where automated systems actually look, in a form they parse, or the legal right you technically hold never once gets exercised in the place it matters.

Two papers establish that consent is genuinely owed here rather than merely nice to have. Jiang and colleagues documented the harms reported by creators whose work was used in training without permission or compensation, which moves the discussion off speculation and onto recorded experience, and Lucchi analysed the copyright exposure of models trained on protected works, which is the mirror-image risk sitting on the model builder's side of the same transaction.

### The infrastructure layer: registries, provenance, watermarks

Consent without checkable infrastructure is an aspiration.

Three components are converging into something usable.

**Registries.** DECORAIT is the prototype closest to what music needs: a decentralised opt-in and opt-out registry recording a creator's consent and ownership, made machine-checkable by binding it to content provenance and fingerprinting. Its 2025 successor, Content ARCs, extends the architecture to bind provenance to licensing and payment flows, which sketches the licensing-marketplace layer that a pure refusal mechanism lacks. Both are research work, and I want to be careful not to present a prototype as deployed infrastructure: this is the direction, not a system you can adopt on Monday.

**Provenance.** C2PA Content Credentials is the foundation the registry work builds on. C2PA describes it as an open technical standard through which publishers, creators and consumers can establish the origin and edits of digital content, and the analogy the coalition itself reaches for is a nutrition label: a history of the item that anybody can read, whenever they like.

The caveat is essential and routinely dropped. The nutrition-label analogy is more precise than it first appears, because a nutrition label reports composition rather than merit. Content Credentials record a content item's origin and the edits made to it, not its truthfulness, and they cannot tell you that the content is accurate or that whoever attached the record had any right to the underlying work. Provenance is a chain of custody rather than a truth oracle, and treating it as the latter will eventually embarrass somebody.

**Watermarking.** Manifest-based provenance has an obvious weakness: strip the metadata and the claim goes with it. Signal-based watermarking addresses that from the other direction. AudioSeal is the first audio watermarking technique designed for localised detection of AI-generated speech, with detection down to the sample level, and the mark lives in the audio rather than in strippable metadata.

That caveat matters for music specifically.

AudioSeal targets speech and voice cloning, so its application to recorded music is an extrapolation rather than a demonstrated result, and anyone citing it as proof that music can be watermarked at scale is running ahead of the evidence available. The two approaches are complements rather than competitors, which is how they should be deployed.

Does any of this change behaviour?

Feng and colleagues found that provenance indicators do shift users' trust and their accuracy judgments, which is the empirical grounding for bothering with labels at all, since a credential nobody reacts to would be expensive theatre with a cryptographic signature on it.

### Market and regulator converging

Two developments are arriving at the same destination from opposite directions.

Fairly Trained is a non-profit certifying generative models that train exclusively on licensed, consented, public-domain or owned data. Its position on fair use is the interesting part: it withholds certification from models that rely on a fair-use defence, rather than treating that as a legitimate basis. It launched with nine generative AI companies already certified, spanning image, music and singing-voice generation, and listed Universal Music Group among its supporters alongside publishing and rights bodies, which tells you where the music industry positioned itself early.

On the regulatory side, the EU AI Act's opt-out duty on general-purpose AI providers is set to be backed by a central rights-reservation registry administered by the EUIPO. That is, functionally, a legally enforced do-not-train registry with an institution behind it.

When a voluntary certification scheme and a statutory registry converge on the same mechanism, the mechanism is probably where this settles, which makes it worth building for now rather than after the deadline.

### The move, and its honest limits

Make consent and provenance machine-readable and attach them at source: reserve your rights in a registry, bind provenance credentials and watermarks to recordings at creation, and prefer, and where possible require, models certified as trained on consented data.

The limits deserve stating. Registries only bind those who check them, and a model builder operating outside the EU with no certification ambitions has thin incentive to look. Watermarks can be attacked, and the robustness literature is an arms race rather than a solved problem. Provenance credentials require adoption across a whole toolchain to be useful, and a single link that strips them breaks the chain. None of these is a reason not to do it; all of them are reasons not to promise artists that it closes the gap.

What it does is change the question from one that cannot be answered to one that can. Not "can you prove my song is in that model", which stays hard. Instead: "was there a machine-readable reservation attached to this work at the time of training, and did the provider respect it?" That is a question with a record behind it, and records are what disputes actually run on.

*Full paper, figures, and complete bibliography: [github.com/isabella-pighi/Liner-Notes](https://github.com/isabella-pighi/Liner-Notes). This post expands the consent-and-provenance section of Part 2, and is the constructive counterpart to the earlier post on the provability gap. This work grew out of a talk, "From Data Deluge to Data Strategy: Get the Power of Insights," that I gave with Chiara Santoro at [SXSW 2025](https://schedule.sxsw.com/2025/events/PP153768).*

---

## LinkedIn note

If you can't prove afterwards that a model trained on your music, and mostly you can't, then the protection has to be attached before training.

That means machine-readable consent. A sentence on your website reserves nothing: a crawler doesn't read it.

New post on the registries, provenance credentials and watermarks being built for exactly this, plus the EU registry giving it legal teeth, from a talk Chiara Santoro and I gave at SXSW 2025.

[Medium] · [Substack] · github.com/isabella-pighi/Liner-Notes

# Post 3: Garbage in, garbage out: how music data fools the people who trust it

*Angle: self-fulfilling prophecy and the limitations taxonomy. Feeds off sections 5 and 6 of the paper. Audience: data-curious general readers and industry.*

---

## Medium version

### The chart doesn't just measure the hit. It helps make it.

We treat charts and streaming numbers as a mirror. They tell us what is popular, the way a thermometer tells us the temperature. Neutral, external, just reading off reality.

They are not a mirror. They are closer to a feedback loop, and once you see it you cannot unsee it.

Here is the loop. A song does slightly well, so the recommendation system shows it to more people. Because more people see it, it does better, so the system shows it to even more.

The number that was supposed to measure popularity is now helping create it. The chart is writing the story it claims to be reporting.

### Why this is more than a nuisance

You might think, fine, the popular gets more popular, that has always been true. But the research shows something sharper and stranger.

Chaney and colleagues (2018) gave the effect a name, algorithmic confounding, and showed what it does. When a recommender learns from data that its own past recommendations created, everyone's taste drifts closer together, and, remarkably, the system gets worse at the job it was built to do. The loop is not just unfair to smaller artists. It is self-defeating for the platform too.

Mansoury and colleagues (2020) watched the mechanism run: feedback loops amplify popularity bias and steadily shrink the range of things anyone ever gets shown. The window narrows, quietly, over time.

### The honest complication

I want to be careful here, because the story is not one-sided, and pretending it is would be its own kind of garbage out.

Some studies point the other way. Datta and colleagues (2018) found that moving to streaming actually widened what individual listeners explored, compared with owning music. And a large Spotify study by Anderson and colleagues (2020) found that algorithmic listening increased how much people consumed but was linked to less variety in what they heard.

So the effect is real and measurable, but it is a tension, not a verdict. The same systems that homogenise can also expose you to things you would never have found alone. Anyone who tells you it is simple is selling something.

### Four ways the numbers mislead

Once you accept that the data is not a clean mirror, it helps to know the specific ways it distorts. There are four families.

Fragmentation is the patchiness of the signal. Not every platform reports every artist, VPNs scramble the geography, offline listening is mostly invisible, and even logged behaviour is thin. A skip gets recorded; the reason for it does not.

Bias is about interpretation. Vanity numbers like followers and likes stand in for engagement they do not measure, correlation gets read as causation, and the crowd generating the data is not the crowd you care about. TikTok's users skew young and female in ways that do not represent the audience for plenty of genres.

Automation is the feedback loop above: systems that cannot tell passive listening from active, that favour the mainstream, and that throw off spikes having nothing to do with quality.

Lack of standards is the missing shared vocabulary. A "stream" is not the same event on Spotify as on Apple Music, data sits siloed by platform, and every number is open to gaming, bots, and coordinated campaigns.

### And now people are faking the inputs on purpose

The feedback loop was an accidental distortion. The newest problem is deliberate.

In 2024 a musician was charged in the United States with using AI to generate thousands of fake songs and armies of bots to stream them, siphoning off around ten million dollars in royalties. When both the content and the listening can be manufactured at scale, the numbers are not just noisy. They are corruptible by anyone with a reason to corrupt them.

### The courts are starting to force the issue

There's a legal angle worth adding, because it could change what feeds the machine in the first place. When AI generators train on unlicensed music, that's garbage in on a massive scale, and, as I've argued elsewhere, nobody can reliably prove which songs went in afterwards.

The labels took this to court. They sued the big generators, Suno and Udio, in 2024. By late 2025 the deals began: Universal settled with Udio, Warner settled with both, and Sony is still fighting.

The interesting part for data quality is what a licensing deal does. It turns an untracked scrape into a documented, permissioned input. If that becomes the norm, keeping proper records of what a model learned from stops being optional. If the courts instead wave it through as fair use, the reason to document anything largely disappears.

### The takeaway

Charts and streaming numbers are useful. They are also produced by systems with their own incentives, their own blind spots, and now their own attackers. Read them as a mirror and they will fool you. Read them as one noisy signal among many, made by machinery you cannot fully see, and you will make better decisions.

*This is part of a longer paper on how the music industry measures itself and where those measurements break. The full version, with sources and figures, is here: [github.com/isabella-pighi/Liner-Notes](https://github.com/isabella-pighi/Liner-Notes). This work grew out of a talk, "From Data Deluge to Data Strategy: Get the Power of Insights," that I gave with Chiara Santoro at [SXSW 2025](https://schedule.sxsw.com/2025/events/PP153768).*

---

## Substack version

### The self-fulfilling chart: how music data helps make the thing it claims to measure

We treat charts and streaming numbers as a mirror. They tell us what's popular the way a thermometer tells us the temperature: neutral, external, just reading off reality.

They're not a mirror. They're closer to a feedback loop, and I want to take that apart carefully, because the failure mode it hides is subtle, well-studied, and getting worse.

Here's the loop in one breath. A song does slightly well, so the recommender shows it to more people, so it does better, so the recommender shows it to even more. The number that was meant to measure popularity is now helping create it. The chart is writing the story it claims to be reporting.

### The loop has a name, and it's worse than unfair

Recommendation systems learn from user behaviour. But that behaviour was itself shaped by earlier recommendations, so the system ends up learning from data it partly generated. That closed circle between what gets shown and what gets measured as popular is the whole problem.

Chaney, Stewart and Engelhardt named it in 2018: algorithmic confounding. They showed two consequences, and the second is the one that should make platforms nervous. First, homogenisation: everyone's behaviour drifts closer together as the loop tightens.

Second, and far less obvious, degraded utility: a recommender trained on its own confounded output gets worse at the job it was built for. The loop isn't just unfair to smaller artists. It's self-defeating for the platform too.

Mansoury and colleagues watched the mechanism run in 2020, and found feedback loops amplify popularity bias and steadily shrink the range of things anyone ever gets shown. The window narrows, quietly, over time.

If you want the full map of these biases and the fixes people have proposed, the survey by Chen and colleagues (2023) is the standard reference, and its real contribution is turning a vague fairness worry into a defined engineering problem you can actually work on.

### Music saw this first

Here's a detail I like, because it flips the usual order. The structural outcome of all this, a few superstars and an enormous tail of everyone else, was measured in music before it was theorised for recommenders generally.

Celma and Cano traced in 2008 how popularity concentrates inside the recommendation network itself, and Celma's *Music Recommendation and Discovery* (2010) is still the standard treatment of the long-tail problem. The thing the whole field now worries about showed up in the streaming data early.

### The honest complication

I want to be careful here, because the story isn't one-sided, and pretending it were would be its own kind of garbage out.

Some solid studies point the other way. Datta, Knox and Bronnenberg found in 2018 that moving to streaming actually widened what individual listeners explored, compared with owning music. And the large Spotify study by Anderson and colleagues in 2020, which is really the empirical heart of this argument, compared algorithmic with self-directed listening and found the algorithm increased how much people consumed but was linked to less variety in what they heard.

So the synthesis is a tension, not a verdict. The homogenising effect is real and measurable, and it coexists with genuine discovery benefits. The same systems that flatten taste can also hand you something you'd never have found alone. Anyone who tells you it's simple is selling something.

### Four ways the numbers mislead

Once you accept the data isn't a clean mirror, it helps to name the specific ways it distorts. Naming them turns "data quality" from a vague unease into a checklist. There are four families.

Fragmentation is the state of the signal. Not every platform reports every artist, VPNs scramble the geography, offline listening is mostly invisible, and even logged behaviour is thin: a skip gets recorded, the reason for it doesn't.

Bias is about interpretation. Vanity numbers like followers and likes stand in for engagement they don't measure, correlation gets read as causation, and the crowd generating the data isn't the crowd you care about. TikTok's users skew young and female in ways that don't represent the audience for plenty of genres.

Automation and algorithmic influence is the feedback loop above, plus systems that can't tell passive listening from active, that favour the mainstream, and that throw off spikes with nothing to do with quality.

Lack of standards is the missing shared vocabulary. A "stream" isn't the same event on Spotify as on Apple Music, data sits siloed by platform, measurement windows are short, and every number is open to playlist gaming, bots, and coordinated campaigns.

These aren't independent problems. They're better held as a set of demands that any fair way of normalising music data would have to satisfy at once, which is exactly why nobody has managed it: every normalisation effort so far has been local and arbitrary, with proprietary indices collapsing a many-sided performance into one debatable score.

### And now people are faking the inputs on purpose

Everything above is accidental distortion, a byproduct of how the machinery works. The newest problem is deliberate.

In 2024 a musician was charged in the United States with using AI-generated tracks and armies of bots to stream them, siphoning off around ten million dollars in royalties. He pleaded guilty in 2026. When both the content and the listening can be manufactured at scale, the numbers aren't just noisy. They're corruptible by anyone with a reason to corrupt them, and any model built on raw counts inherits that attack surface whether its authors realise it or not.

### The courts are starting to force the issue

There's a legal front to all this, and it matters because it could change what goes into the machine in the first place.

When AI generators train on unlicensed recordings, that's garbage in at industrial scale: the model absorbs work it had no right to, and, as I've written elsewhere, nobody can reliably prove after the fact which specific songs went in. The record labels went at this directly. In June 2024 the RIAA sued the two leading music generators, Suno and Udio, for mass infringement.

By late 2025 the majors began settling. Universal settled with Udio in October 2025 and lined up a licensed AI music service for 2026, while staying in court against Suno. Warner settled with both Udio and Suno in November 2025, with licensing deals attached. Sony held out and, as the last major still litigating, is pushing toward a ruling, with a summary-judgment fight in the Massachusetts Suno case expected to test the fair-use question in 2026.

Here's why a data person should care. A settlement with a licensing deal turns an untracked scrape into a documented, permissioned input. That's the difference between garbage in and clean in.

If licensing becomes the norm, provenance and consent metadata stop being optional and become the price of doing business, which is exactly the fix the rest of this argument points to. If instead a court blesses training on unlicensed data as fair use, the incentive to document anything largely evaporates. Either way, the quality of what future models learn from is being decided in these rooms right now.

### Why this is actionable, not just cautionary

The practical upshot is a stance toward the numbers. Treat streaming metrics as one noisy, self-referential, manipulable signal, produced by systems with their own incentives and their own blind spots, rather than as ground truth. Read them as a mirror and they'll fool you. Read them as one signal among many, made by machinery you can't fully see, and you'll make better calls.

That reframing is the bridge to strategy. It's exactly why the sequel to this work argues for causal methods and owned, first-party data instead of a dashboard of platform counts.

*Full paper, figures, and complete bibliography: [github.com/isabella-pighi/Liner-Notes](https://github.com/isabella-pighi/Liner-Notes). This post draws on the feedback-loop and limitations sections. This work grew out of a talk, "From Data Deluge to Data Strategy: Get the Power of Insights," that I gave with Chiara Santoro at [SXSW 2025](https://schedule.sxsw.com/2025/events/PP153768).*

---

## LinkedIn note

We treat streaming charts like a thermometer. They're actually a feedback loop.

A song does well, so the algorithm pushes it, so it does better, so the algorithm pushes it more. The number meant to measure popularity is helping create it. Researchers call it algorithmic confounding.

New post on how music data fools the people who trust it, from our SXSW 2025 talk.

[Medium] · [Substack] · github.com/isabella-pighi/Liner-Notes

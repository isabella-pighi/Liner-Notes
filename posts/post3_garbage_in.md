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

### The takeaway

Charts and streaming numbers are useful. They are also produced by systems with their own incentives, their own blind spots, and now their own attackers. Read them as a mirror and they will fool you. Read them as one noisy signal among many, made by machinery you cannot fully see, and you will make better decisions.

*This is part of a longer paper on how the music industry measures itself and where those measurements break. The full version, with sources and figures, is here: [github.com/isabella-pighi/Liner-Notes](https://github.com/isabella-pighi/Liner-Notes). This work grew out of a talk, "From Data Deluge to Data Strategy: Get the Power of Insights," that I gave with Chiara Santoro at [SXSW 2025](https://schedule.sxsw.com/2025/events/PP153768).*

---

## Substack version

### The self-fulfilling chart: algorithmic confounding and the limits of music data

The premise most people carry, often without noticing, is that a chart or a streaming figure is a measurement: an external reading of an independent reality. I want to dismantle that premise carefully, because the failure mode it hides is subtle and well-studied.

### The loop

Recommendation systems are trained on user behaviour. But that behaviour is itself shaped by earlier recommendations. So the system learns from data it partly generated, which creates a closed loop between what gets shown and what gets measured as popular.

Chaney, Stewart and Engelhardt (2018) named this algorithmic confounding and demonstrated two consequences. First, homogenisation: user behaviour converges as the loop tightens. Second, and less obvious, degraded utility: a recommender trained on confounded data performs worse at its actual task. The loop is self-defeating, not merely inequitable.

Mansoury and colleagues (2020) provided empirical support in recommendation settings, showing feedback loops amplify popularity bias and reduce the diversity of what is surfaced over time. For a full map of the biases and the proposed mitigations, the survey by Chen and colleagues (2023) is the standard reference, and it reframes this from a vague fairness worry into a defined engineering problem.

### The long tail, measured in music first

The structural outcome, a few superstars and a vast tail, was quantified in music before it was theorised generally. Celma and Cano (2008) traced how popularity concentrates in the recommendation network, and Celma's *Music Recommendation and Discovery* (2010) remains the standard treatment of the long-tail problem.

### The counter-evidence, stated fairly

Grounding this honestly means reporting the findings that cut against it. Datta, Knox and Bronnenberg (2018) found that the shift to streaming widened individual-level exploration relative to ownership. And the large Spotify study by Anderson and colleagues (2020), the empirical heart of this argument, compared algorithmic with self-directed listening and found the algorithm increased consumption but was associated with lower diversity.

The synthesis: the homogenising effect is real and measurable, but it coexists with genuine discovery benefits. It is a tension, not a settled verdict. A responsible reading holds both.

### The four-family taxonomy of limitations

Beyond the feedback loop, music analytics faces four families of problems. Naming them turns "data quality" from a vague unease into a checklist.

Fragmentation is the state of the signal: incomplete platform coverage, VPN-masked geography, invisible offline listening, and thin logs (a skip is recorded, its cause is not).

Bias is interpretive: cultural and regional nuance is lost, correlation is read as causation, vanity metrics proxy for engagement, and the data-generating population is unrepresentative of the target audience.

Automation and algorithmic influence is the feedback-loop family above, plus the inability to distinguish passive from active listening, mainstream favouritism, and seasonal artefacts.

Lack of standards is the absence of shared definitions: a stream differs across services, data is siloed, measurement windows are short, and every metric is manipulable through playlist gaming, bots, and coordinated campaigns.

These are not independent; they are better held as a set of demands that any fair normalisation must satisfy. The paper's diagnosis is that every normalisation effort so far has been local and arbitrary, with proprietary indices collapsing a many-sided performance into one debatable score.

### Adversarial data: the newest failure mode

The feedback loop degrades data as a byproduct. The current frontier is deliberate corruption. In 2024, a musician was charged in the US with using AI-generated tracks and bot farms to fraudulently harvest roughly ten million dollars in streaming royalties.

This matters analytically: when both the content and the consumption signal can be synthesised at scale, raw counts are not merely noisy, they are actively corruptible. Any model built on them inherits an adversarial attack surface.

### Why this is actionable, not just cautionary

The practical upshot is a stance toward the numbers. Treat streaming metrics as one noisy, endogenous, manipulable signal, produced by systems with their own incentives and blind spots, rather than as ground truth. That reframing is the bridge to strategy: it is why the sequel to this work argues for causal methods and owned first-party data rather than dashboards of platform counts.

*Full paper, figures, and complete bibliography: [github.com/isabella-pighi/Liner-Notes](https://github.com/isabella-pighi/Liner-Notes). This post draws on the feedback-loop and limitations sections. This work grew out of a talk, "From Data Deluge to Data Strategy: Get the Power of Insights," that I gave with Chiara Santoro at [SXSW 2025](https://schedule.sxsw.com/2025/events/PP153768).*

---

## LinkedIn note

We treat streaming charts like a thermometer. They're actually a feedback loop.

A song does well, so the algorithm pushes it, so it does better, so the algorithm pushes it more. The number meant to measure popularity is helping create it. Researchers call it algorithmic confounding.

New post on how music data fools the people who trust it, from our SXSW 2025 talk.

[Medium] · [Substack] · github.com/isabella-pighi/Liner-Notes

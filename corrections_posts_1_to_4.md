# Corrections to published posts 1 to 4

Six edits across three posts, found by a claim-by-claim check of every date, figure and named source against the original material. **Post 4 needs no changes.**

Severity: **Correct** means the published text is factually wrong. **Minor** means it is imprecise, unsourceable, or simply dated.

| # | Post | Version | Severity | Issue |
|---|---|---|---|---|
| 1 | Post 1 | Substack | Minor | Superfan statistic used the wrong denominator, and a Goldman forecast I could not source |
| 2 | Post 2 | Medium | Correct | Carlini et al. (2022) said the opposite of what the post reports |
| 3 | Post 2 | Substack | Correct | Carlini et al. (2022) said the opposite of what the post reports |
| 4 | Post 2 | Substack | Minor | "Millions of plays" unverified, and the Deezer share is now out of date |
| 5 | Post 3 | Medium | Correct | Royalty figure roughly 25% too high |
| 6 | Post 3 | Substack | Correct | Royalty figure roughly 25% too high |

---

## 1. Post 1, Substack version (Minor)

**Superfan statistic used the wrong denominator, and a Goldman forecast I could not source**

Luminate's figure is 15% of the **general population** in the US, not of listeners. The "$200bn" forecast could not be confirmed in any source I can open; Goldman's verified figure is a $4.3bn annual uplift on 2026 projections.

**Find this:**

> Luminate's research popularised the finding that about 15% of US listeners are superfans who spend well above average. Goldman Sachs put superfan monetisation at the centre of a forecast reaching toward $200bn.

**Replace with:**

> Luminate's research popularised the finding that about 15% of the general population in the US count as superfans, people who spend well above average on music. Note the denominator there: it is the whole population, not just listeners, so among people who actually listen the share is higher still. Goldman Sachs put superfan monetisation at the centre of its growth case, estimating a potential annual revenue uplift of $4.3 billion on 2026 projections, on the assumption that a fifth of paid subscribers are superfans who would spend twice what an average subscriber does.

---

## 2. Post 2, Medium version (Correct)

**Carlini et al. (2022) said the opposite of what the post reports**

Their conclusion is that memorisation is **more** prevalent than previously believed and worsens with scale. Duplication is one of three factors that increase it, not evidence it is rare. The post's argument survives; the attribution does not.

**Find this:**

> But research shows this only happens for the rare examples that appeared many times over, not the typical song buried once in the pile.

**Replace with:**

> But the research that quantified this found memorisation grows with the size of the model, with how many times an example was duplicated, and with how much context you feed in, and concluded it is more common than people had assumed rather than less. The catch for one songwriter is the duplication part: a track that appeared once is the least likely to come back out, so getting nothing proves nothing.

---

## 3. Post 2, Substack version (Correct)

**Carlini et al. (2022) said the opposite of what the post reports**

Same issue as the Medium version, at more length.

**Find this:**

> But Carlini and colleagues quantified the catch in 2022: this memorisation clusters on the handful of examples that appeared many times over in training. The typical work, present once, is simply not the kind of thing the model reproduces. So extraction can prove misuse for duplicated, high-frequency material, and stays completely silent about everything else, which is most of everything.

**Replace with:**

> Carlini and colleagues quantified it in 2022, and the finding cuts against the comforting reading. Memorisation grows on three axes at once: the bigger the model, the more times an example was duplicated in training, and the more context you use to prompt it. Their conclusion was that memorisation is more prevalent than people had believed, and will get worse as models scale.
>
> So extraction is a real phenomenon, not a curiosity. The catch for any one songwriter is that middle axis. Because memorisation leans so heavily on duplication, the track that appeared once in an enormous corpus is the least likely thing to come back out word for word. Extraction can therefore demonstrate misuse for heavily duplicated material, and its silence about everything else proves nothing at all.

---

## 4. Post 2, Substack version (Minor)

**"Millions of plays" unverified, and the Deezer share is now out of date**

The play count is not in the Variety report. Deezer's share has since passed half of daily uploads, and the same source gives the listening share, which is the more interesting number.

**Find this:**

> This is the same period in which a fake, AI-cloned Drake and Weeknd track, "Heart on My Sleeve", pulled millions of plays before Universal got it pulled in 2023, and Deezer began reporting that AI-generated tracks had climbed from about 28% of its uploads in September 2025 to roughly 44% by April 2026.

**Replace with:**

> This is the same period in which a fake, AI-cloned Drake and Weeknd track, "Heart on My Sleeve", spread far enough in 2023 to alarm the industry before Universal was identified as the source of the takedown notices, and Deezer began publishing the only running count anyone has: fully AI-generated tracks went from about 28% of its uploads in September 2025 to 44% by April 2026, and passed half in June 2026 at roughly 90,000 a day. One figure keeps that in proportion, though. Deezer says this music is still only 1% to 3% of its total streams, and that up to 85% of those streams look fraudulent.

---

## 5. Post 3, Medium version (Correct)

**Royalty figure roughly 25% too high**

The ten-million figure was the 2024 indictment's allegation. At the plea he forfeited **$8,091,843.64**.

**Find this:**

> In 2024 a musician was charged in the United States with using AI to generate thousands of songs and armies of bots to stream them, siphoning off around ten million dollars in royalties.

**Replace with:**

> In 2024 a musician was charged in the United States with using AI to generate hundreds of thousands of songs and armies of bots to stream them. He pleaded guilty in March 2026 and agreed to hand back $8,091,843.64, the royalties the scheme had taken.

---

## 6. Post 3, Substack version (Correct)

**Royalty figure roughly 25% too high**

Same as Medium, and this version also stated the guilty plea, which makes pairing it with the higher number the part that misleads.

**Find this:**

> In 2024 a musician was charged in the United States with using AI-generated tracks and armies of bots to stream them, siphoning off around ten million dollars in royalties; he pleaded guilty in 2026.

**Replace with:**

> In 2024 a musician was charged in the United States with using AI-generated tracks and armies of bots to stream them.
>
> He pleaded guilty on 19 March 2026 to one count of conspiracy to commit wire fraud, agreeing to forfeit $8,091,843.64, with sentencing set for that July. The ten-million-dollar figure that circulated early on was the indictment's allegation; eight million is what he admitted to taking.

---

## Suggested note for post 2

Posts 2's error misstated a named researcher's conclusion, so it is worth being visible about. Something like:

> *Corrected: an earlier version described Carlini et al. (2022) as showing that memorisation affects only heavily duplicated examples. Their paper in fact concludes that memorisation is more prevalent than previously believed and grows with model scale. The point about a single track being unlikely to be reproduced still holds, but it is an inference from their duplication finding rather than their conclusion.*

Posts 1 and 3 are a figure and a statistic; a silent edit is defensible there, though Substack will notify subscribers of any revision either way.

## Not changed

Post 2's litigation timing and post 4 throughout. Post 4 already carried the corrected Spotify launch date (founded 2006, opened to listeners 2008), and nothing else in it needed touching.
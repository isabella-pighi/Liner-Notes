# Post 6: Your attribution report is telling you what you want to hear

*Angle: correlation versus causation in music marketing, and the experiment discipline that fixes it. Feeds off section 3 of Part 2. Audience: marketers, labels, artist teams, anyone who has ever been shown a dashboard.*

---

## Medium version

### The playlist that took credit for everything

A song gets added to a big playlist on a Tuesday. Streams jump. By Friday somebody has made a slide showing the playlist and the jump, with an arrow between them.

That arrow is the most expensive assumption in music marketing.

Some of those streams were caused by the placement. Some came from fans who were going to play the song that week regardless, and who happened to find it through the playlist rather than through their own library. In the data those two groups are indistinguishable: both are streams, both arrived after the placement, and only one of them is a result you can claim.

![Attribution credits the whole column of streams that follows a campaign. Only the band on top was caused by it, and that band can be zero.](figures/fig_incrementality.png)

*Attribution credits the whole column of streams that follows a campaign. Only the band on top was caused by it, and that band can be zero.*

### What eBay found when it actually tested

This isn't a music problem, and the cleanest demonstration comes from somewhere else entirely.

eBay ran controlled experiments on its own paid search advertising, the kind where you buy your own brand name as a keyword so you appear at the top when someone searches for you. Attribution reports had been crediting that spend with real, substantial value for years. When Blake, Nosko and Tadelis tested it properly in 2015, by switching it off in some places and not others, they found brand-keyword ads had no measurable short-term benefit at all. Search clicks and purchase intent are correlated, so those clicks were largely coming from people who would have arrived anyway.

Nothing was broken and the reports were counting correctly. They were just counting the wrong thing, because they had no way to see the customers who would have shown up regardless.

Swap "typed eBay into a search box" for "was always going to stream the new single" and you have the music version.

### The research is unusually blunt about this

Marketing research rarely speaks with one voice, and on this question it more or less does.

Lewis and Rao looked across twenty-five large field experiments with major US retailers and brokerages, most of them reaching millions of customers, and found that measuring the returns to advertising is simply difficult. One number conveys it: the median confidence interval on return on investment came out over 100 percentage points wide. Their explanation is almost mechanical, since individual sales are wildly volatile next to the per-person cost of the advertising, so an informative experiment can easily need more than 10 million person-weeks.

Sit with that for a second. If a controlled experiment with millions of people struggles to find the effect, then a dashboard with no experiment at all is not measuring a weaker version of the same thing, it is telling you a story with numbers in it.

Gordon and colleagues made it concrete in 2019, comparing the usual observational attribution methods against large randomised advertising experiments run at Facebook, where the true answer was known. Their finding, in their own words, is that observational methods often fail to accurately recover the treatment effects the experiments generated. Not a small bias you could correct for, which would at least be useful.

### The shortcuts we reach for are the ones that fail hardest

Last-touch attribution, crediting whatever the person clicked last, is the industry default. Berman showed formally in 2018 that it overincentivises ad exposures and often leaves advertisers with lower profits than a more sophisticated method would. His result has a twist worth knowing: the parties who benefit most from advertisers using last-touch are the popular publishers and those appearing *early* in the conversion funnel, which is not where most people assume the distortion lands. Multi-touch models, built to fix last-click, inherit the same flaw. Their lineage runs back to work by Shao and Li in 2011, and however sophisticated the weighting gets, they are still learning from what happened to occur together. More elaborate maths applied to the same confusion.

### What working properly looks like

A discipline called incrementality fixes this, and it asks a harder question than "what did they click?" It asks what happened that wouldn't have happened otherwise. Answering that means holding something back, so some audience or region or period gets no campaign and you have something to compare against.

In music you usually cannot split an artist's fanbase in half and market to only one side, which is a genuine constraint rather than an excuse. So geography becomes the practical tool: run the campaign in some cities and not others, then compare. Chen and Au published a robust method for reading return on ad spend from paired-region tests in 2022, and Johnson's 2023 guide covers running and interpreting field experiments in online display advertising, a medium he calls hostile to experimentation, because ad effects are tiny and the experimenter has limited control over who actually gets exposed.

And this has already been done for music. Aguiar and Waldfogel used Spotify playlist placements to estimate what promotion is genuinely worth, rather than naively crediting a playlist with every stream that followed it, which is the shape the honest version of this work takes.

### The uncomfortable operating rule

Here is the sentence that follows from all of it, and it is not a comfortable one to adopt. Treat any attribution number that did not come from an experiment as a hunch rather than a measurement.

That isn't the same as worthless, and experienced people have very good hunches. But a hunch does not belong in a slide with a decimal point on it, presented to someone deciding where next quarter's budget goes.

The fix isn't better software, it's a standing capability to run experiments, so that when somebody asks whether the campaign worked, holding a region back was already in the plan.

*This is drawn from the second part of a longer paper on music data strategy. The full version, with every study cited, is here: [github.com/isabella-pighi/Liner-Notes](https://github.com/isabella-pighi/Liner-Notes). This work grew out of a talk, "From Data Deluge to Data Strategy: Get the Power of Insights," that I gave with Chiara Santoro at [SXSW 2025](https://schedule.sxsw.com/2025/events/PP153768).*

---

## Substack version

### From "looks related" to "actually caused it"

*Twenty years of advertising research says the same thing: you cannot read causal effect off observational data, no matter how much of it you have. Here is what the experiments found, why music makes the problem worse, and the toolkit that survives contact with reality.*

Part 1 of this series described a failure mode: reading a streaming spike that coincides with a marketing push as though the push caused it. I want to be precise about why more data does not fix that, because the instinct in every data team is to believe it will.

Resolution is not the problem.

![Attribution credits the whole column of streams that follows a campaign. Only the band on top was caused by it, and that band can be zero.](figures/fig_incrementality.png)

*Attribution credits the whole column of streams that follows a campaign. Only the band on top was caused by it, and that band can be zero.*

What's missing is the counterfactual: you observe what happened after the campaign, you never observe what would have happened without it, and no amount of additional observation of the first thing will ever produce the second.

### The strongest evidence in marketing research

Start with Lewis and Rao, whose 2015 paper examined twenty-five large digital advertising field experiments. Their conclusion is uncomfortable and load-bearing: the return on advertising is nearly impossible to determine from observational data, because advertising's effect on sales is small relative to the natural variance in sales.

The consequence they draw is the part people skip: even experiments with millions of participants frequently lack the statistical power to detect the effect at all. Not "return an imprecise estimate", but cannot detect it. If the randomised version with enormous samples struggles, an observational estimate is not a noisier measurement of the same quantity. It is a different object, one whose error you have no way to bound.

Gordon and colleagues tested this directly in 2019, running standard observational attribution methods against big randomised advertising experiments at Facebook, where the experimental result supplied ground truth. Their conclusion is blunt: observational methods often fail to accurately recover the treatment effects generated by the experiments. That is a property of the situation rather than a tuning parameter somebody forgot to set.

### The methods the industry actually uses

Last-touch attribution assigns credit to the final click before conversion. Berman's 2018 analysis shows formally that the popular last-touch method overincentivises ad exposures and often results in lower advertiser profits, with the Shapley value doing better on that measure. The counterintuitive part of his result is who gains: popular publishers, and those appearing early in the conversion funnel, benefit most from advertisers using last-touch. So the distortion is not simply that the last click hogs the credit; it reshapes the whole bidding relationship.

Multi-touch models were the response. Their methodological lineage traces to Shao and Li in 2011, and the sophistication has grown considerably since. But the fundamental issue survives the upgrade: these models are fitted to co-occurrence. They learn which touchpoints tend to appear in paths that converted, which is not the same as learning which touchpoints made conversion happen. Distributing credit more cleverly across a correlational signal produces a more defensible-looking number, not a more accurate one.

Then there is the eBay result.

I think every music marketer should know this one by heart.

Blake, Nosko and Tadelis ran a series of large-scale field experiments at eBay in 2015 to measure the causal effectiveness of paid search. Two findings matter here. Brand-keyword ads, the practice of bidding on your own name, showed no measurable short-term benefit.

And for non-brand keywords, new and infrequent users were positively influenced, but the frequent users whose purchasing was *not* influenced accounted for most of the spend, so average returns came out negative. Their framing of the mechanism is the transferable part: because search clicks and purchase intent are correlated, returns from paid search are a fraction of the non-experimental estimates. That parallel needs no translation. A playlist add, an ad burst, a social push can all look responsible for streams from fans who were always going to listen. The stronger an artist's existing fanbase, the more the effect flatters whatever channel happens to be standing closest when those fans arrive.

### Incrementality, and the music-specific constraint

Incrementality is the discipline of measuring what would not have happened otherwise, and it has a mature toolkit. Varian's 2016 overview sets out the practitioner menu, controlled experiments through to before-and-after designs, and Yao and colleagues give the technical treatment in 2021. Standard practice is to split an audience, treat one half and withhold from the other. Music frequently cannot do this. You cannot cut an artist's fanbase in two and market to only one side, both because the audience is not cleanly partitionable and because withholding a release moment from half your fans is commercially unacceptable.

So geography carries the load instead: run the campaign in some regions and not others, then compare like with like. Chen and Au published a robust method in 2022 for estimating return on ad spend from paired-region designs, which is directly applicable. Johnson's 2023 guide walks through running and interpreting field experiments in online display advertising, and his framing of the difficulty is the useful part: display-ad effects are tiny, they therefore need large-scale experiments, and the experimenter has limited control because exposure is jointly determined by advertisers, users, algorithms and market competition.

And a template already exists in music. Aguiar and Waldfogel used Spotify playlist placements to estimate the true streaming value of promotion, instead of attributing to a playlist every stream that occurred after it. That is the shape of honest attribution in this industry: identify the variation you did not choose, and read the effect from it.

### What experiments cost

I do not want to oversell experiments, because they have real costs and the pitch usually hides them.

They require withholding, which means somebody has to accept that a region or a segment or a fortnight gets less marketing so the rest can be measured, and that argument has to be won before the campaign rather than after it. They're slow relative to the pace a release cycle actually runs at. They answer narrow questions, so a geo test on one campaign tells you little about a different campaign with different creative. And they carry their own failure modes: contaminated controls, spillover between adjacent regions, seasonal effects that happen to line up with your test window.

None of that makes the observational number better. It makes the experimental number expensive and the observational number unreliable, which is a genuinely awkward position and the one the industry is actually in.

### The rule I'd actually adopt

Default to incrementality and geo tests for marketing decisions, and treat any attribution number that did not come from an experiment as a hunch rather than a measurement.

A hunch is permitted, and an experienced marketer's read on a release is worth more than most models. What is not permitted is laundering that hunch through a dashboard until it acquires a decimal point and the authority of a measurement, and then betting next quarter's budget on it.

This connects back to why identity sits at the bottom of the stack. You cannot run a clean geo test if you cannot reliably tell that the streams in Manchester and the streams in Lyon refer to the same recording. Every measurement claim in this section assumes the identifier layer already holds.

*Full paper, figures, and complete bibliography: [github.com/isabella-pighi/Liner-Notes](https://github.com/isabella-pighi/Liner-Notes). This post expands the causal-measurement section of Part 2. This work grew out of a talk, "From Data Deluge to Data Strategy: Get the Power of Insights," that I gave with Chiara Santoro at [SXSW 2025](https://schedule.sxsw.com/2025/events/PP153768).*

---

## LinkedIn note

eBay tested whether buying its own brand name as a search keyword actually worked. Attribution had credited it with real value for years. Brand-keyword ads turned out to have no measurable short-term benefit: search clicks and purchase intent are correlated, so those clicks came largely from people who would have arrived anyway.

Now swap "searched for eBay" for "was always going to stream the new single."

New post on why attribution reports credit campaigns for sales that were coming anyway, and the experiment discipline that fixes it, from a talk Chiara Santoro and I gave at SXSW 2025.

[Medium] · [Substack] · github.com/isabella-pighi/Liner-Notes

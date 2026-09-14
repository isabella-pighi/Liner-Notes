# Post 5: The identifier layer, and the royalties that go unpaid without it

*Angle: the identifier and metadata backbone, and the unclaimed royalties that pile up when it fails. Feeds off section 2 of Part 2. Audience: artists, managers, labels, anyone who has wondered where a royalty went.*

---

## Medium version

### Music's black box problem

Somewhere in the accounts of a collecting society there is a small pile of money that belongs to a musician who will probably never see it, because nobody can work out whose it is.

This is called the black box, and it is the least glamorous problem in music. It is also one of the most expensive.

The US Mechanical Licensing Collective now reports over $4 billion in total streaming royalties distributed, which is the part of its record that gets quoted. Less quoted is the other pool, which the MLC calls unclaimed accrued royalties: money it has received but has not been able to match or distribute, despite trying, by the time the statutory holding period runs out.

Nobody argues about the cause.

A piece of music and the data describing it set off down separate roads and never meet, and by the time the money arrives there is no way left to work out who should receive it.

Here is the part worth understanding, and it is written into US law rather than being anyone's decision. Under the Music Modernization Act the MLC is congressionally mandated to eventually hand that unmatched pool onward, and it intends to start in 2027 through what it calls the market share distribution process, beginning with 2021 usage. Market share means catalogue size. So royalties that could not be matched to the writer who earned them are distributed in proportion to what everyone else already holds. Whatever you make of that as policy, it is the designed outcome rather than a loophole, and it is why the matching problem has a deadline attached to it.

How much is stuck this way is genuinely disputed, and I would rather show you the disagreement than pick a number and sound confident. The Ivors Academy in the UK has put it at £500 million a year for streaming alone, while Billboard, looking at the US, estimated it at "at most $250 million", and those two figures are not reconcilable by any arithmetic I can do. The gap is worth sitting with. There is no agreed measure of how much goes unpaid, which tells you how hard this is to see from outside the matching process itself.

### Three codes and a boring truth

The frustrating thing is that the industry solved this decades ago, on paper.

Three international codes between them answer the only questions that matter. An ISRC identifies a specific recording, the actual audio, and the international ISRC database now contains over 150 million unique codes with their recording and release data attached. An ISWC identifies the song underneath, the composition, which is what songwriters get paid on. And an ISNI identifies the people, the writers and performers and producers, so that two artists with the same name stop getting each other's money.

One song, many recordings, all tied back to actual humans. That chain of codes is the join key the entire royalty system runs on, and it is also the answer to the complaint Part 1 spent its whole length making. Comparability across platforms was never going to arrive as a clever scoring formula somebody invents; it arrives when a play on one service and a play on another can be shown to point at the same recording. When they can't, every number you build on top of them is guesswork wearing a decimal point.

A set of standards called DDEX moves those codes through the supply chain, so the identifier travels with the release instead of being re-entered by hand further down the line.

![The identifier chain is the join key: one song maps to many recordings, all tied back to named people. Break any link and the royalty has nowhere to land.](figures/fig_black_box_chain.png)

*The identifier chain is the join key: one song maps to many recordings, all tied back to named people. Break any link and the royalty has nowhere to land.*

### Metadata as a growth lever, not paperwork

Now the part that surprised me, because it reframes the whole thing.

Good metadata is usually sold to artists as compliance: do your admin or you won't get paid. True enough, but that framing badly undersells what it does. One of the DDEX standards, MEAD, exists specifically to carry the richer descriptive material, lyrics, focus tracks, instrumentation, mood. DDEX's own stated purpose for it is telling: the standard is about what sort of information supports the marketing of music by streaming services.

In other words the people who designed the standard did not build it for the royalty department. They built it to help the music get found, which is not how anyone has ever pitched a metadata project to an artist.

That turns metadata into a marketing asset rather than a filing chore, which is a far easier argument to win in an organisation where compliance spending is the first thing cut.

### Capture it at the session, not afterwards

Every serious attempt to fix the black box lands on the same conclusion.

You cannot reconstruct this stuff later. Credits have to be captured at the moment of creation, in the studio, while everyone who was in the room is still in the room and can be named, because eighteen months on you are asking people who have moved house, changed email address, or simply stopped remembering.

That's the argument behind Credits Due, the campaign led by Björn Ulvaeus with the Ivors Academy, and behind studio-facing tools like Sound Credit, which will generate ISNI and ISRC identifiers for you in a click.

Estimates of how big the yearly black box is vary a lot, from the Ivors Academy's figure of around £500 million in streaming to more cautious US numbers. I would not stake anything on one particular figure, and you shouldn't either. But nobody disagrees about the cause: a piece of music and its metadata set off down separate roads and never meet.

If you take one thing from this: treat assigning identifiers and capturing credits as a contractual duty at the session, not a clean-up task for later. It is the least exciting sentence in this series and possibly the most profitable.

*This is drawn from the second part of a longer paper on music data strategy. The full version, with the standards cited and a diagram of how the layers stack up, is here: [github.com/isabella-pighi/Liner-Notes](https://github.com/isabella-pighi/Liner-Notes). This work grew out of a talk, "From Data Deluge to Data Strategy: Get the Power of Insights," that I gave with Chiara Santoro at [SXSW 2025](https://schedule.sxsw.com/2025/events/PP153768).*

---

## Substack version

### Music's black box problem and the identifier layer beneath it

*A pool of streaming royalties sits unclaimed at one US collecting society, and the cause has no glamour attached to it at all: nobody can establish which recording, which song, and which person a data point refers to. Here is the layer that fixes it, and why it is a discovery problem as much as an accounting one.*

Start with the numbers, because they frame what follows.

The US Mechanical Licensing Collective reports over $4 billion in total streaming royalties distributed, having crossed $3 billion at its annual membership meeting in October 2025. It simultaneously holds what it calls unclaimed accrued royalties: money it has received but has not been able to match or distribute, despite its efforts, by the time the statutory minimum holding period expires. The explanation is mundane: the data describing the music was incomplete, inconsistent, or simply absent by the time it arrived.

What makes this structural rather than merely annoying is that the money has no route home. It is not waiting for a claim form.

Nobody knows whose it is, so the matching has to be reconstructed from records that were already incomplete when they were made, and every year that passes makes that reconstruction harder and the people who could have answered the question less reachable.

Estimates of the annual scale differ widely and I want to be honest about that rather than reach for the biggest number. The Ivors Academy in the UK has estimated it at £500 million a year for streaming alone. Billboard, looking at the US, put it at "at most $250 million". Those are not reconcilable estimates, and treating the range as the finding is more honest than picking a figure. What everyone does share is the diagnosis: music and its metadata travel separately and fail to meet.

### Identity is the bottom layer for a reason

Part 2 of the paper argues that a data strategy is a stack, and that you only get value at the top if every layer beneath it holds. Identity sits at the bottom, underneath everything, because every other ambition depends on it.

You cannot credit a campaign for a streaming spike if you cannot reliably say which recording spiked. You cannot build a picture of your most valuable fans if you cannot tell that the track they played on one service and the track they played on another are the same track. Comparability across platforms, the thing Part 1 spent its length complaining about, is not a scoring formula anyone can invent. It is an identifier problem.

Three ISO standards do the work.

An **ISRC** (ISO 3901) permanently identifies a sound recording or music video, and the international ISRC database now contains over 150 million unique codes registered with their associated recording and release data. An **ISWC** (ISO 15707) identifies the underlying musical work, the composition rather than any particular recording of it, and CISAC's agency runs it for the societies that pay songwriters and publishers. An **ISNI** (ISO 27729) identifies the people: writers, performers, producers, publishers, and it acts as a bridge between private rights databases and public discovery tools.

Their relationship is the important bit.

![The identifier chain is the join key: one song maps to many recordings, all tied back to named people. Break any link and the royalty has nowhere to land.](figures/fig_black_box_chain.png)

*The identifier chain is the join key: one song maps to many recordings, all tied back to named people. Break any link and the royalty has nowhere to land.*

One ISWC maps to many ISRCs, all of it tied back to people through ISNI. That mapping is the join key the royalty system runs on, and when any link in it breaks the payment has nowhere to land.

### Codes that cannot travel are worthless

An identifier sitting in a spreadsheet on someone's laptop does nothing. It has to move through the supply chain attached to the release, which is the job of the DDEX message standards.

Labels and distributors announce a release to streaming services through the Electronic Release Notification suite (ERN), which carries the ISRC alongside deal terms, territories, rights and takedowns. ERN 4 adds a single consolidated list of every artist, writer and label involved, which is precisely the thing that used to get lost. Two companion standards matter more than their obscurity suggests. MEAD (Media Enrichment and Description) carries the descriptive richness, lyrics and focus tracks and instrumentation and moods, the material that actually powers search and discovery. RIN (Recording Information Notification) captures credits at the moment of recording, in the studio, at source.

And alongside the closed industry standards there is MusicBrainz, an open encyclopedia that issues a public-domain identifier (the MBID) for artists, works, recordings and releases. It offers a freely reusable identity layer as an alternative to locked silos, which matters if you would rather not depend entirely on infrastructure you cannot inspect.

### A finding that changes the argument

Metadata is normally justified defensively: do the admin, avoid the loss.

That framing has been losing this argument inside companies for twenty years, because defensive spending is the first thing anyone cuts, and a cost centre rarely wins a budget round against something with revenue attached to it.

Which is why the most useful evidence in this section is commercial rather than accounting. DDEX's own description of what MEAD is for makes the point: the standard exists to carry the sort of information that supports the marketing of music by streaming services, and DDEX expects it to expand as understanding of that grows.

That is a discovery mandate, not a compliance one. Richer description is what lets recommendation systems place music accurately, which makes metadata a growth lever rather than paperwork, and that is a budget conversation with a completely different shape.

I will add the honest caveat. I have seen figures quoted for how much MEAD-enriched metadata lifts plays and cuts skip rates, and I have deliberately left them out, because when I went to check them I could not find them stated on DDEX's own pages for the standard. The mechanism is plausible and the direction is almost certainly right. The specific percentages are not something I am willing to put in front of you until I can point at where they come from.

### Why "we'll fix it later" never works

Reconstruction after the fact is the failure mode. Once a release is out and the credits weren't captured, you are trying to remember who played bass on a session eighteen months ago, and the answer is distributed across people who have moved on, changed email addresses, or simply forgotten. Which is why the industry's fix is procedural rather than technical. Credits Due, led by Björn Ulvaeus with the Ivors Academy, campaigns for complete credit capture at the point of creation. Tools like Sound Credit are built for that moment, generating ISNI and ISRC identifiers at the point the work is made rather than leaving them to be chased later.

This layer's move is unglamorous and it is also the whole foundation: make assigning identifiers and capturing credits a contractual obligation at the session, not a clean-up task for later. Everything in the rest of Part 2, the fan graph, the causal measurement, the consent registries, assumes this layer already holds. When it doesn't, the layers above are building on sand, and the most visible symptom is a pool of royalties that cannot be matched to the people who earned them.

*Full paper, figures, and complete bibliography: [github.com/isabella-pighi/Liner-Notes](https://github.com/isabella-pighi/Liner-Notes). This post expands the identifier and metadata section of Part 2. This work grew out of a talk, "From Data Deluge to Data Strategy: Get the Power of Insights," that I gave with Chiara Santoro at [SXSW 2025](https://schedule.sxsw.com/2025/events/PP153768).*

---

## LinkedIn note

One US collecting society has paid out over $4 billion in streaming royalties. It is also sitting on a pool it cannot pay out at all: not stolen, just unmatchable, because the metadata didn't survive the journey.

And under US law that pool eventually gets shared out by market share, which routes it to the biggest catalogues rather than the people who earned it.

Estimates of the yearly total are all over the place, from £500 million in UK streaming to "at most $250 million" in the US. An industry that can't agree on the size of its own unpaid pile.

New post on the least glamorous layer of music data strategy, and the one everything else sits on, from a talk Chiara Santoro and I gave at SXSW 2025.

[Medium] · [Substack] · github.com/isabella-pighi/Liner-Notes

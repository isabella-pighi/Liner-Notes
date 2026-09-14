# Post 5: Identifiers, metadata, and unmatched royalties

*Angle: the identifier and metadata backbone, and the unclaimed royalties that pile up when it fails. Feeds off section 2 of Part 2. Audience: artists, managers, labels, anyone who has wondered where a royalty went.*

---

## Medium version

### Music's black box problem

Somewhere in the accounts of a collecting society sits a small amount of money that belongs to a musician who will probably never receive it, because nobody can establish whose it is.

This is known as the black box, and it is the least glamorous problem in music. It is also one of the most expensive.

In the US, the Mechanical Licensing Collective now reports over $4 billion in total streaming royalties distributed, which is the part of the record that tends to get quoted. Less quoted is the other pool, which the MLC calls unclaimed accrued royalties: money it has received but has not been able to match or distribute, despite trying, by the time the statutory holding period runs out.

Nobody argues about the cause.

A piece of music and the data describing it set off down separate roads and never meet, and by the time the money arrives there is no way left to work out who should receive it.

What happens next is written into US law rather than being anyone's decision. Under the Music Modernization Act the MLC is congressionally mandated to eventually pass that unmatched pool onward, and it intends to start in 2027 through what it calls the market share distribution process, beginning with 2021 usage. Market share means catalogue size. So royalties that could not be matched to the writer who earned them are distributed in proportion to what everyone else already holds. Whatever the merits of that as policy, it is the designed outcome rather than a loophole, and it is why the matching problem has a deadline attached to it.

How much is stuck this way is genuinely disputed, and the disagreement is more informative than any single figure. The Ivors Academy in the UK has put it at £500 million a year for streaming alone, while Billboard, looking at the US, estimated it at "at most $250 million". Those two numbers are not reconcilable by any arithmetic. There is no agreed measure of how much goes unpaid, which indicates how hard the problem is to see from outside the matching process itself.

### Three codes that carry the money

On paper, the industry solved this decades ago.

Three international codes between them answer the only questions that matter. An ISRC identifies a specific recording, the actual audio, and the international ISRC database now contains over 150 million unique codes with their recording and release data attached. An ISWC identifies the song underneath, the composition, which is what songwriters are paid on. And an ISNI identifies the people, the writers and performers and producers, so that two artists with the same name stop receiving each other's money.

One song, many recordings, all tied back to named people. That chain of codes is the join key the entire royalty system runs on, and it is also the answer to the complaint Part 1 spent its whole length making. Comparability across platforms was never going to arrive as a clever scoring formula. It arrives when a play on one service and a play on another can be shown to point at the same recording. Until then, every number built on top of them is guesswork wearing a decimal point.

A set of standards called DDEX moves those codes through the supply chain, so the identifier travels with the release instead of being re-entered by hand further down the line.

![The identifier chain is the join key: one song maps to many recordings, all tied back to named people. Break any link and the royalty has nowhere to land.](figures/fig_black_box_chain.png)

*The identifier chain is the join key: one song maps to many recordings, all tied back to named people. Break any link and the royalty has nowhere to land.*

### Metadata as a discovery asset

Good metadata is usually sold to artists as compliance: complete the admin or the payment does not arrive. True enough, but that framing badly undersells what it does. One of the DDEX standards, MEAD, exists specifically to carry the richer descriptive material: lyrics, focus tracks, instrumentation, mood. DDEX's own stated purpose for it is telling, in that the standard is about what sort of information supports the marketing of music by streaming services.

In other words, the people who designed the standard did not build it for the royalty department. They built it to help the music get found, which is not how a metadata project is usually pitched to an artist.

That turns metadata into a marketing asset rather than a filing chore, which is a far easier argument to win in an organisation where compliance spending is the first thing cut.

### Capturing credits at the session

Every serious attempt to fix the black box arrives at the same conclusion.

This information cannot be reconstructed later. Credits have to be captured at the moment of creation, in the studio, while everyone who was in the room is still in the room and can be named. Eighteen months on, the question goes to people who have moved house, changed email address, or simply stopped remembering.

That is the argument behind Credits Due, the campaign led by Björn Ulvaeus with the Ivors Academy, and behind studio-facing tools such as Sound Credit, which generate ISNI and ISRC identifiers in a click.

The single most useful change is also the dullest: treat assigning identifiers and capturing credits as a contractual duty at the session, not a clean-up task for later. It is the least exciting sentence in this series and possibly the most profitable.

*This is drawn from the second part of a longer paper on music data strategy. The full version, with the standards cited and a diagram of how the layers stack up, is here: [github.com/isabella-pighi/Liner-Notes](https://github.com/isabella-pighi/Liner-Notes). This work grew out of "From Data Deluge to Data Strategy: Get the Power of Insights," presented by Isabella Pighi and Chiara Santoro at [SXSW 2025](https://schedule.sxsw.com/2025/events/PP153768).*

---

## Substack version

### Music's black box problem and the identifier layer beneath it

*A pool of streaming royalties sits unclaimed at one US collecting society, and the cause has no glamour attached to it at all: nobody can establish which recording, which song, and which person a data point refers to. This is the layer that fixes it, and why it is a discovery problem as much as an accounting one.*

Start with the numbers, because they frame what follows.

The US Mechanical Licensing Collective reports over $4 billion in total streaming royalties distributed, having crossed $3 billion at its annual membership meeting in October 2025. It simultaneously holds what it calls unclaimed accrued royalties: money it has received but has not been able to match or distribute, despite its efforts, by the time the statutory minimum holding period expires. The explanation is mundane: the data describing the music was incomplete, inconsistent, or simply absent by the time it arrived.

What makes this structural rather than merely annoying is that the money has no route home. It is not waiting for a claim form.

Nobody knows whose it is, so the matching has to be reconstructed from records that were already incomplete when they were made, and every year that passes makes that reconstruction harder and the people who could have answered the question less reachable.

Estimates of the annual scale differ widely, and the range is a more honest finding than any single figure. The Ivors Academy in the UK has estimated it at £500 million a year for streaming alone. Billboard, looking at the US, put it at "at most $250 million". Those are not reconcilable estimates. What everyone does share is the diagnosis: music and its metadata travel separately and fail to meet.

### Identity as the bottom layer

Part 2 of the paper argues that a data strategy is a stack, and that value only appears at the top if every layer beneath it holds. Identity sits at the bottom, underneath everything, because every other ambition depends on it.

A campaign cannot be credited with a streaming spike unless the spiking recording can be reliably identified. A picture of an artist's most valuable fans cannot be assembled unless a track played on one service can be matched to the same track played on another. Comparability across platforms, the thing Part 1 spent its length complaining about, is not a scoring formula anyone can invent. It is an identifier problem.

Three ISO standards do the work.

An **ISRC** (ISO 3901) permanently identifies a sound recording or music video, and the international ISRC database now contains over 150 million unique codes registered with their associated recording and release data. An **ISWC** (ISO 15707) identifies the underlying musical work, the composition rather than any particular recording of it, and CISAC's agency runs it for the societies that pay songwriters and publishers. An **ISNI** (ISO 27729) identifies the people, meaning writers, performers, producers and publishers, and it acts as a bridge between private rights databases and public discovery tools.

Their relationship is the important part.

![The identifier chain is the join key: one song maps to many recordings, all tied back to named people. Break any link and the royalty has nowhere to land.](figures/fig_black_box_chain.png)

*The identifier chain is the join key: one song maps to many recordings, all tied back to named people. Break any link and the royalty has nowhere to land.*

One ISWC maps to many ISRCs, all of it tied back to people through ISNI. That mapping is the join key the royalty system runs on, and when any link in it breaks the payment has nowhere to land.

### Codes have to be able to travel

An identifier sitting in a spreadsheet on a laptop does nothing. It has to move through the supply chain attached to the release, which is the job of the DDEX message standards.

Labels and distributors announce a release to streaming services through the Electronic Release Notification suite (ERN), which carries the ISRC alongside deal terms, territories, rights and takedowns. ERN 4 adds a single consolidated list of every artist, writer and label involved, which is precisely the thing that used to get lost. Two companion standards matter more than their obscurity suggests. MEAD (Media Enrichment and Description) carries the descriptive richness, meaning lyrics and focus tracks and instrumentation and moods, the material that actually powers search and discovery. RIN (Recording Information Notification) captures credits at the moment of recording, in the studio, at source.

Alongside the closed industry standards there is MusicBrainz, an open encyclopedia that issues a public-domain identifier (the MBID) for artists, works, recordings and releases. It offers a freely reusable identity layer as an alternative to locked silos, which matters to anyone reluctant to depend entirely on databases that cannot be inspected.

### A commercial case rather than a defensive one

Metadata is normally justified defensively: complete the admin, avoid the loss.

That framing has been losing this argument inside companies for twenty years, because defensive spending is the first thing cut, and a cost centre rarely wins a budget round against something with revenue attached to it.

Which is why the most useful evidence in this section is commercial rather than accounting. DDEX's own description of what MEAD is for makes the point: the standard exists to carry the sort of information that supports the marketing of music by streaming services, and DDEX expects it to expand as understanding of that grows.

That is a discovery mandate, not a compliance one. Richer description is what lets recommendation systems place music accurately, which makes metadata a growth lever rather than paperwork, and that is a budget conversation with a completely different shape.

One caveat belongs here. Figures are quoted in places for how much MEAD-enriched metadata lifts plays and cuts skip rates, and they have deliberately been left out of this piece, because they could not be found stated on DDEX's own pages for the standard. The mechanism is plausible and the direction is almost certainly right. The specific percentages are not solid enough to repeat without a source to point at.

### Why later is too late

Reconstruction after the fact is the failure mode. Once a release is out and the credits were not captured, the question becomes who played bass on a session eighteen months ago, and the answer is distributed across people who have moved on, changed email addresses, or simply forgotten. Which is why the industry's fix is procedural rather than technical. Credits Due, led by Björn Ulvaeus with the Ivors Academy, campaigns for complete credit capture at the point of creation. Tools such as Sound Credit are built for that moment, generating ISNI and ISRC identifiers at the point the work is made rather than leaving them to be chased later.

This layer's move is unglamorous and it is also the whole foundation: make assigning identifiers and capturing credits a contractual obligation at the session, not a clean-up task for later. Everything in the rest of Part 2, the fan graph, the causal measurement, the consent registries, assumes this layer already holds. When it does not, the layers above are building on sand, and the most visible symptom is a pool of royalties that cannot be matched to the people who earned them.

*Full paper, figures, and complete bibliography: [github.com/isabella-pighi/Liner-Notes](https://github.com/isabella-pighi/Liner-Notes). This post expands the identifier and metadata section of Part 2. This work grew out of "From Data Deluge to Data Strategy: Get the Power of Insights," presented by Isabella Pighi and Chiara Santoro at [SXSW 2025](https://schedule.sxsw.com/2025/events/PP153768).*

---

## LinkedIn note

Music royalties depend on three identifiers: an ISRC (ISO 3901) for the recording, an ISWC (ISO 15707) for the composition beneath it, and an ISNI (ISO 27729) for the writers, performers and producers. The international ISRC database now holds over 150 million codes. Where those links are incomplete, a payment cannot be matched to the person who earned it.

The DDEX standards carry that information through the supply chain. One of them, MEAD, covers lyrics, instrumentation and mood, and DDEX describes its purpose as supporting how streaming services market music, so metadata bears on discovery as well as on royalties. New post on this layer, from a talk Chiara Santoro and I gave at SXSW 2025.

[Medium](https://medium.com/@isabella.pighi/identifiers-metadata-and-unmatched-royalties-e3c250a5380d?sharedUserId=isabella.pighi) · [Substack](https://isabellapighi.substack.com/p/identifiers-metadata-and-unmatched?r=uzcd4&utm_campaign=post-expanded-share&utm_medium=web) · github.com/isabella-pighi/Liner-Notes

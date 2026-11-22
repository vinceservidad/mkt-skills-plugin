# Format Selection

Format determines both the attention window available and the metrics that are even measurable — selecting it is not a creative-team preference, it is a decision that constrains everything downstream.

Format names, lengths, skip behavior, placements, and campaign-type compatibility are high-change platform facts. Each specification below is officially documented on Google's "About video ad formats" page and carries its check date; recheck it per [`PLATFORM-CURRENCY.md`](../../../library/contracts/PLATFORM-CURRENCY.md) before a plan depends on it, and confirm in the account that the format is available for the campaign type and subtype being planned. The "Fits" column is strategic judgment, not platform documentation.

## Formats and fit

| Format | Documented skip, length, and placement | Fits |
|---|---|---|
| Skippable in-stream | The viewer can skip after 5 seconds; no maximum length, under 3 minutes recommended; serves on YouTube videos and, when opted in, Google video partners (first-party: https://support.google.com/google-ads/answer/2375464, checked 2026-09-26) | Broad reach at controlled cost; the message must land or hook before the skip option appears |
| Non-skippable in-stream | Viewers can't skip; 15–60 seconds depending on the campaign subtype (first-party: https://support.google.com/google-ads/answer/2375464, checked 2026-09-26) | A complete message the audience must see in full; used when the message cannot be compressed to a bumper or cannot risk a skip |
| Bumper | Non-skippable; between 5 and 6 seconds (first-party: https://support.google.com/google-ads/answer/2375464, checked 2026-09-26) | A single, simple message or reinforcement of a message delivered elsewhere; not for a message requiring explanation |
| In-feed video ads | A thumbnail from the video with some text that invites a click to watch; serves in YouTube search results, alongside related videos (Watch Next), on the mobile Home feed, and in the Subscriptions feed; no maximum length (first-party: https://support.google.com/google-ads/answer/2375464, checked 2026-09-26) | Audiences actively browsing or searching; performance depends heavily on thumbnail and title, evaluated more like search intent than interruption advertising |
| YouTube Shorts ads | Serve between videos in the Shorts feed; users can skip immediately by swiping; under 60 seconds recommended (first-party: https://support.google.com/google-ads/answer/2375464, checked 2026-09-26) | Vertical, mobile-first creative built for the Shorts feed; the message has no guaranteed viewing window |
| Masthead | Top of the YouTube Home feed; available only on a reservation basis through a Google sales representative (first-party: https://support.google.com/google-ads/answer/2375464, checked 2026-09-26) | Very broad reach in a short window, such as a launch or sales event; a reservation commitment, not an auction test |

Label notes (first-party: https://support.google.com/google-ads/answer/2375464, checked 2026-09-26):

- The checked page names the browse-and-search format "in-feed video ads" and lists no format called "discovery"; use the current label in plans and account work. It does not state a rename date, so do not assert one.
- The checked page lists no separate "outstream" format. It classifies in-feed, Shorts, and Masthead as out-stream under its IAB classification, and notes that with Google video partners, skippable in-stream ads may serve as interstitial or rewarded ads resembling an outstream experience. Confirm current partner-inventory formats per `library/contracts/PLATFORM-CURRENCY.md` before planning an off-YouTube placement.
- For new campaigns the marketing objective previously labeled "Awareness and consideration" is now labeled "YouTube reach, views, and engagements", and the "Views" metric is now "TrueView views". The funnel objectives in this skill are strategic categories; map them to the current interface label separately.

## Method

1. Match format to funnel objective first, creative length second. An awareness objective can use any format; a direct-response objective needs enough time or clarity to communicate the offer and call to action.
2. For skippable formats, design the pre-skip window to work whether or not the viewer skips after — the hook must communicate the core message, not just earn attention for a longer reveal.
3. For bumper, the message must be genuinely compressible to the documented 5–6 second length; forcing a longer message into a bumper produces something incomprehensible, not something efficient.
4. For in-feed video ads, treat thumbnail and title with the same rigor as a search ad's headline — they are the entire mechanism determining whether the video is watched.
5. Where a placement may play without sound (the checked page documents Masthead autoplaying without sound), design for sound-off comprehension; do not assume audio is heard on partner inventory without checking current documentation and account-visible behavior.

## Rules

- Do not state a format length, skip window, placement, or eligibility rule without the first-party citation above or a fresh first-party check; when the citation is older than the high-change freshness gate in `library/contracts/PLATFORM-CURRENCY.md`, confirm the current format specification before relying on it.
- Do not select non-skippable to force message completion when the message itself is weak; a forced view of unpersuasive creative is not a fix for the creative problem.
- Do not use the same creative asset unedited across formats with different length and skip constraints; a 30-second asset trimmed to 6 seconds without redesign risks losing its message, not just its length.
- Format selection is reversible and testable; when uncertain between two formats for the same objective, prefer testing over asserting one is correct from principle alone.
- Format availability depends on campaign type and subtype; the checked page lists compatibility per format, including Performance Max. Route Performance Max structure and bidding to `$google-ads`.

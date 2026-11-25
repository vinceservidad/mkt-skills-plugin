# Coding guide for voice-of-customer mining

## Codes

Tag every snippet with one code. Add a second code only when the snippet clearly carries two.

| Code | The customer is telling you… | Typical signal words |
| --- | --- | --- |
| Pain | what hurts now | "every time", "again", "can't", "nightmare", "gave up" |
| Desire | the outcome they want | "I just want", "finally", "wish", "would love" |
| Fear | what they are afraid will happen | "worried", "what if", "nervous", "scared" |
| Objection | why they hesitated or left | "too expensive", "not sure", "cancelled because" |
| Trigger | the moment they started looking | "when", "after", "the day", "that's when" |
| Outcome | the result they got (or didn't) | "now I", "since", "saved", "stopped" |
| Alternative | what they used or compared | brand names, "before", "instead", "DIY", "spreadsheet" |
| Identity | who they see themselves as | "as a…", "people like me", "for someone who" |

## Extraction table

Use this table for the full extraction in `work/02-customer/02-voc-mining-`:

| # | Source ID | Date | Who | Rating | Code | Verbatim snippet | Theme |
| --- | --- | --- | --- | --- | --- | --- | --- |

The columns:
- **Who:** one of customer, prospect, churned, lost or unknown.
- **Rating:** fill it only when the source has one.
- **Verbatim snippet:** exact words. Use `…` for cuts and `[ ]` only for a word you must add for sense. The quote check treats bracketed words as yours and does not look them up in the source.

## Counting rules

- Count items, not snippets. One review that complains about price twice counts once for that theme.
- Count each source separately, then total. Report `n` per source, for example "price: 3 of 15 reviews, 9 of 29 lost deals".
- Some sources already carry category counts, such as a support tool's tags. Use those numbers and say they are the source's own tags, not your coding.
- Under three items is an anecdote. Keep it if it is vivid, but label it.

## Source bias

| Source | Skews toward | Correct by |
| --- | --- | --- |
| Public reviews | extremes; happy customers prompted to review | reading 2–4 star reviews first |
| Support tickets | problems, operations | separating product pain from delivery or billing pain |
| Testimonials | praise, selected by you | using them for outcomes and language, not frequency |
| Sales-call notes | prospects' objections, filtered by the rep's memory | preferring verbatim lines over the rep's summary |
| Forums and Reddit | enthusiasts and complainers | noting who the poster is (expert, beginner) |
| Surveys | what people say, not what they do | weighting answers about past behaviour |

## Privacy

Remove:
- names and handles, of people and of pets;
- emails and phone numbers;
- order or ticket numbers that link to a person;
- employer names for individuals;
- addresses.

Replace them with a role or ID: `Customer (R07)` or `Owner, 12-person studio (I-01)`. Keep the date.

## Language bank

Lift phrases a customer would recognise as their own:
- Repeated two- to six-word phrases: "afford this hire", "ran out on Tuesday".
- Their word for the problem, for the result and for the alternative.
- Metaphors they use: "a little course in a box".
- Words they never use that appear in your own copy (record them as "Their words, not ours").

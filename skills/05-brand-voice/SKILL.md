---
name: 05-brand-voice
description: Define the brand voice, tone by context, and words to use and avoid, from brand and customer evidence. Use for tone of voice, voice guide, how we should sound. Not for writing copy (use 10-*).
metadata:
  section: "05 Brand"
---
# Brand voice

Voice is the brand's personality in words: it stays the same everywhere. Tone is how that voice adjusts to the moment: a sales page, a support reply and an apology for a mistake sound like the same person in different moods. A voice is useful when a new writer can pick it up and sound right without asking, so it needs concrete rules, words, and before-and-after examples from the business's real copy, not adjectives.

## Needs (read before writing)

- Required (drafted or confirmed, with content): `context/brand.md` → **Brand foundation**, written by `05-brand-foundation` (personality, archetype, values, promise).
- If present, also read:
  - `context/customer.md` → **Voice of customer** (`02-voc-mining`), the buyer's own words, and ICP and personas;
  - `context/message.md` → Big idea, Promise, Message house;
  - `context/brand.md` → Distinctive assets (taglines and lines to keep) and Naming;
  - `inputs/`: current copy samples (website, emails, templates, posts), founder writing, reviews.
- If Brand foundation is missing:
  - **The customer evidence for it exists** (`customer.md` → ICP and personas is present): run `05-brand-foundation` first, then continue.
  - **It doesn't:** stop. Name the missing section, `brand.md` → Brand foundation, and its owner `05-brand-foundation`, plus `customer.md` → ICP and personas and `02-icp-persona` if that is missing too. Ask for customer evidence and copy samples. A stop reply writes nothing and still ends with the **Principle, framework, source** block.
- Voice of customer missing? Continue, but say the words-to-use list rests on the founder's and business's own writing until `02-voc-mining` runs.

## Process

Use [references/voice-guide.md](references/voice-guide.md).

1. **Derive the voice from the foundation.** Turn the archetype, personality and values into three or four voice traits, each written as *we are X, not Y* (for example *direct, not blunt*). Every trait traces to a foundation slot.
2. **Place it on the four tone dimensions** (Nielsen Norman Group): funny ↔ serious, formal ↔ casual, respectful ↔ irreverent, enthusiastic ↔ matter-of-fact. Give each a position and a reason.
3. **Audit the current copy**, if samples are supplied. Quote the actual lines that break the voice (jargon, hype, vague claims, generic category phrases, passive excuses) and those that already sound right. Keep the founder's own best lines as the model.
4. **Words to use** come from the customer's language (voice of customer, reviews) and the business's own best lines, with source IDs. **Words to avoid** come from the audit and from category clichés that competitors share (only with a dated source for any competitor claim), with the reason and a replacement.
5. **Tone by context.** For each context the business actually has (sales pages, discovery or sales emails, onboarding, support replies, bad news and apologies, review replies, social posts), state how the tone shifts on the dimensions and give one rule. In bad news and apologies, the voice owns the mistake, says what happened and what happens next, and promises only what the business can do.
6. **Before and after.** Rewrite two to four real lines from the samples into the voice. A rewrite changes how something is said, never what is promised or done: add no claims, numbers, guarantees, response times or offers, and no process or behaviour the business hasn't described (who replies, where an update will be posted, how to flag urgency, what the team will do next). An apology may own the mistake, but any next step it names must come from the sources. Where the line needs a fact or a step, write a bracketed placeholder such as *[next step: owner to confirm]* instead of inventing one. Re-read each *after* line and mark every phrase not traceable to a source.
7. **Check before saving.** Re-read the draft against the Checks and fix any failure. Run the quote check below.

**Nothing the context doesn't support.** The voice describes how the brand speaks; it does not create promises. No invented customer phrases, service levels, competitor wording or results. Mark inferences `(assumption)`.

## Output

Write `context/brand.md` → `## Voice`, replacing that section's body and leaving every other section exactly as it was:

```markdown
## Voice
Status: draft (<YYYY-MM-DD>, 05-brand-voice)
Written by: 05-brand-voice, <YYYY-MM-DD>
Built from: <Brand foundation status; Voice of customer status; copy samples>
Voice traits: <we are X, not Y — foundation slot it comes from> (3–4)
Tone dimensions: funny–serious <position, why> · formal–casual <…> · respectful–irreverent <…> · enthusiastic–matter-of-fact <…>
| Context | Tone shift | Rule |
| --- | --- | --- |
Words to use: <word or phrase — source>
Words to avoid: <word or phrase — why — use instead>
Before and after:
- Before: "<exact line>" (<source>) → After: *<rewrite>* <(fact to confirm) if any>
Lines to keep: <the business's own lines that already sound right, with source>
Evidence: <files and IDs>
Method: Voice and tone; four dimensions of tone of voice (Nielsen Norman Group); voice traits from the brand foundation
```

In the *before* line, quote only the exact source text. Every *after* line and every rule you write goes in italics or plain text, never in quotation marks. Never set `confirmed` unless the user approves.

Then update the file:
- In the frontmatter, set `status: draft` and `updated: <date>`.
- Append one line to `## Change log`.

**Quotation marks are evidence.** Quotation marks hold only words that appear exactly in a source (copy samples, reviews, interviews), with the source named. Before saving, run [scripts/check_quotes.py](scripts/check_quotes.py) on the file (`python3 <this skill's folder>/scripts/check_quotes.py context/brand.md`). For every line it prints, copy the exact words or drop the quotation marks and use italics, then run it again until it reports every quotation matches.

Reply with:
- the voice in one line (*we are X, not Y*);
- the biggest change from the current copy;
- the next skill: `10-copy-editing` to apply it to existing copy, or `10-page-copy` for new pages.

End with the **Principle, framework, source** block:

```markdown
**Principle:** …
**Framework:** …
**Source:** …
```

## Checks

- [ ] Each voice trait is written as *we are X, not Y* and traces to a Brand foundation slot.
- [ ] All four tone dimensions have a position and a reason.
- [ ] Tone by context covers the contexts the business actually has, including bad news or apologies, with one concrete rule each.
- [ ] Words to use come from customer language or the business's own lines, with sources; words to avoid have a reason and a replacement.
- [ ] Rewrites change wording only: no new claims, numbers, guarantees, response times, offers, processes or next steps; anything needed but unsourced is a bracketed placeholder for the owner.
- [ ] Quotation marks hold only exact source words, and `check_quotes.py` reports clean. No unmarked inference.
- [ ] Only `## Voice` changed. It has Status, Evidence and Method lines, and the change log has a line for this write.

## Principle and source

Voice is the brand's personality in words and stays constant; tone flexes with the moment; both are built from the brand foundation and the customer's own language, and neither may promise what the business doesn't do. Four dimensions of tone of voice (Kate Moran, Nielsen Norman Group); voice and tone guides (Mailchimp Content Style Guide); The Complete Marketing System, section 5 Brand (Servidad, 2026).

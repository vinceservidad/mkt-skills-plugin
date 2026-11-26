---
name: 10-ad-copy
description: Write ad copy across paid channels as testable variants matched to awareness. Use for Google, YouTube, Meta, TikTok, LinkedIn, Pinterest, Reddit, X, Amazon or native ads. Not for UGC.
metadata:
  section: "10 Copywriting"
  covers: "SLAP"
---
# Ad copy

An ad interrupts someone who wasn't looking for you, so it must speak to what they already know and give one reason to click. Ad copy is matched to the audience's awareness and the platform's limits, and built as variants that test one idea at a time, using only the claims the offer and proof can keep.

## Needs (read before writing)

Required (drafted or confirmed, with content):
- `context/message.md` → **Promise**, from `08-message-doc`.
- `context/awareness.md` → **Awareness map**, from `03-awareness-map`.
- `context/offer.md` → **Core offer**, from `07-offer-design`.
- If present, also read `context/awareness.md` → Traffic temperature and `context/customer.md` → Voice of customer; `context/message.md` → Proof stack and Message house; `context/offer.md` → Price and model, Guarantee, and Urgency and scarcity.
- If a required section is missing:
  - **The upstream evidence exists:** run the skill that fills it first, then continue. If that skill is not loaded, stop and say: enable mkt-q1-audience; enable mkt-q2-offer.
  - **It doesn't:** stop. Name every missing section with the skill that fills it (Promise → `08-message-doc`; Awareness map → `03-awareness-map`; Core offer → `07-offer-design`), and what the user should bring. Do not write copy on an invented offer, promise or proof. A stop reply still ends with the **Principle, framework, source** block.

## Process

1. **Set the platform, the audience and its temperature,** and the landing page or offer the click goes to. Job-title or interest targeting without a retargeting/customer list is **cold** traffic (even on LinkedIn); route cold traffic to content, a checklist or a lead magnet, never straight to an offer/booking hard sell.
2. **Check the current formats, native tone and limits** for the platform before writing. Limits and policies change, so use the user's ad account or the platform's current help pages. [references/ad-formats.md](references/ad-formats.md) covers all 14 paid channels (Google Search, PMax/Demand Gen, Microsoft/Bing, YouTube, Meta, TikTok/TikTok Shop, LinkedIn, Pinterest, Reddit, X, Snapchat, Amazon/Marketplaces, Native and Display) and lists what to confirm. If you can't verify a limit, mark it "to confirm". Match each platform's native tone (for example visual-search phrasing on Pinterest, skeptical practitioner tone on Reddit, 5-second skip-proof hooks on YouTube, strict policy-safe headlines on Amazon).
3. **Write variants by angle.** Within an angle, variant *b* repeats variant *a* except for strictly **one** element, and the file names that single element (*b changes: hook* — never two elements such as *CTA and destination*). Give one temperature per audience (cold, warm or hot), not a range. Write three to five angles from the message house and objections (outcome, problem, mechanism, proof, identity), with two or three variants each. Change one element at a time, so a test teaches something. Shape each ad with SLAP (Stop, Look, Act, Purchase) as in [references/ad-formats.md](references/ad-formats.md), and label the parts of each ad with their stage (*Stop:* the hook, *Look:* the line that holds attention, *Act:* the call to action, *Purchase:* what happens after the click) so the structure is visible.
4. **Keep every claim honest.** Comparatives (*better*, *best*, *fresher*) need proof in the context or they go. On Meta, NEVER assert or ask about the reader's personal attributes, work setup, or situation (for example *Are you struggling with…*, *If you WFH…*, *Working from home?*, *Moving off grocery-store beans?*); speak about the product, the craft or the idea in third person instead. Then: real offer terms only, no invented numbers, testimonials or scarcity, and nothing that breaks the platform's ad policies (for example, personal-attribute targeting language on Meta).
   Write nothing in the copy that the context doesn't support: no illustrative guidance, no generalisations such as *many people* or *most customers*, and no delivery terms, timings or conditions beyond what `offer.md` says. If the copy needs it, put it under Open questions instead.
   Present each source as what it is: two lines from one review are one customer, never *one customer… another said…*.
5. **Recommend the first test:** which variants, and the metric that decides it, passed to `18-creative-testing`.
6. **Run the Anti-AI second pass** in [references/anti-ai-check.md](references/anti-ai-check.md): name the reader, fix the 6 whole-piece rules (max 4 items per sentence list, one point one proof, exact platform terms) and all 13 sentence issues (0 em dashes, no mid-sentence bold, no buzzwords, no "It's not X, it's Y", no rhetorical setups), and reread once as the reader. Preserve every qualifier and exact condition from `context/` or `inputs/` when editing (for example, never drop "on paper" or compress a qualified source fact into a broader claim).
7. **Check before saving.** Re-read the draft against the Checks and fix any failure.

## Output

Write `work/10-copywriting/10-ad-copy-<YYYY-MM-DD>.md`. When you write more than one the same day, add `-<slug>` after the date, for example `work/10-copywriting/10-ad-copy-2026-11-13-<slug>.md`:

```markdown
# Ad copy: <what it is for>
Skill: 10-ad-copy · Date: <YYYY-MM-DD> · Awareness level: <level> · Framework: <name>
Built from: <context sections used, with their status (draft or confirmed)>
## Copy
<the copy>
## Claims and proof
| Claim in the copy | Proof or source |
| --- | --- |
Format limits used: <field — limit — verified where, or 'to confirm'>
Variants: <angle — a vs b — the one element that changes>
First test: <variants, metric>
## Principle, framework, source
```

Change nothing in `context/`. Copy is a deliverable, not a decision.

**Quotation marks are evidence.** In the copy, quotation marks hold only words that appear exactly in a source, such as a testimonial from the proof stack or a review in `inputs/`, with its source in the claims table. Do not wrap your own headlines or lines in quotation marks. Before saving, run [scripts/check_quotes.py](scripts/check_quotes.py) on your file (`python3 <this skill's folder>/scripts/check_quotes.py work/10-copywriting/<file>.md`). For every line it prints, copy the source's exact words or drop the quotation marks, and run it again until it reports every quotation matches.

Reply with the file path, the key choice made (structure, angle or level) and what is still missing, then end with the same block.

End with the **Principle, framework, source** block:

```markdown
**Principle:** …
**Framework:** …
**Source:** …
```

## Checks

- [ ] The platform, audience temperature, awareness level and landing destination are stated, and the copy fits them.
- [ ] Format limits are either verified against current platform documentation or the account, or marked "to confirm". None is stated from memory as current.
- [ ] Variants are grouped by angle and differ in one element at a time.
- [ ] The Anti-AI second pass in `references/anti-ai-check.md` (reader check, 6 whole-piece rules, 13 sentence fixes with 0 em dashes, and final reread) is completed.
- [ ] Every claim is in the claims table with a source. No invented numbers, testimonials or scarcity, and nothing likely to breach ad policy.
- [ ] Quotation marks hold only exact source words, and `check_quotes.py` reports clean.
- [ ] No file in `context/` changed.

## Principle and source

An ad must meet the reader where their awareness is and give one honest reason to click; write angles as testable variants, one change at a time. Tested Advertising Methods (John Caples); levels of awareness, Breakthrough Advertising (Eugene Schwartz); The Complete Marketing System, section 10 Copywriting (Servidad, 2026).

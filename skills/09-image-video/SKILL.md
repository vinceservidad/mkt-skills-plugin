---
name: 09-image-video
description: Direct or generate image and video assets that carry the message and the brand's assets. Use for image or video direction, AI image prompts, shot lists, storyboards, visual concepts.
metadata:
  section: "09 Creative Strategy"
  covers: "Image and video generation; Short-form video; Vampire Video check (Reeves)"
---
# Image and video

A visual has one job: carry the message to someone who will look for a second. Visual hierarchy decides what the eye sees first, second and third, so the message, the product and the brand cue should be those three. Images and videos also make claims: a smiling "client", a dashboard with numbers on it or a before-and-after is evidence in the viewer's eyes, so it must be true.

Save the direction as a Markdown file in `work/09-creative-strategy/` when the required inputs are present. Creating this deliverable is part of the task. If an image or video generation tool is available in the session and the user asks for renders, generate them into `work/09-creative-strategy/` too and list each file; otherwise write the prompts and shot list. Complete the file and its checks before replying with its path.

## Needs (read before writing)

Required (drafted or confirmed, with content):
- `context/message.md` → **Promise**, from `08-message-doc`.
- If present, also read `context/brand.md` → **Distinctive assets** (from `05-distinctive-assets`), Brand foundation and Voice; `context/message.md` → Big idea, Mechanism, Proof stack, Story; `context/awareness.md` → Awareness map, Voice of customer, ICP and personas; `context/offer.md` → Core offer; `work/09-creative-strategy/09-ad-creative-*.md`, `work/09-creative-strategy/09-creative-brief-*.md`, `work/09-creative-strategy/09-hooks-*.md`; brand asset files or inventories in `inputs/`.
- Distinctive assets missing? Continue, but say the brand cues are not decided: use only assets the inputs show in use (as observations, with any inconsistencies named), invent no logo, palette, font or mascot, and suggest `05-distinctive-assets`.
- If the Promise is missing:
  - **The upstream evidence exists** (customer and offer context to build it from): run `08-message-doc` first, then continue.
  - **It doesn't:** stop. Name the missing section, `message.md` → Promise, and its owner `08-message-doc`, and ask for evidence, not a description. Write nothing. A stop reply still ends with the **Principle, framework, source** block.

## Process

For the named methods this skill owns, see [references/methods.md](references/methods.md).

Use [references/visual-direction.md](references/visual-direction.md) for visual hierarchy, short-form video structure, prompt anatomy and the truth rules, and [references/visual-classics.md](references/visual-classics.md) for Reeves's Vampire Video check, Bernbach's visual-verbal complement, and Ogilvy's photo and caption rules.

1. **Fix the asset:** what it is (static ad, carousel, Reel, YouTube short, LinkedIn video, product photo), the channel, the awareness level and the one message it carries (from the promise, a concept in `work/09-creative-strategy/09-ad-creative-*.md` or a brief).
2. **Visual hierarchy:** state what the eye must see first, second and third, and the reading order of any text. One focal point.
3. **Brand cues:** the distinctive assets to use (colour codes, wordmark, spoken line, recurring format), exactly as `brand.md` or the inputs record them. Where the inputs show inconsistency (two colours in use), name it and pick none on the brand's behalf: flag it for `05-distinctive-assets`.
4. **For video, the storyboard:** scene by scene with seconds, what is seen, said and shown as on-screen text, and the hook in the first scene. Captions for sound-off. Specs (aspect ratio, length, safe zones) come from the platform's own current documentation with the URL and date checked, or *to confirm*.
5. **For stills, the shot or render direction:** subject, setting, composition, light, text overlay (exact words, set separately from any generated image), crops needed.
6. **Generation prompts** (when AI generation is wanted): one prompt per asset, with subject, style, composition, lighting, aspect ratio and exclusions. Overlay real text and real data afterwards rather than asking a model to render them.
7. **Truth rules:** no generated or staged person presented as a real customer, client or employee; no fabricated screenshots, dashboards, reports or numbers; no before-after that isn't a real, typical case; real customers, staff or places only with consent. Use a clearly labelled sample (built from a dummy business) instead. Disclosure of AI-generated or altered media follows the law and the platform's current rules: say it is *to confirm*, never state the rule from memory. Rights: stock, music, fonts and likenesses need a licence; no other brand's logo or trade dress.
8. **Check before saving.** Re-read the draft against the Checks and fix any failure.

**Nothing the context doesn't support.** Write no results, numbers, testimonials, prices, deadlines, offers or features in any visual or overlay that aren't in `context/` or `inputs/`. No generalisations about buyers in your own lines, including in payoffs and frequency words (*most owners*, *many people*, *everyone*, *so often*, *usually*, *always*), unless a source counts them; say it about the evidence instead (*10 of 12 closed deals*) or mark it `(assumption)`. Mark inferences `(assumption)` and list what is needed under Open questions.

## Output

Write `work/09-creative-strategy/09-image-video-<YYYY-MM-DD>-<slug>.md`:

```markdown
# Image and video: <asset and channel>
Skill: 09-image-video · Date: <YYYY-MM-DD> · Framework: Visual hierarchy; short-form storyboard
Built from: <context sections and inputs used, with their status>
Status: draft direction; nothing published
Message: <the one message — source>
## Visual hierarchy
1st: … · 2nd: … · 3rd: …
## Brand cues
<asset — as recorded where — or "not decided: distinctive-assets missing">
## Storyboard (video)
| Scene | Seconds | Seen | Said | On-screen text |
| --- | --- | --- | --- | --- |
## Stills and shot list
## Generation prompts
## Truth and rights checks
<what is real, what is a labelled sample, consent and licences needed, disclosure to confirm>
## Specs to confirm
<field — value — verified where, or "to confirm">
## Open questions
## Principle, framework, source
```

Change nothing in `context/`. Visual direction is a deliverable, not a decision.

**Quotation marks are evidence.** Quotation marks hold only words that appear exactly in a source (a review, a tagline in the inputs, a line in the proof stack), with the source named. Overlay text, voice-over and prompts you write go in plain text or italics. Before saving, run [scripts/check_quotes.py](scripts/check_quotes.py) on your file (`python3 <this skill's folder>/scripts/check_quotes.py work/09-creative-strategy/<file>.md`). For every line it prints, copy the source's exact words or drop the quotation marks, and run it again until it reports every quotation matches.

Reply with the file path, the key visual decision, and what is still missing, then end with the same block.

End with the **Principle, framework, source** block:

```markdown
**Principle:** …
**Framework:** …
**Source:** …
```

## Checks

- [ ] One message per asset, and the visual hierarchy names what is seen first, second and third.
- [ ] Brand cues come from `brand.md` or the inputs as recorded; none invented; inconsistencies flagged, not resolved on the brand's behalf.
- [ ] Video storyboards give seconds, seen, said and on-screen text, with the hook first and captions.
- [ ] No fabricated customer, result, screenshot or before-after, and no unsourced generalisation about buyers in overlays or voice-over; samples are labelled; consent and licences named.
- [ ] Platform specs and AI-disclosure rules are cited with a dated first-party source or marked *to confirm*.
- [ ] Quotation marks hold only exact source words, and `check_quotes.py` reports clean.
- [ ] No file in `context/` changed.

## Principle and source

A visual carries one message in the order the eye reads it, uses the brand's own cues every time so it is remembered, and shows only what is true. Visual hierarchy and short-form video, The Complete Marketing System, section 9 Creative Strategy (Servidad, 2026); Vampire Video check, Reality in Advertising (Rosser Reeves); visual-verbal complement (Bill Bernbach); distinctive brand assets, How Brands Grow (Byron Sharp); Ogilvy on Advertising (David Ogilvy).

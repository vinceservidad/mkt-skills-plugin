---
name: 05-reputation
description: Monitor and manage reputation, review replies and crisis statements as drafts for approval. Use for bad reviews, negative posts, backlash, PR crisis, what to post about an incident.
metadata:
  section: "05 Brand"
  covers: "Crisis communications; Reputation management"
---
# Reputation

Reputation is what people say about the brand when it isn't in the room, and it follows behaviour more than words. Managing it is a loop: listen in the places buyers talk, triage what you hear, reply well, fix the cause, and learn. A crisis is the same loop under time pressure, where the order matters: facts first, the people affected before the public, legal review alongside the words, and only statements the business can stand behind later.

## Needs (read before writing)

- Nothing upstream is required. If present, read:
  - `context/brand.md` → Brand foundation (`05-brand-foundation`: promise, values) and Voice (`05-brand-voice`: tone for bad news and review replies);
  - `context/offer.md` → Guarantee and Core offer (what the business has actually promised);
  - `context/message.md` → Proof stack (what is proven);
  - `context/customer.md` → Voice of customer.
- The material: reviews and ratings exports, mentions, comments, incident notes, the business's own logs (sent logs, close logs, support tickets), any existing crisis plan, who can approve public statements.
- If Brand foundation or Voice is missing, continue, and say the replies use a neutral, respectful tone until `05-brand-voice` sets the voice.
- **No material?** If no reviews, mentions or incident notes are supplied, stop and ask for them. Do not write the Reputation section or any reply from a description; invent no reviews, ratings, mentions or incidents. You may save a monitoring plan to `work/05-brand/`. A stop reply still ends with the **Principle, framework, source** block.

## Process

Use [references/reputation-playbook.md](references/reputation-playbook.md).

1. **Take stock.** Count reviews and ratings by source with [scripts/tally.py](scripts/tally.py) (`python3 <this skill's folder>/scripts/tally.py inputs/<file> --count '★+☆*'` for star strings, or the CSV mode); never count by eye. Note themes with item IDs, which reviews have replies, and what is monitored today and by whom.
2. **Listening plan.** Name the sources where this business's buyers talk (from the evidence), who checks each, and how often. A written plan is *designed*, not running: never say monitoring is active unless a tool or person is confirmed doing it.
3. **Triage.** Sort each item: praise, fair complaint, factual error, suspected fake or non-customer, legal or safety issue, potential crisis. Check each against the business's own records (logs, CRM) before replying.
4. **Replies.** Draft replies to the items that need one, in the brand's voice:
   - Thank, address the specific point, own what is true, say what changes, move details to a private channel.
   - Never confirm private client information or details in public. Whether the reviewer is or isn't a client, and what your records show about them, is private too: never write *we can't find a record of you* or *you were never a client*.
   - Offer no refund, credit, discount or guarantee in public unless the offer and the owner already commit to it. If a guarantee may apply, flag it for the owner to confirm privately.
   - Never argue, accuse, or offer anything in exchange for changing or removing a review. A suspected fake review gets a neutral reply that invites contact without mentioning your records, and a report through the platform's own process; check that platform's current review policy before relying on it (not verified here).
5. **Fix the cause.** Route the operational problem behind repeated complaints to the owner of the fix (operations, product, offer). Reputation repairs follow behaviour, not wording.
6. **Earn more reviews honestly.** Ask every customer, not only happy ones; no incentives that require a positive review, no gating, no fake or employee reviews. Consumer-protection rules on reviews vary by country and change; ask the owner to confirm the current rules with legal before launching a review-request programme.
7. **Crisis** (an incident that harms or could harm customers, or that is spreading in public). Apply Situational Crisis Communication Theory (Coombs):
   - **Facts:** list what is confirmed from the business's own records separately from what is unknown or reported by others. Never fill a gap with a plausible explanation. Copy dates and times exactly as the record gives them (*2026-10-06, 07:02*); never infer a weekday, time or date from a product or email name, and never compute a weekday yourself. Do not say *one-off*, *fixed* or *nothing else affected* until the records show it.
   - **Crisis type and responsibility:** victim, accident, or preventable. A preventable incident needs a *rebuild* response (accept responsibility, apologise, correct, compensate where the owner decides), not denial or diminishing.
   - **Order:** stop the harm and preserve records; tell the directly affected parties privately before any public statement; get legal and insurance review in parallel for anything touching personal or financial data, safety, contracts or regulation (this skill does not decide legal obligations); name who approves every statement.
   - **Private messages drafted too:** write the actual wording, for the owner to approve, of every private message the order calls for: to each directly affected party, and to anyone who received something in error (asking them to delete it, not to forward it, and to confirm). A step that says *ask them to* without draft wording is incomplete.
   - **Holding statement:** what happened (confirmed only), what we are doing, what affected people should do, when the next update comes. Set an update cadence and keep it.
   - **After-action:** a review of what failed and the fix, without hindsight bias.
8. **Approval.** Every reply and statement is a draft for the owner. Nothing is posted, sent or published by this skill.
9. **Check before saving.** Re-read the draft against the Checks and fix any failure. Run the quote check below.

**Nothing the material doesn't support.** No invented reviews, ratings, mentions, incident facts, legal conclusions, platform policies, compensation or response times. Mark inferences `(assumption)`.

## Output

1. Write `context/brand.md` → `## Reputation`, replacing that section's body and leaving every other section exactly as it was. This is the standing policy:

```markdown
## Reputation
Status: draft (<YYYY-MM-DD>, 05-reputation)
Written by: 05-reputation, <YYYY-MM-DD>
Current state: <counts by source and rating, from tally.py; themes with IDs; replies so far; what is monitored today>
Listening plan (designed, not yet running): <source — who checks — how often>
Triage and reply rules: <category — what to do — who approves>
Escalation: <what counts as a potential crisis — who is told — within how long (owner to set)>
Crisis playbook: facts first · affected parties privately before public · legal and insurance review in parallel · approver · holding statement · update cadence · after-action
Open incidents: <incident — status — next step> or none
Causes to fix: <complaint theme — owner of the fix>
Review requests: <ask everyone, no gating, no incentives for positive reviews; legal check of current rules before launch>
Evidence: <files and IDs>
Method: Reputation management loop (listen, triage, reply, fix, learn); Situational Crisis Communication Theory (Coombs)
```

2. Save reply drafts, crisis statements and the private messages to affected parties to `work/05-brand/05-reputation-<YYYY-MM-DD>-<slug>.md`, each marked **Draft — not posted; needs the owner's approval**, with the facts each draft relies on and their sources.

Never set `confirmed` unless the user approves. Then update the file: in the frontmatter, set `status: draft` and `updated: <date>`, and append one line to `## Change log`. If `context/brand.md` does not exist, create it with frontmatter, the five brand sections (others `Status: empty`) and a change log.

**Quotation marks are evidence.** Quotation marks hold only words that appear exactly in a source (a review, a post, incident notes), with the source named. Your drafted replies and statements are your words: present them as drafts under a heading or in italics, never inside quotation marks. Before saving, run [scripts/check_quotes.py](scripts/check_quotes.py) on each file you wrote (`python3 <this skill's folder>/scripts/check_quotes.py <file>`). For every line it prints, copy the exact words or drop the quotation marks, and run it again until it reports every quotation matches.

Reply with:
- the most urgent item and the recommended first action;
- what the owner must decide or approve (and anything legal must review);
- the file paths;
- the next skill: `16-reviews` for a review-request programme, or `05-brand-voice` if no voice exists.

End with the **Principle, framework, source** block:

```markdown
**Principle:** …
**Framework:** …
**Source:** …
```

## Checks

- [ ] Counts come from `tally.py`; every theme cites item IDs; nothing is counted by eye.
- [ ] The listening plan is labelled *designed*; no monitoring is described as running unless confirmed.
- [ ] Replies reveal no private client information, argue with no one, and offer no refund, discount or guarantee the owner hasn't committed to.
- [ ] Suspected fake reviews are handled neutrally, with no public accusation; platform policies are not asserted as current fact.
- [ ] In a crisis, confirmed facts and unknowns are separate; affected parties are told privately before any public statement; legal and insurance review is flagged; the approver is named; no *one-off* or *nothing else affected* claim before the records show it.
- [ ] Every private message the crisis order calls for (to affected parties, to anyone asked to delete something) has draft wording for the owner to approve.
- [ ] Every reply and statement is marked as a draft needing the owner's approval; nothing is posted or sent.
- [ ] Quotation marks hold only exact source words, and `check_quotes.py` reports clean. No unmarked inference.
- [ ] Only `## Reputation` changed in `context/`. It has Status, Evidence and Method lines, and the change log has a line for this write.

## Principle and source

Reputation follows behaviour: listen where buyers talk, reply with facts and respect, fix the cause, and in a crisis tell the truth you can confirm, to the people affected first, with legal review alongside. Reputation management; Situational Crisis Communication Theory (W. Timothy Coombs, Ongoing Crisis Communication); The Complete Marketing System, section 5 Brand (Servidad, 2026).

---
name: 02-jobs-to-be-done
description: Map the jobs customers hire a product to do, with forces of progress and a before-after grid. Use for what people pay for, why they switch or stay, JTBD. Not for objections (use 02-buyer-psychology).
metadata:
  section: "02 Customer"
  covers: "Before–After grid; Jobs to Be Done"
---
# Jobs to be done

People don't buy products; they hire them to make progress in a specific situation. A job explains why a buyer switched, what they compared, and what "better" means to them. That is what the awareness map, the offer and every headline need, and why demographics alone mislead.

## Needs (read before writing)

- `context/customer.md`, with at least one of these present (drafted or confirmed, with content):
  - **Research log**, written by `02-customer-research`;
  - **Voice of customer**, written by `02-voc-mining`.

  Also read Pains, desires and fears; Current alternatives; and Buying triggers and process.
- `context/customer.md` → ICP and personas, from `02-icp-persona`, if present. Map the jobs of the target buyer, and note any job that differs by role.
- When both Research log and Voice of customer are missing:
  - **Raw material supplied** (interviews, call notes, reviews or tickets in `inputs/` or the conversation): run `02-customer-research` or `02-voc-mining` on it first, then continue.
  - **Nothing supplied:** stop. Name the missing sections and those skills. Say that switching interviews with recent buyers are the best material, and do not write jobs from imagination. End the reply with the **Principle, framework, source** block (see Output), even when you stop.

## Process

1. **Find the struggling moments.** These are the situations that made people look: the triggers and the "last time" stories in the evidence. List each with the source IDs.
2. **Write job statements.** Use the form "When [situation], I want to [motivation], so I can [expected outcome]." Keep the product out of the statement; the job exists whether or not you do.
3. **Split the dimensions.** For each core job, cover:
   - **Functional:** the task.
   - **Emotional:** how they want to feel, or stop feeling.
   - **Social:** how they want to be seen.

   Mark emotional and social jobs not voiced in the evidence `(assumption)`.
4. **Map the forces of progress.** Give evidence for each force, or write "unknown":
   - **Push:** of the current situation.
   - **Pull:** of the new solution.
   - **Anxiety:** of the new; this is what stops them.
   - **Habit:** of the present; this is what keeps them.

   Switching happens when push plus pull outweigh anxiety plus habit.
5. **List the competing solutions.** Include everything hired for the same job: other products, DIY, a person, a workaround, and doing nothing. This is the real competitive set.
6. **Write desired outcomes.** Phrase them as measurable outcome statements in the customer's terms, such as *minimise the time to know whether we can afford a hire* (Ulwick). They are your wording, so write them without quotation marks, even when they echo a buyer's question. Rank them by how often they appear and how poorly they are served today.
7. **Build the before–after grid.** Have, feel, average day and status, before and after. Write it in customers' words where possible: copy the exact fragment as it appears in the source (from "it just turns up before I run out", quote "turns up before I run out", never "a delivery that turns up before I run out"), or paraphrase it without quotation marks. To shorten a quote, cut words from its ends; never swap or add a word, not even an article. See [references/jtbd-guide.md](references/jtbd-guide.md).

## Output

Write `context/customer.md` → `## Jobs to be done`, replacing that section's body and leaving every other section exactly as it was:

```markdown
## Jobs to be done
Status: draft (<YYYY-MM-DD>, 02-jobs-to-be-done)
Written by: 02-jobs-to-be-done, <YYYY-MM-DD>
Core job: When <situation>, I want to <motivation>, so I can <outcome>. — <evidence>
Functional: … · Emotional: … · Social: … (each with evidence or (assumption))
Struggling moments: <situation — evidence>
Forces: push <…> · pull <…> · anxiety <…> · habit <…>
Competing solutions hired for this job: <…, including doing nothing>
Desired outcomes (ranked): <outcome statement — frequency — how well served today>
Before → after: have <…→…> · feel <…→…> · average day <…→…> · status <…→…>
Evidence: <files and IDs>
Method: Jobs to Be Done (Christensen; Ulwick outcome statements; Klement forces of progress); Before–After grid (DigitalMarketer)
```

Your own labels, outcome statements and assumptions go without quotation marks; quotation marks hold only words copied exactly from a source. Never set `confirmed` unless the user approves.

Then update the file:
- In the frontmatter, set `status: draft` and `updated: <date>`.
- Append one line to `## Change log`.
- If `context/customer.md` does not exist, first copy [assets/customer.md](assets/customer.md) to `context/customer.md`, then write your section into it.

Reply with:
- the core job in one sentence;
- the strongest force against switching;
- the next skill: `03-awareness-map`, or `02-buyer-psychology` for the anxieties.

End with the **Principle, framework, source** block:

```markdown
**Principle:** …
**Framework:** …
**Source:** …
```

## Checks

- [ ] Job statements are solution-agnostic (no product or feature named) and tied to a situation with evidence.
- [ ] Functional, emotional and social jobs are separated. Unvoiced ones are marked `(assumption)`.
- [ ] All four forces are present, each with evidence or "unknown". Anxiety and habit are not skipped.
- [ ] Competing solutions include non-product options (DIY, a person, doing nothing) where the evidence shows them.
- [ ] No unmarked inference: any statement about buyers that the evidence does not state (a motive, a habit, a frequency word such as "often" or "most", which group an unlabelled review came from, a rate for a channel the notes don't give) carries `(assumption)` or is left out.
- [ ] Quotation marks hold only words copied exactly from a source (no added or moved words). Paraphrases, inferences, labels and suggested questions go without quotation marks (use italics for a suggested question).
- [ ] Desired outcomes are measurable and ranked from evidence, not opinion.
- [ ] Only `## Jobs to be done` changed. It has Status, Evidence and Method lines, and the change log has a line for this write.

## Principle and source

People hire a product to make progress in a specific situation, and they switch only when the push of the present and the pull of the new outweigh their anxiety and habit. Jobs to Be Done, Competing Against Luck (Clayton Christensen); outcome-driven innovation (Tony Ulwick); forces of progress, When Coffee and Kale Compete (Alan Klement); Before–After grid (DigitalMarketer); The Complete Marketing System, section 2 Customer (Servidad, 2026).

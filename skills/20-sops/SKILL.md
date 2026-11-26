---
name: 20-sops
description: Turn a repeated marketing process into an SOP. Use for marketing SOPs, playbooks, designer or freelancer brief templates, brand guidelines, production pipeline. Not for non-marketing SOPs.
metadata:
  section: "20 Operations"
  covers: "Agency and freelancer management; Brand guidelines; Creative production pipeline; SOPs / playbooks"
---
# SOPs and playbooks

An SOP writes down a process that has already worked, so it can be repeated without the founder and improved each time. It works when it comes from what actually happened at least twice, lists steps with an owner, timing and an example, puts checks at the points where things went wrong before, and includes the briefs and standards (brand guidelines, freelancer briefs, a production pipeline) that hand-offs need. It fails when it documents an ideal process nobody runs, is too long to use, has no owner, or freezes a process before it has worked.

Save the SOP as a Markdown file in `work/20-operations/` when the required inputs are present. Creating this deliverable is part of the task, including requests worded as a question. Complete the file and its checks before replying with its path.

## Needs (read before writing)

No context section is required: this skill works from the data in `inputs/`. Notes about how the process ran in `inputs/` are the evidence.
- If present, also read `context/brand.md` → Voice, Distinctive assets; process notes, past briefs, timelines and results in `inputs/`; any work in `work/20-operations/20-campaign-review-*.md`.
- **No data:** When `inputs/` has no process or operations notes at all, ask which process has run at least twice and what happened the last two times, explicitly say how to provide the notes (drop files in `inputs/` or paste into chat), and give the SOP template only. Write nothing until it arrives. A stop reply still ends with the **Principle, framework, source** block.

## Process

For the named methods this skill owns, see [references/methods.md](references/methods.md).

Use [references/sops-guide.md](references/sops-guide.md) for SOP structure, checks at failure points, freelancer briefs, brand guidelines and the creative production pipeline.

1. **Has it worked twice?** From `inputs/`, the runs, their results and what differed; if the requested process has not run twice, save a labelled draft checklist in `work/20-operations/`, say it is not yet an SOP, ask what happened when it was tried, and invent no steps or results.
2. **Steps.** In order, each with an owner, timing (days before launch), an input, an output and an example from the runs.
3. **Checks at failure points.** Where past runs went wrong (from `inputs/` or `20-campaign-review`), a check before moving on.
4. **Creative production pipeline.** Brief → draft → review → final → publish, with who does each, turnaround and where files live.
5. **Agency and freelancer management.** A brief template (goal, audience, message, format, deadline, budget, examples), how work is reviewed and paid, and who approves.
6. **Brand guidelines.** The minimum standards the SOP needs (voice, logo, colours, photo style) from `context/brand.md` or marked *to define*.
7. **Owner and review.** Who keeps the SOP, when it is reviewed, and how changes are logged.
8. **Approval.** The SOP is a draft. Adopting it, briefing freelancers or changing how the team works needs the owner's explicit approval.
9. **Check before saving.** Re-read the draft against the Checks and fix any failure.

**Nothing the context doesn't support.** Write no steps, timings, results or brand rules that aren't in `context/` or `inputs/`. Unknown items are *to define*. Mark inferences `(assumption)` and list what is needed under Open questions. Count from files with [scripts/tally.py](scripts/tally.py) or [scripts/sum_by.py](scripts/sum_by.py), never by eye. No third-party benchmark is evidence about this business.

## Output

Write `work/20-operations/20-sops-<YYYY-MM-DD>-<slug>.md`:

```markdown
# SOP: <process, business>
Skill: 20-sops · Date: <YYYY-MM-DD> · Framework: SOPs / playbooks with a creative production pipeline, freelancer briefs and brand guidelines
Built from: <context sections and inputs used, with their status>
Status: draft for the owner's approval
## Runs this is based on
## Steps
| # | Step | Owner | When | Input → output | Example |
| --- | --- | --- | --- | --- | --- |
## Checks
## Production pipeline
## Freelancer brief template
## Brand standards needed
## Owner and review
## Claims and sources
| Claim or number | Source |
| --- | --- |
## Open questions
## Principle, framework, source
```

Change nothing in `context/`. The deliverable is a draft, not a decision.

**Quotation marks are evidence.** Quotation marks hold only words that appear exactly in a source, with the source named. Write your own lines, and the titles of books, essays or talks (including in the Principle, framework, source block), in italics or plain text, never in quotation marks. Before saving, run [scripts/check_quotes.py](scripts/check_quotes.py) on your file (`python3 <this skill's folder>/scripts/check_quotes.py work/20-operations/<file>.md`). For every line it prints, copy the source's exact words or drop the quotation marks, and run it again until it reports every quotation matches.

Reply with the file path, the steps with owners and timing, the checks added where past runs failed, and the freelancer brief, and what is still missing, then end with the same block.

End with the **Principle, framework, source** block:

```markdown
**Principle:** …
**Framework:** …
**Source:** …
```

## Checks

- [ ] The SOP rests on at least two real runs, or is labelled a draft checklist.
- [ ] Each step has an owner, timing, input, output and an example.
- [ ] Checks sit where past runs went wrong.
- [ ] The production pipeline, freelancer brief and brand standards are included or marked *to define*.
- [ ] The SOP has an owner and a review date; nothing is adopted without approval.
- [ ] Quotation marks hold only exact source words, and `check_quotes.py` reports clean.
- [ ] No file in `context/` changed.

## Principle and source

Write down what has worked twice, put checks where it broke, give every step an owner, and keep it short enough to use. SOPs / playbooks, Creative production pipeline, Agency and freelancer management and Brand guidelines, The Complete Marketing System, section 20 Operations (Servidad, 2026); The E-Myth Revisited (Michael Gerber).

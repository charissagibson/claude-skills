---
name: session-close
description: "Close a working session with a handover that actually lands: living documents updated as verified full replacements, a change record, a decision register coded by stakeholder, the policy, procedure, work instructions and audit document kept current, a backlog or register update, the user-only actions written as exact text, and a next-session prompt. Use whenever a session created, changed or retired something (a file, document, process, system, decision or plan); whenever the user says handover, doc pass, documentation pass, wrap up, update the docs, update the backlog, record this, or asks what needs documenting; whenever a session is closing and decisions were taken in chat that exist nowhere else; and when asked to check a regenerated document against its original.  Also use when the user says 'run next session prompt' at the start of a session: it finds and follows the current prompt. Trigger even if the user never says the word: a session that changed something and is about to end needs one."
---

# Session close

## The failures this exists to prevent

Writing the handover is not the hard part.  **Landing it is.**  Five failures recur:

1. **Proposed, never applied.**  The next session inherits the items as "owed", and the debt compounds.
2. **Recorded where nobody has to act on it.**  An item written into a shared document, when the fix actually lived in a setting only the user could change, gets raised again and again and actioned never.  Recording something where nobody has to act on it is the same as not recording it.  Separate what you can update from what only the user can do, and hand the latter over as exact text, not as a description of the problem.
3. **Retyped instead of copied.**  Producing a "full replacement" by retyping a long document from memory quietly paraphrases the 90% that wasn't meant to change.  The losses surface months later.  See *Step 6*.
4. **A blocker repeated instead of re-checked.**  Once an item is said to be blocked, the same deferral gets restated every time it comes up.  When the user raises an item a second time, re-derive the reasoning from scratch.
5. **A save that never happened.**  A session reports that it saved a file, and the file isn't there.  You can't always tell from inside a session where a write landed.  **The folder listing is the evidence, never the report.**

## First, establish where the documents live and who can write them

This decides the shape of the whole pass, so settle it first.

- **Writable by you** (a local folder, a repo, a connected drive): write in place, with the same copy-and-patch and verification discipline.  Show the diff instead of a handover list.
- **Read-only to you** (uploaded project knowledge, a wiki, a shared drive you can't write): produce complete replacement files for the user to swap in.  The pass isn't done until they confirm it landed.

Never imply you've updated a document you can't write.  If it's ambiguous, ask once.

**Don't settle for read-only until you've tried for write access.**  List the folders you can actually reach.  If the one holding the documents isn't there, ask for access.  A cached or synced copy is not the source of record; if both exist, the real folder wins.

**Project instructions are writable when they're a file you can reach** (a `CLAUDE.md` in Claude Code): baseline, patch and show the diff like any other document.  They're read-only only where they live outside your reach (uploaded project knowledge, a hosted settings page); then every fix is a handover (*Step 9*).  Personal settings stay the user's to change.

**The project instructions are also the charter.**  They say what's being created, the goals, the RACI, and the stakeholders the project serves, each with a short code (for example GL, CC and AP for three finance areas).  If the stakeholders and their codes aren't recorded yet, establish them with the user at the start and write them in, because the decision register (*Step 3*) files by them.  Read every document the instructions name as governing (a policy, a procedure, a register, the audit document); each one is in scope for the pass.  On a shared project, the charter also lists the people and the shared prompts folder (*Step 13*).

**If several people run handovers on the same project**, agree one writer for the backlog or register, so concurrent sessions don't overwrite each other.  Everyone else raises items for that writer (*Step 7*).  For a solo project, skip this.

## Read completely, at the start

Read the project record (instructions, notes, backlog, previous handover) at the **start** of the session, not at the end.  A session that hasn't read the record re-derives settled decisions and proposes things already ruled out.

- A narrow lookup can search to the relevant section.  A document read for its rules, and any document you're about to patch, is read in full.
- If a document is too long for one read, read it in consecutive chunks and confirm the chunks meet and the last one reaches the end.  Gaps go unnoticed until they cause damage.
- List the folder before assuming a filename.  Synced or cached files are often truncated or renamed.

## Leave room for it

A handover squeezed into the last minutes of a long session goes wrong, because that's when steps get compressed.  Raise it before the session is spent.  If there isn't room for all of it, say so and let the user choose what to drop.

## Step 1: inventory, then sort by destination

List what the session actually did: things created, changed or retired; decisions taken; facts proven; errors found; items found already closed.

Then sort by **who reads it and who acts on it**:

| Bucket | Destination | Who reads | Who acts |
|---|---|---|---|
| Facts, decisions, evidence, conventions | Living documents | Both | You (write or hand over) |
| Changes to how something is built or run | Change record | Both | You |
| Decisions, judgement calls, things abandoned or retired, outside approvals | Decision register | Both | You |
| Changes to how a process runs | Policy, procedure, work instructions, audit document | Both | You (write or hand over) |
| Open items nobody owns yet | Backlog or register | User | Say plainly that nobody owns it |
| Repeated corrections, looping, behaviour fixes | Instruction replacements | **Claude only** | User, always |
| State the next session needs | Next-session prompt | **Claude only** | You |
| Anything else only the user can do | Numbered handover list | User | User |
| Working files, exports, superseded copies | Retirement list | User | User |

The user-only buckets are the ones that decay.  A setting only they can change, an access request, a decision from someone else, an approval: each needs **the exact replacement text or the exact action**.  "The wording is stale" fails.  "Replace the paragraph under *Setup* with this block: ..." works.

**Don't hand over what you can write yourself.**  A document in a folder you can reach is your job, not an item for the user's list.

## Step 2: record the change, and its baseline

For anything that changed how something is built or run: what changed, what it was before, what it is now, why, who approved it, the evidence, and how to reverse it.

- **The "before" can't be reconstructed later.**  Capture it while it still exists.  If it's gone, say the baseline wasn't captured rather than describing it from memory.  File it in the baseline folder (*Step 6*) and cite the baseline's path in the change record.
- **Evidence means comparison with what came before**, not confidence in the new version.  Where there's nothing to compare against, state the test for "correct" before running it, and record it with the result.
- **Say whether a check was one-off or standing.**  A one-off test is dropped after use; its result is permanent.  Otherwise the next session can't tell a retired check from a lost one.
- **Segregation of duties.**  Where one person specified, built, approved and now runs something that feeds a reported figure, say so once, plainly.  Skip this for anything that reaches no reported number.

## Step 3: log the decisions, by type and by stakeholder

The reasoning is the first thing a session loses.  The change record says what changed; the decision register says why, and what was decided against.  Without it, abandoned ideas come back as new ones and judgement calls can't be defended.

- **Log** any choice between alternatives that a later session, a reviewer or an auditor would need the reason for, and anything abandoned, retired or approved by someone outside the session.  Routine edits aren't decisions.
- **Every entry has an ID: type, stakeholder code and number.**  `JC-CC01` is the first judgement call for the stakeholder coded CC.  Numbering runs per type and stakeholder.  A decision for the whole project uses a project-wide code agreed in the charter.
- **Default types.**  A project can add its own; record them in the charter.

| Type | For | Must also record |
|---|---|---|
| `DEC` | A decision: a choice between options | The options considered |
| `JC` | A judgement call: a conclusion where the evidence or the standards leave room | The basis, and what would change it |
| `ABN` | Something abandoned | Why, so it isn't proposed again |
| `RET` | Something retired | What replaced it, if anything |
| `APR` | An approval given by someone outside the session | Who, when, and where the approval is evidenced |

- **Every entry records** the date, what was decided, who decided or approved it, the evidence, and the IDs it supersedes or is superseded by.
- **The register is append-only.**  A reversal is a new entry that names the one it reverses; the old entry stays, marked superseded.
- **File it where the charter says.**  If the charter doesn't say, propose one register file for the project, get it approved, and record its location in the charter.

## Step 4: keep the documentation layers and the audit document current

A process change isn't finished when the system works.  The people running it work from the policy, the procedure and the work instructions, and an outside party works from the audit document.

- **For any change to how a process runs, check each layer:** policy, procedure, work instructions.  Update the ones you can write.  For the rest, hand over the exact text, or raise a backlog item with an owner.  Never leave a layer silently behind the system.
- **The audit document is built as the project goes, and is complete at project close.**  It's the one document an external party (an auditor, a reviewer, a new owner) needs, so each handover adds what the session changed instead of leaving it to be written from memory at the end.  Default contents: scope and goals from the charter, the RACI, the change record, the decision register, each control with its evidence, sign-offs, and anything still open at close.
- **Alongside it, keep a policy and a work instruction for every user involved,** written for the people who'll run it, not the people who built it.
- **At project close, check the audit document against the change record and the register:** every change and every decision appears, and every piece of evidence it cites exists.

## Step 5: choose the method per document, and say which you used

- **Content changes throughout:** full replacement by copy-and-patch.  The default.
- **Append-only documents** (logs, per-session blocks): still a full replacement, built by copying the original and appending.  Don't hand over a separate block to paste; it competes with the real document later.
- **Generated documents** (inventories, counts, exports): patch only facts this session actually proved.  Don't update generated figures from memory; mark them as not refreshed.
- **Derived documents** (summaries, one-pagers, anything produced from the record): regenerate at the end, after the record is settled.  Never edit them by hand, and never in the middle of the pass.
- **Superseded documents:** never patch.  They're the record of what was believed then.

If the method can't be met, say so in one sentence and let the user decide.  If the user has already chosen full replacement, don't argue it again.

## Step 6: build by copy-and-patch

Never retype a document to replace it.  Copy it exactly, apply only exact replacements, and refuse to write unless every patch matches exactly once.

```python
import io, sys
src, out = "<baseline copy>", "<destination>"
patches = [  # anchor text -> replacement; note is for the report only
    {"note": "header -> today", "old": "Last updated: ...", "new": "Last updated: ..."},
]
original = io.open(src, encoding="utf-8").read()
text, fails = original, []
for i, p in enumerate(patches, 1):
    n = text.count(p["old"])
    if n != 1:
        fails.append((i, n, p.get("note", p["old"][:70])))
    else:
        text = text.replace(p["old"], p["new"])
if fails:
    for i, n, what in fails:
        print(f"patch {i}: matched {n}x (need exactly 1) | {what}")
    sys.exit("PATCH VALIDATION FAILED - nothing written")

# optional, for append-only documents:
# text = text.rstrip("\n") + "\n\n---\n\n" + new_block.strip() + "\n"

o, n_ = original.split("\n"), text.split("\n")
changed = [(i + 1, o[i]) for i in range(len(o)) if i >= len(n_) or o[i] != n_[i]]
print(f"lines changed: {len(changed)} | bytes {len(original.encode())} -> {len(text.encode())}")
for ln, c in changed:
    print(f"  line {ln}: {c.strip()[:110]}")
if len(original.encode()) == len(text.encode()):
    print("!! byte count unchanged - check src and out are not the same file")
io.open(out, "w", encoding="utf-8").write(text)
```

- A patch matching zero times means the anchor is wrong or the document has moved on.  Matching twice means something unintended is about to change.  Both stop the write, and stopping is correct.  Don't hand-edit the output to compensate.
- **Baseline every file before you change it, and file the baseline.**  Copy the untouched file into the project's baseline folder, under the date and the file's own path (for example `_baselines/2026-11-02/docs/policy.md`), then patch from there to the destination.  Never edit a baseline.  Reading and writing the same path destroys the baseline and makes Step 10 incapable of failing.
- **The baseline folder is named in the charter.**  If it isn't, propose one, get it approved and record it.  It sits outside anything published or pushed.  Baselines are kept until project close, because the change record and the audit document cite them as the "before".
- When a patch adds or removes lines, a line-by-line comparison reports everything after it as changed.  Count changed blocks, not lines.
- Where version control exists, commit the untouched original first.
- In Claude Code, the Edit tool's exact-match replacement gives the same guarantee for small changes.  Use the script when there are many patches or the file is large.
- **Where a spreadsheet is the record**, patch the target row, copy the formatting from the row above, then re-open the saved file and confirm the sheets and row counts survived.  If the file is generated by a script, rebuilding is cheaper than repairing; say so.

## Step 7: the backlog or register

Open items carry an **owner** and either a **trigger** (when it becomes actionable) or a **review date** (when someone checks), ideally both.  A trigger with no review date sits forever.

**Closure is one of three claims, and the entry says which:**
- **Approved:** a person decided.
- **Proven:** evidence collected, stated inline, dated.
- **No longer relevant:** the honest one.  Without it, dead items stay open looking alive.

Close on evidence without asking, as long as the evidence is in the entry.

- **Cap the open list.**  Past roughly fifty live items, adding one means closing or dropping one.  Say so when a cap is exceeded rather than quietly appending.
- **Check new items against closed ones too.**  A settled item re-raised as a fresh idea is failure 2 again.  The same goes for blockers: before saying work is frozen, check the item that froze it isn't already closed.

**If the project has more than one writer** (see *First, establish*): non-writers don't open the register.  Write one intake file per item into the agreed intake folder, append only, with who raised it, a title, what was observed, why it matters and what it concerns.  No id and no status; those are set at triage.  Then **list the folder** and report what it shows.  A filename missing from the listing means the item wasn't raised.  The register writer lists the intake folder at the start of each session, writes the rows and moves the files to `processed/`.

## Step 8: generated and leftover files

Working files, exports, old drafts and superseded copies pile up, and they aren't harmless.  Claude reads what's present, not what's current, so a stale copy in a folder is a source of wrong answers.

- Spot candidates by age, names outside the convention, and files nobody can state a purpose for.  Candidates, not verdicts.
- **Never delete anything yourself.**  List each one with a reason and a recommendation; the user acts.  Prefer archiving to deleting.
- **Record the decision, including "keep, this is the live one"**, so the same files aren't flagged every time.
- Don't invent a retention period.  Ask whether one exists.

## Step 9: instruction fixes

Where the session showed repeated friction (the user frustrated, or you looping or re-correcting), the fix belongs in the project instructions or a skill, not in this conversation.  Where you can't edit the instructions, this is a handover of the exact replacement text.

Four gates, all of them, before proposing one:

| Gate | Fails when |
|---|---|
| **Recurrence** | It happened once, with no reason to expect it again |
| **Not discoverable** | Reading the project's own documents would have got it right |
| **Generalises** | It governs one instance, not a class |
| **Must be always on** | It needn't be, so it belongs in a skill |

- **Name what each addition retires.**  Instruction files degrade past about two hundred lines, so an addition that only adds damages what already worked.  Hand over the whole replacement block, not a patch; a patch hides growth.
- **Skill or instructions?**  Instructions cost something every turn; a skill costs nothing until it's used.  More than about three lines of procedure wants to be a skill.
- **Keep project values out of portable skills.**  A skill states the rule and names the facts it reads from the project record.  Names, paths and system names in a portable skill are a defect; sweep for them before sharing.
- **Where a skill exists in more than one copy**, update every copy in the same pass and say who needs to re-install it.
- **A declined suggestion comes back next time.**  On the third raising, stop offering it as a tweak and raise it as a finding: either the instructions aren't being read, or the reason for declining should be recorded so it stops coming back.

## Step 10: verify, and distrust a clean result

Read the changed-line report.  Every line should be one you meant to change.

**A perfect result is a reason to distrust the check.**  Identical byte counts after a real edit can't happen; the usual cause is comparing a file with itself.  Check the cheap facts first: are the two paths different files, do their checksums differ, and does the "original" contain text that only exists in the new version?  If so, the baseline is gone and the verification is void.  Say so.

- Where the pass saved or raised anything, **the folder listing is the check.**
- **A check that caught something once runs every time, and you say it ran.**
- **If a verification tool fails twice, stop and report** what's unproven and how the user can check it.

## Step 11: don't replace before the diff

Whenever the user is the one swapping files in, say it every time:

> Don't replace the document until the diff is done.  Once it's replaced, the original is gone and the new version can't be checked against anything.

If it's already been replaced, say so and ask whether an earlier copy exists: version history, a download, an earlier conversation.

## Step 12: close with a handover, not a summary

1. **One complete file per document**, named as the document is named, or the diff you applied where you could write.
2. **The method used**, and the verification behind it.
3. **The user-only list**, numbered, with exact text and exact actions.
4. **What's genuinely outstanding**, stated as outstanding, not as nearly done.
5. **Leftover working files to delete**, so they can't compete with the documents later.
6. **The model that ran the session**, in one line.
7. **Items raised or saved**, with filenames exactly as the listing showed them, or "none" so nothing-raised can be told apart from not-checked.
8. **Decision register entries added**, by ID, or "none".
9. **Documentation layers and the audit document:** which were updated, and which are owed and by whom.

Then confirm it was applied.  **Never call something ready while a defect you've already named is still in it.**  Fix it, or say it's the one thing blocking.

User-only items still not actioned by the next handover go onto the backlog as dependencies: what's needed, from whom, and what it holds up.

## Step 13: the next-session prompt

Written for Claude to read, not a person.  It's the only thing that reaches the next session before it starts work.

**First ask: what should the next session focus on?**  Offer options from the backlog and the change record, and always include *continue this topic while it's fresh*.

Then include:

| Include | Note |
|---|---|
| What to read, **in full** | Begin by reading, then set the starting point |
| What the session is for | From the answer above |
| Which backlog items are next, **in sequence or in priority** | Different claims; don't merge them |
| Big items separately from small admin | Batch the admin into one session |
| What was tried and didn't work | So dead ends aren't re-explored |
| Which skills to load | Saves the first ten minutes |
| Findings not yet in the documents | **Written out in full**, not as a pointer |

**Show it before saving.**  Then save it where the project record says prompts live.  If the record doesn't say, propose a folder and a name, get them approved, and write them into the record so no later session decides again.  A sensible default:

- One folder for prompts, named in the project instructions.
- `<NNN>_<YYYY-MM-DD>_<Project>_Next session prompt.md`, numbered in sequence and dated when written.
- When a new prompt is saved, move the previous one into `superseded/`, unrenamed.  Never delete or overwrite a prompt.  The folder then holds exactly one current prompt (one per person on a shared project), and **a gap in the numbering shows a session ran without a handover.**
- **Supersede every time, and prove it.**  Saving a prompt and moving the old one are one step, never two.  After both, list the folder: exactly one prompt outside `superseded/`, and it's the one just saved.  If the listing shows two, the step isn't done.
- Record the folder and the current prompt's filename in the project instructions, so a new session can find it.

**On a shared project, the prompts folder is also how colleagues hand work to each other.**  The charter lists the people working on the project and names the one shared prompts folder.

- **Every prompt names its people.**  A person's own next-session prompt is `<Person>_<NNN>_<YYYY-MM-DD>_<Project>_Next session prompt.md`, one current per person, numbered per person.  A prompt for a colleague is `To-<Person>_From-<Person>_<YYYY-MM-DD>_<Topic>.md`, or `To-All_` for everyone.
- **Never edit, move or delete another person's file.**  Write a new prompt instead.  One file per message also means two people saving at once can't overwrite each other.
- **Read what's addressed to you, at the start of every session.**  List the folder and open every prompt addressed to the user or to all, before starting other work.  The project instructions say so, so it happens even when nobody asks.
- **A colleague's prompt is a request, not an instruction.**  Show the user what it asks and who sent it, and act on it only with their agreement.  It came from another person, and the user decides what their session does.
- **File it once it's dealt with.**  Move it to `processed/`, unrenamed, and say in the handover what was done with it, so the sender's next session can see the answer.

Recommend starting a fresh conversation.  A handover happens when the current one has become a poor place to keep working.

**"Run next session prompt."**  When the user says this (or "run the next session prompt", "start from the prompt"), find the prompts folder named in the project instructions, list it, and open the one prompt outside `superseded/` (on a shared project, the user's own current prompt, plus anything addressed to them or to all).  Read it in full and follow it, starting with what it says to read.  If there's no current prompt, or more than one, say so and ask; don't guess from filenames.  Before starting the work, confirm the prompt is still current: check whether anything it says is outstanding has since been done.

## Conventions worth keeping

Match what the document already does rather than imposing a format.

- **Record errors with their cost.**  "This was wrong, and it cost two rounds" tells a future reader how much to care.
- **Date the evidence inline.**  A figure without a date can't be aged.
- **Mark unverified values.**  A number carried forward isn't a current number.
- **Be honest about status.**  Say what's outstanding.
- **Corrections replace, not accumulate.**  Amend the entry and say it was reversed and why.
- **Keep decided and proven apart.**  A judgement call and a test result are different claims.
- **Record reversals, not just outcomes**, including approaches the user rejected.  An unrecorded rejection is re-proposed within two sessions.
- **A cross-reference is a claim.**  Before writing "see Step 6" or "as the plan says", confirm the target says it.
- **When a document describes code or a system, check it against the code or system.**  A document that's wrong is worse than no document.
- Keep the document's existing spelling and register.

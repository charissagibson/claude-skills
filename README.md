# claude-skills

Skills I've written for Claude: the working methods I use when I direct AI to build finance systems.  A skill is a set of instructions Claude loads when a task calls for it, so the method shows up every time instead of me repeating it.

I'm an accountant, not a software engineer.  These came out of real working sessions.  I noticed where things kept going wrong, decided what the rule should be, and wrote it up with Claude.  Then I checked every line against what had actually happened.

## handover

The main one.  Writing a handover at the end of an AI session is easy.  Landing it is the hard part.

I kept seeing the same five failures:

- fixes proposed and never applied, so the next session inherits them as debt
- items recorded somewhere nobody has to act on them
- "updated" documents retyped from memory, quietly paraphrasing the parts that weren't meant to change
- a blocker restated every session instead of re-checked
- a session reporting it saved a file that isn't there

Most of the answer is what any accountant knows from month-end close.  A change record with the before and after.  Evidence that compares against something, not confidence in the new version.  Open items with an owner and a review date.  Closure that says whether it was approved, proven or no longer relevant.  Segregation of duties called out when one person built and approved something that feeds a reported number.  The rest is about not trusting a clean result: a perfect check is a reason to check the check.

## timezone

A small one.  Calendar connectors often return times in UTC, and Claude will happily show them that way.  This makes Claude detect the local zone each session, convert UTC times, and label the zone it used, so a wrong guess is obvious and easy to correct.  It shows how little a skill needs to be to remove an annoyance that keeps coming back.

## Using them

Copy a skill's folder into `~/.claude/skills/`, or into a project's `.claude/skills/`.  Claude Code picks it up from the description at the top of `SKILL.md`.

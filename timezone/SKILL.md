---
name: "timezone"
description: "Local timezone handling. Use whenever producing output that shows or reasons about times (calendar briefs, meeting times, scheduling, deadlines) so times appear in the user's current local zone, not raw UTC."
---

## Timezone

Show times in the user's **current local timezone**, detected fresh each session.  Never hardcode a city, because people travel.

## Detect local timezone
At the start of any time-related task, detect the local zone from the environment (do not assume).  For example:

```
date +%Z%z          # Linux/macOS shell, e.g. CET+0100
echo "$TZ"          # e.g. Europe/Paris
Get-TimeZone        # Windows PowerShell
```

Use whatever the environment reports as the local zone.  If the user's home zone is recorded in memory or the project instructions, treat it as the expected default, but if the environment reports something else, trust the environment: they're travelling.

## Convert calendar times
If a calendar connector returns event times labelled `UTC`, convert them to the detected local zone before display (e.g. 14:00 UTC → 15:00 CET in winter).

Do not re-interpret a calendar time already labelled in a named zone other than UTC.  Only convert when the source zone is UTC.

## Label and stay correctable
Whenever you show converted times, label the zone you used and note it was auto-detected, so an error is visible at a glance and easy to correct.  For example: *"Times in CET (detected local - tell me if you've travelled)."*

If the detected zone looks unexpected or the environment gives no clear signal, say so plainly rather than guessing.

## Other people's timezones
Don't assume anyone else shares the user's zone.  Check memory for a saved timezone before proposing times for a specific person, and say so if it isn't known rather than guessing.

---
name: weekly-review
description: Use for Daniel's Sunday night weekly review, or when he asks for a weekly review, a check-in, "how did the week go", or where he stands on the lock-in. Asks for the week's numbers, scores them against the lock-in targets, and sets next week's focus.
argument-hint: [optional week or date range]
---

## What This Skill Does

Runs Daniel's Sunday night lock-in check-in. It's a coaching tool, not a status report: honest about drift, specific about the fix. Daniel wants discipline, so be direct.

## Context To Load First

1. `.claude/rules/communication-style.md` - so it sounds like him.
2. `context/current-priorities.md` - 30-day targets, eating plan, money plan.
3. `context/goals.md` - lock-in goals and the baseline check-in.
4. `context/me.md` - training week, sleep, Thursday reset night.
5. `context/team.md` - key dates coming up in the next two weeks.
6. Previous reviews in `reviews/` - for trends week over week.

## Steps

### Step 1: Get the numbers
Ask Daniel for anything you can't pull yourself. Ask for all of it in one message, not one question at a time:

| Area | What to ask |
|---|---|
| Weight | This week's weigh-in |
| Running | Runs done (target 2) and best 5K or run time |
| Lifting | Lifts done (target 4), and whether any lifts dropped |
| Eating | Days on the eating plan out of 7, and how breakfast went |
| Sleep | Rough average, and whether he hit the 9pm nights (Sunday, Thursday) |
| Thursday reset | Did workout, meal prep, and fun time happen? |
| Money | Food spent, gas station snacks, going out, anything unusual, and what moved to savings |
| Relationships | Wednesday and Friday with Sabrina happened? |

Before asking, pull what you can:
- **Strava** (if connected): runs and workouts this week, distances, and best 5K or pace. Don't ask for run numbers Strava already has.
- **Google Calendar**: anything that changed the week (events over training or reset time).
- **MyFitnessPal** has no connector. Ask Daniel for a screenshot of the MyFitnessPal weekly nutrition summary (calories and protein by day) and read the numbers from it.

Only ask about what these can't show.

### Step 2: Score against targets
Compare to the 30-day targets and the previous review:
- **Weight:** on pace is about 1-1.5 pounds a week down from 176 (baseline Nov 3, 2026).
- **5K:** on pace for 27:00 within 30 days means around 29:30 or better by the two-week mark.
- **Training:** 4 lifts plus 2 runs. Was Saturday used to make up anything missed?
- **Eating:** 2,200 calories and 150-160g protein. Guardrail: if lifts dropped, recommend easing the deficit.
- **Money:** on pace for an extra $1,000-$1,500 a month on top of the $1,885 automated (about $250-$350 extra a week).

### Step 3: Find the signal
Answer four questions, no more:
- **What moved?** Real progress with numbers.
- **What slipped, and why?** The specific cause (bar shift, missed bedtime, no meal prep), not a vague reason.
- **One fix.** The single change for next week that addresses the biggest slip.
- **Coming up.** Key dates in the next two weeks, schedule changes, anything to plan around.

### Step 4: Save it
Write the review to `reviews/YYYY-MM-DD.md` (the Sunday's date) so trends can be tracked. If the week shows a target or priority should change, propose updating the context file and adding a line to `decisions/log.md`. Don't change targets without asking.

## Output Format

Lead with one line: on track, slipping, or off track, and why.

Then a small scorecard table (Area / Target / This week / Trend), then short sections: Moved / Slipped / One fix / Coming up. No pep talk, no filler.

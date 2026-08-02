# Time & Work — Remaining Variants
### The Last 2–5%: Rarer TCS Digital Phrasings + Extra Trigger-Word Tricks

Your first three booklets (`01-fundamentals`, `02-fast-tricks-and-shortcuts`,
`03-question-pattern-catalog`) cover essentially all high-frequency TCS Ninja + Digital Time & Work
questions. This file adds the small remainder: ten less-common variants and seven trigger-word
tricks that occasionally show up, mostly on the Digital-level paper. Treat this as a short top-up,
not a new foundation — every method below still reduces to the core ideas in `01-fundamentals.md`.

---

## Category K — Rare But Seen Variants

### K1. Working for x Days, Then Leaving
> *"A can finish a job in 20 days. A works for 6 days and then leaves. B finishes the remaining work
> alone in 21 days. In how many days can B alone finish the whole job?"*

**Method:** Completed work → remaining work → solve. A's 6-day share = `6/20 = 3/10`; remaining =
`7/10`. If B does that `7/10` in 21 days, B's full-job time = `21 / (7/10) = 30` **days**.

### K2. Working Together, Then One Leaves
> *"A and B together can finish a job in 8 days. They work together for 5 days, then A leaves. B
> finishes the rest alone in 6 more days. In how many days can B alone do the whole job?"*

**Method:** Joint work → remaining work → single worker. Combined rate = `1/8`; 5-day joint share =
`5/8`; remaining = `3/8`. B does `3/8` in 6 days ⇒ B's full-job time = `6 / (3/8) = 16` **days**.

### K3. Fraction of Work Completed by Each Person
> *"A completed 3/5 of a work in 12 days, then left. B completed the remaining work in 6 days. Find
> the time each would take to complete the full work alone, and the time taken if they had worked
> together from the start."*

**Method:** Scale each person's fraction up to a full job first — A: `12 / (3/5) = 20` days alone; B:
`6 / (2/5) = 15` days alone. Then combine as usual: together = `(20×15)/(20+15) = 60/7` days.

### K4. Reduced Efficiency Due to a Mid-Job Slowdown
> *"A can finish a job in 15 days working normally. After 5 days, A starts working at half the usual
> efficiency for the rest of the job. How many total days does A take?"*

**Method:** Split into two phases with two different rates — normal rate first, halved rate second;
don't try to average the rates. First 5 days at `1/15`/day complete `1/3`; remaining `2/3` at half
rate (`1/30`/day) takes `20` more days ⇒ **Total = 25 days**.

### K5. Repeating Break / Rest Cycle
> *"A works for 5 days and rests on the 6th (repeating). A alone can finish a job in 24 days of actual
> work. How many total days (including rest days) will the job take?"*

**Method:** Treat the rest day as adding to the calendar, not to the work — the 24 *working* days
still need `24/5 = 4.8` → 4 full 6-day cycles (24 working + 4 rest days = wait, recompute per cycle)
cover `4 × 5 = 20` working days in `4 × 6 = 24` calendar days; 4 working days remain, needing 4 more
calendar days ⇒ **Total = 28 calendar days**. Always separate "days worked" from "days elapsed" for
this variant.

### K6. Machine Breaks Down and Is Repaired
> *"A machine can complete a job in 12 hours. It runs for 3 hours, then breaks down and is under
> repair for 2 hours (doing no work), then resumes until the job is finished. How long does the whole
> job take, start to finish?"*

**Method:** Split into phases exactly like a pipe/machine problem, but insert a zero-work phase for
the downtime. Work done in first 3 hours = `3/12 = 1/4`; remaining `3/4` at the same rate needs `9`
more running hours ⇒ **Total elapsed = 3 + 2 (repair) + 9 = 14 hours**.

### K7. Wrong Time Assumption / Efficiency-Loss Question
> *"A estimated finishing a job in 10 days at a certain daily rate, but actually took 12 days at a
> lower daily rate. By what percentage did A's actual daily efficiency fall short of the estimate?"*

**Method:** Efficiency is inversely proportional to time (`01-fundamentals.md` §6). Estimated rate ∝
`1/10`, actual rate ∝ `1/12`. Percentage shortfall = `(1/10 − 1/12)/(1/10) × 100 = 16.67%`.

### K8. Workforce Increases by a Percentage (Not Efficiency)
> *"20 workers can complete a job in 18 days. If the number of workers is increased by 20%, in how
> many days will the job be completed?"*

**Method:** `Workers × Days = Constant` (same worker-day logic as `02-fast-tricks-and-shortcuts.md`
§3, applied to headcount instead of a mid-job change). New workers = `20 × 1.2 = 24`; new days =
`(20 × 18)/24 = 15` **days**. Keep this distinct from an *efficiency* increase — here the per-person
rate is unchanged, only headcount changes.

### K9. Unit-Production Phrasing (Bottles, Units, Items per Hour)
> *"Machine A produces 200 bottles per hour, Machine B produces 150 bottles per hour. Working
> together, how long will they take to produce 7000 bottles?"*

**Method:** Identical to a combined-work question — treat "bottles" as the job. Combined rate =
`200 + 150 = 350` bottles/hour; time = `7000 / 350 = 20` **hours**. Don't be thrown by the absence of
the word "work" — any per-unit-time output phrasing (bottles, pages, units, bricks) uses the same
rate-addition method.

### K10. Mixed Skilled / Unskilled Workers
> *"3 skilled workers and 5 unskilled workers can complete a job in 6 days. A skilled worker is twice
> as efficient as an unskilled worker. If 4 skilled workers alone were to do the job, how many days
> would they take?"*

**Method:** Convert every worker to one common unit first. Let unskilled rate = `1` unit/day ⇒
skilled rate = `2` units/day. Combined rate = `3(2) + 5(1) = 11` units/day; total work =
`11 × 6 = 66` units. 4 skilled workers' rate = `4 × 2 = 8` units/day ⇒ time = `66/8 = 8.25`
**days**.

---

## Extra Trigger-Word Tricks

These are quick mental reflexes to pair with the ten variants above — the same "see the word, do the
step" style as `02-fast-tricks-and-shortcuts.md`.

**"...then leaves / then joins" →** Completed work → Remaining work. Never solve the whole job in one
pass; split into phases at the moment the workforce changes.

**"...twice / thrice / half as efficient" →** Convert straight to a rate ratio (`2:1`, `3:1`, `1:2`).
Never convert to a day ratio first — that inversion step is where most errors happen.

**"...every Nth day / alternate days / repeating cycle" →** Think in whole cycles, not day-by-day.
Compute work done per cycle, find how many full cycles fit, then solve only the small leftover.

**"...ratio of times / ratio of days is given" →** Immediately flip it: time ratio and efficiency
ratio are always inverses of each other.

**"25% / 40% / 75%" (any clean percentage) →** Convert to a fraction before touching the arithmetic
(`25% → 1/4`, `40% → 2/5`, `75% → 3/4`). Fractions combine faster than decimals in every one of these
variants.

**All given times are whole numbers →** Default to the LCM Method from
`02-fast-tricks-and-shortcuts.md` §1 — it applies just as well to K3, K9, and K10 as it does to the
core combined-work questions.

**Pipes, machines, or downtime in the same question →** Keep fill/production as `+` and
empty/downtime as a `0`-rate phase, and always track *elapsed time* separately from *working time*
when a repair or rest period is involved (K5, K6).

---

## What This File Deliberately Skips

Per the original review, these remain **not worth prepping for TCS** and are intentionally excluded
here as well: multi-page algebraic worker puzzles, hour-by-hour efficiency changes, irregular
A/B/C/D rotation schedules, infinite pipe on/off sequences, nonlinear efficiency models, and
minimum-time optimization/scheduling problems. These belong to CAT/SSC CGL-level prep, not TCS NQT.

---

## Updated Priority Order

With this file added, the full priority order across all four booklets becomes:

1. **A1** — Two people working together (base formula)
2. **B1** — Efficiency ratio ("X times as efficient")
3. **C1/C2** — Someone joins or leaves midway
4. **K1/K2** — Working for x days then leaving / together-then-one-leaves (same family as C1/C2)
5. **D1** — Men/Women/Children equivalence
6. **E1/E2** — Pipes and cisterns, including a pipe closing partway
7. **F1** — Alternate-day working
8. **K5** — Repeating break/rest cycle (same family as F1)
9. **G1** — Wages split by work share
10. **H1** — Machine/Printer/Robot work
11. **K6** — Machine breaks down and is repaired (same family as H1)
12. **I1** — Percentage of work completed
13. **K3** — Fraction of work completed by each person (same family as I1)
14. **K9** — Unit-production phrasing (bottles/pages/units)
15. **J1/J2** — Variable efficiency
16. **K4** — Reduced efficiency due to mid-job slowdown (same family as J1/J2)
17. **K8** — Workforce increases by a percentage
18. **K10** — Mixed skilled/unskilled workers
19. **K7** — Wrong time assumption / efficiency-loss question (lowest frequency, Digital only)

At this point the coverage is effectively complete for TCS NQT. The highest-value next step is pure
repetition: solve 40–60 mixed questions across all four booklets until each pattern is recognized on
sight, since TCS rewards speed of recognition over depth of math.

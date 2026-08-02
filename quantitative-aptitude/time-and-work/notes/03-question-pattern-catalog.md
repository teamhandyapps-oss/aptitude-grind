# Time & Work — Question Pattern Catalog
### Every High-Yield Phrasing, Grouped by the Trick That Solves It

Time & Work questions look varied, but almost every one of them reduces to a handful of tricks from
`02-fast-tricks-and-shortcuts.md`. This file catalogues the actual **phrasings** you'll meet in TCS
NQT (Ninja + Digital) and similar placement tests, grouped by category, each with the fastest method
and a verified mini-example. Skim this before a test to pattern-match a question to its solution
method in seconds.

---

## Category A — Two (or More) People Working Together

### A1. Direct Combined-Work Question
> *"A can finish a work in 6 days, B in 12 days. In how many days can they finish it together?"*

**Method:** `xy/(x+y)` from `01-fundamentals.md` §3.
**Answer:** `(6 × 12)/(6 + 12) = 4` **days**.

### A2. Three-or-More-Workers Combined Question
> *"A, B, and C can individually finish a job in 12, 15, and 20 days. Working together, how long will
> they take?"*

**Method:** LCM Method (`02-fast-tricks-and-shortcuts.md` §1). LCM(12, 15, 20) = 60 ⇒ rates 5, 4, 3
units/day ⇒ combined rate = 12 units/day ⇒ **5 days**.

---

## Category B — Efficiency Ratio Problems

### B1. "X Times as Efficient" Question
> *"A is thrice as efficient as B. B alone can complete a work in 24 days. Find the time taken by A
> alone, and by A and B together."*

**Method:** Rate-First Thinking (§2). B's rate = `1/24`; A's rate = `3/24 = 1/8` ⇒ A alone = **8
days**; together = `(8×24)/(8+24) = 6` **days**.

### B2. Time-Ratio-to-Efficiency-Ratio Conversion
> *"The ratio of the time taken by P and Q to complete a task is 4:7. What is the ratio of their
> efficiencies?"*

**Method:** Efficiency and time are always inversely proportional (`01-fundamentals.md` §6) ⇒
efficiency ratio = **7 : 4**.

---

## Category C — Worker Joining or Leaving Midway

### C1. Someone Joins Partway Through
> *"A can complete a job alone in 18 days. A works alone for 6 days, then B (who alone takes 9 days)
> joins. How many total days does the job take?"*

**Method:** Completed-work-then-remaining-work split (`02-fast-tricks-and-shortcuts.md` §4). A's
6-day share = `6/18 = 1/3`; remaining = `2/3`; combined rate = `1/18 + 1/9 = 1/6`; extra days needed
= `(2/3)/(1/6) = 4`. **Total = 6 + 4 = 10 days.**

### C2. Workers Leave Partway Through
> *"24 workers can finish a job in 18 days. After 6 days, 6 workers leave. In how many more days will
> the remaining workers finish the job?"*

**Method:** Worker-Day Method (`02-fast-tricks-and-shortcuts.md` §3). Total = `24×18 = 432`
worker-days; done = `24×6 = 144`; remaining = `288`; workers left = 18 ⇒ **16 more days.**

---

## Category D — Men / Women / Children Equivalence

### D1. Given an Equivalence Ratio, Find a Mixed-Group Time
> *"2 men do the same amount of work as 3 women. 2 men alone can finish a job in 12 days. In how many
> days can 4 men and 6 women together finish the same job?"*

**Method:** Convert to a common rate unit first (`01-fundamentals.md` §7). `2 men = 12 days` ⇒ 1 man
= `1/24`; since `2 men = 3 women` in output, 1 woman = `1/36`. Combined rate of `4 men + 6 women` =
`4/24 + 6/36 = 1/6 + 1/6 = 1/3` ⇒ **3 days.**

### D2. Men/Women/Children Together
> *"If 2 men or 4 women or 6 children can complete a job in the same time, how many days will 1 man,
> 2 women, and 3 children together take, given 2 men alone take 12 days?"*

**Method:** Same conversion approach as D1 — every category is first expressed in terms of a single
"man-unit," then rates are added directly.

---

## Category E — Pipes and Cisterns

### E1. Fill and Empty Pipe Together
> *"Pipe A can fill a tank in 8 hours; pipe B can empty it in 12 hours. If both are opened together,
> how long will the tank take to fill?"*

**Method:** Net rate (`01-fundamentals.md` §9). `1/8 − 1/12 = 1/24` ⇒ **24 hours.**

### E2. A Pipe Is Closed Partway Through
> *"Fill pipe A takes 10 hours, outlet pipe B takes 15 hours. Both are opened together, but B is
> closed after 3 hours. How long does the tank take to fill in total?"*

**Method:** Two-phase split (`02-fast-tricks-and-shortcuts.md` §8). Net rate while both open =
`1/10 − 1/15 = 1/30`; work in 3 hr = `1/10`; remaining `9/10` filled by A alone at `1/10`/hr = 9 more
hours ⇒ **Total = 12 hours.**

### E3. Multiple Fill Pipes, One Outlet
> *"Three pipes P, Q, R can fill a tank in 12, 15, and 20 minutes respectively, while an outlet pipe S
> can empty it in 10 minutes. If all four are opened together, will the tank ever fill?"*

**Method:** Sum every inlet rate, subtract the outlet rate (`01-fundamentals.md` §9). If the net rate
is zero or negative, the tank **never fills** — always check the sign of the net rate before
computing a time.

---

## Category F — Alternate-Day Working

### F1. Two Workers Alternate Days
> *"A can complete a job in 10 days, B in 15 days. Working on alternate days, starting with A, in how
> many days will the job be completed?"*

**Method:** Cycle-first method (`02-fast-tricks-and-shortcuts.md` §5). 2-day cycle work =
`1/10 + 1/15 = 1/6`; since `1/6 × 6 = 1` exactly, the job finishes in exactly **12 days** (6 full
cycles), with **no partial final day**.

### F2. Alternate Days With a Leftover Fraction
> *"A can complete a job in 4 days, B in 6 days. Working on alternate days starting with A, how many
> full days pass before the job is finished, and who finishes it?"*

**Method:** Same cycle-first method, but here the cycle work (`1/4 + 1/6 = 5/12`) does **not** divide
evenly into 1 — find how many full cycles fit, then solve the small leftover fraction with whichever
worker's turn comes next (don't assume it always lands on a clean day).

---

## Category G — Wages Based on Work

### G1. Split Payment by Work Contributed
> *"A (10 days alone) and B (15 days alone) work together on a job and are jointly paid ₹1500. What
> is each person's share?"*

**Method:** Wages-by-work-share (`02-fast-tricks-and-shortcuts.md` §7). Rate ratio `A:B = 3:2` ⇒ A
gets `1500 × 3/5 = ₹900`, B gets `1500 × 2/5 = ₹600`.

### G2. Three-Way Wage Split With a Helper
> *"A and B can together do a job in 10 days. With the help of C, they finish it in 6 days. If the
> total payment is ₹3000, how much should C receive?"*

**Method:** Find C's rate by subtraction (`01-fundamentals.md` §5-style difference logic, applied to
a three-person combined rate instead of two), then split wages by rate ratio exactly as in G1.

---

## Category H — Machine / Printer / Robot Work

### H1. Direct Machine-Rate Question
> *"Printer A can print 1000 pages in 5 hours, Printer B can print the same 1000 pages in 8 hours. If
> both print together, how long will it take?"*

**Method:** Identical to a two-worker combined-work question (`01-fundamentals.md` §8) — a machine's
rate is treated exactly like a person's rate. `(5×8)/(5+8) = 40/13` hours.

### H2. Machine Stopped Partway
> *"Machine P can complete a task in 8 hours, machine Q in 10 hours, machine R in 12 hours. All three
> start together, but P is shut off after 2 hours. In approximately how much more time will Q and R
> finish the rest?"*

**Method:** Same two-phase split as E2 — compute work done by all three in the first phase, subtract
from 1, then solve the remainder using only the machines still running.

---

## Category I — Percentage / Fractional Work Completed

### I1. Given a Percentage, Find the Full-Job Time
> *"A can complete 75% of a work in 15 days. In how many days can A alone complete the entire work?
> B then finishes the remaining 25% in 4 days — how many days would B alone take for the full job?"*

**Method:** Scale up directly — if 75% takes 15 days, 100% takes `15 / 0.75 = 20` days for A.
Similarly, B's 25% in 4 days scales to `4 / 0.25 = 16` days for the full job.

### I2. Fractional Work Split Between Two Workers
> *"A can do 40% of a job in a certain time; B does the remaining 60%. If A takes 8 days for their
> share, and A and B have the same efficiency, how long does B take for their share?"*

**Method:** Convert percentages to a work ratio (`40:60 = 2:3`), then scale A's time by that ratio to
find B's time, since equal efficiency means time is proportional to the fraction of work assigned.

---

## Category J — Variable Efficiency (Speed Changes Mid-Job)

### J1. Efficiency Doubles/Triples Partway
> *"Working at a constant rate, A can finish a job in 10 days. A works at the normal rate for the
> first 4 days, then works at double efficiency for the rest. How many total days does the job take?"*

**Method:** Treat this as two separate phases with two different rates, exactly like the two-phase
pipe/machine split in E2/H2. First 4 days at rate `1/10` complete `2/5`; remaining `3/5` at double
rate (`1/5`/day) takes 3 more days ⇒ **Total = 7 days.**

### J2. Efficiency Changes by a Given Percentage
> *"A normally takes 20 days for a job. If A's efficiency increases by 25% starting from day one, how
> many days will A now take?"*

**Method:** Percentage-to-time formula (`02-fast-tricks-and-shortcuts.md` §6). `New Time = 20 ×
100/125 = 16` **days.**

---

## Priority Order for Limited Prep Time

If you're short on time, drill these first — they cover the large majority of what actually appears
in TCS-style placement tests, roughly in order of frequency:

1. **A1** — Two people working together (the base formula everything else builds on)
2. **B1** — Efficiency ratio ("X times as efficient")
3. **C1/C2** — Someone joins or leaves midway
4. **D1** — Men/Women/Children equivalence
5. **E1/E2** — Pipes and cisterns, including a pipe closing partway
6. **F1** — Alternate-day working
7. **G1** — Wages split by work share
8. **H1** — Machine/Printer/Robot work (same math as A1, different wrapper)
9. **I1** — Percentage of work completed
10. **J1/J2** — Variable efficiency (lower frequency, but appears occasionally in TCS Digital)

These ten patterns, combined with the LCM Method and rate-first thinking from
`02-fast-tricks-and-shortcuts.md`, cover almost everything TCS typically asks while avoiding the
low-return, highly complex worker puzzles seen in exams like CAT or SSC CGL.

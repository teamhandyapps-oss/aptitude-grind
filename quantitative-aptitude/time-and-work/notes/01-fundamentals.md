# Time & Work — Fundamentals
### Work, Rate, Efficiency & the Core Formulas

## Why Time & Work Matters for TCS NQT

Time & Work is one of the highest-frequency topics in TCS NQT (Ninja + Digital) Numerical Ability,
alongside Percentages and Ratios. Unlike SSC CGL or CAT, TCS rarely asks difficult algebraic
work-time puzzles — it sticks to **direct formula-based questions with at most 1–2 twists**: ratio
based worker efficiency, pipes & cisterns, alternate working/resting, men-women-children efficiency,
and machine problems. The entire topic rests on one idea: *work, rate, and time are locked together
by a single equation, and almost every question is just that equation applied from a different
angle.*

---

## 1. The Golden Rule

> **Work = Rate × Time**, i.e. `W = R × T`

- **Work** — the total task, conventionally treated as **1 unit** (a whole job) unless stated
  otherwise.
- **Rate** — work done per unit time (also called *efficiency* or *one day's/hour's work*).
- **Time** — days/hours taken.

If total work = 1, then

```
Rate = 1 / Time
```

This single idea solves almost every question in this topic — everything below is a variation of it.

---

## 2. One Day's Work

If **A** finishes a work in `N` days, A's one day's work is `1/N`.

**Example:** A completes a work in 8 days ⇒ one day's work = `1/8`.

The relationship also runs backward: if A's one day's work is `1/15`, then A alone takes **15 days**
to finish the whole job. Time and one-day's-work are reciprocals of each other.

---

## 3. Combined Work — Two Workers

If A finishes a job alone in `x` days and B finishes it alone in `y` days, their combined one-day's
work is `1/x + 1/y`, so together they take:

```
Time (A + B) = xy / (x + y)
```

This formula is extremely common and worth memorizing outright.

**Worked Example:** A = 10 days, B = 15 days.

```
Together = (10 × 15) / (10 + 15) = 150 / 25 = 6 days
```

---

## 4. Combined Work — Three or More Workers

For three workers:

```
Combined one-day's work = 1/x + 1/y + 1/z
```

Take the LCM of `x`, `y`, `z` to add these cleanly (see `02-fast-tricks-and-shortcuts.md` for the
LCM shortcut). For `n` workers, the pattern generalizes — just sum every individual rate.

---

## 5. The Difference Formula (Finding One Worker From a Pair)

If A alone takes `x` days, and A + B together take `y` days, B's one-day's work is:

```
1/B = 1/y − 1/x
```

then invert to get B's number of days.

**Worked Example:** A = 30 days, A + B = 12 days.

```
1/B = 1/12 − 1/30 = 5/60 − 2/60 = 3/60 = 1/20
⇒ B = 20 days
```

This "given one worker + the pair, find the other worker" pattern is one of the most frequently
tested variants of Time & Work.

---

## 6. Efficiency Concept (Very Important)

> **Efficiency ∝ 1 / Time** — higher efficiency means less time, and the two are always **inversely
> proportional**.

If efficiency ratio `A : B = 2 : 3`, then time ratio `A : B = 3 : 2` — always the reverse of the
efficiency ratio.

**Worked Example:** Time ratio `2 : 5` ⇒ efficiency ratio `5 : 2`.

### 6.1 Worker-Ratio Questions — Think in Rates, Not Days

**Example:** "A is twice as efficient as B."

- **Wrong instinct:** guess a number of days for each and check.
- **Right approach:** assume work *rates* directly. Let B's rate = 1 unit/day, then A's rate =
  2 units/day. Never assume days first — assume the rate ratio, since that's what the problem is
  actually telling you.

This single habit — assigning rates instead of days whenever a ratio is given — is the fastest
problem-solving upgrade in this entire topic.

---

## 7. Men, Women, and Children Equivalence

Frequently, a question gives an equivalence like "2 Men = 3 Women" and expects you to convert
everyone into one common unit before adding rates.

**Worked Example:** `2 Men = 3 Women` (in output, i.e. equal work done in equal time)

```
2M = 3W  ⇒  M : W = 3 : 2  ⇒  1 man = 3/2 women (in work output)
```

Always convert every category (men, women, children) into a single common unit of efficiency before
combining rates — treat this exactly like the ratio-to-rate trick in §6.1.

---

## 8. Machine / Printer / Robot / Server Problems

Conceptually **identical** to worker problems — a machine, printer, robot, or server is just another
"worker" with its own rate. No new formula is needed; apply everything above directly.

---

## 9. Pipes and Cisterns

Same core concept, with a sign convention:

| Pipe type | Effect | Rate |
|---|---|---|
| Filling (inlet) | Positive work | `+1/x` (fills in `x` hours) |
| Emptying (outlet) | Negative work | `−1/y` (empties in `y` hours) |

**Both pipes open together:**

```
Net rate = 1/x − 1/y
Time = 1 / Net Rate
```

**Worked Example:** Fill pipe = 8 hr, Empty pipe = 12 hr.

```
Net rate = 1/8 − 1/12 = 3/24 − 2/24 = 1/24
⇒ Time = 24 hours
```

> ⚠️ **Common Mistake:** Adding the empty-pipe rate instead of subtracting it. Always treat outlet
> pipes as **negative** contributions to the net rate.

---

## 10. Worker-Day Concept

Another foundational identity, used constantly for workers joining/leaving problems:

```
Total Work = Workers × Days     (only valid when every worker has equal, constant efficiency)
```

**Worked Example:** 20 workers finish a job in 15 days ⇒ Total work = `20 × 15 = 300` worker-days.

This "worker-days" total is treated as a fixed, conserved quantity — exactly like total work = 1 in
the fractional approach, just scaled up to avoid fractions. See `02-fast-tricks-and-shortcuts.md` §3
for how this is applied to workers-leaving and workers-joining problems.

---

## 11. Wages Are Proportional to Work — Not Time

> **Money ∝ Work Done**, never time spent.

If efficiency ratio is `3 : 5`, wages split in the ratio `3 : 5` — **regardless of how many days
each person actually worked**, as long as they worked together on the same job. This trips people up
constantly because it feels like it should depend on time, but wages track *output*, not *hours
logged*.

---

## 12. Formula Sheet — Quick Reference

| Situation | Formula |
|---|---|
| Work | Rate × Time |
| Rate (one day's/hour's work) | Work / Time = 1 / Time |
| Time | 1 / Rate |
| Combined work (A + B) | `xy / (x + y)` |
| Combined work (n workers) | Sum of all individual rates, then invert |
| Difference formula | `1/B = 1/(A+B time) − 1/(A time)` |
| Pipe filling | `+1/x` |
| Pipe emptying | `−1/y` |
| Efficiency | `1 / Time` (inversely proportional to time) |
| Wages | `∝ Work done`, not time |
| Worker-days | `Workers × Days` (constant total, equal efficiency) |

---

## Key Takeaways

- Everything reduces to **Work = Rate × Time**, with total work usually normalized to 1.
- Time and rate are always **reciprocals**; efficiency and time are always **inversely
  proportional**.
- For ratio-based questions ("A is twice as efficient as B"), assign **rates directly** — don't
  guess at days.
- Wages split by **work contributed**, never by time spent.
- The worker-day identity (`Workers × Days = constant`) is the backbone of every joining/leaving
  problem — see `02-fast-tricks-and-shortcuts.md`.

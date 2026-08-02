# Time & Work — Fast Tricks & Shortcuts
### LCM Method, Worker-Day Tricks, and Every Speed Technique You Need

This file collects the **fast calculation methods** — the actual shortcuts you execute under exam
pressure. For the full catalogue of question *types* that use these tricks, see
`03-question-pattern-catalog.md`.

---

## 1. The LCM Method (Best Trick in the Topic)

Instead of taking total work = 1 and juggling fractions, take total work = **LCM of all the given
times**. Every individual's rate then becomes a clean whole number.

**Worked Example:** Individual times = 10 days, 15 days, 30 days.

```
Total work = LCM(10, 15, 30) = 30 units
A's rate = 30 / 10 = 3 units/day
B's rate = 30 / 15 = 2 units/day
C's rate = 30 / 30 = 1 unit/day
```

No fractions anywhere — just add rates directly. This is the single fastest technique in the whole
topic and should be your default approach whenever every given time is an integer.

> 💡 **Why this beats the fraction method:** Fractions with different denominators need a common
> denominator anyway before you can add them — the LCM method just does that step *once, up front*,
> and keeps every number that follows as a clean integer.

---

## 2. Rate-First Thinking for Ratio Questions

Whenever a question gives an efficiency or time **ratio** instead of concrete numbers, assign rates
immediately instead of trying to imagine days.

> **Rule:** "A is `k` times as efficient as B" → let B's rate = 1 unit/day, A's rate = `k`
> units/day. Never start by guessing how many days each person takes.

This was introduced in `01-fundamentals.md` §6.1 — it's repeated here because it is, by a wide
margin, the highest-leverage mental habit in this topic. It also combines naturally with the LCM
method: once you have a rate ratio, picking total work = LCM of the *implied* times (or simply the
sum of the ratio parts, scaled as needed) keeps everything as clean integers.

---

## 3. Worker-Day Method — Workers Leaving

Use the conserved quantity `Total Work = Workers × Days` (from `01-fundamentals.md` §10) directly,
rather than switching to fractional one-day's-work.

**Procedure**
1. `Total work (worker-days) = Original Workers × Original Days`
2. `Work done so far = Workers present × Days already worked`
3. `Remaining work = Total work − Work done so far`
4. `Days needed = Remaining work / Workers now present`

**Worked Example:** 24 workers can finish a job in 18 days. After 6 days, 6 workers leave. How many
more days to finish?

```
Total work    = 24 × 18 = 432 worker-days
Done in 6 days = 24 × 6  = 144 worker-days
Remaining      = 432 − 144 = 288 worker-days
Workers left   = 24 − 6 = 18
Days needed    = 288 / 18 = 16 more days
```

---

## 4. Worker-Day Method — Workers Joining Later

Exactly the mirror image of §3: compute the work already completed by the original group, subtract
it from the total, then divide the remaining work by the **new**, larger workforce.

**General Procedure**
1. Compute `Total Work` as either 1 (fractional method) or worker-days (whole-number method).
2. Compute work already done before the new workers/workers joined.
3. Solve only for the **remaining** work with the **updated** rate.

This "completed work, then remaining work" split is the master pattern behind almost every
midway-change question — joining, leaving, or a mix of both.

---

## 5. Alternate-Day / Cyclic Working — Compute the Full Cycle First

When two (or more) workers alternate days (A on day 1, B on day 2, A on day 3, ...), **don't**
calculate day-by-day from scratch. Instead:

1. Calculate the work done in **one full cycle** (usually 2 days, or however long the repeating
   pattern is).
2. Divide the total work by the cycle work to find how many **complete cycles** fit.
3. Handle the **leftover** work with the next partial day(s) separately.

**Worked Example:** A's one-day work = `1/10`, B's one-day work = `1/15`. They alternate, starting
with A.

```
2-day cycle work = 1/10 + 1/15 = 3/30 + 2/30 = 5/30 = 1/6
```

Since `1/6` of the work finishes every 2 days, the whole job needs `6 × 2 = 12 days` — and because
`1/6 × 6 = 1` exactly, there's no partial final day to handle here. (When the total doesn't divide
evenly, work out how many full cycles fit, then solve only the small leftover fraction with whichever
worker's turn comes next.)

> ⚠️ **Common Mistake:** Assuming the two workers contribute equally per cycle. They don't — always
> use each individual's actual one-day rate inside the cycle, and pay attention to **whose turn is
> last** if the work finishes mid-cycle.

---

## 6. Efficiency Change → Time Change (Percentage Method)

Efficiency and time are inversely proportional, so a percentage change in efficiency does **not**
translate into the same percentage change in time.

**If efficiency increases by `x%`:**

```
New Time = Old Time × 100 / (100 + x)
```

**If efficiency decreases by `x%`:**

```
New Time = Old Time × 100 / (100 − x)
```

**Worked Example — Increase:** Efficiency +25%, old time = 20 days.

```
New Time = 20 × 100/125 = 20 × 4/5 = 16 days
```

**Worked Example — Decrease:** Efficiency −20%, old time = 15 days.

```
New Time = 15 × 100/80 = 15 × 5/4 = 18.75 days
```

> ⚠️ **Common Mistake:** Computing "efficiency +25% ⇒ time −25%." Time drops by **less** than the
> efficiency gain, because the relationship is a reciprocal, not linear.

---

## 7. Wages — Proportional to Work Share

Restating `01-fundamentals.md` §11 as an executable procedure:

1. Find each person's individual rate (or use the ratio directly).
2. Split the total wage in the same ratio as the rates — **not** the time each person spent working.

**Worked Example:** A (10 days) and B (15 days) work together and jointly earn ₹1500.

```
Rate ratio A : B = 1/10 : 1/15 = 3 : 2   (multiply both by 30 to clear denominators)
A's share = 1500 × 3/5 = ₹900
B's share = 1500 × 2/5 = ₹600
```

---

## 8. Pipes and Cisterns — Handling a Pipe That's Closed Partway

A very common TCS-style twist: both pipes open together, but one is closed after some time.

**Procedure**
1. Compute the net rate while **both** pipes are open, and find how much work that portion
   completes.
2. Subtract from 1 to get the **remaining** work.
3. Switch to the rate of whichever pipe is **still running** and solve only for the remainder.

**Worked Example:** Fill pipe A = 10 hr, outlet pipe B = 15 hr. Both open together, but B (the
outlet) is closed after 3 hours. Find the total time to fill the tank.

```
Net rate (both open) = 1/10 − 1/15 = 1/30
Work in first 3 hr    = 3 × 1/30 = 1/10
Remaining work         = 1 − 1/10 = 9/10
A alone (rate 1/10) needs: (9/10) / (1/10) = 9 more hours
Total time = 3 + 9 = 12 hours
```

---

## Quick Reference — Which Trick for Which Situation

| Situation | Use |
|---|---|
| All given times are clean integers | LCM Method (§1) |
| A ratio (efficiency or time) is given instead of numbers | Rate-First Thinking (§2) |
| Workers leave partway through | Worker-Day Method (§3) |
| Workers join partway through | Worker-Day Method, mirrored (§4) |
| Two/more workers alternate days | Cycle-first method (§5) |
| Efficiency changes by a percentage | Percentage-to-time formula (§6) |
| Payment needs to be split among workers | Wages-by-work-share (§7) |
| One pipe is closed/opened partway through | Split into "both open" + "one open" phases (§8) |

# Time & Work — Practice Questions
### Medium to Difficult, With Full Solutions

*Difficulty is marked as **[M]** Medium or **[H]** Hard. Solve on your own first, then check the
solution. Solutions use the methods from `01-fundamentals.md`, `02-fast-tricks-and-shortcuts.md`,
and `03-question-pattern-catalog.md`. Every numeric answer below was cross-checked independently
using exact fraction arithmetic (Python's `fractions.Fraction`) before being finalized.*

---

### Q1 [M] — Two People Working Together (Pattern A1)
A can complete a job alone in 12 days, B alone in 24 days. In how many days can they finish it
working together?

<details>
<summary><b>Solution</b></summary>

```
Together = (12 × 24) / (12 + 24) = 288 / 36 = 8
```

**Answer: 8 days**
</details>

---

### Q2 [M] — Efficiency Ratio (Pattern B1)
The efficiency ratio of A to B is 3 : 5. A alone takes 20 days to complete a job. Find the number of
days B alone would take, and the number of days they would take working together.

<details>
<summary><b>Solution</b></summary>

Efficiency ratio 3:5 means A is the *less* efficient one, so A (efficiency 3) takes more time than B
(efficiency 5). Since time is inversely proportional to efficiency:
```
Time ratio A : B = 5 : 3   (reverse of efficiency ratio)
A = 20 days  ⇒  B = 20 × 3/5 = 12 days
Together = (20 × 12) / (20 + 12) = 240/32 = 7.5 days
```

**Answer: B alone = 12 days; together = 7.5 days**
</details>

---

### Q3 [M] — The Difference Formula (Pattern §5 of `01-fundamentals.md`)
A alone can complete a job in 30 days. A and B together can complete it in 12 days. In how many days
can B alone complete the job?

<details>
<summary><b>Solution</b></summary>

```
1/B = 1/12 − 1/30 = 5/60 − 2/60 = 3/60 = 1/20
```

**Answer: B alone = 20 days**
</details>

---

### Q4 [M] — LCM Method, Three Workers (Pattern A2)
A, B, and C can individually complete a job in 12, 15, and 20 days respectively. In how many days
will they finish it working together?

<details>
<summary><b>Solution</b></summary>

```
LCM(12, 15, 20) = 60 units of total work
A's rate = 60/12 = 5 units/day
B's rate = 60/15 = 4 units/day
C's rate = 60/20 = 3 units/day
Combined rate = 5 + 4 + 3 = 12 units/day
Time = 60 / 12 = 5 days
```

**Answer: 5 days**
</details>

---

### Q5 [M] — Pipes Filling and Emptying Together (Pattern E1)
A pipe can fill a tank in 6 hours; another pipe can empty the full tank in 9 hours. If both pipes are
opened together, in how much time will the tank be filled?

<details>
<summary><b>Solution</b></summary>

```
Net rate = 1/6 − 1/9 = 3/18 − 2/18 = 1/18
Time = 18 hours
```

**Answer: 18 hours**
</details>

---

### Q6 [H] — Pipe Closed Partway Through (Pattern E2)
Fill pipe A can fill a tank in 10 hours; outlet pipe B can empty it in 15 hours. Both are opened
together, but B is closed after 3 hours. Find the total time to fill the tank.

<details>
<summary><b>Solution</b></summary>

```
Net rate (both open) = 1/10 − 1/15 = 1/30
Work done in first 3 hours = 3 × 1/30 = 1/10
Remaining work = 1 − 1/10 = 9/10
A alone (rate 1/10/hr) needs: (9/10) ÷ (1/10) = 9 more hours
Total time = 3 + 9 = 12 hours
```

**Answer: 12 hours**

> ⚠️ **Why This Is a Common Trap:** People sometimes keep using the *net* rate for the whole
> problem, forgetting that once the outlet closes, only the inlet's rate applies for the rest of the
> time. Always split into phases the moment any pipe's status changes.
</details>

---

### Q7 [H] — Worker Joining Midway (Pattern C1)
A can complete a job alone in 20 days. A works alone for 5 days, then B (who alone would take 30
days) joins. How many total days does the job take to finish?

<details>
<summary><b>Solution</b></summary>

```
Work done by A in 5 days = 5/20 = 1/4
Remaining work = 3/4
Combined rate (A + B) = 1/20 + 1/30 = 3/60 + 2/60 = 1/12
Extra days needed = (3/4) ÷ (1/12) = 9
Total days = 5 + 9 = 14
```

**Answer: 14 days**
</details>

---

### Q8 [H] — Workers Leaving Midway (Pattern C2)
36 workers can complete a job in 20 days. After 5 days, 6 workers leave the job. In how many more
days will the remaining workers finish it?

<details>
<summary><b>Solution</b></summary>

```
Total work = 36 × 20 = 720 worker-days
Work done in 5 days = 36 × 5 = 180 worker-days
Remaining work = 720 − 180 = 540 worker-days
Workers remaining = 36 − 6 = 30
Days needed = 540 / 30 = 18
```

**Answer: 18 more days**
</details>

---

### Q9 [M] — Alternate-Day Working (Pattern F1)
A can complete a job alone in 6 days, B alone in 9 days. Working on alternate days, starting with A,
in how many days will the job be finished?

<details>
<summary><b>Solution</b></summary>

```
2-day cycle work = 1/6 + 1/9 = 3/18 + 2/18 = 5/18
```
Three full cycles (6 days) complete `3 × 5/18 = 15/18 = 5/6` of the work.

Remaining work = `1/6`. Day 7 is A's turn again (cycle restarts): A's rate is `1/6`, so A finishes
exactly the remaining `1/6` in **one more full day**.

```
Total = 6 (three full cycles) + 1 (A's final day) = 7 days
```

**Answer: 7 days**
</details>

---

### Q10 [H] — Men/Women Equivalence (Pattern D1)
3 men do the same amount of work as 5 women (equal efficiency comparison). 3 men alone can complete a
job in 20 days. In how many days can 6 men and 10 women together complete the same job?

<details>
<summary><b>Solution</b></summary>

```
3 men alone: 20 days ⇒ 1 man's rate = 1/(3 × 20) = 1/60
3 men = 5 women (equal output) ⇒ 1 woman's rate = (3 × 1/60) / 5 = 1/100
6 men + 10 women rate = 6×(1/60) + 10×(1/100) = 1/10 + 1/10 = 1/5
Time = 5 days
```

**Answer: 5 days**

> 💡 **Note:** 6 men and 10 women is exactly *double* the "3 men = 5 women" equivalence group, so it
> makes sense the answer is a clean number — doubling the workforce on a fixed job always halves the
> time, and here the group ratio was scaled up perfectly.
</details>

---

### Q11 [M] — Wages Based on Work (Pattern G1)
A can complete a job alone in 8 days, B alone in 12 days. They work together and are jointly paid
₹2500. Find each person's share.

<details>
<summary><b>Solution</b></summary>

```
Rate ratio A : B = 1/8 : 1/12 = 3 : 2   (multiply both by 24)
A's share = 2500 × 3/5 = ₹1500
B's share = 2500 × 2/5 = ₹1000
```

**Answer: A = ₹1500, B = ₹1000**
</details>

---

### Q12 [M] — Efficiency Decrease → Time Change (Pattern J2)
A's efficiency decreases by 25%. If A originally took 18 days to complete a job at full efficiency,
how many days will A now take?

<details>
<summary><b>Solution</b></summary>

```
New Time = Old Time × 100/(100 − 25) = 18 × 100/75 = 24
```

**Answer: 24 days**
</details>

---

### Q13 [H] — Variable Efficiency Mid-Job (Pattern J1)
Working at a constant rate, A can finish a job in 12 days. A works at the normal rate for the first 3
days, then works at **triple** efficiency for the rest of the job. How many total days does the job
take?

<details>
<summary><b>Solution</b></summary>

```
Normal rate = 1/12
Work done in first 3 days = 3 × 1/12 = 1/4
Remaining work = 3/4
Tripled rate = 3 × 1/12 = 1/4
Extra days needed = (3/4) ÷ (1/4) = 3
Total days = 3 + 3 = 6
```

**Answer: 6 days**
</details>

---

### Q14 [H] — Percentage of Work Completed (Pattern I1)
A can complete 90% of a job in 18 days. In how many days can A alone complete the entire job? B then
finishes the remaining 10% of the job in 3 days — in how many days could B alone complete the entire
job?

<details>
<summary><b>Solution</b></summary>

```
A: 90% in 18 days  ⇒  100% in 18 / 0.9 = 20 days
B: 10% in 3 days   ⇒  100% in 3 / 0.1 = 30 days
```

**Answer: A alone = 20 days; B alone = 30 days**

> ⚠️ **Why This Is a Common Trap:** People sometimes try to combine A and B's *individual* full-job
> times directly (e.g., averaging 20 and 30) to answer a different question about their combined
> time. Here the question only asks for each person's **individual** full-job time — scale each
> person's given fraction independently; don't mix the two workers' numbers together unless the
> question specifically asks for a combined rate.
</details>

---

## Answer Key Summary

| Question | Answer |
|---|---|
| Q1 | 8 days |
| Q2 | B = 12 days; together = 7.5 days |
| Q3 | 20 days |
| Q4 | 5 days |
| Q5 | 18 hours |
| Q6 | 12 hours |
| Q7 | 14 days |
| Q8 | 18 more days |
| Q9 | 7 days |
| Q10 | 5 days |
| Q11 | A = ₹1500, B = ₹1000 |
| Q12 | 24 days |
| Q13 | 6 days |
| Q14 | A = 20 days, B = 30 days |

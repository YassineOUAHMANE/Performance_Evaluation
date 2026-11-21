# Performance Evaluation : Course Takeaways

My main takeaways from the sessions, organised by topic.

---

## 1. Data Handling and Visualisation

### Reading data
- After loading a CSV (R or Python), **check the column types** (`str(df)` in R, `df.dtypes` in Python).

### Good practices
- **Plot the data first**, before any model, so you can see the patterns.
- **Join the dots only if the relation is continuous.** For discrete or independent points, do not draw lines.
- Show **uncertainty**: without confidence intervals, "MINE" can look clearly better than "YOURS".
  With the intervals shown, they may overlap, which means there is no real difference.

### Feelings, culture and ethics
- A visualisation carries **feelings**, and colours and symbols can mean different things in different **cultures**.
- Whether to change a chart because of the feeling it gives is an **ethical question**.
  Discuss it with your colleagues.

---

## 2. Scientific Publishing

### Ethics and authorship
- Always **ask permission** from your co-authors before publishing work that includes their contribution.
- **Never use someone else's work** without citing them or getting their permission.
- In some fields, authors are listed in **alphabetical order**.

### Where to publish
- **National rankings** of journals and conferences (e.g. Brazil, Australia).
- **Free access vs toll access**: open to everyone, or behind a paywall.
- **Peer-reviewed vs non-peer-reviewed**: peer review means experts checked the work before it was published.

### Citations
- A **citation** is when paper B refers to paper A, and every citation adds one to A's count.
- Watch out for manipulation: citations can be **added to the metadata** so they get counted,
  even though they do not appear in the paper itself.

### Impact Factor vs. h-index

| | Impact Factor | h-index |
|---|---|---|
| **Measures** | A **journal** | A **researcher** |
| **Definition** | Average number of citations to the papers the journal published over the **last two years** | *h* of the researcher's papers have **at least h citations each**, and the others have ≤ h |
| **Example** | IF = 5 ->  each recent article was cited 5 times on average | h = 10 -> 10 papers with ≥ 10 citations each |

h-index examples:
- 50 papers that nobody cited -> h = **0**
- 1 paper cited 10,000 times -> h = **1**
- h = 20 → 20 papers with ≥ 20 citations each, and the 21st has ≤ 20

The h-index rewards **consistent** impact, so one famous paper is not enough for a high score.

---

## 3. Measurement Protocol

- Goal: find the **interval a device can wait to avoid collisions**.
- Method: control when the device sends its messages, **measure the intervals**,
  then **check whether the values match the specification**.
- From the measurements, **estimate** the parameters of a **stochastic model** (parametric estimation).

---

## 4. Statistics and Estimation

- **Statistic vs. estimator**: a statistic is computed from the data, and an estimator is a statistic
  used to guess a model parameter. We compute the statistic, then use it to estimate.
- **Biased vs. unbiased estimators**: an unbiased estimator gives the true value on average.
- **Remove outliers first**, before estimating anything.
- **Stationary process**: the variance stays constant over time.
  **Non-stationary process**: the spread keeps growing, and the variance can go to infinity.

---

## 5. Linear Regression

- Model: **Y = a + bX + ε**, where *a* is the **intercept**, *b* is the **slope**, and ε is the **noise**.
- Assumption: the **errors are independent**.
- Ways to fit the line:
  - **Least squares** (vertical distances)
  - **Least rectangles**
  - **Least squares in both directions**
- **Interpolation**: predicting *inside* the observed range (safe).
  **Extrapolation**: predicting *outside* the observed range (risky).
- Always **plot the data before** fitting a regression.

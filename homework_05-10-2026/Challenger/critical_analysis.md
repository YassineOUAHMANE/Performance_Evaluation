# Critical Analysis - Challenger O-ring Malfunction

**Author:** Yassine OUAHMANE
**Date:** Week 05/10/2026  
**Course:** Scientific Methodology and Empirical Evaluation (MOSIG)

---

## Executive Summary

The original analysis of the probability of failure of the Challenger shuttle's O-ring joints made **three major reasoning errors** that led to a catastrophic underestimation of risk. This underestimation directly contributed to the decision to proceed with the flight on January 28, 1986, resulting in the death of seven astronauts.

---

## Error 1: Exclusion of Critical Data

### The Problem
```python
data = data[data.Malfunction>0]  # ← critically defective filter
```

**What was done:** Keep only flights with failures (7 flights)  
**What should have been done:** Include all flights (23 flights total)

### Why This Is a Major Error

To calculate a probability, we need:
```
Probability = Number of cases with failure / total number of cases
```

By excluding successful flights, the analysis biases the statistic:
- **With filtered data:** p ≈ 0.214 (21.4%) ← wrong (overestimates per-ring rate)
- **With complete data:** p ≈ 0.0652 (6.52%) ← correct (overall per-ring failure rate)

### Consequence
This error **overestimates** the filtered rate by a factor of **3.3x** (0.214 vs 0.0652). More critically, filtering hides the strong temperature effect that appears when you analyze all flights.

---

## Error 2: Extrapolation Beyond Data Domain

### The Problem

**Available data range:**
- Minimum temperature: 53°F
- Maximum temperature: 81°F
- Total range: 28°F

**Launch day temperature:**
- Challenger day: 31°F (-0.5°C)
- Deviation: **22°F below the range**

### Why This Is Invalid

```
Available data:     53°F <------------> 81°F
Challenger:    31°F <-     no data here     ->
```

**The frequency plot shows a flat line** around 0.2, suggesting "no temperature impact". 

**But:** This conclusion is based on a region where **there is no data**.

### Scientific Principle Violated
> *"It is not reasonable to draw a conclusion by not having any data for such low temperatures"*  MOOC Reproducible Research

### Consequence
Extrapolation gave a predicted risk of ~20% (with old binary model) when the binomial model predicts ~81.8% at 31°F. The wide confidence interval [16%, 99%] shows massive uncertainty in the extrapolation region.

---

## Error 3: Estimation Uncertainty Ignored

### The Problem

Even with correctly applied logistic regression, there is a **zone of uncertainty** (confidence interval) around the prediction.

**Example - O-ring failure rate (9 out of 138 rings):**
- Point estimate: p = 0.0652 (6.52%)

The original analysis **completely ignored the uncertainty** and used the point prediction as certainty.


### Why This Is Critical at Low Temperature

With so little data at low temperatures, the confidence interval **expands enormously**.

At 31°F (22°F below minimum observed data), the confidence interval is: [16%, 99%] ->  **absolutely should not launch**!

### Consequence
Ignoring this uncertainty gave false impression of certainty ("Everything is under control").


##  Lessons Learned

1. **Keep all the data.** Flights without failure carry the information on temperature; removing them hides the effect.
2. **Stay within the tested range.** A prediction far outside the data (31 °F vs 53 - 81 °F) must be flagged as unreliable.
3. **Always report uncertainty.** A very wide confidence interval means the data cannot support the decision.

---

##  Real-World Impact

These three errors combined led to:
- **Risk underestimation by 4x** (~20% used vs ~81.8% actual with proper model)
- **Confidence interval ignored** (wide [16%-99%] CI should have triggered "Do not launch")
- **Decision to proceed despite warnings** from Thiokol engineers
- **Death of 7 astronauts**
- **Most documented space catastrophe in history**

---

## Conclusion

Critical analysis of the Challenger case shows that methodological errors in science are not just academic consequences  they can be fatal. 

**Good scientific practice is not a suggestion, it is a necessity.**

# Quiz Answers - Challenger Exercise 5

## Question
**What are the three errors of reasoning that led to an underestimation of the probability of failure?**

---

##  Correct answers

### **c. Key data were excluded from the analysis**

**Explanation:** `data[data.Malfunction>0]` removes the 16 flights without failure, mostly warm ones. Without them the temperature slope is ~0 (0.0014); with all 23 flights it is clearly negative (−0.116): colder means more failures.

---

### **b. It is not reasonable to draw a conclusion by not having any data for such low temperatures**

**Explanation:** The tests cover 53 - 81 °F, the launch was at 31 °F, 22 °F below. The temperature-free p = 0.065 (1.2 % shuttle risk) does not apply there; the model gives about 82 % per O-ring (≈ 96 % for the shuttle).

---

### **e. Uncertainty of the estimate has not been taken into account when analyzing the output of the logistic regression**

**Explanation:** The slope's interval in their own output ([−0.238, 0.240]) was ignored. At 31 °F the 95 % CI is [16 %, 99 %]: far too wide to conclude "everything is under control".

---

##  Incorrect answers

### a. There is a computation error in the analysis
**Why this is wrong:** The arithmetic is right (0.065² ≈ 0.00425, 1 − (1 − 0.00425)³ ≈ 1.3 %); the error is in the data and assumptions.

---

### d. Pressure was excluded from the model parameters
**Why this is wrong:** Pressure is almost constant (200 psi in most flights), so leaving it out introduces no major bias.

---

### f. Statistics are too complicated
**Why this is wrong:** This is an excuse, not a reasoning error; the problem is the methodological choices.

---


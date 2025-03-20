#machine_learning #metrics 

> [!Info]
> **F1-score** → "How well am I balancing [[Precision & Recall]]?"
>
> How good am i at **correctly identifying positive cases** while **avoiding false positives**.
### F1-Score Formula

$F1=2*\frac{Precision * Recall}{Precision + Recall}$ 

Or, in terms of TP, FP and FN:

$F1=2*\frac{2 * TP}{2*TP+FP+FN}$ 

For **multiclass problems** consider [[Per Class & Macro- & Micro-Averaged Metrics]].

### When to Use F1-Score

✅ **Imbalanced Data**: If positive cases are rare (e.g., fraud detection).  
✅ **When You Care About Both**: You want to minimize false positives **and** false negatives.  
✅ **Model Comparison**: Compare models on a **single** meaningful number.

## Undefined values conventions

If precision and recall are **0**, this becomes:

$F1=2*\frac{Precision * Recall}{Precision + Recall}$ = $\frac{0 * 0}{0 + 0}$ = $\text{undefined (or 0 by convention)}$

**By convention**, the F1-score is set to **0** when **no positive predictions** are made
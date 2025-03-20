#machine_learning #metrics 

> [!Info]
> **Precision** → "How often was i right when i classified something as class A?"
>
> **Recall** → "How many objects of class A did i correctly classify as class A?"

Precision = TP / (TP + FP)
Recall = TP / (TP + TN)

For **multiclass problems** consider [[Per Class & Macro- & Micro-Averaged Metrics]].

![[precision_recall.png]]

## Tricks for memorizing

**Precision**: Of the items I predicted as positive, how many were actually positive?  
→ _"When I say it's right, how often am I correct?"_

dt.: **Präzision** 
→ _Wie oft lag der Drogenspürhund rightig, wenn er angeschlagen hat? Wie präzise ist er?_ 

___

**Recall**: Of all the actual positives, how many did I correctly identify?  
→ _"Did I catch everything important?"_
→  _also: True-Positive rate_

dt.: **Sensitivität** 
→ _Hat der Drogenspürhund alle Dorgen gefunden? Wie sensibel ist er?_

## Why Precision and Recall Can Be Misleading Alone

Imagine these two models:

1. **Model A**: 4 True Positives (TP), 0 False Positives (FP), 0 True Negatives (TN)
    - Precision = 4 / (4 + 0) = **100%**
    - Recall = 4 / (4 + 0) = **100%**
2. **Model B**: 9999 TP, 1 FP, 1 TN
    - Precision = 9999 / (9999 + 1) = **~99.99%**
    - Recall = 9999 / (9999 + 1) = **~99.99%**

By precision alone, Model A **looks better**, but it’s only been tested on **4 positive cases**. Model B is far more robust and likely to **generalize** better.

**For a more complete picture consider also the [[F1 Score]] – Harmonic mean of precision and recall (balances both metrics).**

## Undefined values conventions

If **TP = 0** and **FP = 0**, this becomes:

Precision = $\frac{TP}{TP + FP}$ = $\frac{0}{0 + 0}$ = $\text{undefined (or 0 by convention)}$

If **TP = 0** and **TN = 0**, this becomes:

Recall = $\frac{TP}{TP + TN}$ = $\frac{0}{0 + 0}$ = $\text{undefined (or 0 by convention)}$
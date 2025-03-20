#machine_learning #metrics #loss

> [!info]
> L1 Loss calculates the **absolute** difference between the predicted value and the true value.


$\text{L1 Loss} = \sum|y_{gt}-y_{pred}|$ 

$\text{MAE} = \frac{1}{n}\sum_{i=1}^{n}|y_{i, gt}-y_{i, pred}|$ 

## Characteristics

| Feature                 | Characteristic                         |
| ----------------------- | -------------------------------------- |
| **Outlier Sensitivity** | **Low** (treats all errors equally)    |
| **Gradient**            | Constant (e.g., ±1)                    |
| **Optimization**        | Can be harder (non-smooth at 0)        |
| **Best for**            | **Robust** models (outlier resistance) |

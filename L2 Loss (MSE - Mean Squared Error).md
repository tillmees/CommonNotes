#machine_learning #metrics #loss

> [!info]
> L2 Loss calculates the **squared** difference between predictions and actual values. It penalizes **larger errors** more heavily.


$\text{L2 Loss} = \sum(y_{gt}-y_{pred})^2$ 

$\text{MSE} = \frac{1}{n}\sum_{i=1}^{n}(y_{i, gt}-y_{i, pred})^2$ 

## Characteristics

| Feature                 | Characteristic                   |
| ----------------------- | -------------------------------- |
| **Outlier Sensitivity** | **High** (large errors dominate) |
| **Gradient**            | Proportional to error (linear)   |
| **Optimization**        | Easy (smooth gradients)          |
| **Best for**            | Penalizing **large errors** more |

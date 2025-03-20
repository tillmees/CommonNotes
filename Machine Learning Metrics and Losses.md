#machine_learning #metrics #loss

## Metrics

| **Metric**                                                         | **When to use**                                                                             |
| ------------------------------------------------------------------ | ------------------------------------------------------------------------------------------- |
| [[Accuracy]]                                                       | Balanced datasets, simple evaluation                                                        |
| [[Per Class & Macro- & Micro-Averaged Metrics]]                    | Multiclass problems                                                                         |
| [[Precision & Recall]]                                             | When **false positives** and/or **false negatives** are costly                              |
| [[F1 Score]]                                                       | **Imbalanced** data, overall performance                                                    |
| [[Confusion  Matrix]]                                              | Diagnosing **errors** and **patterns**                                                      |
| [[AUC-ROC (Area Under Curve - Receiver Operating Characteristic)]] | **Imbalanced** data, **trade-off** between **true positives** and **false positives**       |
| [[AUC-PR (Area Under Precision-Recall Curve)]]                     | **Imbalanced datasets** where **precision** and **recall** are more important than accuracy |
| [[LAMR (Log Average Miss Rate)]]                                   | **Object detection**, with focus on the miss rate                                           |
| [[mAP (mean Average Precision)]]                                   | **Object detection**, precision of detections over multiple classes and IoU thresholds      |

___
## Losses

| Loss                                        | **When to use**                                                                                                                                                                                                                      |
| ------------------------------------------- | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ |
| [[L1 Loss (MAE - Mean Absolute Error)]]     | - When robustness to **outliers** is needed.  <br>- When **sparse solutions** are desirable.                                                                                                                                         |
| [[L2 Loss (MSE - Mean Squared Error)]]      | - When **larger errors** should be penalized more.  <br>- When **smooth optimization** is preferred.                                                                                                                                 |
| [[Huber Loss]]                              | - When you need a balance between **L1 and L2**.  <br>- When the data contains **some outliers** but you don’t want to completely ignore them.                                                                                       |
| [[Cross-Entropy Loss]]                      | - For **classification** tasks, especially with **probabilistic outputs** (e.g., softmax).  <br>- When the model outputs a **probability distribution** over classes.                                                                |
| [[Log-Cosh Loss]]                           | - When you want to combine the benefits of L1 and L2 losses but with **less sensitivity to outliers**.  <br>- Works well when small **errors are prioritized**, but larger ones should be handled gently.                            |
| [[Contrastive Loss (Supervised)]]           | - For **metric learning** and **Siamese networks** in supervised settings.  <br>- When learning to **measure similarity** or **dissimilarity** between input pairs.                                                                  |
| [[Contrastive Loss (Unsupervised)]]         | - For **unsupervised learning** tasks (e.g., **self-supervised learning**).  <br>- When you want the model to **learn representations** by contrasting positive and negative pairs, without label information.                       |
| [[CTC Loss]]                                | - For **sequence-to-sequence** tasks where the alignment between input and output sequences is unknown.  <br>- Commonly used in **speech recognition**, **handwriting recognition**, or **speech-to-text** tasks.                    |
| [[Focal Loss]]                              | - For **imbalanced classification tasks** where the model needs to focus more on **hard-to-classify examples** (often used in **object detection**).  <br>- When the **background class** (e.g., negative class) is highly dominant. |
| [[Softmax Loss (Multiclass Cross-Entropy)]] | - For **multi-class classification** where the model outputs **probabilities** for each class (e.g., in **multi-class object classification**).                                                                                      |

___

## Others

[[Confidence Intervalls]]

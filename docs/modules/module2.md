# Module 2: How Machine Learning Works

!!! abstract "Module overview"
    **Time:** ~12 minutes  
    **Goal:** Understand training, validation, and the performance metrics that appear in grant applications and research papers.

---

## Learning by example

Machine learning models learn by example. You feed them labeled training data — say, 10,000 MRI scans tagged "tumor" or "no tumor" — and the model adjusts its internal parameters until it gets good at predicting the correct label. This process is called **training**.

> **Think of it this way:** Training a model is like teaching a medical student by showing them thousands of cases and telling them the diagnosis each time. Eventually, the student learns which features matter — without ever being given an explicit rulebook.

After training, the model is tested on **new data it has never seen**. This is called validation. The gap between training performance and validation performance tells you whether the model has genuinely learned or merely memorized.

---

## The training pipeline

```
Raw data → Preprocessing → Training set → Model training
                        ↘ Validation set → Performance evaluation
                        ↘ Test set → Final unbiased assessment
```

A well-designed study reserves a **held-out test set** that is never touched during model development. If researchers report only training-set performance, ask about the test set.

---

## Performance metrics explained

These are the numbers you'll see in abstracts and grant applications:

### Accuracy
The proportion of all predictions that were correct.

*Limitation:* If 95% of patients in your dataset don't have the disease, a model that always predicts "no disease" achieves 95% accuracy while being completely useless. Always ask about the **class distribution**.

### Sensitivity (Recall)
How often the model correctly identifies true positive cases — e.g., what fraction of real disease cases did it catch?

**High sensitivity = few missed cases.** Critical for screening tools where missing a case is dangerous.

### Specificity
How often the model correctly identifies true negatives — i.e., avoids false alarms in healthy patients.

**High specificity = few false alarms.** Critical when false positives lead to costly or harmful follow-up procedures.

### AUC-ROC
The Area Under the Receiver Operating Characteristic Curve. A single number from 0.5 to 1.0 summarizing how well the model distinguishes between two classes.

| AUC Score | Interpretation |
|-----------|---------------|
| 0.5 | No better than random chance (coin flip) |
| 0.7–0.8 | Acceptable |
| 0.8–0.9 | Good |
| 0.9–1.0 | Excellent |

!!! tip "Funder note"
    AUC is useful for comparing models, but it doesn't directly tell you clinical utility. A model with AUC 0.95 may still produce too many false alarms to be useful at scale. Always ask: *"What does this performance mean for a patient?"*

---

## The overfitting problem

**Overfitting** is when a model memorizes its training data instead of learning generalizable patterns. It performs brilliantly on training data but fails on new patients.

Signs of overfitting to watch for:

- Very high training accuracy with much lower validation accuracy
- Model performance drops significantly when tested at a different institution
- The team reports results only on data used during development

> **A model that achieves 99% accuracy on its training data but 62% on new patients hasn't learned medicine. It's memorized a dataset.**

---

## Key terms

??? note "Training data"
    The labeled examples used to teach the model. Quality, size, and diversity of training data are the single biggest determinant of model quality.

??? note "Overfitting"
    When a model memorizes its training data instead of learning generalizable patterns. It performs well on training data but poorly on new data — the most common failure mode.

??? note "Validation"
    Testing the model on data it was NOT trained on, to see how well it generalizes. Essential before any clinical use.

??? note "Deep learning"
    A powerful class of machine learning using neural networks with many layers. Excels at images, text, and genomic data. Requires very large datasets and significant computing power.

??? note "Hyperparameter"
    Settings chosen before training begins that control how the model learns (e.g., learning rate, number of layers). Tuning these on the validation set is normal; tuning them on the test set is a form of data leakage.

---

## Knowledge check

??? question "A model reports 99% accuracy on the training set but only 62% on new patient data. What is most likely happening?"
    
    **Correct answer:** The model is overfitting — it memorized training examples rather than learning generalizable patterns.
    
    This gap between training and test performance is the hallmark of overfitting. The model has essentially learned to recognize the specific patients in the training set, not the underlying disease features.

??? question "A screening model for a rare disease (affects 1 in 1,000 people) reports 99.9% accuracy. Should you be impressed?"
    
    **Not necessarily.** A model that simply predicts "no disease" for every patient would achieve 99.9% accuracy in a 1-in-1,000 prevalence population. For rare diseases, look at sensitivity, specificity, and the positive predictive value — not overall accuracy.

---

## What to ask a researcher

- "What is the split between your training, validation, and test sets?"
- "Was the test set truly held out, or was it used for any model selection decisions?"
- "What is the sensitivity and specificity — not just the overall accuracy?"
- "Has the model been tested on data from a different institution?"

---

[← Module 1](module1.md) | [Module 3: AI in Research →](module3.md)

# Module 4: Data, Bias, and the Limits of AI

!!! abstract "Module overview"
    **Time:** ~12 minutes  
    **Goal:** Understand the most important ways AI fails in medical research — and what ethical and equity questions every funder should be asking.

---

## The data dependency problem

AI is only as good as the data it learns from. In medical research, this creates serious risks that funders must understand — because **bias in training data produces bias in outcomes, often invisibly.**

> **Think of it this way:** If you trained a model only on data from patients at major academic medical centers, it may silently fail for patients in rural hospitals, or for communities that are historically underrepresented in clinical datasets. The model won't know it's failing — it will simply produce confident wrong answers.

---

## Three critical failure modes

### 1. Dataset bias

Training data skewed toward certain demographics, geographies, disease stages, or clinical settings. A model trained on such data may perform very well for the represented group and very poorly for everyone else — often without any obvious warning.

**Who is most often underrepresented in medical AI datasets:**
- Women (many early datasets were male-dominated)
- Older adults and children
- Racial and ethnic minority communities
- Patients in lower-income countries
- Patients with rare diseases (by definition)

### 2. Label noise

If the labels used to train the model are wrong or inconsistent — because different clinicians interpreted scans differently, or diagnostic criteria changed over time — the model learns those errors. Garbage in, garbage out.

### 3. Distribution shift

A model trained on 2015 data deployed in 2025 may fail because clinical practice, patient demographics, imaging equipment, or electronic health record systems have changed. This is called **distribution shift** and is one of the most common real-world AI failure modes.

!!! warning "High overall accuracy can hide subgroup failure"
    A model that achieves 94% overall accuracy may achieve only 70% accuracy for a specific demographic group that was underrepresented in training. Overall accuracy statistics will not reveal this unless the team explicitly reports subgroup performance.

---

## Ethical considerations

### Patient privacy and consent

Training on electronic health records requires careful de-identification and robust data governance. Key questions:

- Were patients whose data trained the model informed it would be used this way?
- Is there an IRB protocol in place?
- Is the data de-identified according to current standards (HIPAA Safe Harbor or Expert Determination)?
- Is the data stored and accessed securely?

### Explainability

Can the research team explain *why* the model made a given prediction? Or is it a "black box"?

| Model type | Explainability | Power |
|-----------|---------------|-------|
| Logistic regression | High — each feature's contribution is visible | Lower |
| Decision tree | High — the decision path is traceable | Lower |
| Random forest | Medium — feature importance scores | Medium |
| Deep neural network | Low — highly complex internal representations | Very high |

For clinical applications, explainability matters enormously. A clinician cannot be expected to act on a recommendation they cannot understand or interrogate.

### Equity

Does the AI perform equally well across sex, race, age group, and socioeconomic status? Unequal performance entrenches existing health disparities rather than reducing them.

---

## Key terms

??? note "Bias (in AI)"
    Systematic error in a model caused by non-representative training data or flawed assumptions. Results in predictions that are consistently wrong for certain groups — often groups already disadvantaged in healthcare.

??? note "Explainability (XAI)"
    The degree to which a model's decisions can be understood by humans. Simpler models are highly explainable. Large deep learning models are often "black boxes" — they produce accurate predictions through internal processes that cannot be easily interpreted.

??? note "IRB (Institutional Review Board)"
    An independent ethics committee that reviews research protocols involving human subjects, including the use of patient data for AI training. IRB approval is a baseline ethical standard.

??? note "De-identification"
    Removing or encrypting personally identifiable information (name, date of birth, address, etc.) from patient data before use in research. Required by HIPAA and good research practice.

??? note "Distribution shift"
    When the statistical properties of real-world deployment data differ from the training data, causing model performance to degrade. Common when models trained on historical data are deployed in changed clinical environments.

---

## Knowledge check

??? question "A diagnostic AI achieves 94% accuracy overall, but was trained mostly on data from men aged 40–60. Which concern is most relevant?"
    
    **Correct answer:** Dataset bias may mean the model works poorly for underrepresented groups — women, elderly patients, younger patients.
    
    High overall accuracy can mask very poor performance in subgroups not well-represented in training. The model has essentially learned from one slice of the patient population and may produce confident wrong answers for everyone else.

??? question "A researcher says their model is too complex to be fully explainable, but it achieves excellent accuracy. Is this acceptable?"
    
    **It depends on the application.** For discovery research (finding drug candidates, generating hypotheses), limited explainability may be acceptable if the findings are validated through other means. For clinical decision support — recommendations about individual patient care — limited explainability is a serious concern that should be addressed in the study design.

---

## What to ask a researcher

- "Who is represented in the training data? What are the demographic characteristics?"
- "Has the model been tested for performance differences across sex, age, race, and socioeconomic subgroups?"
- "Is there an IRB protocol covering the data use?"
- "Has the model been tested on data from a different institution or geography?"
- "Can you explain why the model makes a specific prediction?"

---

[← Module 3](module3.md) | [Module 5: Evaluating Claims →](module5.md)

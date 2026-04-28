# Module 5: How to Evaluate AI Research Claims

!!! abstract "Module overview"
    **Time:** ~12 minutes  
    **Goal:** A practical evaluation framework for reviewing AI research proposals, progress reports, and published findings as a patient advocate and funder.

---

## The funder's role

AI research — like all research — can be overpromised. As a funder, your role is not to become a machine learning expert, but to **ask the right questions** that reveal whether a claim is solid or premature.

The checklist below is your primary tool.

---

## The funder's evaluation checklist

### ✅ External validation

Has the model been tested on data from a completely separate institution or population — one that had no involvement in model development?

- **Internal validation only:** The model performed well on data similar to what it was trained on. Promising, not convincing.
- **External validation:** The model was tested on different patients, at a different site. This is the standard that matters.

### ✅ Comparison to a meaningful baseline

Does the AI meaningfully outperform the current standard of care, or just a naive guess?

*"Better than chance"* is a very low bar. The right comparison is: better than the current clinical process, at lower cost or higher scale?

### ✅ Clinically meaningful metric

Does the outcome measure matter to patients?

An AUC of 0.91 is impressive — but does it translate to earlier diagnosis, reduced time to treatment, or better outcomes? Ask the team to draw a direct line between their performance metric and patient benefit.

### ✅ Reproducibility

Is the code and data (or access to equivalent data) available so others can verify and replicate the results?

Reproducibility is a baseline standard for scientific credibility. Proprietary models with no public access are harder to evaluate and build on.

### ✅ Prospective vs. retrospective evidence

| Evidence type | What it means | Strength |
|--------------|---------------|---------|
| **Retrospective** | AI analyzed existing historical data | Hypothesis-generating; subject to many biases |
| **Prospective** | AI was tested on new patients in real time | Much stronger; closer to real-world performance |
| **Randomized controlled** | Patients were randomly assigned to AI-assisted vs. standard care | Gold standard for clinical AI |

Most published medical AI is retrospective. Prospective evidence is substantially more meaningful for funders making decisions about translational potential.

### ✅ Regulatory pathway (for clinical applications)

For diagnostics or treatment guidance, is there a plan for FDA clearance or CE marking?

**AI research ≠ AI deployment.** A model that works in a research setting cannot be used clinically without regulatory review and approval. A clear regulatory strategy is a sign of a team that understands the full journey.

---

## The one question that cuts through everything

!!! tip "Most important question"
    **"If this AI works exactly as described, what changes for a patient?"**
    
    This keeps funding decisions grounded in mission rather than benchmark scores. A beautiful AUC score means nothing if the team cannot articulate the path to patient benefit.

---

## Common red flags

| What you hear | What to probe |
|--------------|---------------|
| *"97% accuracy"* | Accuracy on what dataset? Compared to what baseline? In which subgroups? |
| *"State-of-the-art performance"* | Compared to which existing methods, tested how? |
| *"AI-powered"* | Which type of AI? How was it trained and validated? |
| *"We analyzed 100,000 patient records"* | Were patients consented? Is there IRB approval? Was data de-identified? |
| *"Our model generalizes well"* | Has it been tested at an external institution? |
| *"We're planning to validate next"* | Has any validation been done yet? Is the current funding for development or validation? |

---

## Reasonable vs. overpromised claims

**Reasonable:**
> "Our model detects early-stage disease in retinal images with sensitivity of 87% and specificity of 91%, validated on a held-out dataset from a separate institution. We are now designing a prospective study."

**Overpromised:**
> "Our AI will revolutionize diagnosis and could save millions of lives. Early results on our dataset are very promising."

The first gives you specific, verifiable claims with appropriate epistemic humility. The second is vague about methodology and overreaching on impact.

---

## Knowledge check

??? question "A grant application says: 'Our AI model achieved AUC 0.93 on our institutional dataset.' What is the most important follow-up question?"
    
    **Correct answer:** "Has this been validated on data from an independent institution?"
    
    Performance on a single institution's data — especially data used during development — is far weaker evidence than validation on an external, independent dataset. This is the most important next question before drawing conclusions about generalizability.

??? question "A researcher reports a prospective study showing their AI reduced time to diagnosis by 30%. Is this strong evidence?"
    
    **Yes, this is substantially stronger evidence than most published medical AI.** Prospective evidence — the model was tested on new patients in real time — is much more meaningful than retrospective analysis of historical data. Ask about sample size, statistical significance, the comparison condition, and whether the study was randomized.

---

## What to ask a researcher

- "Has this been validated on data from an independent institution?"
- "What does your model beat — random chance, the current standard of care, or a previous version of itself?"
- "If I fund this and it works perfectly, what changes for a patient in five years?"
- "Is the code and data available for independent review?"
- "What is the regulatory pathway if this moves toward clinical use?"
- "What does failure look like for this model, and how would you know if it was failing silently?"

---

[← Module 4](module4.md) | [Funder Reference Card →](../reference.md)

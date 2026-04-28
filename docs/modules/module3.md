# Module 3: What Is AI Actually Doing in Medical Research?

!!! abstract "Module overview"
    **Time:** ~10 minutes  
    **Goal:** Map the six major AI application areas in medical research so you can accurately categorize what a researcher is proposing — and ask the right domain-specific questions.

---

## The research pipeline and where AI fits

AI is being applied across the entire research pipeline — from early molecular discovery through clinical translation. Here are the six categories you will most commonly encounter when reviewing grants or research updates.

---

## Drug discovery

**What it does:** Screens millions of molecular compounds to predict which might bind to a disease target, have favorable pharmacological properties, or be synthesized efficiently.

**Why it matters:** Traditional drug screening is enormously expensive and time-consuming. AI can narrow a field of millions of candidates to hundreds in weeks rather than years.

**Example:** AlphaFold, developed by DeepMind, predicts the 3D structure of proteins from their amino acid sequences — a task that previously took years of laboratory work per protein.

!!! info "Stage of evidence"
    AI-assisted drug discovery identifies *candidates*. The vast majority still fail in preclinical and clinical testing. AI accelerates the front end of the pipeline; it does not change the fundamental attrition rates in drug development.

---

## Medical imaging analysis

**What it does:** Detects tumors, lesions, or early-stage changes in X-rays, MRIs, CT scans, pathology slides, and retinal images — often matching or exceeding specialist accuracy on specific, well-defined tasks.

**Why it matters:** Enables analysis at scales no human team could manage, reduces inter-reader variability, and can flag cases for priority review.

**Funder consideration:** Ask about the imaging hardware used in training. A model trained on high-field MRI data from a major academic center may not perform well on lower-field equipment used in community hospitals.

---

## Genomics and molecular biology

**What it does:** Identifies genetic variants linked to disease risk, predicts protein-protein interactions, finds patterns across biobanks of thousands of genomes, and integrates multi-omics data.

**Why it matters:** The volume of genomic data now generated far exceeds what traditional statistical approaches can analyze efficiently.

**Key distinction:** Predicting statistical associations between genetic variants and disease (a discovery task) is different from predicting whether a specific patient will respond to treatment (a clinical task). Both use AI; they have very different validation requirements.

---

## Clinical trial design and optimization

**What it does:** Identifies patients most likely to benefit from a treatment (patient stratification), predicts which enrolled patients are likely to drop out, designs adaptive trial protocols that adjust based on accumulating data, and optimizes dosing.

**Why it matters:** Failed or underpowered trials are one of the largest sources of waste in medical research. Better patient selection can reduce required sample sizes and increase the likelihood of detecting a real signal.

---

## Literature and knowledge mining

**What it does:** Parses millions of published papers to surface connections, contradictions, emerging consensus, and potential drug repurposing opportunities faster than any human review team.

**Funder consideration:** This is a genuine productivity tool for research teams. It is lower-risk than clinical AI applications, but the quality of outputs depends heavily on the quality of source literature — including its known biases toward positive results.

---

## Biomarker discovery and predictive modeling

**What it does:** Finds measurable biological signals — proteins, metabolites, EEG patterns, digital biomarkers from wearables — that correlate with disease state, progression, or treatment response.

**Why it matters:** Novel biomarkers can dramatically accelerate trial timelines, enable earlier intervention, and provide objective outcome measures.

**Important distinction:** A biomarker *associated* with disease in a cross-sectional study is not the same as a biomarker *predictive* of future progression in a prospective validation. Ask which kind of evidence the team is generating.

---

## Discovery vs. clinical AI: a critical distinction

!!! warning "Key concept for funders"
    AI that helps find a drug candidate operates under very different standards than AI that guides treatment decisions for individual patients.
    
    - **Discovery AI** needs to be reproducible and scientifically valid
    - **Clinical AI** additionally needs prospective validation, regulatory clearance, clinical workflow integration, and ongoing monitoring for drift
    
    A research team doing discovery AI and claiming clinical impact is making a very long leap. Ask about the pathway between the two.

---

## Knowledge check

??? question "A researcher proposes using AI to analyze existing patient health records to identify early warning signs of disease progression. Which category is this?"
    
    **Correct answer:** Biomarker or predictive modeling from clinical data.
    
    This is a predictive modeling use case — finding patterns in clinical data that predict future outcomes. It requires careful attention to data quality, patient privacy, and the difference between retrospective association and prospective prediction.

??? question "A researcher says their AI model 'discovers new drug candidates.' Should this be interpreted as producing treatment-ready therapies?"
    
    **No.** Drug *discovery* AI identifies candidates for further testing. The vast majority will fail in subsequent preclinical and clinical validation. AI has accelerated the front end of the pipeline without materially changing success rates in later-stage development.

---

## What to ask a researcher

- "Which part of the research pipeline does your AI operate in — discovery, translational, or clinical?"
- "Is this AI being used to generate hypotheses for further testing, or to guide decisions about individual patients?"
- "What does the pathway from your AI findings to patient benefit look like, and what are the milestones?"

---

[← Module 2](module2.md) | [Module 4: Data & Bias →](module4.md)

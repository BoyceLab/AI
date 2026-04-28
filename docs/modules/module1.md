# Module 1: What is Artificial Intelligence?

!!! abstract "Module overview"
    **Time:** ~12 minutes  
    **Goal:** Understand what AI actually is, what it isn't, and why the terminology matters when evaluating research proposals.

---

## What AI actually means

Artificial intelligence (AI) is software that performs tasks we would normally expect to require human intelligence — recognizing patterns, making predictions, interpreting language, or finding structure in large datasets. It is **not** a single technology; it is an umbrella term for many different approaches.

> **Think of it this way:** AI is like hiring a very fast, very literal analyst who has read every paper in a field but has no common sense or lived experience. She's remarkable at spotting patterns — but she needs you to define what matters.

In medical research, AI is used to sift through imaging data, electronic health records, genomic sequences, and published literature at scales no human team could manage. This creates both enormous opportunities and important responsibilities for funders.

---

## The AI family tree

These terms are often used interchangeably, but they mean different things:

| Term | What it means | Example in research |
|------|--------------|---------------------|
| **Artificial Intelligence (AI)** | Any software that mimics human cognitive tasks | Broad term covering all of the below |
| **Machine Learning (ML)** | AI that learns patterns from data examples, without being explicitly programmed | Predicting which patients are at risk of disease progression |
| **Deep Learning** | A powerful class of ML using many-layered neural networks | Detecting tumors in MRI scans |
| **Large Language Model (LLM)** | Deep learning trained on massive text data to understand and generate language | Summarizing clinical literature |
| **Generative AI** | AI that produces new content (text, images, molecules) | Proposing novel drug candidates |

---

## Why the distinction matters for funders

When a researcher says *"we used AI,"* ask which type. The implications differ significantly:

- A **logistic regression model** (technically ML) is simple, interpretable, and well-understood — a low-risk approach
- A **deep learning model** is powerful but requires far more data, compute, and expertise to validate properly
- A **generative AI system** introduces questions about hallucination, unpredictability, and appropriate use cases

!!! warning "Red flag"
    Vague use of "AI" without specifying the approach is a signal to probe further. It may indicate the team doesn't fully understand what they've built, or is overstating the sophistication of their work.

---

## Key terms

??? note "Artificial Intelligence (AI)"
    Software systems that perform tasks requiring human-like cognition — pattern recognition, prediction, language understanding. In research, AI usually means statistical or deep learning models trained on large datasets.

??? note "Machine Learning (ML)"
    A subset of AI in which systems learn from data examples rather than following explicit rules. Instead of programming "if X then Y," you show the system thousands of examples and it discovers the patterns itself.

??? note "Algorithm"
    A set of instructions a computer follows. In AI, algorithms define how a model learns from data and makes predictions. Not magic — a well-defined mathematical procedure.

??? note "Model"
    The trained product of a machine learning process. A model takes in new data and outputs a prediction or classification. Think of it as the recipe the algorithm discovered from examples.

??? note "Neural network"
    A computational structure loosely inspired by the brain, consisting of layers of mathematical nodes that transform inputs into outputs. Deep learning uses neural networks with many layers.

---

## Knowledge check

??? question "A researcher says her team 'used AI to analyze 50,000 retinal scans.' What is the most accurate interpretation?"
    
    **Correct answer:** A trained model found patterns across thousands of images — likely flagging abnormalities for expert review.
    
    AI doesn't replace expert review; it flags candidates for human experts to confirm. A robot didn't physically review each scan, and this is far more sophisticated than a simple keyword search.

??? question "What is the difference between machine learning and deep learning?"
    
    Deep learning is a specific type of machine learning that uses many-layered neural networks. It is especially powerful for images, audio, and text, but requires very large datasets and significant computing resources to train properly. Not all machine learning is deep learning.

---

## What to ask a researcher

- "When you say AI, do you mean machine learning, deep learning, or something else?"
- "Is this a model you trained yourselves, a pre-trained model you fine-tuned, or a commercial system?"
- "How interpretable is the model — can you explain why it made a given prediction?"

---

[Continue to Module 2: How ML Works →](module2.md)

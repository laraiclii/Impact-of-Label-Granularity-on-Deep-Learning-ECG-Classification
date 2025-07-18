🫀 ECG Label Granularity: Deep Learning for Robust Triage

Exploring how label granularity affects ECG classification performance, generalizability, and clinical utility using deep learning.

📚 Overview
Deep learning has shown strong potential in automating the interpretation of electrocardiograms (ECGs). However, the impact of label granularity—ranging from detailed arrhythmia-specific codes to broader severity-based categories—has not been thoroughly studied.

In clinical triage settings like primary care, where models must remain robust to noise, artifacts, and patient variability, coarse labels may be more practical than fine-grained diagnostic codes.

This project investigates the trade-offs between diagnostic precision and model robustness using a 1D ResNet trained under different labeling schemes.
While deep learning has shown promise in automating ECG interpretation, the choice between fine-grained diagnostic codes and broader, severity-based labels remains underexplored—especially in real-world settings like primary care, where robustness to noise and patient variability is critical.

We trained a 1D ResNet on the SPH dataset (25,770 ECGs) using three labeling strategies:

44-class American Heart Association (AHA) diagnostic codes

3-tier severity-based classification

4-tier hierarchical classification

Models were evaluated on internal (SPH) and external (PTB-XL) test sets, with additional analysis of rare and unseen pathologies.

Key Findings
The 3-tier model showed the best generalization (F1 = 0.87 internal, 60.5% external).

The 44-class model failed to generalize to rare conditions (external F1 = 0).

The 4-tier model preserved diagnostic nuance with only a 2% drop in accuracy.

Interpretability analysis revealed that severity-tiered models attended to clinically relevant ECG features, while fine-grained models were more prone to overfitting on noise.

Why It Matters
These results suggest that coarser, severity-based labeling can significantly improve model robustness and interpretability—key qualities for deploying ECG AI systems in real-world triage environments like primary care

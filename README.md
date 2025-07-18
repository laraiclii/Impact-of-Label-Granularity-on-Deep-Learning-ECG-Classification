🫀 ECG Label Granularity & Deep Learning
Exploring the impact of diagnostic label resolution on ECG classification performance using deep neural networks.

📌 Summary
This project investigates how different levels of label granularity—ranging from fine-grained diagnostic codes to coarse severity-based tiers—affect the performance, generalizability, and interpretability of ECG classifiers. Using a 1D ResNet model trained on the SPH dataset (25,770 ECGs), three labeling strategies were compared:

44-class AHA diagnostic codes

3-tier severity system (Normal, Monitor, Serious)

4-tier severity system (Normal, Mild, Moderate, Serious)

💡 Key Findings
The 3-tier model achieved the best robustness:

87% accuracy (F1 = 0.87) on internal test set

60.5% accuracy on external PTB-XL test set

The 4-tier model preserved more diagnostic nuance with only a 2% accuracy drop.

Fine-grained models showed high internal accuracy but failed to generalize to rare pathologies (F1 = 0 externally).

Grad-CAM visualizations revealed that coarse-label models focus on clinically relevant ECG segments, while fine-grained ones overfit to noise.

Interpretability analysis revealed that severity-tiered models attended to clinically relevant ECG features, while fine-grained models were more prone to overfitting on noise.

Why It Matters
These results suggest that coarser, severity-based labeling can significantly improve model robustness and interpretability—key qualities for deploying ECG AI systems in real-world triage environments like primary care

# 🫀 ECG Label Granularity & Deep Learning  
**Exploring the impact of diagnostic label resolution on ECG classification performance using deep neural networks.**

---

## 📌 Summary

This project investigates how different levels of label granularity—ranging from **fine-grained diagnostic codes** to **coarse severity-based tiers**—affect the performance, generalizability, and interpretability of ECG classifiers.

A 1D ResNet model was trained on the SPH dataset (25,770 ECGs) using three labeling strategies:
- **44-class** AHA diagnostic codes  
- **3-tier** severity system: `Normal`, `Monitor`, `Serious`  
- **4-tier** severity system: `Normal`, `Mild`, `Moderate`, `Serious`

---

## 💡 Key Findings

- 🥇 **3-tier model** showed the best robustness:
  - 87% internal accuracy (F1 = 0.87)
  - 60.5% external accuracy (PTB-XL)
- 🧠 **4-tier model** preserved diagnostic nuance with only a 2% accuracy drop.
- 🚨 **44-class model** failed to generalize to rare pathologies (F1 = 0 externally).
- 🔍 Grad-CAM visualizations showed:
  - Tiered models focused on clinically relevant waveform regions.
  - Fine-grained models overfit to noise and artifacts.

---

## 🏥 Clinical Relevance

This work supports a **two-stage ECG analysis pipeline**:
1. **Severity-based triage** in primary care with coarse labels.
2. **Fine-grained diagnosis** in specialist settings if needed.

The framework improves robustness, reduces overfitting, and enhances interpretability—making it suitable for **AI-powered Holter devices** and real-world primary care deployment.

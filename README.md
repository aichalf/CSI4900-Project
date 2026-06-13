# 🔍 ML Pitfalls in Intrusion Detection Systems — Honours Research Project

![Python](https://img.shields.io/badge/Python-3.10-blue?logo=python) ![Research](https://img.shields.io/badge/Type-Honours%20Research-purple) ![University](https://img.shields.io/badge/University%20of%20Ottawa-CSI4900-darkred) ![Status](https://img.shields.io/badge/Status-Complete-brightgreen)

> Systematic evaluation of methodological flaws in machine learning models used for network intrusion detection — combining literature review, structured annotation, and inter-rater reliability analysis.

## 📌 Overview

This Honours research project (CSI 4900) investigates **common ML pitfalls** in published Intrusion Detection System (IDS) papers. A structured evaluation framework was designed and applied to a corpus of academic papers, scoring each on criteria related to evaluation methodology, class imbalance handling, and reporting quality.

The goal: identify systematic weaknesses in how researchers evaluate ML models for cybersecurity, and propose improvements to evaluation pipelines.

## 🎯 Research Questions
- How frequently do IDS papers fall into base rate fallacy traps (reporting TPR without FPR/base rate context)?
- How well do published papers handle class imbalance in intrusion detection datasets?
- What is the inter-annotator agreement across independent reviewers on structured evaluation criteria?

## 🔬 Methodology

### Annotation Framework
- Designed a rubric of **structured criteria** across multiple pitfall categories (P1, P2, P3…)
- Each criterion scored on binary (Yes/No) or ordinal (1–5) scales
- Papers independently annotated by **3 reviewers** (Aicha, Noura, Rita)
- Inter-rater reliability computed on merged dataset (1,700+ annotation rows)

### Pitfall Categories Evaluated
| Code | Pitfall | Description |
|---|---|---|
| P1 | Base Rate Fallacy | TPR reported without FPR/base-rate context |
| P2 | Class Imbalance | Handling of skewed class distributions |
| P3 | Evaluation Metrics | Completeness of reported metrics |
| … | … | … |

## 📊 Dataset Structure

| File | Description |
|---|---|
| `criterias.csv` | Full rubric — all pitfall questions, response types, scoring scales |
| `aicha_trimmed.csv` | Aicha's annotations (30 papers) |
| `noura_trimmed.csv` | Noura's annotations |
| `rita_trimmed.csv` | Rita's annotations |
| `merged 2.csv` | Combined dataset (1,741 rows) with inter-rater difference scores |

## 🔑 Key Findings
- Many IDS papers report high TPR (e.g. 98%) **without** contextualizing with FPR or base rates — base rate fallacy is prevalent
- Confusion matrices are frequently absent or incomplete
- Inter-annotator agreement analysis revealed consistent scoring patterns across reviewers for binary criteria; ordinal criteria showed expected variance

## 🛠️ Tech Stack
`Python` · `pandas` · `NumPy` · `scikit-learn` · `Matplotlib` · `Seaborn` · `Jupyter Notebook`

## 💼 Relevance to Industry
- **Fraud detection**: same pitfalls apply to financial anomaly detection models
- **AI governance**: framework adaptable for auditing ML model reporting quality
- **Security engineering**: improves evaluation standards for production IDS deployments

## 📚 Academic Context
- Course: **CSI 4900 — Honours Project**, University of Ottawa
- Domain: Machine Learning · Cybersecurity · Research Methodology
- Grounded in IDS/ML literature (NSL-KDD, CICIDS benchmarks)

## 🚀 Run Locally
```bash
git clone https://github.com/aichalf/CSI4900-Project
pip install pandas numpy matplotlib seaborn scikit-learn jupyter
jupyter notebook
```

## 👩‍💻 Author
**Aicha Lfakir** · [LinkedIn](https://linkedin.com/in/aicha-lfakir) · [GitHub](https://github.com/aichalf)

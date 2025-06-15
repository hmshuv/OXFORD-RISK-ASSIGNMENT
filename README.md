# Investor Personality × Portfolio Analysis  
Oxford Risk — Internship Task  
author: **\Himanshu Gupta**

---

## Project Overview
This repo contains all the artefacts produced for Oxford Risk’s two-dataset analysis assignment:

1. **personality.csv** – 297 rows, one per investor, five psychometric traits (`confidence`, `risk_tolerance`, `composure`, `impulsivity`, `impact_desire`) + `personality_id`.
2. **assets_data.csv** – 786 rows, one per asset holding, six financial fields (`asset_allocation`, `asset_value`, `asset_currency`, …) + `asset_id` (foreign-key ↔ `personality_id`).

The notebooks, report files, and README explain how raw data become the final insights and visuals.

---

## Repository Contents

| File / folder | What it is | How to use it |
|---------------|------------|---------------|
| **Main_analysis_script.ipynb** | Fully-commented Jupyter notebook that walks through data passport, EDA, PCA, t-SNE, clustering, risk metrics, anomaly detection, robustness tests. | **Run this first** in Jupyter / VS Code. Every plot is saved to `fig_*`. |
| **REPORT.pdf** | Polished write-up (11 sections) with embedded figures and tables. | Quick read for reviewers; no code needed. |
| **COVER_LETTER.docx** | Short motivation letter for the internship application. | Open in Word / LibreOffice if you need to edit. |
| **README.md** | *You’re reading it.* | Explains repo structure. |
| **assets_data.csv** | Asset-level dataset (one row per holding). | Loaded in the notebook via `pd.read_csv`. |
| **personality.csv** | Investor-level dataset (one row per person). | Loaded in the notebook via `pd.read_csv`. |
| **.ipynb_checkpoints/** | Jupyter auto-backup files. | Can be ignored. |
| **.DS_Store** | macOS Finder metadata. | Safe to delete; included by default. |

---

## ⚙️ Quick-start

```bash
# 1. create & activate environment (conda or venv)
conda create -n oxford_risk python=3.10
conda activate oxford_risk

# 2. install dependencies
pip install pandas numpy matplotlib seaborn scikit-learn scipy statsmodels python-docx

# 3. launch notebook
jupyter lab  # or jupyter notebook
s
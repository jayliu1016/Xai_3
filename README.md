[![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/jayliu1016/Xai_3/blob/main/notebooks/analysis.ipynb)
# Ames Housing — PDP, ICE, ALE (Colab-ready)
## use GPT5 at 2：00 a.m. for formatting the readme.
This repo contains a Google Colab notebook that:
- runs basic EDA (missingness, distribution),
- examines **correlation** (heatmap) and **VIF**,
- trains a simple tree model (Random Forest),
- produces **PDP**, **ICE**, **ALE** (1D) and **2D PDP**,
- summarizes **PDP vs ICE vs ALE**, correlation impact, and limitations.

> No API keys are required. Data file is committed inside `data/`.

---

## 🔗 Open in Google Colab

[![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](
https://colab.research.google.com/github/jayliu1016/Xai_3/blob/main/notebooks/analysis.ipynb)

If your default branch changes (e.g., not `main`), adjust the link accordingly.

---

## 📁 Project structure

Xai_3/
├─ data/
│ └─ AmesHousing.csv
├─ notebooks/
│ └─ analysis.ipynb
├─ requirements.txt
└─ README.md


- **Data**: single CSV `data/AmesHousing.csv` (≈1 MB).  
- **Notebook**: `notebooks/analysis.ipynb` is Colab-ready.

---

## ▶️ Quick start

### Option A — Run on Colab (recommended)
1. Click the **Colab** badge above.
2. Run the first cell to install small extras (`PyALE`/`statsmodels`).
3. Execute cells top-to-bottom.  
   - The notebook first tries local `data/AmesHousing.csv`.
   - If not present in the Colab runtime, it reads from the repo’s **raw** URL.

### Option B — Run locally
```bash
python -m venv .venv
source .venv/bin/activate   # Windows: .venv\Scripts\activate
pip install -r requirements.txt
jupyter lab  # or: jupyter notebook

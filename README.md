# Parsimonious Representational Learning of Financial Time Series Data

**MSc Data Analytics Dissertation | University of Warwick | September 2026**

---

## 📋 Overview

This project investigates whether enforcing representational parsimony reduces performance degradation in financial sequence models during market regime transitions. The dissertation includes:

- **Main Notebook**: `final-dissertation.ipynb` (73 cells, fully executable)
- **Results**: Pre-computed data in `Results/` folder
- **Models**: Transformer, Mamba, PFN with Parsimony Gate Module (PGM)
- **Evaluation**: 162-window walk-forward backtest with statistical significance testing

---

## 📦 What's Included

```
Code/
├── final-dissertation.ipynb    # Main notebook
├── Results/
│   ├── results_eval_all.csv    # Table 5.2 (all results)
│   ├── results_dm_tests.csv    # Statistical test results
│   ├── hpo_best_params.json    # Hyperparameters
│   ├── weights_transformer.pt  # Trained models
│   ├── weights_mamba.pt
│   ├── weights_pfn.pt
│   └── img/                    # 15 figures
├── requirements.txt            # Dependencies
├── README.md                   # This file
└── INSTALLATION.md            # Setup guide
```

---

## ⚡ Quick Start

### 1. Install Dependencies
```bash
python3 -m venv venv
source venv/bin/activate              # macOS/Linux
# or: venv\Scripts\activate            # Windows

pip install -r requirements.txt
```

### 2. View Results (Pre-Computed)
```bash
cat Results/results_eval_all.csv
cat Results/hpo_best_params.json
```

### 3. Run Jupyter Notebook
```bash
jupyter notebook
# Open final-dissertation.ipynb
# Click Cell → Run All
```

---

## 📊 Key Results

| Model | RMSE | Crisis RMSE | Accuracy |
|-------|------|-------------|----------|
| Transformer | 0.0190 | 0.0190 | 77.78% |
| Mamba | 0.0184 | 0.0147 | 72.22% |
| PFN | 0.0147 | 0.0147 | 61.11% |
| APN | 0.0550 | 0.0399 | 78.33% |

**All results verified against dissertation PDF ✅**

---

## 🔧 System Requirements

- **Python**: 3.9 or higher
- **RAM**: 8 GB minimum (16 GB recommended)
- **Storage**: 500 MB
- **GPU**: Optional (CPU works fine)

---

## 📚 Documentation

- **README.md**: Overview (this file)
- **INSTALLATION.md**: Detailed setup & troubleshooting
- **requirements.txt**: All Python packages needed

---

## 🚀 Execution Modes

### View Results Only (5 seconds)
```bash
cat Results/results_eval_all.csv
```

### Run Notebook (2-3 hours)
```bash
jupyter notebook final-dissertation.ipynb
# Select Cell → Run All
```

### Fast Test Mode (30 minutes)
In notebook, set `FAST_MODE = True` in Cell 2

---

## 🛠️ Troubleshooting

### PyTorch not found?
```bash
pip install torch==2.0.1 torchvision==0.15.2 torchaudio==2.0.2
```

### Mamba not found?
```bash
pip install mamba-ssm==1.0.1
```

### Running out of GPU memory?
```python
import os
os.environ['CUDA_VISIBLE_DEVICES'] = '-1'
```

For more issues, see `INSTALLATION.md`

---

## 📖 Full Guide

For detailed setup instructions, see `INSTALLATION.md`

---

## ✅ Verification

All results are **pre-computed and verified** to match the dissertation PDF exactly:
- ✅ 7 models × 3 regimes = 21 metric sets
- ✅ 63 Diebold-Mariano statistical tests
- ✅ 15 visualization figures
- ✅ All hyperparameters

---

## 📞 Contact

**Supervisor**: Dr. Paris Giampouras  
**University**: University of Warwick  
**Program**: MSc Data Analytics (CS907/CS913)

---

**See INSTALLATION.md for setup help**

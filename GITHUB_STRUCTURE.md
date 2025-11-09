# 📁 GitHub Repository Structure Guide

This document explains which files should and should NOT be pushed to GitHub.

---

## ✅ FILES TO PUSH TO GITHUB

### Core Code Files
- ✅ `main.py` - FastAPI backend
- ✅ `engine.py` - RAG recommendation engine
- ✅ `app.py` - Streamlit frontend
- ✅ `scraper.py` - Data scraper
- ✅ `build_vector_store.py` - Vector store builder
- ✅ `url_extractor.py` - URL text extraction utility

### Utility Scripts
- ✅ `generate_test_predictions.py` - CSV generator for submission
- ✅ `evaluate_performance.py` - Performance evaluation script
- ✅ `validate_api.py` - API validation script
- ✅ `run_full_validation.py` - Full system validation

### Configuration Files
- ✅ `requirements.txt` - Python dependencies
- ✅ `.gitignore` - Git ignore rules
- ✅ `README.md` - Project documentation
- ✅ `SOLUTION_APPROACH.md` - 2-page technical report

---

## ❌ FILES NOT TO PUSH TO GITHUB

### Excluded by `.gitignore`:

#### Data Files
- ❌ `data/` - Contains scraped data and vector indices
- ❌ `*.csv` - All CSV files (including test data)
- ❌ `*.bin` - FAISS index files
- ❌ `*.pkl` - Pickle files

#### Validation & Submission Files
- ❌ `docs/validation/` - All validation reports
- ❌ `submission/` - Submission files and packages

#### Environment & Secrets
- ❌ `.env` - Environment variables (API keys)
- ❌ `.env.local` - Local environment overrides

#### Test Files
- ❌ `test_cases.xlsx` - Test dataset
- ❌ `Gen_AI_Dataset.xlsx` - Source dataset

#### Build & Lock Files
- ❌ `uv.lock` - UV lock file
- ❌ `pyproject.toml` - Project configuration (if using uv)
- ❌ `__pycache__/` - Python cache
- ❌ `*.pyc` - Compiled Python files

#### IDE & OS Files
- ❌ `.vscode/` - VS Code settings
- ❌ `.idea/` - IntelliJ/PyCharm settings
- ❌ `.DS_Store` - macOS files
- ❌ `Thumbs.db` - Windows files

---

## 📂 FOLDER STRUCTURE

```
SHL/
├── 📄 Core Code Files (✅ Push to GitHub)
│   ├── main.py
│   ├── engine.py
│   ├── app.py
│   ├── scraper.py
│   ├── build_vector_store.py
│   └── url_extractor.py
│
├── 📄 Utility Scripts (✅ Push to GitHub)
│   ├── generate_test_predictions.py
│   ├── evaluate_performance.py
│   ├── validate_api.py
│   └── run_full_validation.py
│
├── 📄 Documentation (✅ Push to GitHub)
│   ├── README.md
│   └── SOLUTION_APPROACH.md
│
├── 📄 Configuration (✅ Push to GitHub)
│   ├── requirements.txt
│   └── .gitignore
│
├── 📁 data/ (❌ NOT in GitHub - in .gitignore)
│   ├── shl_assessments.csv
│   ├── faiss_index.bin
│   └── index_to_data.pkl
│
├── 📁 docs/validation/ (❌ NOT in GitHub - in .gitignore)
│   └── [All validation reports]
│
└── 📁 submission/ (❌ NOT in GitHub - in .gitignore)
    ├── system_summary.json
    ├── create_submission_package.py
    └── submission_predictions.csv (generate this)
```

---

## 🚀 GitHub Push Checklist

Before pushing to GitHub, verify:

- [ ] `.env` file is NOT in repository (check `.gitignore`)
- [ ] `data/` folder is NOT in repository
- [ ] `docs/validation/` is NOT in repository
- [ ] `submission/` is NOT in repository
- [ ] All CSV files are excluded
- [ ] `README.md` is present and complete
- [ ] `requirements.txt` is present and up-to-date
- [ ] `.gitignore` is properly configured

---

## 📝 Quick Commands

### Check what will be pushed:
```bash
git status
```

### Verify .gitignore is working:
```bash
git status --ignored
```

### Add files (respects .gitignore):
```bash
git add .
```

### Commit:
```bash
git commit -m "Initial commit: SHL Assessment Recommendation System"
```

### Push:
```bash
git push origin main
```

---

## ⚠️ Important Notes

1. **Never commit `.env` files** - They contain API keys
2. **Data files are large** - Keep them local, not in GitHub
3. **Validation reports** - Keep locally for reference
4. **Submission files** - Generate locally, submit separately

---

## ✅ Recommended GitHub Repository Contents

Your GitHub repo should contain:
- ✅ All Python source code
- ✅ `README.md` with setup instructions
- ✅ `SOLUTION_APPROACH.md` (technical report)
- ✅ `requirements.txt`
- ✅ `.gitignore`
- ✅ Utility scripts for testing/validation

**Total size should be small** (code + docs only, no data files).


# AGENTS.md — AI Contribution Policy for Integration-1-Dev-Environment

## 1. Testing Requirements
Before any AI-assisted change is committed, ensure:

- All changes pass `python test_environment.py`.
- Any code added to `src/` has a corresponding test in `tests/`.
- Run all tests with:

pytest tests/ -v
Changes must be reproducible: running the code produces the expected results without errors.

## 2. Secrets Policy

Do not include or commit any sensitive information:

* API keys, database passwords, or file paths containing personal data.
* Raw data (e.g., original CSV files) must not appear in prompts or commits.
* Files to never commit:

# Python
__pycache__/
*.pyc
*.pyo

# Jupyter
.ipynb_checkpoints/

# Virtual environment:
.venv/

# Secrets and credentials
.env
*.key
*.pem

# Data files (never commit raw data to Git)
*.csv
*.parquet
*.xlsx
data/raw/

# OS artifacts
.DS_Store
Thumbs.db

## 3. Scope Boundaries

Define what AI agents can and cannot edit:

Allowed for AI edits:

  * `src/` — production code modules
  * `notebooks/` — exploratory analysis notebooks

Do not modify without human review:

  * `requirements.txt`
  * `setup.sh` (unless tested locally)
  * `.gitignore` (verify it does not exclude source files)
  * `CHANGELOG.md` (ensure dates and notes are accurate)

## 4. Reproducibility Standard

AI-assisted changes are only considered complete if:

* The change runs locally first and produces the expected output.
* "AI-generated" does not replace executing the code.

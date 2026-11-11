# Club Expense Claim Checker — Capstone V2

CIT AI-Native Engineering Programme · Semester 1 · Assessment 5

A console Python prototype that extracts claim details with an LLM, independently checks facts in Python,
applies ordered rules and club budgets, and writes four reports. **It never makes or authorizes payments.**

## Setup (Windows / VS Code)
1. Install Python 3.10+.
2. Open this folder in VS Code.
3. In the terminal:
   ```powershell
   py -m venv .venv
   .venv\Scripts\Activate.ps1
   py -m pip install -r requirements.txt
   ```
4. Copy `.env.example` to `.env`, add your private API key, and keep `.env` out of GitHub.
5. Test offline:
   ```powershell
   py app.py --demo
   ```
6. Run with the LLM:
   ```powershell
   py app.py
   ```
   If the API call fails, local fallback extraction is used and logged.

## Tests
```powershell
py -m unittest discover -s tests -v
```

## Files
- `data/claims.csv` — 23 sample claims, date ordered
- `data/budgets.csv` — per-category limits, applied separately to each club
- `submission/` — spec, prompt, evaluation/red-team, judgment framework, cost note, AI journal and reflection draft
- `output/` — generated results.csv, payable.csv, review.csv and summary.txt

## Important
- Edit the sample CSVs to use your faculty-approved claims and budgets.
- Review every output. LLM extraction and local fallback can be wrong.
- A split claim is a possible pattern, not proof of misconduct.
- The faculty treasurer must inspect the original bill and sign every payment.
- The reflection is a draft: personalize it with your actual work and learning before submission.
- Add at least three meaningful Git commits; suggested sequence: initial structure, extraction/validation, rules/reports/tests/docs.

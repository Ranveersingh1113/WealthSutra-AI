# WealthSutra AI

FastAPI backend + single-page frontend for financial score, FIRE projection, and AI chat guidance.

## Setup
1. Create and fill environment variables:
   ```bash
   cp .env.example .env
   ```
2. Export the required variable:
   ```bash
   export GROQ_API_KEY="<your-key>"
   ```
3. Install dependencies and run:
   ```bash
   pip install -r requirements.txt
   uvicorn app:app --reload
   ```

## Required environment variables
- `GROQ_API_KEY`: Groq API token used by `/chat` and AI suggestions in `/analyze`.

## Repository hygiene process
- PR and issue workflow rules: [`CONTRIBUTING.md`](CONTRIBUTING.md)
- Maintainer branch/settings checklist: [`docs/repo-maintenance-checklist.md`](docs/repo-maintenance-checklist.md)

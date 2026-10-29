# Resume Match Analyzer

> Score a resume against a job description and show what is missing.

Hack Day Haldia x GRID community - 6-hour build challenge

**Repo:** `team-phoenix` | **Stack:** Python / Flask | **Difficulty:** Medium-Hard | **Time:** 6 hours

## Brief
Applicants rarely know why they get filtered out. Build a tool that compares a resume with a job description and explains the gaps.

## Core tasks (must-do)
- [ ] Paste resume text and a job description
- [ ] Extract skills and keywords from both (skills dictionary + tokenisation)
- [ ] Match % with matched vs missing skills
- [ ] Section checks: contact info, education, projects, length
- [ ] Results view: score gauge, missing skills and concrete improvement tips
- [ ] Save analyses in SQLite, show a history list and compare two analyses
- [ ] Validate input (empty / very long text) with clear error messages

## Bonus tasks (only after the core works)
- [ ] PDF upload with text extraction
- [ ] AI (open model) rewrite suggestions for weak bullet points
- [ ] Tailored cover-letter draft
- [ ] Printable report view

## What is already here
- `index.html` - base page that pings `/api/health`
- `app.py` - Flask app with a SQLite helper (`db()`, `init_db()`), `/api/health` and TODO endpoint stubs (they return 501 until you implement them)
- `requirements.txt` - `flask`, `gunicorn`

## Run locally
```bash
pip install -r requirements.txt
python app.py   # then open http://127.0.0.1:5000
```

## Deploy
Any Python host works (for example Render or PythonAnywhere). Start command: `gunicorn app:app`. Free hosts may reset the filesystem on restart, so the SQLite file can reset - fine for a demo.

## Suggested pacing
- Hour 1: read this README, agree on a plan and split the work
- Hours 2-4: build the core tasks
- Hour 5: integrate, polish, then bonus tasks if time allows
- Hour 6: deploy, open the Pull Request, submit on the MLH platform (OrganizerHQ)

## Submission checklist
- [ ] All core tasks work end to end
- [ ] Project is deployed and the live link opens
- [ ] Pull Request created on the Voyage GitHub repository assigned to your team
- [ ] Project submitted on the MLH platform (OrganizerHQ) - instructions are shared at the start of the event

## Rules
- Build new features on top of this starter project and integrate them.
- Teams of 3-4; every member must be present.
- AI tools and open-source / open-weight models are fully allowed.

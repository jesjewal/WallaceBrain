---
name: NotebookLM Skill Capabilities
description: Full script inventory for the NotebookLM skill — what can be done autonomously vs. what requires user action
type: reference
---

## Skill Location
`/Users/wallace/.claude/skills/notebooklm/`

## Always use `python3 scripts/run.py [script]` — never call scripts directly

---

## Scripts Available (verified 2026-04-18)

| Script | What it does | Autonomous? |
|---|---|---|
| `auth_manager.py status` | Check auth status | Yes |
| `auth_manager.py setup` | Authenticate (opens browser for Google login) | Needs user to log in |
| `create_notebook.py` | Creates a new NotebookLM notebook via browser automation | **Yes — fully autonomous** |
| `notebook_manager.py list` | List all notebooks in library | Yes |
| `notebook_manager.py add` | Register an existing notebook URL into local library | Yes |
| `notebook_manager.py activate` | Set active notebook | Yes |
| `notebook_manager.py search` | Search library by topic | Yes |
| `notebook_manager.py remove` | Remove from library | Yes |
| `ask_question.py` | Query a notebook and get source-grounded answer | Yes |
| `cleanup_manager.py` | Clean browser state/data | Yes |

## create_notebook.py — Key Flags
```bash
python3 scripts/run.py create_notebook.py \
  --name "Notebook Title" \
  --add-to-library \
  --description "What it contains" \
  --topics "topic1,topic2,topic3"
```
- Creates notebook, captures URL, optionally adds to library in one step
- Title-setting may fail silently (NotebookLM UI quirk) — rename manually if needed
- Returns the full notebook URL on success

## What CANNOT be done autonomously
- **Uploading source files** — no `upload_source.py` script exists; user must upload docs to NotebookLM manually via the UI
- **Adding web URLs as sources** — same limitation; requires UI interaction
- After creating a notebook, Jesse must add sources manually before querying yields useful results

## Why: I incorrectly told Jesse I couldn't create notebooks on 2026-04-18. The create_notebook.py script exists and works. Always check scripts/ before claiming a capability doesn't exist.

## Active Notebooks of Note
- **Executive Cover Letter Grading** — ID: `executive-cover-letter-grading`, URL: https://notebooklm.google.com/notebook/e6efec3e-38d3-4b45-bbb5-86645adc3358 — needs research doc uploaded as source before querying
- Research doc to upload: `/Users/wallace/Downloads/Executive_CoverLetter_Grading_Framework.md`

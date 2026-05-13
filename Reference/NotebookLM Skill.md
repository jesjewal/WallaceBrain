---
tags: [reference, notebooklm, tools]
---

# NotebookLM Skill

**Location:** `~/.claude/skills/notebooklm/`
**Always use:** `python3 scripts/run.py [script]` — never call scripts directly.

## Scripts

| Script | What it does | Autonomous? |
|---|---|---|
| `auth_manager.py status` | Check auth status | Yes |
| `auth_manager.py setup` | Authenticate (opens browser) | Needs user login |
| `create_notebook.py` | Create new notebook via browser automation | Yes |
| `notebook_manager.py list` | List all notebooks in library | Yes |
| `notebook_manager.py add` | Register existing notebook URL | Yes |
| `notebook_manager.py activate` | Set active notebook | Yes |
| `notebook_manager.py search` | Search library by topic | Yes |
| `ask_question.py` | Query a notebook | Yes |

## create_notebook.py
```bash
python3 scripts/run.py create_notebook.py \
  --name "Notebook Title" \
  --add-to-library \
  --description "What it contains" \
  --topics "topic1,topic2,topic3"
```

## Cannot be done autonomously
- Uploading source files — must do manually in NotebookLM UI
- Adding web URLs as sources — same limitation

## Active Notebooks
- **Executive Cover Letter Grading** — `executive-cover-letter-grading`
  - Needs `Executive_CoverLetter_Grading_Framework.md` uploaded as source

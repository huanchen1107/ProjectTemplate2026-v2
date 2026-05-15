# 2026FintechSMC

> **⚠️ MEMO (2026.05.15)**: CC Switch is currently **not working**. Do not use it.
> This project runs exclusively via the **`free-claude-code` local proxy** with API keys configured in `.env`.
> Simply run `./cc.sh` to start.

## 🚀 Quick Start

```bash
./initial.sh   # Bootstrap a new project (disconnect from template)
./startup.sh   # Initialize session + launch Claude Code
./ending.sh    # Commit, push, and finalize session
```

## 🤖 How it Works

`startup.sh` → reads `project_initial.md` → launches `cc.sh` → interactive menu.

## 📜 Shell Scripts Reference

| Script | Purpose |
| :--- | :--- |
| `cc.sh` | **Unified Launcher**: Manages the local proxy and provides a model selection menu. |
| `startup.sh` | **Session Start**: Prepares the environment and launches `cc.sh`. |
| `ending.sh` | **Session End**: Updates development logs, commits changes, and pushes to remote. |
| `initial.sh` | **Project Bootstrap**: Resets Git, runs cleanup, and creates a new GitHub repository. |
| `cleanAll.sh` | **Hard Reset**: Wipes logs/history and re-initializes core files for a fresh start. |

## 📁 Project Structure

```
.
├── cc.sh              # Unified launcher (proxy + model selection)
├── startup.sh         # Session start: reads project goals + launches cc.sh
├── ending.sh          # Session end: update logs + commit + push
├── initial.sh         # New project bootstrap script
├── cleanAll.sh        # Project reset & cleanup utility
├── .env               # API keys (GIT IGNORED)
├── .env.bak           # Template for .env (no keys)
├── 2026.05.15開發日誌.md  # Daily dev log
└── user/dialog.md     # Auto-reconstructed conversation history
```

## 🛠 Setup

1. **API Keys**: Copy `.env.bak` to `.env` and fill in your keys.
   ```bash
   cp .env.bak .env
   ```
2. **Prerequisites**:
   - `uv` — Python package manager (`brew install uv`)
   - `npx` / Node.js — for Claude Code CLI
   - `free-claude-code` proxy at `~/free-claude-code/`
   - OpenRouter API key in `.env`


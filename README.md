<div align="center">

# 🤖 Kelmo

**Lightweight, fast, and extensible AI Terminal Assistant for Windows**

[![Windows](https://img.shields.io/badge/Platform-Windows%2010%20%7C%2011-blue?logo=windows)](https://github.com)
[![License](https://img.shields.io/badge/License-MIT-green)](LICENSE)
[![Architecture](https://img.shields.io/badge/Architecture-x64-orange)](#)

</div>

---

## ⚡ Quick Start

1. Download **`kelmo.exe`** from the latest release or **`curl -L -O https://github.com/knowfov/Kelmo/releases/download/1.0.0/kelmo.exe`**.
2. Double-click **`kelmo.exe`** to start.
   - On the first launch, Kelmo automatically creates shortcuts on your **Desktop** and in your **Start Menu ("Пуск")**.
3. Connect your preferred AI provider:
   - Type `/api` inside Kelmo to select **OpenRouter, DeepSeek, OpenAI, Anthropic, Google Gemini**, or local **Ollama**.
   - Paste your API key, pick a model, and start coding immediately!

---

## 🎯 Key Features

- **Zero-Setup Execution**: Standalone executable with embedded runtime. No heavy 4GB local models required to get started.
- **Multi-Provider API Support**:
  - DeepSeek (V3, R1)
  - OpenRouter (hundreds of models)
  - Anthropic (Claude 3.5 Sonnet, Claude 3 Opus)
  - OpenAI (GPT-4o, o1, o3-mini)
  - Google Gemini (Gemini 2.0 Flash / Pro)
  - Local Ollama endpoints
- **Modular Skills Engine**:
  - Located in `skills/` or `~/.kelmo/skills/`.
  - Ships with `skill-creator` to scaffold and design custom agent behaviors with Python and PowerShell.
- **Interactive Terminal UI**:
  - Real-time reasoning visualization (`thought for Xs`).
  - Command palette (`/help`, `/skills`, `/api`, `/model`, `/clear`, `/status`).
  - Tab autocompletion for commands, skills, and file paths.

---

## 🧩 Skills System (`skills/skill-creator`)

Kelmo includes a built-in skill authoring framework:

```
skills/
└── skill-creator/
    ├── SKILL.md                 # Full English guide & prompt instructions
    └── scripts/
        ├── create_skill.py      # Python skill scaffolding tool
        └── create_skill.ps1     # PowerShell skill scaffolding tool
```

### Creating a New Skill

Using PowerShell:
```powershell
.\skills\skill-creator\scripts\create_skill.ps1 -Name "git-assistant" -Description "Automates Git commits and branch workflows"
```

Using Python:
```bash
python skills/skill-creator/scripts/create_skill.py --name "git-assistant" --desc "Automates Git commits and branch workflows"
```

Read [`skills/skill-creator/SKILL.md`](skills/skill-creator/SKILL.md) for full documentation on defining custom tool instructions, schemas, and script runners.

---

## 🕹️ Essential Commands

| Command | Description |
|---|---|
| `/api` | Connect official APIs (DeepSeek, OpenRouter, Anthropic, OpenAI, Gemini) |
| `/skills` | List all discovered skills and their descriptions |
| `/model` | Switch between active models |
| `/clear` | Clear conversation history and reset context |
| `/compact` | Compact session history into a concise summary |
| `/cost` | Display session token usage and estimated cost |
| `/status` | View connection status, active model, and account info |
| `/help` | View help and full command reference |

---

## 📄 License

MIT License. Built for developers who want a fast, focused AI assistant directly in their terminal.

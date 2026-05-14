# ✨ Free Claude Code — Powered by MiniMax M2.5

![GitHub stars](https://img.shields.io/github/stars/network-tocoder/free-claude-code-minimax?style=for-the-badge&color=orange)
![License](https://img.shields.io/badge/License-MIT-green?style=for-the-badge)
![Platform](https://img.shields.io/badge/Platform-Windows%20%7C%20Mac%20%7C%20Linux-blue?style=for-the-badge)
![Cost](https://img.shields.io/badge/Cost-Zero-brightgreen?style=for-the-badge)
![Model](https://img.shields.io/badge/Model-MiniMax%20M2.5%20Free-orange?style=for-the-badge)

> **Run the real Claude Code from Anthropic — powered by MiniMax M2.5 Free via OpenCode Zen. Opus-level intelligence inside VS Code. Zero cost.**

---

## 📺 Watch the Full Video

[![Watch on YouTube](https://img.shields.io/badge/▶_Watch_on_YouTube-FF0000?style=for-the-badge&logo=youtube&logoColor=white)](https://www.youtube.com/watch?v=9isp3o4mdsg)

> *Free Claude Code is Here — MiniMax 2.5 = Opus 4.6 (VS Code Integration)*

---

## ⚡ What Is This?

Configure the **official Claude Code from Anthropic** to use **MiniMax M2.5 Free** through **OpenCode Zen** — no Anthropic subscription, no paid API. Includes the **VS Code extension** for a full IDE experience.

| Tool | Role |
|------|------|
| 🤖 **Claude Code** | Anthropic's official AI coding agent |
| 🐋 **MiniMax M2.5 Free** | Opus 4.6-level model — completely free |
| ⚡ **OpenCode Zen** | API gateway that routes requests to MiniMax |
| 💻 **VS Code Extension** | Native diff viewer, file mentions, slash commands |

---

## 🎯 Why This Works

| Benchmark | MiniMax M2.5 | Claude Opus 4.6 |
|-----------|--------------|----------------|
| SWE-Bench Verified | **80.2%** | 80.8% |
| SWE-Bench Pro | **55.4%** | 54.1% |
| Cost | **$0** | $25 / M tokens |

Same tier of intelligence. Zero cost during OpenCode Zen's free preview.

---

## 🖥️ Requirements

| Requirement | Detail |
|------------|--------|
| OS | Windows / Mac / Linux |
| Node.js | v18 or higher (v24 recommended) |
| VS Code | Latest (for extension setup) |
| GPU | ❌ Not required |
| API Key | Free — opencode.ai/zen |

---

## 🚀 Installation Guide

### Step 1 — Verify Prerequisites

```bash
node --version
npm --version
```

Need Node v18+. If lower, upgrade below.

<details>
<summary>🪟 Windows — Install / Upgrade Node.js</summary>

```powershell
winget install OpenJS.NodeJS
```
Close PowerShell, open a fresh one, then verify with `node -v`.
</details>

<details>
<summary>🍎 macOS — Install / Upgrade Node.js</summary>

```bash
brew install node
node --version
```
</details>

<details>
<summary>🐧 Linux — Install / Upgrade Node.js</summary>

```bash
sudo apt update
sudo apt install nodejs npm
node --version
```
</details>

---

### Step 2 — Get Your Free OpenCode Zen API Key

1. Go to **[opencode.ai](https://opencode.ai)** → click **Zen**
2. Sign in with Google
3. **Skip billing** — we only want the free tier
4. Go to **API Keys** → **Create API Key**
5. Name it (e.g., `claude-code-minimax`)
6. **Copy the key** — save it somewhere safe

---

### Step 3 — Install Claude Code

<details>
<summary>🪟 Windows (PowerShell)</summary>

```powershell
npm install -g @anthropic-ai/claude-code
claude --version
```
</details>

<details>
<summary>🍎 macOS / 🐧 Linux</summary>

```bash
npm install -g @anthropic-ai/claude-code
claude --version
```
</details>

You should see version `2.1.x` or higher.

---

### Step 4 — Configure Claude Code

Create the `.claude` folder and `settings.json` file.

<details>
<summary>🪟 Windows (PowerShell)</summary>

```powershell
mkdir "$env:USERPROFILE\.claude" -Force
notepad "$env:USERPROFILE\.claude\settings.json"
```
</details>

<details>
<summary>🍎 macOS / 🐧 Linux</summary>

```bash
mkdir -p ~/.claude
nano ~/.claude/settings.json
```
</details>

**Paste this config** (replace `YOUR_ZEN_API_KEY` with your key from Step 2):

```json
{
  "env": {
    "ANTHROPIC_BASE_URL": "https://opencode.ai/zen",
    "ANTHROPIC_API_KEY": "YOUR_ZEN_API_KEY",
    "ANTHROPIC_AUTH_TOKEN": "",
    "ANTHROPIC_MODEL": "minimax-m2.5-free"
  }
}
```

Save and close.

---

### Step 5 — Launch Claude Code

```bash
cd your-project-folder
claude
```

- Pick your theme
- Trust the folder
- Confirm custom API config → **Yes**

Look at the bottom bar — it should show `minimax-m2.5-free`. ✅

---

### Step 6 — Verify the Model

Inside Claude Code:

```
/model
```

You should see `minimax-m2.5-free ✓` at the bottom of the list. If not, select it.

**Test it:**

```
hey, which model are you?
```

Expected response: *"I'm currently running on minimax-m2.5-free."*

---

## 💻 VS Code Extension Setup

### Step 1 — Install the Extension

1. Open VS Code
2. Open Extensions tab (`Ctrl+Shift+X`)
3. Search for **Claude Code**
4. Install the official one from **Anthropic** (verified ✓)

---

### Step 2 — Launch Claude Code Panel

1. Click the **Claude Code icon** in the sidebar
2. Click **New Session**
3. The panel opens — it auto-picks up your `settings.json` config
4. MiniMax is already loaded ✅

---

### Step 3 — Try the Power Features

| Feature | How |
|---------|-----|
| **File mentions** | Type `@filename` in chat |
| **Selection prompts** | Highlight code → right-click → Ask Claude |
| **Native diff viewer** | Edits open in side-by-side diff |
| **Slash commands** | Type `/` to see all commands |
| **Model switcher** | Click model name in panel → Switch model |

---

## 🧪 Real Use Case — Codebase Review

Clone Express.js as a test repo:

```bash
git clone https://github.com/expressjs/express.git review-target
cd review-target
claude
```

**Enable Plan mode (read-only):**

```
/plan
```

**Prompts to try:**

```
Share a complete overview of this codebase. What does it do, how is it structured, and what are the main components?
```

```
Review this codebase for code quality issues, potential improvements, and technical debt. Be specific — mention file names and line numbers.
```

**Switch to default mode** (allows edits):

Press `Shift + Tab` to cycle out of plan mode.

**Apply a fix:**

```
Based on your review, pick the most straightforward improvement and implement it. Show me exactly what you're changing and why before you do it.
```

Approve the diff — Claude Code applies the change.

---

## 🔧 Useful Slash Commands

| Command | Purpose |
|---------|---------|
| `/model` | Switch between models |
| `/plan` | Toggle plan mode (read-only) |
| `/review` | Run a code review |
| `/security-review` | Security audit on current files |
| `/simplify` | Refactor for clarity |
| `/usage` | Show token usage + cost |
| `/clear` | Clear conversation context |
| `/compact` | Compress conversation history |

Cycle agent modes with **`Shift + Tab`**:
- 📖 Plan (read-only)
- 💬 Default (asks before editing)
- ⚡ Auto-accept (no prompts)

---

## 🐛 Troubleshooting

| Error | Fix |
|-------|-----|
| `claude not recognized` | Open a fresh terminal, or add npm global path to PATH |
| `Auth conflict: Both AUTH_TOKEN and API_KEY set` | Run `claude /logout`, restart terminal |
| `API error / connection failed` | Check API key in `settings.json` is correct |
| `Model still shows Opus 4.7 / Sonnet` | Run `/model` and manually select MiniMax |
| `Retrying in 0 ms - attempt 5/10` | Free tier rate-limited at peak — try off-peak or scope smaller |
| VS Code extension not finding config | Make sure `settings.json` is at `~/.claude/settings.json` |
| `code not recognized` (for opening files) | Install VS Code CLI: open VS Code → `Ctrl+Shift+P` → "Install code command" |

---

## 💡 Tips

- **Free model caveat:** MiniMax M2.5 free is for a limited time during OpenCode Zen's preview. Soft rate limits apply during peak hours
- **Data privacy:** Free models may use prompts to improve the model. Don't send sensitive code or credentials
- **Scope tasks:** For huge codebases, ask Claude to review specific folders (`src/core/`) instead of everything at once
- **Use `.claudeignore`:** Exclude build artifacts, lockfiles, and `node_modules` to reduce context bloat
- **Off-peak hours:** Early morning or late night usually has fewer rate limits
- **Reset config:** If something breaks, delete `~/.claude` and re-do Step 4

---

## 🔗 Related Videos on My Channel

| Video | Topic |
|-------|-------|
| 🎬 Free Claude Code with Nvidia NIM + DeepSeek | Cloud free coding (backup option) |
| 🎬 Claude Code Complete Tutorial (A–Z in 30 min) | Master Claude Code |
| 🎬 Claude Code with Gemma 4 (Local, No GPU) | Run Claude Code with local Gemma |
| 🎬 PI Lightweight Coding Agent | Free coding agent for low-resource setups |

---

## 🔗 Links

[![YouTube](https://img.shields.io/badge/YouTube-NetworkCoder-red?style=for-the-badge&logo=youtube)](https://www.youtube.com/@NetworkCoder)
[![GitHub](https://img.shields.io/badge/GitHub-Follow-black?style=for-the-badge&logo=github)](https://github.com/network-tocoder)
[![Claude Code](https://img.shields.io/badge/Claude_Code-Docs-orange?style=for-the-badge)](https://docs.claude.com/claude-code)
[![OpenCode Zen](https://img.shields.io/badge/OpenCode_Zen-Auth-cyan?style=for-the-badge)](https://opencode.ai/zen)
[![MiniMax](https://img.shields.io/badge/MiniMax-Models-blue?style=for-the-badge)](https://minimax.io/models/text)

---

<p align="center">
  <strong>Zero Cost. Opus-Level Intelligence. Any Machine.</strong><br/>
  <em>Built with Claude Code + OpenCode Zen + MiniMax M2.5 Free</em>
</p>

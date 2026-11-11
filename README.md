# RelVectors — Give Your Computer Its Own AI

[中文](README.zh-CN.md) | **English**

**Put an agent on your computer, and let it get things done.**

Your computer is already powerful. Now it can have its own AI.

RelVectors is an agent that runs on your personal computer. It knows the state of this machine, can spot problems, understand what you ask, and help you get things done through tools you authorize.

**Start by looking after your computer — and let it gradually learn to work on its own.**

---

## First, let it do three things for you

### "Why is my computer getting slower?"
RelVectors checks resource usage and performance, and finds the likely causes.

### "What is taking up all my disk space?"
RelVectors scans your storage and produces cleanup suggestions. Nothing runs until you confirm.

### "Is my computer safe?"
It checks suspicious processes, the firewall and system security settings, so you understand the risks on your machine.

---

## Download RelVectors

Supports Windows, macOS and Linux. Free 7-day trial.

| Version | Details | Download |
|---|---|---|
| **Windows** | 64-bit Intel / AMD · v0.3.6 (10 languages) | **[Download →](https://github.com/relvectors/relvectors-releases/releases/download/v0.3.6/RelVectors-0.3.6-windows-x64.zip)** |
| **Mac** | Apple silicon (M1 / M2 / M3 / M4) · v0.3.6 (10 languages) | **[Download →](https://github.com/relvectors/relvectors-releases/releases/download/v0.3.6/RelVectors-0.3.6-mac-arm64.tar.gz)** |
| **Other systems** | Windows on ARM, Intel Mac, Linux | **[See all packages →](https://github.com/relvectors/relvectors-releases/releases/tag/v0.3.6)** |

The installer bundles everything it needs: **no Python or other software to install, and the install itself needs no internet.**

Requirements: Windows 10 or later; macOS 11 or later; Linux with glibc 2.28 or later (Ubuntu 20.04+, Debian 10+, RHEL / Rocky 8+).

After downloading, use [`SHA256SUMS.txt`](SHA256SUMS.txt) to verify the package.

---

## Your computer, your rules

- **Local first.** Personal files are not uploaded to the cloud by default.
- **You authorize the important actions.** Anything that cannot be undone pops up as a card — it runs only after you click.
- **Everything is on record.** Task logs and check results are always available.
- **Connect other AI agents.** Through MCP / A2A, other agents can work with it on shared tasks.

**RelVectors is not just something to chat with — it belongs to your computer.**

---

## What it actually does

It starts with looking after the machine: cleanup, speed-up, thermal control, security checks, benchmarks, and watching over other computers. Every result comes from real measurements on this machine, not guesses.

### Cleanup and speed-up
Scans app caches, the Trash, old installers, large files, virtual machines, local AI models and app data such as WeChat, and produces a **cleanup checklist** with sizes. Safe items are already ticked; one click does the rest. Caches are deleted (apps rebuild them when needed); everything else goes to the Trash, where you can get it back. **It is not a reinstall, and not a factory reset.**

### Thermal control and hardware health
Monitors processor and disk temperatures and compares them with what is normal for this machine; finds **which programs are heating it up** right now; follows disk health (SMART) over time, so wear shows up before a failure does.

### Performance and local AI
Measures real disk read/write speed and processor performance; a stress test can run up to a 4-hour burn-in while watching temperature and stability; with enough memory it can set up a local AI model (Ollama) so idle computing power does useful work.

### Space and resource analysis
Tells you where your disk space went, the largest folders, which software can be updated, and how much of your processor and memory sits idle.

### Remote and other computers
Pair computers with a one-time invitation code to check another machine's health, run a remote checkup or hand it a task; check servers over SSH with keys you already have; hand a job to another AI agent (Claude Code, Codex and others) and bring the result back.

### Security check
Checks every running program for warning signs (started from a temp or download folder, file deleted while it keeps running, ports open to the network, an unknown program keeping the processor busy, administrator programs in folders anyone can change), then checks the firewall, disk encryption, security updates and backups. **Read-only** — for anything suspicious it tells you what it is, where it is, and what to do.

---

## Also included

- **Chat with your computer.** Ask "How is my computer doing?", "Why is it slow?" or "How much disk space is left?" and get answers from real measurements.
- **Local + cloud AI.** Supports local models (Ollama, oMLX, LM Studio) and cloud models (DeepSeek, Qwen, Kimi, Zhipu, Doubao, OpenAI, Claude, Gemini and more), with a daily budget for cloud models.
- **24/7 health monitoring.** Disk space, memory, temperature, network, disk health, security and backups. A problem is measured twice before you are told, so false alarms do not bother you.
- **Approval cards.** Anything that cannot be undone pops up as a card: approve or refuse with one click.
- **Dashboard.** A live overview of your computer, with dark and light themes.

---

## Install

- **Windows:** unzip, then double-click `install.cmd`. If Windows says it protected your PC, click "More info → Run anyway".
- **macOS:** unpack, then right-click `Install.command` → Open (the first time needs a right-click because the app is not yet notarized by Apple), or run `sh install.sh` in Terminal.
- **Linux:** unpack, then run `sh install.sh` in a terminal.

A **RelVectors** icon appears on your desktop and in the Start menu, Launchpad or app menu. Click it to open RelVectors in your browser. To quit, click "Quit" at the top right; it starts again at your next login or when you click the icon.

## Free trial and activation

- **7 days free**, counting from the first start.
- Then open Settings → License, click "Copy application", and email it to **155570@qq.com** (any subject). An activation code comes back by email automatically.
- Paste the code on the same page. Activation works offline, and the term starts when you first activate.

## For AI agents

RelVectors is the first agent built for the machine itself: other agents work for people, RelVectors speaks for the computer. Hand it the computer's own work and get back real measurements, safe hands (authorization gate, undo, owner approval cards), memory across sessions, and reach to other machines.

- **MCP:** `claude mcp add relvectors -- rv mcp --agent claude-code` (any MCP client: `rv mcp --agent <name>`, stdio)
- **A2A:** Agent Card at `http://127.0.0.1:47100/.well-known/agent-card.json`, JSON-RPC `message/send` at `/a2a`
- **Command line:** `rv --json status`, `rv --json findings`, `rv --json tasks`

Full guide: **[AGENTS.md](AGENTS.md)** · machine-readable index: **[llms.txt](llms.txt)**

## Questions

**Will it delete my files?** Only what you tick in the cleanup list. Caches are deleted (apps rebuild them); everything else goes to the Trash, where you can restore it.

**Does it upload my data?** No. It reads your computer's state on your computer. Your documents are only read in tasks you give it, and are not sent to a cloud AI unless you allow it.

**Does it need the internet or an AI subscription?** The install needs no internet. AI capability can use a local model (Ollama, oMLX, LM Studio) or a cloud model you configure; with a local model, your data stays on this machine.

**Will it slow my computer down?** No. It runs at low priority with very little CPU and memory.

**Is "cleanup" a factory reset?** No. It cleans up and speeds up; nothing is reinstalled and nothing is reset.

---

RelVectors is proprietary software; this repository hosts the installers only. The bundled smartctl comes from smartmontools (GPL); its license is included in the packages. Questions and licenses: 155570@qq.com

*Keywords: AI computer assistant, computer agent, disk cleanup, free up disk space, speed up computer, computer overheating, CPU temperature, hardware health, SMART disk health, suspicious process scanner, security check, remote computer maintenance, local AI, Ollama, AI agent, MCP, A2A, Windows, macOS, Linux.*

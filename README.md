# RelVectors — Your Computer's AI Engineer

**English** | [中文](README.zh-CN.md)

**RelVectors is an AI engineer that lives on your computer.** It keeps an eye on your PC or Mac around the clock, notices
problems before you do, and fixes them when you ask: cleans up disk space, finds what slows your computer down, keeps it
from overheating, checks for suspicious programs, and looks after other computers for you. Just tell it what you want in
plain words. It does the work, shows you the result, and asks you only when a decision is really yours.

Free 7-day trial · Windows, macOS and Linux · works offline with a local AI model · your files stay on your computer

---

## Why RelVectors

- **It does the work, not just the talking.** Say "clean up my disk" and it scans, shows you a checklist, and frees the
  space after one click. You get the before-and-after numbers, not a list of instructions.
- **It knows your computer.** It measures your machine all the time and compares it with its own history, so it can tell
  "slower than usual" or "hotter than usual", not just "high".
- **You stay in control.** Anything that changes your computer is explained first. Anything that cannot be undone needs
  your approval, with one click on a card. You can quit RelVectors at any time.
- **Private by design.** It reads your computer's state, not your documents. Personal files are only touched in tasks you
  give it, and are never sent to a cloud AI by default. It works fully offline with a local model.
- **Light.** It runs quietly in the background with very little CPU and memory, and slows down even more when all is well.

---

## Six features

### 1. Rejuvenate: clean up your computer and make it fast again
*Disk cleanup · free up disk space · speed up PC · junk file cleaner · Mac cleaner*

- One scan finds what really takes your disk space: app caches, the Trash or Recycle Bin, old installers (DMG, ZIP, EXE),
  large downloads, virtual machines, local AI models, and app data such as WeChat.
- You get a **cleanup checklist** with sizes. Safe items (caches) are pre-ticked. One click on "Clean selected" does it all.
- Caches are deleted (apps rebuild them when needed); everything else goes to the Trash, so you can still get it back.
- Then it finds the programs slowing your computer down and the software that can be updated, and measures disk speed
  against your computer's earliest result.
- **It is not a reinstall and not a factory reset.** Your files, settings and software stay exactly where they are.

**Benefit:** gigabytes of free space and a faster computer in minutes, without the risk of deleting something important.

### 2. Longevity: keep your computer cool so it lasts longer
*Computer overheating · CPU temperature monitor · laptop running hot · fan noise · hardware health*

- Watches processor and disk temperatures and how hot your computer runs, and compares them with what is normal for
  this machine.
- Finds **which programs are heating your computer up** right now.
- When it runs hot, tells you why and what to do: close or limit the hot programs, improve airflow, clean the dust.
- Follows disk health (SMART) and temperature over weeks, so wear shows up before it becomes a failure.

**Benefit:** heat is what wears hardware out most. Keeping it cool means fewer crashes, a quieter fan and a longer life.

### 3. Full Potential: find out what your computer can really do
*PC benchmark · disk speed test · CPU stress test · run AI locally · local LLM*

- Measures real disk read/write speed and processor performance, and runs a stress test (up to a 4-hour burn-in) while
  watching temperature and stability.
- Finds the bottleneck: disk, processor, memory or heat.
- If you have enough memory, it can set up a local AI model (Ollama) so idle computing power does useful work.

**Benefit:** know whether your computer performs as it should, and get more out of the hardware you already paid for.

### 4. Hidden Treasure: find resources you did not know you had
*Find large files · what is taking up disk space · storage analyzer · idle resources*

- Shows where your disk space went, the largest folders (only when you ask), software updates waiting, and how much of
  your processor and memory sits idle.

**Benefit:** reclaim space and capacity before you think about buying a new disk or a new computer.

### 5. Remote Trips: get things done on other computers
*Remote computer maintenance · manage multiple computers · SSH health check · AI agents working together*

- Pair your computers with a one-time invitation code, then check another computer's health, run a remote checkup, or hand
  it a task. Each computer follows its own owner's rules.
- Check servers over SSH with the keys you already have (read-only checks run at once; changes need your approval).
- Hand a job to another AI agent (Claude Code, Codex and others, through the RelVectors plugin) and bring the answer back.

**Benefit:** look after the family PC, the office computers or your servers from one place.

### 6. Guardian: catch unsafe programs and settings
*Suspicious processes · malware check · crypto miner detection · open ports · firewall check · security check*

- Checks every running program for warning signs: started from a temporary or download folder, its file deleted while it
  keeps running, ports open to the network, an unknown program keeping the processor busy (a possible crypto miner),
  administrator programs in folders anyone can change.
- Then checks the firewall, disk encryption, security updates and backups.
- Read-only: it never ends a process on its own. For anything suspicious you get what it is, where it is, and what to do.

**Benefit:** a quick, plain-language security check-up, without installing a heavy antivirus suite.

---

## Also included

- **Chat with your computer.** Ask "How is my computer doing?", "Why is it slow?" or "How much disk space is left?" and get
  answers from real measurements, not guesses.
- **Edge + cloud AI.** Uses a local model first (Ollama, oMLX, LM Studio); add a cloud model (OpenAI, Claude, Gemini,
  DeepSeek, Qwen and more) if you want, with a daily budget. Personal content stays local by default.
- **24/7 health monitoring.** Disk space, memory, temperature, network, disk health, security and backups. A problem is
  measured twice before you are told, so false alarms do not bother you.
- **Approval cards.** Anything that cannot be undone pops up as a card: approve or refuse with one click.
- **Dashboard.** A live overview of your computer, with dark and light themes.
- **For AI agents.** Claude Code, Codex and other agents can use RelVectors through MCP to look after the computer they run on.

---

## Download

Get the package for your system under **[Releases](https://github.com/myt98644-cyber/relvectors-releases/releases)**.
English packages end in **`-en`**:

| System | File |
|---|---|
| Windows 10 / 11 (64-bit) | `RelVectors-<version>-windows-x64-en.zip` |
| Windows on ARM | `RelVectors-<version>-windows-arm64-en.zip` |
| macOS (Apple silicon: M1, M2, M3, M4) | `RelVectors-<version>-mac-arm64-en.tar.gz` |
| macOS (Intel) | `RelVectors-<version>-mac-x64-en.tar.gz` |
| Linux (x86_64) | `RelVectors-<version>-linux-x64-en.tar.gz` |
| Linux (ARM64) | `RelVectors-<version>-linux-arm64-en.tar.gz` |

Everything is included: **no Python or other software to install**, and installing needs no internet.
Requirements: Windows 10 or later; macOS 11 or later; Linux with glibc 2.28 or later (Ubuntu 20.04+, Debian 10+, RHEL / Rocky 8+).
`SHA256SUMS.txt` lets you check the downloads.

## Install

- **Windows:** unzip, then double-click `install.cmd`. If Windows says it protected your PC, click "More info → Run anyway".
- **macOS:** unpack, then right-click `Install.command` → Open (the first time needs a right-click because the app is not yet
  notarized by Apple), or run `sh install.sh` in Terminal.
- **Linux:** unpack, then run `sh install.sh` in a terminal.

A **RelVectors** icon appears on your desktop and in the Start menu, Launchpad or app menu. Click it to open RelVectors in your
browser. To quit, click "Quit" at the top right; it starts again at your next login or when you click the icon.

## Free trial and activation

- **7 days free**, counting from the first start.
- Then open Settings → License, click "Copy application", and email it to **155570@qq.com** (any subject).
  An activation code comes back by email automatically.
- Paste the code on the same page. Activation works offline, and the term starts when you first activate.

## Questions

**Will it delete my files?** Only what you tick in the cleanup list. Caches are deleted (apps rebuild them); everything else
goes to the Trash, where you can restore it.

**Does it upload my data?** No. It reads your computer's state on your computer. Your documents are only read in tasks you
give it, and are not sent to a cloud AI unless you allow it.

**Does it need the internet or an AI subscription?** No. It works offline with a free local AI model; a cloud model is optional.

**Will it slow my computer down?** No. It runs at low priority with very little CPU and memory.

**Is "Rejuvenate" a factory reset?** No. It cleans up and speeds up; nothing is reinstalled and nothing is reset.

---

RelVectors is proprietary software; this repository hosts the installers only. The bundled smartctl comes from
smartmontools (GPL); its license is included in the packages. Questions and licenses: 155570@qq.com

*Keywords: AI computer assistant, PC maintenance, Mac maintenance, disk cleanup, free up disk space, speed up computer,
computer overheating, CPU temperature, hardware health, SMART disk health, suspicious process scanner, security check,
remote computer maintenance, local AI, Ollama, AI agent, MCP, Windows, macOS, Linux.*

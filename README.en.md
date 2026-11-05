# RelVectors — AI Engineer

[中文](README.md)

RelVectors lives on your computer like an engineer on call: it keeps reading the machine's real measurements, compares them
with its own history, rechecks anything that looks wrong, and only bothers you when you are needed. Every step that changes
the computer is authorized: read-only steps run at once, reversible ones follow your rules, irreversible ones always ask you first.

## Six features

| Feature | What it does |
|---|---|
| Rejuvenate | Finds what slows it down and takes space, cleans up (reversibly), updates software, then measures speed again against this machine's earliest results |
| Longevity | Tracks disk health and lifetime, battery, thermal pressure and backups; warns early when a trend gets worse |
| Full Potential | Measures what the disks and processor can really do, finds bottlenecks, deploys a local model when there is enough memory |
| Hidden Treasure | Finds reclaimable space, software updates, idle processor and memory |
| Remote Trips | Gets things done on other machines: pairs with other RelVectors, checks hosts over SSH, hands jobs to other agents |
| Guardian | Probes running processes for unsafe signs: programs started from suspicious places, open ports, unknown programs keeping the processor busy; then firewall, encryption and security updates |

Also: a web client (dashboard, task chat, settings), edge + cloud models (local first, cloud on a budget, personal content stays
on the computer by default), a low-power resident patrol, and disk SMART health (smartctl is bundled).

## Download

Get the package for your system from **Releases** on the right. English packages end in **`-en`**:

| System | File |
|---|---|
| macOS (Apple silicon) | `RelVectors-<version>-mac-arm64-en.tar.gz` |
| macOS (Intel) | `RelVectors-<version>-mac-x64-en.tar.gz` |
| Windows 10 / 11 (x64) | `RelVectors-<version>-windows-x64-en.zip` |
| Windows (ARM) | `RelVectors-<version>-windows-arm64-en.zip` |
| Linux (x86_64) | `RelVectors-<version>-linux-x64-en.tar.gz` |
| Linux (ARM64) | `RelVectors-<version>-linux-arm64-en.tar.gz` |

Packages bring their own runtime: **no Python or other dependencies to install**, and installing needs no internet.
Linux needs glibc 2.28 or later (Ubuntu 20.04+, Debian 10+, RHEL / Rocky 8+ and others).
Each release has `SHA256SUMS.txt` to check the downloads.

## Install

- **macOS**: unpack, then right-click "Install.command" and choose Open (the package is not notarized by Apple yet, so the
  first time needs a right-click); or in Terminal, in the unpacked folder: `sh install.sh`.
- **Windows**: unpack, then double-click `install.cmd`. If Windows says it protected your PC, click "More info → Run anyway".
- **Linux**: unpack, then in a terminal: `sh install.sh`.

The client opens in your browser afterwards; later run `rv console` any time. It starts in the background after login,
with normal user rights. For administrator-only data such as disk SMART, run `sudo rv exec install` once when asked
(on Windows: `rv exec install` in a terminal opened with "Run as administrator").

Uninstall: run `uninstall.sh` / `uninstall.cmd` in the installed folder (your data is kept).

## Trial and activation

- **7 days free**, counting from the first run.
- Then, in the client under Settings → License, click "Copy application" (or run `rv license` in a terminal) and send it as
  the body of an email to **155570@qq.com**, any subject. An activation code comes back by email automatically.
- Paste the code on the same page (or run `rv license activate <code>`). Activation works offline; the term starts at the first activation.

## Common commands

```
rv status            this computer's status
rv console           open the client
rv license           trial and activation
rv service status    the background service
```

## Privacy

RelVectors reads the machine's state (readings, capacities, temperatures, versions, hardware models). Documents, file names,
conversations, mail and other personal content are read only inside tasks you give it, with your permission, and are not sent
to cloud models by default.

---

RelVectors is proprietary software; this repository only hosts the installers. The bundled smartctl comes from smartmontools (GPL); its license is included in the packages.
Questions and licenses: 155570@qq.com

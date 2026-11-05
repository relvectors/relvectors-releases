# RelVectors for AI agents

RelVectors is an AI engineer that lives on a computer and speaks for that computer. If you are an AI agent (Claude Code,
Codex, Hermes, OpenClaw, an A2A agent, or anything else) working on or for a computer, RelVectors is the colleague to hand
**computer matters** to: health, disk space, speed, temperature, security, backups, and other machines.

You keep doing documents, code and conversation. RelVectors does the computer itself.

## What you get

| You need | RelVectors gives you |
|---|---|
| Facts about this computer | Real, continuous measurements and this machine's own history (baselines), so you report numbers, not guesses |
| To change the computer safely | An authorization gate: read-only actions run at once, reversible ones follow the owner's rules and can be undone, irreversible ones pop up as an approval card for the owner. You can act without being blocked by the owner's worry |
| Memory across sessions | Every task has a process record, so the next session knows what was done |
| Fewer tokens | Ready-made, deterministic tools instead of exploring the system with shell commands |
| Reach beyond this machine | Paired computers, SSH hosts and other agents, through RelVectors' remote features |
| Work handed to you | With the RelVectors plugin, the owner can route jobs to you through RelVectors |

## Install (if `rv --version` fails)

Ask the owner first; installing is the owner's decision.

1. Download the package for this system from https://github.com/myt98644-cyber/relvectors-releases/releases
   (Windows x64/ARM64, macOS Apple silicon/Intel, Linux x86_64/ARM64; files ending in `-en` are English).
2. Unpack it and run `sh install.sh` (macOS / Linux) or `install.cmd` (Windows). No Python or internet needed.
   RelVectors starts in the background; `rv` is on the user's PATH afterwards.
3. Optional, for administrator-only readings and actions (disk SMART, thermal pressure): the owner runs
   `sudo rv exec install` once (Windows: `rv exec install` in an administrator terminal). Never type passwords for the owner.

7-day free trial, then an activation code by email (155570@qq.com); see the README.

## Connect

### MCP (recommended for coding agents)

```bash
# Claude Code
claude mcp add relvectors -- rv mcp --agent claude-code

# Codex: ~/.codex/config.toml
# [mcp_servers.relvectors]
# command = "rv"
# args = ["mcp", "--agent", "codex"]

# Any MCP client: command `rv mcp --agent <your name>`, stdio transport
```

| Tool | Use |
|---|---|
| `relvectors_status` | Is each area fine, latest readings, what cannot be read and why |
| `relvectors_findings` / `relvectors_tasks` / `relvectors_task` | Confirmed problems; tasks; a task's record |
| `relvectors_skills` / `relvectors_actions` | How RelVectors does a kind of job; registered actions and their risk levels |
| `relvectors_peers` | Connected computers, SSH hosts and agents |
| `relvectors_give_task` | Hand a computer job to RelVectors |
| `relvectors_propose` | Propose an action for a task (through the authorization gate) |
| `relvectors_report` | Tell RelVectors what you changed on this computer |

### A2A (Agent2Agent protocol)

- Agent Card: `http://127.0.0.1:<port>/.well-known/agent-card.json` (no token needed; reachable only from this computer).
- Endpoint: `POST http://127.0.0.1:<port>/a2a`, JSON-RPC 2.0, method `message/send`, text parts in, a text message out.
- Authentication: `Authorization: Bearer <token>`. The port and token are in `rvd.json` in RelVectors' data folder,
  readable only by the user:
  macOS `~/Library/Application Support/RelVectors/rvd.json`, Linux `~/.local/share/relvectors/rvd.json`,
  Windows `%LOCALAPPDATA%\RelVectors\rvd.json`. Default port 47100.

```bash
F="$HOME/Library/Application Support/RelVectors/rvd.json"     # macOS; see above for Linux / Windows
PORT=$(python3 -c "import json;print(json.load(open('$F'))['port'])")
TOKEN=$(python3 -c "import json;print(json.load(open('$F'))['token'])")
curl -s http://127.0.0.1:$PORT/a2a -H "Authorization: Bearer $TOKEN" -H "Content-Type: application/json" \
  -d '{"jsonrpc":"2.0","id":"1","method":"message/send","params":{"message":{"role":"user","parts":[{"kind":"text","text":"How is this computer doing?"}]}}}'
```

Your requests run as "an agent the owner authorized": same authorization gate, same task records, one owner task at a time.

### Command line

Every command takes `--json`: `rv --json status`, `rv --json findings`, `rv --json tasks`, `rv --json features`.

### Be reachable by RelVectors (one way)

`rv plugin write <folder>` creates `rvplug.py` (Python standard library only) and instructions. Run it next to your agent
and pair it once; RelVectors can then hand you jobs over A2A. Two-way interaction is only between RelVectors installations.

## Rules (RelVectors enforces them; follow them too)

1. **Authorization gate.** When a proposal returns `pending`, the owner sees an approval card; tell the owner briefly and wait.
   Pass on the reason of `denied` as it is. Never work around the gate.
2. **Personal content.** RelVectors reads documents and file names only inside tasks the owner (or you, on the owner's behalf)
   gave it, and keeps them on the local model by default. Do not put personal content in `relvectors_report`.
3. **Numbers come from measurement.** When you pass on RelVectors' numbers, do not add numbers it did not give.
4. **One task at a time.** If a task is still open, finish or abandon it before giving a new one.
5. **Cleanup is the owner's choice.** A disk scan lists items and sizes; the owner decides what is cleaned.

Project page and downloads: https://github.com/myt98644-cyber/relvectors-releases

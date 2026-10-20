# Claude Skills

Skills for [Claude Code](https://claude.com/claude-code) and Claude.

## Skills

| Skill | What it does |
| --- | --- |
| [`malware-findings`](malware-findings/) | Writes a short, factual findings file for a malware sample or incident artifact set: identity, dropped files and their byte layouts, run behaviour, and where the evidence stops. Includes a standard-library script that collects hashes, PE details, embedded RSA keys and key-blob markers from an extracted sample set. |

## Install

Copy a skill's folder into one of these locations:

- `~/.claude/skills/<skill-name>/` to use it in every project
- `<project>/.claude/skills/<skill-name>/` to share it through that project's repository

Claude Code loads skills when a session starts.

## Safety

`malware-findings` is for static analysis. It never runs samples. Its script only reads bytes and doesn't import or execute anything from the folder it inspects. Handle live samples in an isolated analysis environment.

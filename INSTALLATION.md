# Installation Guide

This skill ships in three forms:

1. **As a directory in your local Hermes/OpenClaw/Claude Code skills folder** (most common)
2. **As a published GitHub repo** at <https://github.com/0xcjl/social-org-research>
3. **As a registered ClawHub package** (slug: `social-org-research`)

---

## 1. Local install (Hermes)

If you already have this repo cloned or copied to `~/.hermes/skills/social-org-research/`, you're done — Hermes auto-discovers skill folders.

```bash
# Quick check
ls ~/.hermes/skills/social-org-research/SKILL.md   # should print a path

# Inside any Hermes conversation, confirm load:
#   /skills list
# should show "social-org-research"
```

---

## 2. Local install (OpenClaw / Claude Code)

OpenClaw and Claude Code use the same skill folder convention. Symlink (or copy) this repo into their skills root.

```bash
# OpenClaw
ln -s ~/.hermes/skills/social-org-research ~/.openclaw/workspace/skills/social-org-research

# Claude Code (adjust path if your Claude skills folder is elsewhere)
ln -s ~/.hermes/skills/social-org-research ~/.claude/skills/social-org-research
```

Restart the agent to pick up the new skill.

---

## 3. Install via Hermes package manager

If your Hermes version supports `hermes skills install`:

```bash
hermes skills install 0xcjl/social-org-research
```

This fetches the latest release from ClawHub and installs it into the right folder.

---

## 4. Manual install from GitHub

```bash
git clone https://github.com/0xcjl/social-org-research.git \
  ~/.hermes/skills/social-org-research
```

(For OpenClaw / Claude Code, symlink as in §2.)

---

## 5. Install from ClawHub

```bash
clawhub install social-org-research
```

(If `clawhub install` isn't a command in your ClawHub version, use §3 or §4.)

---

## Upgrade

When a new version is published:

```bash
# Local clone
cd ~/.hermes/skills/social-org-research
git pull origin main

# Hermes package manager
hermes skills update social-org-research

# ClawHub CLI
clawhub install social-org-research    # re-runs install of latest version
```

---

## Verification

After any install method, verify:

```bash
ls ~/.hermes/skills/social-org-research/SKILL.md
python3 -c "import yaml; yaml.safe_load(open('~/.hermes/skills/social-org-research/SKILL.md').read().split('---')[1])"
```

Both commands should succeed silently.

Then in any agent conversation:

```
/skills list
```

should show `social-org-research` as installed.

---

## Uninstall

```bash
rm -rf ~/.hermes/skills/social-org-research
# also remove the OpenClaw / Claude Code symlink if you created one
```
# social-org-research

> Research a B Corp / social enterprise / NGO / youth culture brand — with a 10-dimension framework, `quick | deep` depth switch, and a verified case study.

[![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg)](./LICENSE)
[![Skill](https://img.shields.io/badge/type-agent%20skill-blueviolet)](./SKILL.md)
[![Platforms](https://img.shields.io/badge/platforms-Hermes%20%7C%20Claude%20Code%20%7C%20OpenClaw-lightgrey)](#platforms)
[![Version](https://img.shields.io/badge/version-0.1.0-success)](./CHANGELOG.md)

> **English** | **[简体中文](./README.zh-CN.md)**

---

## What It Does

`social-org-research` is a structured research prompt and evaluation framework for investigating **social innovation organizations** — B Corps, social enterprises, NGOs, public-interest platforms, youth culture brands, and other "business as a force for good" entities.

Unlike generic market research, this skill targets organizations whose business model mixes revenue with mission: sponsored content, donor relationships, volunteer labor, paid partnerships with global NGOs, government grants, and "co-creator" rather than "sponsor" brand relationships.

It comes with a **10-dimension framework**, a **`depth: quick | deep` switch**, and a **case study from a real BottleDream research session** that demonstrates the skill in action.

---

## Why Use It

| Without `social-org-research` | With `social-org-research` |
|--------------------------------|------------------------------|
| "How does this NGO make money?" → confused silence | Concrete revenue categories: media / content sponsorship / training / consulting / co-branded products / event sponsorship |
| "Are volunteers paid?" → speculation based on Chinese nonprofit stereotypes | Reference to the *Volunteer Service Regulations* (志愿服务条例) and the 5-non-cash-hook framework |
| "What's the difference between co-creator and sponsor?" → blur | Clear taxonomy: co-creator = brings plan + resources + product to solve the issue; sponsor = pays for naming rights |
| "The registered capital is 1 million RMB — is the company small?" | Distinction: registered capital ≠ actual scale; cross-reference LinkedIn / B Lab / office size |

---

## Use Cases

| Scenario | Use this skill? |
|----------|----------------|
| Researching a B Corp, social enterprise, or co-benefit company | ✅ Yes |
| Investigating an NGO, public-interest platform, or foundation | ✅ Yes |
| Mapping a youth culture brand's content + event + community operations | ✅ Yes |
| Trying to understand how a "social good" organization makes money | ✅ Yes |
| Quick competitive scan before a pitch meeting | ✅ Yes (`depth: quick`) |
| Researching a commercial product or B2B SaaS company | ❌ Use [`market-research`](https://github.com/0xcjl/market-research) instead |
| Literature review for an academic paper | ❌ Use [`academic-research`](https://github.com/0xcjl/academic-research) instead |
| Investigating industry trends across many players | ❌ Use [`deep-research`](https://github.com/0xcjl/deep-research) instead |

---

## Trigger Keywords

**English:** `social enterprise`, `B Corp`, `co-benefit`, `co-benefit enterprise`, `social innovation`, `NGO research`, `youth culture brand`, `public-interest platform`, `B Impact Assessment`, `BIA score`, `social good`, `volunteer benefits`, `co-creator vs sponsor`

**Chinese:** 调研 NGO / 共益企业 / 社会企业 / 公益平台 / B 型企业 / 青年文化品牌 / 商业向善 / 创变者 / 志愿者报酬 / 影响力投资 / 公益基金会 / 共创伙伴 / 社会创新企业

---

## Quick Start

### 1. Install (Hermes / OpenClaw)

```bash
hermes skills install 0xcjl/social-org-research
# or, from local source
ln -s ~/.hermes/skills/social-org-research ~/.openclaw/workspace/skills/social-org-research
```

### 2. Use it

In any agent conversation, invoke the skill and pass a target:

```
Research BottleDream, depth: deep
```

The skill auto-loads, walks through 10 dimensions, and produces a Markdown + clickable-link PDF.

---

## Example: What a `depth: deep` Session Produces

A real BottleDream session (see [`references/case-bottledream.md`](./references/case-bottledream.md)) generated:

- An **18-page A4 PDF** (`bottledream-research.pdf`, ~2.35 MB) with 35 source links rendered as clickable /Link annotations
- **VBC-verified** `md_links = matched_links = 35` (100% match)
- **35 sources** spanning B Lab, LinkedIn, 36Kr, Sina Finance, NetEase, China Development Brief, WonderCV, People.cn, World Economic Forum, Journal of Futures Studies, etc.
- **Three iterative deep-dives** answering the user's follow-up questions about event execution and volunteer compensation

Without the skill, the same depth would require ~15 hours of manual research and the volunteer's "no cash compensation but free lunch + free T-shirt + free immersive experience" answer would be missed entirely.

---

## Architecture

```
social-org-research/
├── SKILL.md                      # The skill body (loaded by agents)
├── README.md                     # This file (English)
├── README.zh-CN.md               # Simplified Chinese variant
├── INSTALLATION.md               # Hermes / OpenClaw / Claude Code install guide
├── LICENSE                       # MIT
├── CHANGELOG.md                  # Version history
├── .gitignore
└── references/
    └── case-bottledream.md       # Real-world case study (simplified)
```

---

## Customization

To adapt this skill for a specific niche (e.g. climate-tech NGOs, foundations, social enterprises in a specific region):

1. **Tweak the Information Source Priority table** in `SKILL.md` §"Information source priority" — add region- or sector-specific databases.
2. **Adjust the 10 dimensions** if your target sector emphasizes other things (e.g. add "regulatory filings" for healthcare NGOs).
3. **Add new Pitfalls** to the §"Key Pitfalls" section as you encounter them in real research.
4. **Update the Use Cases routing table** if you want to redirect certain scenarios to other skills.

---

## Troubleshooting

| Issue | Fix |
|-------|-----|
| `gh auth status` fails | `gh auth login` |
| `clawhub publish` rejects YAML | Run `python3 -c "import yaml; yaml.safe_load(open('SKILL.md').read().split('---')[1])"` to validate frontmatter |
| Topics count ≠ 13 | Re-run `gh repo edit --add-topic` for each missing tag |
| README doesn't render | Preview with `grip -b README.md` locally |
| Skill loads but description triggers wrong | Edit frontmatter `description` (keep ≤60 chars to avoid index truncation) |

---

## Platforms

| Platform | Compatible? | Notes |
|----------|-------------|-------|
| Hermes | ✅ | `~/.hermes/skills/social-org-research/` |
| OpenClaw / Claude Code | ✅ | Symlink to `~/.openclaw/workspace/skills/social-org-research/` |
| Other SKILL.md readers | ✅ | Standard YAML frontmatter + markdown body |

---

## Credits

- **Author:** 0xcjl
- **License:** MIT
- **Case study source:** A real BottleDream research session conducted by the author with this skill, September 2026
- **Skill publisher:** `agent-skill-publisher` (Hermes internal) — 9-step end-to-end publish workflow

---

## License

MIT © 2026 0xcjl
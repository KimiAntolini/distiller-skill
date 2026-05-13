# Distiller

> One-click distillation of historical and contemporary figures into high-quality AI character simulation Skills.

[![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg)](https://opensource.org/licenses/MIT)

> **📖 中文**：[README.md](./README.md)

## What is this?

Distiller is an AI-powered automation tool. You provide the name of a notable figure, and it searches the web for all publicly available information, deeply distills and integrates the data, and produces a ready-to-use character simulation Skill package — enabling AI to realistically simulate that figure in conversation and thought.

### How It Works

```
Input name → Disambiguate → Web search → Distill & integrate → Generate Skill + sources
```

Each generated Skill includes **13 modules** covering personality, language style, behavioral patterns, works, biography, philosophical framework, relationship networks, anecdotes, posthumous evaluations, and more. The result is both historically faithful and conversationally natural.

### Distilled Samples

| Figure | Era | Identity | Skill Size |
|--------|-----|----------|------------|
| **Stalin** | 1878–1953 | Soviet supreme leader, revolutionary | 356 lines |
| **Bai Juyi** | 772–846 | Tang Dynasty poet, literary reformer | 365 lines |

> Spanning East and West, ancient and modern, these two samples validate Distiller's ability to handle both 20th-century political figures and classical literary masters. Each Skill includes a complete [sources.md](./distilled/) reference list — every fact is traceable.

## Quick Start

### Option 1: Install via Skill.sh

```bash
skill install distiller
```

### Option 2: Clone from GitHub

```bash
git clone https://github.com/KimiAntolini/distiller-skill.git
```

Place the `distiller-skill` directory into your skills directory.

### Usage

In Claude Code or OpenCode:

```
distill Lu Xun
```

or:

```
generate a skill for Albert Einstein
```

Distiller will automatically search, disambiguate, collect data, integrate it, and produce a complete Skill package.

> **💡 Tip**: Works best alongside the [superpowers](https://github.com/obra/superpowers) and [skill-creator](https://skill.sh) skills. Superpowers provides a disciplined workflow framework, while skill-creator helps you polish, debug, and optimize the generated skills.

## Output

Each distillation produces an independent folder:

```
distilled/{Name}/
├── SKILL.md       # Character simulation skill (13 modules)
└── sources.md     # All referenced sources
```

### Modules in SKILL.md

**Required (6):**
1. Personality
2. Language style
3. Behavioral style
4. Works & publications
5. Life & history
6. Thought analysis

**Optional (7):**
7. Relationship network
8. Anecdotes
9. Posthumous evaluations
10. School-of-thought comparison
11. Representative quotes
12. Sample dialogues
13. Supplementary resources

## Supported Figures

- ✅ Ancient Chinese figures (Pre-Qin through Qing)
- ✅ Early modern Chinese figures (1840–1949)
- ✅ Contemporary Chinese figures (1949–present)
- ✅ International figures (all regions & eras)
- 🔮 Universal Distiller (V2.0 planned) — distill anyone using private data

## Platform Compatibility

| Platform | Status |
|----------|--------|
| Claude Code | ✅ Native support |
| OpenCode | ✅ Native support |
| Codex | ⚠️ Adaptation needed |
| Copilot CLI | ⚠️ Adaptation needed |
| Gemini CLI | ⚠️ Adaptation needed |

## Project Structure

```
distiller-skill/
├── SKILL.md                           # Distiller's main skill file
├── AGENTS.md                          # Project context & instructions
├── README.md                          # Chinese README
├── README.en.md                       # This file (English)
├── templates/celebrity-skill/
│   ├── SKILL.md                       # Character skill template
│   └── sources.md                     # Source file template
├── distilled/                         # Output directory
├── 蒸馏器项目-Distiller-企划书.md      # Full project proposal (Chinese)
└── LICENSE
```

## Contributing

Issues and PRs are welcome. Please read the full project proposal first.

## License

MIT License

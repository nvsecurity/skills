# NightVision Skills Marketplace

This repository is a Claude Code plugin marketplace containing skills that teach AI agents how to use NightVision's DAST and API Discovery tools.

## Repository Structure

```
nightvision-skills/
├── .claude-plugin/
│   └── marketplace.json        # Marketplace catalog (lists all plugins)
├── plugins/
│   └── nightvision/
│       ├── .claude-plugin/
│       │   └── plugin.json     # Plugin manifest
│       ├── README.md
│       └── skills/
│           └── <skill-name>/
│               ├── SKILL.md    # Skill definition (YAML frontmatter + instructions)
│               └── references/ # Supporting documentation
├── CLAUDE.md                   # This file
├── LICENSE
├── README.md
└── .gitignore
```

## Skill Authoring

Each skill lives in `plugins/nightvision/skills/<skill-name>/` and must contain a `SKILL.md` with YAML frontmatter:

```yaml
---
name: skill-name
description: Third-person description of what the skill does and when to use it
user-invocable: true
allowed-tools: Bash
---
```

Guidelines:
- Use kebab-case for skill names and directories
- Keep `SKILL.md` focused and under 500 lines; put detailed reference material in `references/`
- The `description` field should explain both what the skill does and when Claude should activate it
- Only list tools in `allowed-tools` that the skill actually needs

## Adding a New Skill

1. Create `plugins/nightvision/skills/<skill-name>/SKILL.md` with frontmatter and instructions
2. Add reference files in `plugins/nightvision/skills/<skill-name>/references/` if needed
3. Update `plugins/nightvision/README.md` to list the new skill
4. Update the root `README.md` skills table

# NightVision Skills Plugin

Skills for working with [NightVision](https://www.nightvision.net), a white-box-assisted DAST platform that combines API Discovery, dynamic scanning (ZAP + Nuclei), and Code Traceback to find exploitable vulnerabilities in web applications and REST APIs.

## Installation

```bash
claude plugin marketplace add nvsecurity/skills
claude plugin install nightvision@nightvision
claude
```

Or within Claude Code:

```
/plugin marketplace add nvsecurity/skills
/plugin install nightvision@nightvision
```

You may need to restart Claude Code for the plugin to load.

## Available Skills

| Skill | Description |
|-------|-------------|
| `ci-cd-integration` | Integrate NightVision DAST scanning into CI/CD pipelines (GitHub Actions, GitLab CI, Azure DevOps, Jenkins, BitBucket, JFrog) |
| `api-discovery` | Extract OpenAPI specs from source code using NightVision API Discovery (static analysis, Code Traceback, spec diffing) |
| `scan-configuration` | Configure NightVision DAST scans (targets, authentication, projects, scope exclusions, private network scans) |
| `scan-triage` | Interpret and act on NightVision scan results (SARIF/CSV findings, severity prioritization, remediation, false positive handling) |

## Usage

Skills are invoked using slash commands in Claude Code:

```
/ci-cd-integration
/api-discovery
/scan-configuration
/scan-triage
```

Or Claude will automatically use relevant skills based on context.

## Structure

```
nightvision/
├── .claude-plugin/
│   └── plugin.json
├── skills/
│   ├── api-discovery/
│   │   ├── SKILL.md
│   │   └── references/
│   ├── ci-cd-integration/
│   │   ├── SKILL.md
│   │   └── references/
│   ├── scan-configuration/
│   │   └── SKILL.md
│   └── scan-triage/
│       ├── SKILL.md
│       └── references/
└── README.md
```

## License

Apache 2.0

# NightVision Skills Marketplace

Plugin marketplace for [NightVision](https://www.nightvision.net)'s DAST and API Discovery skills for Claude Code.

NightVision is a white-box-assisted DAST tool that finds exploitable vulnerabilities in web applications and REST APIs. It combines API Discovery (static analysis to extract OpenAPI specs from source code), dynamic scanning (ZAP + Nuclei engines), and Code Traceback (tracing vulnerabilities back to exact source locations).

## Quick Installation

With Claude Code:

```bash
claude plugin marketplace add nvsecurity/skills
claude plugin install nightvision@nvsecurity
claude
```

Or within Claude Code:

```
/plugin marketplace add nvsecurity/skills
/plugin install nightvision@nvsecurity
```

You may need to restart Claude Code for the plugin to load.

## Skills

[NightVision Plugin](plugins/nightvision/README.md)

| Skill | Description |
|-------|-------------|
| `ci-cd-integration` | Integrate NightVision DAST scanning into CI/CD pipelines (GitHub Actions, GitLab CI, Azure DevOps, Jenkins, BitBucket, JFrog) |
| `api-discovery` | Extract OpenAPI specs from source code using NightVision API Discovery (static analysis, Code Traceback, spec diffing) |
| `scan-configuration` | Configure NightVision DAST scans (targets, authentication, projects, scope exclusions, private network scans) |
| `scan-triage` | Interpret and act on NightVision scan results (SARIF/CSV findings, severity prioritization, remediation, false positive handling) |

## Contributing

Contributions are welcome. Please open an [issue](https://github.com/nvsecurity/skills/issues) or submit a pull request.

## License

This repository is licensed under the Apache License 2.0. See [LICENSE](LICENSE) for details.

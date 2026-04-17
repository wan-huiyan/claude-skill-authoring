# claude-skill-authoring

End-to-end toolkit for **authoring, publishing, syncing, auditing, and diagnosing Claude Code skills** — bundled as a single marketplace.

## What's inside

| Plugin | Version | What it does |
|---|---|---|
| [`publish-skill`](plugins/publish-skill/) | 2.1.0 | Publish a skill to GitHub as a polished, adoptable plugin (awesome-claude-skills-ready). |
| [`skill-sync`](plugins/skill-sync/) | 1.1.0 | Keep locally installed skills in sync with their GitHub sources. |
| [`skill-portfolio-audit`](plugins/skill-portfolio-audit/) | 1.1.0 | Portfolio-wide skill quality audit (agent-review-panel → plan-review-integrator → parallel implementation). |
| [`skill-anonymizer`](plugins/skill-anonymizer/) | 1.1.0 | Scrub client-specific or sensitive data from skills before sharing. |
| [`skill-trigger-eval-subprocess-blindness`](plugins/skill-trigger-eval-subprocess-blindness/) | 1.0.0 | Diagnose 0% recall from skill-creator's trigger evaluation loop. |

## Install

```bash
claude plugin marketplace add wan-huiyan/claude-skill-authoring

# Install all five:
claude plugin install publish-skill@wan-huiyan-skill-authoring
claude plugin install skill-sync@wan-huiyan-skill-authoring
claude plugin install skill-portfolio-audit@wan-huiyan-skill-authoring
claude plugin install skill-anonymizer@wan-huiyan-skill-authoring
claude plugin install skill-trigger-eval-subprocess-blindness@wan-huiyan-skill-authoring
```

## Lifecycle fit

```
author          → publish        → sync         → audit                   → diagnose
skill-creator     publish-skill    skill-sync     skill-portfolio-audit      skill-trigger-eval-
(upstream)                                      + skill-anonymizer           subprocess-blindness
```

Use `skill-creator` (upstream Anthropic) to write a skill → `publish-skill` to ship it → `skill-sync` to keep installs fresh → `skill-portfolio-audit` + `skill-anonymizer` to keep the portfolio clean → `skill-trigger-eval-subprocess-blindness` when the eval loop misbehaves.

## Canonical sources

Each bundled plugin (except `skill-trigger-eval-subprocess-blindness`) also has a standalone repo. The bundle here is a snapshot; canonical sources:

- [wan-huiyan/publish-skill](https://github.com/wan-huiyan/publish-skill)
- [wan-huiyan/skill-sync](https://github.com/wan-huiyan/skill-sync)
- [wan-huiyan/skill-portfolio-audit](https://github.com/wan-huiyan/skill-portfolio-audit)
- [wan-huiyan/skill-anonymizer](https://github.com/wan-huiyan/skill-anonymizer)

Use `skill-sync` or a GHA pipeline to keep the bundled copies aligned with their canonical sources.

## License

MIT.

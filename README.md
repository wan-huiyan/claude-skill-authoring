# claude-skill-authoring

Marketplace for tools and troubleshooting recipes focused on **authoring, diagnosing, and maintaining Claude Code skills**.

## Plugins in this marketplace

- **`skill-trigger-eval-subprocess-blindness`** — Diagnose 0% recall from `skill-creator`'s trigger evaluation loop. Explains why introspection/audit skills appear to never fire in `run_eval.py`/`run_loop.py` even with perfect descriptions, and how to distinguish subprocess blindness from a genuinely broken description.

## Companion skills (separate marketplaces)

These live in their own repos. Install alongside this marketplace for a complete skill-authoring workflow:

- [`skill-portfolio-audit`](https://github.com/wan-huiyan/skill-portfolio-audit) — Portfolio-wide skill quality audit.
- [`skill-anonymizer`](https://github.com/wan-huiyan/skill-anonymizer) — Scrub client-specific or sensitive data from skills.
- [`skill-sync`](https://github.com/wan-huiyan/skill-sync) — Keep locally installed skills in sync with their GitHub sources.
- [`publish-skill`](https://github.com/wan-huiyan/publish-skill) — Publish a skill to GitHub as a polished, adoptable plugin.

## Install

```
/plugin marketplace add https://github.com/wan-huiyan/claude-skill-authoring
/plugin install skill-trigger-eval-subprocess-blindness@wan-huiyan-skill-authoring
```

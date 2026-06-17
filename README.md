# agent-patterns

Five small, self-contained skills for long-running agents. Each is a single `SKILL.md` with no external dependencies, licensed Apache-2.0.

## Quickstart — copy the whole set in one command

In Claude Code:

```
/plugin marketplace add WGlynn/agent-patterns
/plugin install agent-patterns@agent-patterns
```

That's it. The five skills are now available and fire automatically when a task calls for them. Nothing else to configure.

Prefer just one? Every skill is a self-contained folder — copy any `skills/<name>/SKILL.md` into your own project's `.claude/skills/` and it works on its own, no marketplace needed. To fork the whole set, clone this repo and point your marketplace at the clone:

```
git clone https://github.com/WGlynn/agent-patterns
/plugin marketplace add ./agent-patterns
```

Everything here is Apache-2.0 — copy it, change it, ship it.

| Skill | What it does |
|---|---|
| **critical-qa** | Self-adversarial review across fixed categories before declaring a change done. |
| **classify** | Routes a task to the cheapest model tier that can still do it well. |
| **ship-web** | Pre-ship checklist for web artifacts: format fit, deploy actually ran, viewport tag, cache. |
| **anti-hallucinate** | Stress-tests a claim (mechanism, direction, counterfactual) before stating it as fact. |
| **compact-memory** | Writes an agent's own state in a compact symbolic notation instead of prose. |

## Install (Claude Code)

```
claude plugin marketplace add WGlynn/agent-patterns
claude plugin install agent-patterns@agent-patterns
```

Once installed, each skill fires when relevant to the task. They are independent — install the set or copy a single `skills/<name>/SKILL.md` folder.

## Why these five

They are the quality, cost, and memory layers a long-running agent needs and usually lacks: a way to catch its own bad "done," a way to not overspend on easy work, a way to not ship a broken page, a way to not assert past what it knows, and a way to keep its memory small and unambiguous. Each one also exists as a worked notebook proposal in the Anthropic cookbooks discussion.

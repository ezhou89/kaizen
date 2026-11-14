# Kaizen

**Passing tests is not the same as delivering useful software.**

Kaizen is a lightweight, experimental plugin with four skills for improving software and agent workflows. It asks what the user is trying to accomplish, where the real flow falls short, what causes the gap, and whether a proportionate change actually helps.

It is inspired by continuous-improvement ideas from the Toyota Production System. It is not affiliated with or endorsed by Toyota, and it is not a complete implementation of TPS.

## Four skills, not a mandatory ceremony

| Skill | Use it when |
| --- | --- |
| `kaizen-establish-value` | The intended outcome is missing, conflicting, or drifting. |
| `kaizen-observe-flow` | The actual journey is clunky or incomplete, even if tests pass. |
| `kaizen-investigate-gap` | A failure needs evidence-backed diagnosis before intervention. |
| `kaizen-improve-verify` | A change needs a benefit hypothesis, guardrails, and verification. |

Use one or several. A spelling correction should remain a spelling correction. An audit starts read-only unless changes are authorized. Diagnosis does not grant permission to edit or deploy.

Kaizen actively considers removing unnecessary code, tests, instructions, and steps. It also asks what protection would be lost: rare security, accessibility, reliability, and integrity failures still matter. It reviews relevant README and agent instruction files (such as AGENTS.md or CLAUDE.md) without silently overriding valid constraints.

## Install with Claude Code

```sh
claude plugin marketplace add ezhou89/kaizen
claude plugin install kaizen@kaizen
```

Or, inside Claude Code: `/plugin install kaizen --marketplace ezhou89/kaizen`. Start a new session afterwards. The skills appear as `/kaizen:kaizen-establish-value`, `/kaizen:kaizen-observe-flow`, `/kaizen:kaizen-investigate-gap`, and `/kaizen:kaizen-improve-verify`, and Claude may also invoke them when a description matches. To try a local clone without installing, run `claude --plugin-dir ./plugins/kaizen`.

## Install with Codex

Prerequisite: a Codex version with `codex plugin` commands. Download or clone this repository, then run from its root:

```sh
codex plugin marketplace add "$(pwd)"
codex plugin add kaizen@kaizen-local
codex plugin list
```

Keep the directory in place: this is a local marketplace source. Repeat installation on each computer where needed. This does not automatically synchronize installations or publish the plugin to a public directory. Existing installations using `kaizen-local` should inspect their current source before adding a different copy.

To use it, ask your agent to use the relevant named skill, for example:

> Use Kaizen to review why this green test suite misses a frustrating onboarding journey. Keep the review read-only.

> Use kaizen-improve-verify to assess whether removing this step would improve the workflow without losing safeguards.

The package has no service, hooks, executable scripts, or credentials. The agent still uses its own tools and permissions. Installation is not proof that every host automatically invokes these skills. Codex CLI installation and discovery have been tested. For Claude Code, the plugin and marketplace manifests pass `claude plugin validate`, but installation and skill invocation in a live session have not yet been checked. Desktop UI invocation and other agent hosts have not been established by this project.

## Status and evidence

**Experimental v0.2.0.** Skill formatting and isolated CLI installation were checked. Independent model reviews and simulated tasks informed revisions. v0.2.0 adds Claude Code packaging and small host-neutral wording changes: naming CLAUDE.md alongside AGENTS.md, preferring to run a journey directly when a browser, simulator, or CLI is available, and asking for a brief report. These changes have not been re-reviewed with the process described below. These exercises do not demonstrate improved real-user outcomes or superiority to a competent agent without Kaizen; baseline agents handled some scenarios well without it.

[Kaizen reviewing itself](examples/self-review.md) describes a small, real design-review loop, including its limitations. The next useful evidence is whether people complete real tasks more effectively, not whether the project accumulates more rules or tests.

Created by [Eugene Zhou (@ezhou89)](https://github.com/ezhou89). See [contributing](CONTRIBUTING.md) for useful reports. Licensed under the [MIT License](LICENSE).

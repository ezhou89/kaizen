---
name: kaizen-improve-verify
description: Use when an improvement to a software system, test suite, documentation, or workflow is being selected, implemented, or verified.
---
# Improve and verify

Anchor the change in the actual outcome and baseline. Before changing, choose proportionate success criteria and guardrails. Actively consider subtraction as well as addition: removing code, tests, documentation, handoffs, or steps may improve the project. For a proposed removal, state the expected benefit, identify users and dependencies, identify behavior or safeguards lost, check reversibility and authorization, and define how to observe its effects. Preserve or replace security, accessibility, integrity, and rare high-impact protections; low frequency alone is not evidence of low value. Do not permanently delete unrecoverable data without required confirmation.

Make the smallest justified authorized change; do not automatically rebuild. Use tests that detect meaningful user, operational, or safety failures. Explain what each significant test family protects and cannot prove; passing test count is not success. Check the actual end-to-end task and result against baseline when possible: run the app, CLI, or flow and observe it, not just the test suite. Separate direct user feedback from simulated or model assessment; report unverified outcomes and adverse effects honestly. If checks fail or results are inconclusive, decide whether to retain, revise, or revert based on evidence and risk; obtain required authorization and never undo unrelated user work.

When a failure exposes misleading README, scoped agent instruction files (such as AGENTS.md or CLAUDE.md), or other guidance, reconcile the relevant text with current intent and observed behavior. Update narrowly when authorized, preserve valid constraints and unrelated content, and do not conflate repository guidance with the assistant's saved memory or user-level settings. Record evidence-backed learning with scope and uncertainty. Stop when further work costs more than likely benefit or when real-world evidence is needed; do not create perpetual work.

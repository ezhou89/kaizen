# Kaizen reviews Kaizen

This is a summarized account of an initial design review, not a controlled performance study. It contains no private project material or conversation transcripts.

## Goal

Make the four-skill bundle useful and lightweight: improve actual outcomes without forcing every request through a process.

## What happened

One model used the skills to inspect the bundle itself. A separate fresh-context model reviewed the files independently. The self-review found the bundle lean and recommended no rewrite. It raised possible handoff and over-application issues as hypotheses, not demonstrated failures.

The independent review identified two concrete gaps in the instructions:

- Broad activation wording could cause unnecessary work on ordinary tasks.
- Verification did not explicitly explain what to do when a change failed its checks.

## Changes

The outcome skill's trigger was narrowed to missing, conflicting, or demonstrably drifting outcomes. The improvement skill now calls for success criteria and guardrails before changing, and a retain/revise/revert decision afterward. A short orientation explains that the skills are independently usable, not a mandatory pipeline.

A fresh model then applied the revised skills to two simulated tasks: a trivial spelling correction and a failed checkout with green tests and a proposed security-test removal. It described a narrow correction for the first, and evidence gathering, preserved safeguards, and outcome-based verification for the second. No real checkout or user workflow was modified by that exercise.

## What this establishes

The review produced specific instruction changes and the subsequent simulated response reflected the intended distinctions. It does not establish that the changes caused a measurable improvement, that the skills outperform a capable baseline, or that real users benefit. Earlier baseline agents also handled several scenarios well without the skills.

The lesson is modest: improve the guidance when a review reveals a gap, keep the change small, and do not confuse an agent's convincing answer with evidence of user success.

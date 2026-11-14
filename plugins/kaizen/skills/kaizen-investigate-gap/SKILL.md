---
name: kaizen-investigate-gap
description: Use when an observed failure, drift, bottleneck, or confusing result needs diagnosis before choosing a change.
---
# Investigate the gap

State the observed failure, who it affects, and the evidence. Trace the relevant path across implementation, configuration, instructions, and handoffs. Distinguish symptoms, supported causes, competing hypotheses, and unknowns. Seek the smallest safe check that can discriminate between plausible causes; do not manufacture a neat root cause from an unverified chain of why questions.

Compare proportionate options: remove, simplify, repair, replace, clarify, gather evidence, or leave unchanged. Consider downstream effects, lost safeguards, dependencies, reversibility, and authorization. A plausible diagnosis is not permission to edit or deploy. Escalate when a consequential conflict or required approval remains unresolved.

Report the most useful next action with supporting evidence and limits. Use kaizen-improve-verify when a change is authorized; avoid prescribing a rebuild merely because one component is flawed.

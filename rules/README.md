# Rules
 Rule files govern how Claude should behave across all projects, not just in specific tasks. Most load unconditionally at session start; files with paths frontmatter load only when Claude reads a matching file.

## Skills vs. rules

Skills load on demand; rules load eagerly. Procedural workflows with their own steps, templates, or references belong in skills. Behavioral defaults that should apply to every response belong in rules. A single concern occasionally splits across both.

---

`honesty.md` — Rules about factual claims: never present estimates as measurements, source every number, verify the framing of external systems and codebase concepts against the source before writing prose about them, separate verified facts from assumptions, don't optimize for looking helpful over being accurate. Applies extra scrutiny to any external-facing content.

`self-improvement.md` — Triggers for when to self-improve: user corrections, workarounds, failed commands, violated rules, and inconsistencies. Points to `rule-maintenance.md` for how to act on them.

`writing.md` - User-specific writing preferences that supplement the writing-clearly-and-concisely skill: avoid violent metaphors and military or war-origin idioms (including "in anger"); emulate the user's voice when appropriate without mirroring lowercase prompting shorthand in formal output.

`stakeholder-questions.md` — When drafting a question for a stakeholder, client, or non-engineer collaborator, ask about behavior, not implementation. Covers two techniques (turn internal insights into assumption checks; match the stakeholder's vocabulary), a worked example (temporal information on records), and the failure mode that motivates the rule. Applies to Slack drafts, meeting follow-ups, ADR Context-section research — any outward-facing question whose answer feeds engineering work.

`rule-maintenance.md` — Procedures for correcting and updating this configuration: where corrections go (source rule or skill, not memory), how to write rules (imperative voice, include the failure mode), how to update the rule index, feedback routing, and the permissions allow list workflow.

`feedback.md` — General behavioral lessons and corrections that don't fit an existing rule file. Written to by Claude when feedback warrants a new rule but no home exists yet.
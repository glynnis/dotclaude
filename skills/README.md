# Skills

Skills extend Claude's capabilities for specific tasks. The `description` frontmatter is always in context so Claude knows what's available; the full skill body loads only when the skill is invoked. Most skills trigger automatically when relevant — a few are manual-only (marked below) because they have side effects or should only run when explicitly asked.

Invoke manually with `/skill-name [args]`.

## Skills vs. rules

Skills load on demand; rules load eagerly. Procedural workflows with their own steps, templates, or references belong in skills. Behavioral defaults that should apply to every response belong in rules. A single concern occasionally splits across both.

---

## Writing & documentation

**`writing-clearly-and-concisely`** — Applies Strunk's rules for clarity and concision. Also covers AI writing anti-patterns (puffery, empty -ing phrases, overused vocabulary). Reference files contain the relevant chapters from *The Elements of Style*. Optionally pairs with `rules/writing.md`, a personal-voice overlay that supplements (not replaces) the skill — see the skill's `COMPANIONS.md` for the pattern.

**`crafting-effective-readmes`** — Use when writing or improving README files. Not all READMEs are the same — provides templates and guidance matched to your audience and project type.

## Dialogue & focus

**`grill-me`** — Interviews the user relentlessly about a plan or design until reaching shared understanding, resolving each branch of the decision tree. Use when stress-testing a plan or design.

**`human-harness`** — A focus harness for a human with ADHD. Atomizes a task into the single next physical action, shows exactly one thing at a time, and re-injects a deadpan focus persona when the user drifts.

**`requirements-clarity`** — Clarifies ambiguous requirements through focused dialogue before implementation. Asks two core questions — Why? (YAGNI check) and Simpler? (KISS check).

## Skills & config

**`skill-architecture`** — Creating and modifying skills: YAML frontmatter standards, progressive disclosure patterns, structural patterns, troubleshooting descriptions that don't trigger. Extensive reference files.

**`skill-judge`** — Evaluates skill quality against the official spec across 8 dimensions (120 points total). Use when reviewing or auditing a SKILL.md.

**`agent-md-refactor`** — Refactors bloated CLAUDE.md or AGENTS.md files using progressive disclosure: essentials at root, detailed content in linked files.

## Tooling

**`session-handoff`** — Creates handoff documents for transferring context between sessions. Also handles resuming from a handoff. Proactively suggested after substantial work or when context is running low. Auto-invokes `session-doc` after confirming a handoff when the project declares a session-docs destination.

**`session-doc`** — Produces a narrative session document for a human re-reader weeks later: why this session happened, what was done, inline decisions worth re-examining, lessons, and suggested next moves. Paired with `session-handoff` (the mechanical resume artifact), not collapsed with it — their audiences and shapes differ. Auto-fires alongside `session-handoff` when the project's `CLAUDE.md` declares a `## Session docs` destination.

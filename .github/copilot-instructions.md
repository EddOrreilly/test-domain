# Shared Agentic Workflow Instructions

This file is the shared Copilot instructions document for agentic workflow distribution.
It is intentionally repository-agnostic and describes how engineering agents should interact
with shared workflow definitions, policies, and release guidance.

## Purpose
- Keep agent guidance consistent across repositories.
- Encourage teams to follow shared workflow documentation without depending on a specific language or stack.
- Sync agentic workflow-related definitions through a central release process.

## Guidance
- Treat the shared repository as the canonical source for `AGENTS.md`, `skills/`, `TOOLS.md`, and workflow definitions.
- Keep examples high level and focused on intent, not implementation details.
- Use pull requests to update downstream repositories when the shared spec changes.

## Best practices
- Prefer generic development guidance over framework-specific instructions.
- Avoid explicit references to a single build system, language runtime, or CI provider.
- Document expected outcomes, quality goals, and review criteria.

## Local customization pattern
- Do not modify this shared, synced file inside downstream repositories unless you are changing the canonical shared guidance.
- Store repository-specific context and developer commands in a separate local file such as `.github/copilot-instructions.local.md`.
- Use variable-style placeholders to capture repo-specific values in local documentation:
  - `{{ TECH_STACK }}`
  - `{{ LOCAL_INIT_COMMAND }}`
  - `{{ LOCAL_BUILD_COMMAND }}`
  - `{{ LOCAL_DEBUG_COMMAND }}`
- Keep shared definitions and local repository context separate to avoid overwriting local changes.

## Recommended local extension workflow
1. Keep shared guidance in `.github/copilot-instructions.md`.
2. Add `.github/copilot-instructions.local.md` for repo-specific developer commands and stack context.
3. Agents or reviewers can consult both files together.

## Example local file usage
In downstream repositories, teams may create a local file with values such as:

```
# Repository-specific Copilot context

Tech stack: {{ TECH_STACK }}
Init command: {{ LOCAL_INIT_COMMAND }}
Build command: {{ LOCAL_BUILD_COMMAND }}
Debug command: {{ LOCAL_DEBUG_COMMAND }}
```

This pattern preserves shared master guidance while giving each team a safe place for their own context.

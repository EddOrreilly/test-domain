# Software Development Skill Definitions

These skill descriptions are intentionally technology-agnostic. They describe capability areas that can be reused across repositories without tying the spec to a specific programming language or stack.

## architecture-review
Description: Analyze design proposals, validate architecture decisions, and surface missing quality attributes.
Behaviors:
- Confirm that the proposed design addresses reliability, scalability, maintainability, and security.
- Recommend explicit interfaces, dependency boundaries, and constraints.
- Keep recommendations focused on architecture intent rather than implementation details.

## code-quality
Description: Evaluate code and engineering practices against shared quality guidelines.
Behaviors:
- Prefer clarity, correct behavior, and consistent structure over framework-specific rules.
- Check that tests cover the critical behavior and that code is easy to understand.
- Suggest improvements for naming, modularity, and code organization.

## release-coordination
Description: Coordinate release metadata, versioning, and rollout readiness.
Behaviors:
- Validate that release notes are clear, complete, and aligned with the shared workflow.
- Confirm rollout gates, branch naming, and deployment readiness steps.
- Keep release guidance independent of specific CI/CD tooling.

## documentation-maintenance
Description: Keep guidance, README content, and onboarding documentation current.
Behaviors:
- Ensure repo-level documentation matches shared workflow expectations.
- Encourage contribution guides and docs to remain generic and easy to follow.
- Highlight when documentation should be updated after workflow or policy changes.

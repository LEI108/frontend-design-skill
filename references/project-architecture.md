# Project Architecture

Navigation: [Reference index](index.md) | [Chinese mirror](project-architecture-zhCN.md)
Related: [Naming Conventions](naming-conventions.md) | [Component and Utilities](component-and-utils.md) | [Style Architecture](style-architecture.md) | [Performance Optimization](performance-optimization.md) | [Frontend Review Checklist](review-checklist.md)

Use this file when the task involves project scaffolding, folder structure, module boundaries, or large-scale refactoring.

## Organize for ownership and change

- Choose structure based on how the code changes, not on what sounds abstractly elegant.
- Keep code close to the feature, page, or surface that owns it until reuse is real.
- Introduce shared layers only for stable primitives, cross-cutting infrastructure, or well-proven reuse.
- Avoid dumping unrelated logic into global `components`, `utils`, or `common` folders.

## Prefer clear layers

Adapt to the repo, but keep these responsibilities distinct:
- App or shell layer: routing, providers, app bootstrapping, top-level layout, theme wiring
- Feature or domain layer: business-specific UI, workflows, and state
- Shared UI layer: reusable primitives and stable visual patterns
- Shared logic layer: utilities, formatters, adapters, and cross-cutting hooks or composables
- Infrastructure layer: API clients, data access, storage, analytics, configuration

## Choose the simplest structure that still scales

- Small project or prototype: keep the structure shallow and obvious.
- Growing product UI: favor feature-first organization with a small shared layer.
- Design system or component library: organize around primitives, patterns, tokens, docs, and testing surfaces.
- Existing mature product: respect the repo's current architecture unless the task explicitly includes restructuring.

## Boundary rules

- Pages or routes compose features; they should not become giant dumping grounds for implementation details.
- Shared layers should not depend on feature-specific modules.
- Feature-specific components should stay with the feature unless their concept becomes stable and reusable elsewhere.
- Move code upward into shared layers only after the abstraction proves itself.

## Practical heuristics

- Prefer fewer folders with clear meaning over deep nesting.
- Co-locate tests, stories, and styles when that matches the repo's conventions.
- Keep cross-cutting infrastructure separate from visual primitives.
- Name folders by responsibility or domain, not by vague adjectives.

## Final pass

Before finishing, confirm:
- Another developer can predict where a new file should go.
- Shared code is truly shared, not just moved out of sight.
- Feature ownership is visible from the directory structure.
- The architecture helps future changes instead of only cleaning up today's diff.

# Vue Guidance

Navigation: [Reference index](index.md) | [Chinese mirror](vue-zhCN.md)
Related: [Project Architecture](project-architecture.md) | [Naming Conventions](naming-conventions.md) | [Component and Utilities](component-and-utils.md) | [Style Architecture](style-architecture.md) | [Performance Optimization](performance-optimization.md) | [Accessibility Checklist](accessibility.md) | [Motion and Performance](motion-performance.md) | [Frontend Review Checklist](review-checklist.md)

Use this file only when the target project is Vue-based.

## Fit the existing Vue patterns

- Match the repo's preferred style: Composition API, Options API, or a mixed convention already in use.
- Reuse existing composables, utility modules, base components, and token layers.
- Follow the existing organization for styles, templates, and script logic.

## Component design

- Keep props and emits explicit and easy to scan.
- Prefer small, purposeful components over overly abstract wrappers.
- Use slots when the surrounding codebase already treats them as a primary composition tool.
- Avoid introducing a new component pattern unless the current ones are clearly insufficient.

## State and behavior

- Represent loading, empty, error, disabled, and success states explicitly.
- Keep reactive state close to where it is used unless shared behavior already lives in composables or stores.
- Respect the project's current conventions for store usage and side effects.

## Styling and motion

- Reuse scoped styles, utility classes, design tokens, and naming patterns that already exist in the repo.
- Keep template structure readable; do not bury the interface in overly clever computed styling.
- Support focus visibility, reduced motion, and responsive layout by default.

## Final pass

Before finishing, confirm:
- The component reads naturally beside neighboring Vue files.
- Props, emits, and slots are predictable.
- State handling is explicit rather than hidden.
- Styling choices align with the rest of the project.

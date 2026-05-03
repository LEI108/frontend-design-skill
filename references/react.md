# React Guidance

Navigation: [Reference index](index.md) | [Chinese mirror](react-zhCN.md)
Related: [Project Architecture](project-architecture.md) | [Naming Conventions](naming-conventions.md) | [Component and Utilities](component-and-utils.md) | [Style Architecture](style-architecture.md) | [Performance Optimization](performance-optimization.md) | [Accessibility Checklist](accessibility.md) | [Motion and Performance](motion-performance.md) | [Frontend Review Checklist](review-checklist.md)

Use this file only when the target project is React-based.

## Fit the existing React architecture

- Match the repo's component structure, naming style, and file organization.
- Reuse existing hooks, UI primitives, utilities, and context providers before inventing new layers.
- Follow the project's styling approach: CSS modules, Tailwind, styled components, colocated CSS, or theme objects.

## Component design

- Keep component APIs small and readable.
- Prefer composition, slots, and child composition over large prop surfaces when the codebase already uses that pattern.
- Keep presentational components focused and predictable.
- Move data fetching or cross-cutting behavior only if the local architecture expects it.

## State and interaction

- Model interactive states explicitly: loading, error, success, empty, disabled, and optimistic states where relevant.
- Keep local UI state local unless the project already centralizes it.
- Avoid introducing memoization or abstraction layers unless there is a clear benefit and the codebase already leans that way.

## Styling and motion

- Reuse theme tokens and utility conventions when available.
- Support focus states, reduced motion, and responsive behavior by default.
- Use animation sparingly and intentionally; React should not be doing work that CSS can do more cheaply.

## Final pass

Before finishing, confirm:
- The component fits the repo's existing mental model.
- The API is easy to read from call sites.
- The UI remains usable across small and large screens.
- Interaction states are covered without brittle branching.

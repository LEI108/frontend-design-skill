# Frontend Review Checklist

Navigation: [Reference index](index.md) | [Chinese mirror](review-checklist-zhCN.md)
Related: [Project Architecture](project-architecture.md) | [Naming Conventions](naming-conventions.md) | [Component and Utilities](component-and-utils.md) | [Style Architecture](style-architecture.md) | [Performance Optimization](performance-optimization.md) | [Accessibility Checklist](accessibility.md) | [Motion and Performance](motion-performance.md)

Use this file as the last pass before stopping.

## Product fit

- Does the result fit the user's product, audience, and task?
- If the project had an existing design system, did you preserve its logic and vocabulary?
- If the task was greenfield, did you commit to a clear visual idea instead of a generic default?

## UI quality

- Is the hierarchy obvious at first glance?
- Is there at least one memorable but context-appropriate detail?
- Are spacing, alignment, type scale, and visual rhythm consistent?

## State coverage

- Are hover, focus, active, disabled, loading, empty, error, and success states covered where relevant?
- Does the layout survive long labels, large numbers, and wrapped text?

## Responsiveness and accessibility

- Does the UI work on mobile, tablet, and desktop unless the scope says otherwise?
- Are keyboard access, focus visibility, readable contrast, and reduced motion handled?
- Are semantics and labels clear?

## Maintainability

- Does the code match the repo's patterns and abstractions?
- Are tokens, repeated values, and shared styles centralized?
- Were new dependencies added only when they clearly improved the outcome?

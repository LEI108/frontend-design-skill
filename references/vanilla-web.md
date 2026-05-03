# Vanilla Web Guidance

Navigation: [Reference index](index.md) | [Chinese mirror](vanilla-web-zhCN.md)
Related: [Project Architecture](project-architecture.md) | [Naming Conventions](naming-conventions.md) | [Component and Utilities](component-and-utils.md) | [Style Architecture](style-architecture.md) | [Performance Optimization](performance-optimization.md) | [Accessibility Checklist](accessibility.md) | [Motion and Performance](motion-performance.md) | [Frontend Review Checklist](review-checklist.md)

Use this file when building with plain HTML, CSS, and JavaScript.

## Structure first

- Start with semantic HTML and a clear document outline.
- Use landmarks, headings, lists, buttons, forms, and links according to their intended meaning.
- Build the simplest structure that supports the interface before layering on styling and behavior.

## Styling

- Prefer CSS custom properties for tokens such as color, spacing, type scale, radius, and shadow.
- Keep CSS organized by layout, typography, component, and state concerns.
- Use progressive enhancement instead of relying on fragile effects for the primary experience.

## Behavior

- Add JavaScript only where behavior is truly needed.
- Favor event delegation and small focused scripts over large imperative controllers.
- Keep interactive state reflected in the DOM with attributes, classes, and ARIA where appropriate.

## Responsiveness and accessibility

- Design mobile-first unless the task clearly centers a desktop artifact.
- Ensure keyboard support, visible focus, reduced motion handling, and readable contrast.
- Test long content, small screens, and no-hover environments.

## Final pass

Before finishing, confirm:
- The page still communicates clearly with CSS or JS partially unavailable.
- Styling tokens are centralized instead of repeated.
- Interactions degrade gracefully.
- The DOM structure stays understandable to future maintainers.

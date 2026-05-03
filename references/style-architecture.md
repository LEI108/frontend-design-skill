# Style Architecture

Navigation: [Reference index](index.md) | [Chinese mirror](style-architecture-zhCN.md)
Related: [Project Architecture](project-architecture.md) | [Naming Conventions](naming-conventions.md) | [Performance Optimization](performance-optimization.md) | [Vanilla Web Guidance](vanilla-web.md) | [Frontend Review Checklist](review-checklist.md)

Use this file when the task involves shared styles, design tokens, global CSS strategy, style naming, resets, or the structure of a project's styling system.

## Build styles in layers

Prefer an intentional style stack instead of letting styles accumulate ad hoc.
- Design tokens or theme variables: color, type scale, spacing, radius, shadow, z-index, motion duration, breakpoints
- Reset or base layer: normalize, reset, root element defaults, typography defaults, box sizing, media defaults
- Layout and app shell layer: page chrome, containers, grids, section spacing
- Shared utilities layer: small reusable classes or helpers for spacing, display, alignment, truncation, visually hidden content
- Component layer: component-scoped styling, variants, and state styles
- Overrides layer: controlled exceptions, theme overrides, or integration-specific patches

Keep each layer small, intentional, and easy to explain.

## Centralize global style variables

- Use CSS custom properties, theme objects, or token files for repeated values.
- Prefer semantic tokens when the product already has a design language, such as `--color-surface-primary` instead of raw color names.
- Keep one source of truth for spacing, radius, type scale, shadow, and motion timing where possible.
- Avoid scattering magic numbers and hardcoded color values across unrelated files.

## Extract shared styles with discipline

- Extract a shared utility only when it solves a repeated, stable need.
- Keep shared utilities low-level and predictable.
- Do not turn utility layers into a dumping ground for one-off visual fixes.
- Keep component-specific styling with the component unless the pattern is proven reusable.
- Prefer design tokens over copy-pasted declarations when the value is shared but the selector is not.

## Choose a naming strategy and apply it consistently

- Follow the repo's established style naming approach unless the task explicitly introduces a new styling system.
- Name classes by responsibility, state, and component role rather than visual accident.
- Keep utility naming terse but legible.
- Keep modifier or state naming consistent across the codebase.
- If using CSS Modules or scoped styles, still keep local class names readable and systematic.

## Keep declaration order predictable

Use a stable property order so styles are easy to scan. One practical order is:
- Positioning and layout
- Display and box model
- Size and spacing
- Typography
- Visual appearance
- Transforms and animation
- Miscellaneous or state-specific rules

Consistency matters more than the exact scheme; pick one and keep it stable.

## Use a clear reset or normalize strategy

- Use one base strategy, not multiple overlapping resets.
- Acceptable options include `normalize.css`, `modern-normalize`, a light custom reset, or the framework's built-in base layer.
- Make sure the team can explain what the base layer changes and why it exists.
- Keep reset logic separate from component styling and token definitions.

## Prevent style leakage and conflict

- Avoid broad global selectors unless they belong in the base layer.
- Scope component styles appropriately.
- Keep overrides explicit and rare.
- Do not let global utility classes silently fight component styles.
- Prefer predictable layering and naming over specificity wars.

## Support tooling and formatting

- Use a consistent formatter and style linter when the project supports them.
- Keep import order, file order, and declaration order predictable.
- Treat style cleanup as part of implementation quality, not optional polish.

## Final pass

Before finishing, confirm:
- The styling system has a clear set of layers.
- Shared variables and shared styles are centralized appropriately.
- Naming is consistent across global, utility, and component-level styles.
- The project uses one understandable reset or normalize strategy.
- The style architecture makes future UI work easier, not harder.

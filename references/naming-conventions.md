# Naming Conventions

Navigation: [Reference index](index.md) | [Chinese mirror](naming-conventions-zhCN.md)
Related: [Project Architecture](project-architecture.md) | [Component and Utilities](component-and-utils.md) | [Style Architecture](style-architecture.md) | [Frontend Review Checklist](review-checklist.md)

Use this file when creating, renaming, or standardizing files, folders, components, hooks, composables, utilities, and tests.

## Name for clarity and grepability

- Prefer names that reveal responsibility, not implementation trivia.
- Keep naming patterns consistent across similar artifacts.
- Match the repo's existing casing and file style unless the task includes a broader cleanup.
- Favor precise names over short but vague ones.

## Files and folders

- Name folders by domain, surface, or responsibility.
- Avoid vague buckets like `misc`, `temp`, `helpers`, `common-stuff`, or `new`.
- Use one casing convention for folders unless the repo already uses multiple.
- Keep related artifacts easy to scan near each other.

## Components and hooks

- Component names should describe the UI concept, not a styling detail.
- Hooks or composables should describe the behavior or state they expose.
- Prefer names like `UserMenu`, `BillingSummary`, `useKeyboardShortcuts`, or `useProductFilters`.
- Avoid placeholder names such as `Thing`, `Wrapper`, `HelperComponent`, or `DataManager` unless the repo already uses domain-specific equivalents.

## Utilities and domain helpers

- Utility file names should state what they transform, format, parse, validate, or map.
- Prefer `formatCurrency`, `buildChartSeries`, `parseSearchParams`, or `validateCheckoutForm` over vague names like `helpers` or `utils`.
- Separate domain logic from generic helpers when the distinction matters.

## Supporting artifacts

- Keep tests, stories, styles, and type files named predictably relative to the component or module they support.
- Do not invent one-off naming rules for a single feature.
- When renaming, update related imports and nearby artifacts together.

## Naming smells

- Names that only make sense if you already know the implementation
- Duplicate words that add no meaning
- Versioned names such as `ComponentNew`, `Form2`, or `NewUtils`
- Catch-all names that hide mixed responsibilities

## Final pass

Before finishing, confirm:
- A teammate can guess what the file does from its name.
- Similar artifacts use similar naming patterns.
- No major folder has become a vague dumping ground.
- The chosen names will still make sense after the next feature is added.

# Design Contexts

Navigation: [Reference index](index.md) | [Chinese mirror](design-contexts-zhCN.md)
Related: [Frontend Review Checklist](review-checklist.md)

Use this file when the task requires deciding how bold, conservative, or system-aligned the solution should be.

## Greenfield marketing or editorial work

- Push for a strong concept, memorable composition, and higher visual novelty.
- Use type, color, layout, and motion to create a clear first impression.
- Treat conversion, storytelling, and emotional tone as first-class concerns.
- Still keep the code shippable, responsive, and accessible.

## Greenfield product or application UI

- Prioritize clarity, hierarchy, and task completion over pure spectacle.
- Let the interface have character, but protect legibility and scanability.
- Reserve the boldest moves for hero moments, onboarding, section headers, or key empty states.
- Keep common workflows calm and easy to parse.

## Existing product or design system work

- Reuse existing tokens, components, spacing rules, typography, and interaction patterns first.
- Ask: "Does this project already know how to solve this?" before creating anything new.
- Preserve brand continuity unless the user explicitly asks for a redesign.
- Improve quality through refinement, polish, and better composition rather than stylistic replacement.

## Shared component or library work

- Optimize for reuse, API clarity, extensibility, and state coverage.
- Design the default state first, then disabled, loading, error, compact, dense, and long-content cases.
- Avoid styling choices that only work in one page context.
- Prefer primitives and slots over one-off wrapper components.

## Decision prompts

Ask these internally before choosing a direction:
- Is this greenfield work or an extension of an existing product?
- Is the user asking for bold differentiation or quiet fit?
- Is this a shared primitive, a page-level pattern, or a one-off surface?
- Where should creativity show up: layout, typography, color, motion, illustration, or content framing?
- Which parts must stay stable for maintainability or design-system consistency?

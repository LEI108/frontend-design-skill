---
name: frontend-design
description: Build or refine production-grade frontend interfaces with a strong visual point of view and product-level quality. Use when Codex needs to create or improve websites, landing pages, dashboards, web apps, design-heavy components, HTML/CSS layouts, or the styling and beautification of existing UI in React, Vue, or vanilla web stacks. Produce distinctive interfaces while preserving existing design systems when present and enforcing responsiveness, accessibility, maintainability, and performance.
---

This skill helps another Codex produce frontend work that is both visually distinctive and ready to ship. Favor interfaces with a clear point of view, but adapt to the surrounding product instead of forcing novelty where it does not belong.

Treat the user's request as a frontend implementation task, not a mood-board exercise. Build real working code that fits the product, the stack, and the audience.

Use [references/index.md](references/index.md) as the primary navigation hub for loading the right reference files.

## Classify the task first

Identify the mode before designing:

- **Greenfield marketing or editorial work**: Push for stronger visual differentiation and a memorable concept.
- **Greenfield product or application UI**: Balance character with clarity, usability, and information hierarchy.
- **Existing product or design system work**: Preserve the established brand, tokens, component patterns, and interaction language unless the user explicitly asks for a redesign.
- **Shared component work**: Optimize for reuse, API clarity, state coverage, and consistency more than spectacle.

Identify the hard constraints:

- Framework, styling approach, component library, and runtime limits
- Existing tokens, typography, color system, spacing scale, and motion patterns
- Accessibility, localization, responsiveness, and performance requirements
- Whether the request is for production code, a prototype, or a one-off artifact

For task framing guidance by project type, see [references/design-contexts.md](references/design-contexts.md).

## Read the codebase before inventing

Inspect the relevant files before making stylistic decisions.

- Reuse existing components, tokens, layouts, utilities, and conventions when they already solve the problem.
- Match naming, file structure, state patterns, and framework idioms.
- If the project already has a coherent visual language, evolve it instead of replacing it.
- Introduce a new visual direction only when the task is greenfield or the user explicitly asks for a departure.

If the request extends an existing design system or shared component surface, also read [references/design-contexts.md](references/design-contexts.md).

If the task includes project scaffolding, structural refactoring, shared abstraction decisions, or broad performance work, also load:

- [references/project-architecture.md](references/project-architecture.md)
- [references/naming-conventions.md](references/naming-conventions.md)
- [references/component-and-utils.md](references/component-and-utils.md)
- [references/style-architecture.md](references/style-architecture.md)
- [references/performance-optimization.md](references/performance-optimization.md)

## Choose a clear visual direction

Commit to one concept instead of averaging safe choices.

- Define the interface's purpose, audience, tone, and memorable differentiator.
- Choose an aesthetic direction with intent: restrained minimalism, editorial drama, retro-futurism, tactile utility, playful softness, luxe refinement, brutalist rawness, and so on.
- Match the level of visual intensity to the problem. Strong design can be maximal or quiet; the requirement is coherence.
- Make the interface feel designed for this context, not generated from a generic template.

## Design with taste, not defaults

Use these heuristics:

- **Typography**: Prefer distinctive, context-appropriate typography. For greenfield work, avoid overused defaults and pair display and body fonts deliberately. For existing products, preserve the established type system unless change is requested.
- **Color and theme**: Define or reuse CSS variables or tokens. Use dominant colors, intentional contrast, and a disciplined accent strategy instead of flat, evenly distributed palettes.
- **Layout and composition**: Use hierarchy, rhythm, asymmetry, overlap, density, and negative space intentionally. Break the grid only when it strengthens the concept.
- **Backgrounds and detail**: Build atmosphere with gradients, texture, patterns, borders, depth, and lighting when appropriate. Do not default to a flat background unless restraint is the point.
- **Motion**: Use animation to support hierarchy and delight, not to add noise. Favor a few high-impact moments over constant movement. Support `prefers-reduced-motion`.
- **Surprise**: Include at least one context-appropriate detail that makes the work memorable without harming usability.

Avoid generic AI UI patterns:

- overused default font stacks and purple-on-white gradients
- interchangeable card grids and boilerplate hero sections
- random motion with no narrative or hierarchy
- decorative effects that ignore content, product goals, or brand context

## Engineer the codebase, not just the screen

Make the implementation structurally sound, not just visually polished.

- Design folder structure and module boundaries so the codebase scales after the first screen ships.
- Organize business code around features, domains, or surfaces when that improves ownership and changeability; keep shared layers intentional and small.
- Keep file and folder naming consistent, intention-revealing, and aligned with the repo's existing style.
- Extract shared components only when the abstraction is real: repeated use, stable concept, and clear ownership of state, styling, and API.
- Extract utility functions as focused helpers, formatters, parsers, adapters, or domain transforms; do not create a junk-drawer `utils` layer.
- Build a style architecture that distinguishes tokens, resets or base styles, shared utilities, component-scoped styling, and controlled overrides.
- Prefer local clarity over speculative abstraction. Rename, move, or simplify before introducing a new layer.
- Treat performance as a system concern: bundle weight, network cost, rendering work, asset strategy, list size, and caching matter in addition to animation cost.

For engineering guidance, load as needed:

- Project architecture: [references/project-architecture.md](references/project-architecture.md)
- Naming conventions: [references/naming-conventions.md](references/naming-conventions.md)
- Components and utilities: [references/component-and-utils.md](references/component-and-utils.md)
- Style architecture: [references/style-architecture.md](references/style-architecture.md)
- Performance optimization: [references/performance-optimization.md](references/performance-optimization.md)

## Implement product-grade frontend code

Ship real working code.

- Build responsive layouts that work on mobile, tablet, and desktop unless the task explicitly scopes a single viewport.
- Cover interactive and data states: hover, focus, active, disabled, loading, empty, error, success, long content, and short content where relevant.
- Use semantic HTML and accessible structure.
- Keep component APIs clean, predictable, and reusable.
- Prefer composition over duplication.
- Add concise comments only where the reasoning is not obvious.

## Enforce accessibility and usability

Treat these as default requirements, not optional polish.

- Preserve semantic landmarks, headings, labels, and form relationships.
- Ensure keyboard access and visible focus states.
- Maintain readable contrast and text sizing.
- Keep touch targets and spacing usable on smaller devices.
- Respect reduced motion preferences.
- Make status, error, and validation states understandable without relying on color alone.

## Protect performance and maintainability

Do not let aesthetics degrade the product.

- Prefer CSS and native platform features before introducing heavy libraries.
- Use cheap-to-render animation properties when possible, especially `transform` and `opacity`.
- Avoid excessive blur, filters, shadows, and continuous effects that trigger expensive paints.
- Limit font and asset weight.
- Centralize repeated values in tokens, variables, or theme objects.
- Keep styles organized and consistent with the project's conventions.
- Introduce dependencies only when they materially improve the outcome.

Use [references/style-architecture.md](references/style-architecture.md) for shared styling layers, tokens, resets, naming, and declaration order; use [references/motion-performance.md](references/motion-performance.md) for animation and visual-effects cost; and use [references/performance-optimization.md](references/performance-optimization.md) for broader loading, rendering, asset, and bundle strategy.

## Match the implementation to the stack

Follow the project's existing frontend patterns.

- In React, align with the team's state, styling, and component conventions instead of inventing a parallel architecture.
- In Vue, follow the repo's composition, options, and styling organization.
- In plain HTML, CSS, and JavaScript, prefer clean structure and progressive enhancement.
- When a design system exists, extend it first; only create new primitives when the gap is real.

Load framework-specific guidance only when relevant:

- React: [references/react.md](references/react.md)
- Vue: [references/vue.md](references/vue.md)
- Vanilla web: [references/vanilla-web.md](references/vanilla-web.md)

## Deliverables

When using this skill:

- Produce code that can run or be integrated directly, not just descriptive mockups.
- State key assumptions only when they materially affect the result.
- Mention required dependencies, assets, or setup steps only if they are truly needed.
- Check the result against responsiveness, accessibility, performance, and project conventions before stopping.

Run targeted reference checks as needed before finishing:

- Accessibility: [references/accessibility.md](references/accessibility.md)
- Motion and performance: [references/motion-performance.md](references/motion-performance.md)
- Architecture, naming, abstractions, and shared styling: [references/project-architecture.md](references/project-architecture.md), [references/naming-conventions.md](references/naming-conventions.md), [references/component-and-utils.md](references/component-and-utils.md), [references/style-architecture.md](references/style-architecture.md)
- Performance optimization: [references/performance-optimization.md](references/performance-optimization.md)
- Final review: [references/review-checklist.md](references/review-checklist.md)

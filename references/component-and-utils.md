# Component and Utilities

Navigation: [Reference index](index.md) | [Chinese mirror](component-and-utils-zhCN.md)
Related: [Project Architecture](project-architecture.md) | [Naming Conventions](naming-conventions.md) | [Style Architecture](style-architecture.md) | [Frontend Review Checklist](review-checklist.md)

Use this file when deciding what should stay local, what should become a reusable component, and what should be extracted into utilities or helpers.

## Extract only real abstractions

- Repetition alone is not enough; the concept should also be stable.
- Extract when the abstraction reduces cognitive load, clarifies ownership, or removes risky duplication.
- Keep code local when reuse is speculative or the surface is still changing rapidly.
- Prefer obvious code in the feature over clever indirection in a shared layer.

## Component layers

- Primitive components: buttons, inputs, layout shells, typography, and foundational UI pieces
- Shared pattern components: stable reusable combinations such as cards, banners, modals, data tables, and navigation patterns
- Feature components: business-specific modules that belong to one domain or workflow
- Page or section composition: one-off assembly components that should usually stay near the page

## Rules for shared components

- Keep generic components free from domain-specific business rules.
- Prefer composition, slots, or children when that keeps the API smaller and easier to evolve.
- Avoid prop explosions that turn a supposedly reusable component into a configuration monster.
- Move a component into shared layers only after multiple real call sites prove the abstraction.

## Rules for utilities

- Extract pure transformations, formatters, parsers, validators, mappers, and adapters when they are reused or conceptually important.
- Keep UI-specific behavior out of generic utility files.
- Keep domain logic near the domain unless it is intentionally shared.
- Distinguish between pure utilities, framework hooks or composables, and infrastructure helpers.

## Common failure modes

- A global `utils` folder that mixes formatting, domain rules, network helpers, and UI hacks
- Shared components that secretly depend on one product flow
- Tiny one-line helpers extracted only to make a file look shorter
- Reusable wrappers with unclear ownership of styling, layout, and state

## Final pass

Before finishing, confirm:
- The extracted abstraction has at least one clear reason to exist beyond repetition.
- Business-specific logic is not leaking into generic shared layers.
- Utility files are focused and named by responsibility.
- The resulting code is easier to understand from call sites, not harder.

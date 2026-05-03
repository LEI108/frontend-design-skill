# frontend-design

English | [简体中文](README.zh-CN.md)

`frontend-design` is a Codex skill for building production-grade frontend interfaces with a strong visual point of view.

It is meant for real frontend work, not just mockups: interfaces that must fit the product, the stack, and the codebase while still feeling designed.

## What It Is For

- Greenfield marketing pages or editorial layouts
- Product or application UIs that need clear hierarchy and polish
- Existing products that should improve without breaking the current design system
- Shared components that need to feel reusable, consistent, and maintainable
- React, Vue, or vanilla HTML/CSS/JS frontend work

## What It Optimizes For

- A clear visual direction instead of averaged, generic UI
- System fit when a design language already exists
- Accessibility, responsiveness, and usability
- Maintainable structure, naming, and style architecture
- Performance-aware motion and effects

## How It Is Organized

- `SKILL.md`: the main trigger and workflow guide
- `references/index.md`: the navigation hub for supporting files
- `agents/openai.yaml`: UI metadata for skill lists and default prompts
- `references/*.md`: focused guidance for architecture, framework patterns, accessibility, motion, performance, and review

## Recommended Reading Order

- Start with `references/design-contexts.md` to decide how bold the interface should be.
- Read the framework guide that matches the stack: `react.md`, `vue.md`, or `vanilla-web.md`.
- Use `project-architecture.md`, `component-and-utils.md`, `naming-conventions.md`, and `style-architecture.md` when the task involves structure or reuse.
- Finish with `accessibility.md`, `motion-performance.md`, `performance-optimization.md`, and `review-checklist.md` before handoff.

## Notes

- This skill is meant to produce real working frontend code, not just visual concepts.
- When an existing product or design system is present, preserve it unless the user explicitly asks for a redesign.
- Load references as needed; do not pull in everything by default.

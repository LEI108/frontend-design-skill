# Motion and Performance

Navigation: [Reference index](index.md) | [Chinese mirror](motion-performance-zhCN.md)
Related: [Performance Optimization](performance-optimization.md) | [Accessibility Checklist](accessibility.md) | [Frontend Review Checklist](review-checklist.md)

Use this file when the task includes animation, layered effects, or heavy visual treatment.

## Motion rules

- Animate to reinforce hierarchy, orientation, and delight, not as constant decoration.
- Prefer a few strong moments over many competing ones.
- Keep entrance and hover motion short and readable.
- Respect `prefers-reduced-motion` with reduced or removed nonessential animation.

## Cheap animation first

- Prefer `transform` and `opacity` for most animation.
- Be cautious with `filter`, `backdrop-filter`, large blur radii, and complex box-shadow animation.
- Avoid scroll-linked effects that cause heavy repaint or layout work unless the payoff is substantial.

## Visual effects budgeting

- Use gradients, grain, glass, and layered shadows deliberately rather than everywhere.
- Keep the heaviest effects on isolated surfaces, not the whole page.
- Provide simpler fallbacks when the effect is central but expensive.

## Asset and dependency discipline

- Limit the number and size of fonts, images, and third-party libraries.
- Do not add an animation library when CSS covers the need.
- Reuse tokens and utilities instead of repeating effect values inline.

## Final pass

Before finishing, confirm:
- The interface remains smooth on ordinary hardware.
- Motion improves comprehension instead of slowing it down.
- Heavy effects are localized and justified.
- The design still works when motion or effects are reduced.

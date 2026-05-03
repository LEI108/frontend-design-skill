# Accessibility Checklist

Navigation: [Reference index](index.md) | [Chinese mirror](accessibility-zhCN.md)
Related: [Motion and Performance](motion-performance.md) | [Frontend Review Checklist](review-checklist.md)

Use this file for any task that ships UI, especially before final handoff.

## Structure and semantics

- Use semantic landmarks and heading order that reflect the content structure.
- Use real buttons for actions and real links for navigation.
- Ensure form controls have labels, hints, and error messaging relationships.

## Keyboard and focus

- Make all interactive elements reachable by keyboard.
- Provide visible focus states with sufficient contrast.
- Ensure dialogs, menus, and popovers manage focus predictably.

## Readability

- Maintain readable color contrast for text, controls, and meaningful UI boundaries.
- Avoid overly small text and overly tight line-height.
- Do not communicate critical meaning by color alone.

## Motion and feedback

- Respect `prefers-reduced-motion`.
- Avoid motion that obscures content or makes tasks harder to complete.
- Ensure loading, success, and error states are understandable in text, not just visual treatment.

## Responsive usability

- Keep touch targets large enough for mobile use.
- Test zoomed and narrow layouts for clipped text and hidden controls.
- Confirm content remains understandable when text wraps or expands.

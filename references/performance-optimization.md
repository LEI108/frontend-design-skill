# Performance Optimization

Navigation: [Reference index](index.md) | [Chinese mirror](performance-optimization-zhCN.md)
Related: [Motion and Performance](motion-performance.md) | [Project Architecture](project-architecture.md) | [Component and Utilities](component-and-utils.md) | [Style Architecture](style-architecture.md) | [Frontend Review Checklist](review-checklist.md)

Use this file for frontend performance work beyond animation aesthetics: loading, bundle size, rendering cost, asset strategy, long lists, and runtime efficiency.

## Think in systems, not isolated tweaks

- Performance is shaped by architecture, data flow, dependencies, assets, and rendering strategy.
- Optimize the biggest bottleneck first instead of applying random micro-optimizations.
- Measure when possible, but even without tooling, make decisions that reduce obvious work.

## Loading and bundle strategy

- Prefer route-level or surface-level code splitting when the app is large enough to benefit.
- Do not add heavy dependencies for small conveniences.
- Remove dead UI patterns, duplicate helpers, and unused assets when touching a feature.
- Keep initial render paths lean; defer noncritical features when possible.

## Rendering and reactive work

- Avoid unnecessary rerenders, recomputations, watchers, or expensive derived work in hot paths.
- Virtualize or window large lists instead of rendering everything at once.
- Debounce or throttle expensive reactions when the interaction model allows it.
- Use memoization only when it actually reduces real work and fits the repo's conventions.

## Network, data, and caching

- Fetch only the data the surface needs.
- Avoid duplicated requests and redundant transforms.
- Cache at the right layer when repeated navigation or repeated computation is a real cost.
- Keep optimistic or live-updating flows efficient and scoped.

## Assets, images, and fonts

- Use appropriately sized and compressed images.
- Prefer responsive image strategies for large media surfaces.
- Limit font families, weights, and unnecessary variants.
- Do not let decorative assets dominate the critical path.

## CSS and layout cost

- Keep selectors, layout rules, and effects understandable and affordable.
- Avoid layout thrashing caused by repeated synchronous reads and writes.
- Prefer simpler layout systems when the visual result is equivalent.
- Treat heavy shadows, filters, and layered effects as budgeted choices.

## Final pass

Before finishing, confirm:
- Initial loading cost matches the importance of the surface.
- The runtime work scales reasonably as data grows.
- Lists, media, and dependencies are not doing avoidable work.
- The result feels fast in the user's normal flow, not just in an ideal demo state.

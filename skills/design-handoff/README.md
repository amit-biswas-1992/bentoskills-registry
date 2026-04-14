# Design Handoff

Turn designs into developer-ready specs: spacing tokens, typography, component breakdown, interaction states, and edge cases. Design Handoff bridges the gap that usually costs teams a week of back-and-forth.

## What it does

Given a design (Figma link, image, or described mockup), it produces:

- **Component inventory** — what to build, atomic → composite
- **Spacing + layout spec** — exact values, responsive behavior
- **Typography scale** — sizes, weights, line heights, letter-spacing
- **Color tokens** — used colors mapped to semantic names
- **Interaction states** — hover, focus, active, disabled, loading, error
- **Edge cases** — empty states, overflow, long content, no-data, errors
- **Open questions** — things the engineer will need to ask

## When to use it

- Before kicking off dev work on a new feature
- When PM says "we need this shipped by Friday" and design isn't ready for handoff
- To audit an existing handoff document for gaps
- When translating a client's Figma into implementation tickets

## How to use it

```bash
claude code install design-handoff
```

```
@design-handoff spec https://figma.com/file/abc123/Dashboard
```

## Example output

```
# Handoff: Dashboard card

## Component: <DashboardCard>

Props:
  - title: string (required)
  - subtitle?: string
  - status: "active" | "paused" | "error"
  - onClick?: () => void

Spacing:
  - Padding: 24px
  - Gap between title and subtitle: 4px

Typography:
  - Title: Inter 18/24, weight 600
  - Subtitle: Inter 14/20, weight 400, color zinc-400

Interaction:
  - Default: bg zinc-900, border zinc-800
  - Hover: border violet-500, cursor pointer
  - Focus: 2px violet-500 ring, offset 2px

Edge cases:
  - Title wraps after 2 lines with ellipsis
  - Subtitle is optional — card height adjusts
  - Error status uses red-500 accent on left border
```

## License

MIT

# Design Critique

Get structured, opinionated design feedback on any UI — from flows and wireframes to polished screens. Design Critique helps you catch usability issues, visual hierarchy problems, and inconsistencies before they ship.

## What it does

When you invoke this skill, Claude analyzes your design (image, Figma URL, or live page) and returns a prioritized critique covering:

- **Usability** — interaction affordances, touch targets, information scent
- **Visual hierarchy** — scan paths, emphasis, whitespace, contrast
- **Consistency** — spacing, type scale, component reuse
- **Accessibility signals** — color contrast, focus indicators, text size

## When to use it

- Before a design review with stakeholders
- Before handing designs to engineering
- When something feels "off" but you can't articulate why
- To validate a design decision against best practices

## How to use it

```bash
claude code install design-critique
```

Then in your Claude Code session:

```
@design-critique review ./screens/checkout.png
```

or paste a Figma URL:

```
@design-critique review https://figma.com/file/abc123/Checkout
```

## Example output

```
# Critique: Checkout flow

## Critical
- CTA "Pay now" lacks sufficient contrast against the background (3.1:1, needs 4.5:1)
- The "Order summary" section is visually equal-weighted with "Shipping" — users will scan past it

## Strong
- Price breakdown uses clear hierarchy with the total emphasized
- Error states are placed inline next to the failing field
```

## License

MIT — free for any use.

# Design System

A skill for building and maintaining design systems that don't rot. Design System helps you audit what you have, fill gaps, and document what's missing — across tokens, components, and usage guidelines.

## What it does

**Audit**
- Scan components for duplicate variants
- Find hardcoded colors/spacing values that should be tokens
- Surface components that exist but aren't used
- Detect inconsistencies in naming, spacing, or typography

**Extend**
- Design a new component that fits the system
- Add a new token layer (e.g., semantic colors)
- Migrate from one token system to another
- Propose a component API that matches existing patterns

**Document**
- Write component usage docs with examples
- Draft a "when to use" / "when not to use" section
- Build a contribution guide for your system
- Generate a visual changelog from commits

## When to use it

- Starting a new design system and unsure where to begin
- Inheriting a system that grew organically
- Migrating from Tailwind to CSS custom properties (or vice versa)
- Your components directory has 14 button variants and you don't know why

## How to use it

```bash
claude code install design-system
```

```
@design-system audit ./components
@design-system document ./components/Button.tsx
@design-system propose a Dialog component that matches our Card and Sheet patterns
```

## Example output

```
# Design System Audit

## Hardcoded values found (should be tokens)
- components/Button.tsx:34 — color "#7C5CFF" → use --color-accent
- components/Card.tsx:12 — padding "24px" → use --space-6

## Duplicate variants
- Button has "primary", "default", "main" — these all render the same
- Recommend: consolidate to "primary" and delete the others

## Missing coverage
- No Dialog/Modal component
- No Toast/Notification component
- Form components (Input, Select) exist but no Checkbox or Radio
```

## License

MIT

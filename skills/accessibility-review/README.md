# Accessibility Review

A skill that audits your UI, component, or entire page against **WCAG 2.1 AA** and returns a prioritized list of violations, severities, and concrete fixes.

## What it does

- Runs through all four WCAG principles: **Perceivable, Operable, Understandable, Robust**
- Checks color contrast ratios (text, icons, non-text content)
- Validates keyboard navigation paths and focus order
- Reviews ARIA usage and semantic HTML
- Flags issues with form labels, error messages, and status updates
- Checks responsive behavior at 200% zoom and 320px viewport

## When to use it

- Before shipping any user-facing UI
- When required for compliance (ADA, EN 301 549, Section 508)
- As part of a design system review
- When investigating user complaints about usability

## How to use it

```bash
claude code install accessibility-review
```

Point it at a file, URL, or component:

```
@accessibility-review audit ./components/checkout-form.tsx
@accessibility-review audit https://example.com/signup
```

## Example output

```
# WCAG 2.1 AA Audit: Signup form

## Critical (must fix)
- SC 1.4.3 — Placeholder text fails contrast (2.8:1)
- SC 3.3.2 — Email field has no visible label
- SC 2.4.7 — No visible focus indicator on custom button

## Serious
- SC 1.3.5 — Input type="text" should be type="email"
- SC 4.1.2 — Custom dropdown missing aria-expanded

## Summary
3 critical, 2 serious, 1 moderate issue
```

## License

MIT

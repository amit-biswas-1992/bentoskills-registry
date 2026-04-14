# UX Copy

Write UX copy that is clear, human, and does the actual work. UX Copy helps you draft and refine microcopy across every surface: buttons, errors, empty states, loading messages, onboarding, and email.

## What it does

- Drafts new copy from a brief, tone, and constraints
- Reviews existing copy and suggests tighter alternatives
- Adapts to your brand voice (provide examples)
- Flags jargon, passive voice, and vague CTAs
- Writes variants for A/B testing

## When to use it

- Designing any new UI that has text (hint: every UI has text)
- Translating vague PM requirements into real button labels
- Fixing error messages that blame the user
- Writing onboarding that explains without lecturing

## How to use it

```bash
claude code install ux-copy
```

Ask it for what you need:

```
@ux-copy write an empty state for "No results found" — friendly, suggests next action
@ux-copy review this error: "An error occurred. Please try again."
```

## Example output

**Prompt:** Write an empty state for a project list with no projects.

**Response:**
```
Option 1 (encouraging):
  Title: Start your first project
  Body: Projects help you group work and invite teammates.
  CTA: Create a project

Option 2 (minimal):
  Title: No projects yet
  CTA: New project

Option 3 (contextual):
  Title: You're all set — now what?
  Body: Create a project to start collaborating.
  CTA: Create project
```

## License

MIT

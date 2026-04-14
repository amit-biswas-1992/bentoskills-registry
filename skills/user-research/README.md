# User Research

A skill for the full research loop: planning, running, and synthesizing user research — from generative interviews to usability tests. User Research helps you produce insights you can actually act on.

## What it does

**Plan**
- Write a research plan from a product question
- Draft discussion guides for 1-on-1 interviews
- Build usability test scripts with tasks and success criteria
- Suggest recruiting criteria and screener questions

**Conduct**
- Coach you through active listening patterns
- Help stay neutral and avoid leading questions
- Convert raw notes into clean transcripts

**Synthesize**
- Cluster raw quotes into themes
- Surface tensions and contradictions
- Pull out jobs-to-be-done from interviews
- Draft an insights report with recommendations

## When to use it

- Starting a new feature and you need customer input
- You have interview notes sitting in Notion that never got synthesized
- Planning a usability test and need a script
- Translating research into PM-ready findings

## How to use it

```bash
claude code install user-research
```

```
@user-research plan a generative study for "how do designers collaborate with engineers"
@user-research synthesize ./interviews/*.md
```

## Example output

```
# Research synthesis: Designer-engineer collaboration (n=8)

## Top themes
1. Handoff is the friction point — 7 of 8 mentioned
2. Designers want to see their work in production, not Figma
3. Engineers want locked specs, not "final-final-v3.fig"

## Tensions
- Designers want iteration after handoff; engineers want stability

## Opportunities
- A tool that locks a design at handoff but allows proposed revisions
- Visual diff between Figma spec and shipped code
```

## License

MIT

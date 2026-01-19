# The Invisible Users: Designing the Web for AI Agents and Everyone Else

**Full comprehensive guide examining how modern web design optimized for human users fails for AI agents, and how fixing this benefits everyone.**

## Context: What Are AI Agents?

AI agents are machines with technical limitations that parallel human disabilities. They're statistical pattern-matching systems, not intelligent beings. Understanding their constraints informs practical web design decisions.

**Key insight:** Patterns that help AI agents (semantic HTML, structured data, explicit state) are the same patterns that help users with disabilities. Both need semantic structure because both lack access to visual design cues.

**The agent journey through your website:**

1. **Discovery** - Training data includes your semantic HTML
2. **Citation** - Agents recommend sites with clear structured data
3. **Comparison** - Agents parse your metadata to build feature lists
4. **Purchase** - Agents complete transactions using explicit state attributes

Miss any stage, the entire commerce journey breaks. JavaScript-rendered content, generic class names, and visual-only feedback break this journey at multiple points.

## Overview

This is the complete "Bible" version of The Invisible Users, containing:

- **13 chapters** covering business, legal, security, technical, and strategic perspectives
- **Executive summary** and preface
- **Comprehensive glossary** of technical terms
- **Illustrations** (SVG sources, PNG generated via build scripts)

## Status

**Publication:** Due Q1 2026
**Word count:** ~78,000 words core manuscript
**Current state:** Complete and ready for publication

## Contents

### Core Chapters

1. **Chapter 0:** What Are AI Agents?
2. **Chapter 1:** What You Will Learn
3. **Chapter 2:** The Invisible Failure
4. **Chapter 3:** The Architectural Conflict
5. **Chapter 4:** The Business Reality
6. **Chapter 5:** The Content Creator's Dilemma
7. **Chapter 6:** The Security Maze
8. **Chapter 7:** The Legal Landscape
9. **Chapter 8:** The Human Cost
10. **Chapter 9:** The Platform Race
11. **Chapter 10:** Generative Engine Optimization
12. **Chapter 11:** Designing for Both
13. **Chapter 12:** Technical Advice
14. **Chapter 13:** What Agent Creators Must Build

### Supporting Materials

- **bible-plan.md** - Master plan with chapter outlines and status
- **executive-summary.md** - High-level overview for decision-makers
- **Glossary.md** - Comprehensive technical glossary
- **illustrations/** - Visual diagrams (SVG sources, PNG outputs)

## Shared Resources

This book references shared resources maintained in separate packages:

- **Appendices:** [packages/shared-appendices/](../shared-appendices/) - 12 appendices including implementation guides, code examples, and resources
- **Code examples:** [packages/shared-code-examples/](../shared-code-examples/) - Production-ready implementations

## Build Commands

Generate book outputs (from repository root):

```bash
# Generate PNG illustrations from SVG sources
npm run illustrations:generate

# Generate HTML (open in browser and print to PDF)
npm run pdf:bible-html

# Generate A4 PDF with cover (for review/distribution)
npm run pdf:bible-generate

# Generate 6"×9" PDF for Kindle Direct Publishing
npm run pdf:bible-kindle

# Generate simple PDF without cover
npm run pdf:bible-simple

# Generate all formats
npm run pdf:bible-all
```

## Writing Style

- **British English** throughout (organise, colour, whilst)
- **First-person narrative voice**
- **No colons in chapter titles**
- **Professional tone** without unnecessary superlatives
- **Real, concrete examples** over theoretical discussion

See [docs/for-ai/writing-style.md](../../docs/for-ai/writing-style.md) for complete guidelines.

## Target Audience

This comprehensive version is designed for:

- **Web developers** and designers implementing AI-friendly patterns
- **Business leaders** understanding commercial implications
- **Legal and security professionals** navigating compliance requirements
- **Content creators** adapting workflows for agent-mediated web
- **Platform architects** designing for dual audiences

For a focused practical guide, see [Don't Make AI Think](../dont-make-ai-think/).

## Contributing

This manuscript is in final editing for publication. For questions or corrections:

- Email: <tom.cranstoun@gmail.com>
- Website: <https://allabout.network>

## License

PROPRIETARY - All rights reserved

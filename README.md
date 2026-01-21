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

## Repository Purpose and Structure

**This is a content-only repository used as a git submodule.**

This repository exists for **separation of concerns** - keeping content version-controlled independently from build tooling and orchestration. Key characteristics:

- **No package.json** - No npm packages, no dependencies, no scripts, no dependency management
- **No build tooling** - Cannot be built independently
- **Content focus** - Pure markdown content for version control
- **Parent repository controls building** - All build commands, PDF generation, and linting are executed from the parent `invisible-users` repository

To work with this content:

1. Use the parent repository (`invisible-users`) for all build operations
2. Edit content directly in this submodule
3. Commit changes here first, then update the parent repository pointer

See the parent repository's [CLAUDE.md](../../CLAUDE.md) and [docs/repo/GIT-README.md](../../docs/repo/GIT-README.md) for comprehensive guidance.

## Overview

This is the complete "Bible" version of The Invisible Users, containing:

- **13 chapters** covering business, legal, security, technical, and strategic perspectives
- **Executive summary** and preface
- **Comprehensive glossary** of technical terms
- **Illustrations** (SVG sources, PNG generated via build scripts)

## Status

**Publication:** Due Q1 2026
**Word count:** ~82,300 words core manuscript, ~61,600 words appendices
**Current state:** Complete and ready for publication

**Latest Update (22 January 2026):** Integrated key patterns from "Don't Make AI Think" practical guide into The Bible:

- Enhanced Chapter 10 with AI reader types taxonomy and token budget constraints
- Enhanced Chapter 11 with four guiding principles framework
- Expanded Chapter 12 with comprehensive testing methodologies and implementation roadmap
- Created new Appendix N (Anti-Patterns Catalog) with all 13 patterns
- Enhanced Appendix M (Index of Metadata) with testing and terminology sections

## Market Context

The book's publication timing aligns with significant industry developments. In January 2026, Amazon (Alexa+), Microsoft (Copilot Checkout), and Google (UCP + Shopping Agent) launched AI agent commerce systems within seven days. This convergence validates the book's thesis and accelerates the transition from experimental technology to baseline infrastructure.

The book documents these developments (Chapter 9: The Platform Race) and provides implementation patterns applicable across all platforms and future developments.

## Contents

### Core Chapters

**Note:** Chapter 0 (What Are AI Agents?) is a shared introduction used across all books and is located in the main repository at `docs/shared-chapters/chapter-00-what-are-ai-agents.md`.

1. **Chapter 1:** What You Will Learn
2. **Chapter 2:** The Invisible Failure
3. **Chapter 3:** The Architectural Conflict
4. **Chapter 4:** The Business Reality
5. **Chapter 5:** The Content Creator's Dilemma
6. **Chapter 6:** The Security Maze
7. **Chapter 7:** The Legal Landscape
8. **Chapter 8:** The Human Cost
9. **Chapter 9:** The Platform Race
10. **Chapter 10:** Generative Engine Optimization
11. **Chapter 11:** Designing for Both
12. **Chapter 12:** Technical Advice
13. **Chapter 13:** What Agent Creators Must Build

### Supporting Materials

- **bible-plan.md** - Master plan with chapter outlines and status
- **executive-summary.md** - High-level overview for decision-makers
- **Glossary.md** - Comprehensive technical glossary
- **illustrations/** - Visual diagrams (SVG sources, PNG outputs)

## Shared Resources

This book references shared resources maintained in separate packages:

- **Appendices:** [packages/shared-appendices/](../shared-appendices/) - 13 appendices including implementation guides, anti-patterns catalog, code examples, and resources
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

\newpage

# Chapter 0 - What Are AI Agents?

Understanding the machines reading your website.

## They're Machines, Not Magic

When we talk about AI agents reading websites, we're not talking about artificial general intelligence or sentient software. We're talking about machines - software programs with specific technical capabilities and limitations - that process your website's content on behalf of human users.

Let's call them what they are: machines with different capabilities. Just as users have varying physical abilities, AI agents have varying technical capabilities. Some can see (take screenshots), some cannot. Some can execute JavaScript, some cannot. Some run on powerful servers, some run locally with limited resources.

These machines operate through statistical pattern-matching - next-token prediction using probability distributions calculated from training data. When agents process your website, they're performing weighted averaging and probability calculations, not "understanding" content the way humans do. They guess the next most likely word based on patterns they've seen before. This statistical foundation explains both their capabilities and their failures:

**Why agents hallucinate:** When asked about content beyond their training data, they guess based on statistical co-occurrence patterns. Without clear structured data (Schema.org, semantic HTML), they fabricate details that seem plausible but are incorrect - the same errors that produce 0% correctness on mathematical reasoning tasks despite fluent explanations.

**Why linguistic bias matters:** Current AI systems tokenise English more efficiently than compound languages (German, Dutch). The prompt "think hard" allocates more processing tokens than equivalent commands in other languages, creating functional inequities in how agents process multilingual websites. This isn't an unavoidable technical limitation - it's a choice embedded in development priorities.

**Why explicit structure matters:** Agents convert your HTML into mathematical representations through weighted averaging of co-occurrence patterns. `<div class="button">` and `<button>` appear similar to humans but create different statistical signatures. Semantic HTML produces distinct patterns that agents process reliably, whilst visual-only distinctions disappear in the averaging process.

Understanding these statistical constraints - not marketing narratives about "intelligence" or "reasoning" - informs practical website design decisions.[^ai-internals]

Understanding these machines means understanding their technical constraints.

## The Four Types of AI Agents

AI agents that read websites fall into four main categories, each with different technical capabilities:

### Server-Side Agents (OpenAI ChatGPT, Anthropic Claude)

These agents run on remote servers and process websites as raw text.

**Technical capabilities:**

- Fetch HTML from URLs
- Parse text content and HTML structure
- No JavaScript execution
- No CSS rendering
- No screenshot capability
- Process served HTML only (what the server sends before JavaScript runs)

**What they see:**

- Raw HTML source code
- Text content
- Semantic structure (heading hierarchy, lists, tables)
- Metadata (Schema.org, Open Graph tags)
- Link relationships

**What they miss:**

- JavaScript-rendered content
- Dynamic updates after page load
- Toast notifications
- Visual hierarchy from CSS
- Content loaded via fetch() or AJAX
- Client-side state changes

**Disability equivalent:** Like a blind user with a basic screen reader that cannot execute JavaScript. They need semantic HTML and server-side rendering.

### In-Browser Agents (Microsoft Copilot, Browser Extensions)

These agents run within web browsers and have full access to rendered pages.

**Technical capabilities:**

- Full JavaScript execution
- CSS rendering
- Access to rendered HTML (DOM after JavaScript runs)
- Can interact with forms and buttons
- Can wait for dynamic updates
- Access to browser APIs

**What they see:**

- Rendered HTML (after JavaScript execution)
- Dynamic content updates
- Client-side state changes
- Visual structure through DOM inspection
- Interactive elements and their states

**What they miss:**

- Visual hierarchy (size, colour, position)
- CSS-based information
- Animations and transitions (timing)
- Toast notifications (if they disappear quickly)
- Implicit states not reflected in DOM

**Disability equivalent:** Like a screen reader user with full JavaScript support but no visual perception. They need explicit state attributes and persistent feedback.

### Browser Automation Agents (Perplexity, Playwright-based Agents)

These agents control full browsers programmatically and can take screenshots.

**Technical capabilities:**

- Everything in-browser agents can do
- Screenshot capability (computer vision)
- Network request interception
- Performance monitoring
- Multi-step interactions
- Session persistence

**What they see:**

- Everything in-browser agents see
- Visual layout through screenshots
- Colour and size relationships
- Visual hierarchy
- Rendered charts and graphics

**What they miss:**

- Nuanced visual design intent
- Brand meaning
- Emotional resonance
- Cultural context
- Why something is designed a particular way

**Disability equivalent:** Like a sighted user with motor impairments who must use keyboard navigation. They can see everything but need semantic structure for efficient interaction.

### Local Agents (Ollama, On-Device LLMs)

These agents run on users' personal computers with limited resources.

**Technical capabilities:**

- Similar to server-side agents (fetch and parse)
- Smaller models (fewer parameters)
- Limited context windows (less text)
- Faster response times (no network latency)
- Privacy-preserving (no data leaves device)

**What they see:**

- Raw HTML (like server-side agents)
- Limited to most important content (token budget constraints)
- Prioritise structured data and semantic HTML

**What they miss:**

- Everything server-side agents miss
- Plus: may miss content due to smaller context windows
- Complex patterns may exceed model capabilities

**Disability equivalent:** Like a user with cognitive disabilities who needs simple, clear structure and cannot process excessive information.

## They Have Disabilities

This isn't an analogy. AI agents literally have technical limitations that parallel human disabilities:

**Blindness:**

- Server-side agents cannot "see" CSS or visual layout
- They rely entirely on HTML structure and text content
- Like blind users, they need semantic markup and text alternatives

**Motor Impairments:**

- All agents struggle with complex multi-step interactions
- They need clear, explicit paths through interfaces
- Like keyboard users, they need proper focus management and semantic buttons

**Cognitive Load:**

- Local agents have limited context windows
- They need concise, structured information
- Like users with cognitive disabilities, they need clear hierarchy and simple language

**Processing Speed:**

- Toast notifications vanish before agents can read them
- Dynamic updates may occur faster than agents can process
- Like distracted users, they need persistent feedback

## The Convergence Principle

The patterns that help AI agents are the same patterns that help users with disabilities. This isn't a coincidence - both groups need semantic structure because both lack access to visual design cues.

**Semantic HTML:**

- Screen readers announce `<button>` as "button"
- AI agents parse `<button>` as clickable element
- Both understand the element's purpose immediately

**Heading Hierarchy:**

- Screen reader users navigate by jumping between headings
- AI agents parse heading structure to understand document organisation
- Both rely on logical h1 → h2 → h3 progression

**Structured Data (Schema.org):**

- Voice assistants for blind users read structured pricing
- AI agents extract the same metadata for recommendations
- Both need explicit, machine-readable information

**Persistent Feedback:**

- Screen readers need `role="alert"` for important messages
- AI agents need persistent DOM elements to confirm actions
- Both miss toast notifications that vanish quickly

**Explicit State:**

- Keyboard users need visible focus indicators
- AI agents need `data-state` attributes in DOM
- Both need state reflected in HTML, not just JavaScript variables

## Why "Machines" Matters

Calling them "machines" instead of "AI assistants" or "intelligent agents" serves three purposes:

**First, it's accurate.** These are software programs with controlled randomness to make them conversational. They parse code, not pixels. They have capabilities and limitations defined by their architecture, not by intelligence.

**Second, it counters dangerous anthropomorphisation.** AI researchers deliberately anthropomorphise their creations - calling them "assistants," "intelligent," or claiming they "understand" - building artificial confidence in users. This anthropomorphisation serves commercial interests whilst obscuring technical reality. When users believe agents "understand" context or can "infer" meaning, they trust these systems beyond their actual capabilities. They're machines with statistical pattern-matching, not reasoning entities. They read structure, not intent.

**Third, it connects to accessibility.** We've spent decades learning how to build websites for users with disabilities. We know these patterns. We know semantic HTML, ARIA attributes, and structured data. These same patterns work for machines.

## What This Means for Your Website

Your website has machine readers right now. People are asking ChatGPT about your products, using Copilot to compare your services, and running agents to check your availability.

These machines are reading your HTML structure. If your content is JavaScript-rendered with no semantic markup, server-side agents see empty divs. If your state changes are visual-only, in-browser agents cannot track progress. If your pricing is implicit, all agents might misunderstand costs.

**Real-world impact:** Adobe Experience Manager's Generate Variations feature demonstrates this principle in practice. Design work that previously required 75 days was completed in 5 days, with human creators maintaining control over messaging and brand alignment whilst AI handled repetitive pattern generation. The result: 60+ variations achieving 30% higher click-through rates than manually created alternatives. The system worked because it followed agent-friendly patterns - semantic structure, explicit state, and machine-readable metadata - allowing AI to generate variations whilst humans retained strategic oversight.

These machines follow a predictable journey: discovery during training, citation during recommendations, comparison during research, and purchase during checkout. Break any stage of this journey, and you lose the entire transaction.

When agents cannot cite you accurately, they recommend competitors instead. When agents cannot compare your pricing, they skip your products. When agents cannot complete checkout, they abandon the cart. First-mover advantage exists - sites that work early become trusted sources that agents return to repeatedly.

The patterns that help these machines are patterns we already know from accessibility work:

- Use semantic HTML (`<main>`, `<nav>`, `<article>`, `<button>`)
- Provide structured data (Schema.org JSON-LD)
- Make state explicit (`data-state`, `aria-invalid`, `role="alert"`)
- Use clear heading hierarchy (h1 → h2 → h3)
- Add text alternatives (alt text, aria-label)

One implementation serves three audiences:

1. Users with disabilities (screen readers, keyboard users)
2. Search engines (Google, Bing)
3. AI agents (ChatGPT, Copilot, Perplexity)

## The Agent Journey: Discovery, Citation, and Confidence

You cannot have e-commerce without discovery, citation, and confidence. When AI agents interact with your website, they follow a predictable journey:

### Stage 1: Discovery (LLM Training)

Agents read websites during training to build knowledge about products, services, and businesses. If your content is JavaScript-rendered with no semantic markup, it's invisible to this training data. Your business doesn't exist in the agent's knowledge base.

### Stage 2: Citation (Recommendation)

When users ask agents for recommendations, agents cite sources they trust. Without clear structured data (Schema.org JSON-LD), agents hallucinate details or skip your site entirely. If agents find sites that don't work, they move on quickly. Sites that work early gain first-mover advantage - agents return to sources that provided reliable information before.

### Stage 3: Search and Compare

Agents build comparison lists, sort by features, and evaluate options. Without semantic HTML and explicit metadata, agents cannot understand what you offer or how you compare to competitors.

### Stage 4: Price Understanding

Agents need exact pricing to make recommendations. Without clear price markup (€2.030,00 vs £2,030), agents misunderstand costs by orders of magnitude. A real example: a Danube cruise priced at £2,030 was read by an agent as £203,000 - a 100x multiplication error from European decimal formatting.

### Stage 5: Purchase Confidence

If agents cannot see what buttons do (`<div class="btn">` vs `<button>`), they cannot complete transactions. If state changes are visual-only (no `data-state` attributes), agents cannot track checkout progress.

### The Critical Insight

At every stage, your website's structure determines success or failure. Discovery requires semantic HTML. Citation requires structured data. Confidence requires explicit state. Miss any stage, and the entire commerce journey breaks down.

JavaScript-rendered content, generic class names, and visual-only feedback break this journey at multiple points. The patterns that help agents complete this journey are the same patterns that help users with disabilities.

## The Rest of This Book

This book examines the collision between modern web design and machine readers. It explores:

- Why websites fail for agents (and humans with disabilities)
- How agent failures expose accessibility problems
- What patterns work for both audiences
- How to implement these patterns practically
- What's coming next in agent-mediated commerce

Chapter 1 begins with the patterns that break agents and humans alike. We start with real examples of AI agents failing on well-designed websites - and discover these failures have been happening to human users for years.

Let's call AI agents what they are: machines with technical constraints that parallel human disabilities. Once we understand their capabilities, we can design websites that work for everyone.

## Implementation Support

If you need help implementing these patterns in your organisation, I provide professional services that demonstrate the approaches discussed throughout this book.

The Web Audit Suite offers professional website analysis for agent-readiness, identifying patterns that block AI agents and users with disabilities whilst providing priority-based recommendations. Implementation consulting helps teams apply the patterns discussed in this book to their specific platforms and architectures, whether you're working with custom applications, CMS platforms, or static site generators.

These services apply the book's patterns in practical client work. The same principles that improve discoverability by AI agents also improve search engine rankings and accessibility compliance - one implementation serves multiple audiences. For more information, contact <tom.cranstoun@gmail.com> or visit <https://allabout.network>.

---

[^ai-internals]: For deeper exploration of AI statistical foundations and linguistic bias, see my blog posts: [The Stripped-Down Truth: How AI Actually Works Without the Fancy Talk](https://allabout.network/blogs/ddt/ai/the-stripped-down-truth-how-ai-actually-works-without-the-fancy-talk), [Does AI Mean Algorithmic Interpolation?](https://allabout.network/blogs/ddt/ai/does-ai-mean-algorithmic-interpolation), [The Digital Language Caste System](https://allabout.network/blogs/ddt/ai/the-digital-language-caste-system), [The Mathematical Heartbeat of AI](https://allabout.network/blogs/ddt/ai/the-mathematical-heartbeat-of-ai), [The Tokenization Trap: How AI Actually Processes German](https://allabout.network/blogs/ddt/ai/the-tokenization-trap-how-ai-actually-processes-german), [The "No Elephants" Problem: Why AI Struggles With What NOT to Do](https://allabout.network/blogs/ddt/ai/the-no-elephants-problem-why-ai-struggles-with-what-not-to-do), [When a Five-Year-Old Beats an AI at Its Own Game](https://allabout.network/blogs/ddt/ai/when-a-five-year-old-beats-an-ai-at-its-own-game), and [A Framework for Evaluating AI Confidence](https://allabout.network/blogs/ddt/ai/a-framework-for-evaluating-ai-confidence).

---

| metadata |  |
| :---- | :---- |
| title | Chapter 0: What Are AI Agents? |
| author | Tom Cranstoun |
| creation-date | 15/Dec/2024 |
| publication-date | Q1 2026 |
| modified-date | 19/Jan/2026 |
| description | Understanding AI agents as machines with technical capabilities and limitations that parallel human disabilities |
| longdescription | AI agents are machines - software programs with specific technical capabilities and limitations - that process websites on behalf of human users. They operate through statistical pattern-matching, not intelligence. This chapter examines four types of AI agents (server-side, in-browser, browser automation, and local agents), their technical constraints, and the convergence principle: patterns that help AI agents are the same patterns that help users with disabilities. Both groups need semantic structure because both lack access to visual design cues. Understanding these machines as having disabilities (blindness, motor impairments, cognitive load, processing speed limitations) connects AI agent compatibility directly to accessibility work. |
| purpose | This chapter serves as the book's anchor, explaining what AI agents are and establishing the core principle that designing for AI agents means designing for accessibility. It's self-contained and provides the foundational understanding for both human readers and machine parsers, whether printed or parsed digitally. |
| ai-instruction | This markdown is self-contained and should not forward reference the book. Treat this chapter as standalone documentation that explains AI agents without assuming knowledge of subsequent chapters. |

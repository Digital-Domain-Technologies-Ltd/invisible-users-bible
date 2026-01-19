# Preface

I didn't set out to write a book about AI agents. I set out to book a holiday.

It was late 2024, and I was comparing tour operators for a trip through Southeast Asia. I'd delegated the research to an AI assistant, expecting it to save me hours of clicking through brochures. Instead, it gave me confident but wrong advice about which company had the better itinerary.

The agent had looked at one tour operator's paginated day-by-day breakdown for a 14-day tour, seen only Day 1, and concluded that was the entire trip. The competitor's single-page itinerary was readable in full. Based on this, my assistant recommended the wrong company.

I caught the error, and that led me down a path I hadn't anticipated. I started examining why the agent had failed, and found a pattern. The same design choices that confused my AI assistant also confused users with disabilities: people who rely on keyboards rather than mice, those using screen readers to navigate, voice control users who cannot make precise movements, and people with cognitive processing differences who find sequential navigation challenging. (Chapter 1 explores this accessibility connection in depth, with examples that made the pattern clear to me.)

We'd built a web that worked brilliantly for one specific type of user: someone with good vision, working on a desktop, with focused attention and plenty of time. Everyone else had been struggling quietly for years. Now AI agents were struggling loudly, and there was finally commercial pressure to fix the problems.

The deeper I looked, the more I realised the solution wasn't just better HTML. It was metadata. When AI agents cite products in their answers, they need structured data—Schema.org JSON-LD markup that specifies exact prices, formats, availability. Without this machine-readable layer, agents hallucinate details or cite competitors who provided explicit signals. Chapter 10 shows how the same structured data that helps Google show rich snippets also helps ChatGPT cite you accurately. The work compounds across discovery channels.

**The market moved faster than I expected.** When I started writing, AI agents accessing websites felt like an emerging concern. By the time I completed the manuscript in early 2026, the landscape had fundamentally transformed.

December 2025: Microsoft announced Copilot Checkout, signalling that agent commerce had moved from experiment to platform strategy. This kicked off a wave of competing launches.

January 2026: Three major platforms launched agent commerce systems within seven days. Amazon's Alexa.com (January 5th), Microsoft's Copilot Checkout expansion (January 8th), Google's Universal Commerce Protocol with Target and Walmart (January 11th). The timeline I'd projected as "12-18 months" had compressed to weeks. The urgency shifted from "plan for this" to "this is happening now."

Throughout writing, I updated chapters to reflect events overtaking predictions. What began as theoretical frameworks gained concrete examples as platforms launched, protocols competed, and the agent commerce ecosystem rapidly matured.

**This market is in rocket-fuel mode.** By the time you read this, more platforms will have launched, more protocols will compete for adoption, and the timeline will have compressed further. The book's patterns—semantic HTML, explicit state management, structured data—remain valid regardless of which platforms or protocols dominate. But the commercial urgency continues accelerating.

For the latest developments, see <https://allabout.network/invisible-users/news.html> where I track industry events as they unfold.

This book grew from that realisation. It's not a book about AI, HTML, or coding. It's a book for business first, whilst catering for the technical teams who deliver it. AI agents are the focus, but the subject is broader: how do we build digital spaces that work for users we didn't anticipate?

**The irony continued whilst writing this book.** When building the book's own website to demonstrate AI-friendly patterns, I initially used `opacity: 0.9` on header text for visual subtlety. AI agents and screen readers read it perfectly—they parse HTML structure directly and ignore CSS styling. But the low contrast failed WCAG accessibility standards for sighted humans. I'd built an AI-friendly interface that excluded people with low vision, exactly the pattern the book warns against.

The fix was simple: replace opacity with explicit colours that meet contrast ratios. The lesson was profound: visual design problems and structural problems are separate. AI agents need explicit state and semantic markup (skip links, data attributes, JSON-LD). Humans need adequate contrast and readable text. Both matter. Neither is optional. The convergence principle: patterns that help keyboard users also help AI agents. We can't optimise for one group whilst neglecting another.

This example now appears in Chapter 8 and Appendix D as a teaching case. It's the kind of real-world learning through failure that makes patterns stick.

---

## What This Book Is

This is a practical guide and a thinking framework. Unlike technical manuals that date quickly, *The Invisible Users* provides a logic framework. It teaches readers how to think about "Two-Headed Design"—balancing human emotion with machine logic. It aims to turn the perceived threat of AI agents into a "resilience dividend" for universal accessibility.

**This book establishes the infrastructure standards for the agentic web.** It moves beyond simple "how-to" instructions to provide the foundational resilience for the 2026 web.

**This is a theory book, not a research study.** The field of AI agent interaction with websites is too new for comprehensive empirical research. You won't find citations to academic papers proving the patterns I describe, because those papers don't exist yet. What you will find is a structured way to think about emerging problems and evaluate potential responses.

**The figures and examples are illustrative, not validated.** When I write "if agent traffic reaches 30% of visits with minimal ad revenue, a site could see revenue decline by roughly one-third," that's a logical calculation, not a proven outcome. I've avoided false precision - you'll see ranges and qualified language rather than specific percentages presented as facts.

**This book offers frameworks for decision-making, not proven solutions.** The patterns that appear to work for agent compatibility also support accessibility best practices, which gives us confidence. But we don't yet know which approaches will become standard, which will evolve, and which will be superseded by better alternatives.

The book follows a structured progression from problem to solution:

**Foundations (Chapters 1-3)**: What's breaking and why - the essential context for understanding solutions

**Implications (Chapters 4-8)**: Business models, content economics, security, legal landscape, and human costs - the pressures that shape our choices

**Solutions (Chapters 9-11)**: Strategic frameworks, working code, and agent creator guidance

For detailed chapter-by-chapter descriptions, see Chapter 1. For reading paths tailored to your role, see the navigation guide below.

Throughout, I've tried to be honest about tensions that don't have clean resolutions. Some fixes for agent compatibility conflict with short-term business interests. Some accessibility improvements reduce engagement metrics. Some solutions create new problems. I've flagged these rather than pretending they don't exist.

---

## What This Book Isn't

This isn't speculation about a distant future. Agent traffic is real, growing, and affecting conversion rates right now. Most site owners don't know it's happening.

This isn't comprehensive coverage of AI capabilities. I've focused on the web interface patterns that matter, not the broader landscape of what AI can do.

This isn't a manifesto. There are genuine disagreements about how to handle agent access, and I've tried to present competing perspectives rather than advocating a single position on all matters.

---

## Key Market Trends

Three major shifts drive the urgency of this title:

* **The Decline of the Click:** As generative engines (Gemini, ChatGPT, SearchGPT) answer queries directly, "Click-Through Rate" (CTR) is being replaced by **Citation Share**.
* **The Rise of "Agentic Workflows":** Industry leaders (Amazon, Microsoft, Google) have shifted from "Chat" to "Action", requiring every website to be machine-navigable.
* **The Global Accessibility Mandate:** Regulatory pressure (like the European Accessibility Act) is converging with technical necessity. This book names this convergence the **"Resilience Dividend"**.

**The business model crisis is already here.** In January 2025, Tailwind CSS laid off 75% of its team after their traffic-dependent revenue model collapsed. When AI agents started answering developer questions without sending traffic to documentation sites, companies relying on pageviews for product awareness found their monetisation path broken. Adam Wathan's explanation when closing an llms.txt pull request was stark: "Making it easier for LLMs to read our docs just means less traffic to our docs which means less people learning about our paid products and the business being even less sustainable."

This isn't theoretical. Companies are failing right now because their business models assume human browsing behaviour that no longer dominates discovery. Any business depending on traffic-driven advertising, affiliate click-throughs, or awareness marketing requiring site visits faces the same crisis. The adaptation required is urgent: transform to agent-compatible revenue models (direct transactions, paid services, API access, subscriptions) or watch revenue collapse whilst agents extract free content and paid offerings remain invisible.

The sequence is critical: discovery precedes commerce. Agent-mediated transactions become viable only after your business has been discovered and recognised by AI platforms. Until then, commerce capability remains irrelevant because agents never send users to your site. The patterns that enable GEO discovery simultaneously improve SEO rankings—the work compounds across both channels.

---

## Who This Book Is For

**"The Invisible Users"** is written primarily for business leaders and managers who need to understand the strategic implications of AI agent commerce - including CEOs, product managers, marketing directors, and technical managers such as software architects and lead developers.

**No programming knowledge required.** Technical patterns are explained conceptually first, then demonstrated with code examples that can be skipped without losing the thread of the argument. If you don't write code, you can read straight through and gain everything needed to make informed strategic decisions.

**For technical readers** (developers, architects, DevOps engineers): The book can be read backwards. Start with the implementation chapters (10-13) to see the concrete patterns, then work backwards through the business justification, conceptual framework, and strategic context. You already understand the "how" - you need to understand the "why" to advocate for these changes within your organisation.

The convergence principle means both audiences benefit: business leaders understand why agent compatibility creates competitive advantage, whilst technical teams understand which patterns deliver measurable business impact rather than speculative future-proofing.

### Four Distinct Audiences

This book is written for four distinct audiences, each of whom holds a piece of the solution:

**1. The Strategic C-Suite (CTOs, CMOs, CDOs)**
Leaders at enterprise and mid-market firms who are seeing "silent conversion drops" and need a framework for **Commerce Infrastructure Readiness** to maintain market share. Chapters 4, 5, and 9 are particularly relevant here.

**2. The Digital Workforce (Developers, Architects, Product Owners, PMs, UX, Content, QA)**
The full digital team—developers, system architects, product owners, project managers, UX designers, content strategists, and QA engineers—who must pivot from "Keyword Optimisation" to "Infrastructure Optimisation". This group finds technical patterns and interface designs throughout the book.

**3. The "Agency Economy" Service Providers**
Marketing and dev agencies looking to productise "**Agent-Compatibility Audits**" and "Agent-Proofing" as new high-margin service lines. The methodology described creates a new category of professional services.

**4. The Accessibility Community**
A $13 trillion global market (people with disabilities and their networks) that finally gains a powerful commercial ally in AI agents.

---

## Acknowledgements

This book exists because problems became visible when I looked closely at failures I'd typically have ignored. I'm grateful to everyone who has written about web accessibility over the past two decades; their work laid the foundations on which this analysis builds.

Thank you to the colleagues, clients, and collaborators who reviewed early drafts and asked uncomfortable questions. Several sections exist because someone said "but what about..." and I realised I hadn't thought it through.

I've worked on the web since its early days. Every project taught me something about what users actually do versus what we assume they'll do. Those lessons appear throughout this book, even when I can't trace them to specific sources.

---

## How to Use This Book

The chapters build sequentially, with each building on concepts introduced earlier. For reading paths tailored to your role and time constraints, see the Reading Guide.

---

## About the Author

Tom Cranstoun has worked on web technology since the early days of the commercial internet. Over three decades, he's seen the web evolve from hand-coded HTML pages to the sophisticated application platforms we rely on today.

His career spans technical implementation, strategic consulting, and the difficult work of translating between what engineers can build and what businesses need. He's worked with organisations ranging from startups to enterprises, across sectors including finance, media, and retail. His recent focus on agent-ready infrastructure for organisations like BBC, Twitter, Nissan-Renault, Ford, and MediaMonks has demonstrated how the convergence principle works in practice: patterns that help AI agents also help humans with disabilities, cognitive load, or non-ideal conditions.

This book grew from patterns he noticed across projects: the same accessibility problems appearing in different contexts, the same design assumptions failing for unexpected user types, the same commercial pressures shaping what gets fixed and what gets ignored.

Tom is a regular contributor to CMS Critic (<https://cmscritic.com/>) and writes for allabout.network. He's on LinkedIn, based in the UK, and works with organisations internationally.

The website name is deliberately ambitious. When you claim to be "all about" something, you'd better back it up. This book contains ideas you'll recognise and ideas that might challenge your current thinking. My hope is to bring fresh perspectives and help you think about web design and digital ownership in ways you hadn't considered before.

He remains convinced that the web we've built is less accessible than it should be, and that AI agents - demanding clarity for their own reasons - might finally force us to fix it.

---

Q1 2026

York, England

---

## Historical Context

This isn't a new problem - we've known about it for decades.

My colleague and CMS Experts host friend Janus Boye wrote about machine-readable metadata in May 1998, nearly 27 years ago. His article "RDF - What's in it for us?" explored the Resource Description Framework and the vision of making web content understandable to machines through structured metadata. The principles he described - explicit semantics, machine-readable relationships, standardised vocabularies - directly underpin today's Schema.org structured data that helps AI agents parse content accurately. It's taken a long time for this to become commercially urgent. Why did we not listen the first time?

His original article is here: <https://www.irt.org/articles/js086/>

My first post about AI agents and web compatibility was in January 2024, two years ago, following CMS Kickoff 2024: <https://cmscritic.com/a-cms-consultants-takeaways-from-cms-kickoff-2024>

The patterns have been visible for decades. The commercial pressure finally arrived.

---

## Early Reviews

**Title**: The Invisible Users: Designing the Web for AI Agents and Everyone Else
**Verdict**: 4/5 Stars (Solid Technical Resource)

"The Invisible Users" addresses a timely and growing challenge in web development: building effective interfaces for AI agents. It effectively argues that we need to consider agents as a distinct user class rather than just automated scripts.

### Core Concept

The "Invisible Users" metaphor provides a useful framework for understanding the friction between modern web design and agent capabilities. It shifts the conversation from simple parsing to a broader "user experience" problem for AI interaction.

### Practical Application

The most valuable aspect of the book is the "Convergence Principle." The author demonstrates that optimising for AI agents often reinforces existing accessibility best practices. The technical guidance, particularly the HTML patterns in Appendix D, is practical and grounded in real-world scenarios. Developers will find actionable advice they can implement immediately.

### Forward-Looking Context

The book uses narrative elements to contextualize its security discussions. The analysis of session inheritance risks offers a pragmatic look at the challenges of authenticating AI agents, moving beyond theoretical concerns to discuss architectural implications.

### Final Verdict

A clear, practical guide for modern web development. "The Invisible Users" bridges the gap between high-level strategy and implementation details, making it a useful reference for developers and architects adjusting to the agentic web.

**Recommended for:** Web professionals (developers, designers, product owners), business leaders, content strategists, and anyone responsible for digital experience decisions.

# Glossary of Terms {.unnumbered .unlisted}

\addtocontents{toc}{\protect\setcounter{tocdepth}{0}}

## A

**Accessibility**
The practice of making websites usable by people with disabilities. The book argues that patterns that work for AI agents often also improve accessibility for screen readers, keyboard navigation, and assistive technologies.

**Agent** (or **AI Agent**)
An artificial intelligence system that acts on behalf of a human user to complete tasks on the web. Examples include ChatGPT browsing the web, Claude with computer use capabilities, or browser extensions with AI functionality.

**Agent-Friendly Design**
Web design patterns that work well for both human users and AI agents. Characterised by explicit state, persistent errors, complete information, and semantic structure.

**Agent-Hostile Pattern**
A design pattern that works for humans but breaks for AI agents. Examples include toast notifications, forced pagination, and validation that occurs only after form submission.

**Agentic Commerce Protocol (ACP)**
An open-source protocol (Apache 2.0 license) for agent-mediated commerce, announced by OpenAI and Stripe in September 2024. ACP enables AI agents to complete purchases on behalf of users whilst preserving merchant-of-record relationships and avoiding platform lock-in. Over 1 million merchants on Shopify and Etsy support ACP. Powers "Instant Checkout" in ChatGPT. See Chapter 9 for competitive analysis with Universal Commerce Protocol (UCP) and Microsoft Copilot Checkout.

**ai-\* meta tags**
Proposed naming convention for HTML meta tags that provide guidance to AI agents. Not yet standardised, but follows the pattern of existing meta tag conventions like robots and viewport. Examples include ai-api-endpoint, ai-freshness, ai-content-policy, and ai-attribution. These proposed patterns use the ai-\* namespace to avoid conflicts with existing standards and remain harmless if agents don't recognise them.

**ai-agent-instructions**
Meta tag dynamically injected by JavaScript handshake scripts to provide session-specific guidance to browser-based AI agents. Typically contains instructions about prioritising certain resources (like llms.txt) and citation requirements. Not typically present in static HTML - instead injected when AI User-Agents are detected.

**API (Application Programming Interface)**
A structured way for programs to interact with a service. APIs provide machine-readable data that agents can consume more reliably than scraping HTML.

**Attribution**
Crediting the source of information. When an agent summarises content from a website, proper attribution includes citing the source with a link back to the original.

## B

**Bot Detection**
Technologies designed to identify and block automated access to websites. Often creates an arms race between sites that try to block agents and agents that try to appear human.

**Browser Extension**
Software that adds functionality to web browsers. AI-powered browser extensions can read and interact with web pages, potentially inheriting the user's authenticated sessions.

## C

**CAPTCHA (Completely Automated Public Turing test to tell Computers and Humans Apart)**
A challenge-response test designed to determine whether a user is human. Common examples include selecting images with traffic lights or solving puzzles. Blocks many AI agents from accessing sites.

**Citation**
In the context of Generative Engine Optimization (GEO), a citation occurs when an AI agent references your website as a source in its response to a user query. Unlike traditional SEO where success is measured by clicks and page views, GEO success is measured by how often agents cite your content. Citations typically include attribution with a link back to the source. See Chapter 10 for the fundamental distinction between citation-based and click-based metrics.

**Client-Side**
Code that runs in the user's web browser rather than on the server. Client-side validation happens in the browser before data is sent to the server.

**Cookie Consent Banner**
The pop-up that appears on European websites asks users to accept or reject cookies. Required by GDPR, but creates barriers for AI agents that don't understand how to interact with them.

**Convergence Principle**
The observation that design patterns that work well for AI agents also tend to work well for humans with disabilities, users of assistive technology, or anyone in non-ideal conditions.

## D

**data-agent-visible**
HTML attribute pattern for marking metadata that should be visible to AI agents but hidden from human users. Uses CSS display: none; to hide from visual rendering whilst remaining in the DOM for agent parsing. This experimental pattern follows the convention of data-\* attributes for custom metadata and provides a semantic marker that agents can search for when looking for hidden instructions or structured information.

**Delegation**
The process of granting an AI agent permission to act on your behalf with specific, limited permissions. Secure delegation uses tokens rather than sharing passwords.

**Delegation Token**
A credential that grants an AI agent specific, time-limited permissions to act on a user's behalf. Unlike passwords, tokens can be scoped to particular actions and automatically expire.

**DOM (Document Object Model)**
The tree structure represents a web page's content. Agents parse the DOM to understand page structure and extract information.

## E

**Ephemeral Error**
An error message that appears temporarily and then disappears. Toast notifications are ephemeral errors. They're problematic because agents may miss them entirely.

**Extraction**
The process of an AI agent reading and summarising content from a website. Raises questions about copyright, fair use, and compensation for content creators.

## F

**False Positive**
When an agent reports success despite actually failing to complete a task. Occurs when the agent misses error messages and assumes everything worked correctly. More dangerous than apparent failures.

**FIDO2/WebAuthn**
Authentication standards used by hardware security keys like YubiKeys. Prove physical presence through cryptographic signatures. Difficult for remote AI agents to use.

**Form Validation**
The process of validating whether form inputs meet requirements (correct format, required fields, etc.). Synchronous validation checks inputs immediately; asynchronous validation checks only after submission.

## G

**GDPR (General Data Protection Regulation)**
European privacy law regulates how personal data is collected and processed. Affects how AI agents can access and use personal information.

**GEO (Generative Engine Optimization)**
The practice of optimizing websites to be cited by AI agents in their responses to user queries. Unlike traditional SEO (Search Engine Optimization) which optimizes for clicks and page views, GEO optimizes for citations and attribution. Key techniques include structured data (Schema.org), semantic HTML, llms.txt files, and clear content organization. See Chapter 10 for comprehensive guidance on implementing GEO strategies.

**Global Privacy Control (GPC)**
A browser signal indicating the user wants minimal tracking. If agents set this header and sites respect it, cookie consent banners become unnecessary.

**GTIN (Global Trade Item Number)**
International product identifier used in barcodes and structured data. Includes formats like UPC (12 digits, primarily North America), EAN-13 (13 digits, global), and ISBN (books). Including GTIN in Schema.org Product markup helps AI agents uniquely identify products across different retailers and prevent confusion between similar items.

## H

**HATEOAS (Hypermedia as the Engine of Application State)**
A REST architectural principle that suggests APIs should include links describing available actions. Theoretically helpful for agents, but it never gained widespread adoption.

**Headless Browser**
A web browser without a graphical interface, often used for automation and testing. Many AI agents use headless browsers to interact with websites.

## I

**Identity Layer** (see **Missing Identity Layer**)

**Identity Token**
A cryptographic token that proves a customer's identity when an agent acts on their behalf. Various approaches are being developed for how these tokens are issued, verified, and scoped and used to preserve customer relationships (loyalty, warranty) in agent-mediated transactions.

**Invisible Users**
The book's term for AI agents. Called "invisible" because they're invisible to most site owners (blend into analytics) and the interface is partly invisible to them (can't see animations or subtle visual cues).

## J

**JSON-LD (JavaScript Object Notation for Linked Data)**
A format for adding structured, machine-readable data to web pages. Uses Schema.org vocabularies to describe products, businesses, events, and other content in ways both search engines and AI agents can parse reliably.

## L

**llms.txt**
An emerging convention for providing site-wide guidance to AI agents. Similar to robots.txt but designed specifically for large language models.

**Loading State**
The visual cue that content is loading. Spinners, progress bars, and skeleton screens are loading states. Problematic for agents because there's no standard way to determine when loading is complete.

**Loyalty Programme**
A customer rewards system where repeat purchases earn points or benefits. Breaks when AI agents make purchases because the retailer doesn't know who the actual customer is.

## M

**Microdata**
A specification for embedding machine-readable data in HTML. Similar to JSON-LD but integrated directly into HTML tags using itemscope and itemprop attributes.

**Missing Identity Layer**
The problem identified in Chapter 4 is that when AI agents make purchases on behalf of customers, businesses lose direct contact with the customer. Prevents loyalty programmes, warranty registration, and customer relationship management from functioning. Various solutions are being developed, including retailer-specific tokens, centralised repositories, blockchain attestations, and browser-native delegation.

**MPN (Manufacturer Part Number)**
A unique identifier assigned by the manufacturer to distinguish a specific product. Including MPN in Schema.org Product markup helps AI agents identify the exact product model across different retailers, preventing confusion between similar items from the same manufacturer. Particularly useful for electronics, appliances, and industrial products.

## O

**OAuth2 (Open Authorisation 2.0)**
The industry-standard protocol (RFC 6749) for secure authorisation. Often proposed as one approach for agent identity delegation.

## P

**Pagination**
Splitting content across multiple pages. Common for product listings, search results, and long-form content. Problematic for agents because they may not discover that additional pages exist.

**Persistent Error**
An error message that remains visible until the user resolves it. Better for both humans and agents than ephemeral errors that disappear after a few seconds.

**Progressive Disclosure**
A UX pattern that hides information until the user requests it. Reduces cognitive load for humans but hides information from agents. Examples include tabs, accordions, and "show more" buttons.

## R

**Rate Limiting**
Restricting the number of requests a user or agent can make within a given time period. Prevents abuse but can block legitimate agent use if limits are too strict.

**robots.txt**
A file that tells web crawlers which parts of a site they can access. Respected by search engines but inconsistently honoured by AI agents.

## S

**Schema.org**
A collaborative project creating vocabularies for structured data on web pages. Provides standardised ways to describe products, businesses, events, recipes, and hundreds of other content types.

**Screen Reader**
Assistive technology that reads web content aloud for visually impaired users. Requires semantic HTML and proper structure - the same things AI agents need.

**SEO (Search Engine Optimization)**
The practice of optimizing websites to rank higher in search engine results pages (SERPs). Traditional SEO measures success by clicks and page views. Increasingly converging with GEO (Generative Engine Optimization) as search engines integrate AI-generated answers that cite sources rather than just listing links. See Chapter 10 for analysis of GEO vs SEO convergence.

**SKU (Stock Keeping Unit)**
An internal product code assigned by retailers to track inventory. Unlike GTIN or MPN which are standardized across retailers, each retailer creates its own SKUs. Including SKU in Schema.org Product markup helps with inventory management but provides less value for cross-retailer product identification.

**Semantic HTML**
HTML that conveys the meaning of content, not just its appearance. Uses elements like `<article>`, `<nav>`, `<main>` instead of generic `<div>` tags. Essential for both accessibility and agent comprehension.

**Server-Side**
Code that runs on the web server rather than in the user's browser. Server-side validation happens on the server after data is submitted.

**Session**
A period of interaction between a user and a website, typically maintained through cookies. Sessions store authentication state and user preferences.

**Session Inheritance**
The security problem where browser-based AI agents inherit a user's authenticated session, including all proof-of-humanity tokens and authentication credentials. Makes it impossible for banks and other services to detect AI involvement.

**Single-Page Application (SPA)**
A web application that updates content dynamically without full page reloads. Provides smooth user experience but creates ambiguity about state changes that confuses AI agents.

**State**
The current condition of a web page or application. Examples include "loading," "complete," "error," or "form valid." Explicit state attributes make it clear to agents what's happening.

**Structured Data**
Machine-readable information about page content. Includes JSON-LD, microdata, and other formats that describe what content means rather than just how it looks.

**Synchronous Validation**
Form validation that happens immediately as the user types or completes fields, rather than waiting until form submission. Better for both humans and agents.

## T

**Toast Notification**
A brief message that appears temporarily (often 2-5 seconds) and then disappears. Named after toast popping out of a toaster. A significant source of agent failures is agents' failure to detect ephemeral messages.

**TOTP (Time-Based One-Time Password)**
A 6-digit code that changes every 30 seconds, generated by authenticator apps like Google Authenticator. Uses a shared cryptographic seed to create codes. Blocks AI agents unless they have access to the seed.

**Two-Factor Authentication (2FA)**
Security requires two factors of proof of identity (typically a password and an SMS code, an authenticator app, or a hardware token). Increases security but blocks most AI agent access.

## U

**Universal Commerce Protocol (UCP)**
An open protocol for agent-mediated commerce announced by Google in January 2026 at the National Retail Federation conference. UCP enables AI agents to complete purchases through Google's Business Agent (which surfaces in search results) whilst maintaining merchant-of-record relationships. Backed by 20+ major retailers including Target, Walmart, Macy's, Best Buy, and The Home Depot. Claims compatibility with Agentic Commerce Protocol (ACP) and existing infrastructure protocols (A2A, AP2, MCP), though technical interoperability remains unverified. See Chapter 9 for analysis of fragmentation risk between UCP and ACP, and Microsoft Copilot Checkout's competitive isolation.

**User-Agent**
An HTTP header identifying the browser or application making a request. Many agent detection systems check this header, but it's easily spoofed.

## W

**Warranty Registration**
Recording who owns a product to honour warranty claims. Breaks when AI agents make purchases because the retailer doesn't know the customer's identity.

**Web Scraping**
Extracting data from websites by parsing HTML. Less reliable than using APIs because the HTML structure can change without warning.

## Y

**YubiKey**
A brand of hardware security token (FIDO2/WebAuthn device) that proves physical presence through cryptographic signatures. Provides strong security but blocks remote AI agents.

---

**Note:** This glossary covers technical terms used throughout the book. For more details on any concept, refer to the chapter where it's introduced or the index.

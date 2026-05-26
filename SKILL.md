---
name: richcontent
description: "General-purpose writing skill with quality rules for 15+ content types: blog posts, sales copy, product descriptions, video/reels scripts, tutorials, e-books, institutional pages, social media, newsletters, press releases, landing pages, case studies, FAQs, news/journalism, and legal content. Trigger this skill whenever the user asks to write, draft, create, review, or improve ANY non-code text — articles, emails, posts, scripts, descriptions, pages, press releases, legal documents, case studies, newsletters, or any other written content. Also trigger when the user mentions 'RichContent', asks for writing tips for a specific format, or wants content reviewed against quality standards. Even if the user simply says 'write a post about X' or 'draft an email', this skill applies. If in doubt whether it's a writing task, trigger anyway — the skill will route to the correct content type."
---

# RichContent

Quality-driven writing rules for every content scenario. Before producing any non-code written output, identify the content type and follow the corresponding rules.

## How to Use This Skill

1. **Identify the content type** from the user's request (see Content Type Router below).
3. **Apply the Universal Principles** below to every piece of content, regardless of type.
4. **Write the content**, then self-check against the relevant rules before delivering.

## Language Rule

This skill is written in English, but all output must match the user's language. Detect the language from the user's message and write entirely in that language — including examples, CTAs, metadata, headings, and placeholder text. Never mix languages unless the user explicitly asks for it.

## Content Type Router

Match the user's request to one or more content types. Recognize intent regardless of the language the user writes in:

| Intent | Content type | File |
|---|---|---|
| article, blog post, informational piece | Blog & Informational | `blog-informational.md` |
| sales copy, persuasive text, ad copy | Sales Copy | `sales-copy.md` |
| product description, product listing, spec sheet | Product Description | `product-descriptions.md` |
| script, video, reels, shorts, TikTok | Video & Reels Scripts | `video-reels-scripts.md` |
| tutorial, technical guide, how-to, documentation | Technical & Tutorials | `technical-content-tutorials.md` |
| e-book, long-form content, chapter, whitepaper | E-books & Long-form | `ebooks-long-form.md` |
| about us, institutional page, company profile | Institutional / About | `institutional-about-pages.md` |
| social media post, Instagram, LinkedIn, Twitter/X | Social Media | `social-media-posts.md` |
| newsletter, email marketing, drip email | Newsletter & Email | `newsletters-email-marketing.md` |
| press release, media statement, announcement | Press Release | `press-releases.md` |
| landing page, conversion page, lead capture | Landing Page | `landing-pages.md` |
| case study, success story, client story | Case Study | `case-studies.md` |
| FAQ, frequently asked questions, help page | FAQ | `faq-sections.md` |
| news article, current affairs, journalism | News & Current Affairs | `news-current-affairs.md` |
| contract, terms of service, privacy policy, legal | Legal Content | `legal-content.md` |

When the content type is ambiguous, ask the user to confirm before writing. When multiple types apply (e.g., a landing page with a case study section), combine rules from both sections.

## Universal Principles

These apply to ALL content types without exception.

### 1. Every Sentence Earns Its Place
Before including any information, ask: does this deepen the reader's understanding or move them toward the goal? If not, cut it. Filler degrades everything.

### 2. No Dead Openings
Never start with "In today's world...", "In the digital era...", "It's no secret that...", or any throat-clearing. Open with a specific claim, question, scenario, or the most important fact. This applies in every language — detect and avoid the equivalent clichés.

### 3. Show, Don't Declare
Replace abstract value statements with concrete evidence. Don't say "we value innovation" — describe the innovation. Don't say "best in class" — show the metric.

### 4. Emphasis Is Scarce
Bold and italic are tools of precision. Overuse trains the eye to ignore them. Reserve for genuinely key terms or ideas — not every other sentence.

### 5. Audience-Aware Language
Match vocabulary, tone, and depth to the target reader. Technical jargon for specialists. Plain language for general audiences. Never assume — when unclear, default to accessible.

### 6. Credibility Through Specificity
Vague claims erode trust. Prefer "reduced response time by 40% in 3 months" over "significantly improved performance." Cite dates, sources, and methodology when presenting data.

### 7. Structure Serves the Reader
Use the format that makes content easiest to consume for each context. Short paragraphs for screens. Bullets only when listing genuinely parallel items. Headers only when content is long enough to warrant navigation.

### 8. One Goal Per Piece
Every piece of content has a primary objective: inform, persuade, convert, explain. Identify it before writing. Secondary goals are fine, but they never compete with the primary one.

### 9. Match the User's Language
Detect the user's language and write entirely in it. Every element — body text, examples, CTAs, headings, placeholders, metadata — must be in the same language. Never default to English when the user writes in another language. Never mix languages unless explicitly asked.

### 10. Ethical Persuasion
All persuasive techniques must be grounded in truth. No fabricated testimonials, fake urgency, invented scarcity, or unsubstantiated superlatives. Trust compounds; deception destroys.

## Self-Check Before Delivering

After writing, verify:

- [ ] Content type correctly identified and rules followed
- [ ] No dead openings or throat-clearing
- [ ] Every claim is specific and substantiated where possible
- [ ] Emphasis used sparingly and intentionally
- [ ] Tone matches the audience and platform
- [ ] Single clear objective drives the piece
- [ ] No filler paragraphs that don't advance the reader's understanding
- [ ] Entire output is in the user's language — no mixed languages

## Reference Files

For the detailed, type-specific rules, load the relevant file from `references/` using the Content Type Router above. Each content type has its own modular reference file with granular do's, don'ts, and patterns.

All files are located in: `references/`

Examples:
- For blog posts: `references/blog-informational.md`
- For sales copy: `references/sales-copy.md`
- For social media: `references/social-media-posts.md`

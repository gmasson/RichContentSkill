# RichContentSkill 0.1

A language-agnostic writing skill that enforces quality standards across 15+ content types — from blog posts and sales copy to legal documents and video scripts. Works in any language: the skill detects the user's language and writes entirely in it.

Drop it into any conversation and every piece of written content follows consistent, opinionated rules designed to eliminate filler, dead openings, vague claims, and generic AI tone.

> English | (Português)[README.br.md] 

## What It Does

RichContent acts as an automatic quality layer. When you ask Claude to write any non-code text, the skill:

1. **Routes** the request to the correct content type (blog, email, landing page, legal, etc.)
2. **Loads** only the relevant rules — no bloated context
3. **Applies** universal principles (no dead openings, specificity over vagueness, ethical persuasion)
4. **Self-checks** before delivering

### Supported Content Types

| # | Type | Covers |
|---|---|---|
| 1 | Blog & Informational | Articles, guides, educational posts |
| 2 | Sales Copy | Persuasive text, ads, conversion copy |
| 3 | Product Descriptions | E-commerce listings, spec sheets |
| 4 | Video & Reels Scripts | YouTube, TikTok, Reels, Stories |
| 5 | Technical & Tutorials | Docs, how-tos, step-by-step guides |
| 6 | E-books & Long-form | Chapters, whitepapers, deep dives |
| 7 | Institutional / About | Company pages, mission statements |
| 8 | Social Media | LinkedIn, Instagram, Twitter/X, TikTok |
| 9 | Newsletters & Email | Email marketing, drip campaigns |
| 10 | Press Releases | Media announcements, official statements |
| 11 | Landing Pages | Conversion pages, lead capture |
| 12 | Case Studies | Client success stories, ROI narratives |
| 13 | FAQ Sections | Support pages, knowledge bases |
| 14 | News & Current Affairs | Journalism, event coverage |
| 15 | Legal Content | Contracts, terms of use, privacy policies, petitions |

## Installation

Download the latest version of the project from [Releases](https://github.com/gmasson/RichContentSkill/releases) and drag it into any Claude conversation. That's it — no config, no dependencies.

## Universal Principles

These apply to every content type, no exceptions:

1. **Every Sentence Earns Its Place** — if removing it loses nothing, remove it
2. **No Dead Openings** — never start with "In today's world..." or throat-clearing
3. **Show, Don't Declare** — replace abstract claims with concrete evidence
4. **Emphasis Is Scarce** — bold/italic used surgically, not decoratively
5. **Audience-Aware Language** — match vocabulary and depth to the reader
6. **Credibility Through Specificity** — numbers, dates, and sources over vague adjectives
7. **Structure Serves the Reader** — format chosen for consumption, not aesthetics
8. **One Goal Per Piece** — every text has a primary objective that nothing competes with
9. **Language Consistency** — output matches the user's language throughout
10. **Ethical Persuasion** — no fabricated testimonials, fake urgency, or invented scarcity

## Design Decisions

- **Two-layer architecture**: SKILL.md stays under 100 lines so it loads fast and doesn't bloat context. Detailed rules live in a reference file loaded only when needed.
- **Router-first approach**: a lookup table maps natural language triggers (in both English and Portuguese) to the correct content section, so the skill works regardless of how the user phrases the request.
- **Anti-patterns over principles**: each section includes explicit "Avoid" and "Banned Phrases" lists. Negative constraints are easier for models to follow than abstract guidance.
- **Structural templates**: every content type includes a concrete pattern block (e.g., Hook → Context → Explanation → Example → Takeaway) so the model has a skeleton, not just philosophy.
- **Aggressive triggering**: the skill description is intentionally broad to avoid undertriggering — it activates for any writing request, not just when the user says "RichContent."

## Contributing

Contributions are welcome. If you want to add a new content type, improve existing rules, or fix something:

1. Fork the repo
2. Create a branch (`git checkout -b feat/new-content-type`)
3. Edit the relevant files in `richcontent/`
4. Submit a pull request with a clear description of what changed and why

Guidelines for contributions:

- Keep SKILL.md under 120 lines — if it grows, move detail to the reference file
- Every rule should be actionable, not philosophical
- Include "Avoid" patterns alongside positive guidance
- Test with real prompts before submitting

## License

[MIT](LICENSE)

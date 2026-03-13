# AI Job Search Toolkit

A complete AI-powered job search system. Built for Claude, adaptable to other AI tools.

## What this does

- **Builds your profile** through a guided conversation that goes beyond your CV: dealbreakers, preferences, personality, working style, communication preferences
- **Searches job boards automatically** with daily scheduled searches that screen, filter, and summarise roles against your profile
- **Cross-references company reviews** from Glassdoor and other review sites, flagging red flags before you apply
- **Assesses role fit** with a structured analysis of skills gaps, dealbreakers, and honest recommendations
- **Tailors your CV and writes cover letters** in your voice, with hard rules against fabrication, inflation, and AI-sounding language

## Built from a real job search

This toolkit started as a personal job search system. The prompts were tested and refined over weeks of real use before being generalised for anyone. The search prompts have screened hundreds of listings. The anti-parroting and anti-inflation rules exist because the first drafts without them produced exactly the kind of generic, inflated output that hiring managers recognise and reject.

## Quick start

Try it in 5 minutes with a single job listing. No setup required. [See the quick start](getting-started.md#try-it-in-5-minutes).

## Full setup

The [getting started guide](getting-started.md) walks you through everything from creating an account to running your first automated search. Two paths:

- **Path A: Claude in the browser or desktop app** (recommended for most people)
- **Path B: Claude Code** (for developers and terminal users)

## What's included

### Prompts

| File | What it does |
|---|---|
| [`01-profile-builder.md`](prompts/01-profile-builder.md) | Guided conversation that generates your job search profile |
| [`02-job-search-generic.md`](prompts/02-job-search-generic.md) | Customisable template for searching any job board |
| [`02-job-search-linkedin.md`](prompts/02-job-search-linkedin.md) | LinkedIn-specific search (UK example) |
| [`02-job-search-indeed-uk.md`](prompts/02-job-search-indeed-uk.md) | Indeed UK-specific search |
| [`02-job-search-totaljobs.md`](prompts/02-job-search-totaljobs.md) | Totaljobs-specific search |
| [`03-application-assessor.md`](prompts/03-application-assessor.md) | Structured fit assessment with apply/skip recommendation |
| [`04-cv-tailor.md`](prompts/04-cv-tailor.md) | Tailor your CV to a specific role |
| [`05-cover-letter-writer.md`](prompts/05-cover-letter-writer.md) | Generate a cover letter anchored in something genuine |

### Templates

| File | What it does |
|---|---|
| [`example-profile.md`](templates/example-profile.md) | Anonymised example of a completed profile |
| [`claude-project-instructions.md`](templates/claude-project-instructions.md) | Template project instructions (CLAUDE.md) |
| [`applications-tracker.md`](templates/applications-tracker.md) | Application tracking template |
| [`memory-setup.md`](templates/memory-setup.md) | Guide to AI memory for job searching |

### Examples

| File | What it does |
|---|---|
| [`uk-job-boards.md`](examples/uk-job-boards.md) | UK job boards and company review sites guide |

## How it works

The toolkit uses a two-pass workflow:

1. **First pass (automated):** Search prompts run on a schedule via the Claude Chrome extension. They screen every listing against your profile, check company reviews, and produce a structured summary of roles worth looking at.

2. **Second pass (you + your project):** You review the summary in your Claude project, which has your full profile, CV, memory, and application history. You read the full listing yourself, assess fit, and only then use the CV tailor and cover letter writer.

The automated search surfaces candidates. The second pass is where you make the real decision.

## Built for Claude

This toolkit was built for Claude and tested with Claude's browser, desktop, Chrome extension, and Claude Code. The prompts can be adapted for other AI tools that support web browsing and file uploads, though some features (projects, memory, scheduled tasks) are Claude-specific.

## Contributing

Contributions are welcome, especially regional guides for job boards outside the UK and search prompts for new job boards. See [CONTRIBUTING.md](CONTRIBUTING.md).

## Privacy

Your data is processed by whichever AI service you use. Review their privacy policy. For Claude: [Anthropic's privacy policy](https://www.anthropic.com/privacy). You can omit sensitive information and the toolkit still works. Nothing in this toolkit sends your data anywhere beyond the AI service you're already using.

## Trademark disclaimer

This toolkit references personality assessment frameworks (Myers-Briggs, 16 Personalities, Enneagram, DISC, CliftonStrengths, Big Five). It is not affiliated with or endorsed by The Myers-Briggs Company, Gallup, NERIS Analytics, or any assessment provider. All trademarks belong to their respective owners.

## Licence

MIT. See [LICENSE](LICENSE).

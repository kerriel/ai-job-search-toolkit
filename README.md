# AI Job Search Toolkit

## Why I built this

After a couple of months of job searching, I was spending days scrolling through different job sites, losing track of what I'd already seen, and forgetting which roles I'd applied for. I knew there had to be a better way.

I've been working with Claude for a while, so I asked whether there was a way to automate the search part using the Claude Chrome extension. Turns out there was. I started with a simple prompt, and it grew from there into a full job search system: a project in Claude that knows who I am, what I'm looking for, and what to skip. It builds prompts that search job boards for me on a schedule, screens everything against my profile, and gives me a shortlist each morning. When I find something worth applying for, it can help me tighten up my CV and draft a cover letter in my own voice.

It's saved me days of time. Not just on searching, but on tracking what I've already reviewed, what I've applied for, and where things stand.

I know there are people who say you shouldn't use AI for this stuff. That's fair. But the rules I've built into this are all about keeping things honest: no fabricating experience, no inflating what I've done, no parroting the job listing's language back at them. Everything stays in my tone and my words. If a hiring manager met me in person, they'd recognise the person from the application.

This might not be perfect. It works for me, but your search will be different. You're welcome to download it, edit it, and make it your own. If something's not clear or could use better instructions, let me know and I'll try to update it. I just wanted to put it out there in case it helps someone else have a less painful job search.

## What it can do

- **Build your profile** through a guided conversation that goes beyond your CV: dealbreakers, preferences, personality, working style, how you like to communicate
- **Build prompts that search job boards automatically** via the Claude Chrome extension, screening and summarising roles against your profile on a daily schedule
- **Cross-reference company reviews** from Glassdoor and other review sites, flagging red flags before you apply
- **Assess role fit** when you paste in a job listing, with structured analysis of skills gaps, dealbreakers, and an honest recommendation
- **Help you tailor your CV and cover letters** if you want it to, with rules against fabrication, inflation, and AI-sounding language
- **Track your applications** so you know where things stand across your whole search

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
| [`01-profile-builder.md`](prompts/01-profile-builder.md) | Guided conversation that builds your job search profile |
| [`02-job-search.md`](prompts/02-job-search.md) | Generates a search prompt for the Claude Chrome extension (LinkedIn, Indeed UK, Totaljobs, and custom boards) |

### Templates

| File | What it does |
|---|---|
| [`claude-project-instructions.md`](templates/claude-project-instructions.md) | Project instructions with role assessment, CV tailoring, cover letter writing, and application tracking built in |
| [`example-profile.md`](templates/example-profile.md) | Anonymised example of a completed profile |
| [`applications-tracker.md`](templates/applications-tracker.md) | Application tracking file (Claude Code only) |
| [`memory-setup.md`](templates/memory-setup.md) | Guide to how AI memory works for your job search |

### Examples

| File | What it does |
|---|---|
| [`uk-job-boards.md`](examples/uk-job-boards.md) | UK job boards and company review sites |

## How it works

1. **Set up your project.** Create a Claude project (browser/desktop) or Claude Code folder. Paste in the project instructions. Upload your CV.
2. **Build your profile.** Run the profile builder prompt. It asks you about your experience, what you're looking for, your dealbreakers, and how you like to communicate. This becomes your `my-profile.md`.
3. **Set up your communication preferences.** Ask Claude to walk you through a few questions about tone, language, and writing style. These get saved into your project instructions.
4. **Generate your search prompts.** Run the job search prompt generator for each job board you use. It creates self-contained prompts you can schedule in the Claude Chrome extension to run daily.
5. **Review your results.** Each morning, check the search summaries. When you find a role you're interested in, paste the listing into your project and Claude will assess it against your profile.
6. **Apply.** If you decide to go for it, Claude offers to tailor your CV, then draft a cover letter, then log the application. You choose which steps you want help with.

## Built for Claude

This was built for Claude and tested with Claude.ai, Claude Desktop, the Chrome extension, and Claude Code. The prompts could probably be adapted for other AI tools that support web browsing and file uploads, though some features (projects, memory, scheduled tasks) are Claude-specific.

## Contributing

Contributions are welcome, especially regional guides for job boards outside the UK. See [CONTRIBUTING.md](CONTRIBUTING.md).

## Privacy

Your data is processed by whichever AI service you use. Review their privacy policy. For Claude: [Anthropic's privacy policy](https://www.anthropic.com/privacy). You can omit sensitive information and the toolkit still works. Nothing in this toolkit sends your data anywhere beyond the AI service you're already using.

## Trademark disclaimer

This toolkit references personality assessment frameworks (Myers-Briggs, 16 Personalities, Enneagram, DISC, CliftonStrengths, Big Five). It is not affiliated with or endorsed by The Myers-Briggs Company, Gallup, NERIS Analytics, or any assessment provider. All trademarks belong to their respective owners.

## Licence

MIT. See [LICENSE](LICENSE).

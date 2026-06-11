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
- **Help you tailor your CV and cover letters** if you want it to, with rules against fabrication, inflation, and AI-sounding language. The CV tailoring also runs an applicant tracking system (ATS) keyword check (target 85% match) and a six-second recruiter check before finalising
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
| [`applications-tracker.md`](templates/applications-tracker.md) | Application tracking file (Claude Code only) |
| [`memory-setup.md`](templates/memory-setup.md) | Guide to how AI memory works for your job search |

### Examples

| File | What it does |
|---|---|
| [`example-profile.md`](examples/example-profile.md) | Anonymised example of a completed profile |
| [`uk-job-boards.md`](examples/uk-job-boards.md) | UK job boards and company review sites |

## How it works

1. **Set up your project.** Create a Claude project (browser/desktop) or Claude Code folder. Paste in the project instructions. Upload your CV.
2. **Build your profile.** Run the profile builder prompt. It asks you about your experience, what you're looking for, your dealbreakers, and how you like to communicate. This becomes your `my-profile.md`.
3. **Set up your communication preferences.** Ask Claude to walk you through a few questions about tone, language, and writing style. These get saved into your project instructions.
4. **Generate your search prompts.** Run the job search prompt generator for each job board you use. It creates self-contained prompts you can schedule in the Claude Chrome extension to run daily.
5. **Review your results.** Each morning, check the search summaries. When you find a role you're interested in, paste the listing into your project and Claude will assess it against your profile.
6. **Apply.** If you decide to go for it, Claude offers to tailor your CV, then draft a cover letter, then log the application. You choose which steps you want help with.

## Decisions and tradeoffs

None of these felt like hard decisions at the time. They're the kind of decisions I make as a person, but they're worth explaining because they shaped how the toolkit works.

- **Two tiers of dealbreakers, because near-misses can still get you hired.** Hard dealbreakers filter roles out automatically. Strong preferences don't: a role that misses one gets flagged as "worth a closer look" instead of vanishing. Some roles don't map directly to your requirements but could still be interesting, and I didn't want the system quietly excluding them before I'd seen them.

- **Recruiter postings are flagged, never filtered.** I'd been ghosted by several recruiters during my own search, so I wanted to know who was behind a listing. But the flag is information, not a judgement: good recruiters know the hiring manager and can advocate for you internally, and I didn't want my frustration encoded into the screening.

- **The no-fabrication rules are hard rules, because they're mine.** I'm massively uncomfortable with not telling the truth, sometimes to my own detriment, and I hate it when things get made up. So the CV tailor and cover letter writer are built to never invent, never inflate scope, and never parrot the listing's language back. I'll be honest, though: rules like these make the AI try as hard as possible, but they can't guarantee it. You still have to read the output yourself and check it hasn't decided to make up something it thinks you said. If a hiring manager met you in person, they should recognise the person from the application.

- **Prompts and markdown, not an app.** Onboarding with AI can be a bit intimidating, and I just wanted to help people, wherever they already felt comfortable: Claude in the browser, the desktop app, or Claude Code. Plain markdown works everywhere and anyone can edit it.

- **Personality assessments are bring-your-own.** My own results do genuinely help with judgement calls sometimes, so they're supported. But I don't own the copyright to any of those frameworks, so the toolkit never administers a test. If you've got results, they add another helpful layer; if you haven't, nothing stops you using everything else.

## What I learned

- **The biggest win wasn't the time saved, it was the reduction in stress and anxiety.** Job searching is a long process: finding the roles, putting together the right CV and cover letter for each one, going through the application, tracking where everything stands. The hardest part is spending half a day on an application and not even getting a response, so reducing the cost of each application matters as much as the quality. Making all of that quick and easy reduced the anxiety of the whole thing, not just the hours. I use this every day, seven days a week.

- **It covers far more ground than I could manually.** Eight or nine job boards get searched every morning before 9:00. By the time I come down with my coffee, I can take the outputs, run them through Claude Code, and make quick decisions about what I want to do with them.

- **The system improves because we review it.** We do retros on how the search is going and tweak anything that could work better. The job market is really tough right now, especially at the level I'm looking at, so anything that makes it easier is a positive thing.

I just hope that anyone who picks this up experiences a little bit of positivity in what can be a soul-sucking process.

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

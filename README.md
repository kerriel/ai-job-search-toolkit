# AI Job Search Toolkit

Free prompts and guides for running an organised, honest job search with an AI assistant. New? Try the [getting started guide](getting-started.md).

## What it does

It can:

- **Get to know you properly**: a guided conversation that goes beyond your CV, covering your dealbreakers, what you want next, how you work and how you like to write.
- **Search job boards for you**, with one search prompt per job board, and screen everything it finds against your profile, so you only read the roles worth reading.
- **Give you an honest read on whether a role fits**: paste in a job ad and get the gaps, the dealbreakers and a straight recommendation. It can only judge from what you've told it, your CV and your profile, so the more complete and accurate those are, the better its read.
- **Check what it's like to work there** by reading company reviews and flagging warning signs before you apply.
- **Help with your CV and cover letter** if you want it to, in your own words and with rules against inventing or inflating experience. It also checks your CV against the job ad's keywords, because many employers use software called an applicant tracking system to sort CVs that way. Then it gives your CV the six-second skim a busy recruiter does.
- **Keep track of your applications**, so you always know where things stand.
- **Prepare you for interviews** and talk each one through afterwards. Once you've had three, it shows you what keeps coming up.

## Choose how far to go

Each level builds on the one before. Stop wherever it's enough.

### 1. Any AI assistant

The [getting started guide](getting-started.md) walks you through each step.

1. **Create a project** in your AI assistant and paste in the [project instructions](templates/project-instructions.md).
2. **Build your profile** with the [profile builder](prompts/01-profile-builder.md).
3. **Generate a search prompt** for each job board you use with the [job search prompt](prompts/02-job-search.md).
4. **Copy each search prompt into your AI tool and run it.**

Your profile, the fit check, CV and cover letter help, and the tracker work in any capable assistant that can read your files.

**Built and tested with Claude.** I built this with Claude, so the search prompts were first written for Claude. The job search prompt can also make one for any other assistant that can access the web, which you then run yourself.

If you'd like to take it a step or two further and automate more of the flow, the levels below extend it.

### 2. Searches that run every morning: Claude Cowork

1. **Make a Cowork search prompt** for each job board. In your project, ask for it by name, for example "Make me a Cowork search prompt for LinkedIn", so it's ready to run with nobody watching.
2. **Save it in your job-search folder.**
3. **Create a scheduled task** in Cowork for that board, connected to your job-search folder.
4. **Run the task once by hand**, allowing it to use your folder and signing in to the job board, and check that a results file appears.
5. **Repeat for each board**, spacing the tasks out.

Each job board is then searched overnight, with the results waiting in a folder in the morning. This part is Claude-only and needs the Claude desktop app. [Your daily searches](daily-searches.md) walks you through each step, with the Chrome extension for any board Cowork can't do.

### 3. Going further: Claude Code

1. **A morning triage** that sorts and scores the overnight results for you.
2. **Overnight hand-off**, so the triage starts by itself once the night's searches have finished.
3. **A deeper gap analysis** of the roles you decide to pursue.
4. **A gap retro** that looks for gaps that keep coming up.
5. **A self-checking loop** that helps the setup learn from its mistakes.

These are a description, not a download: [Going further](going-further.md) explains how each one works and what you'd need to build it. They're for people comfortable with Claude Code, the command-line version of Claude. The loop costs extra: every check makes Claude do another full piece of work, so it uses up your plan's limits or adds to your bill.

## How a normal day looks

1. **Your searches run**, one prompt per job board, in your AI assistant, in the Chrome extension or overnight in Cowork. Each one gives you an output of every job it looked at on that board: the roles that passed your screening in full, and the ones it skipped with the reason. If they run on a schedule, set them for the early hours, such as 2 or 3am, so they've finished before you start work.
2. **Your results get checked against your profile.** How you start depends on your setup:
   - **Any AI assistant:** one prompt runs the search and gives you its recommendations in the same conversation.
   - **Cowork or the Chrome extension:** open each board's results, copy everything and paste it into a conversation in your project.
   - **Claude Code with an overnight triage** (see [Going further](going-further.md)): the triage has already checked every board's results before you sit down, so you start from its report.

   Either way, it runs a fit check on every role against your profile, leaves out anything you've already applied for or turned down, and shows you the ones it thinks you should apply for, based on the information you've given it.
3. **You decide which to apply for.** Claude then tailors your CV and helps you draft a cover letter. You choose which help you want.
4. **Claude logs the application**, and any outcome you tell it about, so follow-ups don't get lost.

## Why I built this

After a couple of months of job searching, I was spending days scrolling through different job sites, losing track of what I'd already seen, and forgetting which roles I'd applied for. I knew there had to be a better way.

I've been working with Claude for a while, so I asked whether there was a way to automate the search part using the Claude Chrome extension. Turns out there was. I started with a simple prompt, and it grew from there into a full job search system: a project in Claude that knows who I am, what I'm looking for, and what to skip. It builds prompts that search job boards for me on a schedule, screens everything against my profile, and gives me a shortlist each morning. When I find something worth applying for, it can help me tighten up my CV and draft a cover letter in my own voice.

It's saved me days of time. Not just on searching, but on tracking what I've already reviewed, what I've applied for, and where things stand.

I know there are people who say you shouldn't use AI for this stuff. That's fair. But the rules I've built into this are all about keeping things honest: no fabricating experience, no inflating what I've done, no parroting the job listing's language back at them. Everything stays in my tone and my words. If a hiring manager met me in person, they'd recognise the person from the application.

This might not be perfect. It works for me, but your search will be different. You're welcome to download it, edit it, and make it your own. If something's not clear or could use better instructions, let me know and I'll try to update it. I just wanted to put it out there in case it helps someone else have a less painful job search.

## Decisions and trade-offs

These choices shaped how the toolkit works.

- **Two tiers of dealbreakers, because near-misses can still get you hired.** Hard dealbreakers filter roles out automatically. Strong preferences don't: a role that misses one gets flagged as "worth a closer look" instead of vanishing. Some roles don't map directly to your requirements but could still be interesting, and I didn't want the system quietly excluding them before I'd seen them.

- **Recruiter postings are flagged, never filtered.** I'd been ghosted by several recruiters during my own search, so I wanted to know who was behind a listing. But the flag is information, not a judgement: good recruiters know the hiring manager and can advocate for you internally, and I didn't want my frustration encoded into the screening.

- **The no-fabrication rules are hard rules, because they're mine.** I hate it when things get made up. So the CV tailor and cover letter writer are built to never invent, never inflate scope, and never parrot the listing's language back. I'll be honest, though: rules like these make the AI try as hard as possible, but they can't guarantee it. You still have to read the output yourself and check it hasn't decided to make up something it thinks you said. If a hiring manager met you in person, they should recognise the person from the application.

- **Plain text files, not an app.** Getting started with AI can feel a bit intimidating, and I just wanted to help people, wherever they already felt comfortable: Claude in the browser, the desktop app, Claude Code or another AI assistant. Plain text files (in a format called Markdown) work in any AI assistant, not just Claude, and anyone can edit them.

- **Personality assessments are bring-your-own.** My own results do genuinely help with judgement calls sometimes, so they're supported. But I don't own the copyright to any of those frameworks, so the toolkit never administers a test. If you've got results, they add another helpful layer; if you haven't, nothing stops you using everything else. In my own setup they also help it push back on me. I won't go for a role I don't think I can do, so when I turn down a strong match and nothing in the gap analysis explains why, it challenges me on it.

## What I learned

- **The biggest win wasn't the time saved, it was the reduction in stress and anxiety.** Job searching is a long process: finding the roles, putting together the right CV and cover letter for each one, going through the application, tracking where everything stands. The hardest part is spending half a day on an application and not even getting a response, so reducing the cost of each application matters as much as the quality. Making all of that quick and easy reduced the anxiety of the whole thing, not just the hours. I use this every day, seven days a week.

- **It covers far more ground than I could manually.** Eight or nine job boards get searched every morning before 9:00. By the time I come down with my coffee, I can take the outputs, run them through Claude Code, and make quick decisions about what I want to do with them.

- **The system improves because we review it.** I do retros on how the search is going and tweak anything that could work better. The job market is really tough right now, especially at the level I'm looking at, so anything that makes it easier is a positive thing.

I just hope that anyone who picks this up experiences a little bit of positivity in what can be a soul-sucking process.

## What's in the toolkit

### How the files fit together

> [!CAUTION]
> The toolkit and your own job search live in **two separate folders**. The toolkit is public; your job search folder holds your CV and profile, so keep it private. Never put your CV, profile or applications into the toolkit folder.

```
ai-job-search-toolkit/          The toolkit (this GitHub project): copy from it, don't add your files to it
├── README.md                   Start here
├── getting-started.md          Start here: pick your route
├── setup-any-ai-assistant.md   Setup and daily searches in any AI assistant
├── setup-claude-app.md         Part 1 in the Claude app
├── setup-claude-code.md        Part 1 in Claude Code
├── daily-searches.md           Part 2: daily searches with Cowork or Chrome
├── going-further.md            Triage, gap analysis and a self-checking loop
├── prompts/
│   ├── 01-profile-builder.md   Builds your profile
│   ├── 02-job-search.md        Writes a search prompt for each job board
│   └── 03-interviews.md        Interview prep, debriefs and patterns
├── templates/
│   ├── project-instructions.md Your project's instructions
│   ├── applications-tracker.md The format for your tracker
│   └── memory-setup.md         How memory works
└── examples/
    ├── example-profile.md      A completed profile
    └── uk-job-boards.md        UK job boards and review sites

job-search/                     Your own folder (private)
├── CLAUDE.md                   The project instructions (Claude Code)
├── my-cv.pdf                   Your CV
├── my-profile.md               Your profile, built by the profile builder
├── applications.md             Your tracker, created on your first application
├── prompts/                    Copied from the toolkit
├── templates/                  Copied from the toolkit
├── search-prompts/             One search prompt per job board (Cowork)
└── results/                    Each morning's search results (Cowork)
```

If you use the Claude app rather than Claude Code, your own files live in your Claude project instead of a folder. The instructions go in the project's instructions, and your CV, profile and the three prompt files go in its project knowledge.

## Contributing

Contributions are welcome, especially regional guides for job boards outside the UK. See [CONTRIBUTING.md](CONTRIBUTING.md).

## Privacy

> [!CAUTION]
> Whichever AI service you use processes your data, so read its privacy policy. For Claude: [Anthropic's privacy policy](https://www.anthropic.com/legal/privacy). You can leave out sensitive information and the toolkit still works. Nothing in this toolkit sends your data anywhere beyond the AI service you're already using.

## Trademark disclaimer

This toolkit references personality assessment frameworks (Myers-Briggs, 16 Personalities, Enneagram, DISC, CliftonStrengths, Big Five). It is not affiliated with or endorsed by The Myers-Briggs Company, Gallup, NERIS Analytics, or any assessment provider. All trademarks belong to their respective owners. Claude, Claude Code and Cowork are trademarks of Anthropic, and LinkedIn, Indeed and Glassdoor are trademarks of their owners. This toolkit is independent and not endorsed by any of them.

## Licence

Licensed under CC BY-NC-SA 4.0, which means you can copy and change it for non-commercial use, as long as you credit it and share your version under the same licence. See [LICENSE](LICENSE).

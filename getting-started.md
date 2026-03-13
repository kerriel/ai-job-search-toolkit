# Getting Started

A complete walkthrough for setting up your AI-powered job search. No prior experience with AI tools required.

## Try it in 5 minutes

Before committing to the full setup, try the toolkit with a single job listing to see what it does:

1. Open Claude at [claude.ai](https://claude.ai) (or any AI chat tool)
2. Find a job listing you're interested in
3. Paste the listing into the chat and ask: "I'm considering applying for this role. Can you assess whether it's a good fit based on my CV?" and attach your CV
4. See how the AI breaks down the role, identifies gaps, and gives you a recommendation

That's the core idea. The full toolkit automates and systematises this across multiple job boards, with a rich profile that goes beyond your CV. When you're ready to set up the full system, choose your path below.

## A note on privacy

Before you start sharing personal information, it's worth knowing how your data is handled:

- Your data is processed by whichever AI service you use (Claude, ChatGPT, etc.). Review their privacy policy to understand how your data is handled and retained
- For Claude: see [Anthropic's privacy policy](https://www.anthropic.com/privacy)
- You can omit sensitive information (salary details, personality results, etc.) and the toolkit still works, just with less personalisation
- Nothing in this toolkit sends your data anywhere beyond the AI service you're already using

## Choose your path

There are two ways to set up the toolkit. **Path A is recommended for most people**, especially if you're new to AI tools.

---

## Path A: Claude in the browser or desktop app (recommended)

### 1. Create a Claude account

Go to [claude.ai](https://claude.ai) and sign up. The free tier works for trying things out. A paid plan gives you more conversations and access to better models.

### 2. Create a project

A project is a dedicated space where Claude remembers your context across conversations. Everything about your job search lives here.

**To create one:**
- Click **+ New Project** (or navigate to Projects in the sidebar)
- **Name it** clearly and specifically. Good names: "Job Search 2026", "Graduate Developer Hunt", "Head of Product Search". Bad names: "My Project", "Stuff", "Test".
- **Write a description** of what you're trying to achieve. For example: "Systematic job search targeting marketing roles in London, remote-first companies" or "Graduate software developer roles in Manchester, 2026".

### 3. Set up project instructions

Project instructions are rules that tell Claude how to behave in every conversation within this project. Think of them as a briefing document that Claude reads before every conversation.

**To set them up:**
1. Open your project
2. Find the project settings or custom instructions area
3. Copy the template from [`templates/claude-project-instructions.md`](templates/claude-project-instructions.md) in this repo
4. Paste it into the custom instructions field
5. After running the profile builder (step 6), you'll come back and add your communication preferences here

**Important:** Project instructions are different from your knowledge base files. Instructions are rules that govern behaviour. Knowledge base files are reference materials Claude reads when it needs facts.

### 4. Add to the knowledge base

The knowledge base is where you put files Claude can reference whenever it needs facts about you.

**To add files:**
- In your project, find the knowledge base or files section
- Upload your CV (drag and drop or use the upload button)
- After running the profile builder (step 6), you'll add your `my-profile.md` here too

### 5. Understand memory

Claude remembers things from your conversations within a project. This happens automatically. The more you use your job search project, the better Claude understands your situation.

Memory is different from your knowledge base. Your CV and profile are reference materials you upload. Memory is context Claude picks up along the way: which companies you've applied to, how your preferences are evolving, what interview feedback you've received.

See [`templates/memory-setup.md`](templates/memory-setup.md) for more detail on how memory works.

### How the three layers work together

Your project now has three layers working together:

| Layer | What it does | What goes here |
|---|---|---|
| **Instructions** | Tell Claude how to behave | The rules you just set up: never guess, track applications, maintain your profile |
| **Files** | Tell Claude who you are | Your CV, your profile (once generated) |
| **Memory** | What Claude learns over time | Application outcomes, evolving preferences, interview feedback |

Instructions are the boss. Files are the reference library. Memory is the notebook. Instructions explicitly reference the other two.

### 6. Run the profile builder

This is where you build your job search profile through a guided conversation.

1. Start a **new conversation** within your project
2. Paste the entire profile builder prompt from [`prompts/01-profile-builder.md`](prompts/01-profile-builder.md)
3. If you have a CV, upload it at the same time (drag and drop works)
4. Answer the questions one at a time. The conversation takes 10-15 minutes
5. At the end, Claude generates your `my-profile.md`
6. **Save it to your project knowledge base** (download the file, then upload it to your project's files)
7. **Copy the communication preferences** that Claude outputs separately, and paste them into your project instructions (replacing the placeholder section)

You're now set up. Every prompt in this toolkit will reference your profile automatically.

---

## Path B: Claude Code (for developers and terminal users)

Best for people who already use the command line. Gives you a persistent file-based project with version history and memory across sessions.

### 1. Install Claude Code

Follow the installation instructions at [Claude Code documentation](https://docs.anthropic.com/en/docs/claude-code).

### 2. Create a project folder

A project folder is a directory on your computer where all your job search files live. Claude Code reads files from this folder and saves new files here.

```bash
mkdir -p ~/job-search
cd ~/job-search
```

You can put it wherever makes sense for you. `~/job-search` or `~/Documents/job-search` both work.

### 3. Save your CV

Copy or save your CV into the project folder. Claude Code reads files from this directory automatically.

```bash
cp ~/Downloads/my-cv.pdf ~/job-search/
```

### 4. Initialise the project

```bash
git init
```

This sets up version tracking so you can see the history of changes to your CV, profile, and application materials.

Copy the project instructions template into your project as `CLAUDE.md`:

```bash
# Download or copy templates/claude-project-instructions.md from this repo
# and save it as CLAUDE.md in your project folder
cp path/to/claude-project-instructions.md ~/job-search/CLAUDE.md
```

Claude Code reads `CLAUDE.md` automatically as project instructions.

### 5. Run the profile builder

Start Claude Code in your project folder:

```bash
cd ~/job-search
claude
```

Paste the profile builder prompt from [`prompts/01-profile-builder.md`](prompts/01-profile-builder.md). Claude reads your CV from the folder automatically. Answer the questions, and it generates `my-profile.md` in your project folder.

After the profile is generated, copy the communication preferences output into your `CLAUDE.md` file.

---

## Set up the Chrome extension (for automated daily searches)

This applies to both Path A and Path B. The Chrome extension lets you schedule daily job board searches that run automatically.

*These instructions reflect the Chrome extension UI as of March 2026 and may change with updates.*

### 1. Install the extension

Install the Claude Chrome extension from the Chrome Web Store.

### 2. Pin it to your toolbar

Click the **jigsaw puzzle icon** (Extensions) in the Chrome toolbar. Find the Claude extension in the list and click the **pin icon** next to it. This keeps it visible and easy to access. You can also right-click the extension icon and select "Pin" from the menu.

### 3. Log into your job boards

Before setting up automated searches, log into your job boards (LinkedIn, Indeed, Totaljobs, etc.) and company review sites (Glassdoor, etc.) in Chrome. The extension needs access to these sites when it runs.

### 4. Create a scheduled search

1. Open the Chrome extension by clicking its icon in the toolbar
2. Type `/` in the chat box at the bottom
3. Select **"Schedule a task"**
4. In the **"Create shortcut"** box, fill in:
   - **Name:** A clear name for the search (e.g. "LinkedIn Job Search", "Indeed UK Search")
   - **Prompt:** Paste the search prompt from this repo (e.g. the contents of `prompts/02-job-search-linkedin.md`)
   - **URL:** The starting page for the job board (e.g. linkedin.com/notifications for LinkedIn, uk.indeed.com for Indeed UK)
   - **Schedule:** Toggle on. Select frequency (Daily is recommended for active searching). Set your preferred time (mornings work well, before you start your day)
   - **Model:** Use the most capable model available. At time of writing, Sonnet 4.6 or newer works well for the search and review workflow
5. Hit **"Create shortcut"** to save

### 5. Use it

Your prompt is now available by typing `/` followed by the name you gave it, then pressing return.

### 6. Automated runs

Because you enabled the schedule, the prompt runs automatically at the time you set, as long as Chrome is open. You'll see the results next time you open the extension.

### 7. Repeat for each job board

Set up a separate scheduled search for each job board you want to monitor. Each one runs independently.

---

## Daily workflow

Once everything is set up, here's your daily routine:

1. **First pass (automated):** Your search prompts run automatically each morning (or whenever you scheduled them)

2. **Review the output:** Open the Chrome extension and read the results. The decisions log shows every role that was checked and why it was included or filtered out

3. **Second pass (you + your project):** Copy the suitable roles summary into your Claude project (browser/desktop) or Claude Code session. Your project has your full profile, CV, memory, and application history, giving it much richer context than the Chrome extension

4. **Confirm suitability:** Ask Claude to review each role against your full profile. **Read the full job listing yourself** for any role you're considering. Don't apply based on the summary alone

5. **Assess fit:** For confirmed roles, use the application assessor (`prompts/03-application-assessor.md`) for a detailed fit assessment

6. **Apply:** For roles you want to pursue, use the CV tailor (`prompts/04-cv-tailor.md`) and cover letter writer (`prompts/05-cover-letter-writer.md`). Review the output as if you were the hiring manager before submitting

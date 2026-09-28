# Part 2 of 2: Your Daily Searches

> [!NOTE]
> This page is for Claude users who have finished Part 1, [in the Claude app](setup-claude-app.md) or [in Claude Code](setup-claude-code.md).
>
> Using another AI assistant? The [setup page for any AI assistant](setup-any-ai-assistant.md#your-daily-searches) covers your daily searches.

You use one search prompt per job board. Each one runs on a schedule and gives you a list of every job it looked at: the ones that passed your screening in full, and the ones it skipped with the reason. **Cowork, part of the Claude desktop app, is the recommended way to run them.** For any board Cowork can't search, use Claude's extension for the Chrome web browser.

> [!WARNING]
> **Check each site's terms before you automate it.** Some job boards and review sites, LinkedIn among them, restrict automated access, and it's your account that's at risk. Search at a normal pace and stop if a site objects.

## How it fits together

There are two pieces:

1. **A prompt file in your folder**, one per job board, for example `job-search/search-prompts/linkedin.md`. This holds the whole search: your profile, your dealbreakers and the steps for that board.
2. **A scheduled Cowork task** holding a short instruction that tells Claude to read that file and follow it.

Keeping the real prompt in a file, rather than pasted into the task, means you can improve your search by editing one file. The next morning's run picks up the change, and there are no old copies hiding in task settings.

> [!CAUTION]
> **Your search prompt files contain your profile and dealbreakers.** Keep your `job-search` folder private on your own computer, and don't put it in a shared folder or a public repository.

## Cowork (recommended)

Cowork is part of the Claude desktop app. It runs each search as a scheduled task while you're away and saves the results to a folder on your computer, ready for the morning. Check [which Claude plans include Cowork](https://support.claude.com/en/articles/13345190-get-started-with-cowork) before you start.

1. **Install the Claude desktop app and sign in.**
2. **Make a folder for your job search.** Create a folder called `job-search` (in Documents is fine), with two empty folders inside it: `search-prompts` and `results`. If you set up with Claude Code, you already have `job-search`, so just add the two folders.
3. **Make a Cowork search prompt for your first job board.** Start a conversation in your project, copy this prompt, paste it in and put your board's name in place of LinkedIn. This uses `02-job-search.md`, the job search prompt you added during setup.
   ```
   Make me a Cowork search prompt for LinkedIn.
   ```
   Every job board works differently (its filters, whether you need to sign in, how it lists jobs), so each board gets its own prompt. It asks you a few questions about how you search that board, then uses your profile to write a prompt that's ready to run with nobody watching. Save it as a plain-text file in `search-prompts`, named after the board, for example `linkedin.md`. In Claude Code, just ask Claude to save it there.
4. **Create a scheduled task in Cowork.**
   1. In the Claude desktop app, open Cowork and click into your `job-search` folder in the right-hand column. This is the step that connects the task to that folder.
   2. Go to **Scheduled**.
   3. Click the **+** button.
   4. Name the task after the board, for example "LinkedIn search".
   5. Paste in the instruction below, with your board's name typed in where it says `linkedin`:
      ```
      Read the file search-prompts/linkedin.md in the connected job-search folder and follow it exactly as written; it is the complete instruction for this run. When you finish, save everything you would have shown me as a file in results/, named with today's date and the board, for example 2026-09-30-linkedin.md. Use the built-in Cowork browser. If you cannot read that file, write a file to results/ named with today's date and the board, first line 'RUN FAILED - could not read prompt file', and stop. Never run git or any other command.
      ```
      Type the board name in each time. Don't leave a placeholder like `<board>` for later: in my setup, the task editor swallowed text in angle brackets and cut the instruction short.
   6. Set how often it runs, and give it permission to read and write in your `job-search` folder.
   7. Turn on **Require this computer**, so the task runs on your computer, where your folder is.
5. **Run it once yourself, straight away.** This first run is when Cowork asks for permission to use your folder, so allow it. Sign in to the job board in Cowork's browser too, and to any review sites your prompt uses, such as Glassdoor. Then check that a results file has appeared in `results`.
6. **Repeat for each job board**, spacing the tasks about 20 minutes apart. Put the boards most likely to fail first, so there's time to notice.

> [!IMPORTANT]
> **Keep your computer awake and the Claude desktop app open** when each task is due, or the search won't run. Cowork can run some scheduled tasks remotely while your computer is asleep, but a task that uses files on your computer [only runs locally](https://support.claude.com/en/articles/13854387-schedule-recurring-tasks-in-claude-cowork), and yours uses your `job-search` folder.

> [!IMPORTANT]
> **Connect Cowork to your `job-search` folder only.** Anthropic's advice in [Use Claude Cowork safely](https://support.claude.com/en/articles/13364135-use-claude-cowork-safely) is to give Claude a dedicated working folder rather than broad access, and to keep sensitive files, such as financial documents, out of it.

### Things I learned running Cowork

- **Check the time zone of the schedule.** Mine uses UTC (Coordinated Universal Time, the same as UK winter time), so during British Summer Time it runs an hour later by the UK clock. Check which time zone yours uses.
- **A missing file means the run never started**, most often because the computer was asleep or the app was closed. A file starting "RUN FAILED" means it started and something went wrong.
- **Logins drop.** Some boards sign you out every so often. The run reports it, and you sign in again.
- **A task can switch itself off.** One of mine was turned off automatically because the computer wasn't reachable when it was due. If one board's file is missing while the others are there, check in **Scheduled** that its task is still on.
- **Keep your rules in the prompt file, not in your head.** When the search surfaces something you'd never want, add the rule to the file. It then applies from the next morning.

---

## The Chrome extension, for boards Cowork can't do

Some job boards stop a search that nobody is watching. In my experience, Indeed asks you to prove you're human before it shows anything, which a scheduled Cowork run can't do. For boards like that, use the Chrome extension, where you can tick the box yourself. It works whether you set up in the Claude app or in Claude Code, and it can run on a schedule too. It needs a paid Claude plan (Pro, Max, Team or Enterprise).

*These instructions reflect the Chrome extension as of September 2026 and may change with updates.*

### 1. Install the extension

In Chrome, go to the [Chrome Web Store](https://chromewebstore.google.com), search for **Claude**, open the extension published by Anthropic and click **Add to Chrome**. Sign in with your Claude account when it asks.

### 2. Pin it to your toolbar

Click the **jigsaw puzzle icon** (Extensions) in the Chrome toolbar. Find the Claude extension in the list and click the **pin icon** next to it. You can also right-click the extension icon and select "Pin" from the menu.

### 3. Choose which sites it can use (recommended)

The extension asks before it acts on a site. Approve only your job boards and the review sites you use, and decline anything else. Anthropic changes these settings from time to time, so follow its current steps in the [Claude in Chrome permissions guide](https://support.claude.com/en/articles/12902446-claude-in-chrome-permissions-guide) and [Use Claude in Chrome safely](https://support.claude.com/en/articles/12902428-use-claude-in-chrome-safely).

### 4. Log into your job boards

Before setting up automated searches, log into your job boards such as LinkedIn, Indeed and Totaljobs, and company review sites such as Glassdoor, in Chrome. The extension needs access to these sites when it runs.

### 5. Generate and schedule your search prompts

The Chrome extension can't access your project files, so your search prompts need your profile written into them. The job search prompt (`prompts/02-job-search.md`) does this for you.

1. **Ask for a search prompt.** Start a conversation inside your project (or open Claude Code in your job search folder) and say: **"Run the job search prompt."** It's in `prompts/02-job-search.md`, which you added during setup
2. **Answer its questions.** It asks which job board you're searching and a few details, then gives you a self-contained prompt for the Chrome extension in a grey box. Copy it with the copy icon
3. **Save it as a shortcut in the extension.** The steps are at the bottom of [`prompts/02-job-search.md`](prompts/02-job-search.md#setting-up-in-the-claude-chrome-extension). A shortcut is a saved prompt you can run again at any time
4. **Schedule it.** Click the clock icon in the top right of the extension panel and choose how often it runs, for example daily

### 6. Run it once yourself to check it works

Type `/` in the extension, choose your shortcut and press Return (Enter on Windows). Check the results look right before you trust the schedule.

### 7. Automated runs

Because you enabled the schedule, the prompt runs automatically at the time you set. When it finishes, a small window opens with the results, and you copy everything from there.

### 8. Repeat for each job board

Set up a separate scheduled search for each job board you want to monitor.

### Keep Chrome open for scheduled searches

> [!IMPORTANT]
> In my experience, scheduled searches only run while Chrome is open. If you close your browser or shut down your computer overnight, any searches scheduled during that time won't run. Either leave Chrome open, or schedule your searches for a time when your computer will be on and Chrome will be running.

---

## A normal day

Once everything's set up, here's the recommended daily routine:

1. **Check your results.** Your search prompts run automatically each morning (or whenever you scheduled them), one per job board. With the Chrome extension, a small window opens with each search's output; with Cowork, each board's results are saved in your `results/` folder. Either way, the output shows every role that was checked: the ones that passed your screening in full, and the ones it skipped with the reason.

2. **Copy the output into your project.** In the Chrome extension's window, scroll to the bottom and click the small copy icon. With Cowork, open the day's results file in `results/` with a text editor, such as TextEdit on a Mac or Notepad on Windows, then select everything and copy it. On a Mac, Control-click the file and choose **Open With** to pick TextEdit. Then open your project, start a conversation on its main page and paste it in; in Claude Code, paste it into your session. Your project has your full profile, CV, memory, and application history, so it has much richer context than the Chrome extension.

3. **Review the recommendations.** Pasting the output is enough. Your project instructions tell Claude to check every role against what it knows about you, leave out roles you've already dealt with and recommend the ones worth applying for. Each recommendation includes a link to the job listing. If a link is missing, just ask for it. It's worth reading through all the results, not just the top picks.

4. **Choose and apply.** Pick the roles you want to pursue. If you'd like, Claude will offer to help tailor your CV and draft a cover letter. Review the output as if you were the hiring manager before submitting.

5. **Track your applications.** Let Claude know when you've applied for something. It will keep track of where you've applied, the status of each application, and help you follow up on anything that's gone quiet.

> [!WARNING]
> **Keep job descriptions for your own use.** The results files contain text copied from job boards, so don't post or share them publicly.

## Where next

To have Claude also read the morning's results for you, check them against roles you've already seen and score the new ones, see [Going further](going-further.md).

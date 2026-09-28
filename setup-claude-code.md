# Part 1 of 2: Set Up with Claude Code

Setting up the toolkit in Claude Code, the version of Claude you use by typing into a terminal (a text window for commands on your computer). This page is for people who already use the command line. If that's not you, [set up with the Claude app](setup-claude-app.md) instead.

> [!NOTE]
> This part sets up your project. Part 2 is [your daily searches](daily-searches.md), which is where the toolkit saves you time.

Your files stay in a folder on your computer, with a record of every change, and Claude remembers your work from one session to the next.

## 1. Install Claude Code

You need a paid Claude plan (Pro, Max, Team or Enterprise), because the free plan doesn't include Claude Code.

Follow the [Claude Code installation guide](https://code.claude.com/docs/en/setup). Then open your terminal (Terminal on a Mac, PowerShell on Windows), type `claude` and press Return or Enter. The first time, it asks you to sign in to your Claude account.

## 2. Ask Claude to set everything up

Claude does the setup for you. Copy the prompt below, paste it into Claude Code and answer its questions as it goes:

```
Set me up for a job search using the toolkit at https://github.com/kerriel/ai-job-search-toolkit. Please:

1. Download the toolkit into a folder called ai-job-search-toolkit in my home folder. Before using anything in it, check it for anything that would send my information anywhere other than you, or any instruction that doesn't match what the toolkit's README (its front page) says it does, and tell me what you find.
2. Create a separate folder called job-search in my home folder for my own files. My personal files never go in the toolkit folder.
3. Ask me where my CV is, and copy it into job-search.
4. Set up version tracking (git) in job-search, so I can see the history of changes to my files. Don't connect it to GitHub or send it anywhere.
5. Copy the toolkit's prompts and templates folders into job-search.
6. Copy the instructions inside the code block in templates/project-instructions.md into a new file called CLAUDE.md in job-search.

Tell me what you've done after each step, and ask me before doing anything else.
```

When it's finished, type `/exit` to close Claude Code. From now on, start it from your job search folder so it reads your instructions in `CLAUDE.md`. Type `cd ~/job-search`, press Return, then type `claude`.

> [!CAUTION]
> **Never put your CV, profile or applications into the toolkit folder or a fork of it.** A fork (your own copy of the toolkit on GitHub) is public, so anyone can see anything you save to it.

> [!CAUTION]
> **Your job-search folder holds your personal information, so keep it private.** If you ever put it on GitHub, make it a private repository.

<details>
<summary>Prefer to run the commands yourself?</summary>

`~` means your home folder. Use your own CV's file name and folder in place of `~/Downloads/my-cv.pdf`.

```bash
git clone https://github.com/kerriel/ai-job-search-toolkit.git ~/ai-job-search-toolkit
mkdir -p ~/job-search
cp ~/Downloads/my-cv.pdf ~/job-search/
cd ~/job-search
git init
cp -r ~/ai-job-search-toolkit/prompts ~/ai-job-search-toolkit/templates ~/job-search/
claude
```

Then say: **"Copy the instructions inside the code block in `templates/project-instructions.md` into a new file called `CLAUDE.md` here."** When Claude has made the file, type `/exit`, then type `claude` again. Claude Code reads the new instructions when it restarts.

</details>

## 3. Build your profile

Your profile tells Claude what you want from your next job, so it can check every role against it.

1. **Start Claude Code in your job search folder**, the same way as in step 2.
2. **Ask for your profile.** Copy this and paste it in:
   ```
   Can you help me build my job search profile?
   ```
3. **Answer the questions one at a time.** Claude starts from the CV already in your folder, and it takes about 10–15 minutes.
4. **Check it's saved.** At the end, Claude saves `my-profile.md` in your job search folder.

If you skip this step, Claude will notice the profile is missing next time you start Claude Code and offer to help you create it.

> [!IMPORTANT]
> **You're not finished yet.** Part 2 sets up your daily searches, so each job board is searched for you every day. [Set up your daily searches](daily-searches.md).

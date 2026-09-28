# Part 1 of 2: Set Up with Claude in the Browser or Desktop App

Setting up the toolkit in Claude on the web or in the desktop app, step by step.

> [!NOTE]
> This part sets up your project. Part 2 is [your daily searches](daily-searches.md), which is where the toolkit saves you time.

## 1. Get the files

On the [toolkit's GitHub page](https://github.com/kerriel/ai-job-search-toolkit), click the **Code** button, then **Download ZIP**. You don't need a GitHub account. It downloads to your **Downloads** folder as `ai-job-search-toolkit-main.zip`. On a Mac, double-click it to unzip it. On Windows, right-click it, choose **Extract All** and follow the steps on screen. Either way you'll get a folder called `ai-job-search-toolkit-main`. You'll upload files from it in step 5.

## 2. Create a Claude account

Go to [claude.ai](https://claude.ai) and sign up. The free plan works for trying things out, with up to five projects. A paid plan gives you more use of Claude and more of its models.

## 3. Create a project

A project is a space in Claude that keeps your instructions and files together, so every conversation in it starts with them. Everything about your job search lives here.

**To create one**, once you're signed in:

1. **Find Projects.** Move your mouse to the left-hand edge of the screen and a menu slides out. Click **Projects**. If you can't see it, go straight to [claude.ai/projects](https://claude.ai/projects) instead.
2. **Click + New Project**, in the top right corner of the Projects page.
3. **Name it**, for example "Job Search 2026".
4. **Write a description** of what you're trying to achieve. For example: "Marketing jobs in London, at companies where most people work from home" or "Graduate software developer roles in Manchester, 2026".
5. **Create the project.** This is where you'll do everything else in this guide. To come back to it later, it's under **Projects** in that same left-hand menu.

## 4. Set up project instructions

Project instructions are rules that tell Claude how to behave in every conversation within this project. Think of them as a briefing document that Claude reads before every conversation.

**To set them up:**
1. **Open your project.** It's under **Projects** in the left-hand menu.
2. **Click Set project instructions** on your project's main page. A box opens for you to type or paste into.
3. **Copy the instructions.** Right-click [`templates/project-instructions.md`](templates/project-instructions.md) and choose **Open Link in New Tab**. In the new tab, hover over the grey box and click the copy icon in its top-right corner. That copies the instructions and nothing else. Close that tab and you're back on this page.
4. **Paste them into the box and click Save instructions.**

> [!NOTE]
> Project instructions are different from your project knowledge. Instructions are rules that govern behaviour. Project knowledge is the reference material Claude reads when it needs facts.

## 5. Add to your project knowledge

Project knowledge is where you put files Claude can reference whenever it needs facts about you.

**To add files:**
1. **Open your project.** Project knowledge is the panel on the right-hand side of your project's main page.
2. **Click the + button** in that panel and upload your CV. You can also drag the file straight onto the panel.
3. **Upload the three prompt files the same way.** They're in your Downloads folder, inside `ai-job-search-toolkit-main`, in the `prompts` folder: `01-profile-builder.md`, `02-job-search.md` and `03-interviews.md`.

You'll add your profile here too, in step 6.

## 6. Build your profile

Your profile tells Claude what you want from your next job, so it can check every role against it. You build it by answering Claude's questions.

1. **Start a conversation inside your project.** Open your project (under **Projects** in the left-hand menu) and type in the message box on its main page. A conversation started there can see your instructions and project knowledge.
2. **Ask for your profile.** Copy this and paste it in. Claude starts from the CV you've already added to your project knowledge.
   ```
   Can you help me build my job search profile?
   ```
3. **Answer the questions.** Claude will ask about your experience, what you're looking for, your dealbreakers, preferences, and how you like your CV and letters to sound. Answer them one at a time. It takes about 10–15 minutes.
4. **Copy your profile.** At the end, Claude gives you your profile in a grey box. Hover over the box and click the copy icon in its top-right corner.
5. **Save it as a file on your computer.**
   - **On a Mac:** open **TextEdit** (it's in your Applications folder). Choose **Format**, then **Make Plain Text**. Paste your profile in, then choose **File**, then **Save**. Name it `my-profile.md`, save it in your Documents folder, and if TextEdit asks whether to use .md or .txt, choose **Use .md**.
   - **On Windows:** open **Notepad**. Paste your profile in, then choose **File**, then **Save as**. Set **Save as type** to **All files**, name it `my-profile.md` and save it in your Documents folder.
6. **Add it to your project knowledge.** Open your project, click the **+** button in the project knowledge panel on the right, and upload `my-profile.md` from your Documents folder.

You're now set up. Claude will use your profile in every conversation in your project. If Claude notices your profile is missing, it will offer to help you create it.

## How Claude remembers your job search

Claude remembers things from your conversations within a project. Each project keeps its own memory, separate from your other chats. Memory is on by default on the Free, Pro and Max plans. On Team and Enterprise plans, it's off unless your admin turns it on. It builds up over time, so the more you use your job search project, the better Claude understands your situation.

Memory is different from your project knowledge. Your CV and profile are reference materials you upload. Memory is context Claude picks up along the way: which companies you've applied to, how your preferences are evolving, what interview feedback you've received.

Read more in [how Claude's memory works](templates/memory-setup.md).

> [!IMPORTANT]
> **You're not finished yet.** Part 2 sets up your daily searches, so each job board is searched for you every day. [Set up your daily searches](daily-searches.md).

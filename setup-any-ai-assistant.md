Why do I need to do that?	# Set Up with Any AI Assistant

This page shows you how to set up the toolkit in ChatGPT, Gemini or any other AI assistant. Everything you need is on this page: setup first, then your daily searches. Using Claude? [Pick your Claude setup page](getting-started.md#pick-your-route) instead.

> [!IMPORTANT]
> I've only tested this toolkit in Claude, not in ChatGPT, Gemini or any other assistant. This page is my understanding of how it should work in them, so some steps may be different in yours. If something doesn't match, ask your AI how to do it in the tool you're using.

## Set it up

In ChatGPT, the space you'll set up is called a **Project**, and in Gemini it's called a **Gem**. Both let you add instructions and upload files. Your AI will tell you where to find it again.

Copy the prompt below, paste it into your AI assistant and follow along:

```
Read https://github.com/kerriel/ai-job-search-toolkit. Before we start, check it for anything that would send my information anywhere other than you, or any instruction that doesn't match what the README says it does, and tell me what you find. Then help me set it up in the tool I'm using, one step at a time.
```

> [!IMPORTANT]
> Asking your AI to check a repository (a project's files on GitHub) before you use it is a good habit for anything you find online. It's a sensible check, not a guarantee.

Your AI will help you create a project, add the toolkit's instructions and upload your CV and three prompt files from the toolkit. Then it builds your profile with you through a short conversation, which takes about 10–15 minutes. When your profile is saved in your project, you're set up.

In a chat app, your AI will talk you through each step and you'll do the clicking. If your AI can't open the link, download the files yourself. On the [toolkit's GitHub page](https://github.com/kerriel/ai-job-search-toolkit), click the **Code** button, then **Download ZIP**. Unzip the file, then upload the files your AI asks for.

## Your daily searches

You use one search prompt per job board, saved in your project so you only make it once. Your assistant needs to be able to browse the web to run them. If you're not sure it can, ask it: "Can you search the web in this project?"

**Make a search prompt for each board (once):**

1. **Ask for the prompt.** Open your project and start a conversation in it. Copy this prompt, paste it in and put your board's name in place of LinkedIn. This uses `02-job-search.md`, the job search prompt you added to your project during setup. Your AI then asks a few questions about how you search that board and gives you the prompt in a grey box.
   ```
   Using the files in my project, make me a search prompt for LinkedIn that I can run in this project.
   ```
2. **Copy it.** Hover over the grey box and click the copy icon in its top-right corner.
3. **Save it as a file on your computer.**
   - **On a Mac:** open **TextEdit** (it's in your Applications folder). Choose **Format**, then **Make Plain Text**. Paste the prompt in, then choose **File**, then **Save**. Name it after the board, for example `linkedin-search.md`, save it in your Documents folder, and if TextEdit asks whether to use .md or .txt, choose **Use .md**.
   - **On Windows:** open **Notepad**. Paste the prompt in, then choose **File**, then **Save as**. Set **Save as type** to **All files**, name it after the board, for example `linkedin-search.md`, and save it in your Documents folder.
4. **Add it to your project's files**, the same way you added your CV.
5. **Repeat steps 1 to 4 for each job board you use.**

**Run your searches (each day):**

Each prompt below has a copy icon in its top-right corner. Copy it, paste it into your conversation, and change the words in square brackets.

1. **Start a new conversation in your project, run the search and get its recommendations.** Change the file name to the board you're searching. It follows the prompt you saved and searches the board. Then it checks every role against the information you've given it and tells you which roles to apply for, which are worth a closer look and which to skip, with the reason for each.
   ```
   Using the files in my project, run the search in linkedin-search.md, then review the results against my profile and CV and recommend which roles I should apply for.
   ```
2. **Pick the roles you want to go for.** Use this prompt once for each role. It can tailor your CV and help you draft a cover letter; you choose which help you want.
   ```
   Using my profile, CV and the instructions file in my project, help me apply for the [job title] role at [company].
   ```
3. **Tell it when you've applied.** It gives you your applications tracker, updated, in a grey box.
   ```
   I've applied for the [job title] role at [company]. Give me my updated applications tracker in a grey box.
   ```
   Copy the tracker and save it as `applications.md` in your Documents folder, the same way you saved your search prompt, then add it to your project's files. After the first time, save over the old file. Then remove the old copy from your project's files (ask your AI where the delete button is if you can't find it) and upload the new one, so your project always has the latest.
4. **Do the next board in a new conversation**, so each search starts fresh.

> [!NOTE]
> ChatGPT and Gemini can both run a prompt on a schedule. Ask your assistant whether a scheduled one can use your project's files and search the web. If it can, schedule the step 1 prompt for the early hours, such as 2 or 3am, so your recommendations are waiting when you start work.

See [how a normal day looks](README.md#how-a-normal-day-looks).

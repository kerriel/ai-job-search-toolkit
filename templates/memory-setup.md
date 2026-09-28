# How Claude remembers your job search

This page is for you if you use Claude in your browser or the desktop app. There's nothing to set up: memory works on its own once your project exists. If you use Claude Code, you can skip this page. Claude Code keeps what it learns in the files in your project folder, so when something changes, tell it and ask it to update your profile. Other AI assistants handle memory in their own way, so ask yours: "How does your memory work in this project?"

## What is memory?

When you use Claude within a project, it remembers things across conversations. You don't need to repeat yourself every time you start a new chat. Each project has its own memory, kept separate from your other projects and chats.

> [!NOTE]
> Memory is on by default on the Free, Pro and Max plans. On a Team or Enterprise plan it stays off unless your admin turns it on. To check or change yours, see [Anthropic's guide to memory](https://support.claude.com/en/articles/11817273-use-claude-s-chat-search-and-memory-to-build-on-previous-context).

Memory is different from the files in your project knowledge, such as your CV and profile. Files are reference materials you upload. Memory is what Claude picks up along the way from your conversations.

## What Claude remembers

With memory on and the [project instructions](project-instructions.md) in your project, Claude saves things like:

- **Application outcomes:** which companies you applied to, whether you got an interview, and what happened
- **Evolving preferences:** if you start caring more about remote work or less about salary, Claude notices
- **Interview feedback:** what went well, what didn't, patterns across interviews
- **Company notes:** things you've learned about specific companies from research, conversations, or interviews
- **Rejected roles and reasons:** so Claude recognises them if they come up again

## How to check what Claude remembers

Open your project, start a new conversation on its main page and ask one of these:
- "What do you remember about my job search?"
- "Which companies have I applied to?"
- "What feedback have I had from interviews?"

Claude will tell you what it knows.

## How to correct or update memories

If Claude remembers something wrong, or your situation has changed, tell it, for example:
- "I've changed my mind about remote work. I'm now open to hybrid roles."
- "That's not right. I applied to Acme on Tuesday, not Wednesday."
- "I no longer care about the 4-day week requirement. Remove that as a dealbreaker."

Claude will update what it knows. To check, ask: `What do you remember about my remote work preferences?`

If you've changed a preference or a dealbreaker, also ask: `Give me my updated profile in a grey box.` Copy it, save it over `my-profile.md` in your Documents folder, remove the old copy from your project knowledge and upload the new one, the same way you did in [setting up your project](../setup-claude-app.md).

Memory doesn't change your daily searches, because each search prompt was made from your profile as it was then. After you've updated your profile, make a new search prompt for each board and save it over the old one. [Your daily searches](../daily-searches.md) shows how.

## Memory and project knowledge

| | Project knowledge | Memory |
|---|---|---|
| **What it is** | Files you upload (CV, profile) | Things Claude learns from your conversations |
| **How it gets there** | You add it manually | Claude saves it automatically |
| **What it's for** | Facts about you that don't change often | Context that evolves over time |
| **Examples** | Your CV, my-profile.md | Application outcomes, interview feedback, changing preferences |

Both work together. Claude reads your files for the facts and draws on memory for the context around them.

## Memory builds over time

Your project gets more useful the longer you use it. In the first week, Claude knows what's in your profile and CV. After a month of searching, it also knows:

- which companies you've spoken to
- the kind of roles you keep going for
- the interview feedback you've had
- how your thinking has changed

That's why it's worth keeping your whole job search in one project, rather than in separate conversations.

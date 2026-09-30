# Interview Prep and Debrief

Get ready for an interview, talk it through afterwards, and, once you've had three, see what keeps coming up. Everything is built from your CV, your profile and the job description, so the answers it suggests are yours.

## How to use

This file sits in your project with your other toolkit files, and your project instructions tell your AI assistant when to use it. Copy the words you need, paste them into a new conversation in your project, and change the words in square brackets.

1. **Before an interview.** It asks what you know about the interview, then gives you a prep pack.
   ```
   I've got an interview for the [job title] role at [company]. Help me prepare.
   ```
2. **After an interview.** It asks you questions one at a time, then writes up the debrief.
   ```
   I've just had my interview for the [job title] role at [company]. Let's debrief.
   ```
3. **Save each debrief.**
   - **Claude Code:** it saves the file for you in an `interview-debriefs` folder.
   - **Claude app or another AI assistant:** it gives you the debrief in a grey box.
     1. Copy it with the copy icon.
     2. Save it in your Documents folder the same way you saved your profile, named with the date and the company, for example `debrief-2026-10-01-acme.md`.
     3. Add it to your project's files.
4. **Patterns.** Once you have three or more debriefs, it looks across them for you after each new one. You can also ask at any time:
   ```
   Look across my interview debriefs and tell me what keeps coming up.
   ```

## What you need

- Your CV and `my-profile.md` in your project
- The job description. If you saved it when you applied, it's already there; if not, paste it in when it asks

> [!NOTE]
> The prep pack only suggests answers from your CV and profile. Where you have no example for a likely question, it says so rather than making one up, so you can think of your own.

---

## Prompt

````
You are helping me prepare for job interviews and learn from them. Use only my CV, my profile (my-profile.md), the job description and anything I tell you. Never invent experience, results or numbers. If something you need is missing, ask me for it. Ask one question at a time and wait for my answer.

### Part 1: Before an interview

Use this part when I say I have an interview coming up.

1. Find the job description in my project's files. If it isn't there, ask me to paste it in.
2. Ask me, one at a time: what stage the interview is (for example a phone call, a first interview or a final round), who is interviewing me if I know, how long it is, and whether they've set a task such as a presentation.
3. Look up the company on its own website and in recent news. Only use pages you can open, and name the page for anything you tell me. If you can't check something, say so.
4. Give me a prep pack, in this order:
   - Company brief: 3–5 points on what the company does, any recent news and anything that tells me about its culture, each with its source
   - Terms in this pack: every acronym or piece of jargon in the pack, with what it means in plain words
   - Likely questions: 8–12, grouped as questions about the role, questions about my experience and questions about the company
   - A suggested answer for each question, built from a named example in my CV or profile. The same example can answer more than one question. Where I have no example, say "No example in your CV or profile" and suggest what kind of example would work
   - Gaps they may ask about: where the job description asks for something my CV doesn't show, with an honest way to answer
   - Questions for me to ask them: 5–8, specific to this company and role
5. Ask me if any part needs more work.

### Part 2: After an interview

Use this part when I say I've had an interview. Ask these questions one at a time:

1. Which company and role was this for?
2. What stage was it?
3. Can you remember what questions they asked? Take me through the ones you can remember, one at a time.
4. For each question: how do you think you answered it?
5. Overall, what went well?
6. What would you do differently?
7. What did you pick up from the interviewers, good or bad?
8. What questions did you ask them, and how did they react?
9. Did they mention any next steps?

Then write up the debrief under these headings: Company and role, Date, Stage, Interviewers, Questions and how I answered (each question with strong, OK or weak and a note), What went well, What to improve, What I picked up from them, My questions and their reactions, Next steps.

If you can save files (for example in Claude Code), save it as interview-debriefs/YYYY-MM-DD-company.md. Otherwise, give it to me in one grey box and remind me to save it, named with the date and the company, and add it to my project's files.

Then count my saved debriefs. If there are three or more, go straight on to Part 3.

### Part 3: Patterns across interviews

Use this part when I have three or more saved debriefs, or when I ask. Read all of them and tell me:

- the kinds of question that keep coming up
- where my answers are usually strong, and where they're usually weak
- anything interviewers keep reacting to, good or bad
- the questions that most need a better prepared answer, and which example from my CV or profile could answer each one

Finish with the two or three changes that would help most before my next interview.
````

# Profile Builder

Build your job search profile through a guided conversation. This generates a `my-profile.md` file that all the other prompts in this toolkit reference.

## How to use

Paste this entire prompt into Claude (or your AI tool of choice). If you have a CV, upload it at the same time. If you don't have a CV yet, that's fine. The prompt will work without one and can help you create one afterwards.

## Inputs

- **Your CV** (optional): upload it, drag it in, or paste the text. If you don't have one, just say so.

---

## Prompt

````
You are helping someone build their job search profile. This profile will be used by other prompts in the AI Job Search Toolkit to search for jobs, assess fit, tailor CVs, and write cover letters. Everything you produce here becomes the foundation for their entire search.

### Important rules

- Ask **one question at a time**. Never bundle multiple questions into a single message.
- Wait for the answer before moving on.
- If a CV was provided, read it first. Use it as a starting point and skip questions the CV already answers clearly. Confirm what you've pulled from the CV before moving on: "From your CV, I can see [summary]. Does that look right, or would you change anything?"
- If no CV was provided, note this and ask all questions from scratch.
- Keep your language clear and straightforward. Assume the user may never have used an AI tool before.
- Never guess or make up information. If something is unclear, ask.

### Stage 1: Core identity

Ask these questions one at a time:

1. "What's your name?"

2. "Where are you based? (City and country.) This helps me suggest the right job boards and company review sites for your region."

3. "Which best describes your career stage?"
   - New graduate (just finished or about to finish education)
   - Early career (0-3 years of experience)
   - Mid-career (3-10 years)
   - Senior (10+ years)
   - Executive (C-suite or VP level)

Note the career stage. It determines how you ask questions in every stage that follows.

### Stage 2: Experience and skills

Adapt your questions based on the career stage from Stage 1.

**If new graduate:**

1. "What did you study? (Subject, level, institution.)"

2. "Have you done any internships, work placements, volunteering, or personal projects? Tell me about them."

3. "What skills did those experiences build? Think beyond technical skills. Communication, teamwork, problem-solving, time management all count."

**If early career or mid-career:**

1. "Walk me through your career so far. What roles have you held and what did you do in each?"

2. "What are your core skills? What do people come to you for?"

3. "What industries or domains do you know well?"

**If senior or executive:**

1. "What's your leadership experience? Teams you've built, departments you've run, organisations you've shaped."

2. "What's your track record of measurable impact? Think about the numbers: revenue, efficiency, growth, cost reduction."

3. "What domains do you specialise in?"

### Stage 3: What you're looking for

**If new graduate:**

1. "What kind of work interests you? Don't worry about specific job titles yet. Think about what you'd enjoy doing day to day."

After their answer, suggest 3-5 relevant job titles based on what they've described. Ask: "Do any of these sound right? Feel free to adjust or add your own."

**If early career, mid-career, senior, or executive:**

1. "What job titles are you targeting?"

**Then for everyone:**

2. "What industries interest you? Are there any you want to avoid?"

3. "What's your preference for working arrangement? Fully remote, hybrid, or office-based? Any flexibility requirements? (For example, a 4-day week, flexible hours, compressed hours.)"

4. Adapt based on career stage:
   - **New graduate:** "What matters most to you in your first role? For example: mentorship and training, interesting work, good team culture, flexible hours, career progression, mission-driven company. Pick your top 3."
   - **Early or mid-career:** "What matters most in your next role? Growth opportunity, team culture, compensation, work-life balance, interesting problems, career progression?"
   - **Senior or executive:** "What matters most? Reporting lines, equity, strategic influence, team you'd inherit, company stage, mission alignment?"

### Stage 4: Dealbreakers and preferences

Explain the two-tier system first:

**If new graduate:**

"Let's talk about what's important to you. Some things might be non-negotiable, others are nice-to-have. Here's how the search tools will use them:

- **Hard dealbreakers** are things that would make you reject a role no matter what. The search tools will filter these out automatically.
- **Strong preferences** are things that matter to you, but you might be flexible on if everything else is right. The search tools will flag these but still show you the role.

Here are some common ones to think about:
- Commute length or location
- Minimum salary (if you have one in mind, I can share typical ranges for your target roles in your region as a reference point)
- Industries you definitely don't want to work in
- Must-haves like a training programme, mentorship, or flexible hours

Which of these matter to you, and which are hard dealbreakers vs strong preferences?"

**If early career, mid-career, senior, or executive:**

"Now let's talk about what you won't accept and what you'd prefer. There's a difference:

- **Hard dealbreakers** are things that would make you reject a role no matter what. The search tools will filter these out automatically.
- **Strong preferences** are things that matter to you, but you might be flexible on if everything else is right. The search tools will flag these but still show you the role."

Then ask one at a time:

1. "What are your hard dealbreakers? Things that would make you reject a role no matter what."

2. "Salary floor? What's the minimum you'd accept?"

3. "Location constraints? Any limits on where you'd work or how far you'd commute?"

4. "Industries or sectors to exclude?"

5. "Any other non-negotiables?"

6. "Now, what are your strong preferences? Important to you, but you might flex on them if everything else is right."

### Stage 5: Personality and working style (optional)

"Would you like to add personality and working style insights? These help me understand how to work with you during your search. For example, recognising when you need facts to regain confidence, when you're reacting emotionally to a setback, or when to challenge your gut instinct. They're a coaching input, not a job-matching tool.

If you've taken any of these assessments, you can share your results. If not, skip this section entirely.

- Myers-Briggs or 16 Personalities (free test at 16personalities.com)
- Enneagram (free test at truity.com/test/enneagram-personality-test)
- DISC (free test at tonyrobbins.com/disc)
- CliftonStrengths (gallup.com/cliftonstrengths, paid)
- Big Five / OCEAN (free test at bigfive-test.com)

Skip this? Just say 'skip' and we'll move on."

If the user shares results, note them. If they skip, move on without comment.

*These frameworks are trademarked by their respective owners. This toolkit is not affiliated with or endorsed by any of them.*

### Stage 6: Communication preferences

Ask one at a time:

1. "How do you want me to write when helping with cover letters and CVs? Pick what feels right:
   - Formal
   - Conversational
   - Direct
   - Somewhere in between"

2. "Are there any words or phrases you hate? Things you never want to see in your applications. For example: 'leverage', 'utilise', 'passionate', em dashes."

3. "UK English or US English?"

4. "When I write a cover letter for you, should the tone be:
   - Confident
   - Understated
   - Enthusiastic
   - Matter-of-fact"

### Output generation

After all stages are complete, generate the profile.

**Step 1: Generate `my-profile.md`**

Use this exact structure:

```markdown
# My Profile

## About me
[Name, location, career stage, professional summary]

## Experience and skills
### Domain knowledge
[Industries, workflows, and systems understood deeply]

### Key skills
[Core competencies and capabilities]

### Track record
[Measurable achievements and impact, if applicable]

## What I'm looking for
### Target roles
[Job titles being searched for]

### Target industries
[Industries of interest, and industries to avoid]

### Working arrangement
[Remote / hybrid / office preferences, flexibility requirements]

### What matters most
[Priorities ranked by importance]

## Hard dealbreakers
[Non-negotiable criteria, automatically filtered out by search prompts]

## Strong preferences
[Important but not absolute, flagged as "worth a closer look" if missed]

## Personality and working style
[Assessment results if provided, or "Not provided" if skipped]

## Communication preferences
[Writing style, tone, banned words, formatting, language variant]

## Regional settings
### Job boards
[Suggested platforms for the user's region]

### Company review sites
[Suggested review sources for the user's region]
```

**Step 2: Auto-populate regional settings**

Based on the user's location, suggest job boards and review sites. Use these as starting points:

- **UK:** LinkedIn, Indeed UK (uk.indeed.com), Totaljobs, Reed, Guardian Jobs. Review sites: Glassdoor UK (glassdoor.co.uk)
- **US:** LinkedIn, Indeed, Glassdoor US, Blind. Review sites: Glassdoor (glassdoor.com), Blind
- **Germany:** LinkedIn, StepStone, Xing. Review sites: Kununu
- **Australia:** LinkedIn, Seek, Indeed AU. Review sites: Glassdoor AU

Present the regional settings to the user: "Based on your location, I've suggested these job boards and review sites. Do these look right? You can add, remove, or adjust any of them."

**Step 3: Output and save the profile**

Output the complete profile in a code block so it's easy to copy.

For Claude Code: also write it directly to `my-profile.md` in the project folder.

Then tell the user:

"Here's your completed profile.
- **Claude Code:** I've saved this as `my-profile.md` in your project folder. You're all set.
- **Claude browser/desktop:** Copy the profile above, save it as a file called `my-profile.md`, and upload it to your project's knowledge base (drag and drop or use the upload button). This is important because your project instructions reference this file for every role assessment, CV, and cover letter."

**Step 4: Communication preferences**

"Your project instructions have a communication preferences section. To set those up, start a new conversation and ask: 'Can you help me set up my communication preferences?' It will walk you through a few quick questions about tone, language, and writing style."

**Step 5: If no CV was provided**

"You mentioned you don't have a CV yet. Once you've saved your profile, ask Claude to help you create one. Just say: 'Can you help me create a CV?' It will use everything from your profile as a starting point."

**Step 6: Set up automated searches**

"If you'd like to set up automated daily job searches, ask: 'Can you help me generate my Chrome extension search prompts?' This will create self-contained prompts you can schedule in the Claude Chrome extension to search job boards for you automatically. You'll need the Chrome extension installed first."
````

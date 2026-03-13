# Application Assessor

Assess whether a role is a good fit for you based on your profile. Use this after the search prompts have surfaced interesting roles and you've done your second-pass review.

## How to use

Paste the full job listing below this prompt. Make sure `my-profile.md` is in your project knowledge base (browser/desktop) or project folder (Claude Code).

**Important:** Read the full job listing yourself before using this prompt. Don't assess based on a search summary alone.

## Inputs

- **Job listing:** Paste the full job listing text below

---

## Prompt

You are helping me assess whether a specific job is a good fit. Read the job listing I've pasted below and assess it against my profile.

### Profile reference

Before starting, read `my-profile.md` for my skills, experience, dealbreakers, and preferences. If you're using Claude in the browser, this is in your project knowledge base. If you're using Claude Code, it's in your project folder.

### Assessment criteria

Evaluate the role across these dimensions:

1. **Hard dealbreaker check:** Does the role hit any of my hard dealbreakers? Check each one explicitly.

2. **Strong preference check:** Does it miss any of my strong preferences? List which ones.

3. **Skills match:** Which required skills do I have? Which am I missing? Which of my skills are partially relevant but not an exact match?

4. **Domain alignment:** How relevant is my industry and domain experience to this role?

5. **Culture indicators:** What can you infer from the listing's language and structure? (e.g. corporate vs startup tone, emphasis on autonomy vs process, language around work-life balance)

6. **Personality and working style fit:** If my profile includes assessment results, consider how my working style aligns with what the role and company appear to need. This is a coaching insight, not a scientific match. Don't overweight it.

7. **Career stage considerations:** If my profile shows I'm a new graduate or early career, weigh learning opportunity, mentorship signals, and training programmes more heavily than exact experience match. Missing 2 years of experience matters less than whether the role will help me grow.

### Recommendation

Give one of three recommendations:

**Apply** - "Strong fit. [Explain why across the dimensions above. Be specific about what aligns well.]"

**Worth a closer look** - "Gaps exist, but they may not be essential. [List the gaps. For each one, explain whether it reads as a hard requirement or a likely wishlist item. Hiring managers often list ideal qualifications knowing they'll compromise. Help me read between the lines.]"

**Skip** - "Hits a hard dealbreaker: [which one and why]. If this dealbreaker no longer applies or you've changed your mind about it, you can override this recommendation."

### Additional output

After the recommendation, include:

- **Skills match summary:** Have / Missing / Partially relevant (as a clear list)
- **Domain alignment:** How relevant my experience is, and any transferable knowledge
- **Strong preferences missed:** Any from my profile that this role doesn't meet
- **Questions to ask if you decide to apply:** Specific questions that address the gaps identified (e.g. "Ask about the team structure since the listing doesn't mention who you'd report to", "Clarify the remote working policy since the listing says 'flexible' without specifics")

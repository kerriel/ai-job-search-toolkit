# Cover Letter Writer

Generate a tailored cover letter for a specific role. Anchored in something personal and specific about why you're interested in this company.

## How to use

Paste the job listing you're applying to. Optionally, also include your tailored CV from the previous step. Make sure `my-profile.md` is in your project knowledge base (browser/desktop) or project folder (Claude Code).

## Inputs

- **The job listing:** Paste the full job listing text
- **Your tailored CV** (optional): If you've already tailored your CV for this role, include it for a more connected letter

---

## Prompt

You are helping me write a cover letter for a specific role. Read the job listing, my profile, and my CV (if provided), then write a tailored cover letter.

### Profile reference

Before starting, read `my-profile.md` for my communication preferences, writing style, skills, and experience. If you're using Claude in the browser, this is in your project knowledge base. If you're using Claude Code, it's in your project folder.

### Before writing anything, ask this question

"Is there a specific reason you're interested in this company? Something you've read, experienced, or believe about them that isn't just in the job listing?"

Wait for the answer. This personal, specific detail becomes the anchor of the letter. A cover letter without something genuine to say about the company is just a summary of the CV, and hiring managers can tell.

If the user says they don't have a specific reason, help them find one: "Have a look at their website, blog, or recent news. Is there anything about their mission, product, culture, or recent work that resonates with you? Even something small gives the letter an authentic anchor."

### Rules - read these carefully

These rules are non-negotiable:

1. **Never fabricate or embellish.** If I haven't done it, don't claim I have. Not even with hedging language.

2. **Never inflate scope, ownership, or impact.** Same rule as the CV tailor. Keep it honest.

3. **Don't parrot the job listing's language.** Write in my voice, not the employer's words reflected back at them.

4. **Avoid generic AI cover letter language.** Never use phrases like:
   - "I am writing to express my keen interest in..."
   - "I believe my unique skill set..."
   - "I am excited about the opportunity to..."
   - "I am confident that my experience..."
   - "I would welcome the chance to discuss..."
   These are dead giveaways. Write something a human would actually say.

5. **Follow my communication preferences.** Use the writing style, tone, language variant, and banned words from my profile.

6. **Draw on personality insights if available.** If my profile includes assessment results, use them to help me articulate my working style authentically. This is about self-expression, not culture fit assessment.

### What to do

1. Use the personal detail from the question above as the anchor
2. Connect my most relevant experience to the role requirements (don't just list everything)
3. Write in my voice, matching the tone and style from my profile
4. Keep it to a natural length for my region and industry (typically 3-4 paragraphs for the UK, adjust based on norms)
5. Output in plain text, ready to paste into an application form or email

### Structure

- **Opening:** Lead with the personal detail or a direct statement about why this role. Not a generic "I am writing to apply for..."
- **Body (1-2 paragraphs):** Connect specific experience and achievements to what the role needs. Pick the 2-3 strongest connections, not everything
- **Closing:** What I'd bring and a straightforward next step. No grovelling, no over-promising

### Review step

After producing the cover letter, ask:

"Read this as if you're the hiring manager. Does it sound like the person they'd meet in the interview? If anything feels generic, forced, or unlike your natural voice, tell me what to change."

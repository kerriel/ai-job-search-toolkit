# CV Tailor

Tailor your CV to a specific role. Adjusts emphasis and framing to highlight the most relevant parts of your experience for this particular job.

## How to use

Upload or paste your master CV and the job listing you're applying to. Make sure `my-profile.md` is in your project knowledge base (browser/desktop) or project folder (Claude Code).

If you don't have a CV yet, this prompt can help you create one from scratch using your profile.

## Inputs

- **Your master CV:** Upload, drag in, or paste the text
- **The job listing:** Paste the full job listing text

---

## Prompt

You are helping me tailor my CV for a specific role. Read my CV, the job listing, and my profile, then produce a tailored version.

### Profile reference

Before starting, read `my-profile.md` for my communication preferences, writing style, and professional context. If you're using Claude in the browser, this is in your project knowledge base. If you're using Claude Code, it's in your project folder.

### Rules - read these carefully

These rules are non-negotiable:

1. **Never fabricate experience or skills.** If I haven't done it, don't say I have. Not even with softer language. Not even if it would make the CV stronger.

2. **Never inflate scope, ownership, or impact.** If I managed one person, don't frame it as "led a team." If I contributed to a project, don't frame it as "drove the initiative." If results were a team effort, don't imply they were mine alone.

3. **Don't parrot the job listing's language.** Reframe my experience in my own voice, not in the employer's words mirrored back at them. Hiring managers notice when a CV reads like their own job ad repeated back.

4. **Adapt emphasis and framing, not facts.** You can reorder sections, adjust which achievements are highlighted, and reword descriptions to better connect with the role. You cannot change what happened.

5. **Follow my communication preferences.** Use the writing style, tone, language variant, and banned words from my profile.

6. **Preserve my CV structure** unless I specifically ask for a restructure. Move things around within sections, but keep the sections themselves.

### What to do

1. Read the CV and the job listing
2. Identify which parts of my experience are most relevant to this specific role
3. Adjust the emphasis: bring the most relevant experience to the front, expand relevant achievements, and reduce less relevant detail
4. Reword descriptions to connect more clearly with the role requirements, in my voice
5. Output the tailored CV in markdown format

### Output

The tailored CV in markdown, followed by:

**Changes made:**
- What was reordered and why
- What was reworded and why
- What was expanded or reduced and why

### Review step

After producing the tailored CV, ask:

"Read this as if you're the person hiring. Does it sound like you? Would you be comfortable saying all of this in an interview? If anything feels like a stretch or doesn't sound like your voice, tell me what to change."

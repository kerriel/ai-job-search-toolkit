# Job Search - Indeed UK

An Indeed UK-specific search prompt that screens job postings against your profile and cross-references company reviews.

## How to use

Paste this prompt into the Claude Chrome extension as a scheduled task, or run it manually. Make sure `my-profile.md` is in your project knowledge base (browser/desktop) or project folder (Claude Code).

## Inputs

- **Job search query:** The role title to search for (e.g. Product Manager, Operations Manager, Head of Engineering)
- **Location:** The geographic location to search (e.g. Remote, Manchester, United Kingdom)

---

## Prompt

You are helping me evaluate job postings from Indeed UK in a systematic way. Your primary deliverable is the structured summary at the end. Every screening step exists to feed that summary. Do not finish without producing it.

### Profile reference

Before starting, read `my-profile.md` for my full profile, screening criteria, preferences, and dealbreakers. If you're using Claude in the browser, this is in your project knowledge base. If you're using Claude Code, it's in your project folder.

Use the profile for all screening decisions. Apply hard dealbreakers as automatic filters. Flag missed strong preferences as "worth a closer look" rather than filtering out.

### Workflow

**Important: As you screen roles, maintain a running shortlist. Each time a role passes all filters, immediately note the job title, company name, and link before moving to the next role. This shortlist is your working reference for the final summary.**

1. Navigate to Indeed UK (uk.indeed.com) and search for the specified job search query in the specified location

2. Filter results to show only recent postings (apply the posting age threshold from your profile's hard dealbreakers), sorted by date

3. For each job posting, working from the top of the results, apply the following checks in order and skip immediately if any hard dealbreaker is found:

   - **Posting date** - Check this first. Apply the posting age threshold from your profile's hard dealbreakers. Skip and close anything older before reading further.

   - **Working arrangement** - Apply working arrangement preferences from your profile. Skip if a hard dealbreaker is hit. Flag as "worth a closer look" if a strong preference is missed.

   - **Industry** - Apply industry exclusions from your profile. Skip excluded industries immediately.

   - **Salary** - Apply salary floor from your profile. Skip if below. If no salary is shown, only surface the role if it's a strong match across skills, domain, and preferences. If surfaced, clearly flag: "No salary listed, needs confirming."

   - **Seniority** - Apply seniority preferences from your profile.

   - **Role fit** - Assess against skills and domain knowledge from your profile. Note any gaps but don't automatically reject unless the gap is fundamental.

   - **Posted by** - Note whether the role is posted by a direct employer or a recruiter. Include the recruiter name and agency if visible. This is informational, not a quality signal.

   - **If the role passes all checks, add it to your running shortlist immediately before continuing to the next role.**

4. For roles posted by direct employers that pass initial screening:

   - Open a new tab and navigate to the company review site(s) listed in your profile's regional settings
   - Search for the company name
   - Navigate to the Reviews section and sort by most recent
   - Expand multiple reviews using "Show more" buttons
   - Navigate through at least page 2 for a comprehensive view
   - Evaluate:
     - Overall rating and "would recommend" percentage
     - Work/life balance rating
     - Culture and values score
     - Senior management score
     - Recent employee feedback on stability, management style, autonomy, and growth
   - Note quality indicators: review volume (number of reviews), recency (date range), source diversity (departments/roles represented)
   - Flag red flags: micromanagement, poor work/life balance, high turnover, instability, lack of autonomy, top-heavy or bureaucratic structure
   - Flag if the review sample is small, outdated, or skewed

5. For each role that passes all filters, extract and summarise the following before moving on to the next role:

   - Job title and company name
   - Whether posted by direct employer or recruiter (include name and agency if visible)
   - Salary range (if shown), or "No salary listed, needs confirming"
   - Exact working arrangement: fully remote, hybrid, or office-based, and how many days in office if stated
   - Office location if relevant
   - Company stage: startup, scale-up, established
   - Who the role reports to and any mention of team size or structure
   - Key responsibilities: the main 4-5 points from the job description
   - Essential requirements: as listed
   - Desirable or nice-to-have requirements
   - Any skills gaps against your profile
   - Any strong preferences from your profile that this role misses
   - Company reviews: overall rating, culture and values score, senior management score, recurring themes. Include review volume, recency, and source diversity
   - Any review red flags noted
   - A direct link to the job listing

### Final output - mandatory

**You must produce this summary. Do not end without it.** Once all roles have been checked, compile your running shortlist into a single structured summary with the full details from step 5 for each passing role. Clearly separate each role. Label the summary:

**"Job Search Summary - Indeed UK - [today's date]"**

This summary should be ready to paste into your Claude project for second-pass review and application materials.

If no roles passed the screening, explicitly state: **"No roles matched the screening criteria today - [today's date]."** Do not end silently.

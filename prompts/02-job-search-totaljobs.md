# Job Search - Totaljobs

A Totaljobs-specific search prompt that screens job postings against your profile and cross-references company reviews. Uses a two-stage screening approach: card preview first, then full description.

## How to use

Paste this prompt into the Claude Chrome extension as a scheduled task, or run it manually. Make sure `my-profile.md` is in your project knowledge base (browser/desktop) or project folder (Claude Code).

## Inputs

- **Job search query:** The role title to search for (e.g. Product Manager, Operations Manager, Head of Engineering)
- **Location:** The geographic location to search (e.g. Remote, Manchester, United Kingdom)
- **Employment type:** Permanent or Contract

---

## Prompt

You are helping me evaluate job postings from Totaljobs in a systematic way. Your primary deliverable is the structured summary at the end. Every screening step exists to feed that summary. Do not finish without producing it.

### Profile reference

Before starting, read `my-profile.md` for my full profile, screening criteria, preferences, and dealbreakers. If you're using Claude in the browser, this is in your project knowledge base. If you're using Claude Code, it's in your project folder.

Use the profile for all screening decisions. Apply hard dealbreakers as automatic filters. Flag missed strong preferences as "worth a closer look" rather than filtering out.

### Workflow

1. Navigate to the Totaljobs "My recommended jobs" section and begin reviewing job listings systematically from the top

2. For each job card displayed on the page, review the visible details:
   - Job title (teal/blue clickable link at top of card)
   - Company name (building icon)
   - Location (location pin icon)
   - Employment type (document icon: Permanent or Contract)
   - Salary information (money icon)
   - Posted time (bottom left of card)

3. Apply the following dealbreaker checks in order using the card preview, and skip immediately if any hard dealbreaker is found:

   - **Posting date** - Check this first. Apply the posting age threshold from your profile's hard dealbreakers. Skip anything older before reading further.

   - **Location and working arrangement** - Apply working arrangement and location preferences from your profile. Skip if a hard dealbreaker is hit. Flag as "worth a closer look" if a strong preference is missed.

   - **Salary** - Apply salary floor from your profile. Skip if below. If no salary is shown, only surface the role if it's a strong match across skills, domain, and preferences. If surfaced, clearly flag: "No salary listed, needs confirming."

   - **Employment type** - Check against the specified preference (Permanent or Contract).

   - **Seniority** - Assess from the job title against your profile's seniority preferences.

4. For job cards that pass the initial card-level screening, click on the job title link to open the full job description and apply deeper checks:

   - **Industry** - Apply industry exclusions from your profile. Skip excluded industries immediately.

   - **Working arrangement (confirm)** - Confirm the exact working arrangement from the full description. Apply preferences from your profile.

   - **Role fit** - Assess against skills and domain knowledge from your profile. Note any gaps but don't automatically reject unless the gap is fundamental.

   - **Posted by** - Note whether the role is posted by a direct employer or a recruitment agency. Include the recruiter name and agency if visible. This is informational, not a quality signal.

   - **If the role passes all checks, add it to your running shortlist immediately.**

5. Click the "See more +" button to load additional job listings and continue the same screening process until all available recent roles have been reviewed

6. For roles posted by direct employers that pass all screening:

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

7. For each role that passes all filters, extract and summarise the following before moving on to the next role:

   - Job title and company name
   - Whether posted by direct employer or recruitment agency (include name if visible)
   - Salary range (if shown), or "No salary listed, needs confirming"
   - Exact working arrangement: fully remote, hybrid, or office-based, and how many days in office if stated
   - Office location if relevant
   - Employment type: Permanent or Contract
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

Once all roles have been checked, compile your running shortlist into a single structured summary with the full details from step 7 for each passing role. Clearly separate each role. Label the summary:

**"Job Search Summary - Totaljobs - [today's date]"**

This summary should be ready to paste into your Claude project for second-pass review and application materials.

If no roles passed the screening, explicitly state: **"No roles matched the screening criteria today - [today's date]."** Do not end silently.

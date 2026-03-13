# Job Search - Generic Template

A customisable template for searching any job board systematically. For UK job boards (LinkedIn, Indeed UK, Totaljobs), use the pre-built prompts in this repo instead.

## How to use

1. Copy this template and customise the **Navigation** section for your job board
2. Keep everything else unchanged (the screening order, summary format, and profile referencing are designed to work together)
3. Paste the customised prompt into the Claude Chrome extension as a scheduled task, or run it manually

## Inputs

- **Job search query:** The role title to search for
- **Location:** The geographic location to search
- **Job board URL:** The starting page for the job board

---

## Prompt

You are helping me search for jobs systematically. Your primary deliverable is the structured summary at the end. Every screening step exists to feed that summary. Do not finish without producing it.

### Profile reference

Before starting, read `my-profile.md` for my screening criteria, preferences, and dealbreakers. If you're using Claude in the browser, this is in your project knowledge base. If you're using Claude Code, it's in your project folder.

Use the profile for:
- Hard dealbreakers (filter these out automatically)
- Strong preferences (flag if missed, but still surface the role as "worth a closer look")
- Skills and domain knowledge (for assessing role fit)
- Target roles and industries
- Regional settings (which review sites to cross-reference)

### Navigation

<!-- CUSTOMISE THIS SECTION for your job board -->

1. Navigate to [job board URL]
2. Search for the specified job search query in the specified location
3. Filter results to show only recent postings, sorted by date
4. Work through listings from the top

<!-- END CUSTOMISATION -->

### Screening workflow

**Important: As you screen roles, maintain a running shortlist. Each time a role passes all filters, immediately note the job title, company name, and link before moving to the next role.**

For each job posting, apply these checks in order. Stop and skip as soon as a hard dealbreaker is found:

1. **Posting date** - Check this first. Apply the posting age threshold from the profile's hard dealbreakers. Skip anything older before reading further.

2. **Working arrangement** - Check against the profile's working arrangement preferences. If remote/hybrid/office requirements are a hard dealbreaker, skip. If they're a strong preference, flag as "worth a closer look" but continue screening.

3. **Industry** - Check against the profile's industry exclusions. Skip excluded industries immediately.

4. **Salary** - Check against the profile's salary floor. Skip if below. If no salary is shown, only surface the role if it's a strong match to the profile across skills, domain, and preferences. If surfaced, clearly flag: "No salary listed, needs confirming."

5. **Seniority** - Check against the profile's target roles and seniority preferences.

6. **Role fit** - Assess against skills and domain knowledge from the profile. Note any gaps but don't automatically reject unless the gap is fundamental (e.g. the role requires hands-on coding and the profile doesn't include that).

7. **Posted by** - Note whether the role is posted by a direct employer or a recruiter. Include the recruiter name and agency if visible. This is informational, not a quality signal. Recruiter postings are a normal part of the job market.

**If the role passes all checks, add it to your running shortlist immediately.**

### Company review cross-referencing

For roles that pass screening and are posted by direct employers:

1. Open the company review site(s) listed in the profile's regional settings
2. Search for the company name
3. Navigate to the Reviews section, sort by most recent
4. Expand multiple reviews and check at least page 2 for a broader view
5. Evaluate:
   - Overall rating and "would recommend" percentage
   - Work/life balance rating
   - Culture and values score
   - Senior management score
   - Recent employee feedback on stability, management style, autonomy, and growth
6. Note quality indicators:
   - **Review volume:** How many reviews does the company have?
   - **Recency:** What date range do the reviews cover?
   - **Source diversity:** Are reviews from multiple departments and roles, or concentrated in one area?
7. Flag red flags: micromanagement, poor work/life balance, high turnover, instability, lack of autonomy, top-heavy or bureaucratic structure
8. Flag if the review sample is small, outdated, or skewed towards a single department

### Summary output format

For each role that passes all filters, extract and summarise using this format:

```
### [Job title] - [Company name]
- **Posted by:** Direct employer / Recruiter name (agency)
- **Salary:** Range if shown, or "No salary listed, needs confirming"
- **Working arrangement:** Fully remote / Hybrid (X days) / Office-based
- **Office location:** If relevant
- **Company stage:** Startup / Scale-up / Established
- **Reports to:** Role title, team size if mentioned
- **Key responsibilities:** Top 4-5 points
- **Essential requirements:** As listed
- **Desirable requirements:** As listed
- **Skills gaps:** Against profile
- **Strong preferences missed:** Any strong preferences from the profile that this role doesn't meet
- **Company reviews:** Overall rating, culture score, management score, recurring themes. Review volume (number of reviews), recency (date range checked), source diversity (departments/roles represented)
- **Review red flags:** Any concerns noted. Flag if review sample is small, outdated, or skewed
- **Link:** Direct URL to the listing
```

### Final output - mandatory

Once all roles have been checked, compile your running shortlist into a single structured summary with the full details above for each passing role. Clearly separate each role. Label the summary:

**"Job Search Summary - [Job Board] - [today's date]"**

If no roles passed the screening, explicitly state: **"No roles matched the screening criteria today - [today's date]."** Do not end silently.

---

## Customisation guidance

**What to customise** for a new job board:
- The Navigation section (how to reach listings, how to filter by date, how pagination works, any platform-specific UI elements)
- Platform-specific filtering (date filters, location filters, employment type filters)

**What to keep unchanged:**
- The screening order (posting date > working arrangement > industry > salary > seniority > role fit > employer vs recruiter)
- The summary output format
- The profile referencing pattern
- The company review cross-referencing process
- The two-tier dealbreaker system
- The mandatory final output section

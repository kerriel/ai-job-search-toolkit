# Job Search Prompt Generator

Generate a self-contained job search prompt for the Claude Chrome extension. The generated prompt will have your profile, screening criteria, and job board instructions baked in so the Chrome extension can run it without access to any external files.

## How to use

1. Paste the prompt below into your Claude project (browser/desktop) or Claude Code session, where it has access to your `my-profile.md`
2. Answer the questions it asks (which job board, what to search for)
3. It will generate a ready-to-use Chrome extension prompt
4. Follow the setup instructions at the bottom of this page to schedule it

## Inputs

- Your `my-profile.md` (must be in your project knowledge base or project folder)

---

## Prompt

````
You are helping me generate a job search prompt for the Claude Chrome extension. The Chrome extension runs independently and cannot access any project files, so the prompt you generate must be completely self-contained with all my profile information, screening criteria, and preferences built in.

### Step 1: Read my profile

Read `my-profile.md` from the project knowledge base (browser/desktop) or project folder (Claude Code). You will use everything in it to build the generated prompt.

### Step 2: Ask which job board

Ask me:

"Which job board is this prompt for?"
- LinkedIn
- Indeed UK
- Totaljobs
- Other (I'll describe how it works)

Wait for my answer before continuing.

### Step 3: Ask for search details

Based on the job board, ask me for:

- **Job search query:** What role title(s) to search for
- **Location:** Where to search

If I chose Totaljobs, also ask:
- **Employment type:** Permanent or Contract

If I chose "Other", also ask:
- **Job board name and URL**
- **How to reach job listings** (e.g. a specific page, saved searches, recommended jobs)
- **How to load more results** (e.g. pagination, "see more" button, infinite scroll)
- **Any platform-specific filtering options** (e.g. date filter, employment type filter)

Wait for my answers before continuing.

### Step 4: Generate the Chrome extension prompt

Generate a single, self-contained prompt that I can paste directly into the Claude Chrome extension. The prompt must:

1. **Open with my profile baked in.** Start with "You are helping me evaluate job postings from [job board] in a systematic way. Before starting, here is my full profile to use when assessing role fit:" followed by all of the following from my profile:
   - About me (summary)
   - Domain knowledge
   - Key skills
   - Track record
   - Hard dealbreakers (label these "Absolute dealbreakers - skip and close immediately")
   - Strong preferences
   - Target roles and seniority preferences
   - Working arrangement preferences
   - Regional settings (which company review sites to use)

2. **Include the platform-specific navigation.** Use the instructions below based on the chosen job board:

   **LinkedIn:**
   - Start on the LinkedIn notifications page and navigate to job search results from saved searches
   - Work through listings from the top

   **Indeed UK:**
   - Navigate to Indeed UK (uk.indeed.com) and search for the specified job search query in the specified location
   - Filter results to show only recent postings (apply the posting age threshold from the dealbreakers), sorted by date
   - Work through listings from the top of the results

   **Totaljobs:**
   - Navigate to the Totaljobs "My recommended jobs" section and begin reviewing job listings systematically from the top
   - For each job card displayed on the page, review the visible details:
     - Job title (teal/blue clickable link at top of card)
     - Company name (building icon)
     - Location (location pin icon)
     - Employment type (document icon: Permanent or Contract)
     - Salary information (money icon)
     - Posted time (bottom left of card)
   - Apply card-level dealbreaker checks first (posting date, location, salary, employment type, seniority from title), then click through to the full description for deeper checks (industry, working arrangement confirmation, role fit, posted by)
   - Click the "See more +" button to load additional job listings and continue until all available recent roles have been reviewed

   **Other:**
   - Use whatever navigation details the user provided

3. **Include the screening workflow.** For each job posting, apply these checks in order. Skip immediately if any hard dealbreaker is found:

   - Posting date: check first, apply the posting age threshold from dealbreakers, skip anything older before reading further
   - Working arrangement: apply preferences, skip if hard dealbreaker, flag as "worth a closer look" if strong preference missed
   - Industry: apply exclusions, skip excluded industries immediately
   - Salary: apply salary floor, skip if below. If no salary shown, only surface if a strong match across skills, domain, and preferences. Flag "No salary listed, needs confirming"
   - Seniority: apply seniority preferences
   - Role fit: assess against skills and domain knowledge. Note gaps but don't reject unless fundamental
   - Posted by: note direct employer vs recruiter/agency. Include name if visible. Informational, not a quality signal
   - If the role passes all checks, add to running shortlist immediately

   For Totaljobs, split this into card-level checks and full-description checks as described in the navigation section.

4. **Include company review cross-referencing.** For roles posted by direct employers that pass screening:
   - Open the company review site(s) from the regional settings
   - Search for the company name
   - Navigate to Reviews, sort by most recent
   - Expand multiple reviews, check at least page 2
   - Evaluate: overall rating, "would recommend" percentage, work/life balance, culture and values, senior management, recent feedback on stability, management style, autonomy, growth
   - Note quality indicators: review volume, recency, source diversity
   - Flag red flags: micromanagement, poor work/life balance, high turnover, instability, lack of autonomy, top-heavy or bureaucratic structure
   - Flag if review sample is small, outdated, or skewed

5. **Include the summary output format.** For each role that passes all filters, extract and summarise:
   - Job title and company name
   - Whether posted by direct employer or recruiter/agency (include name if visible)
   - Salary range (if shown), or "No salary listed, needs confirming"
   - Exact working arrangement: fully remote, hybrid, or office-based, and how many days in office if stated
   - Office location if relevant
   - Employment type: Permanent or Contract (include this field for Totaljobs; omit for other platforms unless relevant)
   - Company stage: startup, scale-up, established
   - Who the role reports to and any mention of team size or structure
   - Key responsibilities: the main 4-5 points
   - Essential requirements: as listed
   - Desirable or nice-to-have requirements
   - Skills gaps against my profile
   - Strong preferences from my profile that this role misses
   - Company reviews: overall rating, culture and values score, senior management score, recurring themes. Include review volume, recency, source diversity
   - Review red flags noted
   - Direct link to the job listing

6. **End with the mandatory final output instruction.** Once all roles have been checked, compile the running shortlist into a single structured summary with full details for each passing role. Clearly separate each role. Label: "Job Search Summary - [job board name] - [today's date]". If no roles passed, state: "No roles matched the screening criteria today - [today's date]." Do not end silently.

### Step 5: Present the generated prompt

Output the complete generated prompt in a code block so I can copy it easily. Do not include any instructions, commentary, or explanation inside the code block. The code block should contain only the prompt text, ready to paste.

After the code block, remind me: "Copy this prompt and follow the Chrome extension setup instructions in the job search prompt generator page."
````

---

## Setting up in the Claude Chrome extension

Once you have your generated prompt:

1. **Log into your job board and review sites first.** Open Chrome and make sure you're logged into the job board (LinkedIn, Indeed, Totaljobs, etc.) and any company review sites (e.g. Glassdoor). The Chrome extension browses as you, so it needs your active sessions to access job listings and reviews. Copy the URL of the page you want the prompt to start from (e.g. the LinkedIn jobs page).
2. **Click the Claude Chrome extension** icon in your browser toolbar
3. **Click the three dots** at the top right of the extension box and click **Settings**
4. In the left-hand nav, go down to **Shortcuts** and click the black **Create shortcut** button
5. **Paste your generated prompt** into the prompt box
6. **Give it a title** in the task name field at the top, e.g.:
   - "LinkedIn - Marketing Manager - London"
   - "Indeed UK - Software Engineer - Remote"
   - "Totaljobs - Operations Lead - Permanent - Manchester"
7. **Paste the starting URL** you copied in step 1
8. **Toggle on the schedule** button. Select the frequency from the first dropdown (daily works well) and set the time you want it to run. Early morning (e.g. 6:00 AM) means results are ready when you sit down to review
9. **Leave the model as it is** and click **Create shortcut**
10. **Repeat for each job board and search query.** Run the generator again to create separate prompts for different boards or search terms

### Site permissions (recommended)

By default, the Chrome extension can run on any website. It's worth restricting it to only the sites it needs.

1. Go to your settings in Claude.ai or Claude Desktop
2. Navigate to **Claude Chrome** in the settings menu
3. Under **Default for all sites**, choose **Block extension**
4. Add the specific websites you want the extension to work on (your job boards and company review sites, e.g. linkedin.com, uk.indeed.com, totaljobs.com, glassdoor.co.uk)

### Tips

- **One prompt per job board per search query.** If you search for "Head of Product" and "Director of Operations" on LinkedIn, generate two separate prompts.
- **Update when your profile changes.** If you update `my-profile.md` (new dealbreakers, different salary expectations, etc.), regenerate your Chrome prompts so they stay in sync.
- **Review the generated prompt before scheduling.** Read through it to make sure your profile details look right and nothing sensitive is included that you wouldn't want in the Chrome extension.
- **Keep Chrome open.** Scheduled searches only run while Chrome is open. If you close your browser or shut down your computer, any searches scheduled during that time won't run.

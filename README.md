# Foundit Jobs Scraper & API - Monster India, Gulf & Singapore

Foundit Jobs Scraper and API: search all nine foundit sites at once, live, and get each job's title, company, location, years of experience asked, skills, job type, pay when shown, first-listed date, closing date, country site and links, newest first. foundit is the new name of Monster India, Monster Gulf and Monster's Southeast Asia sites: foundit.in, founditgulf.com, foundit.sg, foundit.com.ph, foundit.my, foundit.id, foundit.hk, monster.co.th and monster.com.vn, with 450,000+ open jobs on 2026-11-08. Turn on full details for the description, every place with its state and the qualifications asked for.

Use it as a foundit jobs API or a Monster India jobs scraper with no login and no key, or as a daily feed of new jobs in Bangalore, Mumbai, Delhi, Dubai, Singapore or Manila, from the Apify Console, the Apify API, Python, JavaScript, n8n, Make or an AI agent, and export JSON, CSV or Excel. Type a place and the run searches the foundit site that lists it, so India and the Gulf fit in one run. Available as an [Apify Actor](https://apify.com/anshumanatrey/foundit-jobs-search). $0.0018 per job, $0.0019 with full details, no start fee.

## What does it do?

- **Searches all nine foundit sites in one run.** On 2026-11-08 they listed 450,058 open jobs: India 219,732, Singapore 107,828, the Philippines 39,492, the Gulf 30,909, Malaysia 21,817, Indonesia 11,602, Vietnam 6,923, Thailand 6,194 and Hong Kong 5,561 (Hong Kong also lists Taiwan and China, the Gulf also lists Egypt).
- **Each place goes to the site that lists it.** Bangalore and Pune go to foundit.in, Dubai and UAE to founditgulf.com, Manila to foundit.com.ph, and a region such as Southeast Asia to all six sites in it. No country selector, and several countries in one run.
- **Only jobs in the place you typed.** foundit's own search adds nearby cities and remote jobs to a city search (Thane to Mumbai, six remote jobs to Dubai in our check); this actor checks every job's location and keeps the ones in your place. Bangalore also finds Bengaluru and Gurgaon finds Gurugram, by foundit's own place list.
- **Years of experience on every row that states them**, as numbers you can filter on: type 3, 2-5, 5+ or fresher.
- **The real first-listed date, newest first.** foundit's "Posted 5 hours ago" moves when an employer renews an old job; postedAt is the date foundit's job page gives Google, and the renewal date comes separately as refreshedAt.
- **Remote jobs foundit's own filter misses.** Most jobs on foundit are copied from other sites and say remote only in their title; this actor reads the title as well as foundit's work-from-home type.
- **Checks job links.** Paste foundit links, old monsterindia.com links included, and each comes back open, closed or not found.

## How is it different from other Foundit scrapers?

- **Nine sites, several in one run.** Of the nine Foundit actors with 10 or more users (the price table below), the ones made for Foundit search India only (themineworks, shahidirfan, data_daemon) or one market per run, picked from a list of four to seven (memo23, khadinakbar, scrapewise, scrapesage). None of the nine lists Thailand or Vietnam, and memo23 and scrapesage leave the Philippines out (one says its site is behind a challenge, the other that it no longer runs); its 39,492 jobs answer here through foundit's own search. This actor sends each typed place to its site and merges the answers, newest first.
- **The place you asked for, checked.** A city search on foundit also returns jobs in nearby cities and remote jobs: of foundit's newest 100 Dubai accountant jobs on 2026-11-08, six were remote jobs with no Dubai in them; of its newest 100 Mumbai sales manager jobs, eight were in Thane and one was a Hyderabad remote job. This actor drops them, so the place column is what you asked for.
- **First-listed date, not the refresh date.** foundit's own date filter and its "Posted 5 hours ago" count from a job's last renewal (memo23's README says the same of its days filter). Here a job renewed today but first listed a month ago is a month old, and refreshedAt still tells you it was renewed.
- **Native or syndicated on every row.** About 98% of the newest foundit jobs are copied from other job sites, mostly LinkedIn, and their apply link goes there; jobSource says which is which, and applyUrl points to the right place.
- **You pay for what you get.** One charge per delivered row, no start fee, and a spending limit stops the run cleanly with the jobs it paid for.

## When should I use it?

- **Job seekers and job boards:** new jobs by title, city, experience and date across India, the Gulf and Southeast Asia, on a daily schedule.
- **Recruiters and staffing agencies:** who is hiring for a role right now, in which city, for how many years of experience, and whether a consultant or the company posted it.
- **Sales and market research:** companies hiring for a function, by country and date, as a buying signal; skills in demand per city.
- **Data teams and AI agents:** one clean feed of foundit jobs through the API or MCP, in the same shape as the sibling job actors below.

## How much does it cost to scrape Foundit jobs?

Pay per event: $1.80 per 1,000 jobs, or $1.90 per 1,000 with full details, and no start fee. Apify's free $5 monthly credit covers about 2,700 jobs. Platform usage is included, and there is no monthly fee.

| Event | Price | When it is charged |
|---|---|---|
| Job | $0.0018 | One saved job, and one checked link that is closed or not found |
| Job with details | $0.0019 | One saved job with full details on |

Foundit Jobs Scraper's Apify Store header, "from $1.44 / 1,000 jobs", shows the lowest discount-tier price: the GOLD price. FREE and BRONZE users (Apify's Free and Starter plans) pay the base price in the table, $0.0018 a job and $0.0019 with details; SILVER (Scale) pays 10% less, $0.00162 and $0.00171; GOLD (Business) and above pay 20% less, $0.00144 and $0.00152.

| Run (Free and Starter price) | Cost |
|---|---|
| 100 newest jobs | $0.18 |
| 100 jobs with full details | $0.19 |
| 1,000 jobs | $1.80 |
| A whole search, the 9,600 newest jobs foundit shows for it on one site | $17.28 |

Number of jobs (`maxJobs`) sets the most a run can cost, and a run stops at its spending limit with a message saying so.

## How does the price compare with other Foundit scrapers?

Every actor on the Apify Store that names Foundit in its title or slug and had 10 or more users in the last 30 days, found by searching the Store for 9 Foundit and Monster terms on 2026-11-08 (59 actors read), ordered by users. Free-plan prices from each actor's current pricing.

| Actor | Users, 30 days | Per job | Start fee | Sites |
|---|---|---|---|---|
| getascraper/india-job-inventory-feed | 213 | $0.00199 | $0.00005 | foundit.in among 12 Indian job boards, 25 jobs a board by default |
| themineworks/foundit-jobs-scraper | 186 | $0.0025 ($0.002 on Starter) | none | foundit.in |
| memo23/foundit-jobs-scraper | 166 | $0.00599 | $0.005 | India, Singapore, Malaysia or Indonesia, one a run |
| shahidirfan/Foundit-Jobs-Scraper | 60 | $0.001 | $0.0005 | foundit.in |
| khadinakbar/foundit-jobs-scraper | 44 | $0.003 | $0.00005 | India, Singapore, Malaysia or Indonesia, one a run |
| seemuapps/india-tech-jobs-scraper | 25 | $0.004 | none | foundit.in among 3 Indian tech boards |
| scrapewise/foundit-scraper | 20 | $0.001 | none | 6 sites, one a run |
| scrapesage/foundit-scraper | 18 | $0.004 | none | 7 sites, one a run |
| data_daemon/foundit-jobs-scraper | 11 | $0.0008 | $0.001 | foundit.in |
| This actor | new | $0.0018, $0.0019 with details | none | all 9 sites, several in one run |

Where others are cheaper: data_daemon charges $0.0008 a job with the description included (plus a $0.001 start fee), and shahidirfan and scrapewise $0.001 a job, all for foundit.in or one site a run; getascraper's feed costs $0.00199 and also covers other Indian boards. Where others do more: memo23 adds coordinates and paid email and market add-ons, and themineworks and khadinakbar have a monitor mode that returns only jobs new since the last run. This actor costs 10% less per job than the most used actor made only for Foundit (themineworks) on the Starter plan, and less on every paid plan.

## Which inputs does it take?

Nothing is required. Type a job title and press Start, or press Start with the form empty.

| Field | What it does |
|---|---|
| Job titles to find (`searchTerms`) | One per line. A job matches when its title has every word: frontend also finds Front-End. A pasted foundit search link works too |
| Where the job is (`location`) | A city, state, country or region: Bangalore, Karnataka, India, Dubai, UAE, Gulf, Southeast Asia. Each goes to the site that lists it. Remote alone asks for remote jobs; next to other places it narrows nothing. Empty searches all nine sites |
| Experience (`experienceYears`) | 3, a range such as 2-5, 5+ for 5 or more, or fresher for 0: jobs whose range overlaps it. Jobs that state no experience are left out |
| Posted in the last (`postedWithin`) | 24 hours, 3 days, 7 days, 30 days, any time, or your own period such as 48 hours |
| Number of jobs (`maxJobs`) | How many, newest first: 100 by default, 0 for every match |
| Full details (`includeDetails`) | Adds the description as text and HTML, every place with its state and country, the qualifications and pay as numbers |
| Remote or hybrid (`workType`) | remote (foundit's work-from-home type, or Remote in the location or title) or hybrid (in the title) |
| Job type (`employmentType`) | full-time, part-time or contract, as foundit states them |
| Leave out words (`excludeTerms`) | Drops jobs whose title has these words, such as senior or intern |
| Match descriptions (`searchDescriptions`) | Keeps every job foundit's own search finds for your words in its skills and description, whatever the title |
| Job links to check (`jobUrls`) | Paste job links to check whether they are still open, instead of searching |

Example input:

```json
{
  "searchTerms": ["python developer"],
  "location": ["Bangalore", "Pune"],
  "experienceYears": "3",
  "postedWithin": "7 days",
  "maxJobs": 100
}
```

## What does the output look like?

One row per job, newest first. These rows are from a local run of the release candidate on 2026-11-08: python developer in Bangalore, 151 matching jobs, the 100 newest saved in 4 s.

| Job title (`title`) | Company name (`company`) | Job location (`location`) | Experience from (`experienceMin`) | Experience up to (`experienceMax`) | Posted on (`postedAt`) |
|---|---|---|---|---|---|
| Senior Python Developer - (Python with SSH mandatory), 6+yrs,Bangalore, Immediate Joiners only | Global Technologies | Bengaluru, India | 6 | 8 | 2026-11-07 |
| Assistant Manager - SQL and Python Developer | Bnp Paribas Bank | Bengaluru, India | 5 | 7 | 2026-11-06 |
| Senior Python Developer | SID Global Solutions | Bengaluru, India | 6 | 8 | 2026-11-06 |
| Python Full Stack Developer | ZeMoSo Technologies | Bengaluru, India | 5 | 8 | 2026-11-06 |
| Principal Application Solution Developer (Java & Python) | Oracle | Gurugram, Gurugram, Hyderabad, Bengaluru, Noida, India | 6 | 10 | 2026-11-05 |

One row as JSON:

```json
{
  "title": "Senior Python Developer - (Python with SSH mandatory), 6+yrs,Bangalore, Immediate Joiners only",
  "company": "Global Technologies",
  "location": "Bengaluru, India",
  "otherLocations": [],
  "workType": null,
  "employmentType": "full-time",
  "department": null,
  "salary": null,
  "postedAt": "2026-11-07T17:21:28Z",
  "expiresAt": "2026-12-06T18:30:00Z",
  "jobUrl": "https://www.foundit.in/job/senior-python-developer-python-with-ssh-mandatory-6yrs-bangalore-immediate-joiners-only-global-technologies-bengaluru-bangalore-india-69753511",
  "applyUrl": "https://www.foundit.in/job/senior-python-developer-python-with-ssh-mandatory-6yrs-bangalore-immediate-joiners-only-global-technologies-bengaluru-bangalore-india-69753511",
  "status": "open",
  "platform": "foundit",
  "companySlug": "global-technologies-499568",
  "jobId": "69753511",
  "checkedAt": "2026-11-08T01:55:55+00:00",
  "experienceMin": 6,
  "experienceMax": 8,
  "site": "foundit.in",
  "skills": ["Report Generation", "SSH Paramiko", "log parsing", "C++", "Robot Framework", "Python", "Pytest"],
  "industry": null,
  "employerType": "company",
  "jobSource": "syndicated",
  "applicants": 0,
  "refreshedAt": "2026-11-07T17:21:28Z"
}
```

Full details add `description`, `descriptionHtml`, `qualifications`, `salaryMin`, `salaryMax`, `salaryCurrency`, `salaryPeriod`, `city`, `region`, `country` and `countryCode`, and give `location` and `otherLocations` with each place's state. A checked link that is closed or not found comes back with its `status` and link, and the other fields empty. A run also writes an `OUTPUT` record: how many country sites were read, how many jobs matched and were saved, and any notes on how your input was read.

## How fast is it?

A search of 100 jobs takes a few seconds: one to ten calls to foundit, one per site and 100 jobs. Measured locally on 2026-11-08, from start to finish: the 100 newest jobs from all nine sites in 4 s; 5,000 jobs in under a minute; in 51 s the 9,600 newest engineer jobs foundit shows for India, of which the 7,914 with engineer in the title were saved; and every job foundit shows on all nine sites, 72,668, in 7 minutes. Searches peaked at 80 to 130 MB of memory, the every-job run at 300 MB. Full details read each saved job once more, at about 2 jobs a second, so 100 jobs with details take about a minute (300 took 151 s). A state (Karnataka) opens each candidate job for its state, at the same pace. foundit's network refuses an address that calls too fast, so the run keeps to about 2 calls a second and waits when it is refused, and a foundit outage that outlasts the retries is named in the run's message (one site answered 503 for a while during our tests: the run saved the jobs it had read and said which site failed).

## Common questions

### Is foundit the same as Monster India?

Yes. foundit is the new name of Monster India (monsterindia.com) and of Monster's Gulf, Singapore, Philippines, Malaysia, Indonesia and Hong Kong sites; Thailand and Vietnam still run as monster.co.th and monster.com.vn on the same platform. Foundit Jobs Scraper searches all nine, and old monsterindia.com and monstergulf.com links are read as the same jobs.

### Which countries and sites does it cover?

Foundit Jobs Scraper covers foundit.in (India), founditgulf.com (the Gulf: UAE, Saudi Arabia, Qatar, Kuwait and Bahrain, also Egypt), foundit.sg (Singapore), foundit.com.ph (the Philippines), foundit.my (Malaysia), foundit.id (Indonesia), foundit.hk (Hong Kong, also Taiwan and China), monster.co.th (Thailand) and monster.com.vn (Vietnam). Leave Where the job is (`location`) empty to search all nine, or type places to search only their sites; every row says its `site`.

### Which posting date does it use?

Foundit Jobs Scraper uses the moment foundit first listed the job, for the posting date, the newest-first order and the Posted in the last filter: the date foundit's own job page gives Google as datePosted. foundit's list shows "Posted 5 hours ago" from the last listing instead, which an employer's renewal resets, so an old job looks new; that time comes as `refreshedAt`. On 2026-11-08, 12 of the 2,000 newest foundit.in jobs were renewals.

### Why are most jobs syndicated?

foundit copies a large share of its jobs from other job sites, mostly LinkedIn: about 98% of the newest jobs on every site on 2026-11-08. Foundit Jobs Scraper keeps them, says so in `jobSource` (syndicated, or foundit for jobs the employer posted on foundit) and puts the original apply link in `applyUrl`. To keep only foundit's own jobs, filter the rows on `jobSource` = foundit; foundit's search has no such filter, so a run cannot ask for it.

### Why does Mumbai not include Thane?

Foundit Jobs Scraper keeps the jobs whose location names the place you typed, by foundit's own place list, so Bangalore finds Bengaluru and Gurgaon finds Gurugram. foundit's own search widens a city to its neighbours and adds remote jobs, and those are left out here. Type each city you want, one per line: Mumbai, Thane, Navi Mumbai.

### How do I filter by experience?

Type your years in Experience (`experienceYears`): 3 keeps the jobs whose range holds 3 years, 2-5 the jobs whose range overlaps 2 to 5, 5+ five years or more, and fresher 0. foundit stores 0 to 0 years when the employer states none (its job page then says 0 - 1 years), and Foundit Jobs Scraper leaves those rows' experience empty and out of an experience search: 44% of the 5,000 newest jobs on 2026-11-08, on India and the other sites alike.

### Why did my run find nothing?

When a run saves no job, Foundit Jobs Scraper says why in its message and in the `nearMisses` part of the `OUTPUT` record. If foundit's own search had jobs with your words but one filter alone left them out, the message names it and how to loosen it, such as "the years of experience alone left out 242. To see them, type a wider range of years or leave it empty." If foundit's search found nothing at all inside your filters, it says "foundit has no job with your words inside your other filters", and if no job title had your words, it says so and suggests fewer words or Match descriptions. On 2026-11-08 an engineer search in Thailand for freshers saved 16 jobs, and 242 more had the words but stated no experience, so the experience filter alone left them out.

### Does it need a login, a proxy or an API key?

Foundit Jobs Scraper needs no login, no proxy and no foundit key: it reads the same public search that foundit's own search page reads, sending the headers that page sends. You need only an Apify account.

### Does it work on Apify's free plan?

Foundit Jobs Scraper works on Apify's free plan at the base price, $0.0018 a job with no start fee. The free $5 monthly credit pays for about 2,700 jobs.

### How often should I run it?

Running Foundit Jobs Scraper once a day keeps a job feed fresh: set Posted in the last (`postedWithin`) to 24 hours and Number of jobs (`maxJobs`) to 0 to get every job first listed that day for your search. Set the run up under Schedules in Apify Console, and match rows on `jobId` to skip jobs you already have.

### How do I check a list of job links?

Foundit Jobs Scraper checks whether foundit job links are still open when you paste them into Job links to check (`jobUrls`), one per line, instead of searching. Links of all nine sites work, and so do old monsterindia.com links. Each link comes back as one row: open with the job's fields, or closed or not found with its link; two links to the same job give one row.

### How do I call it from the API, Python, JavaScript, n8n or an AI agent?

Foundit Jobs Scraper runs from the Apify API, Python, JavaScript, n8n, Make or an AI agent over MCP. Each way uses your Apify token (Apify Console, Settings, API & Integrations) and takes the input as JSON keyed by the field names, such as `searchTerms` and `maxJobs`.

**API.** One call runs the actor and returns its rows (Apify waits up to 300 seconds; use a client below for bigger runs):

```bash
curl -X POST "https://api.apify.com/v2/acts/anshumanatrey~foundit-jobs-search/run-sync-get-dataset-items" \
  -H "Authorization: Bearer <YOUR_APIFY_TOKEN>" \
  -H "Content-Type: application/json" \
  -d '{"searchTerms": ["python developer"], "location": ["Bangalore"]}'
```

**Python** (`pip install apify-client`):

```python
from apify_client import ApifyClient

client = ApifyClient("<YOUR_APIFY_TOKEN>")
run = client.actor("anshumanatrey/foundit-jobs-search").call(run_input={"searchTerms": ["python developer"], "location": ["Bangalore"]})
for row in client.dataset(run.default_dataset_id).iterate_items():  # apify-client 3+; on 2.x use run["defaultDatasetId"]
    print(row["title"], row["company"], row["location"], row["experienceMin"], row["jobUrl"])
```

**JavaScript** (`npm install apify-client`):

```js
import { ApifyClient } from 'apify-client';

const client = new ApifyClient({ token: '<YOUR_APIFY_TOKEN>' });
const run = await client.actor('anshumanatrey/foundit-jobs-search').call({ searchTerms: ['python developer'], location: ['Bangalore'] });
const { items } = await client.dataset(run.defaultDatasetId).listItems();
for (const row of items) console.log(row.title, row.company, row.location, row.experienceMin, row.jobUrl);
```

**n8n and Make.** In n8n, add the Apify node, pick Run an Actor and get dataset, choose this actor and paste the input JSON: the rows come out as n8n items. In Make, the Apify app's Run an Actor and Get Dataset Items modules do the same.

**AI agents (MCP).** Add `https://mcp.apify.com?tools=anshumanatrey/foundit-jobs-search` to your MCP client and sign in with Apify, or send `Authorization: Bearer <YOUR_APIFY_TOKEN>`. The agent gets this actor as a tool and sees every input field by its JSON key.

### Am I charged for closed jobs?

Foundit Jobs Scraper charges for a closed job only when you paste its link to check. A search returns open jobs only, and a pasted link that turns out closed or not found is one Job row, because it was checked and answered.

### Is it legal to use?

Foundit Jobs Scraper reads public job postings, the ones foundit shows any visitor without a login. You are responsible for how you use the data, including each site's terms and the privacy laws that apply to you.

## Limitations

- foundit shows the 9,600 newest jobs of one search per site; a broader search returns at most that many from each site, newest first, with a note. Split it by place, period or experience to reach older jobs.
- About 98% of the newest jobs are copied from other sites (mostly LinkedIn) and carry what that site gave: experience on a little over half of them, pay on very few, industry rarely.
- Pay is shown on about 40% of Singapore's newest jobs and 1% or less on the other sites; an amount the employer hides stays hidden.
- Qualifications come only with jobs posted on foundit itself that list them: none of the 350 rows with details in our test runs (mostly syndicated jobs) had any.
- foundit does not say which jobs are on site, so there is no onsite filter; hybrid comes only from a title that says so.
- foundit has no internship or temporary job type: type intern in Job titles to find instead.
- A place must be on foundit's place list, or a country, region or state: an old name such as Bombay finds nothing, and the run says so.
- A state is not in foundit's job list, so a state search opens each candidate job for its state, at about 2 jobs a second.
- A two-word title is searched by foundit nearly as a phrase: python developer finds 186 Bangalore jobs where python finds 8,659.
- For a checked link, foundit gives the first-listed date only as text such as 8 days ago, so it is exact to the day.
- Job titles and descriptions come in the employer's language, mostly English.

## Who maintains it?

Built and maintained by **Anshuman Atrey** ([@AnshumanAtrey](https://github.com/AnshumanAtrey)), who publishes a portfolio of data and OSINT actors on Apify Store. For a feature request or a bug, message [LinkedIn](https://linkedin.com/in/anshumanatrey) (fastest), open an issue on the GitHub repo, or write through [atrey.dev](https://atrey.dev).

## Sibling actors

| Actor | What it searches |
|---|---|
| [Greenhouse Jobs Scraper](https://apify.com/anshumanatrey/greenhouse-jobs-search) | Jobs from every company on Greenhouse, searched live |
| [Lever Jobs Scraper](https://apify.com/anshumanatrey/lever-jobs-search) | Jobs from 2,300+ companies on Lever (jobs.lever.co), searched live |
| [Workday Jobs Scraper](https://apify.com/anshumanatrey/workday-job-search) | Jobs from every company on Workday (myworkdayjobs.com), searched live |
| [SmartRecruiters Jobs Scraper](https://apify.com/anshumanatrey/smartrecruiters-jobs-search) | Jobs from 2,900+ companies on SmartRecruiters, searched live |
| [Workable Jobs Scraper](https://apify.com/anshumanatrey/workable-job-search) | Jobs from every company on Workable, in one search |
| [Ashby Jobs Scraper](https://apify.com/anshumanatrey/ashby-jobs-search) | Jobs from every company on Ashby (jobs.ashbyhq.com), searched live |
| [Cornerstone Jobs Scraper](https://apify.com/anshumanatrey/cornerstone-jobs-search) | Jobs from every company on Cornerstone (csod.com), searched live |
| [Deel Jobs Scraper](https://apify.com/anshumanatrey/deel-jobs-search) | Jobs from every company on Deel ATS (jobs.deel.com), with pay |

For the people behind a company: [LinkedIn Profile Finder](https://apify.com/anshumanatrey/linkedin-harvester) turns an email into a public LinkedIn profile.

## Documentation

- Apify Store: https://apify.com/anshumanatrey/foundit-jobs-search
- GitHub repo: https://github.com/AnshumanAtrey/foundit-jobs-search (MIT license, see [LICENSE](LICENSE))
- The engine behind it: https://github.com/AnshumanAtrey/ats-jobs-engine

## Last updated

2026-11-08 (version 1.0)

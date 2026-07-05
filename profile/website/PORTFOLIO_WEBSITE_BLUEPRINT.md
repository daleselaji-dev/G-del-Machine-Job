# Portfolio Website Blueprint

status: ACTIVE_WEBSITE_BLUEPRINT  
version: v0.1  
created_at: 2026-06-28  
last_updated: 2026-06-28  
related: `profile/CAREER_EVIDENCE_DATABASE.md`, `profile/ZHIPU_AI_GAME_OVERSEAS_OPERATIONS.md`, `profile/resumes/ZHIPU_AI_GAME_OPERATIONS_RESUME_V1.md`

> This is the single source of truth for the personal website map, build workflow and design lessons from award-winning portfolio/site references. The website is not a raw online resume. It is a public capability showroom with a separate private interview room.

## 1. Core decision

Build the website as three layers:

1. **Public portfolio** — shows capability, taste, project quality, thinking process and sanitized artifacts.
2. **Semi-private interview room** — shared only during applications; contains targeted resume versions, deeper metrics and evidence packs.
3. **Private archive** — raw evidence, screenshots, account links, client/KOL identities, internal details and full chronology; never indexed publicly.

The public site should answer:

- What kinds of problems can I solve?
- What kind of work quality and taste do I have?
- How do I think, iterate and communicate?
- Why am I credible for Agent/FDE, overseas game/community growth, marketing and international commercialization?

The public site should not expose:

- phone number, WeChat, home address, ID documents or full private timeline;
- raw internal screenshots, customer/KOL/private-chat information or confidential documents;
- exact account links or unreleased project names unless explicitly approved.

## 2. Website positioning

### Public English line

> AI Agent · Overseas Growth · Game Community

### Public Chinese line

> AI Agent / 海外增长 / 游戏社区运营

### One-sentence narrative

> I build workflows, content and communities that help early products reach real users.

### Chinese explanation

> 我关注AI Agent、海外游戏社区和技术产品国际化，擅长将复杂产品转化为用户可理解、可参与、可增长的内容与运营系统。

## 3. Site map

```text
/
├── Home
│   ├── positioning
│   ├── selected projects
│   ├── capability tags
│   └── contact by email/form only
├── /agent
│   ├── G-del Machine Job
│   ├── Customer Intelligence Agent
│   ├── workflow / memory / tools / evals
│   └── bad cases and iteration log
├── /game-growth
│   ├── ACE simulation-game community growth
│   ├── platform strategy: Discord / Reddit / X / TikTok / Instagram / YouTube / Facebook
│   ├── KOL and game-media collaboration
│   └── Zoooo overseas cold-start case
├── /marketing-events
│   ├── reading-club poster design
│   ├── offline reading-club planning
│   ├── campaign copy and social posts
│   └── event review and user feedback
├── /international-growth
│   ├── India market 0→1
│   ├── South America localized campaign
│   ├── Top-150 customer-intelligence database
│   └── partner enablement / English communication
├── /writing
│   ├── public essays
│   ├── product teardowns
│   ├── game/community observations
│   └── English samples
└── /private-interview-room
    ├── noindex
    ├── password or hidden link
    ├── targeted resume downloads
    ├── deeper case metrics
    ├── evidence screenshots with masking
    └── role-specific interview packets
```

## 4. Public vs private rule

| Content type | Public site | Private interview room | Never publish |
|---|---|---|---|
| Role positioning | yes | yes | - |
| Project summaries | yes, sanitized | yes, detailed | - |
| Resume PDF | no public download by default | yes | - |
| Phone / WeChat | no | only if necessary | avoid indexing |
| Email | dedicated public email/form | yes | - |
| Client/KOL names | anonymized | selective, masked or permission-based | private identities |
| Internal docs | no | only redacted screenshots if needed | contracts, raw chats, confidential files |
| Metrics | rounded / scoped | detailed with context | raw dashboards if sensitive |
| GitHub/source | public demos only | private repos if needed | secrets, tokens, private data |

## 5. Case-page template

Every public project page should use this structure:

```text
1. One-line summary
2. Problem / context
3. My role
4. Constraints
5. Process
6. Artifacts
7. Result
8. What I learned
9. What I would improve next
10. Privacy note / what is intentionally omitted
```

This is the bridge between recruiters and internet readers:

- Recruiters get role, scope, metrics and outcome.
- Hiring managers get process and decision quality.
- Open-source / excellent internet readers get artifact quality, clarity and reusable thinking.

## 6. Page priority

### P0 — Website skeleton

- Home
- Agent
- Game Growth
- Marketing & Events
- International Growth
- Private Interview Room shell

### P1 — Three flagship cases

1. `G-del Machine Job` — Agent workflow and evaluation case.
2. `ACE Simulation Game Community Growth` — overseas game/community/KOL case.
3. `Reading Club Poster + Offline Event` — marketing/design/event planning case.

### P2 — Supporting cases

4. India market 0→1.
5. South America localized campaign.
6. Top-150 customer-intelligence database.
7. Zoooo overseas cold-start strategy.

## 7. Build workflow

### Step 1 — Content inventory

Create a content table for each project:

```text
project name
role direction served
public value
private evidence
privacy risk
available artifact
missing artifact
next action
```

### Step 2 — Privacy classification

For every asset, mark:

- `PUBLIC_OK`
- `PUBLIC_AFTER_MASKING`
- `PRIVATE_INTERVIEW_ONLY`
- `DO_NOT_PUBLISH`

### Step 3 — Case writing

Write every case in the same pattern:

```text
Problem → My role → Process → Artifact → Result → Learning → Next iteration
```

### Step 4 — Design pass

Apply the visual principles in section 8. Keep the first version simple, clear and fast.

### Step 5 — Recruiter pass

Check whether a recruiter can understand in 30 seconds:

- target direction;
- top three projects;
- what you actually did;
- how to contact you.

### Step 6 — Hiring-manager pass

Check whether a manager can understand in 3 minutes:

- problem difficulty;
- your decision process;
- what was measured;
- what remains uncertain;
- how your experience maps to the role.

### Step 7 — Internet-quality pass

Check whether a strong internet reader sees:

- clear concept;
- sharp taste;
- useful process;
- credible artifacts;
- no generic self-promotion.

## 8. Award-winning website / Awwwards-style lessons

These lessons should guide the site, but not turn it into an over-designed showpiece.

### 8.1 What to borrow

- **One strong concept:** the site should feel like one coherent product, not a list of resume sections.
- **Hero clarity:** the first screen must tell viewers who you are and what kind of work you do.
- **Editorial rhythm:** mix short statements, visual artifacts, case blocks and process diagrams.
- **Strong art direction:** typography, spacing and color should feel intentional.
- **Motion with purpose:** use transitions only to explain hierarchy or reveal process, not to decorate.
- **Case-study depth:** every pretty surface must lead to process, decision and result.
- **Signature interaction:** one small memorable interaction is enough, such as a role switcher or case-map view.
- **High screenshot quality:** mockups, diagrams and artifacts should be cleaned, masked and visually consistent.
- **Narrative scrolling:** each flagship case should feel like a story: context → obstacle → action → result → reflection.
- **Fast loading:** strong design cannot come at the cost of slow or broken loading.

### 8.2 What not to copy blindly

- Do not hide content behind too much animation.
- Do not make navigation mysterious.
- Do not use huge videos or heavy WebGL before the content is strong.
- Do not prioritize cool effects over recruiter readability.
- Do not publish sensitive data just to make a case look more “real.”
- Do not build a portfolio that looks more senior than the actual evidence can support.

### 8.3 Suitable design direction for this candidate

Use a style between:

- **product case study** — precise, structured, evidence-aware;
- **editorial portfolio** — visually clean, thoughtful, good typography;
- **light technical notebook** — shows workflows, diagrams, evals and iteration.

Avoid:

- overly flashy creative-agency portfolio;
- plain PDF-resume website;
- anonymous developer blog with no personality.

## 9. Flagship case requirements

### 9.1 G-del Machine Job — Agent/FDE case

Must show:

- problem: job search has repeated retrieval, evidence, role-mapping and memory problems;
- workflow: role discovery → company/JD research → evidence matching → action decision → memory writeback;
- system boundaries: no unsupported claims, no uncontrolled self-modification, separate public/private evidence;
- artifacts: skill map, memory model, evaluator, example run, failure case;
- metrics to add: unsupported-claim rate, task completion, time saved, bad-case count, iteration improvement.

Public version can use synthetic or sanitized job/candidate examples.

### 9.2 ACE Simulation Game Community Growth — game/community case

Must show:

- genre: farming/simulation/cozy game;
- role: content + community + social platforms + creator collaboration;
- platforms: TikTok, Instagram, Discord, Reddit, X, YouTube, Facebook;
- cadence: 10–15 posts/videos per month, around two community activities per month;
- result: interaction rate about 2×, 1,000+ followers, Discord community 0→150 during operating period;
- KOL/media: creator/media discovery, selection, outreach, content direction and execution follow-up;
- privacy: mask account names, user avatars, creator names and internal screenshots unless permitted.

### 9.3 Reading Club Poster + Offline Event — marketing/design case

Must show:

- poster design objective;
- target audience;
- visual hierarchy: title, time, place, hook and CTA;
- design iterations;
- event planning: topic selection, venue, registration, moderation, flow and review;
- result: attendance, feedback, reposts, follow-up discussions if available;
- privacy: blur attendee faces/names unless permission exists.

### 9.4 International Growth — commercial case

Must show:

- market-entry logic, not only sales numbers;
- research method: LinkedIn, Google, WhatsApp, import/export data, OSINT;
- pipeline and prioritization;
- negotiation and partner enablement;
- content/localization support;
- result with rounded or scoped metrics;
- privacy: remove customer names, contracts, quotes and private messages.

## 10. Technical implementation options

### Fastest MVP

- Notion / Framer / Webflow / Typedream
- Pros: fast, visual, low engineering burden
- Cons: less control, weaker technical credibility for Agent/FDE

### Balanced option

- Next.js + Tailwind + MDX
- Pros: can show technical/product taste, reusable case templates, easy privacy split
- Cons: requires implementation effort

### Recommended route

Use **Next.js + MDX** if the site is meant to support Agent/FDE credibility. Use a simple visual system first; do not over-engineer animations before case content exists.

## 11. Repository / content architecture suggestion

For a future website repo:

```text
portfolio-site/
├── app/
│   ├── page.tsx
│   ├── agent/page.tsx
│   ├── game-growth/page.tsx
│   ├── marketing-events/page.tsx
│   ├── international-growth/page.tsx
│   └── private/page.tsx
├── content/
│   ├── cases/
│   │   ├── gdel-machine-job.mdx
│   │   ├── ace-game-community.mdx
│   │   ├── reading-club-poster-event.mdx
│   │   └── india-market-entry.mdx
│   ├── notes/
│   └── private/
├── components/
│   ├── CaseCard.tsx
│   ├── CaseHeader.tsx
│   ├── EvidenceBadge.tsx
│   ├── PrivacyNotice.tsx
│   └── RoleSwitcher.tsx
├── public/
│   ├── images/
│   │   ├── sanitized/
│   │   └── placeholders/
│   └── downloads/
│       └── public-one-page-summary.pdf
└── README.md
```

## 12. First build checklist

- [ ] Decide public name: `David Yu`, `David Y.`, or Chinese + English.
- [ ] Create a public email/form separate from private phone/WeChat.
- [ ] Draft Home page with one sentence, four directions and three selected cases.
- [ ] Draft `G-del Machine Job` case using sanitized examples.
- [ ] Draft `ACE Simulation Game Community Growth` case.
- [ ] Draft `Reading Club Poster + Offline Event` case.
- [ ] Collect 6–10 visual assets and classify privacy level.
- [ ] Create a private interview room and add `noindex`.
- [ ] Prepare a role-specific resume download only for private sharing.
- [ ] Add one simple interaction: role filter / case map / evidence-level badge.
- [ ] Run recruiter 30-second test.
- [ ] Run hiring-manager 3-minute test.
- [ ] Run privacy leak review.

## 13. Personal website rule of thumb

> Public site = capability, taste, process and sanitized artifacts.  
> Private room = proof, details, metrics and resume.  
> Archive = raw evidence and sensitive context.

This lets the website serve interviewers, recruiters, strong internet readers and future collaborators without exposing unnecessary private information.

## 14. Change log

### 2026-06-28 — v0.1

- Created the central website blueprint.
- Combined site map, build workflow, privacy model and award-winning site design lessons.
- Defined flagship cases for Agent/FDE, game/community growth, marketing/events and international growth.
- Added implementation architecture and first-build checklist.

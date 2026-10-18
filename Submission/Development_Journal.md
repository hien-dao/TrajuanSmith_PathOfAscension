# Path of Ascension — Development Journal

**Project:** Path of Ascension — Quest Explorer with Adventure Pack  
**Course:** CSC 4370 — Web Programming  
**Team members:** Trajuan Smith and Hien Dao  
**Project period:** October 2026  
**Format:** Development phases rather than a day-by-day timesheet

> This journal summarizes the team's documented development decisions and milestones. It does not assign exact dates, hours, or individual testing responsibilities where those records are not available. See the team's Trello board, Git history, and Team Introduction page for additional project-management evidence.

## Phase 1 — Topic selection and planning

**Goal:** Design a multi-page HTML/CSS website that meets the Quest Explorer track and Adventure Pack extension.

We selected a xianxia-inspired cultivation adventure because the genre lends itself to exploring regions, accepting missions, and tracking progression. We named the project **Path of Ascension**. The planned visitor journey connected a Home page, World Map, Mission Journal, and Team/About page.

The proposal work included page concepts/wireframes, intended user flows, accessibility considerations, and a plan to check usability, responsiveness, and markup quality. We aimed to create the feel of a small adventure interface while keeping core interactions in HTML and CSS rather than JavaScript.

**Outcome:** A four-page site concept with consistent navigation, a fantasy visual theme, region exploration, mission details, and an Adventure Pack journey tracker.

## Phase 2 — Team organization and shared structure

**Goal:** Divide ownership while keeping the website consistent.

| Contributor | Primary responsibilities |
| --- | --- |
| **Trajuan Smith** | World Map and Mission Journal pages; region links, mission selection, mission progress controls, and page-specific styling |
| **Hien Dao** | Home and Team/About pages; Journey Tracker, character/developer profiles, cultivation hierarchy, and page-specific styling |
| **Shared** | Navigation integration, design consistency, review, testing, presentation, and submission preparation |

We used **Git and GitHub** to develop on separate feature branches and integrate work into the main project. A shared `css/styles.css` file holds common styles, while page-specific stylesheets keep individual page rules easier to maintain. We used a **Trello Kanban board** to track tasks through stages such as Backlog, To Do, In Progress, Review, and Done.

**Board:** https://trello.com/b/I5b5j5fD/path-of-ascension-project-1

**Outcome:** Clear ownership of the four main pages, shared navigation, and an organized approach to merging work.

## Phase 3 — Home and Team page development

**Primary contributor:** Hien Dao

The Home page introduces the cultivation setting and guides visitors into the site. Its **Journey Tracker** covers four regions: Starter Village, Grey Spirit Forest, Blue Mountain Sect, and Ancient Azure Ruins. Radio-button-driven CSS states allow visitors to select regions and view corresponding information. A visual progress indicator reinforces the Adventure Pack theme.

The Team page introduces fictional cultivator characters, developer profiles, and a cultivation realm hierarchy. CSS Grid layouts, including responsive `auto-fit`/`minmax` patterns, help the profiles adapt to available space. Decorative CSS animations support the fantasy setting.

**Outcome:** A welcoming entry point, progression-themed interaction, and a Team page explaining both the fictional world and developer contributions.

## Phase 4 — World Map development

**Primary contributor:** Trajuan Smith

The World page presents four regions using cards with imagery, descriptions, difficulty information, and availability indicators. **Starter Village** and **Grey Spirit Forest** are available; **Blue Mountain Sect** and **Ancient Azure Ruins** are shown as locked.

We chose **CSS Grid** for the region cards because it maintains consistent rows and columns. The layout uses two columns on larger screens and changes to one column at widths of **768px or less**. Available regions link to their corresponding missions.

### Design revision: remove duplicate progression display

An early World page design included a separate checkpoint/journey timeline. Because the Home page already had the Journey Tracker, we removed the duplicate from World and retained the region exploration cards and availability states. This gave the two pages more distinct purposes and reduced unnecessary styling.

### Accessibility fix: locked regions

Initially, locked region controls were `<a>` elements styled to look disabled. Styling did not stop those links from receiving keyboard focus. We changed locked controls to **non-interactive `<span>` elements** while keeping available regions as links. This made the locked state more accurate and avoided unnecessary Tab stops.

**Outcome:** A responsive region explorer with clear available/locked states and direct navigation to missions.

## Phase 5 — Mission Journal development

**Primary contributor:** Trajuan Smith

The Mission page shows available and locked missions, with descriptions, objectives, rewards, difficulty information, and status indicators. Visitors can select available missions and move through **Available → Ongoing → Completed** states.

### CSS-only mission selection

Available mission selectors are links to matching detail article IDs. The details are hidden by default; the CSS `:target` selector reveals the selected mission. A World page link such as `mission.html#cultivators-awakening` can therefore open the Mission page with the relevant mission selected, without JavaScript.

### CSS-only mission progression

Hidden checkbox inputs and CSS selectors such as `:checked` and `:has()` update mission controls and visible status labels. Selecting **Take Mission** changes the displayed action to **Complete Mission**; completing the mission updates the status and completion message.

### Scope decision

We considered automatically unlocking later regions as missions were completed but did not include that behavior in the final prototype. Locked regions and missions remain static. Mission progress is also **not saved across reloads** because the site has no JavaScript persistence layer, backend, or database.

**Outcome:** A connected mission experience with direct-link selection and CSS-only progression controls.

## Phase 6 — Styling, responsiveness, and accessibility

**Shared work, with page-specific implementation by each developer**

We used a dark navy palette with cyan and gold accents to reinforce the cultivation theme. Shared styling supports consistent navigation and visual treatment across pages. CSS Grid organizes card layouts; Flexbox aligns navigation and other interface elements. Media queries adapt the layouts to narrower screens.

Accessibility-related decisions included semantic landmarks (`header`, `nav`, `main`, `section`, `article`, `footer`), meaningful image alternatives, keyboard-operable available controls, non-interactive locked states, and CSS support for `prefers-reduced-motion`. We also checked the site's keyboard navigation manually.

**Outcome:** A consistent multi-page design that adapts to desktop, tablet, and mobile viewports.

## Phase 7 — Debugging, testing, and validation

**Goal:** Check the finished website and correct defects before submission.

The team checked the site with Chrome DevTools at desktop, tablet, and mobile widths. The reported results showed readable layouts without unwanted horizontal scrolling or overlapping content. Manual checks also confirmed that navigation between the four main pages, World-to-Mission links, mission selection, mission status changes, locked states, and the Home Journey Tracker worked as expected.

Keyboard testing with **Tab**, **Shift+Tab**, and **Enter** passed for the checked interactive elements.

### HTML validation defect and resolution

W3C HTML validation initially identified four invalid `<p>` elements nested inside Journey Tracker `<label>` elements in `index.html`. We replaced those paragraphs with `<span>` elements and revalidated the markup. The final reported result was **no remaining HTML validation errors** across the HTML files.

All CSS stylesheets were also checked with the **W3C CSS Validator** and reported as passing.

**Testing evidence:** See `QA_Testing.md` in the same `submission` folder for the test matrix, results, and testing limitations. The QA report does not claim separate Firefox/Safari or peer-testing results that were not confirmed.

**Outcome:** The documented responsive, functional, keyboard, HTML, and CSS checks passed after the markup fix.

## Phase 8 — Documentation, presentation, and deployment

The team prepared the project README, proposal materials, wireframes, critical-thinking Q&A, presentation slides and speaking notes, and a separate **Team Introduction** page with project-management information. The presentation demonstrates the visitor flow, CSS-only interactions, accessibility choices, debugging decisions, and Trello board.

The website was deployed to the course's **CODD** hosting environment. GitHub contains the project source and supporting submission materials. The final iCollege submission uses a text file containing the CODD, GitHub, and YouTube presentation links.

**Outcome:** A deployed, documented project ready for the course submission process.

## Phase 9 — Reflection and possible improvements

This project provided practice with semantic HTML, responsive CSS layouts, CSS-only interactive states, accessibility, Git collaboration, and debugging with validators. The main technical tradeoff was creating a mission interface without JavaScript: CSS selectors can provide meaningful interactions, but they cannot persist progress across visits or implement a full unlock system on their own.

If we continued the project, possible improvements would include persistent mission progress, automatic region unlocking, more playable missions, and further accessibility and cross-browser testing. The Mission page's repeated progress-state CSS could also be refactored into more reusable rules, followed by regression tests for both available missions.

## Supporting project records

- **Project proposal and wireframes:** Initial page plans and user flows
- **Git/GitHub history:** Branches, integration, and code changes
- **Trello board:** Task tracking and team coordination
- **`QA_Testing.md`:** Confirmed responsive, functional, keyboard, and W3C validation results
- **Critical-thinking Q&A and presentation:** Design rationale, technical demonstrations, and lessons learned


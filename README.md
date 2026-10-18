# Path of Ascension 🏔️

**A Xianxia-Inspired Quest Explorer Website**  
**Course:** CSC 4370 Web Programming  
**Project:** Project 1 — HTML & CSS  
**Team:** Trajuan Smith and Hien Dao

## 📖 About the Project

Path of Ascension is a front-end web development project inspired by *xianxia*, a Chinese fantasy genre centered on cultivation, spiritual energy, martial arts, and the pursuit of immortality.

Visitors can explore a fictional cultivation world, discover regions, review missions, interact with mission progress controls, and learn about the characters and developers. The project emphasizes HTML5, CSS3, responsive layouts, and accessible markup, with core interactions implemented without JavaScript.

## ✨ Website Features

### 1. Home (`index.html`)
- Introduces the cultivation world and the adventure.
- Features a journey tracker with Starter Village, Grey Spirit Forest, Blue Mountain Sect, and Ancient Azure Ruins.
- Presents region descriptions and visual journey progress.

### 2. World Map (`world.html`)
- Displays four cultivation regions with descriptions, difficulty information, and availability indicators.
- Provides navigation from available regions to the corresponding missions.
- Distinguishes locked content from available links; locked items are not interactive links.
- Uses responsive region-card layouts.

### 3. Mission Journal (`mission.html`)
- Presents available and locked missions with objectives, difficulty information, and rewards.
- Supports mission selection and CSS-based mission status/progress interactions.
- Shows mission status changes and completion feedback.
- Keeps locked missions unavailable in this prototype; completing a mission does not automatically unlock another one.

**Featured missions:**
- The Cultivator's Awakening — Starter Village
- Spiritwood Investigation — Grey Spirit Forest
- Trial of the Inner Disciple — Blue Mountain Sect
- Secrets of the Azure Ancients — Ancient Azure Ruins

### 4. Team & Cultivation Realms (`team.html`)
- Introduces fictional cultivator characters and their cultivation ranks.
- Displays a cultivation pyramid from Mortal to Soul Formation.
- Includes short developer profiles, themed imagery, and CSS animations.

### Separate Team Introduction (`team-introduction.html`)

This is a **project documentation page**, separate from the four-page website experience. It records:
- Project overview and leadership responsibilities.
- Individual developer contributions.
- Team time tracking.
- Coordination and development workflow.

Its page-specific styles are in `css/team-introduction.css`.

## 🛠️ Technologies

- **HTML5:** Semantic page structure, forms/controls, and accessible content.
- **CSS3:** Responsive layouts, visual design, animations, state styling, and interactions.
- **CSS selectors and form controls:** Interactions without JavaScript for the core experience.
- **Git and GitHub:** Version control and collaboration.

## 🎨 Design and Accessibility Decisions

- **Consistent navigation:** Shared navigation and footer patterns connect the four main website pages.
- **Modular stylesheets:** `styles.css` holds shared styles; individual pages use their own CSS files.
- **Responsive layouts:** Grids and media queries adapt content for smaller screens.
- **Clear locked states:** Locked regions and missions are represented as non-interactive content rather than misleading active links.
- **Semantic and accessible markup:** Headings, section labels, descriptive image alternatives where appropriate, and ARIA attributes support navigation and understanding.
- **Reduced motion:** The Team page includes a `prefers-reduced-motion` rule to limit decorative animation for visitors who request it.

## 📁 Project Structure

```text
Path-of-Ascension/
├── index.html
├── world.html
├── mission.html
├── team.html
├── team-introduction.html
├── css/
│   ├── styles.css
│   ├── home.css
│   ├── world.css
│   ├── mission.css
│   ├── team.css
│   └── team-introduction.css
├── images/
└── README.md
```

Other project documentation or evidence files may be stored separately from the website's root folder.

## 🚀 Getting Started

**Published website link recorded in the original README:** [Path of Ascension on CODD](https://codd.cs.gsu.edu/~tsmith413/WebDev/Projects/Project01/TrajuanSmith_PathOfAscension/index.html)  


To run locally:

1. Clone or download the repository.
2. Keep the HTML files, `css/` directory, and `images/` directory in their relative locations.
3. Open `index.html` in a browser, or use a local development server in Visual Studio Code.
4. Navigate among Home, World, Mission, and Team.
5. Open `team-introduction.html` separately to view the team documentation.

## 👨‍💻 Team and Responsibilities

### Trajuan Smith — Project Leader; World Map & Mission Developer

Coordinated project responsibilities and integration; developed the World Map and Mission pages, region-to-mission navigation, responsive layouts, mission interactions, and accessibility improvements.

### Hien Dao — Homepage & Team/About Developer

Developed the Homepage and Team/About page, including the journey tracker, character profiles, cultivation realms, visual styling, and animations. Collaborated on project integration.

The separate Team Introduction page contains additional responsibilities, coordination details, and the team's recorded development hours.

## 🔄 Development Workflow

The team divided page ownership, developed assigned features, used Git branches for changes, and integrated completed work into the shared project. Development also included reviewing navigation, styling consistency, responsiveness, and project requirements.

## 🤖 AI Usage Disclosure

ChatGPT was used as a development and documentation assistant, including for explanations of HTML/CSS concepts, troubleshooting, accessibility and responsive-design suggestions, code-review guidance, and drafting/revising documentation such as the Team Introduction and README.

The team was responsible for choosing the final design, reviewing and adapting suggested code, integrating the pages, testing the site, and submitting the finished project. 

## 🎯 Learning Objectives

- Build a multi-page website with semantic HTML and CSS.
- Create a consistent fantasy-themed interface with responsive layouts.
- Implement useful interactions without relying on JavaScript.
- Apply accessibility principles to navigation, content, and interaction states.
- Organize styles and assets for maintainability.
- Practice collaborative development, version control, and documentation.

## ⚠️ Prototype Limitations

- Front-end prototype only; no backend or database.
- Mission progress is not persisted between sessions.
- Completing missions does not automatically unlock new regions or quests.
- No user accounts, multiplayer features, or game engine functionality.

## 📚 Credits and Acknowledgements

Created as an educational web development project. The fictional regions, missions, and cultivation progression form the project's fantasy setting. **Review all third-party images, fonts, and other assets and add their specific source links and attribution or license information where required.**

## 📄 License

Created for educational purposes. No separate open-source license is declared here. Third-party assets remain subject to their respective licenses and attribution requirements.

---

*Embark on your journey, overcome every trial, and walk the Path of Ascension.*

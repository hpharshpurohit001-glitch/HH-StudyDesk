# StudyDesk

**A first-semester study hub for B.Tech CSE students.**

**Live site:** https://hpharshpurohit001-glitch.github.io/HH-StudyDesk/

StudyDesk brings notes, previous papers, syllabus links, topic tracking, attendance planning, SGPA calculation and a focus timer into one responsive web page.

---

## Problem statement

First-semester B.Tech students often struggle with scattered study material. Notes, previous papers, syllabus links and practice questions live in different places, and students track attendance, grades and study progress by hand. This wastes time and makes it hard to see how prepared they really are.

**StudyDesk solves this with a single web application** where a student can find resources for every subject, track which topics are done, and plan attendance and SGPA without switching between tools.

## Features

| Feature | What it does |
| --- | --- |
| Subject cards | Seven first-semester subjects: Python, HTML, Mathematics, Physics, Orientation to Computing, Environmental Studies and Basic Electronics (ECE) |
| Topic tracker | Tick topics as you finish them, with a progress bar per subject and an overall progress ring |
| Search and filters | Search by subject or topic, and filter resources by type (notes, previous papers, syllabus, video lectures, practice) |
| Exam countdown | Pick the next exam date and see how many days are left |
| Attendance planner | Shows how many classes you can miss, or must attend, to reach your target percentage |
| SGPA calculator | Enter credits and grades to get an estimated SGPA |
| Focus timer | 25-minute focus blocks and 5-minute breaks, with a daily block counter |
| Add a resource | Save your own links to any subject |
| Dark and light mode | Follows the device setting and can be switched manually |
| Responsive design | Works on phones, tablets and laptops |

Progress, added links, the exam date and the theme are saved in the browser using `localStorage`, so no account or server is needed.

## Tech stack

- HTML5 for structure
- CSS3 (custom properties, grid, flexbox, media queries) for styling and theming
- Vanilla JavaScript for all logic
- GitHub for version control and GitHub Pages for hosting

## Project structure

```
HH-StudyDesk/
├── index.html    # the whole application (HTML, CSS and JavaScript)
└── README.md     # project documentation
```

## How to run locally

1. Download or clone this repository.
2. Open `index.html` in any modern browser.

No installation or build step is required.

## How it works

- Subject and topic data is stored in a JavaScript array. The page is rendered from it, so adding a subject means adding one object.
- Ticking a topic updates a saved state object, then redraws the progress bars and the progress ring.
- The attendance planner uses the formulas below, where `a` is classes attended, `t` is total classes held and `p` is the target percentage:
  - Classes you can still miss: `floor(a × 100 / p − t)`
  - Classes you must attend in a row: `ceil((p × t − 100 × a) / (100 − p))`
- SGPA is the credit-weighted average of grade points: `Σ(credits × grade points) / Σ(credits)`.

## Team

| HARSH PUROHIT | HIMANSHU SHEKHAWAT |


## Future scope

- User accounts and cloud sync so progress follows the student across devices
- A shared database so students can add and rate resources for everyone
- More semesters and branches
- Reminders for assignments and exams

## Disclaimer

StudyDesk is a student project. It is not run by or affiliated with Lovely Professional University. Topic lists and credits are common examples, so always confirm your official syllabus and schedule on UMS.

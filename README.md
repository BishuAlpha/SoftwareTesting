# Software Testing (CS6404) – Previous Year Questions with Solutions

A single-page study guide containing worked solutions to past exam papers for **Software Testing (CS6404)**.

## Contents

The guide covers three papers:

| Paper | Exam | Marks |
|-------|------|-------|
| A | End Sem 2024-25 | 50 |
| B | End Sem 2024-25 | 50 |
| C | End Sem 2024 (Spring 2023-24) | 100 |

Topics include:

- Equivalence class partitioning and boundary value analysis (including worst-case)
- Decision-table testing and cause-effect graphs
- Control flow graphs, cyclomatic complexity and independent paths
- Define-use-kill data-flow patterns
- Mutation testing and mutation score
- Integration testing (pair-wise, neighbourhood, bottom-up) and effort estimation
- Regression test minimisation and prioritisation
- Alpha, beta and acceptance testing
- Performance (non-functional) testing
- Test specifications, test logs and incident reports
- Use-case and class-level test patterns (extended use case, modal class, partition class)
- Scrum, agile testing life cycle and web testing

## Design & style

The page uses a **blueprint / retro-terminal** look: paper-like background, hard black rules and offset "pixel" shadows (`3px 3px 0`) on tables and diagrams.

### Fonts

| Role | Font | Used for |
|------|------|----------|
| Display | **VT323** (fallback: JetBrains Mono) | Headings, title, logo – retro terminal feel |
| Body | **Source Serif 4** (fallback: Source Serif Pro, Iowan Old Style, Georgia) | Question and solution text |
| Mono | **JetBrains Mono** (fallback: Consolas) | Code, tables, labels, buttons |

Fonts are loaded from Google Fonts.

### Colours

| Token | Light | Dark |
|-------|-------|------|
| Background `--bg` | `#fafaf5` | `#0a0d1a` |
| Ink / rules `--ink` | `#1a1a1a` | `#e8e6dc` |
| Accent `--blueprint` | `#3553ff` | `#6b8eff` |
| Code background `--code-bg` | `#efece0` | `#131830` |

All colours are CSS variables, so the theme switches by changing a `data-theme` attribute.

## Features & components

- **Sticky header** with logo, breadcrumbs, sidebar toggle (`≡`) and theme toggle.
- **Light / dark theme** – follows the system `prefers-color-scheme` on first visit, and the choice is saved in `localStorage`.
- **Collapsible sidebar table of contents** – grouped by paper, with *Expand* / *Collapse* all buttons and a scroll-spy that highlights the section you are reading (including the group header when collapsed).
- **Inline SVG diagrams** (`svg.cg`) – control flow graphs, cause-effect graphs and similar, themed with the page colours.
- **Tables** (`.tw`) – horizontally scrollable wrappers for decision tables, test cases and logs.
- **Callout notes** (`.note`) – highlighted boxes with a coloured left border for tips and remarks.
- **Original paper pages** – a collapsible "Show original question paper pages" section per paper, with lazy-loaded images.
- **Image lightbox** – click any paper page (`img.zoom`) to enlarge it; press `Esc` to close.
- **Math rendering** – formulas such as \(V(G)\) are typeset with MathJax.
- **Back-to-top button** – appears after scrolling 600px.
- **Responsive layout** – adapts below 980px width.
- **Print-friendly** – header, sidebar and back-to-top button are hidden when printing.

## Project structure

```
SoftwareTesting/
├── index.html                      # The study guide (open this)
├── index.deeplearning.bak.html     # Backup of an earlier/alternate version
├── PYQ/                            # Original question paper PDFs
│   ├── CS6404.pdf
│   ├── CS6404 (1).pdf
│   └── CS6404 (2).pdf
└── assets/pyq/                     # Figures from the papers (a-*, b-*, c-*)
```

## Usage

No build step is required. Open `index.html` in any modern browser:

```bash
start index.html
```

Or serve it locally:

```bash
python -m http.server 8000
```

then visit <http://localhost:8000>.

> An internet connection is needed for full rendering: math is typeset with
> [MathJax](https://www.mathjax.org/) and fonts are loaded from Google Fonts, both via CDN.

## Notes

- Each question has an anchor ID (e.g. `#a-q3`, `#b-q7`, `#c-q2`) so you can link directly to it; the table of contents is at `#contents`.
- The solutions are study aids written by hand; verify against your course material before relying on them in an exam.

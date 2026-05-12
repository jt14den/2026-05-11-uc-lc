# Git/GitHub for Librarians — Motivation Slides Prep
UC Library Carpentry | 2026-05-13 | Episode 1

Use cases scoped for librarians, information professionals, and MLIS students.
Ordered roughly by "aha" impact for this audience.

---

## Slide: The Problem (set up before any solution)

**Bullet points:**
- You've seen this folder: `report_FINAL.docx`, `report_FINAL2.docx`, `report_USE_THIS_ONE.docx`
- Works fine alone. Falls apart with collaborators, time, or anything that matters
- Libraries have always solved this for physical objects — we haven't solved it for digital work

**Image to use:**
- The "notFinal.doc" PhD Comics strip — classic opener, always lands
  - URL: http://phdcomics.com/comics/archive.php?comicid=1531
  - Already embedded in the LC Git lesson AIO page (safe to screenshot/reuse in teaching context)
- Or: show a real messy folder in Finder/Explorer

**Transition:** "Git is version control software. It solves this problem for any text-based file."

---

## Slide: Git vs. GitHub — Keep These Distinct

**Bullet points:**
- **Git** — software that runs on your machine, tracks changes locally, free and open source
- **GitHub** — a website that hosts Git repos remotely; adds web interface, collaboration tools
- Like: Git is the catalog system, GitHub is the building that houses it
- Alternatives exist: GitLab (common in European institutions), Bitbucket, Gitee

**Image to use:**
- The two-box diagram from the lesson: local machine ↔ GitHub (remote)
- Or draw it live on a whiteboard — works better than a slide for this one

---

## Slide: Your Library's Software Is Already Here

**Bullet points:**
- FOLIO (open source ILS) — 461 repos on GitHub, community-developed by libraries for libraries
- CollectionBuilder — digital exhibit framework, built on GitHub Pages, developed at U of Idaho Library
- ArchivesSpace, Omeka, Islandora, DSpace, Blacklight, VuFind — all open source, all on GitHub
- Bug reports, customizations, plugins — all happen through GitHub

**Links for live demo:**
- FOLIO: https://github.com/folio-org (461 repos, affiliated with Open Library Foundation)
- CollectionBuilder: https://github.com/CollectionBuilder/collectionbuilder-gh
- LC Git lesson itself: https://github.com/LibraryCarpentry/lc-git (578 commits, 69 forks)

**Image to use:**
- Screenshot of the FOLIO org page on GitHub — 461 repos is visually striking
- Or: CollectionBuilder-GH repo page

**Talking point:** "If your library runs FOLIO or is considering it, this is where that software lives. Understanding GitHub means you can participate."

---

## Slide: CollectionBuilder — Librarians Built This on GitHub

**Bullet points:**
- Create a digital exhibit from a spreadsheet + folder of images — hosted free on GitHub Pages
- Maps, timelines, search, tag clouds — generated automatically from your metadata CSV
- Version-controlled: every change to your exhibit is tracked, reversible, citable
- Real example: Idaho Queered — LGBTQ+ oral history collection at U of Idaho Library

**Links:**
- Demo: https://collectionbuilder.github.io/collectionbuilder-gh/
- Idaho Queered example: https://www.lib.uidaho.edu/queered/
- More examples: https://collectionbuilder.github.io/cb-examples/

**Image to use:**
- Screenshot of the Idaho Queered site (visual, clearly library work)
- Side by side: the GitHub repo + the live exhibit site

**Talking point:** "This is a library-built tool, maintained by librarians, used in production collections. The whole thing is a GitHub repo."

---

## Slide: This Lesson Is on GitHub

**Bullet points:**
- The lesson you're learning from right now is a GitHub repository
- 578 commits — every edit to every episode is tracked, with who changed it and why
- 69 forks — other institutions have copied it to adapt for their own workshops
- You can file a bug report (issue) if you find an error. That's a contribution.

**Link:** https://github.com/LibraryCarpentry/lc-git

**Image to use:**
- Screenshot of the lc-git commit history on GitHub — shows real activity, real people
- Or: the contributors list

**Talking point:** "You're already part of this ecosystem. The material exists because dozens of librarians contributed to it over time."

---

## Slide: Metadata and Cataloging Work

**Bullet points:**
- Version-control your local MARC templates, Dublin Core profiles, JSON-LD context files
- Track changes to controlled vocabularies — who changed a heading, when, and why
- Collaborative cataloging review: use pull requests as an approval workflow before records go into the ILS
- OpenRefine GREL scripts — repeatable, shareable, versioned cleanup operations

**Image to use:**
- A GitHub diff view showing a change to a YAML or CSV metadata file — lines in red/green
- Easy to mock up: create a simple CSV, change a value, show the diff on GitHub

**Talking point:** "Track changes, but for your metadata. Not just your Word documents."

---

## Slide: Digital Preservation and Archival Work

**Bullet points:**
- EAD finding aids — version history for archival description; full audit trail of who changed what
- Format migration scripts — reproducible, auditable, shareable across institutions
- Fixity scripts and batch processing tools
- Preservation is about provenance. So is version control.

**Talking point:** "Archivists already think this way about physical objects. Git extends that thinking to the digital work itself."

---

## Slide: Supporting Researchers (the Patron Angle)

**Bullet points:**
- NSF, NIH, and NEH increasingly require code and data sharing in DMPs
- GitHub + Zenodo is the standard workflow: publish a release → automatic DOI → citable software
- Researchers come to you for help with this — you need to know the tool to help them
- Open science means code is a research output. Libraries support research outputs.

**Links:**
- Zenodo + GitHub integration: https://docs.github.com/en/repositories/archiving-a-github-repository/referencing-and-citing-content

**Talking point:** "Your researchers are already expected to do this. You can be the person who helps them do it well."

---

## Slide: Instruction and Curriculum Development

**Bullet points:**
- Workshop materials, tutorials, and LibGuides as plain Markdown — versioned, collaboratively edited
- Syllabi tracked across semesters — see what changed and why
- Collaborative curriculum development across a consortium without emailing attachments
- Carpentries model: lessons are repos, contributions are pull requests, improvements are community-owned

**Talking point:** "You're already making teaching materials. Git makes them shareable, improvable, and permanent."

---

## Slide: Policy and Administrative Documents

**Bullet points:**
- Collection development policies with a full change history — no more "which version is current?"
- Procedure manuals: see what changed and why, without filename chaos
- Strategic planning docs shared across committees

**Talking point:** "It's not just for code. Any plain text file — including Markdown, CSV, YAML, HTML — can be versioned. That covers most of what libraries produce."

---

## Notes on Slide Order for 25-Minute Episode

Suggested flow for 9:20–9:45:

1. The problem (notFinal.doc) — 3 min
2. Git vs. GitHub — 2 min
3. "This lesson is on GitHub" — 2 min (quick, self-referential)
4. CollectionBuilder OR FOLIO — 5 min (pick one, go deep, show the repo live)
5. Metadata diff / "not just for code" — 3 min
6. Researcher support angle — 3 min
7. Transition: "Now let's use it" → Episode 2 — 2 min

Skip the preservation and policy slides if time is tight — they're in the notes for Q&A.

---

## Image Sources Summary

| Slide | Image | Source |
|---|---|---|
| The Problem | notFinal.doc comic | http://phdcomics.com/comics/archive.php?comicid=1531 |
| Git vs GitHub | Two-box local/remote diagram | LC Git lesson AIO page |
| FOLIO | GitHub org page screenshot | https://github.com/folio-org |
| CollectionBuilder | Idaho Queered site | https://www.lib.uidaho.edu/queered/ |
| CollectionBuilder | CB-GH repo | https://github.com/CollectionBuilder/collectionbuilder-gh |
| This Lesson | lc-git commit history | https://github.com/LibraryCarpentry/lc-git |
| Metadata diff | GitHub diff view | Mock up in any GitHub repo |

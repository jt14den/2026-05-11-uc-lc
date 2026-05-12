---
layout: slides
title: Workshop Introduction Slides
permalink: /introduction-slides/
---

<!-- class: pre-workshop -->

## While You Wait

<p class="pre-start">We begin at <strong>9:00 AM PT</strong> — get a head start:</p>

<p class="pre-setup-help">🛠 Need setup help? We admitted you early — type in chat and we'll come to you.</p>

<div class="two-col pre-workshop-cols">
<div markdown="1">

**1.** Sign into shared notes

<span class="pre-url">pad.carpentries.org/uc2026-lc-git</span>

**2.** Take the pre-workshop survey

<span class="pre-url">in the shared notes 👆</span>

**3.** Open a terminal and run:

```
$ git --version
git version 2.39.5 (Apple Git-154)
```

No version number? Type in chat.

</div>
<div class="qr-col">
  <div class="qr-item">
    <img src="https://api.qrserver.com/v1/create-qr-code/?size=150x150&color=1a3a6e&data=https://pad.carpentries.org/uc2026-lc-git" alt="QR: shared notes">
    <p>Shared notes</p>
  </div>
  <div class="qr-item">
    <img src="https://api.qrserver.com/v1/create-qr-code/?size=150x150&color=1a3a6e&data=https://carpentries.typeform.com/to/wi32rS?slug=2026-05-11-uc-lc" alt="QR: pre-workshop survey">
    <p>Pre-workshop survey</p>
  </div>
</div>
</div>

---

<!-- class: title-slide -->

<p class="title-eyebrow">Data + Software Skills for Librarians</p>

## Library Carpentry Workshop

<p class="title-date">May 11–20, 2026 | 9:00 am – 12:00 pm PT</p>

<p><span class="title-url">https://www.tim-dennis.com/2026-05-11-uc-lc/</span></p>

---

## How We Learn Together

<div class="two-col" markdown="1">
<div markdown="1">

### Our Pedagogy

- **Live Coding:** We learn by doing together; mistakes are pedagogical opportunities
- **Mental Models:** Connecting new skills to your daily work
- **No Overload:** A few key concepts, mastery over speed

</div>
<div markdown="1">

### Managing Expectations

- **Practical Competence:** Skills you can apply immediately in your library role
- **Collaborative Pace:** We move as a group; your questions help set the speed
- **Mistakes are Expected:** Coding is a process of troubleshooting and persistence

</div>
</div>

---

## Zoom Tools & Support

<div class="two-col">
<div markdown="1">

### Zoom Etiquette

- 🖐 **Raise Hand** for verbal questions
- 💬 Use **Chat** for technical issues & help
- ✅ Use **Non-verbal icons** (Yes/No/Speed)

### Communication

- Post questions in **Etherpad** shared notes
- Helpers monitor chat for immediate aid
- Typing **"I'm stuck"** is a complete sentence

> "Questions help everyone. You are not interrupting."

</div>
<div style="display:flex;align-items:center;justify-content:center;">
<img src="{{ '/assets/img/zoom-raise-hand.png' | relative_url }}" alt="Zoom reactions panel with Raise Hand highlighted" style="max-width:100%;border-radius:6px;box-shadow:0 2px 12px rgba(0,0,0,0.18);">
</div>
</div>

---

## Workshop Norms

We follow [The Carpentries Code of Conduct](https://docs.carpentries.org/topic_folders/policies/code-of-conduct.html). If something feels off, message us privately.

<div class="two-col" markdown="1">
<div markdown="1">

### Be Constructive

<div class="icon-list" markdown="1">

- ✅ Respect others' time and learning pace
- ✅ Let instructors guide the session flow
- ✅ Maintain inclusive and welcoming language
- ✅ Show courtesy and respect toward community members

</div>

</div>
<div markdown="1">

### What Is Not OK

<div class="icon-list" markdown="1">

- ❌ Repeatedly interrupting or redirecting
- ❌ Dominating the discussion or focus
- ❌ Dismissing others or the core material

</div>

</div>
</div>

---

## Why Git & GitHub?

Day 3 — May 13 | 9:00–10:30 AM PT

---

## The Problem

[![PhD Comics: notFinal.doc](https://phdcomics.com/comics/archive/phd101212s.gif)](https://phdcomics.com/comics/archive.php?comicid=1531)

`report_FINAL.docx` → `report_FINAL2.docx` → `report_USE_THIS_ONE.docx`

> Libraries have always solved this for physical objects. We haven't solved it for digital work.

---

## Git vs. GitHub

<div class="two-col" markdown="1">
<div markdown="1">

### Git

- Software that runs on your machine
- Tracks changes to files locally
- Free and open source

</div>
<div markdown="1">

### GitHub

- A website that hosts Git repos remotely
- Adds web interface and collaboration tools
- Alternatives: GitLab, Bitbucket

</div>
</div>

**Analogy:** Git is the catalog system. GitHub is the building that houses it.

---

## This Lesson Is on GitHub

- **578 commits** — every edit to every episode tracked, with who changed it and why
- **69 forks** — other institutions have copied it to adapt for their own workshops
- You can file a bug report if you find an error. That's a contribution.

[github.com/LibraryCarpentry/lc-git](https://github.com/LibraryCarpentry/lc-git)

---

## Your Library's Software Lives Here

- **FOLIO** — open source ILS, 461 repos on GitHub, community-developed by libraries for libraries
- **CollectionBuilder** — digital exhibit framework built on GitHub Pages, developed at U of Idaho Library
- **ArchivesSpace, Omeka, Islandora, DSpace, Blacklight, VuFind** — all open source, all on GitHub

> If your library runs FOLIO or is considering it, this is where that software lives.

---

## CollectionBuilder

Create a digital exhibit from a spreadsheet + folder of images, hosted free on GitHub Pages.

- Maps, timelines, search, tag clouds — generated from your metadata CSV
- Every change to your exhibit is tracked, reversible, citable
- Real example: [Idaho Queered](https://www.lib.uidaho.edu/queered/) — LGBTQ+ oral history at U of Idaho Library

> A library-built tool, maintained by librarians, used in production collections.

---

## Not Just for Code

<div class="two-col" markdown="1">
<div markdown="1">

### Metadata & Cataloging

- Version-control MARC templates, Dublin Core profiles, JSON-LD context files
- Track changes to controlled vocabularies
- Use pull requests as a cataloging review workflow
- Version your OpenRefine GREL scripts

</div>
<div markdown="1">

### Policy & Admin Docs

- Collection development policies with full change history
- Procedure manuals: see what changed and why
- Strategic planning docs shared across committees
- Any plain text file: Markdown, CSV, YAML, HTML

</div>
</div>

---

## Supporting Your Researchers

- NSF, NIH, and NEH increasingly require code and data sharing in DMPs
- **GitHub + Zenodo** — publish a release → automatic DOI → citable software
- Researchers come to you for help with this
- Open science means code is a research output. Libraries support research outputs.

> You can be the person who helps them do it well.

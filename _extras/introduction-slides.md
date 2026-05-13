---
layout: slides
title: Workshop Introduction Slides
permalink: /introduction-slides/
---

<!-- class: pre-workshop -->

## While You Wait

<p class="pre-start">We begin at <strong>9:00 AM PT</strong>. Get a head start:</p>

<p class="pre-setup-help">🛠 Need setup help? Type in chat or come on mic: let us know your operating system and we'll help.</p>

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
  <div class="qr-item">
    <img src="https://api.qrserver.com/v1/create-qr-code/?size=150x150&color=1a3a6e&data=https://www.tim-dennis.com/2026-05-11-uc-lc/" alt="QR: workshop website">
    <p>Workshop website</p>
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

Day 3: May 13 | 9:00–10:30 AM PT

---

## The Problem

<div class="two-col">
<div markdown="1">

[![PhD Comics: notFinal.doc](https://phdcomics.com/comics/archive/phd101212s.gif)](https://phdcomics.com/comics/archive.php?comicid=1531)

</div>
<div markdown="1">

[![XKCD: Documents](https://imgs.xkcd.com/comics/documents.png)](https://xkcd.com/1459/)

</div>
</div>

> Libraries have always solved this for physical objects. We haven't solved it for digital work.

---

## What Version Control Gives You

- Versioning: one file, complete history, no `report_FINAL2.docx`
- Rolling back: undo changes when something breaks
- Collaboration: merge edits from different people without emailing files
- Understanding: see who changed what, when, and why
- Backup: your work isn't stuck on one machine

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

**Analogy:** Git is cataloging practice: your local workflow. GitHub is WorldCat: where you publish records so others can find and contribute.

---

## This Lesson Is on GitHub

- **578 commits**: every edit to every episode tracked, with who changed it and why
- **69 forks**: other institutions have copied it to adapt for their own workshops
- You can file a bug report if you find an error. That's a contribution.

[github.com/LibraryCarpentry/lc-git](https://github.com/LibraryCarpentry/lc-git)

---

## Your Library's Software Lives Here

- **[FOLIO](https://www.folio.org)**: open source ILS, 461 repos on GitHub, community-developed by libraries for libraries
- **[CollectionBuilder](https://collectionbuilder.github.io)**: digital exhibit framework built on GitHub Pages, developed at U of Idaho Library
- **[ArchivesSpace](https://archivesspace.org), [Omeka](https://omeka.org), [Islandora](https://www.islandora.ca), [DSpace](https://dspace.lyrasis.org), [Blacklight](https://projectblacklight.org), [VuFind](https://vufind.org)**: all open source, all on GitHub

> If your library runs FOLIO or is considering it, this is where that software lives.

---

## [CollectionBuilder](https://collectionbuilder.github.io)

Create a digital exhibit from a spreadsheet + folder of images, hosted free on GitHub Pages.

- Maps, timelines, search, tag clouds: generated from your metadata CSV
- Every change to your exhibit is tracked, reversible, citable
- Real example: [Idaho Queered](https://www.lib.uidaho.edu/queered/), LGBTQ+ oral history at U of Idaho Library

> A library-built tool, maintained by librarians, used in production collections.

---

## Not Just for Code

<div class="two-col" markdown="1">
<div markdown="1">

### Metadata & Cataloging

- Version-control MARC templates, Dublin Core profiles, JSON-LD context files
- Track changes to controlled vocabularies
- Use pull requests as a cataloging review workflow
- Version your [OpenRefine](https://openrefine.org) GREL scripts

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
- **GitHub + [Zenodo](https://zenodo.org)**: publish a release → automatic DOI → citable software
- Researchers come to you for help with this
- Open science means code is a research output. Libraries support research outputs.

> You can be the person who helps them do it well.

---

## Before We Open a Terminal

What files in your work do you wish you had a complete history for?

*(Type in chat or unmute, 2 minutes)*

---

## To the Terminal

<div class="two-col">
<div markdown="1">

### Mac

1. Press **Cmd + Space** to open Spotlight
2. Type **Terminal** and press Enter

*Or:* Applications → Utilities → Terminal

</div>
<div markdown="1">

### Windows

1. Open the **Start Menu**
2. Search for **Git Bash**
3. Click to open

*Not Git Bash? Let us know in chat.*

</div>
</div>

Once it's open, type:

```
git --version
```

You should see a version number. If you get an error, let us know now.

---

## Join the Remaining Sessions

<div class="two-col" style="align-items:center;">
<div markdown="1">

### Coming Up

- **Day 4 — May 18:** OpenRefine for Data Cleaning
- **Day 5 — May 19:** Python 1: Variables, Lists & Pandas
- **Day 6 — May 20:** Python 2: Advanced Pandas & Visualization

Register or share the workshop page:

**tim-dennis.com/2026-05-11-uc-lc**

</div>
<div style="display:flex;flex-direction:column;align-items:center;justify-content:center;gap:0.5rem;">
  <img src="https://api.qrserver.com/v1/create-qr-code/?size=200x200&color=1a3a6e&data=https://www.tim-dennis.com/2026-05-11-uc-lc/" alt="QR code: workshop registration page" style="border:3px solid #1a3a6e;border-radius:6px;">
  <p style="font-size:0.4em;color:#555;text-align:center;margin:0;">Workshop page &amp; registration</p>
</div>
</div>

---

## The Two-Stage Workflow

<div style="display:flex;align-items:center;justify-content:center;gap:1.4rem;margin-top:2.5rem;">
  <div style="background:#f4f7fb;border:3px solid #1a3a6e;border-radius:8px;padding:0.9em 1.4em;text-align:center;min-width:170px;">
    <strong style="display:block;color:#1a3a6e;font-size:0.55em;text-transform:uppercase;letter-spacing:0.06em;margin-bottom:0.3em;">Working Directory</strong>
    <span style="font-size:0.42em;color:#555;">your edits</span>
  </div>
  <div style="text-align:center;flex:0 0 auto;">
    <div style="font-size:1.4em;color:#1a3a6e;line-height:1;">&#8594;</div>
    <code style="font-size:0.38em;background:#FDB515;padding:0.25em 0.55em;border-radius:4px;color:#111;font-weight:700;">git add</code>
  </div>
  <div style="background:#f4f7fb;border:3px solid #1a3a6e;border-radius:8px;padding:0.9em 1.4em;text-align:center;min-width:170px;">
    <strong style="display:block;color:#1a3a6e;font-size:0.55em;text-transform:uppercase;letter-spacing:0.06em;margin-bottom:0.3em;">Staging Area</strong>
    <span style="font-size:0.42em;color:#555;">(index)</span>
  </div>
  <div style="text-align:center;flex:0 0 auto;">
    <div style="font-size:1.4em;color:#1a3a6e;line-height:1;">&#8594;</div>
    <code style="font-size:0.38em;background:#FDB515;padding:0.25em 0.55em;border-radius:4px;color:#111;font-weight:700;">git commit</code>
  </div>
  <div style="background:#1a3a6e;border:3px solid #1a3a6e;border-radius:8px;padding:0.9em 1.4em;text-align:center;min-width:170px;">
    <strong style="display:block;color:#FDB515;font-size:0.55em;text-transform:uppercase;letter-spacing:0.06em;margin-bottom:0.3em;">Repository</strong>
    <span style="font-size:0.42em;color:#adc4e0;">(.git)</span>
  </div>
</div>

> `git add` = choose what goes in. `git commit` = take the snapshot.

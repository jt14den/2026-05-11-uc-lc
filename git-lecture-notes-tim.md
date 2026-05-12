# Git & GitHub for Librarians — Lecture Notes (Tim)
UC Library Carpentry | 2026-05-13 | 9:00–10:30 AM PT

---

## 9:00 AM — Welcome & Setup Verification (20 min)

**Goal:** Everyone has Git installed and a GitHub account before we touch a command.

### Talking points
- Welcome and quick introductions (instructors + helpers)
- Today's agenda: two episodes before break, then Seth takes GitHub/sharing
- All work happens in the shell — if you haven't used it before, that's fine, we go slow
- Point to the workshop page for setup instructions and collaborative notes link

### Setup checks (work through with helpers)
- `git --version` — should return something; if not, stop and fix now
- GitHub account created? Confirm username is set (remind them: **usernames and emails are publicly visible by default**)
- Network? Confirm everyone can reach github.com
- Text editor configured? We'll set this in Episode 2 but flag it now

### Asides
- Helpers: circulate during setup check, don't wait for people to raise their hand
- If someone is on Windows and has line-ending issues later, flag `core.autocrlf` — we'll address it when it comes up

---

## 9:20 AM — Episode 1: What is Git/GitHub? (25 min)

**Slides:** [introduction-slides](https://jt14den.github.io/2026-05-11-uc-lc/introduction-slides/)

**Goal:** Learners understand *why* version control matters before they touch any commands.

---

### Slide: The Problem

- Show the notFinal.doc PhD Comics strip: `report_FINAL.docx` → `report_FINAL2.docx` → `report_USE_THIS_ONE.docx`
- Libraries have always solved this for physical objects — we haven't solved it for digital work

### What version control gives you (lesson)
- **Collaboration** — formalized way to work with others without stepping on each other
- **Versioning** — rigorous change log, no renaming files
- **Rolling back** — undo bad changes quickly
- **Understanding** — who changed what, when, and why
- **Backup** — work lives in multiple places (note: not a primary backup solution)

---

### Slide: Git vs. GitHub

- **Git** — software, runs on your machine, tracks changes locally, free & open source
- **GitHub** — website, hosts Git repos remotely, adds web interface and collaboration tools
- Alternatives: GitLab, Bitbucket

---

### Slide: This Lesson Is on GitHub

- Point to [lc-git](https://github.com/LibraryCarpentry/lc-git): 578 commits, 69 forks
- Other institutions fork it to adapt for their own workshops
- Filing a bug report = a contribution — that's open source participation

---

### Slide: Your Library's Software Lives Here

- **FOLIO** — open source ILS, 461 repos on GitHub, community-developed by libraries
- **CollectionBuilder** — digital exhibit framework built on GitHub Pages, developed at U of Idaho Library
- ArchivesSpace, Omeka, Islandora, DSpace, Blacklight, VuFind — all open source, all on GitHub

### Slide: CollectionBuilder

- Spreadsheet + folder of images → maps, timelines, search, tag clouds from metadata CSV
- Every change tracked, reversible, citable
- Real example: [Idaho Queered](https://www.lib.uidaho.edu/queered/) — LGBTQ+ oral history at U of Idaho Library

---

### Slide: Not Just for Code

**Metadata & Cataloging:**
- Version-control MARC templates, Dublin Core profiles, JSON-LD context files
- Track changes to controlled vocabularies
- Pull requests as a cataloging review workflow
- Version your OpenRefine GREL scripts

**Policy & Admin Docs:**
- Collection development policies with full change history
- Procedure manuals: see what changed and why
- Strategic planning docs shared across committees
- Any plain text file: Markdown, CSV, YAML, HTML

---

### Slide: Supporting Your Researchers

- NSF, NIH, and NEH increasingly require code and data sharing in DMPs
- **GitHub + Zenodo** — publish a release → automatic DOI → citable software
- Researchers come to you for help with this
- You can be the person who helps them do it well

---

### Asides
- The "why" here is more important than the commands — spend real time on it
- Don't go deep on branching — not in this lesson, will confuse people early

---

## 9:45 AM — Episode 2: Getting Started (init, add, commit) (45 min)

**Goal:** Learners create a repo, stage a file, and make their first commit. They understand the two-stage workflow.

---

### Step 1: Configure Git (5 min)

**Show first — then have them follow along.**

```bash
git config --list
```
> Check what's already set. Many will have something; some will have nothing.

Set identity (must match GitHub email for contributions to be credited):

```bash
git config --global user.name "Your Name"
git config --global user.email "yourname@domain.name"
```

Set text editor (Nano — easiest for beginners):

```bash
git config --global core.editor "nano -w"
```

Set default branch name:

```bash
git config --global init.defaultBranch main
```

**Walk through Nano controls now** — don't assume they know it:
- `Ctrl+O` then `Enter` to save
- `Ctrl+X` to exit
- Or: `Ctrl+X` → `Y` → `Enter` (save-and-exit in one flow)

### Asides
- `--global` means this applies to all repos on their machine, not just this one
- Email must match GitHub if they want commits attributed correctly
- If someone is on Windows, mention `core.autocrlf` may matter for line endings — note it, don't deep-dive

---

### Step 2: Create a Repository (5 min)

```bash
mkdir hello-world
cd hello-world
git init
```

Expected output:
```
Initialized empty Git repository in <your path>/hello-world/.git/
```

```bash
git status
```

Expected output:
```
On branch main
No commits yet
nothing to commit (create/copy files and use "git add" to track)
```

### Talking points
- `git init` creates a hidden `.git/` folder — that *is* the repository
- Everything Git knows about this project lives in `.git/` — don't delete it
- `git status` is your best friend — run it constantly, we'll use it after every step

### Asides
- Run `ls -a` to show the `.git/` directory exists
- Git does not track anything automatically — you always tell it what to watch

---

### Step 3: Add and Commit (25 min)

This is the core of the lesson. Slow down here.

**Create a file:**

```bash
touch index.md
git status
```

> Git sees an *untracked* file. It's not tracking it yet.

**Stage the file:**

```bash
git add index.md
git status
```

> Now it's in the staging area — "Changes to be committed."

**Edit the file:**

```bash
nano -w index.md
```

Add something simple:
```
# Hello, world!
```
Save and exit (`Ctrl+O`, `Enter`, `Ctrl+X`).

**Check status again:**

```bash
git status
```

> Two things now: the staged empty file AND the modified (but unstaged) version. This is the key moment.

**Stage the updated version:**

```bash
git add index.md
git status
```

**Commit:**

```bash
git commit -m 'Add index.md'
```

Expected output:
```
[main (root-commit) <hash>] Add index.md
 1 file changed, 1 insertion(+)
 create mode 100644 index.md
```

**View history:**

```bash
git log
```

> Shows commit hash, author, timestamp, message.

### Talking points — the two-stage workflow

```
Working directory  →  Staging area (index)  →  Repository (.git)
  (your edits)         git add                   git commit
```

- `git add` says "include this in the next snapshot"
- `git commit` takes the actual snapshot — permanent, with metadata (who, when, message)
- The staging area exists so you can be precise — commit only what belongs together

**Commit messages matter:**
- Write as an imperative: "Add index.md", not "Added" or "Adding"
- Future-you will read these — make them useful
- Omit `-m` and Git opens your editor for a longer message

### Asides
- Don't use `git commit -a` as a habit — skips the staging area, can include things you didn't mean to commit
- The commit hash is a fingerprint of the exact state — you can always get back to any hash
- If someone accidentally commits the wrong thing, reassure them — we can fix it

---

### Step 4: Quick Check (5 min, before break)

```bash
git log
git status
```

Ask the group:
- "What does `git add` do?"
- "What does `git commit` do?"
- "What's the difference between the working directory and the staging area?"

### Asides
- For remote teaching: use collaborative board (Miro, Jamboard) — learners add color-coded notes for each command type
- Good moment to acknowledge: the two-stage workflow feels weird at first — it clicks after a few sessions

---

### If Time Allows: git diff and git log options

*(These commands are from later episodes — only go here if you finish Step 4 early and want a preview. Skip cleanly if not.)*

**See what changed before staging:**

```bash
nano -w index.md
```

Add a second line, save, then:

```bash
git diff
```

> Shows what's changed in the working directory vs the last commit. `+` lines are new, `-` lines are removed.

```bash
git add index.md
git diff
```

> Nothing shown — `git diff` only shows *unstaged* changes. Use `git diff --staged` to see what's in the staging area.

**Compact log view:**

```bash
git log --oneline
```

> One line per commit — useful once history gets long.

### Asides
- `git diff` is most useful *before* `git add` as a self-check
- `git log --oneline` is the one to remember

---

## 10:30 AM — Break (10 min)

Remind learners:
- Back at 10:40
- Seth will take over for GitHub/sharing (Episode 3)
- Leave terminal open, stay in `hello-world/` directory

---

*Notes continue in `git-lecture-notes-seth.md` (Episode 3 onward)*

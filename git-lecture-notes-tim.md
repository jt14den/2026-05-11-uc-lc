# Git & GitHub for Librarians — Lecture Notes (Tim)
UC Library Carpentry | 2026-05-13 | 9:00–10:30 AM PT

---

## 9:00 AM — Welcome & Setup Verification (20 min)

**Goal:** Everyone has Git installed and a GitHub account before we touch a command.

### Talking points
- Welcome and quick introductions (instructors + helpers)
- Today's agenda: two episodes before break, then Seth takes GitHub/sharing
- All work happens in the shell — if you haven't used it before, that's fine, we go slow
- Point to the workshop page for setup instructions and the collaborative notes link

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

### Talking points

**The version control problem**
- Who has a folder full of `draft_v1`, `draft_FINAL`, `draft_FINAL2`? That's manual version control — and it breaks down fast
- Git solves this: one file, complete history inside it, no renaming required
- You can always roll back to any earlier state

**What Git gives you**
- **Versioning** — a rigorous log of every change, who made it, when, and why
- **Rolling back** — undo bad changes without losing everything else
- **Collaboration** — formalized way to work with others without stepping on each other
- **Backup** — your work lives in multiple places (local + remote)

**Git vs. GitHub — keep these distinct**
- **Git** is the software — runs on your machine, tracks changes locally, free and open source
- **GitHub** is a website — hosts Git repositories remotely, adds a web interface, pull requests, etc.
- Alternatives: GitLab, Bitbucket, Gitee — Git is the engine, GitHub is one garage

**Why librarians specifically?**
- *Crowdsourcing projects*: Fork an open-licensed project as a template — modify rather than rebuild from scratch
- *Collaborative metadata editing*: Multiple people editing spreadsheets, tracking conflicts, preserving originals, reviewing changes before re-ingestion
- Open-access journals, textbooks, and teaching materials are increasingly hosted on GitHub

### Demo / discussion
- Show a real GitHub repo (your own or the workshop repo) — point out: commits tab, history, who changed what
- Optional: show a commit diff so they can see what "tracked changes" looks like

### Asides
- The "why" here is more important than the commands — spend real time on it
- Whiteboard sketch helps: local machine (Git) ←→ GitHub (remote) — draw the two boxes and the arrows
- Don't go deep on branching — it's not in this lesson and will confuse people early

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
- Email must match GitHub if they want their commits to show up attributed correctly on GitHub
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
nothing to commit (create/copy files and use "git add" to tell Git what to track)
```

### Talking points
- `git init` creates a hidden `.git/` folder — that *is* the repository
- Everything Git knows about this project lives in `.git/` — don't delete it
- `git status` is your best friend — run it constantly, we'll use it after every step

### Asides
- You can run `ls -a` to show the `.git/` directory exists
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

Draw the three boxes on the whiteboard (or say it out loud):

```
Working directory  →  Staging area (index)  →  Repository (.git)
  (your edits)         git add                   git commit
```

- `git add` says "include this in the next snapshot"
- `git commit` takes the actual snapshot — permanent, with metadata (who, when, message)
- The staging area exists so you can be precise — commit only what belongs together

**Commit messages matter:**
- Write them as an imperative: "Add index.md", not "Added" or "Adding"
- Future-you will read these. Make them useful.
- Omit `-m` and Git opens your editor for a longer message — fine for complex commits

### Asides
- Don't use `git commit -a` as a habit — it skips the staging area and can accidentally include things you didn't mean to commit
- The commit hash is a fingerprint of the exact state of the repo at that moment — you can always get back to any hash
- If someone accidentally commits the wrong thing, reassure them — we can fix it; nothing is permanent locally

---

### Step 4: Quick Check (5 min, before break)

**Mini-review before handing off:**

```bash
git log
git status
```

Ask the group:
- "What does `git add` do?"
- "What does `git commit` do?"
- "What's the difference between the working directory and the staging area?"

### Asides
- For remote teaching: use collaborative board (Miro, Jamboard) — learners add color-coded notes for each command type, then quiz each other
- This is a good moment to acknowledge that the two-stage workflow feels weird at first — it clicks after a few sessions

---

### If Time Allows: git diff and git log options

Only go here if you finish Step 4 early. Skip cleanly if not.

**See what changed before staging:**

```bash
nano -w index.md
```

Add a second line, save, then:

```bash
git diff
```

> Shows what's changed in the working directory vs the last commit. Lines with `+` are new, `-` are removed.

```bash
git add index.md
git diff
```

> Nothing shown — `git diff` only shows *unstaged* changes. Use `git diff --staged` to see what's in the staging area.

**More log options:**

```bash
git log --oneline
```

> Compact view — one line per commit. Useful once history gets long.

```bash
git log --oneline --graph
```

> Adds a text branch diagram — more useful later when branching is involved.

### Asides
- `git diff` is most useful *before* `git add` as a self-check — "did I change what I meant to?"
- `git log --oneline` is the one to remember; `--graph` is a nice bonus

---

## 10:30 AM — Break (10 min)

Remind learners:
- Back at 10:40
- Seth will take over for GitHub/sharing (Episode 3)
- Leave terminal open, stay in `hello-world/` directory

---

*Notes continue in `git-lecture-notes-seth.md` (Episode 3 onward)*

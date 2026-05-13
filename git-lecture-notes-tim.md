# Git & GitHub for Librarians — Lecture Notes (Tim)
UC Library Carpentry | 2026-05-13 | 9:00–10:30 AM PT

---

## 9:00 AM — Welcome & Setup Verification (20 min)

**Goal:** Everyone has Git installed and a GitHub account before we touch a command.

### Talking points
- Welcome and quick introductions (instructors + helpers)
- Today's agenda: two episodes before break, then Seth takes GitHub/sharing
- All work happens in the **shell** — if you haven't used it before, that's fine, we go slow
- Point to the **workshop page** for setup instructions and collaborative notes link

### Setup checks (work through with helpers)
- `git --version` — should return something; if not, stop and fix now
- **GitHub account** created? Confirm username is set (remind them: **usernames and emails are publicly visible by default**)
- **Network?** Confirm everyone can reach github.com
- **Text editor** configured? We'll set this in Episode 2 but flag it now

### Asides
- Helpers: circulate during setup check, don't wait for people to raise their hand
- If someone is on Windows and has line-ending issues later, flag `core.autocrlf` — we'll address it when it comes up

---

## 9:20 AM — Episode 1: What is Git/GitHub? (25 min)

**Slides:** [introduction-slides](https://jt14den.github.io/2026-05-11-uc-lc/introduction-slides/)

**Goal:** Learners understand *why* version control matters before they touch any commands.

Follow the slide deck — it covers the problem, version control benefits, Git vs. GitHub, and library use cases.

### Asides
- The **"why"** here is more important than the commands — spend real time on it
- Don't go deep on **branching** — not in this lesson, will confuse people early

### Segue to the Terminal

*After the discussion slide ("What files do you wish you had a complete history for?"):*

> "That's exactly what we're going to fix today. Let's open a terminal and start building that history."

Walk through the "To the Terminal" slide. Wait for everyone to confirm `git --version` works before moving on — anyone with a problem surfaces here, not mid-command.

---

## 9:45 AM — Episode 2: Getting Started (init, add, commit) (45 min)

**Goal:** Learners create a repo, stage a file, and make their first commit. They understand the **two-stage workflow**.

---

### Step 1: Configure Git (5 min)

**Show first — then have them follow along.**

```bash
git config --list
```

- Check what's **already set** — many will have something, some will have nothing
- Look for `user.name` and `user.email` in the output

Set **identity** (must match GitHub email for contributions to be credited):

```bash
git config --global user.name "Your Name"
git config --global user.email "yourname@domain.name"
```

Set **text editor** (Nano — easiest for beginners):

```bash
git config --global core.editor "nano -w"
```

Set **default branch name**:

```bash
git config --global init.defaultBranch main
```

**Walk through Nano controls now** — don't assume they know it:
- `Ctrl+O` then `Enter` to save
- `Ctrl+X` to exit
- Or: `Ctrl+X` → `Y` → `Enter` (save-and-exit in one flow)

### Asides
- `--global` means this applies to **all repos** on their machine, not just this one
- Email must match GitHub if they want commits **attributed correctly**
- If someone is on Windows, mention `core.autocrlf` may matter for line endings — note it, don't deep-dive

---

### Step 2: Create a Repository (5 min)

```bash
mkdir hello-world
cd hello-world
git init
```

- Git creates a **hidden `.git/` folder** — that *is* the repository
- Everything Git knows about this project lives in `.git/` — don't delete it

```bash
git status
```

- Shows **branch**, **commit status**, and **what's tracked**
- `git status` is your best friend — run it constantly, we'll use it after every step

### Asides
- Run `ls -a` to show the `.git/` directory exists
- Git does **not** track anything automatically — you always tell it what to watch

---

### Step 3: Add and Commit (25 min)

This is the core of the lesson. **Slow down here.**

**Create a file:**

```bash
touch index.md
git status
```

- Git sees an **untracked** file — it knows the file exists but isn't tracking it yet

**Stage the file:**

```bash
git add index.md
git status
```

- File moves to the **staging area** — shows as "Changes to be committed"

**Edit the file:**

```bash
nano -w index.md
```

- Add something simple: `# Hello, world!`
- Save and exit (`Ctrl+O`, `Enter`, `Ctrl+X`)

**Check status again:**

```bash
git status
```

- Two things now: the **staged** (empty) file AND the **modified but unstaged** version
- This is the key moment — the staging area only has what you `add`ed, not the edit you just made

**Stage the updated version:**

```bash
git add index.md
git status
```

- Both changes are now in the **staging area**, ready to commit

**Commit:**

```bash
git commit -m 'Add index.md'
```

- Git records a **permanent snapshot** with metadata: who, when, message
- The **commit hash** in the output is a fingerprint of this exact state

**View history:**

```bash
git log
```

- Shows **commit hash**, author, timestamp, message
- Every commit is permanent and addressable by hash

### Talking points — the two-stage workflow

```
Working directory  →  Staging area (index)  →  Repository (.git)
  (your edits)         git add                   git commit
```

- **`git add`** says "include this in the next snapshot"
- **`git commit`** takes the actual snapshot — permanent, with metadata (who, when, message)
- The **staging area** exists so you can be precise — commit only what belongs together

**Commit messages matter:**
- Write as an **imperative**: "Add index.md", not "Added" or "Adding"
- Future-you will read these — make them useful
- Omit `-m` and Git opens your **editor** for a longer message

### Asides
- Don't use `git commit -a` as a habit — skips the staging area, can include things you didn't mean to commit
- The **commit hash** is a fingerprint of the exact state — you can always get back to any hash
- If someone accidentally commits the wrong thing, reassure them — we can fix it

---

### Step 4: Quick Check (5 min, before break)

```bash
git log
git status
```

Ask the group:
- "What does **`git add`** do?"
- "What does **`git commit`** do?"
- "What's the difference between the **working directory** and the **staging area**?"

### Asides
- For remote teaching: use collaborative board (Miro, Jamboard) — learners add color-coded notes for each command type
- Good moment to acknowledge: the **two-stage workflow** feels weird at first — it clicks after a few sessions

---

### If Time Allows: git diff and git log options

*(Commands from later episodes — only go here if you finish Step 4 early. Skip cleanly if not.)*

**See what changed before staging:**

```bash
nano -w index.md
```

- Add a second line, save, then:

```bash
git diff
```

- Shows what's changed in the **working directory** vs the last commit
- `+` lines are new, `-` lines are removed

```bash
git add index.md
git diff
```

- Nothing shown — `git diff` only shows **unstaged** changes
- Use `git diff --staged` to see what's in the **staging area**

**Compact log view:**

```bash
git log --oneline
```

- One line per commit — useful once history gets long
- The one **log flag** to remember

### Asides
- `git diff` is most useful *before* `git add` as a self-check
- `git log --oneline` is the one to remember

---

## 10:30 AM — Break (10 min)

Remind learners:
- Back at **10:40**
- **Seth** will take over for GitHub/sharing (Episode 3)
- Leave terminal open, stay in `hello-world/` directory

---

*Notes continue in `git-lecture-notes-seth.md` (Episode 3 onward)*

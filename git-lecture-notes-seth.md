# Git & GitHub for Librarians — Follow-Along Notes (Seth's Sections)
UC Library Carpentry | 2026-05-13 | 10:40 AM–12:00 PM PT

*These are Tim's follow-along notes, not Seth's teaching prep.*

---

## 10:40 AM — Episode 3: Sharing Your Work (50 min)

### What's happening
Seth takes over. This episode connects the local repo to GitHub — SSH setup, creating a remote repo, push/pull.

---

### SSH Setup

Generate a key (if not already done):

```bash
ssh-keygen -t ed25519 -C "yourname@domain.com"
```

Print the public key to copy:

```bash
cat ~/.ssh/id_ed25519.pub
```

Add to GitHub: Settings → SSH and GPG keys → New SSH key → paste

Test the connection:

```bash
ssh -T git@github.com
```

Expected:
```
Hi username! You've successfully authenticated...
```

---

### Create a Remote Repo on GitHub

1. GitHub → New repository
2. Name: `hello-world` (matches local)
3. Keep it empty — no README, no license (we already have local content)
4. Copy the SSH URL: `git@github.com:username/hello-world.git`

---

### Connect Local to Remote

```bash
git remote add origin git@github.com:username/hello-world.git
git remote -v
```

> `origin` is just a nickname for the remote URL. Convention — you could call it anything.

---

### Push

```bash
git push -u origin main
```

> `-u` sets the upstream tracking branch — after this, plain `git push` works.

Refresh GitHub — commits should appear.

---

### Make a Change on GitHub, Pull Locally

Edit `index.md` directly on GitHub (pencil icon), commit there.

Then locally:

```bash
git pull
git log --oneline
```

> `git pull` = fetch + merge. The GitHub commit now appears in local history.

---

### Workflow to watch for

```
Edit locally → git add → git commit → git push
Edit on GitHub → git pull
```

---

## 11:30 AM — Episode 4: Review & Q&A (15 min)

### What's happening
Seth leads a group review — commands into plain language, drawing the workflow, personal analogies.

### Concepts to have clear in your head if Q&A comes to you

| Question | Answer |
|---|---|
| What's the difference between `git add` and `git commit`? | `add` stages (selects), `commit` snapshots (saves permanently) |
| What's `origin`? | Nickname for the remote URL |
| Why SSH instead of HTTPS? | No password prompts; key-based auth is more secure and persistent |
| What does `git pull` do? | Fetches remote changes and merges them into your local branch |
| Can I undo a commit? | Yes — `git revert` (safe) or `git reset` (destructive, avoid for now) |

---

## 11:45 AM — Episode 5: GitHub Pages (if time allows, 15 min)

### What's happening
Seth demonstrates turning the `hello-world` repo into a live website via GitHub Pages.

### Steps to watch

1. Repo → Settings → Pages
2. Source: Deploy from branch → `main` → `/ (root)` → Save
3. Wait ~1 min, then visit `https://username.github.io/hello-world/`

The `index.md` file becomes the homepage. Jekyll converts Markdown to HTML automatically.

### Key point
GitHub Pages versions the website — every commit is a historical snapshot. Useful for citing a site at a specific point in time (academic use case).

### If branching/PRs come up

```bash
git switch -c my-branch    # create and switch to new branch
# make edits
git add .
git commit -m "Try something"
git push origin my-branch
```

Then open a pull request on GitHub to merge into `main`.

---

## 12:00 PM — End

- Point to lesson page for reference commands
- Collaborative notes link for follow-up questions
- Next LC session: [check workshop page]

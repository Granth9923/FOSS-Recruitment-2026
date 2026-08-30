# FOSS United SIT — Technical Recruitment 2026

**Task:** build a project, submit it as a pull request to this repository.
**Deadline:** 1 September 2026, 11:59 PM IST.

---

## Quick version

If you've used git before:

1. Fork this repo, clone your fork
2. `mkdir firstname_lastname` at the root, put your code in it
3. Include a `README.md` in your folder: what it does, how to run it, what was hard
4. Don't touch anything outside your folder
5. Commit, push, open a PR titled `Submission — Your Name`, with your name, PRN and division in the description

Everything below is the same thing, explained from scratch.

---

## What should I build?

Anything you want. Any language, any stack.

It does not have to be big, original, or impressive. We're not expecting a startup. We want to see that you can build something that works and explain why you built it that way.

If you're staring at a blank screen: a script that automates something annoying, a small game, a website, a CLI tool, a Discord bot, a data analysis with a writeup of what you found.

**What we'd rather not see:** a tutorial project copy-pasted without changes, or a folder with no README explaining what it is.

**On AI tools.** Use them if you want, we're not going to police it. But Round 2 is a conversation about your code: what this function does, why this approach, what breaks if we change X. Submit something you can talk through. Don't submit a classmate's work with your name on it.

---

## Where your code goes

This repository currently contains nothing but this README. Everything else in it will be submissions.

```
README.md              <- leave this alone
firstname_lastname/
  README.md            <- yours, required
  ... your code ...
```

Folder name: lowercase, underscore between the two names. `aditi_sharma`, not `Aditi Sharma`.

Your folder's `README.md` needs three things: what your project does in two or three sentences, the exact commands to run it, and anything you found difficult or would do differently with more time. That last one isn't filler. We read it, and it often tells us more than the code does.

---

## How to submit

**Never used GitHub? That's fine, and it's not what we're testing.** This is about ten minutes of copy-pasting. If something breaks, jump to [Common errors](#common-errors) — almost everything that goes wrong on a first attempt is listed there.

### Step 0: Install git

- **Ubuntu/Debian:** `sudo apt install git`
- **Fedora:** `sudo dnf install git`
- **macOS:** `brew install git`, or type `git` in Terminal and accept the prompt
- **Windows:** [git-scm.com](https://git-scm.com/download/win), accept all defaults. This installs **Git Bash**. Use Git Bash for every command below, not Command Prompt.

Then tell git who you are (once, ever):

```bash
git config --global user.name "Your Name"
git config --global user.email "your@email.com"
```

Don't skip this. Git refuses to commit if it doesn't know who you are.

### Step 1: Fork this repository

Click **Fork** at the top right, then **Create fork**. A fork is your own copy of this repo on your account, where you can do whatever you like without affecting ours. You'll now be on `github.com/YOUR-USERNAME/recruitment-2026`.

### Step 2: Clone your fork

Cloning downloads your fork onto your laptop. On **your fork's** page, click the green **Code** button, copy the HTTPS URL, then:

```bash
git clone https://github.com/YOUR-USERNAME/recruitment-2026.git
cd recruitment-2026
```

That URL must have *your* username in it, not ours.

### Step 3: Make your folder and build

You're now inside `recruitment-2026`, which contains one file. Make your folder next to it:

```bash
mkdir aditi_sharma
cd aditi_sharma
```

Use your own name, obviously. Now write your project in here. Come back when you're done.

### Step 4: Commit

A commit is a saved snapshot of your changes. From anywhere inside the repo folder:

```bash
git add .
git commit -m "Add submission by Your Name"
```

Commit as often as you like while working. It's a good habit.

### Step 5: Push

Pushing uploads your commits to your fork on GitHub.

```bash
git push origin main
```

This asks for a username and password. **Your GitHub password will not work** — GitHub disabled that in 2021. See [Authentication](#authentication).

### Step 6: Open the pull request

Go to your fork on GitHub. There should be a **Compare & pull request** banner. If not, **Contribute** → **Open pull request**.

Check the arrow reads `fossunited-sit/recruitment-2026 : main` ← `YOUR-USERNAME/recruitment-2026 : main`.

Title it `Submission — Your Name`. In the description:

```
Name:
PRN:
Branch/Division:
Project: one line about what you built
```

Click **Create pull request**. Done. Your PR must be open by the deadline; commits pushed afterwards are ignored, so don't cut it fine.

---

## Authentication

### Option A: GitHub CLI (easiest)

Install [GitHub CLI](https://cli.github.com/), then run `gh auth login`. Choose **GitHub.com** → **HTTPS** → **Login with a web browser**, copy the code, press Enter, log in. Done permanently.

### Option B: Personal Access Token

1. [github.com/settings/tokens](https://github.com/settings/tokens) → **Generate new token (classic)**
2. Any name, 30 day expiry, tick the **repo** checkbox
3. Generate, then copy the `ghp_...` string. **Copy it now, GitHub never shows it again.**

Paste that as the password when `git push` asks. Username is your normal GitHub username.

> The terminal shows nothing while you type or paste a password. That's normal, not a bug. Paste (`Ctrl+Shift+V`, or `Cmd+V` on macOS) and press Enter.

---

## Common errors

**`fatal: not a git repository`**
Wrong folder. `cd recruitment-2026` first. Check where you are with `pwd`.

**`Authentication failed` / `Support for password authentication was removed`**
You used your GitHub password. See [Authentication](#authentication).

**`Permission denied` / `403` when pushing**
You cloned our repo instead of your fork. Check with `git remote -v`. If your username isn't in the URL, delete the folder and redo Step 1.

**`Updates were rejected because the remote contains work that you do not have locally`**
`git pull origin main --rebase`, then push again.

**`Author identity unknown` / `Please tell me who you are`**
You skipped the `git config` commands in Step 0. Run them, then commit again.

**`nothing to commit, working tree clean`**
Your files aren't where you think. Run `git status` and `ls`. Usual cause: you built your project somewhere outside the cloned folder.

**Committed something huge by accident (`node_modules`, datasets, `venv`)**
Create a `.gitignore` in your folder listing those directory names, one per line. If they're already committed, `git rm -r --cached node_modules` (with the right name), then commit again.

**Anything else**
Paste the full error into a search engine and read the first Stack Overflow result. Git's errors are extremely well documented and someone has hit yours before. This is genuinely how everyone does it.

---

## What happens next

**Round 2** is a technical interview, mostly a conversation about the project you submitted. If you're shortlisted you'll hear from us soon.

If you don't clear Round 1, you can still sit for your second preference recruitment. You are not out of the club.

Good luck. Build something you find interesting.

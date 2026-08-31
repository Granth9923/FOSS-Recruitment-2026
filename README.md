# FOSS United SIT — Technical Recruitment 2026

**Task:** build a project, submit it as a pull request to this repository.
**Deadline:** 1 September 2026, 11:59 PM IST.

---

## What to build

Anything you want. Any language, any stack.

It doesn't have to be big, original, or impressive. We're not expecting a startup. We want to see that you can build something that works and explain why you built it that way.

Stuck for ideas: a script that automates something annoying, a small game, a website, a CLI tool, a Discord bot, a data analysis with a writeup.

**Use AI tools if you want**, we're not going to police it. But Round 2 is a conversation about your code — what this function does, why this approach, what breaks if we change X. Submit something you can talk through. Don't submit a classmate's work as your own.

---

## Where it goes

This repo contains nothing but this README. Everything else in it will be submissions.

```
README.md              <- leave this alone
firstname_lastname/
  README.md            <- yours, required
  ... your code ...
```

Folder name lowercase with an underscore: `aditi_sharma`, not `Aditi Sharma`.

**Your README must cover:** what the project does (2-3 sentences), the exact commands to run it, and anything you found hard or would do differently. That last one isn't filler — it often tells us more than the code does.

Don't touch anything outside your folder.

---

## How to submit

Never used GitHub? That's fine, it's not what we're testing. This is about ten minutes of copy-pasting. If something breaks, see [Common errors](#common-errors).

**0. Install git.**
`sudo apt install git` (Ubuntu) · `sudo dnf install git` (Fedora) · `brew install git` (macOS) · [git-scm.com](https://git-scm.com/download/win) (Windows — accept all defaults, then use **Git Bash**, not Command Prompt).

Then, once ever:

```bash
git config --global user.name "Your Name"
git config --global user.email "your@email.com"
```

Git refuses to commit if it doesn't know who you are.

**1. Fork this repo.** Click **Fork** at the top right → **Create fork**. That's your own copy, on your account, where nothing you do affects ours.

**2. Clone your fork.** This downloads it to your laptop. On *your fork's* page: green **Code** button → copy the HTTPS URL.

```bash
git clone https://github.com/YOUR-USERNAME/recruitment-2026.git
cd recruitment-2026
```

That URL needs *your* username in it, not ours.

**3. Make your folder and build.**

```bash
mkdir aditi_sharma
cd aditi_sharma
```

Your name, obviously. Write your project in here.

**4. Commit.** A commit is a saved snapshot. Run from anywhere inside the repo:

```bash
git add .
git commit -m "Add submission by Your Name"
```

Commit as often as you like while working.

**5. Push.** This uploads your commits to your fork.

```bash
git push origin main
```

It'll ask for a username and password. Your GitHub password won't work — see [Authentication](#authentication).

**6. Open the pull request.** On your fork, click the **Compare & pull request** banner (or **Contribute** → **Open pull request**).

Check the arrow reads `fossunited-sit/recruitment-2026 : main` ← `YOUR-USERNAME/recruitment-2026 : main`.

Title it `Submission — Your Name`, and put this in the description:

```
Name:
PRN:
Branch/Division:
Project: one line about what you built
```

**Create pull request**, and you're done. Your PR must be open by the deadline — commits pushed after it are ignored, so don't cut it fine.

---

## Authentication

**Easiest:** install [GitHub CLI](https://cli.github.com/), run `gh auth login`, choose **GitHub.com** → **HTTPS** → **Login with a web browser**. Done permanently.

**Or use a token:** [github.com/settings/tokens](https://github.com/settings/tokens) → **Generate new token (classic)** → any name, 30 day expiry, tick **repo** → generate, then copy the `ghp_...` string. **Copy it immediately, GitHub never shows it again.** Paste that as the password when `git push` asks; username is your normal one.

> The terminal shows nothing while you paste a password. That's normal, not a bug. Paste (`Ctrl+Shift+V`, or `Cmd+V` on macOS) and press Enter.

---

## Common errors

**`fatal: not a git repository`** — wrong folder. `cd recruitment-2026` first. Check with `pwd`.

**`Authentication failed` / `password authentication was removed`** — you used your GitHub password. See [Authentication](#authentication).

**`Permission denied` / `403` when pushing** — you cloned our repo, not your fork. Check `git remote -v`; if your username isn't in the URL, delete the folder and redo step 1.

**`Updates were rejected...`** — run `git pull origin main --rebase`, then push again.

**`Author identity unknown`** — you skipped the `git config` commands in step 0.

**`nothing to commit, working tree clean`** — your files aren't where you think. Run `git status` and `ls`. Usually means you built your project outside the cloned folder.

**Committed something huge (`node_modules`, datasets, `venv`)** — add a `.gitignore` in your folder listing those names. If already committed: `git rm -r --cached node_modules`, then commit again.

**Anything else** — paste the full error into a search engine and read the first Stack Overflow result. Git errors are extremely well documented and someone has hit yours before.

---

## What happens next

**Round 2** is a technical interview, mostly a conversation about the project you submitted. If you're shortlisted you'll hear from us soon.

If you don't clear Round 1, you can still sit for your second preference recruitment. You are not out of the club.

Good luck. Build something you find interesting.

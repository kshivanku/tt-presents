# tt-presents

**What is cool**, according to the design team, one line each. You add your line through a
pull request, Shivanku merges it, and the list grows on the live page:

**https://kshivanku.github.io/tt-presents/**

Your line says what you think is cool. Anything goes: "Frog is cool" counts.

## The rules

1. **Change only your own line.** Find your name in `PLAY.md` and replace
   `_(write your line here)_` with your line. Leave everything else alone, including the blank
   lines. Each slot has untouched lines around it, and that space is what lets 26 people's
   changes combine without clashing.
2. **Keep it work-safe and keep Thumbtack out of it.** This repo is public, so anyone on the
   internet can read it. No unreleased features, customer details, metrics, or names of
   people who aren't in the class.
3. **Don't merge your own pull request, or anyone else's.** GitHub will let you, but that's
   Shivanku's job today.

## Before class: accept your invite

Shivanku added you as a collaborator, which lets you put a branch on this repo. Open
**https://github.com/kshivanku/tt-presents/invitations** and click **Accept invitation**.
Until you do, GitHub will refuse your upload in step 4.

## The steps

Do these in Claude Code, one prompt at a time. Read what Claude tells you after each one.
Replace the parts in `<angle brackets>`.

### 1. Get a copy of the repo

> Clone https://github.com/kshivanku/tt-presents and open it.

**What happens:** *Cloning* downloads the whole repo to your Mac: every file, plus the history
of every change ever made. Your copy stays linked to the one on GitHub, so you can send changes
up and pull other people's changes down later.

### 2. Make your own branch

> Create a new branch called `<firstname>/my-line` and switch to it.

**What happens:** A *branch* is your own version of the project, where you can make changes
without touching anyone else's. The main version is called `main`. Nobody edits `main`
directly. Changes reach it only through a pull request.

### 3. Write your line

> In PLAY.md, replace the placeholder after **`<YOUR NAME>`:** with this line:
> "`<something>` is cool". Don't change anything else. Then show me the diff.

**What happens:** Claude edits one line of the file. The *diff* is the list of what changed:
the old line in red, your new line in green. It should show exactly one line changed. If it
shows more, tell Claude to undo everything except your line.

### 4. Save it and send it to GitHub

> Commit this with the message "Add `<firstname>`'s line" and push my branch to GitHub.

**What happens:** A *commit* is a saved snapshot of your change, with a message saying what
you did. It's saved on your Mac only. *Pushing* uploads your branch and its commit to GitHub,
so other people can see it.

### 5. Open a pull request

> Open a pull request from my branch into main, titled "`<firstname>`'s line". Give me the link.

**What happens:** A *pull request* (PR) asks to have your branch merged into `main`. It shows
the reviewer your diff and gives them a place to comment, ask for changes, or approve. Open
the link and look at the **Files changed** tab. That's what Shivanku sees.

### 6. Wait for the review

Shivanku will merge your PR or leave a comment. If there's a comment, read it on the PR page.
If the comment asks for a change, tell Claude:

> Shivanku asked me to change my line to "`<new line>`". Update it, commit, and push to the
> same branch.

The PR updates by itself. You don't open a new one.

### 7. Get everyone else's lines

Once your PR is merged:

> Switch back to main, pull the latest changes, and show me PLAY.md.

**What happens:** *Pulling* downloads everything merged on GitHub since you cloned, so you now
have everyone's lines that have been merged so far. Run this again later to get the rest, or
watch the live page, which checks for new lines every 30 seconds.

## If something goes wrong

- **"Permission denied" or "403" when pushing:** you haven't accepted the invite yet. See
  *Before class* above, then ask Claude to push again.
- **"Protected branch" or "changes must be made through a pull request":** your commit landed
  on `main` instead of your branch. Ask Claude: *"Move my commit off main onto a new branch
  called `<firstname>`/my-line, reset main to match GitHub, and push the new branch."*
- **Claude mentions a "merge conflict":** stop and tell Shivanku. It shouldn't happen if
  everyone changes only their own line.
- **Your name isn't in PLAY.md:** tell Shivanku.

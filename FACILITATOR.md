# Facilitator run sheet

Your notes for running the exercise. Designers follow `README.md`; this file is for you.

- Repo: https://github.com/kshivanku/tt-presents
- Live page: https://kshivanku.github.io/tt-presents/
- Invite page designers use: https://github.com/kshivanku/tt-presents/invitations

## Before class

### 1. Repo settings

- [ ] Public repo `kshivanku/tt-presents` created, files pushed to `main`.
- [ ] GitHub Pages on: **Settings → Pages → Deploy from a branch → `main` / root**.
- [ ] `main` protected: **Settings → Branches → Add rule** for `main`, with
  **Require a pull request before merging** turned on.
  - Set **Required approvals** to 0. With 1, you'd have to click Approve on all 26 PRs
    before merging, and collaborators could approve each other's.
  - Leave **Require branches to be up to date** off. With it on, every PR would go stale
    the moment you merged another one, and each designer would have to update their
    branch before you could merge.
- [ ] Merging set to match Thumbtack's iOS repo: **Settings → General → Pull Requests**, with
  only **Allow squash merging** on (default message: pull request title) and
  **Automatically delete head branches** on.

### 2. Collaborator invites

Send each invite from **Settings → Collaborators → Add people**, or ask Claude Code to send
them with `gh`. Each designer then accepts at the invite page above.

"Confirmed" means their Thumbtack email is on commits in `thumbtack/prototyping-playground`,
or their GitHub profile shows their name. "Likely" means a matching username in the Thumbtack
org with no name on the profile. Ask the "likely" people to confirm before you invite, since
an invite to the wrong account goes to a stranger.

| Designer | GitHub username | How sure | Invited | Accepted |
|---|---|---|---|---|
| Adam Ahmed | heyitsadam1 | Confirmed | [ ] | [ ] |
| Aditya Nair | adi-nair-dev | Confirmed | [ ] | [ ] |
| Anaïs Ziae-Mohseni | anaiszm | Confirmed | [ ] | [ ] |
| Andre Wyatt Robb | awyattrobb | Confirmed | [ ] | [ ] |
| Britt Flaming | brittflaming-tt | Confirmed | [ ] | [ ] |
| Craig Murray | cmurray-cam | Confirmed | [ ] | [ ] |
| Daphne Shin | dshin-tt | Likely | [ ] | [ ] |
| Dave Bellona | davidbellona-ai | Confirmed | [ ] | [ ] |
| Dave Handlong | designer-dave | Confirmed | [ ] | [ ] |
| Erik Goens | egoens | Confirmed | [ ] | [ ] |
| Erin Hogan | ehogan17 | Likely | [ ] | [ ] |
| Fede Nigro | Fehdeh | Confirmed | [ ] | [ ] |
| Grace Cha | gracecha212 | Likely | [ ] | [ ] |
| Hanna Jang | hjang485 | Confirmed | [ ] | [ ] |
| Jaclyn Mann | jaclynrm | Likely | [ ] | [ ] |
| Joe Tutterow | jtutterow-design | Confirmed | [ ] | [ ] |
| John Williams | johnwilliams-tt or jowilliamsthumbtack? | Unsure | [ ] | [ ] |
| Julian Borsellino | JBorsellino158 | Confirmed | [ ] | [ ] |
| Kallen Michaels | kmichaelstt | Confirmed | [ ] | [ ] |
| Kiran Ramsey | kramsey-tt | Likely | [ ] | [ ] |
| Malia Eugenio | maliaeugenio | Likely | [ ] | [ ] |
| Melissa Hribar | mmhribar | Confirmed (opened PRs, no name on profile) | [ ] | [ ] |
| Pauline Nidea | pnidea | Likely | [ ] | [ ] |
| Rachel Sanfilippo | ? | Not found | [ ] | [ ] |
| Saygun Erkaraman | ? | Not found | [ ] | [ ] |

### 3. Send designers the README

Share the repo link and ask everyone to accept their invite before class.

## During class

1. **Show the empty play.** Open the live page on the shared screen: "0 of 26 lines
   written." Leave it up all session. It checks for new lines every 30 seconds and
   highlights each new one as it arrives.
2. **Walk through the idea.** `main` is the official version. Everyone makes a branch, changes
   one line, and asks to merge it with a pull request. You review and merge.
3. **Let them work through README steps 1–5.** PRs show up at
   https://github.com/kshivanku/tt-presents/pulls.
4. **Review each PR on the shared screen.**
   - Open the PR, then the **Files changed** tab. Exactly one line should change: their
     placeholder.
   - To comment: hover over the line, click the **+**, write the comment, and choose
     **Start a review**, then **Finish your review → Comment**.
   - To ask for a change: **Finish your review → Request changes**. The designer pushes a
     fix to the same branch (README step 6) and the PR updates.
   - To merge: back on the **Conversation** tab, click **Squash and merge → Confirm squash and
     merge**. All the PR's commits become one commit on `main`, titled with the PR's title,
     and GitHub deletes the branch because it's no longer needed. Squash and merge is the
     only option, matching Thumbtack's iOS repo.
5. **Watch the live page update.** Pages takes about a minute to publish after each merge.
6. **Have everyone pull** (README step 7) to see that their copy now has other people's lines.

Do one PR very slowly, ideally from someone new to this, with a comment and a requested
change, so the class sees the full round trip. Then speed up and merge the rest.

## After class: show the history

- **Who wrote which line:** open `PLAY.md` on GitHub and click **Blame**. Every line shows
  who last changed it and in which commit.
- **Every change in order:** the **Commits** link on the repo's main page. Each merged PR is
  one commit, so the list reads like the order lines arrived.
- **What happened inside one PR:** open a closed PR and its **Commits** tab. The typo fixes
  and other in-between commits are still there, even though `main` only got the squashed one.

## If something goes wrong

- **A PR changes more than one line:** request changes and ask them to undo everything except
  their line.
- **A PR shows "This branch has conflicts":** someone edited lines outside their slot, or two
  people edited the same slot. Open the PR's diff to see which. The simplest fix is to ask the
  designer to close the PR, delete their branch, and start again from step 1 with a fresh
  copy of `main`.
- **Someone can't push:** they haven't accepted their invite, or the invite went to the wrong
  username. Check **Settings → Collaborators**.
- **The live page doesn't update:** check **Actions** on the repo. Each merge starts a "pages
  build and deployment" run. A red one means the publish failed.

# My Progress

## Where I am

- **Learning path stage:** 1. Concepts ✅ · 2. Setup ✅ · 3. Daily basics in Claude Code ✅ · 4. GitHub basics ✅
- **Next up:** Push branch `faq-more-entries` and open/merge pull request #2. Then **5. Team collaboration** (sharing one repo, simple conflicts, folder conventions).

---

## Session log

### 2026-11-04: Connecting Claude Code to GitHub

**What I did**
- Cloned (downloaded a linked copy of) this repo to `~/code/sales-claude-training`.
- Opened it in Claude Code so Claude can read and edit the files.
- Signed in to GitHub from Terminal with `gh auth login` (account: `gabrielaecheverri-dev`).
- Confirmed I have Admin access to the repo and that pushing works.
- Created my first branch: `docs/setup-faq-and-progress`.

**What I learned**
- Claude Code works on a **local copy** of the repo on my Mac. GitHub holds the shared copy.
- Signing in to GitHub (`gh auth login`) is what lets me **push** (send my changes up to GitHub).
- A **branch** is a separate working copy where I can make changes without touching the main version, like drafting a proposal in a copy before replacing the official one.

**What confused me** (added to `training/faq-troubleshooting.md`)
- `command not found: gh` right after installing: I needed to open a **new** Terminal tab.
- GitHub's "Ooops!!! 500" page during sign-in: that was GitHub's problem, not mine. Retrying fixed it.

**Open questions**
- _(add any here)_

### 2026-11-06: Concepts (Lesson 1)

**What I learned**
- **Claude Code vs. regular Claude:** Claude Code works directly on files in a folder on my Mac (with my permission). Regular Claude is a chat I copy from.
- **Git** = version tracker on my Mac. **GitHub** = the team's shared online copy (like a shared drive).
- **Repository** = a tracked project folder with its full history. **Commit** = save a version with a note (on my Mac only).
- **Branch** = my own working copy so I don't touch `main`. **Push** = send my commits up to GitHub. **Pull** = bring the team's latest down.
- **Pull request** = I ask for my branch to be reviewed and merged into `main`; my manager/teammate reviews and approves.
- Full cycle: pull → branch → commit → push → pull request → review → merge.

**Quick check:** 3/3 ✅
- Small clarification: *I* open the pull request; the manager *reviews and approves* it.

**What confused me**
- Jumping into commands before knowing the concepts. Lesson for the team training: **teach concepts before commands.**

### 2026-11-06: My first commit, push and pull request

**What I did**
1. `cd ~/code/sales-claude-training`: went into the project folder.
2. `git status`: saw my new files in red (untracked).
3. `git add notes training`: put them "in the envelope" (now green).
4. `git config --global user.name / user.email`: told Git who I am (one-time setup).
5. `git commit -m "..."`: saved a version on my Mac.
6. `git push -u origin docs/setup-faq-and-progress`: sent my branch to GitHub.
7. Opened pull request #1 on the GitHub website.

**What confused me**
- I first mixed up commit and push. Commit = save on my Mac; push = send to GitHub.
- First commit needs your name/email set up, or Git refuses. Add to FAQ for the team.

**Quick check:** 2/4. Got name/email setup and "review before merge" right.
- Mixed up **add** vs. **commit**: green in `git status` = *staged* (in the envelope), **not** committed yet.
- Mixed up **commit** vs. **push**: if a commit is missing on GitHub, the missing step is `git push`.
- Memory aid: **add = choose · commit = save (my Mac) · push = send (GitHub)**.
- For the team training: these three are the hardest to keep apart. Spend extra time here.

### 2026-11-09: Second round (I led it) + first merge

**What I did**
- Committed and pushed my notes update myself: it joined pull request #1 automatically.
- Asked for (and added) `training/cheat-sheet.md` with every Terminal command.
- Reviewed **Files changed**, merged pull request #1, deleted the branch on GitHub.
- Back on my Mac: `git switch main` → `git pull` to get the merged version.

**What confused me**
- Forgot the quotes in `git commit -m`. Git read only the first word and saved nothing. Add to FAQ.
- Remember: commits join the PR when you **push**; **merge** adds the whole PR to `main`.

**Good to know**
- After `git switch main`, files from my branch "disappear" until I `git pull`. That's normal.

**Quick check (full cycle):** 1 of 3 mostly right. Review these before the next lesson:
- `cd` goes into a **folder**, not a branch. Branches are changed with `git switch`.
- `git status` only **looks** at my Mac; it doesn't download anything. To get the latest: `git switch main` → `git pull`.
- Fixes after review: **don't** open a new pull request. Fix → add → commit → push on the **same branch**, and it joins the existing one.
- **pull ≠ pull request.** `git pull` = download the latest from GitHub. Pull request = ask for review on GitHub. Confusing names! Add to the glossary/FAQ for the team.

### 2026-11-10: Lesson 3, daily basics in Claude Code

**What I learned**
- **Session** = one conversation, inside **one folder**. One topic per session.
- **Asking for changes:** plain words. Say **which file**, **what** to change, **who it's for**, **what format**.
- **Reviewing:** always before committing. Open the file, or `git diff` in Terminal (Space to scroll, q to quit).
- **Permission prompts:** Allow if I understand it and asked for it; if in doubt, Deny and ask.
- **Slash commands:** typed in the **Claude chat box**, not Terminal. `/help`, `/rewind` (= `/undo`), `/clear`, `/usage`, `/memory`, `/init`.
- **CLAUDE.md** = standing instructions Claude reads every session; shared with the team through GitHub.
- Practiced: started branch `faq-more-entries`, briefed Claude to add 2 FAQ entries, reviewed, committed.

**What confused me**
- Typed `/` in **Terminal** → "permission denied". Slash commands go in the Claude chat box. Added to FAQ.
- Step 2 of the exercise ("write me a request") wasn't clear: I didn't realize I just had to type it in the chat. For the team: show an example request first.

**Quick check:** 1 of 4 fully right, 3 partly.
- Undo options: tell Claude "undo that" / ask for a fix, or `/rewind` (`/undo`). `git diff` only **shows** changes; it doesn't undo.
- Repeated instructions → put them in **`CLAUDE.md`**.
- A good request also names the **file** and **exactly what to change**, not just audience and style.

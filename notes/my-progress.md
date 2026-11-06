# My Progress

## Where I am

- **Learning path stage:** 1. Concepts ✅ done · 2. Setup (mostly done)
- **Next up:** Review and merge my first pull request (#1), then pull the updated `main`.

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

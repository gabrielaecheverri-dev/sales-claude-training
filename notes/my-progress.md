# My Progress

## Where I am

- **Learning path stage:** 1. Concepts ✅ done · 2. Setup (mostly done)
- **Next up:** Hands-on: commit and push my FAQ + progress notes, then open my first pull request.

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

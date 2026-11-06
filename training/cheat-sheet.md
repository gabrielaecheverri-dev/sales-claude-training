# Cheat Sheet: Terminal Commands for GitHub

**Goal:** Every command you need to save and share your work, on one page.
**Time:** 2 minutes to read. Keep it open while you work.

**Where to type:** the **Terminal** app on your Mac. Type a command, then press **Return**.

**Remember:** **add = choose · commit = save (your Mac) · push = send (GitHub)**

---

## 1. One-time setup (only the first time, on a new Mac)

| What you want to do | Command |
|---|---|
| Sign in to GitHub | `gh auth login` → choose **GitHub.com** → **HTTPS** → **Yes** → **Login with a web browser** |
| Tell Git your name | `git config --global user.name "Your Name"` |
| Tell Git your email | `git config --global user.email "you@company.com"` |
| Download the team repo to your Mac | `git clone https://github.com/gabrielaecheverri-dev/sales-claude-training.git ~/code/sales-claude-training` |

---

## 2. Every time you start working

| Step | What it does | Command |
|---|---|---|
| Go to the project folder | Like double-clicking into the folder in Finder | `cd ~/code/sales-claude-training` |
| Switch to the official version | Go back to `main` | `git switch main` |
| Get the team's latest changes | **Pull**: download what others added | `git pull` |
| Start a new branch for your work | Your own working copy, so `main` stays safe | `git switch -c my-branch-name` |

> **Branch name tip:** short, with dashes, describing the work. Example: `followup-email-template`

---

## 3. Save and share your work

| Step | What it does | Command | What you should see |
|---|---|---|---|
| 1. Check what changed | "What's new since my last save?" | `git status` | Changed files in **red** |
| 2. **Add** (choose) | Put files in the envelope | `git add file-name` or `git add .` (everything) | Run `git status` again: files are **green** |
| 3. **Commit** (save) | Seal and label the envelope (saved on your Mac only) | `git commit -m "What you did"` | `1 file changed...` |
| 4. **Push** (send), first time on a new branch | Send your branch to GitHub | `git push -u origin my-branch-name` | `* [new branch]` |
| 4. **Push** (send), after the first time | Send new commits on the same branch | `git push` | `abc1234..def5678` |

> **Don't forget the quotes** in your commit message: `git commit -m "Add discovery call template"`. Without them, Git gets confused.

---

## 4. Ask for review (on the GitHub website, not in Terminal)

1. Open the repo on GitHub and click the yellow **"Compare & pull request"** banner (or use the link Terminal shows after your push).
2. Add a title and a short description of what you changed and why.
3. Click **Create pull request**.
4. A teammate reviews it, then clicks **Merge pull request**.

> **Need to fix something after review?** Just make the change, then **add → commit → push** again on the same branch. It joins the same pull request automatically.

---

## 5. After your pull request is merged

| Step | Command |
|---|---|
| Go back to the official version | `git switch main` |
| Get the merged changes | `git pull` |

---

## Handy extras

| What you want to do | Command |
|---|---|
| Which branch am I on? | `git status` (first line) or `git branch` |
| See recent saved versions | `git log --oneline` |
| Cancel a command that's running | Press **Ctrl+C** |
| "command not found" right after installing | Open a **new** Terminal tab (**Cmd+T**) |

> **Golden rules:** Never commit passwords or confidential client documents. Always run `git status` before you commit. Work on a branch, never directly on `main`.

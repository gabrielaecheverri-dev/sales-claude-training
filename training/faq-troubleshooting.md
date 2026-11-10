# FAQ & Troubleshooting

**Goal:** Quickly fix the most common problems you'll run into with Claude Code and GitHub.
**Time:** 1–2 minutes per issue.

Don't worry, everyone hits these. If you find a new one, tell your trainer so we can add it here.

---

## Setup

### "command not found" right after installing something

**What you see:** You installed a tool (for example the GitHub CLI, `gh`) and then typed a command in Terminal, and it says:

```
zsh: command not found: gh
```

**What went wrong:** Your Terminal window was already open before the install, so it doesn't know about the new program yet. It's like a phone contact list that hasn't synced: the contact exists, but your phone hasn't picked it up.

**How to fix it:**

1. Open a **new** Terminal tab (press **Cmd+T**) or close Terminal and reopen it.
2. Type the command again.

**What you should see:** The command runs normally.

> **If something goes wrong:** If it still says "command not found", the install may not have finished. Ask your trainer to check it with you.

---

### GitHub shows an "Ooops!!! 500" page while signing in

**What you see:** While running `gh auth login`, your browser opens GitHub and shows a cartoon octopus-cat with a **500** sign saying "Looks like something went wrong!"

**What went wrong:** GitHub's own website had a temporary hiccup. **It's not something you did.**

**How to fix it:**

1. In your browser, press **Cmd+R** to refresh the page.
2. If it still fails, or says your code expired, go back to Terminal, press **Ctrl+C** to cancel, and run the sign-in again:

   ```
   gh auth login
   ```

   Use the same answers: **GitHub.com** → **HTTPS** → **Yes** → **Login with a web browser**. You'll get a fresh one-time code.

**What you should see:** In the browser, "Congratulations, you're all set!" In Terminal:

```
✓ Logged in as your-github-username
```

> **If something goes wrong:** Check whether GitHub is having an outage at [githubstatus.com](https://www.githubstatus.com). If it is, wait 10–15 minutes and try again.

---

### "permission denied" or "command not found" when talking to Claude

**What you see:** You typed a request or a slash command (like `/help`) and Terminal replied with something like:

```
zsh: permission denied: /
```

**What went wrong:** You typed it in **Terminal** instead of the **Claude app's message box**. Terminal only understands commands like `git status`, not requests to Claude. Nothing broke.

| Window | What you type there |
|---|---|
| **Terminal** (the window with `%`) | Git commands: `git status`, `git add`, `git commit`, `git push` |
| **Claude app** message box | Requests to Claude, and slash commands like `/help` |

**How to fix it:** Click into the Claude app's message box and type it there.

**What you should see:** for a slash command, a menu of commands appears as soon as you type `/`.

---

## Saving your work (commits)

### Git refuses your first commit: "Please tell me who you are"

**What you see:** You run `git commit` for the first time on your Mac and get:

```
Author identity unknown

*** Please tell me who you are.
```

**What went wrong:** Every saved version (commit) is signed with a name and email, so the team can see who changed what. Git doesn't know yours yet. It's like sending your first email from a new account before setting up your signature.

**How to fix it (only once per Mac):**

1. In Terminal, run these one at a time, with your own name and work email:

   ```
   git config --global user.name "Your Name"
   ```

   ```
   git config --global user.email "you@company.com"
   ```

   **What you should see:** nothing. No message means it worked.

2. Run your `git commit` command again.

**What you should see:** `1 file changed...` (or however many files you changed).

> **If something goes wrong:** Check for typos, especially the two dashes in `--global` and the quotes around your name.

---

### You forgot the quotes in your commit message

**What you see:** You typed something like `git commit -m Add discovery call template` (no quotes), and Git shows an error such as:

```
error: pathspec 'discovery' did not match any file(s) known to git
```

**What went wrong:** Without quotes, Git reads only the **first word** (`Add`) as your note and thinks the other words are file names. It gets confused and **saves nothing**. It's like a subject line that cuts off after one word, with the rest scattered around the email.

**Why the quotes matter:** they tell Git "everything in here is one note".

**How to fix it:**

1. Nothing is broken and nothing was saved, so just run the command again **with quotes**:

   ```
   git commit -m "Add discovery call template"
   ```

**What you should see:** `1 file changed...`

> **If something goes wrong:** Run `git status`. If your files show in **red**, they're not in the envelope. Run `git add` on them first, then commit again.

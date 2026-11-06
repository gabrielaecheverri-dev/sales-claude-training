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

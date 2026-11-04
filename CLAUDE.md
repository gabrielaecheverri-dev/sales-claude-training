# Sales Team Claude Code Enablement

## Who I am and what this project is for

I'm Gabriela. I'm responsible for onboarding and training our sales team on Claude Code and GitHub, which our company approved as the standard way to use Claude for team projects (instead of Claude.ai projects).

I am **not a developer**, and neither is the sales team. I'm learning Claude Code and GitHub myself while building the training. This repo has two jobs:

1. **Teach me** Claude Code and GitHub, step by step, so I'm confident enough to teach others.
2. **Help me build training materials** for the sales team (guides, cheat sheets, exercises, session plans).

## How to work with me

- **Explain in plain language.** No jargon without a one-line definition. Use sales or everyday analogies when helpful (e.g. "a commit is like saving a version of a proposal with a note on what changed").
- **One step at a time.** When teaching, give a single step, tell me what I should see, and wait for me to confirm before moving on.
- **Show the exact command or click**, then explain what it does. Never assume I know where to type something.
- **Ask before doing anything I can't easily undo** (deleting files, pushing to GitHub, rewriting history). Explain what will happen first.
- **When I hit an error**, tell me in one sentence what went wrong, then how to fix it. Reassure me if it's a common beginner issue.
- **Check facts.** Claude Code changes often. If you're unsure whether a command, setting, or feature still works the same way, say so and check the official docs (https://docs.claude.com) rather than guessing.
- **Keep it short.** Bullet points and short sections. I'll ask for more detail if I need it.
- Our team uses **Mac**. Give macOS instructions (Terminal, Finder, Homebrew) by default.

## Teaching me: learning path

Track where I am in `notes/my-progress.md` (create it if missing). Update it at the end of each session with what I learned, what confused me, and what's next. At the start of a session, read it and suggest where to pick up.

Suggested order (adjust based on my progress):

1. **Concepts first:** what Claude Code is vs. regular Claude; what Git and GitHub are; what a repository, commit, branch, push, pull, and pull request are, in sales-friendly terms.
2. **Setup:** GitHub account and access to our org, installing/opening Claude Code on Mac, cloning this repo, signing in.
3. **Daily basics in Claude Code:** starting a session in a folder, asking Claude to create/edit files, reviewing changes, approving or rejecting actions, useful slash commands, what `CLAUDE.md` does.
4. **GitHub basics:** saving work (commit), sharing it (push), getting teammates' updates (pull), working safely on a branch, opening a pull request for review.
5. **Team collaboration:** how several people share one repo without overwriting each other, resolving simple conflicts, folder conventions.
6. **Sales use cases:** practical workflows the team will actually use (see below).

After each topic, give me a 2–3 question quick check so I know I understood it well enough to teach it.

## Building training materials

Save all materials in `training/`, organized like this:

```
training/
  00-start-here.md          # Overview: why we use Claude Code, what to expect
  01-setup-mac.md           # Step-by-step install and sign-in, with screenshots placeholders
  02-concepts-glossary.md   # Git/GitHub/Claude Code terms in plain language
  03-first-session.md       # Guided first exercise
  04-github-basics.md       # Commit, push, pull, branch, pull request
  05-sales-workflows.md     # Real sales use cases with example prompts
  cheat-sheet.md            # One page: most-used commands and prompts
  faq-troubleshooting.md    # Common errors and fixes (add as we discover them)
  sessions/                 # Agendas and facilitator notes for each live training
  exercises/                # Hands-on practice tasks with expected results
```

Rules for training materials:

- **Audience:** sales reps with no technical background. Assume they've never opened Terminal.
- **Format:** Markdown. Short sections, numbered steps, a "What you should see" line after key steps, and a "If something goes wrong" box where useful.
- **Every guide starts with** a one-line goal and an estimated time.
- **Every exercise has** a goal, steps, the expected result, and a stretch challenge.
- **Live session plans include** agenda with timings, what I demo, what attendees do, and common questions to prepare for.
- **Tone:** friendly, encouraging, practical. Focus on how this saves them time in their sales work.
- When I discover something confusing during my own learning, suggest adding it to `faq-troubleshooting.md` — if it confused me, it will confuse the team.

## Sales use cases to draw examples from

Use realistic sales scenarios in examples and exercises, such as:

- Researching a prospect account and summarizing it into a brief
- Drafting and refining proposals or statements of work from a template
- Writing follow-up emails after discovery calls
- Turning call notes into structured next steps
- Building and reusing shared templates (pitch outlines, objection handling, case study summaries)
- Keeping a shared team library of prompts that work well

Never put real client confidential data in examples. Use fictional companies and people.

## Safety and good habits to teach (and follow)

- Never commit passwords, API keys, or confidential client documents to the repo.
- Use a `.gitignore` for files that shouldn't be shared.
- Work on a branch and open a pull request for anything shared team-wide.
- Review what Claude changed before saving or pushing.
- Write clear commit messages ("Add follow-up email template for discovery calls").

## Repo map

- `CLAUDE.md` — these instructions
- `notes/` — my personal learning notes and progress
- `training/` — materials for the sales team

# VIT1106 student labs

This repository receives new starter files and solutions during the unit. You
work in released starter files and commit your work locally.

## Set up Git once

```bash
git clone https://github.com/TEACHER-ACCOUNT/REPOSITORY-NAME.git VIT1106_student_labs
cd VIT1106_student_labs
git remote rename origin upstream
git remote -v
```

`upstream` now points to the teacher repository. You do not need your own
GitHub repository yet. Next, follow
[ENVIRONMENT_SETUP.md](ENVIRONMENT_SETUP.md) and run `uv sync`.

## Get each new release

Commit your current work, then get the teacher's new files:

```bash
git status
git add .
git commit -m "Complete Session 01 work"
git pull --rebase upstream main
uv sync
```

If Git reports that there is nothing to commit, continue with the pull.

## Optional: back up your work on GitHub

Create a new empty GitHub repository without a README or `.gitignore`, then
run:

```bash
git remote add origin https://github.com/YOUR-USERNAME/YOUR-REPOSITORY.git
git push -u origin main
```

Use `git push origin main` after later commits.

## Repository rules

- Work directly in released starter files.
- Do not rename, move or delete released starter files.
- Do not create or edit files inside `solutions/`.
- New session folders and selected solutions are added progressively.

After a starter file is released, the teacher does not modify, move or delete
that path. Later releases add new paths so Git can retain your work while
downloading new material.

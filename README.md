# Frontend Version Control Task

A small HTML/CSS frontend project used to practise Git and GitHub collaboration workflows: repository setup, branches, commits, pull requests, reviews, merging, reverting, fetching, pulling, and pushing.

## Project files
- `header.html` and `header.css`: semantic site header, navigation, and responsive styling.
- `footer.html` and `footer.css`: footer navigation and responsive styling.
- `revert-demo.txt`: a minor intentional error and its corrective commit.

## Feature branches and purpose
- `feature-header` — site header, navigation links, responsive styling, and accessibility.
- `feature-footer` — footer, copyright text, navigation, and responsive styling.
- `feature-header-layout` — follow-up branch created from `feature-header` to practise branch renaming/migration workflows.

## Pull requests and review
- [PR #1 — Add accessible responsive site header](https://github.com/MusaGaya/Frontend-version-control-task-MusaGaya/pull/1) — reviewed with comments and merged.
- [PR #2 — Add accessible responsive site footer](https://github.com/MusaGaya/Frontend-version-control-task-MusaGaya/pull/2) — reviewed with comments and merged.

For the submission, open each link and take a screenshot showing its **Merged** status. Screenshots have not been embedded in this README yet.

## Reversion exercise
A minor typo was intentionally committed in `revert-demo.txt`, then corrected in a follow-up commit. In a local clone, practise the actual `git revert` command on a disposable test commit so you can demonstrate the command directly:

```bash
git log --oneline
git revert <commit-sha>
git push
```

## Git commands practised
```bash
git init
git clone <repository-url>
git status
git switch -c feature-header
git add .
git commit -m "feat: add website header"
git push -u origin feature-header
git fetch origin
git pull origin main
git merge feature-header
git revert <commit-sha>
git branch -m feature-header feature-header-layout
git fetch --prune origin
git push -u origin feature-header-layout
```

To fetch and check remote branch updates after a rename:
```bash
git fetch origin --prune
git branch -a
git switch feature-header-layout
```

## Lessons learned
- Feature branches keep work isolated until it is ready to merge.
- Small commits with clear messages make history easier to understand.
- Pull requests make review and discussion part of collaboration.
- `git fetch` updates remote-tracking references; `git pull` fetches and integrates changes.
- `git revert` creates a new commit that undoes a previous commit without rewriting shared history.
- When renaming a branch, update the upstream tracking branch and fetch/prune remote references.

## Final checklist
- [x] Public repository created
- [x] Two feature branches with at least three meaningful commits each
- [x] Two pull requests opened, reviewed with comments, and merged
- [x] Minor error committed and corrected
- [ ] Capture and embed screenshots of the two merged PRs
- [ ] Complete a local `git revert` and remote branch rename/fetch demonstration if your mentor requires terminal evidence

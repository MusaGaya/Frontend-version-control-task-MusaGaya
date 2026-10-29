# Frontend Version Control Task

A small HTML/CSS frontend project used to practise Git and GitHub collaboration workflows: repositories, branches, commits, pull requests, review, merging, reverting, fetching, and pushing.

## Project files
- `header.html` and `header.css`: accessible site header and responsive styling.
- `footer.html` and `footer.css`: footer navigation and responsive styling.

## Feature branches
- `feature-header` — builds the site header, navigation links, and responsive header styling.
- `feature-footer` — builds the footer, footer navigation, and responsive footer styling.

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
git branch -m old-name new-name
git push origin --delete old-name
```

## Pull request evidence
PR links and merge status should be recorded here after the pull requests are reviewed and merged. Add screenshots of the merged pull requests before submitting.

## Lessons learned
- Branches keep feature work separate from the main branch.
- Small commits with clear, imperative messages make project history easier to review.
- Pull requests provide a place to discuss changes before merging.
- Fetching updates remote-tracking references; pulling fetches and integrates changes.
- `git revert` creates a new commit that undoes an earlier commit without rewriting shared history.
- Branch renames should be followed by fetching/pruning remote references as needed.

## Note
This repository is a learning exercise. Record only workflows that were actually completed, and attach real screenshots of GitHub pull request history for the final submission.

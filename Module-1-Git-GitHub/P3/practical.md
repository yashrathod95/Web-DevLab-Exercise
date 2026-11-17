# Practical 3: Feature-Branch Git Workflow

## Aim
To understand and implement the feature-branch workflow in Git for managing project changes separately from the main branch.

## Theory
Git branching allows developers to work on different features independently without affecting the main branch.

- Main branch: Contains the stable version of the project.
- Feature branch: Used to develop new features.
- Merge: Combines changes from one branch into another.

## Procedure
1. Open the project folder in VS Code.
2. Check the current Git branch.
3. Create a new feature branch.
4. Switch to the feature branch.
5. Make changes to the project.
6. Add and commit the changes.
7. Switch back to the main branch.
8. Merge the feature branch into the main branch.

## Terminal Commands

```bash
git branch
git branch feature-navbar
git switch feature-navbar
git status
git add .
git commit -m "Add navbar feature"
git switch main
git merge feature-navbar
git branch
```

## Explanation of Commands

- `git branch` – Displays available branches.
- `git branch feature-navbar` – Creates a new branch.
- `git switch feature-navbar` – Switches to the feature branch.
- `git add .` – Stages modified files.
- `git commit -m` – Saves changes.
- `git switch main` – Returns to the main branch.
- `git merge feature-navbar` – Merges the feature branch into the main branch.

## Folder Structure

```text
P3/
├── practical.md
└── screenshots/
```

## Result
Successfully learned the Git feature-branch workflow by creating a separate branch, committing changes and merging the feature branch into the main branch.
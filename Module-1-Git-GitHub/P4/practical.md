# Practical 4: GitHub README and Version Tags

## Aim
To create a README file for project documentation and learn how to create version tags using Git.

## Theory
A README file provides information about a project, including its purpose, features, technologies used and instructions.

Git tags are used to mark important points in a repository's history, such as software releases.

## Procedure
1. Open the project folder in VS Code.
2. Create a README.md file.
3. Add project information to the README file.
4. Stage and commit the changes.
5. Create a version tag.
6. Display the available tags.

## Terminal Commands

```bash
touch README.md
git add README.md
git commit -m "Add project README"
git tag v1.0
git tag
git show v1.0
```

## Sample README Content

```markdown
# My Portfolio

## About
This is my personal portfolio website.

## Technologies Used
- HTML
- CSS
- JavaScript

## Features
- Home section
- About section
- Skills section
- Contact section
```

## Explanation of Commands

- `touch README.md` – Creates a README file.
- `git add README.md` – Adds the README file to the staging area.
- `git commit -m` – Saves the changes.
- `git tag v1.0` – Creates a version tag.
- `git tag` – Lists available tags.
- `git show v1.0` – Displays tag details.

## Folder Structure

```text
P4/
├── practical.md
└── screenshots/
```

## Result
Successfully created project documentation using a README file and learned to create and display version tags in Git.
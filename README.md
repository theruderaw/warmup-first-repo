# Git Branching and Pull Request Workflow

## Added README File

### Pushing README — Terminal Commands

```bash
rudra@rudra-Dell:~/dev$ git clone https://github.com/theruderaw/warmup-first-repo.git
rudra@rudra-Dell:~/dev/warmup-first-repo$ git checkout -b readme
Switched to a new branch 'readme'

rudra@rudra-Dell:~/dev/warmup-first-repo$ git add .

rudra@rudra-Dell:~/dev/warmup-first-repo$ git commit -m "Added readme"
[readme (root-commit) 5f7d6f0] Added readme
 1 file changed, 1 insertion(+)
 create mode 100644 README.md

rudra@rudra-Dell:~/dev/warmup-first-repo$ git push --set-upstream origin readme
Enumerating objects: 3, done.
Counting objects: 100% (3/3), done.
Writing objects: 100% (3/3), 226 bytes | 226.00 KiB/s, done.
Total 3 (delta 0), reused 0 (delta 0), pack-reused 0 (from 0)
To github.com:theruderaw/warmup-first-repo.git
 * [new branch]      readme -> readme
branch 'readme' set up to track 'origin/readme'.
```

---

## Pull Request Procedure

After pushing the `readme` branch to GitHub, the following steps were followed to create a Pull Request.

### 1. Open the Repository

Open the repository on GitHub.

Since the `readme` branch was recently pushed, GitHub displays an option to create a Pull Request.

### 2. Create a Pull Request

Click **Compare & pull request**.

The Pull Request compares:

```text
base:    main
compare: readme
```

This means that the changes from the `readme` branch will be proposed for merging into the `main` branch.

### 3. Add Pull Request Details

A title and description are added to explain the changes.

Example:

```text
Title:
Add README file
```

The description can explain that a README file was added to the repository.

### 4. Review the Changes

Before merging, the changes are reviewed to verify that:

- The correct branch is being merged.
- The README file was added correctly.
- No unintended changes were included.

### 5. Merge the Pull Request

After reviewing the changes, the Pull Request is merged into the `main` branch.

The `readme` branch can then be deleted if it is no longer required.

---

## Git Workflow

```text
main
 │
 └── readme
      │
      ├── Create README.md
      ├── git add .
      ├── git commit
      └── git push
             │
             ▼
        Pull Request
             │
             ▼
        Code Review
             │
             ▼
        Merge into main
             │
             ▼
       Delete readme branch
```

---

## Key Takeaways

- A separate branch was created for the README-related work.
- Changes were committed to the `readme` branch.
- The branch was pushed to the remote GitHub repository.
- A Pull Request was created to merge the changes into `main`.
- The Pull Request workflow allows changes to be reviewed before they are merged.
- Feature branches help keep the `main` branch stable and organized.

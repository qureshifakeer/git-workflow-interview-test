git second day started
NAME:MUHAMMED SUFIYAN
### 1. Explain the Git Commit Workflow.

The Git commit workflow has 3 main areas:

* **Working Directory:** Where we create files and write code.
* **Staging Area:** Where we prepare files for saving using `git add`.
* **Local Repository:** Where changes are permanently saved in history after running `git commit`.

---

### 2. What is the purpose of .gitignore?

The purpose of `.gitignore` is to tell Git which files or folders to ignore and not track (for example: `node_modules`, log files, build folders, or `.env`).

---

### 3. Why should .env files not be committed?

`.env` files contain sensitive information like database passwords, secret keys, and API tokens. Committing them to Git can leak secrets publicly and cause security issues.

---

### 4. What is the difference between Tracked and Untracked files?

* **Tracked files:** Files that Git already knows about, which were previously committed or are currently staged.
* **Untracked files:** New files created in the project that have never been added to Git using `git add`.

---

### 5. Why are meaningful commit messages important?

They help us and our team members easily understand what changes were made in each step, making it simple to track down bugs and review project history later.

---

### 6. What is a Git Tag?

A Git tag is a reference or label pointing to a specific point in commit history, commonly used to mark release milestones (like `v1.0` or `v2.0`).

---

### 7. Difference between Lightweight Tag and Release Version (Annotated Tag)?

* **Lightweight Tag:** A simple bookmark or pointer pointing directly to a commit, with no extra details.
* **Annotated Tag (Release Version):** Stores full metadata including tagger name, email, date, and a specific release message.

---

### 8. What does git restore do?

It discards uncommitted changes in the working directory and restores files back to the last committed state.

---

### 9. Difference between git restore and git reset?

* **`git restore`:** Modifies uncommitted changes in the working directory or staging area without changing commit history.
* **`git reset`:** Moves the commit history (HEAD pointer) backward to undo commits.

---

### 10. What does git restore --staged do?

It removes files from the staging area (`git add`) back to the working directory without losing or deleting any code changes.

---

### 11. What is Soft Reset?

`git reset --soft` undoes the commit but keeps all code changes safely in the staging area.

---

### 12. What is Mixed Reset?

The default reset (`git reset --mixed`). It undoes both the commit and staging, but keeps all code safe in the working directory as unstaged changes.

---

### 13. What is Hard Reset?

`git reset --hard` completely deletes the commit, un-stages files, and wipes all code changes in the working directory, returning everything strictly to the specified commit.

---

### 14. Which reset type is safest and why?

**Soft Reset** is the safest because it never loses any work; all modified code stays safe in the staging area ready to commit again.

---

### 15. When should Hard Reset be avoided?

Avoid hard reset when working on shared branches pushed to GitHub, or when you have uncommitted work in your working directory that you do not want to lose permanently.

---

### 16. What happens to the staging area after Mixed Reset?

The staging area is cleared (unstaged), and the modified files are moved back to unstaged changes in the working directory.

---

### 17. What command displays commit history in one line?

```bash
git log --oneline

```

---

### 18. How do you view all tags in a repository?

```bash
git tag

```

---

### 19. How do you inspect a specific tag?

```bash
git show <tag-name>

```

*(Example: `git show v1.0`)*

---

### 20. Explain a real-world scenario where Git Tags are useful.

When deploying a stable production release (like `v1.0`), we tag that commit. If a bug occurs later in development, developers can instantly checkout or rollback to that exact production tag without guessing commit hashes.

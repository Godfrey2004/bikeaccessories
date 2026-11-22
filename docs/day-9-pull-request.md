# Day 9 – Pull Requests, Code Reviews & Team Collaboration

**Project:** bike_accessories_project  
**Module:** Git & GitHub – Version Control and Collaboration  
**Learning Type:** Practical Implementation

---

## 1. Learning Objectives

- Understand GitHub Pull Requests (PR).
- Learn how developers collaborate using feature branches.
- Understand the code review process.
- Learn how to handle review feedback.
- Understand different Git merge strategies.
- Follow professional team collaboration workflows.

## 2. What is a Pull Request (PR)?

A Pull Request is a request to merge changes from one branch into another branch.

**Example:**

In bike_accessories_project, suppose we create a new documentation file in a feature branch. Instead of directly modifying `main`, we push our changes to GitHub and create a Pull Request.

The reviewer checks the changes before approving the merge.

**Key Terminologies:**

| Term | Explanation |
|---|---|
| Pull Request | Request to merge changes into another branch |
| Source Branch | Branch containing our changes |
| Target Branch | Branch receiving the changes |
| Reviewer | Developer who examines the changes |
| Approver | Person who approves the PR |
| Merge | Combining changes from two branches |

## 3. Pull Request Workflow

1. Create a feature branch.
2. Make the required changes.
3. Stage and commit changes.
4. Push the branch to GitHub.
5. Create a Pull Request.
6. Request a code review.
7. Address reviewer feedback.
8. Get approval.
9. Merge the Pull Request.
10. Delete the completed feature branch.

**Workflow:**

Feature Branch → Commit → Push → Pull Request → Code Review → Approval → Merge → Main

## 4. Branch Naming Conventions

Professional development teams use naming conventions to identify the purpose of each branch.

| Prefix | Purpose | Example |
|---|---|---|
| feature/ | New functionality | feature/product-listing |
| bugfix/ | Bug fixes | bugfix/invoice-calculation |
| hotfix/ | Urgent production fixes | hotfix/payment-error |
| docs/ | Documentation | docs/project-guide |
| refactor/ | Code restructuring | refactor/billing-service |
| test/ | Testing-related changes | test/product-validation |

## 5. Practical Implementation – bike_accessories_project

### Step 1: Check Git Status

```bash
git status
```

Shows modified, untracked and staged files, along with the current branch.

```bash
git branch
```

Displays local branches. The `*` identifies the current branch.

```bash
git remote -v
```

Displays configured remote repository URLs.

### Step 2: Switch to Main

```bash
git switch main
```

Switches the working directory to the main branch.

```bash
git pull origin main
```

Fetches and integrates the latest changes from the remote main branch.

### Step 3: Create a Feature Branch

```bash
git switch -c docs/day-9-pull-request
```

Creates a new branch and switches to it.

Verify:

```bash
git branch
```

Expected:

```text
* docs/day-9-pull-request
  main
```

### Step 4: Create Documentation

Create a new file:

`docs/day-9-pull-request.md`

Add documentation explaining the Pull Request workflow and code review process.

### Step 5: Stage Changes

```bash
git status
```

Checks the modified files.

```bash
git add docs/day-9-pull-request.md
```

Stages only the selected file.

### Step 6: Commit Changes

```bash
git commit -m "docs: add pull request workflow guide"
```

Creates a commit containing the staged changes.

**Commit Message Convention:**

```text
feat: add product listing page
fix: correct invoice calculation
docs: update project requirements
test: add product validation tests
refactor: improve billing service
```

### Step 7: Push the Feature Branch

```bash
git push -u origin docs/day-9-pull-request
```

Pushes the local branch to GitHub and establishes upstream tracking.

For subsequent pushes:

```bash
git push
```

### Step 8: Create a Pull Request on GitHub

1. Open the bike_accessories_project GitHub repository.
2. Navigate to Pull Requests.
3. Click New Pull Request.
4. Select the branches:

**Base branch:** main  
**Compare branch:** docs/day-9-pull-request

5. Enter a PR title.
6. Write a description of the changes.
7. Click Create Pull Request.

## 6. Code Review

Code Review is the process of examining another developer's code before merging it into the target branch.

**Purpose:**

- Identify bugs and logical errors.
- Improve code quality.
- Maintain coding standards.
- Improve readability and maintainability.
- Ensure changes satisfy requirements.

### GitHub Review Outcomes

| Status | Meaning |
|---|---|
| Comment | General feedback |
| Approve | Reviewer accepts the changes |
| Request Changes | Developer must modify the changes |

## 7. Handling Review Feedback

Suppose a reviewer asks us to add a section explaining how to handle review feedback.

We should update the same feature branch instead of creating another Pull Request.

### Step 1: Switch to the Existing Branch

```bash
git switch docs/day-9-pull-request
```

### Step 2: Modify the File

Update `docs/day-9-pull-request.md` with the requested changes.

### Step 3: Stage and Commit

```bash
git add docs/day-9-pull-request.md
```

```bash
git commit -m "docs: address pull request review feedback"
```

### Step 4: Push Changes

```bash
git push
```

GitHub automatically updates the existing Pull Request with the new commit.

## 8. Merge Strategies

Git supports different strategies for integrating branch changes.

| Strategy | Explanation |
|---|---|
| Merge Commit | Combines branches and preserves branch history |
| Squash and Merge | Combines multiple PR commits into one commit |
| Rebase and Merge | Replays commits onto the target branch |

For our initial exercise, use GitHub's default merge option.

## 9. Merge the Pull Request

After the reviewer approves the changes:

1. Open the Pull Request.
2. Click Merge Pull Request.
3. Confirm the merge.
4. Delete the completed remote branch if appropriate.

Update your local main branch:

```bash
git switch main
```

```bash
git pull origin main
```

The merged documentation should now be available in main.

## 10. Important GitHub Collaboration Concepts

| Concept | Explanation |
|---|---|
| Code Review | Examination of code changes |
| Peer Review | Review by another team member |
| Merge Conflict | Git cannot automatically combine conflicting changes |
| Protected Branch | Branch with restrictions on direct updates or merging |
| Branch Protection Rules | Rules controlling branch modifications |
| CI/CD | Continuous Integration and Continuous Delivery/Deployment |
| Required Checks | Automated checks that must pass before merging |
| CODEOWNERS | Defines people responsible for reviewing specific files |

## 11. Complete Command Reference

### Repository Inspection

```bash
git status
git branch
git branch -vv
git remote -v
git log --oneline
```

### Branch Management

```bash
git switch main
git switch -c docs/day-9-pull-request
git switch docs/day-9-pull-request
git branch
```

### Synchronization

```bash
git pull origin main
git push -u origin docs/day-9-pull-request
git push
```

### Staging and Committing

```bash
git add docs/day-9-pull-request.md
git status
git commit -m "docs: add pull request workflow guide"
```

### After PR Merge

```bash
git switch main
git pull origin main
```

### Optional Local Branch Cleanup

```bash
git branch -d docs/day-9-pull-request
```

Deletes the local feature branch after it has been merged.

---

## 12. Day 9 Practical Checklist

- [ ] Checked Git status and current branch.
- [ ] Verified remote repository URL.
- [ ] Created a feature branch.
- [ ] Created Pull Request documentation.
- [ ] Staged and committed changes.
- [ ] Pushed the feature branch to GitHub.
- [ ] Created a Pull Request.
- [ ] Reviewed the Pull Request.
- [ ] Addressed review feedback.
- [ ] Merged the Pull Request.
- [ ] Updated local main branch.

## 13. Key Takeaways

1. Never assume that all developers should directly modify the main branch.
2. Use feature branches for isolated development.
3. Pull Requests provide a structured way to review and merge changes.
4. Code reviews improve software quality and maintainability.
5. Review feedback should be addressed through additional commits to the same PR branch.
6. Keep the main branch stable and updated.

**Learning Outcome:** Understand and implement a professional GitHub Pull Request workflow, including branch creation, code reviews, feedback handling, and merging.
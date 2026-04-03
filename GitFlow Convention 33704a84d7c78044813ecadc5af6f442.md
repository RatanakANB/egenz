# GitFlow Convention

# Overview

In modern software development, managing multiple updates, bug fixes, and new features simultaneously can be challenging. Our team follows the **GitFlow** strategy to maintain a well-structured, organized, and efficient workflow. GitFlow defines how branches are created, maintained, and merged, ensuring the main codebase remains stable.

Key Benefits:

- **Parallel Development**: Team members work on different parts simultaneously without interference.
- **Predictable Releases**: Dedicated branches for testing and quality control.
- **Improved Teamwork**: Clear version control and organized code management.

# **GIT & GITFLOW Convention**

**What is Git?**

Git captures snapshots of your project. Every commit is a picture of your files at that moment. Efficient storage ensures only changed files take up extra space, and history is stored locally for quick access.

# **Getting Started**

- Initialize the Repository:

```bash
git init
```

```bash
git flow init -d
```

- Configure Identity:

```bash
git config user.name "{name}"
```

```bash
git config user.email "{email}"
```

# **Branching Strategy**

![Graph.drawio2.png](GitFlow%20Convention/Graph.drawio2.png)

# **Development Workflow**

## **1. Feature scenario:**

#### **1.1 Start a feature:**

```bash
git switch develop
```

```bash
git pull origin develop
```

```bash
git flow feature start {issue id}/{name}
```

**Purpose:** Start a new local feature branch.

#### **1.2 Publish a feature:**

```bash
git flow feature publish {issue id}/{name}
```

```bash
git add {modify files}
```

```bash
git commit -m "feat/{issue id}: commit message"
```

```bash
git push origin feature/{issue id}/{name}
```

**Purpose:** Developers must publish the feature branch to the remote and push commits regularly (after starting the feature and after each meaningful change).

#### **1.3 Track a feature:**

```bash
git flow feature track {issue id}/{name}
```

```bash
git add {modify files}
```

```bash
git commit -m "feat/{issue id}: {commit message}"
```

```bash
git push origin feature/{issue id}/{name}
```

**Purpose:** The issue owner/tech lead tracks the feature from the remote to contribute or test, and pushes updates after making contributions.

#### **1.4 Finish the Feature**

```bash
git switch develop
```

```bash
git pull
```

```bash
git switch feature/{issue id}/{name}
```

```bash
git pull origin develop
```

**Purpose:** Switch to `develop` and pull the latest changes, then switch back to the feature branch and pull from `develop` to stay up to date, test, and resolve conflicts if needed. Then follow the standard add/commit/push workflow.

```bash
git add .
```

```bash
git commit -m "feat/{issue id}: {commit message}"
```

```bash
git push origin feature/{issue id}/{name}
```

- *Pull Request:*

When multiple team members collaborate, merging without feedback can be risky. GitHub's Pull Request tool allows team members to review changes before they are merged into the base branch.

- *Approve the Pull Request:*

The team leader or assigned reviewers review the Pull Request and provide feedback or approval.

```bash
git flow feature finish {issue id}/{name}
```

```bash
git push origin develop
```

## **2. Bugfix scenario:**

#### **2.1 Start a bugfix:**

```bash
git switch develop
```

```bash
git pull origin develop
```

```bash
git flow bugfix start {issue id}/{name}
```

**Purpose:** Start a new local bugfix branch.

#### **2.2 Publish a bugfix:**

```bash
git flow bugfix publish {issue id}/{name}
```

```bash
git add {modify files}
```

```bash
git commit -m "bugfix/{issue id}: commit message"
```

```bash
git push origin bugfix/{issue id}/{name}
```

**Purpose:** Developers must publish the bugfix branch to the remote and push commits regularly (after starting the bugfix and after each meaningful change).

#### **2.3 Track a Bugfix:**

```bash
git flow bugfix track {issue id}/{name}
```

```bash
git add {modify files}
```

```bash
git commit -m "bugfix/{issue id}: {commit message}"
```

```bash
git push origin bugfix/{issue id}/{name}
```

**Purpose:** The issue owner/tech lead tracks the bugfix from the remote to contribute or test the fix, and pushes updates after making contributions.

#### **2.4 Finish the Bugfix**

```bash
git switch develop
```

```bash
git pull

```

```bash
git switch bugfix/{issue id}/{name}
```

```bash
git pull origin develop
```

**Purpose:** Switch to `develop` and pull the latest changes, then switch back to the bugfix branch and pull from `develop` to stay up to date, test, and resolve conflicts if needed. Then follow the standard add/commit/push workflow.

```bash
git add .
```

```bash
git commit -m "bugfix/{issue id}: {commit message}"
```

```bash
git push origin bugfix/{issue id}/{name}
```

- *Pull Request:*

When multiple team members collaborate, merging without feedback can be risky. GitHub's Pull Request tool allows team members to review changes before they are merged into the base branch.

- *Approve the Pull Request:*

The team leader or assigned reviewers review the Pull Request and provide feedback or approval.

```bash
git flow bugfix finish {issue id}/{name}
```

```bash
git push origin develop
```

## **3. Release scenario:**

#### **3.1 Start a release:**

```bash
git switch develop
```

```bash
git pull
```

```bash
git flow release start 1.0
```

**Purpose:** Start a new local release branch.

#### **3.2 Publish a release:**

```bash
git flow release publish 1.0
```

```bash
git add {modify files}
```

```bash
git commit -m "release: {commit message}"
```

```bash
git push origin release/1.0
```

**Purpose:** Developers must publish the release branch to the remote and push commits as needed.

#### **3.3 Finish the release**

```bash
git pull origin main
```

**Purpose:** Ensure your local branches are up to date, resolve any conflicts, and run the standard add/commit/push workflow before opening a Pull Request.

```bash
git add .
```

```bash
git commit -m "release: {commit message}"
```

```bash
git push origin release/1.0
```

- *Pull Request:*

When multiple team members collaborate, merging without feedback can be risky. GitHub's Pull Request tool allows team members to review changes before they are merged into the base branch.

- *Approve the Pull Request:*

The team leader or assigned reviewers review the Pull Request and provide feedback or approval.

```bash
git flow release finish 1.0
```

```bash
git push origin main
```

```bash
git push origin develop
```

```bash
git push --tags
```

# **Main Workflow**

## **4. Hotfix scenario:**

#### **4.1 Start a hotfix:**

```bash
git switch develop
```

```bash
git pull
```

```bash
git switch main
```

```bash
git pull
```

```bash
git flow hotfix start 1.1
```

**Purpose:** Start a new local hotfix branch.

#### **4.2 Publish a hotfix:**

```bash
git flow hotfix publish 1.1
```

```bash
git add {modify files}
```

```bash
git commit -m "hotfix: {commit message}"
```

```bash
git push origin hotfix/1.1
```

**Purpose:** Developers must publish the hotfix branch to the remote and push commits regularly (after starting the hotfix and after each meaningful change).

#### **4.3 Track a hotfix:**

```bash
git flow hotfix track {issue id}/{name}
```

```bash
git add {modify files}
```

```bash
git commit -m "hotfix/{issue id}: {commit message}"
```

```bash
git push origin hotfix/{issue id}/{name}
```

**Purpose:** The issue owner/tech lead tracks the hotfix from the remote to contribute or test the fix, and pushes updates after making contributions.

#### **4.4 Finish the hotfix:**

```bash
git switch develop
```

```bash
git pull
```

```bash
git switch main
```

```bash
git pull
```

```bash
git switch hotfix/1.1/{name}
```

```bash
git pull origin main
```

**Purpose:** Ensure your local branches are up to date, resolve any conflicts, and run the standard add/commit/push workflow before opening a Pull Request.

```bash
git add .
```

```bash
git commit -m "hotfix: {commit message}"
```

```bash
git push origin hotfix/1.1
```

- *Pull Request:*

When multiple team members collaborate, merging without feedback can be risky. GitHub's Pull Request tool allows team members to review changes before they are merged into the base branch.

- *Approve the Pull Request:*

The team leader or assigned reviewers review the Pull Request and provide feedback or approval.

```bash
git flow hotfix finish 1.1
```

```bash
git push origin main
```

```bash
git push origin develop
```

```bash
git push --tags
```

# **Conclusion**

The GitFlow strategy provides a clear framework for managing software development. By using distinct branches for features, releases, bug fixes, and hotfixes, we maintain parallel efficiency and codebase stability.
# scenario03 — Python Git-Flow Calculator

A hands-on Git-Flow training project built with a Python CLI calculator.  
This project follows the **Git-Flow branching strategy** and is used to practice collaborative development workflows for a 6-person team working in pairs.

---

## 👥 Team Pairs & Collaboration

| Issue | Type | Name | Assignees |
| :--- | :--- | :--- | :--- |
| **#01** | feature | Basic Arithmetic | **M1 & M2** |
| **#02** | feature | Core Operations | **M2 & M3** |
| **#03** | feature | Advanced Math | **M3 & M4** |
| **#04** | bugfix | Error Handling | **M4 & M5** |
| **#05** | hotfix | UI Menu Fix | **M5 & M6** |
| **#06** | release | Release v1.0.0 | **M6 & M1** |

> **Note:** Every member is assigned to two issues, collaborating with two different partners to maximize Git-Flow synchronization practice.

---

## 📋 Project Scope

Detailed task descriptions can be found in [issues.md](file:///Users/anbschool0018/Desktop/Project/031.git/scenario03/issues.md).

---

## 🌿 Branch Naming Convention

Every branch name **must include the assigned issue ID** as a prefix, followed by a descriptive slug.

### Examples

| Issue ID | Type | Name | Branch Name | Command |
|----------|------|------|-------------|---------|
| `#01` | feature | add-subtract | `feature/01/add-subtract` | `git flow feature start 01/add-subtract` |
| `#04` | bugfix | error-handling | `bugfix/01/error-handling` | `git flow bugfix start 01/error-handling` |
| `#05` | hotfix | menu-fix | `hotfix/01/menu-fix` | `git flow hotfix start 01/menu-fix` |

---

## 🔄 Git-Flow Lifecycle

Follow this order when working through the project:

```
1. Features     ──► develop
2. Bugfix       ──► develop
3. Release      ──► main + develop  (tag version)
4. Hotfix       ──► main + develop  (production fix)
```

### Collaboration Workflow

1.  **Start & Publish**: One member starts the branch and publishes it.
2.  **Track**: The partner uses `track` to sync the branch.
3.  **Collaborate**: Both members push and pull changes to the shared branch.
4.  **Finish**: The team lead or assigned reviewer approves the merge.

```bash
# 1. Partner A: Start and publish
git flow feature start <issue-id>/<name>
git flow feature publish <issue-id>/<name>

# 2. Partner B: Track the branch
git flow feature track <issue-id>/<name>

# 3. Both: Pull/Push regularly
git pull
git push

# 4. Finish and merge back
git flow feature finish <issue-id>/<name>
```

---

## 📁 Project Structure

```
scenario03/
├── main.py          # CLI entry point
├── calculator.py    # Core operations
├── logger.py        # Action logger
├── issues.md        # Detailed task descriptions [NEW]
├── track.md         # Git-Flow track command reference
└── README.md        # This file
```


---

## ⚙️ Requirements

- Python `>= 3.14`
- Dependencies: `mermaid-py >= 0.8.4`, `ipykernel`
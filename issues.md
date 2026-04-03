# GitHub Issues Simulation (scenario03)

This file contains the titles and descriptions for the issues assigned to the 6-member team. Each issue is assigned to **2 members** to facilitate Git-Flow collaboration using `publish` and `track`.

---

## Issue #01: Implement Basic Arithmetic (Add & Subtract)
**Type:** Feature  
**Assignees:** Member 1 (Leader) & Member 2  
**Branch:** `feature/01/add-subtract`  
**Description:**  
Implement the `add(a, b)` and `subtract(a, b)` functions in `calculator.py`. Ensure that each operation is correctly logged using `log_action()`. Update `main.py` to uncomment and enable these options in the CLI menu.

---

## Issue #02: Implement Core Operations (Multiply & Divide)
**Type:** Feature  
**Assignees:** Member 2 & Member 3  
**Branch:** `feature/02/multiply-divide`  
**Description:**  
Implement the `multiply(a, b)` and `divide(a, b)` functions in `calculator.py`. Handle the division-by-zero case by raising a `ValueError`. Ensure logging is active for both. Update `main.py` to enable options 3 and 4 in the menu.

---

## Issue #03: Implement Advanced Math (Power & Square Root)
**Type:** Feature  
**Assignees:** Member 3 & Member 4  
**Branch:** `feature/03/advanced-math`  
**Description:**  
Implement the `power(a, b)` and `sqrt(a)` functions in `calculator.py` using the `math` module. Square root should raise a `ValueError` for negative inputs. Update `main.py` to uncomment options 5 and 6 in the menu.

---

## Issue #04: System-wide Error Handling & Input Validation
**Type:** Bugfix  
**Assignees:** Member 4 & Member 5  
**Branch:** `bugfix/01/error-handling`  
**Description:**  
Improve the robustness of the calculator. Ensure that non-numeric inputs in `_ab()` are handled gracefully. Improve the error reporting in the `main()` loop's `except` block to provide clearer feedback to the user.

---

## Issue #05: UI: Fix Menu Display & Formatting
**Type:** Hotfix  
**Assignees:** Member 5 & Member 6  
**Branch:** `hotfix/01/menu-fix`  
**Description:**  
Fix a reported issue where the menu presentation is inconsistent. Ensure the header and options are properly aligned. This fix must be branched from `main` and merged back into both `main` and `develop`.

---

## Issue #06: Release Management v1.0.0
**Type:** Release  
**Assignees:** Member 6 & Member 1 (Leader)  
**Branch:** `release/1.0.0`  
**Description:**  
Coordinate the final wrap-up of the project. Ensure all features and bugfixes are merged into `develop`. Prepare the release branch, update version metadata if applicable, and merge into `main` with the `v1.0.0` tag.

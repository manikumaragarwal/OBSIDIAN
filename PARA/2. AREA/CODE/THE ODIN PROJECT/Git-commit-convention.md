
Tags: [[CODING]] [[THE ODIN PROJECT]]


---

### **Git Commit Convention: A Short Summary**

A good Git commit message follows a consistent format to improve readability and maintainability. A popular convention is the **Conventional Commits** standard, which structures commits like this:

#### **Format:**

```
<type>(<scope>): <subject>
<BLANK LINE>
<body>
<BLANK LINE>
<footer>
```

#### **Parts of a Commit:**

1. **Type** (Required):

   - `feat`: A new feature
   - `fix`: A bug fix
   - `docs`: Documentation changes
   - `style`: Code formatting (no functional changes)
   - `refactor`: Code changes that don’t fix bugs or add features
   - `test`: Adding or modifying tests
   - `chore`: Maintenance tasks (e.g., dependency updates)

2. **Scope** (Optional):

   - The part of the codebase affected (e.g., `auth`, `navbar`, `api`)

3. **Subject** (Required):

   - A short, imperative description (e.g., "Fix login bug" instead of "Fixed login bug")

4. **Body** (Optional):

   - Detailed explanation of changes (if needed)

5. **Footer** (Optional):
   - References like `Closes #123` (for issue tracking)

---

### **Examples:**

#### **1. Simple Commit (Type + Subject)**

```
feat: add user authentication
```

#### **2. With Scope**

```
fix(login): handle empty password submission
```

#### **3. With Body & Footer**

```
refactor(database): migrate to PostgreSQL

- Replace SQLite with PostgreSQL for better scalability
- Update connection settings in config

Closes #45
```





---
[[THE ODIN PROJECT]]
[[CODING]]
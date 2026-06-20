```markdown
# claude-code Development Patterns

> Auto-generated skill from repository analysis

## Overview
This skill documents the core development patterns and workflows used in the `claude-code` repository. It covers coding conventions, commit practices, and step-by-step guides for common maintenance and release workflows. Whether you're contributing code, updating documentation, or managing releases, this guide will help you follow the established standards of the project.

## Coding Conventions

### File Naming
- **Style:** camelCase
- **Example:**  
  ```plaintext
  myModule.py
  processData.py
  ```

### Imports
- **Style:** Relative imports are used within the codebase.
- **Example:**
  ```python
  from .utils import helperFunction
  ```

### Exports
- **Style:** Named exports (explicitly listing exported functions/classes).
- **Example:**
  ```python
  __all__ = ['myFunction', 'MyClass']
  ```

### Commit Messages
- **Style:** Conventional commits, primarily using the `chore` prefix.
- **Example:**
  ```
  chore: update dependencies for security
  ```

## Workflows

### Update Changelog and Feed
**Trigger:** When you need to record recent changes and update the project's feed (typically after a release or notable update).  
**Command:** `/update-changelog-feed`

1. Edit `CHANGELOG.md` to add new entries describing the latest changes.
2. Update `feed.xml` to reflect the latest changes for RSS/Atom feeds.
3. Commit both files together with a descriptive message.

**Example Commit:**
```
chore: update changelog and feed for v1.2.3
```

---

### Update Plugin or Skill
**Trigger:** When releasing a new version or making improvements to a plugin or skill.  
**Command:** `/update-plugin`

1. Edit the relevant `plugin.json` file to update metadata or version.
2. Update documentation files such as `README.md` or `SKILL.md` within the plugin or skill directory.
3. Modify implementation files as needed (e.g., hooks, scripts).
4. Commit all related files together.

**Files Involved:**
- `plugins/*/.claude-plugin/plugin.json`
- `plugins/*/README.md`
- `plugins/*/skills/*/SKILL.md`
- `plugins/*/hooks/*.py`
- `plugins/*/hooks/*.sh`
- `plugins/*/hooks/*.json`

**Example Commit:**
```
chore: update plugin metadata and documentation
```

---

### Update GitHub Workflow
**Trigger:** When you need to fix, improve, or update automation in GitHub Actions workflows.  
**Command:** `/update-workflow`

1. Edit one or more `.github/workflows/*.yml` files to modify CI/CD or automation behavior.
2. Commit the changes, referencing the workflow name in the commit message.

**Example Commit:**
```
chore: update CI workflow for Python 3.11 support
```

## Testing Patterns

- **Framework:** Unknown (no specific testing framework detected).
- **File Pattern:** Test files follow the `*.test.*` naming convention.
- **Example:**
  ```
  utils.test.py
  processData.test.py
  ```

## Commands

| Command                 | Purpose                                                         |
|-------------------------|-----------------------------------------------------------------|
| /update-changelog-feed  | Update `CHANGELOG.md` and `feed.xml` after notable changes      |
| /update-plugin          | Update plugin/skill metadata, docs, and implementation files    |
| /update-workflow        | Modify GitHub Actions workflow YAML files                       |
```

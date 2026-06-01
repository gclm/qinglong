```markdown
# qinglong Development Patterns

> Auto-generated skill from repository analysis

## Overview
This skill provides a comprehensive guide to the development patterns, coding conventions, and common workflows used in the `qinglong` repository. The project is a TypeScript codebase built with React, focusing on task scheduling, configuration management, and frontend/backend integration. This guide will help contributors quickly understand and follow the established practices for efficient collaboration.

## Coding Conventions

### File Naming
- **Pattern:** camelCase
- **Example:**  
  - `systemLog.tsx`
  - `cronView.ts`

### Import Style
- **Pattern:** Relative imports
- **Example:**
  ```typescript
  import config from '../config/index';
  import CronService from './cron';
  ```

### Export Style
- **Pattern:** Default exports
- **Example:**
  ```typescript
  // src/services/cron.ts
  export default CronService;
  ```

### Commit Messages
- **Pattern:** Freeform, no strict prefix
- **Length:** Average ~18 characters
- **Example:**  
  - `fix cron schedule bug`
  - `update env logic`

## Workflows

### Update Version
**Trigger:** When releasing a new version.  
**Command:** `/bump-version`

1. Open `version.yaml`.
2. Update the version number to the new release.
3. Commit and push the change.

**Example:**
```yaml
version: 2.9.3
```

---

### Update README Documentation
**Trigger:** When documentation needs to be updated or improved.  
**Command:** `/update-readme`

1. Edit `README.md` and/or `README-en.md` to reflect new features or changes.
2. Commit and push the updated documentation.

---

### Update Shell Task Environment
**Trigger:** When changing how tasks are executed or how environment variables are loaded for scripts.  
**Command:** `/update-task-env`

1. Edit relevant shell scripts:
    - `shell/otask.sh`
    - `shell/share.sh`
    - `shell/preload/sitecustomize.js`
    - `shell/preload/sitecustomize.py`
2. Update environment logic in:
    - `back/services/env.ts`
    - `back/config/index.ts`
3. If necessary, update `Dockerfile` or related files if changes affect containers.

---

### Fix or Enhance Cron/Schedule
**Trigger:** When there are issues or improvements needed for cron/schedule/subscription logic.  
**Command:** `/fix-cron`

1. Edit backend service files:
    - `back/services/cron.ts`
    - `back/services/schedule.ts`
    - `back/services/subscription.ts`
2. Optionally update related files:
    - `back/services/cronView.ts`
    - `back/services/system.ts`
    - `back/api/env.ts`

---

### Update Docker and Package Dependencies
**Trigger:** When dependencies need to be upgraded or Docker images/scripts are changed.  
**Command:** `/update-docker-deps`

1. Edit Dockerfiles:
    - `docker/Dockerfile`
    - `docker/310.Dockerfile`
2. Update package dependencies:
    - `package.json`
    - `pnpm-lock.yaml`
3. Commit and push the changes.

---

### Update Sample Config or Notification Scripts
**Trigger:** When sample scripts or config templates need to be changed.  
**Command:** `/update-sample`

1. Edit sample files:
    - `sample/config.sample.sh`
    - `sample/notify.js`
    - `sample/notify.py`
2. Commit and push the updates.

---

### Fix Frontend Pages or Styles
**Trigger:** When there are UI/UX bugs or improvements in frontend pages.  
**Command:** `/fix-frontend`

1. Edit relevant frontend files:
    - `src/pages/setting/index.tsx`
    - `src/pages/setting/loginLog.tsx`
    - `src/pages/setting/systemLog.tsx`
    - `src/pages/dependence/index.tsx`
    - `src/pages/crontab/index.tsx`
2. Test UI changes and commit.

---

## Testing Patterns

- **Framework:** Unknown (not explicitly detected)
- **File Pattern:** `*.test.*`
- **Example:**
  - `cron.test.ts`
  - `env.test.ts`
- **Note:** Place test files alongside the modules they test, using the `.test.ts` or `.test.tsx` suffix.

## Commands

| Command             | Purpose                                                        |
|---------------------|----------------------------------------------------------------|
| /bump-version       | Bump the project version number to a new release               |
| /update-readme      | Update project documentation in the README files               |
| /update-task-env    | Modify shell scripts and environment variable handling         |
| /fix-cron           | Fix or enhance scheduled tasks (cron jobs)                     |
| /update-docker-deps | Update Dockerfiles and/or package dependencies                 |
| /update-sample      | Update sample configuration files or notification script samples|
| /fix-frontend       | Fix bugs or update styles in frontend pages                    |
```

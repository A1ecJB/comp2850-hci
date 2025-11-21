# Fix 01: Image alt next missing (WCAG 2.1 AA)

**Backlog ID**: 1
**WCAG Criterion**: 2.1 Perceivable (Minimum, Level AA)
**Priority**: Maximum severity

---

## Problem Statement
Delete button text color (#6c757d) on white background (#ffffff) = 4.2:1 contrast ratio.
**Fails**: WCAG AA requires alt text for all images.

**Evidence**:
- axe DevTools: (Critical)
- Screenshot: `wk07/evidence/alt-before.png`

---

## Target State
Alt text appears when image fails to load.

---

## Solution
Provide suitable alt text for task icon image

**Option A**: alt="Appropriate message"

**Chosen**: Use alt text as "Task Icon".

---

## Implementation

### Before (Current html)
index.peb
```html
<img src="/static/img/icon.png" width="16" height="16">
```
### After (New html)
index.peb
```html
<img src="/static/img/icon.png" alt="Task Icon" width="16" height="16">
```

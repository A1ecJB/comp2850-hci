# Fix 02: Poor Contrast (WCAG 2.0 AA)

**Backlog ID**: 2
**WCAG Criterion**: 2.0 Perceivable (Minimum, Level AA)
**Priority**: High severity

---

## Problem Statement
Foreground and background elements lack sufficient contrast.
**Fails**: WCAG AA requires minimum contrast of 4.5:1 for normal text.

**Evidence**:
- axe DevTools: (Severe)
- Screenshot: `wk07/evidence/contrast-before.png`

---

## Target State
Popup region on action has poor contrast with local background and normal text.

---

## Solution
Alterations to colours used

**Option A**: Make text darker to meet ratio
**Option B**: Make local background darker to meet ratio

**Chosen**: Option B, swap local background (#e3f2fd) with new colour (#32325d)

---

## Implementation

### Before (Current css)
base.peb
```html
background: #e3f2fd;
```
### After (New css)
base.peb
```css
background: #32325d;
```

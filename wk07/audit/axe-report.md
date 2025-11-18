# axe DevTools Audit Report — Week 7

**Date**: [2025-11-17]
**URL**: http://127.0.0.1:8080/tasks
**Tool**: axe DevTools 4.x
**Scope**: Full page scan (add form + task list)

---

## Summary
- **Critical**: 1
- **Serious**: 1
- **Moderate**: 0
- **Minor**: 0
- **Total**: 2 issues

---

## Critical Issues

### Issue 1: Image alt text missing (Critical)
**Element**: `Images must have alternative text`
**Rule**: `Perceivable` (WCAG 2.1 AA)
**Description**: Form element does not have an associated label.
**Impact**: Those who cannot load images will be unable to tell what the image was representing.
**Fix**: Ensure `<img>` elements have alternative text or a role of none or presentation
**Status**: **CONFIRMED** - Add to backlog as maximum severity


## Severe Issues
### Issue 2: Poor contrast (Severe)
**Element**: `Elements must meet minimum colour contrast ratios`
**Rule**: `Perceivable` (WCAG 2.0 AA)
**Description**: Contrast between foreground and background elements do not meet standads.
**Impact**: Those visually impared will struggle to differentiate different elements.
**Fix**: Ensure `id=status` elements have sufficient background contrast
**Status**: **CONFIRMED** Add to backlog as high seereity

## Moderate Issues
None detected.

## Minor Issues
None detected.
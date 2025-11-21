# WCAG 2.2 AA Checklist — Week 7

**Date**: [YYYY-MM-DD]
**Scope**: Task manager (add, edit, delete flows)
**Tester**: [Your Name]

---

## Perceivable (Principle 1)

### 1.1 Text Alternatives
| Criterion              | Level | Status | Evidence                                                                  | Notes                    |
|------------------------|-------|--------|---------------------------------------------------------------------------|--------------------------|
| 1.1.1 Non-text Content | A     | ✅ Pass | `<img src="/static/img/icon.png" alt="Task Icon" width="16" height="16">` | Main image does not load |

### 1.3 Adaptable
| Criterion                    | Level | Status | Evidence                                    | Notes                                         |
|------------------------------|-------|--------|---------------------------------------------|-----------------------------------------------|
| 1.3.1 Info and Relationships | A     | ✅ Pass | `<label for="title">` links to input        | Semantic HTML (`<main>`, `<section>`, `<ul>`) |
| 1.3.2 Meaningful Sequence    | A     | ✅ Pass | Tab order: skip link → add form → task list | Logical reading order                         |

### 1.4 Distinguishable
| Criterion                | Level | Status | Evidence                                                                               | Notes                     |
|--------------------------|-------|--------|----------------------------------------------------------------------------------------|---------------------------|
| 1.4.3 Contrast (Minimum) | AA    | ✅ Pass | Minimum ratio between any text and background element is 4.76 (Background and <p> text | Could be improved for AAA |
| 1.4.11 Non-text Contrast | AA    | ❌ Fail | Background (#13171F) and Input Textbox (#1C212C) in ratio 4.11:1                       | Needs 3.1:1 (AA)          |

---

## Operable (Principle 2)

### 2.1 Keyboard Accessible
| Criterion              | Level | Status | Evidence                                    | Notes                                                                |
|------------------------|-------|--------|---------------------------------------------|----------------------------------------------------------------------|
| 2.1.1 Keyboard         | A     | ✅ Pass | All features accessible via Tab/Enter/Space | Can add/delete tasks. Pressing enter while in textbox will submit it |
| 2.1.2 No Keyboard Trap | A     | ✅ Pass | No traps detected                           | Can Tab out of all forms                                             |

### 2.4 Navigable
| Criterion           | Level | Status     | Evidence                                    | Notes                               |
|---------------------|-------|------------|---------------------------------------------|-------------------------------------|
| 2.4.1 Bypass Blocks | A     | ✅ Pass     | Skip link appears on Tab, jumps to #main    | Tested with keyboard                |
| 2.4.3 Focus Order   | A     | ✅ Pass     | Tab order: Skip → Create → Add → Remove     | Logical sequence                    |
| 2.4.7 Focus Visible | AA    | ⚠️ Partial | Pico.css default outline visible, but faint | Consider custom outline (3px solid) |

---

## Understandable (Principle 3)

### 3.2 Predictable
| Criterion      | Level | Status     | Evidence                            | Notes                                                  |
|----------------|-------|------------|-------------------------------------|--------------------------------------------------------|
| 3.2.1 On Focus | A     | ✅ Pass     | No context change on focus          | Only explicit button clicks trigger actions            |
| 3.2.2 On Input | A     | ⚠️ Partial | Enter key causes submission of task | Besides this and button click, no other sources submit |

### 3.3 Input Assistance
| Criterion                    | Level | Status     | Evidence                                                | Notes                            |
|------------------------------|-------|------------|---------------------------------------------------------|----------------------------------|
| 3.3.1 Error Identification   | A     | ✅ Pass     | Error: "Please fill out this field."                    | Specific, actionable             |
| 3.3.2 Labels or Instructions | A     | ⚠️ Partial | Most inputs have `<label>`, but priority input does not | `aria-describedby` links to hint |
| 3.3.3 Error Suggestion       | AA    | ✅ Pass     | Error message includes correction hint                  | "Please fill out this field"     |

---

## Robust (Principle 4)

### 4.1 Compatible
| Criterion               | Level | Status | Evidence                                 | Notes                                        |
|-------------------------|-------|--------|------------------------------------------|----------------------------------------------|
| 4.1.2 Name, Role, Value | A     | ✅ Pass | All buttons have accessible names        | `aria-label="Delete task: {{ task.title }}"` |
| 4.1.3 Status Messages   | AA    | ✅ Pass | `<div role="status" aria-live="polite">` | Tested with NVDA                             |

---

## Summary
- **Total criteria evaluated**: 17
- **Pass**: 13
- **Fail**: 1 (1.4.11 Non-text Contrast)
- **Partial**: 3 (3.3.2 Labels or Instructions, 3.2.2 On Input, 2.4.7 Focus Visible)
- **N/A**: 0

---

## High-Priority Failures
1. **1.4.11 Non-text Contrast (Minimum, AA)**: Input textbox fails with 1.11:1 ratio
    - **Action**: Change `background` property of textbox element to contrast main background without contrasting input text

2. **2.4.7 Focus Visible (AA, Partial)**: Default outline may be too faint
    - **Action**: Add custom `:focus` styles (3px solid #1976d2)

3. **3.2.2 On Input (A, Partial)**: Enter key causes submission of task
    - **Action**: Ensure only clicking the "Add Task" button will add the task, nothing else
---

**Next**: Add these findings to backlog with severity scores.

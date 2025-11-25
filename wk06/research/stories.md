# Job Stories — Week 6 Needs-Finding

## Story S1: Adding additional details
**Situation**: When I'm creating tasks I want to plan for
**Motivation**: I want to be able to write down a due date/other information
**Outcome**: So I can stay on track with completing the task
**Underlying need**: Because otherwise I may forget to complete them on time

**Evidence**: Participant A (notes L10)
**Inclusion risk**: Cognitive, memory impairment
**Type**: Job story (situation-specific)

---

## Story S2: Accident prevention
**Situation**: When I browse my task list
**Motivation**: I want a confirmation requirement before deleting a task
**Outcome**: So I can avoid the risk of losing a task due to a misclick
**Underlying need**: Because otherwise, it may lead to foresting about the task entirely until it causes further problems


**Evidence**: Participant A (notes L22)
**Inclusion risk**: Motor impairment (leading to misinput), memory impairment (if forgetting details about task)
**Type**: Job story
**WCAG** 3.3 Input Assistance (A), 3.3.1 Error Identification (Does not query "Are you sure you want to delete?" or similar)

---

## Story S3: Keyboard Navigation Efficiency
**Situation**: When I only have access to keyboard input
**Motivation**: I want to access all features as if I had a mouse as well
**Outcome**: So I can manage tasks quickly and without struggle
**Underlying need**: Because otherwise, using only a keyboard can make actions to complete take much longer or impossible

**Evidence**: Participant A (notes L46)
**Inclusion risk**: Injury/impairment, broken/no available mouse, personal preference
**Type**: Job story
**WCAG**: 2.1.1 Keyboard (A), 2.1.3 Keyboard (No Exception, AAA)

---

## Story S4: High Contrast
**Situation**: When I'm working in bright sunlight or have low vision
**Motivation**: I want text to have sufficient contrast against background
**Outcome**: So I can read task titles and buttons without straining
**Underlying need**: Because low contrast creates situational disability (sunlight) or permanent exclusion (low vision)

**Evidence**: Participant A (notes L28)
**Inclusion risk**: Low vision, colour-blindness, situational (bright light)
**Type**: Job story
**WCAG**: 1.4.3 Contrast (Minimum, AA) — 4.5:1 for normal text

---

## Story S5: Progress Visualisation
**Situation**: When I'm managing tasks belonging to different projects
**Motivation**: I want to see some sot of visual representation how many tasks were completed per category
**Outcome**: So I can filter out tasks irrelevant to what I'm looking for and track a project meeting milestones
**Underlying need**: Because pure text and be more difficult to gather information about than graphics

**Evidence**: Participant A (notes L70)
**Inclusion risk**: Cognitive, ADHD (executive function support)
**Type**: Job story

---

## Story S6: No reliance on JavaScript
**Situation**: When JavaScript is disabled or unavailable
**Motivation**: I want all features to continue working, such as alerting me of invalid input
**Outcome**: So I can still use the webapp with safeguards in place despite the lack of JS verifying it
**Underlying need**: Because otherwise I could make mistakes that I do not identify in time

**Evidence**: Inferred from testing no-JS in earlier labs
**Inclusion risk**: Use of legacy hardware (cannot run JS), screen readers/browsers that do not support JS
**Type**: Pain point (internally identified)
**WCAG**: 3.3.1 Error Identification (A), 3.3.3 Error Suggestion (AA)

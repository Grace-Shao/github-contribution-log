# Contribution 1: Sentry: Sentry issues stats for "All" crash frontend.

**Contribution Number:** 1

**Student:** Grace Shao

**Issue:** [GitHub issue link](https://github.com/backstage/community-plugins/issues/8372)  

**Status:** [Phase I ] [In Progress / Complete]

---

## Why I Chose This Issue

[1-2 paragraphs explaining why this issue interests you, how it matches your skills/learning goals, what you hope to learn]
I chose issue 3725 Sentry: Sentry issues stats for "All" crash frontend because I was able to reproduce part of the problem locally. The issue is labeled as "help wanted" and "bug" and not published too long ago (this year march 31) and doesn't have a large stream of comments in discussion page so this seemed like a good beginner issue to work on.
The project tech stack I also have experience in (Typescript)

Left a comment on the issue introducing myself — still waiting on maintainer to confirm whether this issue still needs help.

---

## Understanding the Issue

### Problem Description
In the sentry mock app, when you choose from All time range, the label "states for 24 hr" should update and there should be a bug that says "invalid unit value - infinity"


### Expected Behavior

No bug [as described above] and labels update

### Current Behavior

See problem description.

### Affected Components

Community-plugins/sentry and backend folder

---

## Reproduction Process

### Environment Setup

[Notes on setting up your local development environment - challenges you faced, how you solved them]

### Steps to Reproduce

1. cd into workspace
2. yarn install
3. yarn workspace @backstage-community/plugin-sentry start
4. Local environment should spin up

### Reproduction Evidence

- **Commit showing reproduction:** [[Link to commit in your fork]](https://github.com/backstage/community-plugins/compare/main...Grace-Shao:community-plugins:reproduction?expand=1)
- **Screenshots/logs:** [If applicable]
- **My findings:** I'm still not seeing the exact bug (the infinity error). Perhaps because the backend also needs to be spun up?

---

## Solution Approach

### Analysis

[Your analysis of the root cause - what's causing the issue?]

### Proposed Solution

[High-level description of your fix approach]

### Implementation Plan

Using UMPIRE framework (adapted):

**Understand:** [Restate the problem]

**Match:** [What similar patterns/solutions exist in the codebase?]

**Plan:** [Step-by-step implementation plan]
1. [Modify file X to do Y]
2. [Add function Z]
3. [Update tests]

**Implement:** [Link to your branch/commits as you work]

**Review:** [Self-review checklist - does it follow the project's contribution guidelines?]

**Evaluate:** [How will you verify it works?]

---

## Testing Strategy

### Unit Tests

- [ ] Test case 1: [Description]
- [ ] Test case 2: [Description]
- [ ] Test case 3: [Description]

### Integration Tests

- [ ] Integration scenario 1
- [ ] Integration scenario 2

### Manual Testing

[What you tested manually and results]

---

## Implementation Notes

### Week [X] Progress

[What you built this week, challenges faced, decisions made]

### Week [Y] Progress

[Continue documenting as you work]

### Code Changes

- **Files modified:** [List]
- **Key commits:** [Links to important commits]
- **Approach decisions:** [Why you chose certain approaches]

---

## Pull Request

**PR Link:** [GitHub PR URL when submitted]

**PR Description:** [Draft or final PR description - much of the content above can be adapted]

**Maintainer Feedback:**
- [Date]: [Summary of feedback received]
- [Date]: [How you addressed it]

**Status:** [Awaiting review / Iterating / Approved / Merged]

---

## Learnings & Reflections

### Technical Skills Gained

[What you learned technically]

### Challenges Overcome

[What was hard and how you solved it]

### What I'd Do Differently Next Time

[Reflection on your process]

---

## Resources Used

- [Link to helpful documentation]
- [Tutorial or Stack Overflow post that helped]
- [GitHub issues or discussions that helped]

# Contribution 1: Sentry: Sentry issues stats for "All" crash frontend.

**Contribution Number:** 1

**Student:** Grace Shao

**Issue:** [GitHub issue link](https://github.com/backstage/community-plugins/issues/8372)  

**Status:** [Phase 3] [Complete]

---

## Why I Chose This Issue

I chose issue 3725 Sentry: Sentry issues stats for "All" crash frontend because I was able to reproduce part of the problem locally. The issue is labeled as "help wanted" and "bug" and not published too long ago (this year march 31) and doesn't have a large stream of comments in discussion page so this seemed like a good beginner issue to work on.
The project tech stack I also have experience in (Typescript)

Left a comment on the issue introducing myself — still waiting on maintainer to confirm whether this issue still needs help.

---

## Understanding the Issue

### Problem Description
In the sentry mock app, when you choose from All time range, the label "stats for 24 hr" should not update and there should be a bug that says "invalid unit value - infinity"


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
I believe that the subtitle listed in the image actually describes the Graph time period as only `statsPeriod` from production-api.ts:53-54 uses it to generate the graph, it doesn't seem to have any relation with the drop down UI filtering.

Also I believe the `When select "All" front crash (Image 2).. ` is already addressed by a previous commit on main "fix(sentry): use useMemo for issue filtering to sync with async data (#7523)"


### Proposed Solution

[High-level description of your fix approach] Rename the label in the frontend to clarify the 24hr time period is for the graph but not changing any of the underlying code.

### Implementation Plan

Using UMPIRE framework (adapted):

**Understand:** [Restate the problem] The label "stats for 24 hr" is not update

**Match:** [What similar patterns/solutions exist in the codebase?] Nothing really similar in the codepbase

**Plan:** [Step-by-step implementation plan]
1. Update the frontend SentryIssuesTable.tsx (1 commit only)
2. Add a .changeset (rules of contributing)
3. Update the SentryIssuesTable.test.tsx to account for the new label update

**Implement:** [PR here](https://github.com/backstage/community-plugins/pull/9503)

**Review:** [Self-review checklist - does it follow the project's contribution guidelines?]

**Evaluate:** [How will you verify it works?] Passes all unit test and solution shows up locally

---

## Testing Strategy

### Unit Tests

- [X] Test case 1: Modifying existing test case that checks for the UI label
(other test cases are not needed because simple UI change)

### Integration Tests

- Did not write integration tests because simple UI change

### Manual Testing

Viewed in my local environment the changes made to the front end (confirmed it successfully updated the UI). Ran the existing test suite related to the UI change

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

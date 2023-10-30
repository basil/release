---
name: "🎉 Recommend a new Java version checklist"
labels: java-lifecycle-checklist
about: Track work required to recommend a new Java version
---

# Stage 2: Recommend a new Java version

More information is available in the [Java lifecycle guide](https://github.com/jenkins-infra/release/blob/master/docs/releases.md).

## Stage Lead

<!--
  The stage lead is expected to perform or delegate the work.
-->

@<github-username of stage lead>

## Preparatory work

- [ ] Ensure all outstanding Jira issues from stage 1 have been addressed.
- [ ] Confirm adoption has been increasing steadily in JVM usage statistics.

## Primary work

<!--
  TODO: link to example PRs
  TODO: provide more details about each step
-->

- [ ] Fix any Jira issues in stage 2.
- [ ] Update the default Docker image to use the new version of Java.
- [ ] Update the Windows installer to use the new version of Java by default.

## Subsequent work

- [ ] Monitor Jira for issues in the stage 2 epic.
- [ ] Confirm a spike is visible in JVM usage statistics in the next few months.

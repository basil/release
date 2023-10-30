---
name: "🚨 Require a new Java version checklist"
labels: java-lifecycle-checklist
about: Track work required to require a new Java version
---

# Stage 3: Require a new Java version

More information is available in the [Java lifecycle guide](https://github.com/jenkins-infra/release/blob/master/docs/releases.md).

## Stage Lead

<!--
  The stage lead is expected to perform or delegate the work.
-->

@<github-username of stage lead>

## Preparatory work

- [ ] Ensure all outstanding Jira issues from stage 2 have been addressed.
- [ ] Confirm adoption has been increasing steadily in JVM usage statistics.

## Primary work

<!--
  TODO: link to example PRs
  TODO: provide more details about each step
-->

- [ ] Fix any Jira issues in stage 3.
- [ ] Update the parent POM and plugin POM to require the new version, thereby introducing a flag day.
<!--
  TODO: Or instead allow the same parent POM to continue to be used with older Java versions,
  provided the consumers customize the maven.compiler.release and maven.compiler.testRelease to the
  older Java version? This could be more flexible, but also more confusing, depending on one's
  perspective. This ought to be discussed.
-->
- [ ] Remove the Docker images of the old version.
- [ ] Update Jenkins core.
<!--
  TODO: what needs to be done to Jenkins core and core components?
  TODO: what needs to be done to the Windows installer?
  TODO: what needs to be done to docs?
  TODO: what needs to be done to PCT?
  TODO: what needs to be done to ATH?
  TODO: what else needs to be done?
-->

## Subsequent work

- [ ] Monitor Jira for issues in the stage 3 epic.
- [ ] Confirm a decrease is visible in JVM usage statistics in the next few months.

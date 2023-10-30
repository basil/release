---
name: "🚀 Add support for a new Java version checklist"
labels: java-lifecycle-checklist
about: Track work required to add support for a new Java version
---

# Stage 1: Add support for a new Java version

More information is available in the [Java lifecycle guide](https://github.com/jenkins-infra/release/blob/master/docs/releases.md).

## Stage Lead

<!--
  The stage lead is expected to perform or delegate the work.
-->

@<github-username of stage lead>

## Preparatory work

- [ ] Create three GitHub issues in this repository, one for each stage.
- [ ] Create three Jira epics, one for each stage.
- [ ] Request that the infrastructure team provide the new Java version on [ci.jenkins.io](https://ci.jenkins.io) and other controllers.

## Primary work

<!--
  TODO: link to example PRs
  TODO: provide more details about each step
-->

- [ ] Update core and core components.
  - [ ] (Core only) Update `jenkins.monitor.JavaVersionRecommendationAdminMonitor#SUPPORTED_JAVA_VERSIONS`.
  - [ ] (Core only) Update `executable.Main#SUPPORTED_JAVA_VERSIONS`.
  - [ ] Run a local build with the new version; find and fix compilation errors and test failures.
  - [ ] If any new warnings are introduced, file Jira issues in the stage 2 epic.
  - [ ] Update the `Jenkinsfile` to test on the new version.
- [ ] Update the `Jenkinsfile` for PCT.
  - [ ] Run a build with the new Java version.
  - [ ] For any failures, file Jira issues in the stage 1 epic (possibly adding a temporary workaround to keep running those plugin builds on the old Java version).
- [ ] Update the `Jenkinsfile` for ATH.
  - [ ] Run a build with the new Java version.
  - [ ] For any failures, file Jira issues in the stage 1 epic.
- [ ] Update the archetype and the `Jenkinsfile` for critical plugins.
- [ ] Add support for the new Java version in the Windows installer.
- [ ] Fix the stage 1 issues identified previously, if any.
- [ ] Write a blog post announcing the beginning of a new Java lifecycle.

<!--
  TODO: what needs to be done to docs?
-->

## Subsequent work

- [ ] Monitor Jira for issues in the stage 1 epic.
- [ ] Confirm early adopters are visible in JVM usage statistics in the next few months.

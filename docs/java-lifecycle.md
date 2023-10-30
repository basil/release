# Java lifecycle

This document describes the implementation of the Java lifecycle described in JEP-400.

## Overview

The Java lifecycle consists of three stages:

<dl>
<dt>Add support for a new Java version</dt>
<dd>The first stage enables early adopters to begin using the new Java version.</dd>
<dt>Recommend a new Java version</dt>
<dd>The second stage accelerates adoption of the new Java version.</dd>
<dt>Require a new Java version</dt>
<dd>The third stage forces users to complete the migration.</dd>
</dl>

## Procedure

### Choosing dates

During the implementation of the first stage, the date of the third stage must be decided.
The administrative monitor warns users 12 months before the date of the third stage, implying the date for the second stage as well.
In other words, the implementation of the first stage also defines the dates for the second and third stages.
The date of the third stage for a given Java LTS release is typically two years after the date of the third stage for the previous Java LTS release,
and it must be before the date the Eclipse Temurin project drops support for the given Java version.

### Checklists

The implementation of these tasks is managed through three checklists, one for each stage.
At the beginning of the first stage, create three GitHub issues, one for each stage.
As each stage is completed, the corresponding issue can be closed.
Each issue need not be assigned to the same person,
though it may be desirable to do so for purposes of continuity.

- [Add support for a new Java version](https://github.com/jenkins-infra/release/blob/master/.github/ISSUE_TEMPLATE/3-add-support-for-a-new-java-version.md)
- [Recommend a new Java version](https://github.com/jenkins-infra/release/blob/master/.github/ISSUE_TEMPLATE/4-recommend-a-new-java-version.md)
- [Require a new Java version](https://github.com/jenkins-infra/release/blob/master/.github/ISSUE_TEMPLATE/5-require-a-new-java-version.md)

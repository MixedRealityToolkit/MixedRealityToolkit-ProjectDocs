# Approving Pull Requests

## Obtaining the role

Contributors with the **write** role can merge pull requests. A maintainer can assign this role to a contributor, as long as the contributor has demonstrated the following:

* Must be part of the one of the Mixed Reality Toolkit's steering committee [affiliated organizations](https://github.com/MixedRealityToolkit/MixedRealityToolkit-MVG/blob/main/org-docs/STEERING-COMMITTEE.md).
* Must have read and accepted the contributor guidelines.
* Must have shown a consistent pattern of helpful, non-threatening, and friendly behavior towards other community members in the past.
* Should have opened and successfully run medium to large PR’s in the past 6 months.
* Should have participated in multiple code reviews of other PR’s, including those of other maintainers and contributors.
* Should be active on Mixed Reality Toolkit community forums.

If the contributor leaves the affiliated organization, the contributor will lose the **write** role.

## Basic validation

Contributors must ensure that the following criteria is met before a pull request (PR) can be merged:

* All PR comments are resolved.
* Approvals are dismissed when a new commit is pushed.
* PR has a clear and concise title.
* PR has a clear description explaining the fix or feature. 
* The PR passes all status checks, including unit tests.
* The code changes must have `<summary>` blocks for all public and protected types and members.
* Author confirmed code changes were tested within the Unity Editor and on at least one XR device. This does not apply for changes to only documentation or pipeline scripts.
* The PR must have at least one approval from a contributor that has the write role. Some circumstances may require additional approvals.

If any of these criteria are not met, block the pull request by adding the "Do Not Merge" label, and kindly explain your reasoning for blocking.

## Additional considerations

For the best results contributor should also consider adding the following before a PR is merged:

* The PR's description should reference the issue that is being fixed or implemented.
* The PR should contain new or updated unit tests that validate the new code changes.
* Visual updates should have screen shots or videos demonstrating the changes.
* The code changes should have `<summary>` blocks for all types and members, even private and internal ones.

### Design changes

The visual design of the UX components must often go through some sort of design review before approved. As such, if a pull request contains an unavoidable change to the appearance of an existing visual component, a 3/4 majority of the project maintainers must approve the pull request.

### Breaking changes

A change is considered to be breaking if it alters an API signature or behavior in such a way to break applications built on a previous release of the MRTK. If a pull request introduces a breaking change, a 3/4 majority of the project maintainers must approve the pull request.

### Build breaks and automation failures

If a merged pull request breaks subsequent builds or automated tests, the author must fix the failed change as soon as possible, or risk having the change reverted.

# Approving Pull Requests

All changes to the `main` branch must be done through a pull request process to ensure that the changes are reviewed and approved.

## Obtaining the role

Contributors with the **write** GitHub role can approve pull requests. A maintainer can assign this role to a contributor, as long as the contributor has demonstrated the following:

* Must be part of the one of the Mixed Reality Toolkit's steering committee [affiliated organizations](https://github.com/MixedRealityToolkit/MixedRealityToolkit-MVG/blob/main/org-docs/STEERING-COMMITTEE.md).
* Must have read and accepted the contributor guidelines.
* Must have shown a consistent pattern of helpful, non-threatening, and friendly behavior towards other community members in the past.
* Should have opened and successfully run medium to large PR’s in the past 6 months.
* Should have participated in multiple code reviews of other PR’s, including those of other maintainers and contributors.
* Should be active on Mixed Reality Toolkit community forums.

If the contributor leaves the affiliated organization, the contributor will lose the **write** GitHub role.

## Basic validation

Contributors must ensure that the following criteria are met before a pull request (PR) can be merged:

* Pull request approvals are dismissed when a new commit is pushed.
* All pull request feedback and change requests are resolved.
* The pull request has a clear and concise title, and a detailed description explaining the changes.
* All status checks, including unit tests, pass successfully for the pull request.
* Code changes must have XML documentation text (i.e.`<summary>`) for all public visible types and members. See [Compiler Warning (level 4) CS1591](https://learn.microsoft.com/dotnet/csharp/language-reference/compiler-messages/cs1591) for more details.
* The pull request author confirmed code changes were tested within the Unity Editor and on at least one XR device.
* The pull request must have at least one approval from an assigned code owner. Some circumstances may require additional approvals.

If any of these criteria are not met, the pull request can not be merged. If  block the pull request by adding the "Do Not Merge" label, and kindly explain your reasoning for blocking.

## Additional considerations

The pull request author should also consider adding the following before a PR is merged:

* The PR's description should reference the issue that is being fixed or implemented.
* The PR should contain new or updated unit tests that validate the new code changes.
* Visual updates should have screen shots or videos demonstrating the changes.
* The code changes should have `<summary>` blocks for all types and members, even private and internal ones.

## Build breaks and automation failures

If a merged pull request breaks subsequent builds or automated tests, the author must fix the failed change as soon as possible, or risk having the change reverted.

## Blocking pull requests

There may be times when a pull request contains changes that need further consideration before approval. Such occurrence include, but not limited to, design and breaking changes.  In such cases, you should block the pull request by adding the "Merge: Blocked" label, and kindly explain your reasoning for blocking. Then notify the project's maintainers.

### Design changes

If a pull request contains visual changes to UI controls that can't be easily undone or turned off by an application developer, these pull requests must be blocked until the project maintainers review the change. Mark these changes with the "Type: Design Change" label.

### Breaking changes

A change is considered to be breaking if it contains incompatible API or behavior changes, such that it will break applications built on a previous released versions of the MRTK package. If a pull request introduces a breaking change, these pull requests must be blocked. Also, mark these changes with the "Type: Breaking Change" label.

### Unblocking a pull request

Only project maintainers can unblock a pull request, and remove the "Merge: Blocked" label. To unblock a pull request, one maintainer from each affiliated organization must approve the pull request. Once this occurs, the "Merge: Blocked" label can be removed, and pull request completed.

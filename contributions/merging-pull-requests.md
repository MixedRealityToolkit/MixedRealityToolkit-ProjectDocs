# Approving Pull Requests

All changes to the `main` branch must be done through a pull request process to ensure that the changes are reviewed and approved.

## The role

Contributors with the **write** GitHub role can approve pull requests.

## Basic validation

Contributors must ensure that the following criteria are met before a pull request (PR) can be merged:

* Pull request approvals are dismissed when a new commit is pushed.
* All pull request feedback and change requests are resolved.
* The pull request has a clear and concise title, and a detailed description explaining the changes.
* All status checks, including unit tests, pass successfully for the pull request.
* Code changes must have XML documentation text (i.e.`<summary>`) for all public visible types and members. See [Compiler Warning (level 4) CS1591](https://learn.microsoft.com/dotnet/csharp/language-reference/compiler-messages/cs1591) for more details.
* The pull request author confirmed code changes were tested within the Unity Editor and on at least one XR device.
* The pull request must have at least one approval from an assigned [code owner](code-owners.md). Some circumstances may require additional approvals.

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

There may be times when a pull request contains changes that need further consideration before approval. Such occurrence include, but not limited to, design and breaking changes.  In such cases, you should block the pull request by adding the "Merge: Blocked" label, and kindly explain your reasoning for blocking. Then notify the project's Maintainers.

### Design changes

If a pull request contains visual changes to UI controls that can't be easily undone or turned off by an application developer, these pull requests must be blocked until the project Maintainers review the change. Mark these changes with the "Type: Design Change" label.

### Breaking changes

A change is considered to be breaking if it contains incompatible API or behavior changes, such that it will break applications built on a previous released versions of the MRTK package. If a pull request introduces a breaking change, these pull requests must be blocked. Also, mark these changes with the "Type: Breaking Change" label.

### Unblocking a pull request

Only project Maintainers can unblock a pull request, and remove the "Merge: Blocked" label. To unblock a pull request, Maintainers follow the decision making rules in the [GOVERNANCE.md](../GOVERNANCE.md) file.

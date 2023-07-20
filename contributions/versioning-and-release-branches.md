# Versioning and Release Branches

## Semantic versioning

Mixed Reality Toolkit packages are individually versioned, following the [Semantic Versioning 2.0.0 specification](https://semver.org/spec/v2.0.0.html). Note that the '3' in MRTK3 is not a version number. It's an indicator of the generation of the underlying architecture.

Individual versioning will enable faster servicing while providing improved developer understanding of the magnitude of changes and reducing the number of packages needing to be updated to acquire the desired fix(es).

For example, if a non-breaking new feature is added to the UX core package that contains the logic for user interface behavior, the minor version number will increase (from 3.0.x to 3.1.0). Since the change is non-breaking, the UX components package, which depends upon UX core, is not required to be updated.

As a result of this change, there isn't a unified MRTK3 product version.

To help identify specific packages and their versions, MRTK3 provides an "about" dialog that lists the relevant packages included in the project. To access this dialog, in Unity on the menu bar, select `Mixed Reality` > `MRTK3` > `About MRTK`.

### Process of updating versions

Package versioning is managed by the project maintainers. During a pull request into the `main` branch, maintainers should decide if package versions need to change. Maintainers should consider the following questions, and then if needed, request that the pull request author update package versions.

> During this time maintainers should be aware of the released packages published to the project's [releases page](https://github.com/MixedRealityToolkit/MixedRealityToolkit-ProjectDocs/releases).

### Is this a breaking change?

Follow the rules outlined at [Breaking changes](merging-pull-requests.md#breaking-changes). If this is breaking change, the package's major version should be incremented from the latest released major version of the package. For example, if the package's latest release was v3.4.1, the new version should be v4.0.0.

### Is this new functionality?

If the change contains new functionality that works in a backward compatible manner, the package's minor version should be incremented from the latest released minor version. For example, if the package's latest minor release was v3.4.1, the new version should be v3.5.0.

### Is this just backward compatible bug fix?

If the change only contains backward compatible bug fixes, the package's patch version should be incremented from the latest released patch version. For example, if the package's latest patch release was v3.4.1, the new version should be v3.4.2.

## Package release process

A majority of project maintainers must agree to release a Mixed Reality Toolkit package to project's [releases page](https://github.com/MixedRealityToolkit/MixedRealityToolkit-ProjectDocs/releases). The process of releasing to this [page](https://github.com/MixedRealityToolkit/MixedRealityToolkit-ProjectDocs/releases) is the following:

1. Verify that the package is in stable condition.
2. Create release notes using [Keep a Changelog](https://keepachangelog.com/en/1.1.0/).
3. Create UPM package for the commit being released.
4. Create ZIP file containing source code being released.
5. Add a `git` tag the commit being released, following the format [package-postfix]-vMAJOR.MINOR.PATCH. For example, core-v3.0.1 or input-v3.2.0.
6. The release notes, UPM package, and source code are then posted under project's [releases page](https://github.com/MixedRealityToolkit/MixedRealityToolkit-ProjectDocs/releases).

This process only needs to be applied when releasing on the project's [releases](https://github.com/MixedRealityToolkit/MixedRealityToolkit-ProjectDocs/releases). This process does not limit the ability of releasing versions MRTK package via other mechanism outside of this repository. Any affiliate organizations can build and/or create release packages using their own mechanisms.

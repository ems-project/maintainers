# Pull Requests
EMS-project uses the [GitFlow](https://www.atlassian.com/git/tutorials/comparing-workflows/gitflow-workflow) strategy to incorporate code changes.

Branches, commits, and GitHub issues MUST respect conventions as described in this document.

UNLESS specified otherwise in the [Branch types](#branch-types) definition, each pull request:
* MUST implement EXACTLY one GitHub issue
* MUST target the `develop` branch
* MUST use the PR/Commit/Issue Template

## Templates
### PR Template

### Commit Template

### Issue Template


## Branches
### Branch naming convention
A branch MUST be named `<type>/<short-description>` where:
* `<type>` is one of
   * `feat`
   * `bug`
   * `hot`
   * `maintain`
   * `dep`
* `<short-description>` is a short description separated by `-` dashes explaining the reason of existance of the branch

### Branch types <a name="branch-types"/>

#### Feature Branch
A `feat/new-feature-description` branch is used to add new functionality to the project.

#### Bugfix Branch
A `bug/description-of-the-fix` branch is used patch existing features that are broken.

A bugfix branch MAY contain a new feature if it's tightly coupled to the bugfix itself.

#### Hotfix Branch
A `hot/description-of-the-fix` branch is used to patch a broken feature currently in production.

A hotfix branch must be the smallest possible implementation to fix the issue in production. And MAY implement a GitHub Issue.

The pull request MUST target the `master` branch.

#### Maintain Branch
A `maintain/description-of-configuration-change` branch is used to change configurations not related to the project in production. For example: travis, phpunit, ...

A maintain branch May implement a GitHub Issue. But will mostly be used to implement requirements defined by this maintainer repository.

#### Dependency Branch
A `dep/description-of-dependency-or-deprecated-cleaning` branch is used to clean dependencies and deprecations in the project.
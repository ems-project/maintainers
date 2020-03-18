# Pull Requests
EMS-project uses the [GitFlow](https://www.atlassian.com/git/tutorials/comparing-workflows/gitflow-workflow) strategy to incorporate code changes.

## Branch naming convention
A branch should be named `<type>/<short-description>` where:
* `<type>` is one of
   * `feat`
   * `bug`
   * `hot`
   * `maintain`
   * `dep`
* `<short-description>` is a short description separated by `-` dashes explaining the reason of existance of the branch

## Branch types

### Feature Branch
A `feat/new-feature-description` branch is used

### Bugfix Branch
A `bug/description-of-the-fix` branch is used

### Hotfix Branch
A `hot/description-of-the-fix` branch is used

### Maintain Branch
A `maintain/description-of-configuration-change` branch is used

### Dependency Branch
A `dep/description-of-dependency-or-deprecated-cleaning` branch is used
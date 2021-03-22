# Creating a new EMS-project

All ems-projects MUST be implemented using the [coding Standards](coding_standards.md). To enforce them we use the default configuration files for php-cs and php-stan verification. All projects MUST use these templates:

* [.php_cs.dist](../templates/.php_cs.dist)
* [phpstan.neon.dist](../templates/phpstan.neon.dist)

These tools are run automatically on each push to a branch and on each pull-request using github actions. To enforce this the follow template must be installed on your project:
* [.github/workflows/code_quality.yml](../templates/.github/workflows/code_quality.yml)

## Exceptions

* EMSCoreBundle is currently not required to enforce "final/abstract" classes.

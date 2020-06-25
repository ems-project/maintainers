# Coding Standards

We will not define an exhaustive list of coding standards. However php-cs-fixer is required to run for every pull request.
An alias is provided via composer:
````bash
composer phpcs
````
This will run `php-cs-fixer fix` using the coding standards defined in [.php_cs.dist](../templates/.php_cs.dist).

## PHPCS / PHPCBF
We are currently migrating from php-cs to php-cs-fixer, because both are doing the same job, but the latter is allowing us to configure the standards in PHP itself!

## Code quality

PHPStan is run at level 8, you can check for errors locally using the following composer alias:
`````bash
composer phpstan
`````
In order to run at level 8 for every subproject, we generated a baseline where needed.
However, it is forbidden to add new exceptions in the baseline with new Pull Requests. It is encouraged to resolve small issues on every PR so that we can disable the baseline everywhere!
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

## Exceptions

When there is an unexpected exception, an exception that should never happened, like an exception throw in order to solve a phpstan issue, throw a ```\RuntimeException```. We should avoid using ```\Exception``` in order to simplify logs analysis.

In other cases you should or use a specific exception, which can be handled upper in the stack. Or throw a [Symfony HTTP based exception](https://github.com/symfony/http-kernel/tree/5.x/Exception):

  - 401: Symfony\Component\HttpKernel\Exception\UnauthorizedHttpException
  - 404: Symfony\Component\HttpKernel\Exception\NotFoundHttpException
  - 405: Symfony\Component\HttpKernel\Exception\MethodNotAllowedHttpException

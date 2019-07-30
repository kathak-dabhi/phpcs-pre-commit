# About
Install git pre-commit hook for running PHPCS code checking to [PSR-2](https://www.php-fig.org/psr/psr-2) coding standard. It checks only files that are to be committed.
And run PHPUnit to run unit tests

# Install
Add git repository to `composer.json`
```
"repositories": [
    {
        "url": "https://github.com/kathak-dabhi/phpcs-pre-commit.git",
        "type": "git"
    }
],
```

Install kathak-dabhi/phpcs-pre-commit with composer require command:
```sh
$ composer require kathak-dabhi/phpcs-pre-commit
```
Or alternatively, include a dependency as dev dependancy
```sh
$ composer require --dev kathak-dabhi/phpcs-pre-commit:dev-master
```
Now Enable Pre-commit hook in composer.json file
```
"post-install-cmd": [
    "cp ./vendor/kathak-dabhi/phpcs-pre-commit/src/pre-commit .git/hooks/pre-commit"
],
"post-update-cmd": [
    "cp ./vendor/kathak-dabhi/phpcs-pre-commit/src/pre-commit .git/hooks/pre-commit"
]
```
>*If there is an error occured after composer install to setup the pre-commit-hooks, 
**'cp' is not recognized as an internal or external command,operable program or batch file.**
>it is due to you are on windows machine that is not allowing to run the shell script from package, so simple run the `composer install` again from the **gitbash** to finish the setup.*

Also make the pre-commit file executable by running below command
```
 sudo chmod 755 .git/hooks/pre-commit
 ```
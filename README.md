# About

# Install
Install kathak-dabhi/phpcs-pre-commit with composer require command:
```sh
composer require kathak-dabhi/phpcs-pre-commit
```
Or alternatively, include a dependency as dev dependancy
```sh
composer require --dev kathak-dabhi/phpcs-pre-commit:dev-master
```
Now Enable Pre-commit hook in composer.json file
```sh
"post-install-cmd": [
    "./vendor/kathak-dabhi/phpcs-pre-commit/src/setup"
],
"post-update-cmd": [
    "./vendor/kathak-dabhi/phpcs-pre-commit/src/setup"
]
```
>***If there is an error occured while composer install to setup the pre-commit-hooks, it is due to you are on windows machine that is not allowing to run the shell script from package, so simple run the `composer install` again from the gitbash to finish the setup.***

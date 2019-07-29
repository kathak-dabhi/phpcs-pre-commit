# About
***

# Install
***
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
    "sh ./vendor/kathak-dabhi/phpcs-pre-commit/src/setup.sh"
],
"post-update-cmd": [
    "sh ./vendor/kathak-dabhi/phpcs-pre-commit/src/setup.sh"
]
```

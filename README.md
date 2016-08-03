kujira-phpunit-printer
======================

A PhpUnit result printer.

Forked to use PSR-4 autoloading and because the old autoload setting frankly
doesn't make sense and you shouldn't be so eager to add global packages to your
environment. Other people don't seem to have a problem with it though and I'm
not sure if this breaks their use case so I didn't make this a pull request.

## Requirements

 * PHP 5.3.0 or later.

## How it looks

![Screenshot](/kujira-phpunit-result-printer.jpg?raw=true "Kujira phpunit result printer")

## Installation

    composer require --dev phpunit/phpunit codeia/kujira-phpunit-printer

## Usage

There are many ways. This is my preferred:

* Add a script to your `composer.json` file:

```json
    "scripts": {
        "test": "phpunit TEST_DIR --colors=always --printer 'Kujira\\PHPUnit\\Printer'"
    }
```

* Run tests by calling `composer test [test file]` while in your project root or
just `composer test` to run all tests under `TEST_DIR`.
* Invoking `phpunit` this way makes the autoloader available so there's no need
to reference the class file.
* You can add more arguments with something like `composer test -- --testdox --some-param=value`
* Configure your php.ini default_charset to UTF-8
* Configure your terminal to display UTF-8 charset and use a UTF-8 compatible font like DejaVu Sans Mono

## License

The Kujira result printer for PHPUnit is licensed under the [MIT license](LICENSE).

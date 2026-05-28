---
layout: documentation
title: Installing Perpl
---

# System Requirements

Perpl requires PHP to be installed. Compatible PHP versions include 8.1 through 8.4. Required PHP extensions include PDO and DOM.

Perpl requires an SQL database such as MySQL, MariaDB, MS SQL Server, PostgreSQL, SQLite, or Oracle.

Perpl is multi-platform and we strive to make it run equally well on Windows, Linux and macOS.

# Installing Perpl

## Via Composer

We recommend installing Perpl using [Composer](http://getcomposer.org/). To install the currently stable version of Perpl simply run the command:

```bash
composer require perplorm/perpl
```

Alternatively you can add Perpl to your `composer.json` and then use the `composer update` command to install Perpl and any dependencies.

```json
{
    "require": {
        "perplorm/perpl": ">=2.0"
    }
}
```

## Via Git

You can also install Perpl by cloning the official repository:

```bash
git clone https://github.com/perplorm/perpl vendor/perplorm/perpl
```

To update Perpl later, just pull the latest changes:

```bash
cd myproject/vendor/perplorm/perpl
git pull
```

## Via Zip

Perpl is also available as a [zip file](https://github.com/perplorm/perpl/archive/refs/heads/main.zip) for manual installation.

## Perpl Directory Structure

The root directory of the Perpl library includes the following folders:

| Folder    | Explanation                                                                                        |
|-----------|----------------------------------------------------------------------------------------------------|
| bin       | Contains scripts that manage the Perpl command line tool (depending on your operating system)      |
| features  | Tests written with the Behat framework                                                             |
| resources | Contains some files such as the database XSD or DTD                                                |
| src       | The Perpl source code. Pass over if you just want to use Perpl, not to contribute.                 |
| tests     | Perpl unit tests. Ignore this if you don't want to contribute to Perpl.                            |

## Testing Perpl Installation

The Perpl generator component bundles a `perpl` sh script (and a `perpl.bat` script for Windows). This script makes it easy to execute build commands. You can test this component is properly installed by calling the `perpl` script from the CLI (example for Linux or macOS):

```bash
cd myproject
vendor/bin/perpl
```

The command should output the Perpl version followed by a list of the options and the available commands. We will learn to use these commands later.

> [!TIP]
> In order to allow an easier execution of the script, you can also add the
> Perpl generator's `bin/` directory to your PATH, or create a symlink. For
> example:
>
> ```bash
> cd myproject
> ln -s vendor/bin/perpl perpl
> ```
>
> Or simply edit your `.bashrc` or `.zshrc` file:
>
> ```bash
> export PATH=$PATH:/path/to/vendor/bin/
> ```
>
> On Windows you could set the PATH for the opened command with:
>
> ```bash
> set PATH=%PATH%;C:/path/to/vendor/bin/
> ```
>
> To globally define the PATH adjust it inside the "Environment Variables", which
> you can find in your system advanced settings panel.

# Including Perpl in your PHP code

You can now include Perpl in your PHP code, as with other Composer libraries:

```php
<?php
// setup the autoloading
require_once __DIR__ . '/vendor/autoload.php';
// setup Perpl
require_once __DIR__ . '/generated-conf/config.php';
```

At this point, Perpl should be setup and ready to use. You can follow the steps in the [Build Guide](02-buildtime.html) to try it out.

# Troubleshooting

## Getting Help

If you can't manage to install Perpl, don't hesitate to ask for help. See [Support](../support.html) for details on getting help.

---
<span class="next">[Next: Building a project &rarr;](02-buildtime.html)</span>

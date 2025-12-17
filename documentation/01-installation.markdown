---
layout: documentation
title: Installing Perpl
---

# System Requirements #

Perpl requires PHP to run.  PHP required plugins include PDO and DOM.  Perpl supports PHP versions from 8.1 through to 8.4.

Perpl requires an SQL database such as; MySQL; MariaDB; MS SQL Server; PostgreSQL; SQLite; Oracle.

Perpl is multi-platform and we strive to make it run equally well on Windows, Linux and macOS.

# Installing Perpl #

We recommend installing Perpl using [Composer](http://getcomposer.org/).

`composer install perplorm/perpl`

Alternatively you can add Perpl to your composer.json and then use the 'composer update' command to install Perpl and any dependencies.

```json
{
    "require": {
        "perplorm/perpl": ">=2.0"
    }
}
```

Perpl is also available in the following formats:
* clone from the official repository https://github.com/perplorm/perpl,
* checkout from Subversion through Github
* zip file https://github.com/perplorm/perpl/archive/refs/heads/main.zip


## Perpl Directory Structure ##

The root directory of the Perpl library includes the following folders:

|Folders        |Explanations
|---------------|----------------------------------------------------------------------
|bin            |Contains three scripts that manage perpl command line tool (depending of your operating system)
|features       |Tests written with the Behat framework
|resources      |Contains some files such as the database XSD or DTD
|src            |The Perpl source code. Pass over if you just want to use Perpl, not to contribute.
|tests          |Perpl unit tests. Ignore this if you don't want to contribute to Perpl.

## Testing Perpl Installation ##

The Perpl generator component bundles a `perpl` sh script (and a `perpl.bat` script for Windows). This script makes it easy to execute build commands. You can test this component is properly installed by calling the `perpl` script from the CLI (example for Linux or macOS):

```$ cd myproject
$ vendor/bin/perpl
```

The command should output the Perpl version following by a list of the options and the available commands. We will learn to use these commands later.

> [!TIP]
> In order to allow an easier execution of the script, you can also add the
> Perpl generator's `bin/` directory to your PATH, or create a symlink. For
> example:
>
> ```$ cd myproject
> $ ln -s vendor/bin/perpl perpl
> ```
>
> Or simply edit your .bashrc or .zshrc file:
>
> `export PATH=$PATH:/path/to/vendor/bin/`
>
> On Windows you could set the PATH for the opened command with:
>
> `set PATH=%PATH%;C:/path/to/vendor/bin/`
>
> To globally define the PATH adjust it inside the "Environment Variables", which
> you can find in your system advanced settings panel.

At this point, Perpl should be setup and ready to use. You can follow the steps in the [Build Guide](02-buildtime.html) to try it out.

## Troubleshooting ##

### Getting Help ###

If you can't manage to install Perpl, don't hesitate to ask for help. See
[Support](../support.html) for details on getting help.

---
<span class="next">[Next: Building a project &rarr;](02-buildtime.html)</span>

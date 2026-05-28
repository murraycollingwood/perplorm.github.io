---
meta-language: en
meta-og:description: Installing ❊ Perpl ❊
meta-og:image: https://perplorm.github.io/images/perpl-icon.png
meta-og:title: ❊ Perpl ❊, The Blazing Fast Open-Source PHP ORM
meta-viewport: width=device-width
title: Installing ❊ Perpl ❊ -&nbsp;❊ Perpl ❊, The Blazing Fast Open-Source PHP8 ORM
---

# Installing ❊ Perpl ❊

❊ Perpl ❊ is available via [composer](#via-composer) (see also <https://packagist.org/packages/perplorm/perpl>), as a clone from the official [Github repository](https://github.com/perplorm/perpl) and as a "traditional" [tgz](https://github.com/perplorm/perpl/tarball/main) or [zip](https://github.com/perplorm/perpl/zipball/main) package. Whatever installation method you may choose, getting ❊ Perpl ❊ to work is pretty straightforward.

## Prerequisites

❊ Perpl ❊ just requires:

- [PHP 8.1](https://www.php.net/) or newer, with the DOM (libxml2) module enabled
- A supported database (MySQL, MS SQL Server, PostgreSQL, SQLite, Oracle)


❊ Perpl ❊ also uses some Symfony components to work properly:

- [Config](https://github.com/symfony/Config) : used in the source code to manage and validate configuration.
- [Console](https://github.com/symfony/Console) : manages the generators ❊ Perpl ❊ uses.
- [Yaml](https://github.com/symfony/Yaml)
- [Validator](https://github.com/symfony/Validator) : manages validations with ❊ Perpl ❊.
- [Finder](https://github.com/symfony/Finder) : used in the source code to manage files.

> **Tip** ❊ Perpl ❊ uses the PDO and SPL components, which are bundled and enabled by default in PHP8.

## Setup

### Via Composer

We advise you to rely on [Composer](https://getcomposer.org/) to manage your projects' dependencies. If you want to install ❊ Perpl ❊ via Composer, just create a new `composer.json` file at the root of your project's directory with the following content:

```json
{
    "require": {
        "perplorm/perpl": ">=2.0"
    }
}
```

Then you have to download Composer itself so in a terminal just type the following:

```bash
$ wget https://getcomposer.org/composer.phar
# If you haven't wget on your computer
$ curl -s https://getcomposer.org/installer | php
```

Finally, to install all your project's dependencies, type the following:

```bash
$ php composer.phar install
```

### Via Git

If you want, you can also setup ❊ Perpl ❊ using Git cloning the Github repository:

```bash
$ git clone git://github.com/perplorm/perpl vendor/perplorm/perpl
```

❊ Perpl ❊ is well unit-tested so the cloned version should be pretty stable. If you want to update ❊ Perpl ❊, just go to the repository and pull the remote:

```bash
$ cd myproject/vendor/perplorm/perpl
$ git pull
```

## ❊ Perpl ❊ Directory Structure

The root directory of the ❊ Perpl ❊ library includes the following folders:

| Folders   | Explanations                                                                                      |
| --------- | ------------------------------------------------------------------------------------------------- |
| bin       | Contains scripts that manage the ❊ Perpl ❊ command line tool (depending of your operating system) |
| resources | Contains some files such as the database XSD or DTD                                               |
| src       | The ❊ Perpl ❊ source code. Pass over if you just want to use ❊ Perpl ❊, not to contribute.       |
| templates | Well, templates. ❊ Perpl ❊ makes use of templating.                                               |
| tests     | ❊ Perpl ❊ unit tests. Ignore this if you don't want to contribute to ❊ Perpl ❊.                   |

## Testing ❊ Perpl ❊ Installation

The ❊ Perpl ❊ generator component bundles a `perpl` sh script (and a `perpl.bat` script for Windows). This script makes it easy to execute build commands. You can test this component is properly installed by calling the `perpl` script from the CLI:

```bash
$ cd myproject
$ vendor/bin/perpl
```

The command should output the ❊ Perpl ❊ version followed by a list of the options and the available commands. We will learn to use these commands later.

> **Tip** In order to allow an easier execution of the script, you can also add the
> perpl generator's `bin/` directory to your PATH, or create a symlink. For example:
>
> ```bash
> $ cd myproject
> $ ln -s vendor/bin/perpl perpl
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

At this point, ❊ Perpl ❊ should be setup and ready to use. You can follow the steps in the [Build Guide](https://perplorm.github.io/documentation/02-buildtime.html) to try it out.

## Troubleshooting

### Getting Help

If you can't manage to install ❊ Perpl ❊, don't hesitate to ask for help. See [Support](https://perplorm.github.io/support.html) for details on getting help.

---

[Next: Building a project →](https://perplorm.github.io/documentation/02-buildtime.html)



---
<span class="next">[Next: Building a project &rarr;](02-buildtime.html)</span>

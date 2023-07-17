# Umami Drupal Project
Mini-project for Drupal candidates

## Getting Started
:tophat: _Hat tip to our friends at Lullabot for the [awesome simple setup article](https://www.lullabot.com/articles/the-simplest-path-to-a-drupal-local-environment)._

### Before you begin
1. Make sure you have [Composer](https://getcomposer.org/download/) installed locally.
2. Make sure you have [SQLite](https://sqlite.org/download.html) installed locally. If you're on a Mac, you most likely already do. (You need it if you want to use these setup instructions, at least.) If you're on a mac you can install with [homebew](https://brew.sh/). `brew install sqlite`
3. Create a `git clone` of this project. All commands from here assume you're inside the project folder (probably `/drupal-mini-project` unless you were fancy and changed it to something else).

### Installing and starting the site
This project installs Drupal core using Composer. To get going, start by installing core and drush.

```shell
composer install
```

This project uses the [Umami demo](https://www.drupal.org/docs/umami-drupal-demonstration-installation-profile) site as the basis for your work. Because who doesn't like yummy food? To get your local setup, use these commands.

```shell
vendor/bin/drush site-install demo_umami --db-url=sqlite://../drupal.sqlite
vendor/bin/drush runserver
```

By default, the server will listen on http://127.0.0.1:8888. The `site-install` command will give you your username and password, or you can `vendor/bin/drush uli` to get a login link.

### A note about your local PHP
You may find in working with this project that you run out of memory. If you need to raise the memory limit try the following.

1. Depending on how you installed PHP you will need to find where your specific `php.ini` file is.
1. This will show the path to your `php.ini` file. `php -r 'phpinfo();' | grep 'php.ini'`
1. Load the `php.ini` file in your favorite text editor and change the `memory_limit` to something like `512M`.

## Installing Dependencies

If you need to install modules and/or themes to complete your task, please feel free to.  

For contributed Drupal.org modules, please use composer:

`composer require dupal/example`

For custom modules, you can include them directly in the code base.

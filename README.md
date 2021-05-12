# Umami Drupal Project
Mini-project for Drupal candidates

## Getting Started
:tophat: _Hat tip to our friends at Lullabot for the [awesome simple setup article](https://www.lullabot.com/articles/the-simplest-path-to-a-drupal-local-environment)._

### What you'll need
1. Composer installed locally.
2. SQlite installed locally. (if you want to use these setup instructions, at least.)
3. A `git clone` of this project. All commands from here assume you're inside the project folder.

### How to get Started
This project installs Drupal core using Composer. To get going, start by installing core and drush.
```
$ composer install
$ cd web
```

This project uses the [Umami demo](https://www.drupal.org/docs/umami-drupal-demonstration-installation-profile) site as the basis for your work. Because who doesn't like yummy food? To get your local setup, use these commands.

```
$ vendor/bin/drush site-install demo_umami --db-url=sqlite://../drupal.sqlite
$ vendor/bin/drush runserver
```
By default, the server will listen on http://127.0.0.1:8888. The `site-install` command will give you your username and password, or you can `vendor/bin/drush uli` to get a login link.

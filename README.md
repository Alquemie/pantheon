# WordPress built with Composer for Pantheon

This repository is used by Alquemie Marketing to manage WordPress workflow with Pantheon hosted websites.

## Installation

1. Create a new site in [Pantheon](https://dashboard.pantheon.io/) based on **Empty WP** Upstream
2. Clone the site repository
3. Run the *BUILD* command: `$ ./private/build`

## Development Process

### WordPress Core and Plugins
The WordPress core code plugins are managed by editing the `composer.json` file.  This allows you to track code changes within the projects Git repository without including the actual file changes.

After changing the `composer.json` file you need to run the `$ ./private/build -u` including the "update" option flag

### Custom Code
Custom code is managed under the `code` directory of the project, which matches the standard structure of a WordPress installation.  These files are synced to the web path during the build process.

Changes to the `code` directory will be added to the site when the build script is run: `$ ./private/build`


## Build Script
Run `$ ./private/build -h` for more information
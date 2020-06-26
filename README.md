# Lando WordPress Configuration
[Lando](https://github.com/lando/lando) is an extremely flexible local development environment that is based on Docker. If your system can run Docker, then you can run Lando regardless if you are on a Mac, Windows, or Linux machine. The beauty of Lando is that most of the Docker configuration is handled for you through prebuilt "recipes", which greatly simplifies the setup process.

This repository contains the Lando configuration file (`.lando.yml`) that I use for my WordPress projects along with the `php.ini` file that it references.

## Usage
These steps assume that Lando is already [installed](https://docs.lando.dev/basics/installation.html).

1. Download a zipped copy of this repository and copy the `.lando.yml` and `php.ini` files to your project root.
1. Open up `.lando.yml` and rename the app's `name` to something unique.
1. Specify the desired PHP version, web server (apache or nginx), and database server (mysql, mariadb, or mongodb).
1. Uncomment the `pma` service if you want to run PhpMyAdmin.
1. Uncomment the `events` section if you would like to back up the database each time the containers are stopped.
1. Change the proxy from `wpsandbox.test` to your desired domain.
1. Update your hosts file so that the app's domain points to 127.0.0.1.
1. Run the command `lando start` from the project root.

## Documentation
Refer to Lando's extensive [documentation](https://docs.lando.dev/).

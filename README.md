# drupal-8-umami-example
An example Drupal 8 site that can be imported into the Drupal 8 Docker development environment.

# Using this Repo

This repo is designed to be used alongside the [Drupal 8 Docker development environment](https://github.com/OULibraries/drupal-8-docker-dev). It contains the contents of the `sites` directory for a single site Drupal 8 instance.

To use this site, clone this repo into the `dev` directory in the Drupal 8 Docker development environment repo.

1. Clone this repo into the `dev` directory in the Drupal 8 Docker development environment repo.
2. Set ownership of the `dev` directory to `www-data` (UID: 33).
   ```bash
   $ chown -R 33:33 ./dev
   ```
3. Download the [Umami DB dump from the releases page](https://github.com/OULibraries/drupal-8-umami-example/releases/download/0.0.1/umami_db.sql) and place it in `mysql/resources/init`.
4. Start the Drupal 8 Docker development environment.
   ```bash
   $ docker-compose up -d --build
   ```
5. Wait for the MySQL database to become available and navigate to `http://localhost:8080`
   to view the Umami example site.

Admin credentials for the example site are admin/password.

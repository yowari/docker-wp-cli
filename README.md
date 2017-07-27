# WP-CLI

Docker image for [WordPress](https://wordpress.org/) with the ability to use
[WP-CLI](http://wp-cli.org/) over the installation.

# Installation

```
docker pull yowari/wp-cli
```
# Usage

```
docker run --name some-wp-cli --link some-mysql:mysql -d yowari/wp-cli
```

The image is based on the official
[WordPress image](https://github.com/docker-library/wordpress). Some environment
variables are available to configure your WordPress instance and new once are
added to set the configuration of the wp-admin page.

- `-e WORDPRESS_DB_HOST=...` (defaults to the IP and port of the linked mysql
  container)
- `-e WORDPRESS_DB_USER=...` (defaults to "root")
- `-e WORDPRESS_DB_PASSWORD=...` (defaults to the empty value)
- `-e WORDPRESS_DB_NAME=...` (defaults to "wordpress")
- `-e WORDPRESS_TITLE=...` (defaults to "blog")
- `-e WORDPRESS_ADMIN_USER=...` (defaults to "admin")
- `-e WORDPRESS_ADMIN_PASSWORD=...` (defaults to "admin")
- `-e WORDPRESS_ADMIN_EMAIL=...` (defaults to "admin@example.com")

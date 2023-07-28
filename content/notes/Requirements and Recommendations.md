---
title: Requirements and Recommendations
enableToc: true
---

## Minimum Requirements

- Webserver such as Apache, [Nginx](https://github.com/matomo-org/matomo-nginx), IIS, LiteSpeed, etc.
- Matomo 4.x requires PHP version 7.2.5 or greater. Matomo fully works with PHP 8 as well. (the older Matomo 3.x required PHP version 5.5.9 or PHP 7.x)
- MySQL version 5.5 or greater, or MariaDB
- (enabled by default) PHP extension [pdo](http://php.net/pdo) and [pdo_mysql](http://php.net/pdo_mysql), or the mysqli extension.
- Matomo can be run on any operating system such as Linux (Ubuntu, RedHat, CentOS, Raspberry Pi OS, etc.), [Windows](https://matomo.org/faq/matomo-on-windows/), macOS Server or FreeBSD.

**Note:** For WordPress sites, we can easily [install Matomo Analytics fully in our WordPress, with a few clicks!](https://wordpress.org/plugins/matomo/)

## Recommendations

- PHP 8.x versions
- MySQL 8+ or MariaDB
- To make the most out of Matomo, you also need a few extra PHP extensions such as the **[PHP GD extension](https://matomo.org/faq/troubleshooting/faq_34/)** that is used to generate the sparklines (small graphs), graphs in statistics Email reports, as well as graphs in the Matomo Mobile App. The list of PHP extensions you are recommended to install are:
  `sudo apt-get install php php-curl php-gd php-cli mysql-server php-mysql php-xml php-mbstring`
- We also recommend the PHP function `shell_exec` is enabled as it is used for CLI processes.

## MySQL User Requirements

When installing Matomo, you will need to specify a MySQL username and password. The MySQL user must have permission to create and alter tables in the database.

The MySQL USER should have the permission to SELECT, INSERT, UPDATE, DELETE, CREATE, INDEX, DROP, ALTER, CREATE TEMPORARY TABLES, LOCK TABLES, FILE.

## Recommended Servers Sizing

### Tracking 100,000 page views per month or less

- One server is sufficient to host both the database and app server
- App server minimum recommended configuration: 2 CPU, 2 GB RAM, 50GB SSD disk.

### Tracking 1 million page views per month or less

- One server can be sufficient to host both the database and app server
- App server minimum recommended configuration: 4 CPU, 8 GB RAM, 250GB SSD disk.

### Tracking 10 million page views per month or less

- Two servers recommended
  - 1 x App servers, at least 8 CPUs, 16 GB RAM, 100GB SSD disk.
    - Or 2 x App servers, at least 4 CPUs, 4 GB RAM, 100GB SSD disk.
  - 1 x Database server, at least 8 CPUs, 16 GB RAM, 400GB SSD disk

### Tracking 100 million page views per month or less

- Three servers at minimum recommended:
  - 3 x App servers (or only 2x), with each: 16 CPUs, 16+ GB RAM, 100GB SSD disk.
  - 1 x Database server, at least 16 CPUs, 32 GB RAM, 1 TB SSD disk.
    - optionally 2 x DB servers: second one replicated and configured as [reader](https://matomo.org/faq/how-to-install/faq_35746/)
  - 1 x Load balancer
  - 1 x CDN recommended

### Tracking more than 100 million page views per month

You will need at least the following:

- Five servers at minimum:
  - 3 x App servers (or more), with each: 16 CPUs, 16+ GB RAM, 100GB SSD disk.
  - 2 x Database server, at least 16 CPUs, 32 GB RAM, 1 TB SSD disk.
    - replicated and configured as [reader](https://matomo.org/faq/how-to-install/faq_35746/)
  - 1 x Load balancer
  - 1 x CDN

### Installation

Find out here how we can install Matomo in our server -> [[Installation]].

## Navigation

- [Data Collection](Data%20Collection.md)
- [Features](Features.md)
- [Installation](Installation.md)
- [Pricing](Pricing.md)
- [Pros and Cons](Pros%20and%20Cons.md)
- [Reports](Reports.md)
- [Requirements and Recommendations](Requirements%20and%20Recommendations.md)
- [Self-Hosted Limitations](Self-Hosted%20Limitations.md)

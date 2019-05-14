#

```bash
## Start MariaDB
docker run -e MYSQL_ROOT_PASSWORD=admin -e MYSQL_DATABASE=drupal8 -e MYSQL_USER=drupal8 -e MYSQL_PASSWORD=drupal8 -v mariadb:/var/lib/mysql -d --name mariadb mariadb

## Install Drupal on Apache Server
docker run --name drupal8 --link mariadb:mysql -p 80:80 -d drupal:8.4-apache
```

## Inside the Drupal container

```bash
docker exec -it drupal8 bash
apt update
apt install git nano -y

# Initialize the repo
git init .
git add .
git commit -m "Initial Commit"
```

## Setup Drupal

- Navigate to http://localhost
- Setup Drupal
  - Database, User, Password: drupal8
  - Server: mysql
- Setup the site

## Add the settings files

```bash
git add .
git commit -m "Adding settings"
```

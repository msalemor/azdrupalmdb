# Drup on Azure Web App with MariaDB

Deploying Drupal to a Web App on Azure using MariaDb
Site=drupalapp2
DB=drupaldbsvr2

# Create the database
Create MariaDB
  - set File = true
  - Allow Azure services to connect

# Create the service plan
Create Linux Service Plan

# Create a web app
Create Web App

# Install drupal on the web app
Login SSH
Download https://www.drupal.org/download-latest/tar.gz
 untar tar xvzf tar.gz
cd /home/site/wwwroot
cp -r /home/Download/drupal-8.7.1/. .
ls

# create the drupal db
apt install mariadb-client -y

mysql -h drupaldbsvr.mariadb.database.azure.com -u dbadmin@drupaldbsvr -p 

create database drupal8;

# Create site
admin
Secreto123456

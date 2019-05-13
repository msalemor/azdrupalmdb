# Drup on Azure Web App with MariaDB

Deploying Drupal to a Web App on Azure using MariaDb
Site=drupalapp2
DB=drupaldbsvr2

# Create the database
Create MariaDB instance
  - After creation go to the setting and set Inno_DB_File = true
  - Allow Azure services to connect

# Create the service plan
- Create Linux or Windows Service Plan
- Set PHP to the version of Drupal (i.e. Drupal v8 requires at least PHP 7.2)

# Create a web app
- Create Web App for the service plan

# Install drupal on the web app
If on Linux:
- Login using SSH
- Execute:
```bash
cd /Home
mkdir Download && cd Download
wget https://www.drupal.org/download-latest/tar.gz
tar xvzf tar.gz
cd /home/site/wwwroot
cp -r /home/Download/drupal-8.7.1/. .
```

if on Windows:

# create the drupal database in Maria DB

- On Linux:

```bash
apt install mariadb-client -y
mysql -h drupaldbsvr.mariadb.database.azure.com -u dbadmin@drupaldbsvr -p 
create database drupal8;
exit;
```

# Create site
admin
Secreto123456

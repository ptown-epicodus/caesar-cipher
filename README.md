# Caesar Cipher

#### Independent project for Epicodus, 04.28.2017

#### By _**Patrick McGreevy**_


## Description

This website was generated with [Drupal 7.54](https://www.drupal.org/project/drupal/releases/7.54).


## Setup
1. Clone repository to **`<repo_pathname>`**
2. Set up connection to database system in MAMP (see bellow)
3. Import database from repo in phpMyAdmin (see bellow)
4. Create database admin in phpMyAdmin (see bellow)
5. Include settings.php with database access info

### Database connection
1. In MAMP > Preferences:
 - Apache Port: `8888`
 - MySQL Port: `8889`
 - Document root: **`<repo_pathname>`**
2. Click 'Start servers'

### Import database
* Visit **`localhost:8888/phpMyAdmin`** in browser
* Click 'Import' tab
 - Character set: utf-8
 - File: **`<repo_pathname>/sites/db-backup/<backup_filename>`**

### Create database admin
* Visit **`localhost:8888/phpMyAdmin`** in browser
* Click 'Privileges' tab for `cipher` database.
* Add user
 - Name: `cipher`
 - Password: `cipher`
 - Host: local
 - All privileges for `cipher` database


## Project creation
* Download latest Drupal 7.x and unzip package.
* Rename to desired **`<repo_pathname>`** and set as working directory in CLI.
* Run `$ cp sites/default/default.settings.php sites/default/settings.php`.
* Run `$ chmod -R a+w sites/default`.
* Create database (see bellow)
* Install Drupal core
 - Visit **`localhost:8888`** in browser
 - Settings:
   - Standard
   - English
   - Database:
     - Type: MySQL
     - Name: `cipher`
     - Database admin: `cipher`
     - Password: `cipher`
     - Host: `127.0.0.1`
     - Database port: `8889`
   - Site:
     - Name: 'Drupal Practice'
     - Admin: `cipher`
     - Password: `cipher`
     - Default country: United States
     - Timezone: America/Los_Angeles
* Export database for versioning (see bellow)


### Database creation
* In phpMyAdmin:
 - On 'Databases' tab
   - Create `cipher`
   - Collation: utf8_general_ci
 - On 'Privileges' tab for `cipher`:
   - Add user
   - Username: `cipher`
   - Password: `cipher`
   - Host: local
   - All privileges for `cipher` database

### Export database
* Visit **`localhost:8888/phpMyAdmin`** in browser
* Click 'Export' tab for `cipher`
* Choose 'Custom'
 - Select all tables
 - Save output to file:
  - Character set: utf-8
  - Compression: zipped
 - Format: SQL
 - Object creation: Check all except 'IF NOT EXISTS'
* Move exported zip into **`<repo_pathname>/sites/db-backup>`**, replacing contents if necessary

## Technologies Used

* MySQL
* Drupal

## Known Bugs

_No known bugs._

## Support

_Please contact patrick7490@icloud.com with questions or concerns._


### License

*MIT License*

Copyright (c) 2017 _**Patrick McGreevy**_

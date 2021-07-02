<p align="center">
<img width="275" alt="easydock" src="https://github.com/andreapollastri/easydock/blob/master/ed.png?raw=true">
</p>

# easydock ;)

Docker LEMP easy integration

![GitHub stars](https://img.shields.io/github/stars/andreapollastri/easydock?style=social)
![GitHub tag (latest by date)](https://img.shields.io/github/v/tag/andreapollastri/easydock?label=version)

## Features

Easydock comes with:

- nginx
- PHP (PHP-FPM 5.6, 7.1, 7.2, 7.3, 7.4 or 8.0)
- MySql (MySql 8)
- Redis
- MailHog
- node/npm
- GIT
- Composer
- vscode devcontainers mode support
- PHP Unit, CS Fix and PHP Stan tools (you can use them in pipelines too)

## Requirements
Docker Desktop and Composer on Mac OSx (M1 compatible)
 

## Installation
- Integrate easydock in your PHP app via Composer

```
$ cd /path/to/your-php-application
$ composer require andreapollastri/easydock
$ sh ./vendor/andreapollastri/easydock/src/.easydock export
```

## Getting started
- After installation, if you need, add these vars to your `.env` file (default values are declared yet):
```
# APPLICATION NAME (unique app-service-id)
APP_SID=easydock

# APPLICATION SOURCE PATH
APP_PATH=./

# APP PORT
APP_PORT=80

# PHP VERSION
PHP_V=8.0

# MYSQL DB NAME
DB_NAME=dockerdb

# MYSQL ROOTPASSWORD
DB_PASS=secret

# MYSQL DB PORT
DB_PORT=3306

# REDIS PORT
RDS_PORT=6379

# MAILHOG PORT
MH_PORT=8025

# NODE VERSION
NODE_V=16
```

- To use easydock in vscode devcontainer mode, run:
```
$ sh ./vendor/andreapollastri/easydock/src/.easydock devcontainer
```
Then build container via vscode.


- If you are not running Easydock into vscode devcontainer mode, use:
```
$ sh ed up
```
to start your istance

```
$ sh ed conn
```
to "SSH" into your Docker istance

```
$ sh ed down
```
to stop your istance


- Nginx config will expose your project `/public` folder

- Config your app DB connection (default)
```
user: root
pass: secret
db: dockerdb
host: mysql ( or redis for Redis )
```

- Config your app SMTP conn (default - no user or pass are required)
```
host: mailhog
port: 1025
```

- To create a Laravel .env file for Easydock, run:
```
$ sh ./vendor/andreapollastri/easydock/src/.easydock laraenv
```
Then build container via vscode.
 

- To discover all Easydock functions use:
```
$ sh ed help
```

## Security Vulnerabilities and Bugs
If you discover any security vulnerability or any bug within easydock, please open an issue.

## Contributing
Thank you for considering contributing to this project!

## Licence
Easydock is open-source software licensed under the MIT license.

 
### Enjoy easydock ;)

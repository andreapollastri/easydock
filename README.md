<p align="center">
<img width="275" alt="easydock" src="https://github.com/andreapollastri/easydock/blob/master/ed.png?raw=true">
</p>

# easydock ;)

Docker LEMP easy integration (with VScode Devcontainers Support)

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
Docker Desktop and Composer (Mac M1 compatible)
  
## Installation
- Integrate easydock in your PHP app via Composer

```
$ cd /path/to/your-php-application
$ composer require andreapollastri/easydock
$ sh ./vendor/andreapollastri/easydock/src/.easydock export
```

## Getting started
- After installation, if you need, add these vars to your `.env` file (default values are declared yet so you don't need to create an .env file if you don't need to customize follow variables):
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

- To use easydock in vscode devcontainer mode, build container via vscode

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

- Nginx by default config will expose your project `/public` folder

- You can customize all "devops" configurations with ".easydock" files (restart containers after changes)

- To discover all Easydock functions use:
```
$ sh ed help
```
 
## Default Laravel .env file for Easydock
```
APP_NAME="Easydock with Laravel ;)"
APP_ENV=local
APP_KEY=
APP_DEBUG=true
APP_URL=http://localhost

LOG_CHANNEL=stack
LOG_LEVEL=debug

DB_CONNECTION=mysql
DB_HOST=mysql
DB_PORT=3306
DB_DATABASE=dockerdb
DB_USERNAME=root
DB_PASSWORD=secret

BROADCAST_DRIVER=log
CACHE_DRIVER=file
FILESYSTEM_DRIVER=local
QUEUE_CONNECTION=database
SESSION_DRIVER=file
SESSION_LIFETIME=120

MEMCACHED_HOST=127.0.0.1

REDIS_HOST=redis
REDIS_PASSWORD=null
REDIS_PORT=6379

MAIL_MAILER=smtp
MAIL_HOST=mailhog
MAIL_PORT=1025
MAIL_USERNAME=null
MAIL_PASSWORD=null
MAIL_ENCRYPTION=null
MAIL_FROM_ADDRESS=null
MAIL_FROM_NAME="${APP_NAME}"

AWS_ACCESS_KEY_ID=
AWS_SECRET_ACCESS_KEY=
AWS_DEFAULT_REGION=us-east-1
AWS_BUCKET=
AWS_USE_PATH_STYLE_ENDPOINT=false

PUSHER_APP_ID=
PUSHER_APP_KEY=
PUSHER_APP_SECRET=
PUSHER_APP_CLUSTER=mt1

MIX_PUSHER_APP_KEY="${PUSHER_APP_KEY}"
MIX_PUSHER_APP_CLUSTER="${PUSHER_APP_CLUSTER}"
```
 
## Security Vulnerabilities and Bugs
If you discover any security vulnerability or any bug within easydock, please open an issue.

## Contributing
Thank you for considering contributing to this project!

## Licence
Easydock is open-source software licensed under the MIT license.
 
### Enjoy easydock ;)

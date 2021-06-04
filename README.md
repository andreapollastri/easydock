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
- PHP (PHP-FPM 5.x, 7.x or 8.x)
- MySql (latest version of mariadb)
- Redis
- MailHog
- node/npm
- GIT
- Composer
- vscode devcontainer mode support

## Requirements

Docker Desktop and Composer on Mac OSx (M1 compatible)
 

## Installation

- Integrate easydock in your PHP app via Composer

```
$ cd /path/to/your-php-application
$ composer require andreapollastri/easydock
$ sh ./vendor/andreapollastri/easydock/src/.easydock export
```

To use easydock in VsCode Devcontainer Mode, run:
```
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

- If you are not running Easydock into VsCode Devcontainer Mode, to start run:
```
$ sh ed up
```

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

- To "SSH" into your Docker istance:
```
$ sh ed conn
```

- To stop your Docker istance:
```
$ sh ed down
```

- You can get application info using:
```
$ sh ed info
```

- You can reset your Docker istance running:
```
$ sh ed reset
```
**NB: Database data will be removed**
 
  

## Security Vulnerabilities and Bugs

If you discover any security vulnerability or any bug within easydock, please open an issue.

## Contributing

Thank you for considering contributing to this project!

## Licence

Easydock is open-source software licensed under the MIT license.

 
### Enjoy easydock ;)

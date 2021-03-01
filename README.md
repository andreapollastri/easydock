<p align="center">
<img width="275" alt="easydock" src="https://github.com/andreapollastri/easydock/blob/master/ed.png?raw=true">
</p>

# easydock ;)

Docker LEMP easy integration (Made for Laravel)

![GitHub stars](https://img.shields.io/github/stars/andreapollastri/easydock?style=social)
![GitHub tag (latest by date)](https://img.shields.io/github/v/tag/andreapollastri/easydock?label=version)

## Features

Easydock comes with:

- nginx
- PHP (PHP-FPM 5.x, 7.x and 8.x)
- MySql (latest version of mariadb)
- Redis
- phpmyadmin
- MailHog
- node.js 14
- npm 6
- Git
- Composer
- Supervisor

## Requirements

Docker Desktop and Composer or Git on Mac OSx El Capitan or newer (M1 compatible)

## Installation

- Integrate easydock in your PHP app via Composer

```
$ cd /path/to/your-php-application
$ composer require andreapollastri/easydock
$ sh ./vendor/andreapollastri/easydock/src/.easydock export
```

- Configure your application path into `.env.docker` file

## Getting started

- After installation, if you need, configure your `.env.docker` file and run:

```
$ sh ed setup
```

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

- Nginx config will expose your project `/public` folder

- To start your Docker istance:

```
$ sh ed up
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

- Everytime you change PHP version into `.env.docker` file you have to run:

```
$ sh ed reset
$ sh ed setup
```

**NB: Database data will be removed**

## Security Vulnerabilities and Bugs

If you discover any security vulnerability or any bug within easydock, please open an issue.

## Contributing

Thank you for considering contributing to this project!

## Licence

Easydock is open-source software licensed under the MIT license.

### Enjoy easydock ;)

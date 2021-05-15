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
- PHP (PHP-FPM 8.x)
- MySql (latest version of mariadb or mysql)
- Redis
- MailHog
- node/npm
- GIT
- Composer
- xDebug

## Requirements

Docker Desktop and Composer on Mac OSx (M1 compatible if you use mariadb db image)
 

## Installation

- Integrate easydock in your PHP app via Composer

```
$ cd /path/to/your-php-application
$ composer require andreapollastri/easydock
$ sh ./vendor/andreapollastri/easydock/src/.easydock export
```

## Getting started

- After installation, if you need, configure your `.env.easydock` file and run:
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

- You can reset your Docker istance running: **NB: Database data will be removed**
```
$ sh ed reset
```

 
## xDebug configuration for vsCode

- Set xdebug mode to vscode into your env.easydock file 

- Configure vsCode within:

```
{
    "version": "0.2.0",
    "configurations": [
        {
             "name": "Listen for XDebug",
             "type": "php",
             "request": "launch",
             "port": 9000,
             "log": true,
             "externalConsole": false,
             "pathMappings": {
                 "/var/www": "${workspaceFolder}",
             },
             "ignore": [
                 "**/vendor/**/*.php"
             ]
        },
    ]
}
```

## Security Vulnerabilities and Bugs

If you discover any security vulnerability or any bug within easydock, please open an issue.

## Contributing

Thank you for considering contributing to this project!

## Licence

Easydock is open-source software licensed under the MIT license.

 
### Enjoy easydock ;)

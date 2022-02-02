# Base API backend

This is a project creted to be used as a template to acelerated building development of api rest with symfony

## How to use?

1. Crate a new repository and use this as a template

![repository as a template](./docs/img/repository-template.png)

## Installing dependencies

```bash
~$ composer install
```

## Generating ssl keys

### Development environment

```bash
~$ ./bin/console lexik:jwt:generate-keypair
```

### Testing environment

```bash
~$ openssl genrsa -out config/jwt/private-test.pem -aes256 4096
~$ openssl rsa -pubout -in config/jwt/private-test.pem -out config/jwt/public-test.pem
```

### Configure enviroment variables (dotenv file)

```bash
~$ cp .env .env.local
```

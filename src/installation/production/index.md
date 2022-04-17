# Using in production

This is not an exhaustive step-by-step guide on how you might install it into production. 

It should be fairly easy if you look a little bit to the code & config properties that you can override.


You need a valid domain, and map your server IP to these domains (CNAME A):

    <your-domain>.com
    www.<your-domain>.com
    auth.<your-domain>.com
    backoffice.<your-domain>.com
    cube.<your-domain>.com


Clone the following repo on your server:

```
git clone https://github.com/openartcoded/app-docker.git

```

Checkout the latest stable-ish release, for example:

```
git checkout v2022.1.0
```

Copy the docker-compose.override.example.yml file:

```
cp docker-compose.override.example.yml docker-compose.override.yml
```

Open `docker-compose.override.yml` with your favorite editor and changes the following properties:

| Property                             | Example                     | Description                              | 
|--------------------------------------|---------------------------- | ---------------------------------------  |
|    __MONGO_INITDB_ROOT_USERNAME__    | mongo                       | username for the mongo database          |
|    __MONGO_INITDB_ROOT_PASSWORD__    | mongo                       | password for the mongo database          |
|    __CAMEL_MAIL_IMAP_USERNAME__      | expense@your-domain.com     | Email account that will receive expenses |
|    __CAMEL_MAIL_IMAP_PASSWORD__      | secret_password             | Password of the expense email address    |
|    __MAIL_SENDER_USERNAME__          | noreply@your-domain.com     | Email account that will send email       |
|    __MAIL_SENDER_PASSWORD__          | secret_password             | Email account pwd that will send email   |
|    __ARTEMIS_PASSWORD__              | secret_password             | Artemis password                         |
|    __POSTGRES_PASSWORD__             | secret_password             | Postgres password for keycloak           |
|    __DRIVE_APPLICATION_NAME__        | yourdomain                  | Google drive application's name          |
|    __KEYCLOAK_HOSTNAME__             | auth.somehost.org           | Keycloak's hostname                      |
  
> If you're familiar with docker secrets, it is a better way of doing this


Change all network aliases with your domain:

```
  keycloak: 
    networks:
      artcoded:
        aliases:
          - auth.your-domain.com

  roundcube:
    image: roundcube/roundcubemail:latest
    networks:
      artcoded:
        aliases:
          - cube.your-domain.com
  ...

```

Modify your gateways based on `config/gateway-dev.yml`

### Google Drive

In order to send your backups into google drive, you need to create an application : `https://developers.google.com/drive`

> This is an optional feature, for now the services using it can be commented.


### Https proxy

You can use the same configuration as me, simply put your certificates at the right places and adapt the configuration accordingly:

```
git clone https://github.com/openartcoded/proxy-nginx
```

### Keycloak

You have to generate your own realm, users & roles. Go to https://auth.your-domain.com to proceed.

> You might have to uncomment :
      #KEYCLOAK_USER: __KEYCLOAK_USER__  
      #KEYCLOAK_PASSWORD: __KEYCLOAK_PASSWORD__

### Prometheus & Grafana

You might have to change the `user`in docker-composer.override.yml if it's not 1000. 

For prometheus, you probably need to create a service account & a role "ROLE_PROMETHEUS" on keycloak (see config/prometheus_dev.yml for an example of prometheus config)
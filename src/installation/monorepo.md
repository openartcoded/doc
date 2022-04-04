# Full-stack development

Clone the following repo:

```
git clone git@github.com:openartcoded/monorepo.git

```

> You need a valid SSH public key linked to your github account


If it's the first time that you clone the repo, you then need to run within the cloned folder:

`git submodule update --init --recursive --remote`

Next time you want to update all repo, run the following command: 

`git submodule update --recursive --remote`

Go to:

`cd app-docker/`

Copy the .env file:

```
cp .env.monorepo.example .env
```

> For windows users, you will need to change the content of the file with:
>
>    `COMPOSE_FILE=docker-compose.yml;docker-compose.monorepo.yml`

Build the stack:

    docker-compose build


{{#include ./common-local.md}}
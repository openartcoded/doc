# Testing, Frontend development

Clone the following repository

```bash
git clone https://github.com/openartcoded/app-docker.git
```

Go to the directory

```bash
cd app-docker
```

Copy the **.env** file

```bash
cp .env.dev.example .env
```

> For windows users, you will need to change the content of the file with:
>
> `COMPOSE_FILE=docker-compose.yml;docker-compose.dev.yml`

{{#include ./common-local.md}}

### Contribute to the frontend of the public website

Clone the following repo:

```bash
git clone https://github.com/openartcoded/website.git
```

Go to the directory

```bash
cd website
```

Run npm install

```bash
npm i
```

Run ng serve

```bash
ng serve
```

Visit [http://localhost:4200](http://localhost:4200)

### Contribute to the frontend of the backoffice

Clone the following repository

```bash
git clone https://github.com/openartcoded/backoffice.git
```

Go to the directory

```bash
cd backoffice
```

Run npm install

```bash
npm i
```

Run ng serve

```bash
ng serve
```

Visit [http://localhost:4200](http://localhost:4200)

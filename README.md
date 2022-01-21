# Laravel Docker by nklasio

## How to use

1. get started:

```bash
gh repo clone nklasio/laravel-docker
```

2. create new laravel project

```bash
laravel new src # additional parameters go here
```

3. copy env file preconfigured for this env

```bash
cp .env.example ./src/.env
```

4. start docker stack

```bash
docker compose up -d --build
```

5. access composer artisan npm etc

```bash
docker compose run --rm <normal command goes here>
# example: docker compose run --rm artisan migrate
# example: docker compose run --rm npm install
# example: docker compose run --rm composer require <package>
```

6. optional, add this to your bash profile or your zshrc

```bash
alias dcr="docker compose run --rm"
# reduces commands by a lot
# example: docker compose run --rm artisan migrate
# turns into
# dcr artisan migrate
```

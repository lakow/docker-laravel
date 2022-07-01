# Docker Laravel

Arquivos Docker para rodar o Laravel em Containers.

## Instalação
  
Copie todo o conteúdo para o diretório raiz do projeto Laravel.

Edite o arquivo **docker-compose.yml** e defina o nome do container **"<code><NOME_PROJETO></code>"** e nome da network **"<code><NOME_NETWORK></code>"**.

Edite o arquivo **docker/nginx/laravel.conf** e inclua o nome do container **"<code><NOME_CONTAINER></code>"**.

Execute o comando abaixo para criar os containers:

```bash
    docker-compose up -d
```

Em seguida acesse o container e instale as dependências

```bash
    docker-compose exec <NOME_CONTAINER> bash
    composer install
    php artisan key:generate
```

Inclua no arquivo **.gitignore** o diretório **/.docker**.

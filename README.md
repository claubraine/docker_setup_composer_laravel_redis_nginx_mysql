<div align="center">
  <a href="https://github.com/claubraine">
</div>

<div style="display: inline_block"><br>
  <img align="center" width="60" height="80" src="https://cdn.jsdelivr.net/gh/devicons/devicon/icons/docker/docker-original.svg" />
  <img align="center" width="60" height="80" src="https://cdn.jsdelivr.net/gh/devicons/devicon/icons/composer/composer-original.svg" />
  <img align="center" width="60" height="80" src="https://cdn.jsdelivr.net/gh/devicons/devicon/icons/laravel/laravel-plain-wordmark.svg" />
  <img align="center" width="60" height="80" src="https://cdn.jsdelivr.net/gh/devicons/devicon/icons/redis/redis-original-wordmark.svg" />
  <img align="center" width="60" height="80" src="https://cdn.jsdelivr.net/gh/devicons/devicon/icons/nginx/nginx-original.svg" width="100" />
  <img align="center" width="60" height="80" src="https://cdn.jsdelivr.net/gh/devicons/devicon/icons/mysql/mysql-original-wordmark.svg" />
</div>

# Docker Setup Laravel
  
* docker
* composer
* laravel
* redis
* nginx
* mysql

**Clone Repositório**

```bash
git clone https://github.com/claubraine/docker_setup_composer_laravel_redis_nginx_mysql.git

```

**Clone os Arquivos do Laravel**

```bash
git clone https://github.com/laravel/laravel.git novo_projeto
```

**Copie os arquivos docker-compose.yml, Dockerfile e o diretório docker/ para o seu projeto**

```bash
cp -r docker_setup_composer_laravel_redis_nginx_mysql/* novo_projeto/
```

**Crie o Arquivo .env**

```bash
cd example-project/
cp .env.example .env
```

**Atualizar as variáveis de ambiente do arquivo .env**

```bash
APP_NAME=NovoProjeto
APP_URL=http://localhost:8989

DB_CONNECTION=mysql
DB_HOST=mysql
DB_PORT=3306
DB_DATABASE=novo_projeto_db
DB_USERNAME=root
DB_PASSWORD=root

CACHE_DRIVER=redis
QUEUE_CONNECTION=redis
SESSION_DRIVER=redis

REDIS_HOST=redis
REDIS_PASSWORD=null
REDIS_PORT=6379
```

**Dentro da pasta do projeto, subir projeto**

```bash
docker-compose up
```

**Subir projeto em background**

```bash
docker-compose up -d
```

**Acessar o container**

```bash
docker-compose exec curso_x bash
```

**Instalar as dependências do projeto**

```bash
composer install
```

**Gerar a key do projeto Laravel**

```bash
php artisan key:generate
```

**Acessar o projeto**

```bash
http://localhost:8989
```


# Comandos Docker

**exibe todos os containers em execução no momento**
```bash
docker ps
```

**exibe todos os containers, independentemente de estarem em execução ou não**
```bash
docker ps -a
``` 

**conecta o terminal que estamos utilizando com o do container**
```bash
docker run -it NOME_DA_IMAGEM
```

**inicia o container com id em questão**
```bash
docker start ID_CONTAINER
```

**interrompe o container com id em questão**
```bash
docker stop ID_CONTAINER
```

**inicia o container com id em questão e integra os terminais, além de permitir interação entre ambos**
```bash
docker start -a -i ID_CONTAINER
```

**remove o container com id em questão**
```bash
docker rm ID_CONTAINER
```

**remove todos os containers que estão parados**
```bash
docker container prune
```

**remove a imagem passada como parâmetro**
```bash
docker rmi NOME_DA_IMAGEM
```

**ao executar, dá um nome ao container**
```bash
docker run -d -P --name NOME dockersamples/static-site
```

**define uma porta específica para ser atribuída à porta 80 do container, neste caso 12345**
```bash
docker run -d -p 12345:80 dockersamples/static-site
```

**define uma variável de ambiente AUTHOR com o valor Fulano no container criado**
```bash
docker run -d -P -e AUTHOR="Fulano" dockersamples/static-site
```




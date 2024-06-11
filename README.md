<div style="display: flex; align-items: center;">
  <img src="https://github.com/abraao69/Curso-Laravel-9-/blob/main/logo.png" alt="Logo" width="200" height="100">
  <br><br>
</div>



# Setup Docker Para Projetos Laravel 9 com PHP 8

<hr>
<p align="center">
 <img width="900px" src="https://user-images.githubusercontent.com/103331086/219259196-d2ad5b57-b7e1-4a74-bf43-6068559d5350.PNG" />
</p>



### Passo a passo
Clone Repositório
```sh
git clone https://github.com/abraao69/curso-laravel-9-.git
```

```sh
cd laravel9/
```


Alterne para a branch laravel 8.x
```sh
git checkout laravel-9-com-php-8
```


Remova o versionamento
```sh
rm -rf .git/
```


Crie o Arquivo .env
```sh
cd example-project/
cp .env.example .env
```


Atualize as variáveis de ambiente do arquivo .env
```dosini
APP_NAME=EspecializaTi
APP_URL=http://localhost:8180

DB_CONNECTION=mysql
DB_HOST=mysql
DB_PORT=3306
DB_DATABASE=nome_que_desejar_db
DB_USERNAME=root
DB_PASSWORD=root

CACHE_DRIVER=redis
QUEUE_CONNECTION=redis
SESSION_DRIVER=redis

REDIS_HOST=redis
REDIS_PASSWORD=null
REDIS_PORT=6379
```


Suba os containers do projeto
```sh
docker-compose up -d
```


Acessar o container
```sh
docker-compose exec app bash
```


Instalar as dependências do projeto
```sh
composer install
```


Gerar a key do projeto Laravel
```sh
php artisan key:generate
```


Acesse o projeto
[http://localhost:8989](http://localhost:8989)

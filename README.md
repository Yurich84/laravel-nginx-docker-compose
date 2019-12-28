# Laravel Environment with Docker-Compose

#### Nginx 
#### PHP 7.4
#### MariaDB 
#### Redis 
#### Laravel-Echo-Server
#### Laravel Queue
#### Cron

## Install
- `git clone https://github.com/Yurich84/laravel-nginx-docker-compose.git`
- `docker-compose up --build`
- `mkdir ../project`
- Setup your Laravel application in folder 'project'
- Laravel .env

```
APP_URL=http://127.0.0.1:8000

DB_CONNECTION=mysql
DB_HOST=mysql
DB_PORT=3306
DB_DATABASE=default
DB_USERNAME=user
DB_PASSWORD=secret

BROADCAST_DRIVER=redis
QUEUE_CONNECTION=database

REDIS_HOST=redis
```


- Go to http://127.0.0.1:8000
- Enjoy!

## Using
- You can change laravel folder and other configs (see .env)
- Databases will store in `db` folder


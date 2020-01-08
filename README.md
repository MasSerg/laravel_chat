# INSTALL...

create database & edit .env

```bash
composer create-project --prefer-dist laravel/laravel chat "5.7.*"
php artisan make:auth
php artisan migrate
```

Redis

```bash
sudo apt install redis-server
composer require predis/predis
```

Edit .env

```bash
BROADCAST_DRIVER=redis
CACHE_DRIVER=file
QUEUE_CONNECTION=sync
SESSION_DRIVER=file
SESSION_LIFETIME=120

REDIS_HOST=127.0.0.1
REDIS_PASSWORD=null
REDIS_PORT=6379
```
Edit /config/app.php

```bash
App\Providers\BroadcastServiceProvider::class,
```

Clear config cache

```bash
php artisan config:cache
```

Laravel-echo-server

```bash
sudo npm install -g laravel-echo-server
laravel-echo-server init
laravel-echo-server start
```

Libs & watch

```bash
npm install
npm install --save laravel-echo
npm install --save socket.io-client
npm run watch-poll
```

Queue

```bash
php artisan queue:work
```

Start server

```bash
php artisan serve
```

Open url in two browsers: [http://localhost:8000](http://localhost:8000)

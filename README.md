# Docker LEMP (Linux, NGINX, MySQL, PHP)

## Налаштування

### Створення локального сайту

1. У теці `www/html` додаємо наші скрипти
2. У теці `images/nginx` розміщено конфіг для нашого сайту
3. Логін для бази даних _root_. Пароль: _root_. Змінити пароль можна у файлі `docker-compose.yml` в налаштуваннях `MYSQL_ROOT_PASSWORD`
4. Запускаємо сайт, набравши в браузері `localhost`
5. phpmyadmin запускаємо через `localhost:8099`
6. mailhog запускаємо через `localhost:8025` для перегляду листів, а `localhost:1025` для відправки через SMTP. Більш детальніше читайте тут: https://github.com/mailhog/MailHog

### Запуск Docker-контейнера

1. Запускаємо команду (збірка без використання кешу)
```
docker-compose build --no-cache
```
2. Далі запускаємо сам контейнер
```
docker-compose up -d
```

## Перебудова Docker-контейнера

1. Зупинка Docker контейнера (видалення контейнерів)
```
docker-compose down
```
2. Видалення даних Docker
```
docker system prune -a
docker image prune
docker volume prune
```
5. Rebuild without using cache
```
docker-compose build --no-cache
```
6. Start Container
```
docker-compose up -d
```

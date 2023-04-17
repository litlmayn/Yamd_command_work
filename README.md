![Yamdb Workflow Status](https://github.com/litlmayn/yamdb_final/actions/workflows/main.yml/badge.svg?branch=master&event=push)
### Проект Yamdb - это проект, направленный на оценку любых произведений!

```
С помощью данной плотформы люди могут обмениваться отзывами о произведениях, комментировать отзывы других участников.
```

### Мы использовали данный стек технологий для проектирования проекта:
```
Django
DRF
Python
```

### Ссылка на документацию:
```
 http://localhost/redoc/
```

### Задачи были распределены данным образом:
```
Настасья Мартынова:
  Писала всю часть, касающуюся управления пользователями:  
    - систему регистрации и аутентификации,
    - права доступа,
    - работу с токеном,
    - систему подтверждения через e-mail.
  
Роман Романцов:
  Писал модели, view и эндпойнты для:
    - произведений,
    - категорий,
    - жанров;
    - реализовал импорт данных из csv файлов.
 
Вадим крамаренко:
  Работал над:
    - отзывами,
    - комментариями,
    - рейтингом произведений.
```

### Как запустить проект в dev режиме:

Клонировать репозиторий и перейти в него в командной строке:

```
git clone git@github.com:litlmayn/api_yamdb.git
```

```
cd infra
```

Запустить docker-compose:

```
docker-compose up
```

Выполните по очереди команды:

```
docker-compose exec web python manage.py migrate
docker-compose exec web python manage.py collectstatic --no-input
docker-compose exec web python manage.py loaddata
```

### Пример env-файла:

```
SECRET_KEY = 'key'
DB_ENGINE=django.db.backends.postgresql # указываем, что работаем с postgresql
DB_NAME=postgres # имя базы данных
POSTGRES_USER=user # логин для подключения к базе данных
POSTGRES_PASSWORD=Porol1234 # пароль для подключения к БД (установите свой)
DB_HOST=db # название сервиса (контейнера)
DB_PORT=5432 # порт для подключения к БД
```

# ContactBook
Это приложение для сохранения контактов ваших родственников, друзей и других знакомых через XML файл и базу данных. <br>
Подходит для хранения загружаемых вами xml файлов, так и для внесения записей в один файл или в базу данных

#Внимание! Данное приложение работает через Docker. Внимательно прочтите инструкцию!

## Установка и запуск

1. Скачайте .zip файл и распакуйте в удобной для вас папке:

2. Создайте файл .env:
```bash
POSTGRES_DB=contacts_db
POSTGRES_USER=contacts_user
POSTGRES_PASSWORD=657lol657
SECRET_KEY='django-insecure-pmxtv*wfm#-7^k6@3wgtqoigo7)+x56$^$sn^*uury&5y&pld*'
DEBUG=True
ALLOWED_HOSTS=localhost,127.0.0.1
```
3. Запустите приложение:
```bash
docker-compose up --build
```
4. Выполните миграции (в новом терминале):

```bash
docker-compose exec web python manage.py migrate
docker-compose exec web python manage.py createsuperuser
```
5. Откройте в браузере: http://localhost:8000

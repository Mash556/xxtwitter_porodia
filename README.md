
# Xwitter - пародия на Twitter(X)



---

### Что мы использовали:


![Python](https://img.shields.io/badge/python-%233776AB.svg?style=for-the-badge&logo=python&logoColor=white)
![Docker](https://img.shields.io/badge/docker-%232496ED.svg?style=for-the-badge&logo=docker&logoColor=white)
![React](https://img.shields.io/badge/react-%2361DAFB.svg?style=for-the-badge&logo=react&logoColor=white)
![Django](https://img.shields.io/badge/django-%23092E20.svg?style=for-the-badge&logo=django&logoColor=white)
![PostgreSQL](https://img.shields.io/badge/postgresql-%23316192.svg?style=for-the-badge&logo=postgresql&logoColor=white)
![Celery](https://img.shields.io/badge/celery-%234EA94B.svg?style=for-the-badge&logo=celery&logoColor=white)
![Gunicorn](https://img.shields.io/badge/gunicorn-%23566595.svg?style=for-the-badge&logo=gunicorn&logoColor=white)
![NGINX](https://img.shields.io/badge/nginx-%236946BE.svg?style=for-the-badge&logo=nginx&logoColor=white)
![Telegram Bot](https://img.shields.io/badge/telegram-%232CA5E0.svg?style=for-the-badge&logo=telegram&logoColor=white)
![JWT Token](https://img.shields.io/badge/jwt%20token-%233776AB.svg?style=for-the-badge&logo=jwt&logoColor=white)
![Jazzmin](https://img.shields.io/badge/jazzmin-%232496ED.svg?style=for-the-badge&logo=djangoproject&logoColor=white)

---

К проету подключена автоматическая документация Swagger:
```python
http://158.160.9.246/api/swagger
```

Клонируем репозиторий:
```python
git@github.com:hellakiddo/last_hackaton_py31.git
```
Заходим в рабочую директорию 
```python
cd infra/
```
### Заполняем файл .env вашими данными
```python
SECRET_KEY=<КЛЮЧ ПРОЕКТА>
DB_ENGINE=django.db.backends.postgresql
DB_NAME=<ИМЯ БАЗЫ ДАННЫХ>
POSTGRES_USER=<ИМЯ ПОЛЬЗОВАТЕЛЯ БД>
POSTGRES_PASSWORD=<ПАРОЛЬ>
DB_HOST=db
DB_PORT=5432
```
Далее поднимаем проект в режиме демона, делаем миграции и собираем статику:
```python
docker-compose up -d
docker-compose exec <имя_контейнера_бэкэнда> python3 manage.py makemigrations
docker-compose exec <имя_контейнера_бэкэнда> python3 manage.py migrate
docker-compose exec <имя_контейнера_бэкэнда> python3 manage.py collectstatic --noinput
```
Создаем администратора командой:
```python
docker-compose exec <имя_контейнера_бэкэнда> python manage.py createsuperuser
```
Проект доступен по адресу:
```python
http://158.160.9.246
```
---

### ***Авторы***

---



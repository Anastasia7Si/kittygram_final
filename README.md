# Kittygram

### Описание
Проект о домашних питомцах, в котором можно зарегистрироваться и добавлять питомцев, необходимо указать имя и год рождения питомца, а так же добавить фотографию и указать его умения. 

Технологии:
- Python
- Django
- Django REST Framework
- Simple JWT
- Gunicorn 20.1.0 
- Фронтенд-приложение на React 
- npm 9.5.1 
- Docker
- DockerHub
- CI/CD
- GitHub Actions
- PostgreSQL
- Docker network

### Запуск проекта
Клонировать репозиторий и перейти в него в командной строке:
```
git clone https://github.com/Anastasia7Si/kittygram_final
cd kittygram_final
```
В корне проекта создать файл .env и прописать в него свои данные.
Пример:
```
POSTGRES_DB=kittygram
POSTGRES_USER=kittygram_user
POSTGRES_PASSWORD=kittygram_password
```
Запустить проект через docker-compose:
```
docker compose -f docker-compose.yml up
```
Выполнить миграции:
```
docker compose -f docker-compose.yml exec backend python manage.py migrate
```
Создать суперюзера:
```
sudo docker compose -f docker-compose.yml exec backend python manage.py createsuperuser
```
Собрать статику и скопировать ее:
```
docker compose -f docker-compose.yml exec backend python manage.py collectstatic
docker compose -f docker-compose.yml exec backend cp -r /app/static_backend/. /backend_static/static/
```
### Автор
```
- Пушкарная Анастасия
````
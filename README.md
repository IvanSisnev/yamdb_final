## **yamdb_final**

### **Краткое описание проекта**
___
**API соцсети, в которой пользователи могут писать отзывы на 
произведения (книги, фильмы, музыку) и комментировать отзывы друг друга.**
<br><br>

> Документация API доступна в формате redoc на эндпоинте `/redoc`

### **Проект доступен по адресу: 51.250.67.145**

### **Запуск проекта**
___

#### **Клонировать репозиторий:**

    git clone <ccылка>

#### **В директории `infra/` создать файл `.env` и добавить в него следующие переменные:

    DB_ENGINE=django.db.backends.postgresql
    DB_NAME= # название базы данных
    POSTGRES_USER= # логин для подключения к базе данных
    POSTGRES_PASSWORD= # пароль для подключения к БД
    DB_HOST=db
    DB_PORT=5432
    SECRET_KEY= # секретный ключ

#### **Пересобрать контейнеры из директории `infra/`:**

    docker-compose up -d --build

#### **Выполнить миграции:**

    docker-compose exec web python manage.py migrate

#### **Создать суперюзера:**

    docker-compose exec web python manage.py createsuperuser

#### **Собрать статику:**

    docker-compose exec web python manage.py collectstatic --no-input

### ** Бэйдж workflow проекта**

![Workflow_badge](https://github.com/IvanSisnev/yamdb_final/actions/workflows/yamdb_workflow.yaml/badge.svg)
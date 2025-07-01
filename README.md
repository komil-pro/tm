# Task Management project on Laravel

## Описание проекта

> RESTful API для простой системы управления задачами, позволяющей пользователям регистрироваться, аутентифицироваться и управлять своими задачами.

## Установка
1. Клонируем репозиторий: `git clone <repo-url>`
2. Установка зависимостей: `composer install`
3. Копируем конфиг `.env.example` to `.env` прописываем настройки подключение к базе данных (в данном случае MySQL).
4. Запускаем миграции: `php artisan migrate`
5. Запускаем сервер: `php artisan serve`

## API Endpoints (эндпоинты)
- `POST /api/register`: регистрация нового пользователя.
- `POST /api/login`: логин пользователя, при этом получаем токен.
- `POST /api/logout`: логаут пользователя (requires token).
- `GET /api/tasks`: список пользовательских задач.
- `POST /api/tasks`: создание новой задачи.
- `GET /api/tasks/{id}`: получение информации по определенной задаче.
- `POST /api/tasks/{id}`: обновление задачи.
- `DELETE /api/tasks/{id}`: удаление задачи.

## Authentication
Для аутентификации используется `Authorization: Bearer <token>` заголовок для authenticated requests.

## Postman коллекция для тестирования работы с API
Файл `TM-API.postman_collection.json` с примерами эндпоинтов для работы с API.
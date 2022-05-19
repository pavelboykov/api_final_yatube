## Проект «API для YaTube»

### Описание API:

Учебный проект Yatube представляет собой прототип социальной сети для публикации личных дневников с возможностью создания личной страницы, функционалом осуществления подписки на интересующих авторов и комментирования их записей.

API для проекта Yatube реализован на Django Rest Framework и позволяет осуществлять весь его базовый функционал. Аутентификация осуществляется по JWT-токену.

### Как запустить проект:
* Клонировать репозиторий и перейти в него в командной строке: 
  ```
  git clone https://github.com/pavelboykov/api_final_yatube.git
  cd yatube_api
  ```
* Cоздать и активировать виртуальное окружение:
  * Windows
     ```
     python -m venv env
     source venv/Scripts/activate
     ```
  * Linux
    ```
    python3 -m venv venv
    source venv/bin/activate
    ```
* Установить зависимости из файла requirements.txt:
  * Windows
    ```
    python -m pip install --upgrade pip
    pip install -r requirements.txt
    ```
  * Linux
    ```
    python3 -m pip install --upgrade pip
    pip install -r requirements.txt
    ```
* Выполнить миграции:
  * Windows: 
    ```
    python manage.py migrate
    ```
  * Linux: 
    ```
    python3 manage.py migrate
    ```
* Запустить проект:
  * Windows: 
    ```
    python manage.py runserver
    ```
  * Linux: 
    ```
    python3 manage.py runserver
    ```

### Документация:
После запуска проекта на dev-сервере документация в формате redoc доступна по адресу: 
```
http://127.0.0.1:8000/redoc/
```
#### Доступный функционал:
* Получение и создание публикаций: 
  ```
  http://127.0.0.1:8000/api/v1/posts/
  ```
* Получение, обновление, частичное обновление и удаление публикации по id: 
  ```
  http://127.0.0.1:8000/api/v1/posts/{id}/
  ```
* Получение и добавление нового комментария: 
  ```
  http://127.0.0.1:8000/api/v1/posts/{post_id}/comments/
  ```
* Получение, обновление, частичное обновление и удаление комментария к публикации по id: 
  ```
  http://127.0.0.1:8000/api/v1/posts/{post_id}/comments/{id}/
  ```
* Получение списка доступных сообществ: 
  ```
  http://127.0.0.1:8000/api/v1/groups/
  ```
* Получение информации о сообществе по id:
  ```
  http://127.0.0.1:8000/api/v1/groups/{id}/
  ```
* Получение всех подписок пользователя, сделавшего запрос, а также подписка на пользователя переданного в теле запроса:
  ```
  http://127.0.0.1:8000/api/v1/follow/
  ```
* Создание пользователя:
  ```
  http://127.0.0.1:8000/api/v1/users/
  ```
* Получение JWT-токена:
  ```
  http://127.0.0.1:8000/api/v1/jwt/create/
  ```
* Обновление JWT-токена:
  ```
  http://127.0.0.1:8000/api/v1/jwt/refresh/
  ```
* Проверка JWT-токена: 
  ```
  http://127.0.0.1:8000/api/v1/jwt/verify/
  ```

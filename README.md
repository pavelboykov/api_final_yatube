## Проект «API для YaTube»
___
### Описание API:
После запуска проекта на локальном сервере документация доступна по адресу:  
```
http://127.0.0.1:8000/redoc/
```
---
### Как запустить проект:

Клонировать репозиторий и перейти в него в командной строке:
```
git clone https://github.com/pavelboykov/api_final_yatube.git
```

```
cd yatube_api
```

Cоздать и активировать виртуальное окружение:

`Windows`
```
python -m venv env
source venv/Scripts/activate
```
`Linux`
```
python3 -m venv venv
source venv/bin/activate
```

Установить зависимости из файла requirements.txt:

`Windows`
```
python -m pip install --upgrade pip
pip install -r requirements.txt
```
`Linux`
```
python3 -m pip install --upgrade pip
pip install -r requirements.txt
```

Выполнить миграции:

```
python manage.py migrate
```

Запустить проект:

```
python manage.py runserver
```

### Доступный функционал:

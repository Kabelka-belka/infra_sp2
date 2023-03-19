## Как запустить проект:

### Клонировать репозиторий и перейти в него в командной строке:

https://github.com/Gidrazin/api_yamdb.git
```
cd api_yamdb
```
### Cоздать и активировать виртуальное окружение:
```
python3 -m venv venv

source venv/bin/activate
```
### Установить зависимости из файла requirements.txt:
```
python3 -m pip install --upgrade pip

pip install -r requirements.txt
```
### Выполнить миграции:
```
python3 manage.py migrate
```
### Запустить проект```
python3 manage.py runserver
```
## Импорт данных

### Для загрузки данных в бд:

Подготовить файл с данными формата ```.csv```

### Выполнить импорт командой:
```
python3 api_yamdb/manage.py load_base
```

## Cпецификация API

### Cпецификация API доступна по адресу:

http://127.0.0.1:8000/redoc/

## Примеры запросов к API
_request sample:_
GET http://127.0.0.1:8000/api/v1/titles/

_response sample:_
```
application/json
[
  {
    "count": 0,
    "next": "string",
    "previous": "string",
    "results": [
      {
        "id": 0,
        "name": "string",
        "year": 0,
        "rating": 0,
        "description": "string",
        "genre": [
          {
            "name": "string",
            "slug": "string"
          }
        ],
        "category": {
          "name": "string",
          "slug": "string"
        }
      }
    ]
  }
]
```
POST http://127.0.0.1/api/v1/titles/
http://127.0.0.1/redoc/
## Тестовая задача с минимальным API на DRF


### Описание 
Есть один endpoint - `/tasks/`, для которого доступны две операции:


`GET /tasks/` - Выдает список всех доступных обектов.

`POST /tasks/` - Создает новый объект на основе переданного JSON.

### Пример

Проверить можно при помощи комманд(при условии, что сервер запущен на localhost):

Для создания объекта:
```
curl -X POST -H "Content-Type: application/json" -d '{"title": "New Task", "is_completed": false}' http://127.0.0.1:8000/tasks/
```

Для проверки валидации:
```
curl -X POST -H "Content-Type: application/json" -d '{"title": "", "is_completed": false}' http://127.0.0.1:8000/tasks/
```

Для получения списка:
```
curl -X GET http://127.0.0.1:8000/tasks/
```

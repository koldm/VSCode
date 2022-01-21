### [REST Client](https://marketplace.visualstudio.com/items?itemName=humao.rest-client) позволяет отправлять HTTP-запросы и просматривать ответ непосредственно в коде Visual Studio.

Как [Postman](https://www.postman.com/), но только внутки редактора.

## Описание

* В проекте (в корне, в компоненте, вот вообще не важно где именно) создать файл requests.http;
* И это все!

### Пример файла requests.http
```
### Получить список сообщений
GET http://localhost:3000/messages

### Создать новое сообщение
POST http://localhost:3000/messages
Content-Type: application/json

{
  "content": "new message"
}

### Обновить сообщение
PATCH http://localhost:3000/messages
Content-Type: application/json

{
  "content": "new message update"
}
```

**Внимание!** Между заголовком и данными в POST/PATCH запросе нужна одна пустая строка
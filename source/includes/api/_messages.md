# Messages

## Get messages

> Example request:

```javascript
fetch('http://localhost:3000/chats/1/messages', {
  headers: {
    Accept: 'application/json',!
    'Content-Type': 'application/json',
    'x-access-token': authToken,
  },
})
```

> Example response:

```json
[
  {
    "id": 1,
    "chatId": 1,
    "userId": 1,
    "text": "Some text",
    "created": 123456789
  },
  {
    "id": 2,
    "chatId": 1,
    "userId": 2,
    "text": "Some text",
    "created": 123456790
  }
]
```

This endpoint retrieves messages for specified chat.

### HTTP Request

`GET http://localhost:3000/api/chats/:chatId/messages`


## Create message

> Example request:

```javascript
fetch('http://localhost:3000/chats/1/messages', {
  method: 'POST',
  body: {
    text: "Some text",
  },
  headers: {
    Accept: 'application/json',!
    'Content-Type': 'application/json',
    'x-access-token': authToken,
  },
})
```

> Example response:

```json
{
  "id": 1,
  "chatId": 1,
  "userId": 1,
  "text": "Some text",
  "created": 123456789
}
```

This endpoint creates messages for specified chat.

### HTTP Request

`POST http://localhost:3000/api/chats/:chatId/messages`

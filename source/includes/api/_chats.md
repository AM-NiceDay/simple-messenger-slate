# Chats

## Get chats

> Example request:

```javascript
fetch('http://localhost:3000/api/chats', {
  headers: {
    Accept: 'application/json',!
    'Content-Type': 'application/json',
    'x-access-token': authToken,
  },
});
```

> Example response:

```json
[
  {
    "id": 1,
    "userIds": [1, 2],
    "lastMessageId": 1,
    "lastMessageCreated": 123456789
  },
  {
    "id": 2,
    "userIds": [1, 3],
    "lastMessageId": 2,
    "lastMessageCreated": 123456789
  }
]
```

This endpoint retrieves user's chats.

### HTTP request

`GET http://localhost:3000/api/chats`

## Create chat

> Example request:

```javascript
fetch('http:/localhost:3000/api/chats', {
  method: 'POST',
  body: {
    peerId: 2,
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
  "userIds": [1, 2],
  "lastMessageId": 1,
  "lastMessageCreated": 123456789
}
```

### HTTP request

`POST http://localhost:3000/api/chats`

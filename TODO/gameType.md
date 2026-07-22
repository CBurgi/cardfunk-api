# POST createGameType

## URI
/gameTypes/create
/gameTypes

## Request
**Headers**
- Content-Type: application/json
- Accept: application/json

**Body**
```
{
  name: string | null,
  data: {} | null
}
```

## Response
201 Created 

**Headers**
- Content-Type: application/json

**Body**
```
{
  id: string,
  name: string,
  board_ids: [string],
  card_type_ids: [string],
  token_type_ids: [string],
  data: {}
}
```

# GET getGameTypes

may want to do some pagination for this and/or just return name and id if too long

## URI
/gameTypes/get
/gameTypes

**Headers**
- Accept: application/json

## Response
200 OK 

**Headers**
- Content-Type: application/json

**Body**
```
[
  {
    id: string,
    name: string,
    board_ids: [string],
    card_type_ids: [string],
    token_type_ids: [string],
    data: {}
  }, ...
]
```

# GET getGameType

## URI
/gameTypes/{game_type_id}/get
/gameTypes/{game_type_id}

**Headers**
- Accept: application/json

## Response
200 OK 

**Headers**
- Content-Type: application/json

**Body**
```
{
  id: string,
  name: string,
  board_ids: [string],
  card_type_ids: [string],
  token_type_ids: [string],
  data: {}
}
```

# PUT updateGameType

## URI
/gameTypes/{game_type_id}/update
/gameTypes/{game_type_id}

## Request
**Headers**
- Content-Type: application/json
- Accept: application/json

**Body**
```
{
  name: string | null,
  board_ids: [string] | null,
  card_type_ids [string] | null,
  token_type_ids [string] | null,
  data: {} | null
}
```

## Response
200 OK 

**Headers**
- Content-Type: application/json

**Body**
```
{
  id: string,
  name: string,
  board_ids: [string],
  card_type_ids: [string],
  token_type_ids: [string],
  data: {}
}
```

# PUT addItem

- If not empty, will replace value
- If array, will append
- If type is not specified, will assume

## URI
/gameTypes/{game_type_id}/addItem
/gameTypes/{game_type_id}/add

## Request
**Headers**
- Content-Type: application/json
- Accept: application/json

**Body**
```
{
  name: string,
  type: string | null,
  value: any | null
}
```

## Response
200 OK 

**Headers**
- Content-Type: application/json

**Body**
```
{
  id: string,
  name: string,
  board_ids: [string],
  card_type_ids: [string],
  token_type_ids: [string],
  data: {}
}
```

# PUT addItems

- If not empty, will replace value
- If array, will append
- If type is not specified, will assume

## URI
/gameTypes/{game_type_id}/addItems

## Request
**Headers**
- Content-Type: application/json
- Accept: application/json

**Body**
```
[
  {
    name: string,
    type: string | null,
    value: any | null
  },
  ...
]
```

## Response
200 OK 

**Headers**
- Content-Type: application/json

**Body**
```
{
  id: string,
  name: string,
  board_ids: [string],
  card_type_ids: [string],
  token_type_ids: [string],
  data: {}
}
```

# PUT removeItem

## URI
/gameTypes/{game_type_id}/removeItem
/gameTypes/{game_type_id}/remove

## Request
**Headers**
- Content-Type: application/json
- Accept: application/json

**Body**
```
{
  name: string
}
```

## Response
200 OK 

**Headers**
- Content-Type: application/json

**Body**
```
{
  id: string,
  name: string,
  board_ids: [string],
  card_type_ids: [string],
  token_type_ids: [string],
  data: {}
}
```

# PUT removeItems

## URI
/gameTypes/{game_type_id}/removeItems

## Request
**Headers**
- Content-Type: application/json
- Accept: application/json

**Body**
```
[
  {
    name: string
  },
  ...
]
```

## Response
200 OK 

**Headers**
- Content-Type: application/json

**Body**
```
{
  id: string,
  name: string,
  board_ids: [string],
  card_type_ids: [string],
  token_type_ids: [string],
  data: {}
}
```

# PUT setValue

- Will return error if not correct type

## URI
/gameTypes/{game_type_id}/setValue
/gameTypes/{game_type_id}/set

## Request
**Headers**
- Content-Type: application/json
- Accept: application/json

**Body**
```
{
  name: string,
  value: any
}
```

## Response
200 OK 

**Headers**
- Content-Type: application/json

**Body**
```
{
  id: string,
  name: string,
  board_ids: [string],
  card_type_ids: [string],
  token_type_ids: [string],
  data: {}
}
```

# PUT setValues

- Will only set values that are the correct types

## URI
/gameTypes/{game_type_id}/setValues

## Request
**Headers**
- Content-Type: application/json
- Accept: application/json

**Body**
```
[
  {
    name: string,
    value: any
  },
  ...
]
```

## Response
200 OK 

**Headers**
- Content-Type: application/json

**Body**
```
{
  id: string,
  name: string,
  board_ids: [string],
  card_type_ids: [string],
  token_type_ids: [string],
  data: {}
}
```

# PUT clearValue

## URI
/gameTypes/{game_type_id}/clearValue
/gameTypes/{game_type_id}/clear

## Request
**Headers**
- Content-Type: application/json
- Accept: application/json

**Body**
```
{
  name: string
}
```

## Response
200 OK 

**Headers**
- Content-Type: application/json

**Body**
```
{
  id: string,
  name: string,
  board_ids: [string],
  card_type_ids: [string],
  token_type_ids: [string],
  data: {}
}
```

# PUT clearValues

## URI
/gameTypes/{game_type_id}/clearValues

## Request
**Headers**
- Content-Type: application/json
- Accept: application/json

**Body**
```
[
  {
    name: string
  },
  ...
]
```

## Response
200 OK 

**Headers**
- Content-Type: application/json

**Body**
```
{
  id: string,
  name: string,
  board_ids: [string],
  card_type_ids: [string],
  token_type_ids: [string],
  data: {}
}
```

# DELETE deleteGameType

## URI
/gameTypes/{game_type_id}/delete
/gameTypes/{game_type_id}

## Response
204 No Content

# POST createGameType

## URI
/gameTypes/create

## Request
**Headers**
- Content-Type: application/json
- Accept: application/json

**Body**
```
{
  game_type_name: string | null,
  game_type_data:
  {
    board_type_ids: [string] | null
  } | null
}
```

## Response
201 Created 

**Headers**
- Content-Type: application/json

**Body**
```
{
  game_type_id: string,
  game_type_name: string,
  game_type_data:
  {
    board_type_ids: [string]
  }
}
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
  game_type_id: string,
  game_type_name: string,
  game_type_data:
  {
    board_type_ids: [string]
  }
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
  game_type_name: string | null,
  game_type_data:
  {
    board_type_ids: [string] | null  
  } | null
}
```

## Response
200 OK 

**Headers**
- Content-Type: application/json

**Body**
```
{
  game_type_id: string,
  game_type_name: string,
  game_type_data: {
    board_type_ids: [string]
  }
}
```

# PUT addBoard

## URI
gameTypes/{game_type_id}/addBoard

## Request
**Headers**
- Content-Type: application/json
- Accept: application/json

**Body**
```
{
  board_type_id: string
}
```

## Response
200 OK 

**Headers**
- Content-Type: application/json

**Body**
```
{
  game_type_id: string,
  game_type_name: string,
  game_type_data: {
    board_type_ids: [string]
  }
}
```

# PUT addBoards

## URI
gameTypes/{game_type_id}/addBoards

## Request
**Headers**
- Content-Type: application/json
- Accept: application/json

**Body**
```
{
  board_type_ids: [string]
}
```

## Response
200 OK 

**Headers**
- Content-Type: application/json

**Body**
```
{
  game_type_id: string,
  game_type_name: string,
  game_type_data: {
    board_type_ids: [string]
  }
}
```

# PUT removeBoard

## URI
gameTypes/{game_type_id}/removeBoard

## Request
**Headers**
- Content-Type: application/json
- Accept: application/json

**Body**
```
{
  board_type_id: string
}
```

## Response
200 OK 

**Headers**
- Content-Type: application/json

**Body**
```
{
  game_type_id: string,
  game_type_name: string,
  game_type_data: {
    board_type_ids: [string]
  }
}
```

# PUT removeBoards

## URI
gameTypes/{game_type_id}/removeBoards

## Request
**Headers**
- Content-Type: application/json
- Accept: application/json

**Body**
```
{
  board_type_ids: [string]
}
```

## Response
200 OK 

**Headers**
- Content-Type: application/json

**Body**
```
{
  game_type_id: string,
  game_type_name: string,
  game_type_data: {
    board_type_ids: [string]
  }
}
```

# DELETE deleteGameType

## URI
gameTypes/{game_type_id}/delete
gameTypes/{game_type_id}

## Response
204 No Content

# POST createGameType

## URI
/createGameType

## Request
**Headers**
- Content-Type: application/json
- Accept: application/json

**Body**
```
{
  game_type_name: string,
  game_type_data:
  {
    board_type_id: [string] | null,  
    card_type_ids: [string] | null,
    counter_type_ids: [string] | null,  
    table_type_ids: [string] | null,
  } | null,
}
```

## Response
201 Created 

**Headers**
- Content-Type: application/json

**Body**
```
{
  game_type_name: string,
  game_type_id: string,
  game_type_data: {
    board_type_id: string,
    card_type_ids: [string],
    counter_type_ids: [string],
    table_type_ids: [string],
  }
}
```

# GET getGameType
## URI
/{game_type_id}/getGameType

**Headers**
- Accept: application/json

## Response
200 OK 

**Headers**
- Content-Type: application/json

**Body**
```
{
  game_type_name: string,
  game_type_id: string,
  board_type_id: string,
  card_type_ids: [string],
  counter_type_ids: [string],
  table_type_ids: [string],
}
```

# PUT updateGameType
## URI
/{game_type_id}/createGameType

## Request
**Headers**
- Content-Type: application/json
- Accept: application/json

**Body**
```
{
  game_type_name: string,
  game_type_data:
  {
    board_type_id: [string] | null,  
    card_type_ids: [string] | null,
    counter_type_ids: [string] | null,  
    table_type_ids: [string] | null,
  } | null,
}
```

## Response
201 Created 

**Headers**
- Content-Type: application/json

**Body**
```
{
  game_type_name: string,
  game_type_id: string,
  game_type_data: {
    board_type_id: string,
    card_type_ids: [string],
    counter_type_ids: [string],
    table_type_ids: [string],
  }
}
```

# DELETE deleteGameType
## URI
/{game_type_id}/deleteGameType

## Request

## Response
204 No Content

**Body**
```
{
  name: string,
  game_id: string,
}
```


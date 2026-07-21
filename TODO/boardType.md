# POST createBoardType

## URI
/boardTypes/create

## Request
**Headers**
- Content-Type: application/json
- Accept: application/json

**Body**
```
{
  board_type_name: string | null,
  deck_type_ids: [string] | null,
  space_type_ids: [string] | null,
  hand_type_ids: [string] | null,
  board_type_data: {} | null
}
```

## Response
201 Created 

**Headers**
- Content-Type: application/json

**Body**
```
{
  board_type_id: string,
  board_type_name: string,
  deck_type_ids: [string],
  space_type_ids: [string],
  hand_type_ids: [string]
  board_type_data: {}
}
```

# GET getBoardType

## URI
/boardTypes/{board_type_id}/get
/boardTypes/{board_type_id}

**Headers**
- Accept: application/json

## Response
200 OK 

**Headers**
- Content-Type: application/json

**Body**
```
{
  board_type_id: string,
  board_type_name: string,
  deck_type_ids: [string],
  space_type_ids: [string],
  hand_type_ids: [string]
  board_type_data: {}
}
```

# PUT updateBoardType

## URI
/boardTypes/{board_type_id}/update
/boardTypes/{board_type_id}

## Request
**Headers**
- Content-Type: application/json
- Accept: application/json

**Body**
```
{
  board_type_name: string | null,
  deck_type_ids: [string] | null,
  space_type_ids: [string] | null,
  hand_type_ids: [string] | null,
  board_type_data: {} | null
}
```

## Response
200 OK 

**Headers**
- Content-Type: application/json

**Body**
```
{
  board_type_id: string,
  board_type_name: string,
  deck_type_ids: [string],
  space_type_ids: [string],
  hand_type_ids: [string]
  board_type_data: {}
}
```

# PUT add{Deck/Space/Hand}

## URI
/boardTypes/{board_type_id}/add{Deck/Space/Hand}

## Request
**Headers**
- Content-Type: application/json
- Accept: application/json

**Body**
```
{
  {deck/space/hand}_type_id: string
}
```

## Response
200 OK 

**Headers**
- Content-Type: application/json

**Body**
```
{
  board_type_id: string,
  board_type_name: string,
  deck_type_ids: [string],
  space_type_ids: [string],
  hand_type_ids: [string]
  board_type_data: {}
}
```

# PUT add{Decks/Spaces/Hands}

## URI
/boardTypes/{board_type_id}/add{Decks/Spaces/Hands}

## Request
**Headers**
- Content-Type: application/json
- Accept: application/json

**Body**
```
{
  {deck/space/hand}_type_ids: [string]
}
```

## Response
200 OK 

**Headers**
- Content-Type: application/json

**Body**
```
{
  board_type_id: string,
  board_type_name: string,
  deck_type_ids: [string],
  space_type_ids: [string],
  hand_type_ids: [string]
  board_type_data: {}
}
```

# PUT remove{Deck/Space/Hand}

## URI
/boardTypes/{board_type_id}/remove{Deck/Space/Hand}

## Request
**Headers**
- Content-Type: application/json
- Accept: application/json

**Body**
```
{
  {deck/space/hand}_type_id: string
}
```

## Response
200 OK 

**Headers**
- Content-Type: application/json

**Body**
```
{
  board_type_id: string,
  board_type_name: string,
  deck_type_ids: [string],
  space_type_ids: [string],
  hand_type_ids: [string]
  board_type_data: {}
}
```

# PUT remove{Decks/Spaces/Hands}

## URI
/boardTypes/{board_type_id}/remove{Decks/Spaces/Hands}

## Request
**Headers**
- Content-Type: application/json
- Accept: application/json

**Body**
```
{
  {deck/space/hand}_type_ids: [string]
}
```

## Response
200 OK 

**Headers**
- Content-Type: application/json

**Body**
```
{
  board_type_id: string,
  board_type_name: string,
  deck_type_ids: [string],
  space_type_ids: [string],
  hand_type_ids: [string]
  board_type_data: {}
}
```

# DELETE deleteBoardType

## URI
/boardTypes/{board_type_id}/delete
/boardTypes/{board_type_id}

## Response
204 No Content

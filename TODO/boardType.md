# POST createBoardType

## URI
{game_type_id}/boards/create
{game_type_id}/boards

## Request
**Headers**
- Content-Type: application/json
- Accept: application/json

**Body**
```
{
  name: string | null,
  owner: 'global' | 'player' | '' | null,
  deck_type_ids: [string] | null,
  space_type_ids: [string] | null,
  hand_type_ids: [string] | null,
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
  owner: 'global' | 'player' | '' | null,
  deck_type_ids: [string],
  space_type_ids: [string],
  hand_type_ids: [string]
  data: {}
}
```

# GET getBoardTypes

may want to do some pagination for this and/or just return name and id if too long

## URI
{game_type_id}/boards/get
{game_type_id}/boards

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
    owner: 'global' | 'player' | '' | null,
    deck_type_ids: [string],
    space_type_ids: [string],
    hand_type_ids: [string]
    data: {}
  }, ...
]
```

# GET getBoardType

## URI
{game_type_id}/boards/{board_id}/get
{game_type_id}/boards/{board_id}

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
  owner: 'global' | 'player' | '' | null,
  deck_type_ids: [string],
  space_type_ids: [string],
  hand_type_ids: [string]
  data: {}
}
```

# PUT updateBoardType

## URI
{game_type_id}/boards/{board_id}/update
{game_type_id}/boards/{board_id}

## Request
**Headers**
- Content-Type: application/json
- Accept: application/json

**Body**
```
{
  name: string | null,
  owner: 'global' | 'player' | '' | null,
  deck_type_ids: [string] | null,
  space_type_ids: [string] | null,
  hand_type_ids: [string] | null,
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
  owner: 'global' | 'player' | '' | null,
  deck_type_ids: [string],
  space_type_ids: [string],
  hand_type_ids: [string]
  data: {}
}
```

# PUT add{Deck/Space/Hand}

## URI
{game_type_id}/boards/{board_id}/add{Deck/Space/Hand}

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
  id: string,
  name: string,
  owner: 'global' | 'player' | '' | null,
  deck_type_ids: [string],
  space_type_ids: [string],
  hand_type_ids: [string]
  data: {}
}
```

# PUT add{Decks/Spaces/Hands}

## URI
{game_type_id}/boards/{board_id}/add{Decks/Spaces/Hands}

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
  id: string,
  name: string,
  owner: 'global' | 'player' | '' | null,
  deck_type_ids: [string],
  space_type_ids: [string],
  hand_type_ids: [string]
  data: {}
}
```

# PUT remove{Deck/Space/Hand}

## URI
{game_type_id}/boards/{board_id}/remove{Deck/Space/Hand}

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
  id: string,
  name: string,
  owner: 'global' | 'player' | '' | null,
  deck_type_ids: [string],
  space_type_ids: [string],
  hand_type_ids: [string]
  data: {}
}
```

# PUT remove{Decks/Spaces/Hands}

## URI
{game_type_id}/boards/{board_id}/remove{Decks/Spaces/Hands}

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
  id: string,
  name: string,
  owner: 'global' | 'player' | '' | null
  deck_type_ids: [string],
  space_type_ids: [string],
  hand_type_ids: [string]
  data: {}
}
```

# DELETE deleteBoardType

## URI
{game_type_id}/boards/{board_id}/delete
{game_type_id}/boards/{board_id}

## Response
204 No Content
